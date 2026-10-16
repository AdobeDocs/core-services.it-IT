---
description: Scopri come impostare certificati protetti da utilizzare con i cookie di prime parti di Adobe CX Enterprise.
solution: Experience Cloud,Analytics
title: Programma di certificazione gestito da Adobe
index: true
snippet: 'y'
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
autotag-review: '2026-09-09T20:12:24.943Z'
TQID: 'https://experienceleague.adobe.com/8CSBLQaw3KOByyxxCYr1By4gyAQsDIhiofOdAzn38dg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 2%
---
# Programma di certificazione gestito da Adobe

Il programma di certificazione gestito da Adobe è il processo consigliato per la configurazione dei certificati di prime parti necessari per un’implementazione CNAME. Una volta configurato, il programma è completamente automatizzato. I certificati vengono rinnovati in modo tempestivo, in modo da non influire sulla raccolta dei dati a causa di certificati scaduti. Il programma è gratuito per i primi 100 CNAME.

Il programma di certificazione gestito da Adobe non supporta l’instradamento della raccolta dati tramite una rete CDN (Content Delivery Network). Se utilizzi una rete CDN, vedi [Instradare la raccolta dati tramite una rete CDN](cdn.md). Le organizzazioni che devono gestire i propri certificati possono utilizzare invece [certificati gestiti dal cliente](customer-managed-cert.md). Se al momento gestisci i tuoi certificati e desideri passare al programma di certificazione gestito da Adobe, contatta l’Assistenza clienti di Adobe.

## Implementazione

Per implementare un nuovo certificato per la raccolta dati di prime parti, effettua le seguenti operazioni:

