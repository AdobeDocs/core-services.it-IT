---
description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
keywords: cookies;privacy
seo-description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
seo-title: Cookie di prime parti
solution: Experience Cloud,Analytics
title: Cookie di prime parti
index: y
snippet: y
translation-type: tm+mt
source-git-commit: c8d38647750747212c2b825feff600419c1f3352
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 96%

---


# Informazioni sui cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Questi cookie inoffensivi provengono da un dominio ospitato da Adobe e sono chiamati cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti, inclusi quelli utilizzati nella raccolta dati di Analytics. Per supportare il tracciamento della modalità di interazione dei visitatori con il tuo sito web, puoi implementare i cookie di prime parti.

Per implementare i cookie di prime parti sono disponibili due opzioni:

* Servizio ID di Experience Platform. Il servizio ID può impostare il cookie nella prima parte utilizzando JavaScript.
* Le voci DNS nel server DNS della società per configurare un alias CNAME in un dominio ospitato da Adobe. Sebbene diversi prodotti Adobe supportino l’uso di un CNAME, in tutti i casi questo viene utilizzato per creare un endpoint di prima parte affidabile per un cliente specifico e rimane di proprietà di tale cliente. Se il cliente controlla più domini, può sfruttare un singolo endpoint CNAME per monitorare gli utenti nei loro domini, ma poiché questo richiede l’uso di cookie di terze parti per tutti i domini al di fuori di quello specifico di CNAME, l’endpoint non funzionerà se i cookie di terze parti sono bloccati e pertanto non è consigliato. I CNAME Adobe non vengono mai utilizzati per monitorare un singolo o un dispositivo tra domini diversi che sono di proprietà di clienti differenti.

Persino quando si utilizza la prima opzione con il servizio Experience Cloud ID, l’ITP di Apple renderà di breve durata i cookie di prime parti, dunque è preferibile utilizzarlo con la seconda opzione.

Per la seconda opzione che utilizza un CNAME, se il tuo sito dispone di pagine sicure con protocollo HTTPS, puoi lavorare con Adobe per ottenere un certificato SSL che ti consenta di implementare i cookie di prime parti. Adobe consiglia vivamente di utilizzare esclusivamente HTTPS per la raccolta dei dati, in quanto il supporto per la raccolta HTTP verrà eliminato nella seconda metà del 2020.

Spesso il processo di rilascio del certificato SSL crea confusione e richiede tempo. Di conseguenza, Adobe ha stabilito una partnership con DigiCert, un’autorità di certificazione (CA) leader del settore, e ha sviluppato un processo integrato per automatizzare l’acquisto e la gestione di tali certificati.

Con la tua autorizzazione, collaboreremo con la nostra CA per rilasciare, distribuire e gestire un nuovo certificato SSL SHA-2 per tuo conto. Adobe continuerà a gestire questo certificato e farà in modo che, in caso di scadenza, revoca o problemi di sicurezza imprevisti, la raccolta sicura delle organizzazioni non venga compromessa.

## Programma di certificazione gestito di Adobe

Il programma di certificazione gestito di Adobe è il processo consigliato per l’implementazione di un nuovo certificato SSL di prima parte per i cookie di prime parti.

Il programma Adobe Managed Certificate consente di implementare un nuovo certificato SSL di prima parte per i cookie di prime parti senza costi aggiuntivi (per i primi 100 CNAME). Se al momento disponi di un tuo certificato SSL gestito dal cliente, chiama l’Assistenza clienti Adobe per informazioni su come effettuare la migrazione al programma di certificazione gestito di Adobe.

### Implementazione

Per implementare un nuovo certificato SSL di prima parte per i cookie di prime parti:

1. Compila il [modulo di richiesta dei cookie di prime parti](/help/interface/cookies/assets/FPC_Request_Form.xlsx) e apri un ticket con l’Assistenza clienti per richiedere la configurazione dei cookie di prime parti nel programma gestito da Adobe. Ogni campo è descritto all’interno del documento con esempi.

1. Crea record CNAME (consulta le istruzioni riportate di seguito).

   Quando ricevi il ticket, un rappresentante dell’assistenza clienti ti fornirà una coppia di record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. I CNAME avranno un aspetto simile a quanto segue:

   **Protetto**: ad esempio, il nome host `smetrics.example.com` punta a: `example.com.ssl.d1.omtrdc.net`.

   **Non protetto**: ad esempio, il nome host `metrics.example.com` punta a: `example.com.d1.omtrdc.net`.

1. Quando questi CNAME diventano attivi, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di produzione di Adobe.

   Se disponi già di un’implementazione, prendi in considerazione Migrazione visitatori per mantenere i visitatori esistenti. Dopo il push live del certificato all’ambiente di produzione di Adobe, potrai aggiornare le variabili del server di tracciamento con i nuovi nomi host. Ciò significa che, se il sito non è protetto (HTTP), devi aggiornare `s.trackingServer`. Se il sito è protetto (HTTPS), aggiorna sia la variabile `s.trackingServer` che la variabile `s.trackingServerSecure`.

