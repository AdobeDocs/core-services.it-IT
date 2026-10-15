---
title: Instradare la raccolta dati tramite una rete CDN
description: Scopri come configurare una rete CDN (Content Delivery Network) per inoltrare le richieste di raccolta dati ad Adobe senza influire sulla qualità dei dati.
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# Instradare la raccolta dati tramite una rete CDN

Alcune organizzazioni indirizzano le richieste di raccolta dati tramite la propria rete CDN (Content Delivery Network) invece di inviarle direttamente ad Adobe. Motivi comuni includono la protezione del firewall dell’applicazione web (WAF), criteri aziendali che richiedono il passaggio di tutto il traffico del sito web attraverso una rete CDN e la possibilità di controllare il traffico inviato ad Adobe. La CDN riceve le richieste su un nome host di proprietà della tua organizzazione, quindi le inoltra a un nome host di raccolta dati di Adobe, denominato origine.

>[!IMPORTANT]
>
>Adobe non può rivedere o convalidare la configurazione CDN. La tua organizzazione e il provider CDN sono responsabili della corretta configurazione della CDN. Per assistenza nella configurazione della rete CDN, contatta il provider CDN. Una configurazione errata delle CDN può causare la perdita di dati.

## Scegli un tipo di origine {#origin-type}

| | Origine di terze parti (scelta consigliata) | Origine di prima parte |
| --- | --- | --- |
| **Nome host origine** | Il sottodominio dell&#39;ID tenant di `data.adobedc.net`, ad esempio `example.data.adobedc.net` | Il nome host di prime parti, ad esempio `data.example.com` |
| **Certificato sui server Adobe** | Certificato di Adobe (`*.data.adobedc.net`) | [Certificato gestito dal cliente](customer-managed-cert.md) |
| **Rinnovi certificato** | Nessuna richiesta | La tua organizzazione rinnova il certificato e lo fornisce ad Adobe prima di ogni scadenza |
| **Area bloccata [RDC](rdc.md)** | Non supportato | Supportato |
| **Quando utilizzare** | Tutte le implementazioni CDN, a meno che l’organizzazione non richieda un’origine di prima parte | I criteri di sicurezza richiedono il controllo diretto del certificato di origine oppure l&#39;organizzazione richiede un tipo di RDC bloccato per area |

>[!NOTE]
>
>Il [programma di certificazione gestito da Adobe](adobe-managed-cert.md) non supporta le implementazioni CDN. Adobe non può convalidare la proprietà del dominio o rinnovare i certificati per i nomi host che puntano alla tua rete CDN. Utilizza un&#39;origine di terze parti o un&#39;origine di prima parte con un [certificato gestito dal cliente](customer-managed-cert.md).

## Requisiti per tutte le implementazioni CDN {#requirements}

Le librerie di raccolta dati di Adobe, come AppMeasurement e Web SDK, includono tutto ciò che serve ad Adobe in ogni richiesta. Configura la tua CDN per inoltrare queste richieste ad Adobe senza modificarle.

>[!IMPORTANT]
>
>Non modificare mai l’endpoint o elementi che determinano la destinazione dei dati, incluso l’ID suite di rapporti (AppMeasurement) o l’ID dello stream di dati (Web SDK). La modifica di questi valori causa la perdita di dati.

La configurazione CDN deve:

* Inoltra il metodo di richiesta, il percorso URL, la stringa di query e il corpo senza modifiche.
* Lascia invariata l&#39;intestazione `Host`.
* Lascia invariato il dominio in cui sono impostati i cookie di Adobe.
* Mantieni tutti i cookie elencati nella [sezione cookie](cookies/overview.md) di questa guida.
* Aggiungi l&#39;intestazione `X-Forwarded-For` contenente l&#39;indirizzo IP del visitatore. Adobe utilizza questa intestazione per la geolocalizzazione. Senza di esso, i dati di geolocalizzazione riflettono la posizione dei server della rete CDN invece che i visitatori.
* Restituisci le risposte di Adobe al browser senza modifiche.

La configurazione CDN può:

* Rimuovi i cookie non utilizzati da Adobe, ad esempio i cookie di altri sistemi sul tuo sito. I cookie non correlati aggiungono un sovraccarico a ogni richiesta.
* Utilizza i servizi WAF, di filtro bot o di rimozione dei dati personali, purché non vengano apportate modifiche ai dati elencati sopra. Test di questi servizi con una suite di rapporti per lo sviluppo o uno stream di dati prima di applicarli al traffico di produzione. Un filtro eccessivamente aggressivo può rimuovere una quantità di dati sufficiente a rendere i rapporti inutilizzabili.

La configurazione CDN non deve:

* Memorizza nella cache le richieste o le risposte di raccolta dati. Ogni richiesta deve raggiungere Adobe.
* Puntare a un nome host di origine che non esiste.
* Accetta i certificati scaduti o fissane uno specifico dall’origine. Adobe non supporta la trasmissione di certificati scaduti e può rimuoverli in qualsiasi momento.

## Configurare una rete CDN con origine di terze parti {#third-party-origin}

Un’origine di terze parti utilizza il certificato proprio di Adobe, pertanto la tua organizzazione non deve mantenere un certificato sui server Adobe.

1. Trova l’ID tenant della tua organizzazione. Consulta [Trovare il tuo ID tenant](collection-domain.md#tenant-id).
1. Nella configurazione CDN, imposta il nome host di origine sul sottodominio dell&#39;ID tenant di `data.adobedc.net`. Ad esempio, `example.data.adobedc.net`.
1. Abilitare SNI (Server Name Indication) per l&#39;origine. Imposta il nome host SNI sul nome host di origine (ad esempio, `example.data.adobedc.net`), non sul nome host del tuo sito Web.
1. Configura la tua CDN in modo da soddisfare i [requisiti per tutte le implementazioni CDN](#requirements) di cui sopra.
1. Se il nome host inviato dall&#39;implementazione cambia, [aggiorna l&#39;implementazione](collection-domain.md#update-implementation). Se mantieni lo stesso nome host, non sono necessarie modifiche all’implementazione.

>[!WARNING]
>
>Non impostare l&#39;origine sul nome host fornito da Adobe come destinazione CNAME, ad esempio `hiodsibxvip01.data.adobedc.net`. Il nome host è associato al certificato di prima parte e può smettere di funzionare quando il certificato viene rimosso.

Le origini di terze parti utilizzano sempre il tipo predefinito [RDC](rdc.md), in modo che i dati possano essere raccolti in qualsiasi percorso di raccolta dati di Adobe.

## Configurare una rete CDN con origine di prime parti {#first-party-origin}

Utilizza un’origine di prima parte solo se l’organizzazione lo richiede. I motivi comuni includono:

* I criteri di sicurezza richiedono il controllo diretto del certificato di origine. Ad esempio, l’organizzazione deve essere in grado di revocare il certificato tramite la propria autorità di certificazione.
* La tua organizzazione richiede un tipo di [RDC](rdc.md) bloccato per area geografica.

1. Contatta l&#39;Assistenza clienti Adobe per configurare un [certificato gestito dal cliente](customer-managed-cert.md) per il nome host di prime parti, ad esempio `data.example.com`. Se l’organizzazione richiede un tipo di RDC bloccato per regione, specificalo nella richiesta.
1. Nella configurazione CDN, imposta il nome host di origine sul nome host di prima parte.
1. Abilitare SNI (Server Name Indication) per l&#39;origine. Imposta il nome host SNI sul nome host di prima parte e configura la rete CDN in modo che il certificato di prima parte arrivi dall’origine.
1. Configura la tua CDN in modo da soddisfare i [requisiti per tutte le implementazioni CDN](#requirements) di cui sopra.
1. Se il nome host inviato dall&#39;implementazione cambia, [aggiorna l&#39;implementazione](collection-domain.md#update-implementation). Se mantieni lo stesso nome host, non sono necessarie modifiche all’implementazione.

>[!IMPORTANT]
>
>La tua organizzazione è responsabile del rinnovo del certificato gestito dal cliente e della sua fornitura all’Assistenza clienti di Adobe prima della scadenza. Se il certificato sui server Adobe scade, la rete CDN può rifiutare la connessione ed eliminare i dati senza ricevere alcuna notifica. Consulta [Rinnovare il certificato](customer-managed-cert.md#renewals).

## Spostare un’implementazione di prima parte esistente in una rete CDN {#migrate}

Se al momento la tua organizzazione invia i dati direttamente a un nome host di prima parte con un certificato ospitato da Adobe, procedi come segue per passare a una rete CDN:

1. Identifica ogni implementazione che invia dati al nome host di prime parti, in tutti i prodotti Adobe. Altri prodotti, come Adobe Target o Adobe Journey Optimizer, potrebbero utilizzare lo stesso nome host e un singolo certificato può coprire molti nomi host.
1. Scegli un [tipo di origine](#origin-type). Se scegli un&#39;origine di prima parte, contatta l&#39;Assistenza clienti Adobe per convertire il certificato in [certificato gestito dal cliente](customer-managed-cert.md) prima della scadenza.
1. Configura la tua CDN. Mantieni il nome host esistente in modo da non dover aggiornare le implementazioni.
1. Prima della scadenza del certificato, punta il nome host alla tua CDN e cambia tutte le implementazioni in modo da utilizzarlo.
1. [Verifica i dati](#check).
1. Se hai scelto un’origine di terze parti, contatta l’Assistenza clienti di Adobe per contrassegnare il certificato di prima parte per la rimozione.

Una volta che il nome host punta alla rete CDN, Adobe non può rinnovare il certificato di prime parti. Se un’implementazione si basa ancora sul certificato quando scade, i dati di tale implementazione andranno persi. Contattare l’Assistenza clienti di Adobe consente all’organizzazione di controllare quando il certificato viene rimosso.

## Verifica i dati {#check}

Adobe non può convalidare la configurazione CDN. Dopo aver indirizzato la raccolta dati tramite la rete CDN, confronta i dati prima e dopo la modifica:

* I dati continuano a pervenire nelle suite di rapporti, negli stream di dati o nei set di dati previsti al volume usuale.
* I rapporti di geolocalizzazione mostrano le posizioni dei visitatori, non un numero limitato di città in cui si trovano i server della rete CDN.
* Il numero di visitatori univoci non aumenta in modo imprevisto.
* Negli strumenti per sviluppatori del browser, le richieste di raccolta dati al nome host hanno esito positivo e i cookie di Adobe sono impostati sullo stesso dominio di prima.

## Configurazioni errate comuni

È noto che i seguenti problemi causano problemi di qualità dei dati o perdita di dati. Questo elenco non è esaustivo.

| Sintomo | Probabile causa |
| --- | --- |
| I dati non arrivano più in una suite di rapporti o in uno stream di dati | La rete CDN modifica l’URL della richiesta oppure il nome host di origine non esiste |
| I dati non arrivano più dopo la scadenza di un certificato | Il CDN richiede un certificato di prima parte dall’origine e tale certificato è scaduto |
| I dati di geolocalizzazione mostrano solo alcune città | Il CDN non aggiunge l&#39;intestazione `X-Forwarded-For` |
| Il numero di visitatori univoci aumenta in modo imprevisto | La rete CDN rimuove i cookie di Adobe, modifica l&#39;intestazione `Host` o modifica il dominio dei cookie |
| Nei rapporti mancano grandi quantità di dati | La rimozione di dati personali o le regole di WAF rimuovono una quantità eccessiva di ogni richiesta |

## Domande frequenti

+++Questa pagina si applica a prodotti diversi da Adobe Analytics?

Sì. Questa pagina si applica a tutti i prodotti Adobe che utilizzano la raccolta dati di Adobe, inclusi Customer Journey Analytics, Adobe Experience Platform, Adobe Target e Adobe Journey Optimizer.

+++

+++Adobe può rifiutare dati che non provengono dalla mia rete CDN?

No. Al momento Adobe non offre un modo per limitare la raccolta dei dati alle richieste provenienti dalla rete CDN.

+++

+++Adobe può fornire o convalidare una configurazione per la mia rete CDN?

No. Le opzioni di configurazione CDN variano da provider a provider e cambiano nel tempo. Contatta il provider CDN per assistenza nella configurazione della rete CDN e consulta [Controlla i tuoi dati](#check) per scoprire come identificare i problemi nella configurazione.

+++
