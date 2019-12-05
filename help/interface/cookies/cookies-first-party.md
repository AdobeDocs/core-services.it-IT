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
source-git-commit: 3cb4d346d07e1625e95e3737230f03a02b45afb2

---


# Informazioni sui cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Questi cookie innocui, provenienti da un dominio ospitato da Adobe, sono noti come cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti, inclusi quelli utilizzati nella raccolta dati di Analytics. Per supportare il tracciamento di come i visitatori interagiscono con il tuo sito Web, puoi implementare i cookie di prime parti.

Sono disponibili due opzioni per implementare i cookie di prime parti:

* Servizio ID di Experience Platform. Il servizio ID può impostare il cookie nella prima parte utilizzando JavaScript.
* Voci DNS nel server DNS della società per configurare un alias CNAME in un dominio ospitato da Adobe. Sebbene diversi prodotti Adobe supportino l’uso di un CNAME, in tutti i casi il CNAME viene utilizzato per creare un endpoint di prime parti affidabile per un cliente specifico ed è di proprietà di tale cliente. Se il cliente controlla più domini, può usare un singolo endpoint CNAME per monitorare gli utenti nei loro domini, ma poiché questo richiede cookie di terze parti per tutti i domini al di fuori del dominio del CNAME, non funziona se i cookie di terze parti sono bloccati e non è consigliato. I CNAME Adobe non vengono mai utilizzati per monitorare un singolo o un dispositivo tra domini diversi di proprietà di clienti diversi.

Anche quando si utilizza la prima opzione con il servizio Experience Cloud ID, l'ITP di Apple renderà i cookie di prime parti di breve durata, in modo che sia meglio utilizzato insieme alla seconda opzione.

Per la seconda opzione che utilizza un CNAME, se il tuo sito dispone di pagine sicure utilizzando il `https:` protocollo, puoi lavorare con Adobe per ottenere un certificato SSL al fine di implementare i cookie di prime parti. Adobe consiglia vivamente di utilizzare esclusivamente HTTPS per la raccolta dei dati, in quanto il supporto per la raccolta HTTP verrà eliminato nella seconda metà del 2020.

Spesso il processo di rilascio del certificato SSL crea confusione e richiede tempo. Di conseguenza, Adobe ha stabilito una partnership con DigiCert, un’autorità di certificazione (CA) leader del settore, e ha sviluppato un processo integrato per automatizzare l’acquisto e la gestione di tali certificati.

Con la tua autorizzazione, collaboreremo con la nostra CA per rilasciare, distribuire e gestire un nuovo certificato SSL SHA-2 per tuo conto. Adobe continuerà a gestire questo certificato e a garantire che una scadenza, una revoca o un problema di sicurezza imprevisti non minaccino la disponibilità della raccolta protetta della tua organizzazione.

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

I certificati SSL scadono ogni anno, il che significa che Adobe deve acquistare un nuovo certificato per ogni implementazione su base annua. Tutti gli utenti supportati all’interno dell’organizzazione riceveranno una notifica e-mail ogni volta che un’implementazione è vicina alla scadenza. Affinché Adobe possa rinnovare il nome host, un utente supportato deve rispondere all'e-mail inviata da Adobe e indicare che si intende continuare a utilizzare il nome host in scadenza per la raccolta dei dati. A questo punto, Adobe acquisterà e installerà automaticamente un nuovo certificato.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito da Adobe è più sicuro del metodo legacy, in quanto nessun certificato o chiave privata vengono trasmessi al di fuori di Adobe e dell’autorità di certificazione emittente. |
| **In che modo Adobe può acquistare un certificato per il mio dominio?** | Il certificato può essere acquistato solo se hai puntato il nome host specificato (ad esempio, smetriche.esempio.com) su un nome host di proprietà di Adobe. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato a tuo nome. |
| **Posso richiedere la revoca del certificato?** | Sì, come proprietario del dominio, hai diritto di richiedere la revoca del certificato. Per completare il processo, dovrai solo aprire un ticket con l’Assistenza clienti. |
| **Il certificato utilizzerà la cifratura SHA-2?** | Sì, Adobe collaborerà con DigiCert per emettere un certificato SHA-2. |
| **Sono previsti costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti Adobe Digital Experience correnti senza costi aggiuntivi. |

## Creazione di record CNAME

Il team che gestisce la rete della tua organizzazione deve configurare i server DNS creando nuovi record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC fornisce i nomi host configurati e i CNAME a cui devono essere puntati. Ad esempio:

* **Nome host SSL**:`smetrics.mysite.com`
* **CNAME SSL**:`mysite.com.ssl.sc.omtrdc.net`
* **Nome host non SSL**:`metrics.mysite.com`
* **CNAME non SSL**:`mysite.com.sc.omtrdc.net`

Fintanto che il codice di implementazione non viene modificato, questo passaggio non influisce sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l’aggiornamento del codice di implementazione.

>[!N] Nota: Il servizio ID visitatori di Experience Cloud fornisce un’alternativa alla configurazione di un CNAME per abilitare i cookie di prime parti. Tuttavia, a causa delle recenti modifiche dell’ITP Apple, è comunque consigliabile allocare un CNAME anche quando si utilizza il servizio Experience Cloud ID.

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

>[!Nota:] se utilizzi `https:// protocol`, il ping risponderà solo dopo la data di caricamento specificata dallo specialista FPC. Inoltre, assicuratevi di eseguire il ping del nome host sicuro e del nome host non sicuro per verificare che entrambi funzionino correttamente prima di aggiornare l'implementazione.

## Aggiorna il codice di implementazione

Prima di modificare il codice sul sito per utilizzare i cookie di prime parti, completa i seguenti prerequisiti:

* Richiedete un certificato SSL seguendo i passaggi descritti in precedenza nella sezione *Implementa* del programma [di certificazione gestito di](#adobe-managed-certificate-program)Adobe.
* Crea record CNAME (vedi sopra).
* Inserire i nomi host (vedere sopra).

Dopo aver verificato che i nomi host rispondano e trasmettano ai server di raccolta dati di Adobe, puoi modificare l’implementazione in modo che punti ai nomi host della tua raccolta dati.

1. Apri il tuo file JavaScript di base (`s_code.js/AppMeasurement.js`).
1. Se vuoi aggiornare la versione del codice, sostituisci l’intero file `s_code.js/AppMeasurement.js` con la versione più recente e sostituisci eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo per i cookie di prime parti, individua le variabili s.trackingServer e s.trackingServerSecure (se utilizzi SSL) e puntale ai nuovi nomi host della tua raccolta dati. Usiamo ilmiosito.com come esempio:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Carica il file JavaScript di base aggiornato sul sito.

1. Se stai passando ai cookie di prime parti da un’implementazione di lunga data o a un nome host di raccolta di prima parte diverso, ti consigliamo di migrare i visitatori dal dominio precedente al nuovo.

Consulta Migrazione [dei](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) visitatori nella Guida all'implementazione di Analytics.

Dopo che hai caricato il file JavaScript, tutto è configurato per la raccolta dati di cookie di prime parti. Per le prime ore, ti consigliamo di monitorare i report di Analytics per verificare che la raccolta dei dati continui come previsto. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e fai contattare l’Assistenza clienti da uno degli utenti supportati dalla tua organizzazione.