1. [Convalida dell’inoltro nome host](#validate) (vedi di seguito).

1. [Aggiorna il codice di implementazione](#update) (vedi di seguito).

### Manutenzione e rinnovi

I certificati SSL scadono ogni anno, il che significa che Adobe deve acquistare un nuovo certificato per ogni implementazione su base annua. Tutti gli utenti supportati all’interno dell’organizzazione riceveranno una notifica e-mail ogni volta che un’implementazione è vicina alla scadenza. Affinché Adobe possa rinnovare il tuo nome host, un utente supportato deve rispondere all’e-mail inviata da Adobe e indicare che intendi continuare a utilizzare il nome host in scadenza per la raccolta dei dati. A questo punto, Adobe acquisterà e installerà automaticamente un nuovo certificato.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito da Adobe è più sicuro del metodo legacy, in quanto nessun certificato o chiave privata vengono trasmessi al di fuori di Adobe e dell’autorità di certificazione emittente. |
| **In che modo Adobe può acquistare un certificato per il mio dominio?** | The certificate can only be purchased when you have pointed the specified hostname (for example, `smetrics.example.com`) to an Adobe owned hostname. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato a tuo nome. |
| **Posso richiedere la revoca del certificato?** | Sì, come proprietario del dominio, hai diritto di richiedere la revoca del certificato. Per completare il processo, dovrai solo aprire un ticket con l’Assistenza clienti. |
| **Il certificato utilizzerà la cifratura SHA-2?** | Sì, Adobe collaborerà con DigiCert per emettere un certificato SHA-2. |
| **Sono previsti costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti attuali di Analytics senza costi aggiuntivi. |

## Creazione di record CNAME

Il team che gestisce la rete della tua organizzazione deve configurare i server DNS creando nuovi record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC fornisce i nomi host configurati e i CNAME a cui devono essere puntati. Ad esempio:

* **Nome host SSL**:`smetrics.mysite.com`
* **CNAME SSL**:`mysite.com.ssl.sc.omtrdc.net`
* **Nome host non SSL**:`metrics.mysite.com`
* **CNAME non SSL**:`mysite.com.sc.omtrdc.net`

Fintanto che il codice di implementazione non viene modificato, questo passaggio non influisce sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l’aggiornamento del codice di implementazione.

>[!Nota:]
>
>Il servizio ID visitatori di Experience Cloud fornisce un’alternativa alla configurazione di un CNAME per abilitare i cookie di prime parti. Tuttavia, a causa delle recenti modifiche dell’ITP Apple, è comunque consigliabile allocare un CNAME persino quando si utilizza il servizio Experience Cloud ID.

## Convalida dell’inoltro nome host {#validate}

Per la convalida sono disponibili i seguenti metodi:

### Convalida tramite browser

Se hai configurato un CNAME e hai installato il certificato, puoi utilizzare il browser per la convalida:

`https://sstats.adobe.com/_check`

>[!Nota:]
>
>Se non è installato un certificato, verrà visualizzato un avviso di protezione.

### Convalida tramite [!DNL curl]

Adobe consiglia di utilizzare [!DNL [curl](https://curl.haxx.se/)] dalla riga di comando. Gli utenti [!DNL Windows] possono eseguire l’installazione di [!DNL curl] da: <https://curl.haxx.se/windows/>

Se disponi di un CNAME ma non è installato alcun certificato, esegui:
`curl -k https://sstats.adobe.com/_check`
Risposta: `SUCCESS`

Il valore `-k` disattiva l’avviso di protezione.

Se hai configurato un CNAME e il certificato è installato, esegui:
`curl https://sstats.adobe.com/_check`
Risposta: `SUCCESS`

### Convalida tramite [!DNL nslookup]

È possibile utilizzare `nslookup` per la convalida. Utilizzando `sstats.adobe.com`come esempio, apri un prompt dei comandi e digita `nslookup sstats.adobe.com`

Se tutto è configurato correttamente, verrà visualizzata una restituzione simile a:

```
nslookup sstats.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

sstats.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## Aggiorna il codice di implementazione {#update}

Prima di modificare il codice sul sito per utilizzare i cookie di prime parti, completa i seguenti prerequisiti:

* Richiedi un certificato SSL seguendo i passaggi descritti in precedenza nella sezione *Implementa* del [Programma di certificazione gestito di Adobe](#adobe-managed-certificate-program).
* Crea record CNAME (vedi sopra).
* Convalida i nomi host (vedi sopra).

Dopo aver verificato che i nomi host rispondano e trasmettano ai server di raccolta dati di Adobe, puoi modificare l’implementazione in modo che punti ai nomi host della tua raccolta dati.

1. Apri il tuo file JavaScript di base (`s_code.js/AppMeasurement.js`).
1. Se vuoi aggiornare la versione del codice, sostituisci l’intero file `s_code.js/AppMeasurement.js` con la versione più recente e sostituisci eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo per i cookie di prime parti, individua le variabili s.trackingServer e s.trackingServerSecure (se utilizzi SSL) e puntale ai nuovi nomi host della tua raccolta dati. Usiamo ilmiosito.com come esempio:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Carica il file JavaScript di base aggiornato sul sito.

1. Se stai passando ai cookie di prime parti da un’implementazione di lunga data o a un nome host di raccolta di prima parte diverso, ti consigliamo di migrare i visitatori dal dominio precedente al nuovo.

Consulta la sezione [Migrazione dei visitatori](https://docs.adobe.com/content/help/it-IT/analytics/technotes/visitor-identification.html) nella Guida all’implementazione di Analytics.

Dopo che hai caricato il file JavaScript, tutto è configurato per la raccolta dati di cookie di prime parti. Per le prime ore, ti consigliamo di monitorare i report di Analytics per verificare che la raccolta dei dati continui come previsto. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e fai contattare l’Assistenza clienti da uno degli utenti supportati dalla tua organizzazione.