1. Scarica e compila il [modulo di richiesta per dominio di prime parti](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Apri un ticket con l’Assistenza clienti di Adobe per richiedere la configurazione della raccolta dati di prime parti nel programma di certificazione gestito da Adobe. Se la tua organizzazione ha requisiti di residenza dei dati o conformità, specifica il tipo di [RDC](rdc.md) desiderato nella richiesta.
1. Quando ricevi il ticket, il rappresentante di Adobe ti fornisce un record CNAME. Questo record deve essere configurato sul server DNS della tua azienda prima che Adobe possa acquistare il certificato per tuo conto. Ad esempio, il nome host `data.example.com` punta a `hiodsibxvip01.data.adobedc.net`. Se l&#39;organizzazione utilizza i record CAA (Certificate Authority Authorization) DNS, assicurarsi che i record CAA consentano a DigiCert di rilasciare certificati. Consulta [Manutenzione e rinnovi](#renewals).
1. Quando il record CNAME è presente sui server dell’organizzazione, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di raccolta dati di Adobe.
1. Se hai bisogno di un aggiornamento del file `robots.txt` quando è in hosting da Adobe CNAME per scopi di prime parti, contatta l&#39;Assistenza clienti con una richiesta. Tale richiesta è rilevante quando si desidera aggiornare il file `robots.txt` per impedire a Google di scansionare i sottodomini.

## Convalida dell’inoltro nome host

Una volta installato il certificato, Adobe può utilizzare uno dei seguenti metodi per verificare che funzioni.

+++**Convalida browser**

Puoi utilizzare qualsiasi browser per verificare che un certificato sia installato correttamente. Digita il tuo CNAME con `_check` come percorso nella barra degli indirizzi. Ad esempio:

`data.example.com/_check`

Se tutto funziona, nel browser viene visualizzato `SUCCESS`. Se il certificato non è installato correttamente, viene visualizzato un avviso di protezione.

+++

+++**Riga di comando (`curl`)**

Nella maggior parte dei sistemi operativi moderni è già installato [`curl`](https://curl.se).

Digitare quanto segue nella riga di comando:

```sh
curl data.example.com/_check
```

Se tutto funziona correttamente, la console restituisce `SUCCESS`.

>[!TIP]
>
>È possibile utilizzare il flag `-k` per disabilitare l&#39;avviso di protezione per facilitare la risoluzione dei problemi.

+++

+++**Riga di comando (`nslookup`)**

Digitare quanto segue nella riga di comando:

```sh
nslookup data.example.com
```

Se tutto funziona correttamente, vengono restituiti i server di raccolta dati di Adobe:

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: data.example.com
```

+++

## Aggiorna il codice di implementazione

Per utilizzare il nuovo nome host CNAME, aggiorna l’implementazione di Adobe dopo aver verificato il corretto funzionamento del certificato. Consulta [Aggiornare la tua implementazione](collection-domain.md#update-implementation).

## Manutenzione e rinnovi {#renewals}

Adobe rinnova automaticamente il certificato. Trenta giorni prima della scadenza del certificato, Adobe verifica che il CNAME sia ancora valido e in uso, quindi rinnova il certificato per tuo conto. Per mantenere attivi i rinnovi, evita le seguenti modifiche DNS:

* **Rimozione o riposizionamento del record CNAME**: se il record CNAME viene rimosso o non punta più al nome host sicuro di Adobe, Adobe non può rinnovare il certificato. Questa condizione include il puntamento del record CNAME a una rete di distribuzione di contenuti (CDN, Content Delivery Network). Se prevedi di utilizzare una rete CDN, consulta [Spostare un&#39;implementazione di prima parte esistente in una rete CDN](cdn.md#migrate) prima di modificare i tuoi record DNS.
* **Aggiunta di record CAA che non autorizzano DigiCert**: le autorità di certificazione verificano i record CAA (Certificate Authority Authorization) nel nome host e nei domini padre. Se si utilizzano i record CAA, includere `digicert.com` come autorità di certificazione autorizzata. Ad esempio, `example.com. IN CAA 0 issue "digicert.com"`.
* **Limitazione dell&#39;emissione di DigiCert a un account specifico**: la funzionalità di blocco del dominio di DigiCert aggiunge un parametro `account=` a un record CAA, ad esempio `example.com. IN CAA 0 issue "digicert.com; account=<token>"`. Questo parametro limita l&#39;emissione all&#39;account DigiCert della tua organizzazione, anche se `digicert.com` è autorizzato, impedendo ad Adobe di ottenere un certificato. Se l&#39;organizzazione richiede il blocco del dominio DigiCert, utilizzare invece [certificati gestiti dal cliente](customer-managed-cert.md). I blocchi di dominio impostati nel programma di registrazione del dominio, talvolta denominati blocchi di trasferimento, non sono correlati e non influiscono sui certificati gestiti da Adobe.

>[!IMPORTANT]
>
>Se il record CNAME non punta più al nome host sicuro di Adobe, la voce nel sistema di Adobe viene contrassegnata per la rimozione senza ulteriori comunicazioni.

## Domande frequenti

+++Il processo è sicuro?

Sì. Il programma di certificazione gestito da Adobe è più sicuro di [certificati gestiti dal cliente](customer-managed-cert.md). Nessun certificato o chiave privata viene trasferito al di fuori di Adobe e dell’autorità di certificazione emittente.

+++

+++In che modo Adobe può acquistare un certificato per il nostro dominio?

Il certificato può essere acquistato solo dopo aver puntato il nome host specificato su un nome host di proprietà di Adobe. Delega questo nome host ad Adobe e consenti ad Adobe di acquistare il certificato per tuo conto.

+++

+++Posso richiedere la revoca del certificato?

Sì. In qualità di proprietario del dominio, hai il diritto di richiedere la revoca del certificato. Per avviare questo processo, contatta l’Assistenza clienti di Adobe.

+++

+++Quale tipo di crittografia viene utilizzato?

Adobe collabora con DigiCert per rilasciare un certificato SHA-2.

+++

+++Il programma comporta costi aggiuntivi?

Adobe offre questo programma a tutti i clienti Adobe CX Enterprise senza costi aggiuntivi per i primi 100 CNAME.

+++

+++Quali livelli di sicurezza con crittografia offre Adobe?

Adobe offre due livelli di sicurezza crittografati per soddisfare le diverse esigenze dei clienti in materia di sicurezza nella raccolta dati di prime parti. Questi livelli determinano gli algoritmi di crittografia supportati per le connessioni HTTPS con i server Adobe. Adobe rivede e aggiorna regolarmente il set di algoritmi supportati in base alle procedure di sicurezza correnti. Per modificare le impostazioni di protezione crittografata, contatta l’Assistenza clienti.

* **Standard** richiede la crittografia TLS 1.2 o successiva e almeno a 128 bit. È progettato per garantire la massima compatibilità con i dispositivi, mantenendo al contempo la crittografia sicura.
* **Alta** richiede TLS 1.2 o versione successiva e rimuove il supporto per le crittografie più deboli. È progettato per i clienti che desiderano la crittografia più avanzata. I client rilasciati prima del 2015 in genere non possono connettersi quando la protezione crittografata è impostata su **Elevata**.

+++

+++Quali tipi di certificato HTTPS sono supportati?

Adobe supporta sia i certificati RSA che i certificati ECC e i client moderni supportano entrambi i tipi di certificato. I certificati ECC richiedono una minore elaborazione sia sul server che sul client. Per i certificati gestiti da Adobe, Adobe fornisce certificati RSA e ECC. Per [certificati gestiti dal cliente](customer-managed-cert.md), è necessario RSA e si consiglia ECC.

+++

