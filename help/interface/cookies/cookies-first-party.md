---
description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
keywords: cookie;privacy
seo-description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
seo-title: Cookie di prime parti
solution: Experience Cloud, Analytics
title: Cookie di prime parti
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 012283d79bda42f9dabb20b25903927b075f6d54

---


# Informazioni sui cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Questi cookie inoffensivi provengono da un dominio ospitato da Adobe e sono chiamati cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti, inclusi quelli utilizzati nella raccolta dati di Analytics. Per aggirare i limiti di tracciamento imposti dai browser e dai programmi, puoi implementare cookie di primr parti.

Per implementare i cookie di prime parti sono disponibili due opzioni

* Servizio ID di Experience Platform. Il servizio ID può impostare il cookie nella prima parte utilizzando JavaScript.
* Voci DNS nel server DNS delle aziende.
* Se il tuo sito contiene pagine sicure che utilizzano il protocollo `https:` e non utilizzi il servizio ID di Experience Platform, puoi lavorare con Adobe in modo da ottenere un certificato SSL per implementare i cookie di prime parti

Spesso il processo di rilascio del certificato SSL crea confusione e richiede tempo. Di conseguenza, Adobe ha stabilito una partnership con DigiCert, un’autorità di certificazione (CA) leader del settore, e ha sviluppato un processo integrato per automatizzare l’acquisto e la gestione di tali certificati.

Con la tua autorizzazione, collaboreremo con la nostra CA per rilasciare, distribuire e gestire un nuovo certificato SSL SHA-2 per tuo conto. Adobe continuerà a gestire questo certificato e farà in modo che, in caso di scadenza, revoca o problemi di sicurezza imprevisti, la raccolta sicura delle organizzazioni non venga compromessa.

## Programma di certificazione gestito di Adobe

Il programma di certificazione gestito di Adobe è il processo consigliato per l’implementazione di un nuovo certificato SSL di prima parte per i cookie di prime parti.

Il programma di certificazione gestito di Adobe consente di implementare un nuovo certificato SSL di prima parte per i cookie dei siti Web visualizzati senza nessun costo aggiuntivo. Se al momento disponi di un tuo certificato SSL gestito dal cliente, chiama l’Assistenza clienti Adobe per informazioni su come effettuare la migrazione al programma di certificazione gestito di Adobe.

### Implementazione

Per implementare un nuovo certificato SSL di prima parte per i cookie di prime parti:

1. Compila il [modulo di richiesta dei cookie di prime parti](/help/interface/cookies/assets/FPC_Request_Form.xlsx) e apri un ticket con l’Assistenza clienti per richiedere la configurazione dei cookie di prime parti nel programma gestito da Adobe. Ogni campo è descritto all’interno del documento con esempi.

1. Crea record CNAME (consulta le istruzioni di seguito). Dopo aver ricevuto il biglietto, un rappresentante dell'assistenza clienti dovrebbe fornirvi un paio di record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. I CNAME saranno simili ai seguenti: **Protetto**: ad esempio, il nome host `smetrics.example.com` punta a: `example.com.ssl.d1.omtrdc.net`. **Non protetto**: ad esempio, il nome host `metrics.example.com` punta a: `example.com.d1.omtrdc.net`.

1. Quando questi CNAME diventano attivi, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di produzione di Adobe. Se hai già un’implementazione, prendi in considerazione Migrazione visitatori per mantenere i visitatori esistenti. Dopo il push live del certificato all’ambiente di produzione di Adobe, potrai aggiornare le variabili del server di tracciamento con i nuovi nomi host. Ciò significa che, se il sito non è protetto (http), devi aggiornare `s.trackingServer`. Se il sito è protetto (https), aggiorna sia la variabile `s.trackingServer` che la variabile `s.trackingServerSecure`.

1. Effettua il ping dell’host (vedi di seguito).

1. Aggiorna il codice di implementazione (vedi di seguito).

### Manutenzione e rinnovi

