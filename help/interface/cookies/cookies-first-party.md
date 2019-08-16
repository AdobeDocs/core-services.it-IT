---
description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
keywords: cookie; privacy
seo-description: Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
seo-title: della documentazione di prodotto
solution: Experience Cloud, Analytics
title: della documentazione di prodotto
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# I cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Questi cookie inoffensivi provengono da un dominio ospitato da Adobe, noto come cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti, inclusi quelli utilizzati nella raccolta dati di Analytics. Per aggirare i limiti di tracciamento imposti dai browser e dai programmi, potete implementare cookie di prime parti.

Sono disponibili due opzioni per implementare i cookie di prime parti

* Servizio ID della piattaforma Experience. Il servizio ID può impostare il cookie nel contesto di prime parti utilizzando javascript.
* Voci DNS nel server DNS delle aziende.
* Se il tuo sito contiene pagine sicure utilizzando il `https:` protocollo e non utilizzi il servizio ID piattaforma Experience Platform, puoi lavorare con Adobe per ottenere un certificato SSL per implementare i cookie di prime parti

Il processo di rilascio dei certificati SSL può spesso essere confusione e dispendioso tempo. Di conseguenza, Adobe ha stabilito una partnership con digicert, un'importante autorità di certificazione (CA), e ha sviluppato un processo integrato tramite il quale l'acquisto e la gestione di tali certificati vengono automatizzati.

Con la vostra autorizzazione, collaboreremo con la nostra CA per rilasciare, implementare e gestire un nuovo certificato SHA -2 SSL per voi. Adobe continuerà a gestire questo certificato e assicura che una scadenza, una revoca o un'importanza di sicurezza imprevista non comprometta la disponibilità delle organizzazioni sicure.

## Programma di certificazione gestito di Adobe

Il programma di certificazione gestito di Adobe è il processo consigliato per l'implementazione di un nuovo certificato SSL di prime parti per i cookie di prime parti.

Il programma di certificazione gestito di Adobe consente di implementare un nuovo certificato SSL di prime parti per i cookie di prime parti senza costi aggiuntivi. Se al momento disponete del vostro certificato SSL gestito dal cliente, parlate con l'Assistenza clienti Adobe sulla migrazione al programma di certificazione gestito di Adobe.

### Implementate

Ecco come implementare un nuovo certificato SSL di prime parti per i cookie di prime parti:

1. Compila il modulo ![di richiesta](assets/FPC_Request_Form.xlsx) e apri un ticket con l'Assistenza clienti richiesta di configurare cookie di prime parti nel programma gestito da Adobe. Ogni campo è descritto all'interno del documento con esempi.

1. Creare record CNAME (consultate le istruzioni di seguito). Quando ricevi il ticket, uno specialista FPSSL deve fornire una coppia di record CNAME. Questi record devono essere configurati sul server DNS della tua azienda prima che Adobe possa acquistare il certificato per conto tuo. I CNAME saranno simili a quelli seguenti.

* **Protetto** : ad esempio, il nome host `smetrics.example.com` punta a: `example.com.ssl.d1.omtrdc.net`.
* **Non protetto** : ad esempio, il nome host `metrics.example.com` punta a: `example.com.d1.omtrdc.net`.

1. Quando questi CNAME saranno attivi, Adobe collaborerà con digicert per acquistare e installare un certificato sui server di produzione di Adobe. Se hai un'implementazione esistente, prendi in considerazione la migrazione dei visitatori per mantenere i visitatori esistenti. Dopo che il certificato è stato inviato in diretta nell'ambiente di produzione di Adobe, potrai aggiornare le variabili del server di tracciamento ai nuovi nomi host. Ciò significa che se il sito non è sicuro (https), aggiorna l ' `s.trackingServer`. Se il sito è protetto (https), aggiornate entrambe `s.trackingServer` le `s.trackingServerSecure` variabili.

1. Ping the host (nomehost) (vedere di seguito).

1. Aggiorna codice di implementazione (vedi di seguito).

### Manutenzione e rinnovi