I certificati SSL scadono ogni anno, il che significa che Adobe deve acquistare un nuovo certificato per ogni implementazione su base annua. Tutti gli utenti supportati all’interno dell’organizzazione riceveranno una notifica e-mail ogni volta che un’implementazione è vicina alla scadenza. Affinché Adobe possa rinnovare il tuo nome host, un utente supportato dovrà rispondere all’e-mail inviata da Adobe e indicare che intendi continuare a utilizzare il nome host in scadenza per la raccolta dei dati. A questo punto, Adobe acquisterà e installerà automaticamente un nuovo certificato.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito da Adobe è più sicuro del metodo legacy, in quanto nessun certificato o chiave privata vengono trasmessi al di fuori di Adobe e dell’autorità di certificazione emittente. |
| **In che modo Adobe può acquistare un certificato per il mio dominio?** | Il certificato può essere acquistato solo se hai puntato il nome host specificato (ad esempio, smetriche.esempio.com) su un nome host di proprietà di Adobe. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato a tuo nome. |
| **Posso richiedere la revoca del certificato?** | Sì, come proprietario del dominio, hai diritto di richiedere la revoca del certificato. Per completare il processo, dovrai solo aprire un ticket con l’Assistenza clienti. |
| **Il certificato utilizzerà la cifratura SHA-2?** | Sì, Adobe collaborerà con DigiCert per emettere un certificato SHA-2. |
| **Sono previsti costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti correnti di Analytics senza costi aggiuntivi. |

## Creazione di record CNAME

Il team che gestisce la rete della tua organizzazione deve configurare i server DNS creando nuovi record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC fornisce i nomi host configurati e i CNAME a cui devono essere puntati. Ad esempio:

* **Nome host SSL**:`smetrics.mysite.com`
* **CNAME SSL**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **Nome host non SSL**:`metrics.mysite.com`
* **CNAME non SSL**:`mysite.com.d1.sc.omtrdc.net`

Fintanto che il codice di implementazione non viene modificato, questo passaggio non influisce sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l’aggiornamento del codice di implementazione.

>[!Nota:] il servizio ID visitatore di Experience Cloud fornisce un’alternativa alla configurazione di un CNAME per abilitare i cookie di prime parti.

## Ping del nome host

Esegui il ping del nome host per assicurarti che l’inoltro venga completato correttamente. Tutti i nomi host devono rispondere a un ping per evitare la perdita di dati.

Una volta configurati correttamente i record CNAME e dopo che Adobe ha confermato l’installazione del certificato, apri un prompt dei comandi ed effettua il ping dei tuoi nomi host. Usando `mysite.com` come esempio: `ping metrics.mysite.com`

Se tutto è stato impostato correttamente, restituirà un risultato simile a questo:

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

Se i record CNAME non sono impostati correttamente o non sono attivi, restituirà quanto segue:

`Ping request could not find the host. Please check the name and try again.`

>[!Nota:] se utilizzi `https:// protocol`, il ping risponderà solo dopo la data di caricamento specificata dallo specialista FPC. Inoltre, assicurati di effettuare il ping del nome host protetto e di quello non-protetto per garantire che entrambi funzionino correttamente prima di aggiornare l’implementazione.

## Aggiorna il codice di implementazione

Prima di modificare il codice sul sito per utilizzare i cookie di prime parti, completa i seguenti prerequisiti:

* Richiedi un certificato SSL come descritto in precedenza nei passaggi di implementazione per il programma di certificazione gestito di Adobe.
* Crea record CNAME (vedi sopra).
* Effettua il ping del nome host (vedi sopra).

Dopo aver verificato che i nomi host rispondano e trasmettano ai server di raccolta dati di Adobe, puoi modificare l’implementazione in modo che punti ai nomi host della tua raccolta dati.

1. Apri il tuo file JavaScript di base (`s_code.js/AppMeasurement.js`).
1. Se vuoi aggiornare la versione del codice, sostituisci l’intero file `s_code.js/AppMeasurement.js` con la versione più recente e sostituisci eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo per i cookie di prime parti, individua le variabili s.trackingServer e s.trackingServerSecure (se utilizzi SSL) e puntale ai nuovi nomi host della tua raccolta dati. Usiamo ilmiosito.com come esempio:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Carica il file JavaScript di base aggiornato sul sito.

1. Se stai passando ai cookie di prime parti da un’implementazione di lunga data o a un nome host di raccolta di prima parte diverso, ti consigliamo di migrare i visitatori dal dominio precedente al nuovo.

Consulta Migrazione [dei](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) visitatori nella Guida all'implementazione di Analytics.

Dopo che hai caricato il file JavaScript, tutto è configurato per la raccolta dati di cookie di prime parti. Per le prime ore, ti consigliamo di monitorare i report di Analytics per verificare che la raccolta dei dati continui come previsto. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e fai contattare l’Assistenza clienti da uno degli utenti supportati dalla tua organizzazione.