I certificati SSL scadono ogni anno, il che significa che Adobe deve acquistare un nuovo certificato per ogni implementazione su base annua. Tutti gli utenti supportati all'interno dell'organizzazione riceveranno una notifica e-mail ogni volta che un'implementazione è vicina alla scadenza. Affinché Adobe possa rinnovare il nome host, un utente supportato dovrà rispondere all'e-mail inviata da Adobe e indicare che intendi continuare a utilizzare il nome host per la raccolta dati. A questo punto, Adobe acquista e installa automaticamente un nuovo certificato.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito Adobe è più sicuro del metodo legacy, in quanto nessun certificato o chiave privata cambia in mani esterne ad Adobe e all'autorità di certificazione emittente. |
| **In che modo Adobe può acquistare un certificato per il nostro dominio?** | Il certificato può essere acquistato solo se hai puntato il nome host specificato (ad esempio, smetrics.example.com) su un nome host di proprietà Adobe. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato in vostro nome. |
| **Posso richiedere la revoca del certificato?** | Sì, come proprietario del dominio, hai diritto a richiedere la revoca del certificato. Per completare il corso, devi aprire un ticket con l'Assistenza clienti. |
| **Il certificato dovrà utilizzare la cifratura SHA -2?** | Sì, Adobe utilizzerà digicert per emettere un certificato SHA -2. |
| **Si tratta di costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti correnti di Analytics senza costi aggiuntivi. |

## Creare record CNAME

Il team delle operazioni di rete della tua organizzazione deve configurare i server DNS creando nuovi record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC fornisce i nomi host configurati e i CNAME a cui puntare. Ad esempio:

* **Nome host SSL**:`smetrics.mysite.com`
* **CNAME SSL**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **Nome host non SSL**:`metrics.mysite.com`
* **CNAME non SSL**:`mysite.com.d1.sc.omtrdc.net`

Fintanto che il codice di implementazione non viene modificato, questo passaggio non influirà sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l'aggiornamento del codice di implementazione.

>[!Note:] Il servizio ID visitatore Experience Cloud fornisce un'alternativa alla configurazione di un CNAME per abilitare i cookie di prime parti.

## Ping del nome host

Ping del nome host per garantire l'inoltro corretto. Tutti i nomi host devono rispondere a un ping per evitare la perdita di dati.

Dopo che i record CNAME sono stati configurati correttamente e Adobe ha confermato l'installazione del certificato, aprite un prompt dei comandi e il ping del vostro nome host. Esempio `mysite.com` di utilizzo: `ping metrics.mysite.com`

Se tutto è stato impostato correttamente, restituirà qualcosa di simile a quanto segue:

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

Se i record CNAME non sono impostati correttamente o non sono attivi, restituiranno quanto segue:

`Ping request could not find the host. Please check the name and try again.`

>[!Note:] In caso di utilizzo `https:// protocol`, il ping risponderà solo alla data di caricamento specificata dallo specialista FPC. Inoltre, assicuratevi di aver toccato il nome host protetto e il nome host non sicuro per garantire che entrambi funzionino correttamente prima di aggiornare l'implementazione.

## Aggiornare il codice di implementazione

Prima di modificare il codice sul sito per utilizzare cookie di prime parti, completate i seguenti prerequisiti:

* Richiedete un certificato SSL, come descritto in Passaggi di implementazione per il programma di certificazione gestito di Adobe.
* Creare record CNAME.
* Ping del nome host.

Dopo aver verificato i nomi host, è possibile rispondere e inoltrare i server di raccolta dati Adobe, modificando l'implementazione in modo che punti ai nomi host della raccolta dati.

1. Aprite il file javascript di base (`s_code.js/AppMeasurement.js`).
1. Se desiderate aggiornare la versione del codice, sostituite l'intero `s_code.js/AppMeasurement.js` file con la versione più recente e sostituite eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo con i cookie di prime parti, individua le variabili s. trackingserver e s. trackingserversecure (se utilizzate SSL) e indicali ai nuovi nomi host della raccolta dati. Come esempio: mysite.com:`s.trackingServer = "metrics.mysite.com"``s.trackingServerSecure = "smetrics.mysite.com"`

1. Caricate il file javascript di base aggiornato sul sito.
1. Se state spostando i cookie di prime parti da un'implementazione di lunga data o che si modificano con un nome host di raccolta diverso, si consiglia di migrare i visitatori dal dominio precedente al nuovo dominio.

Consulta [Migrazione dei visitatori](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) nella Guida all'implementazione di Analytics.

Dopo aver caricato il file javascript, tutto è configurato per la raccolta dati di cookie di prime parti. Consigliamo di monitorare i rapporti di Analytics per le prossime ore in modo che la raccolta dei dati continui come normale. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e che uno degli utenti supportati della tua organizzazione possa contattare l'Assistenza clienti.
