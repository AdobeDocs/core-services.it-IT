---
description: Scopri come Adobe Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
keywords: cookie;privacy
solution: Experience Cloud,Analytics
title: '"Cookie di prime parti "'
index: y
snippet: y
feature: Cookie
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 11b999ef0c0d4f258e8665eb9c5bf427f5d618c4
workflow-type: tm+mt
source-wordcount: '1576'
ht-degree: 55%

---

# Informazioni sui cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Laddove possibile, ad Adobe, vengono utilizzati cookie di prime parti per registrare le attività sul sito. Per registrare l’attività su siti diversi, ad esempio su altri domini di tua proprietà, sono necessari cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti, inclusi i cookie utilizzati nella raccolta dati [!DNL Analytics]. Per supportare il tracciamento dell’interazione dei visitatori con il sito web, assicurati di aver configurato la raccolta dati per l’utilizzo dei cookie di prime parti:

Per implementare i cookie di prime parti sono disponibili due opzioni:

* Se utilizzi il servizio Experience Platform Identity (servizio ECID), imposta automaticamente i cookie nel contesto di prime parti utilizzando JavaScript.
* Se utilizzi [!DNL Analytics] identificatori legacy (ovvero il cookie `s_vi` ), dipende da come hai configurato il server di raccolta dati. Se il server di raccolta dati corrisponde al dominio del sito, i cookie vengono impostati come di prime parti. Se il server di raccolta non corrisponde al dominio corrente, i cookie vengono impostati come terze parti. In questo caso, se i cookie di terze parti sono bloccati, [!DNL Analytics] imposta un [fallback id (s_fid)](cookies-analytics.md) di prima parte invece del cookie standard &quot;s_vi&quot;.

Per garantire che il server di raccolta corrisponda al dominio del sito, puoi utilizzare un’implementazione CNAME per impostare i cookie in un contesto di prime parti. Ciò comporta modifiche alle impostazioni DNS della tua azienda per configurare un alias CNAME che punta a un dominio ospitato di Adobe. Sebbene diversi prodotti Adobe supportino l’uso di un CNAME, in tutti i casi questo viene utilizzato per creare un endpoint di prima parte affidabile per un cliente specifico e rimane di proprietà di tale cliente. Se controlli più domini, puoi utilizzare un singolo endpoint CNAME per monitorare gli utenti nei loro domini, ma ovunque il dominio del sito non corrisponda ai cookie del dominio CNAME viene impostato come di terze parti.

>[!NOTE]
>
>Per entrambe le opzioni, il programma ITP (Intelligent Tracking Prevention) di Apple rende i cookie di prime parti di breve durata sui browser gestiti da ITP, che includono Safari su macOS e tutti i browser su iOS e iPadOS. A partire da novembre 2020, entrambi i tipi di cookie scadono dopo sette giorni. Questa scadenza è soggetta a modifiche.

Per la seconda opzione che utilizza un CNAME, se il tuo sito dispone di pagine sicure con protocollo HTTPS, puoi lavorare con Adobe per ottenere un certificato SSL che ti consenta di implementare i cookie di prime parti. Adobe consiglia vivamente di utilizzare esclusivamente HTTPS per la raccolta dei dati, in quanto, ad Adobe, il supporto per la raccolta HTTP verrà eliminato nella seconda metà del 2020.

Spesso il processo di rilascio del certificato SSL crea confusione e richiede tempo. Di conseguenza, l’Adobe ha stabilito una partnership con DigiCert, un’autorità di certificazione (CA) leader del settore, e ha sviluppato un processo integrato che automatizza l’acquisto e la gestione di tali certificati.

Con la tua autorizzazione, collaboriamo con CA per rilasciare, distribuire e gestire un nuovo certificato SSL SHA-2 per te. Adobe continua a gestire questo certificato e assicura che una scadenza, una revoca o un problema di sicurezza imprevisti non comprometta la disponibilità della raccolta sicura della tua organizzazione.

## Programma di certificazione gestito da Adobe

Il programma di certificazione gestito di Adobe è il processo consigliato per l’implementazione di un nuovo certificato SSL di prima parte per i cookie di prime parti.

Il programma di certificazione gestito di Adobe consente di implementare un nuovo certificato SSL di prima parte per i cookie di prime parti senza costi aggiuntivi (per i primi 100 CNAME). Se al momento disponi di un certificato SSL gestito dal cliente, rivolgiti all’Assistenza clienti Adobe per informazioni sulla migrazione al programma di certificazione gestito da Adobe.

### Implementazione

Per implementare un nuovo certificato SSL di prima parte per i cookie di prime parti:

1. Compila il [modulo di richiesta dei cookie di prime parti](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) e apri un ticket con l’Assistenza clienti per richiedere la configurazione dei cookie di prime parti nel programma gestito da Adobe. Ogni campo è descritto all’interno del documento con esempi.

2. Crea record CNAME (consulta le istruzioni riportate di seguito).

   Quando viene ricevuto il ticket, un rappresentante dell’assistenza clienti ti fornirà un record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. Il CNAME è simile al seguente:

   **Protetto**: ad esempio, il nome host `smetrics.example.com` punta a: `example.com.adobedc.net`.

>[!NOTE]
> In passato, Adobe consigliava ai clienti di impostare due CNAME uno per HTTPS e uno per HTTP. Poiché è buona prassi crittografare il traffico e la maggior parte dei browser scoraggia fortemente HTTP, ora non sconsigliamo più di impostare un CNAME per HTTP. Se necessario, sarà così:
>    **Non protetto**: il nome host `metrics.example.com` punta a `example.com.adobedc.net`.

1. Quando il CNAME è attivo, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di produzione di Adobe.

   Se disponi già di un’implementazione, prendi in considerazione Migrazione visitatori per mantenere i visitatori esistenti. Dopo il push live del certificato all’ambiente di produzione di Adobe, potrai aggiornare le variabili del server di tracciamento con i nuovi nomi host. Ciò significa che, se il sito non è protetto (HTTP), devi aggiornare `s.trackingServer`. Se il sito è protetto (HTTPS), aggiorna sia la variabile `s.trackingServer` che la variabile `s.trackingServerSecure`.

2. [Convalida dell’inoltro nome host](#validate) (vedi di seguito).

3. [Aggiorna il codice di implementazione](#update) (vedi di seguito).

### Manutenzione e rinnovi

I certificati SSL scadono ogni anno, il che significa che Adobe deve acquistare un nuovo certificato per ogni implementazione su base annua. Tutti gli utenti supportati all’interno della tua organizzazione ricevono una notifica e-mail ogni volta che un’implementazione è vicina alla scadenza. Affinché Adobe possa rinnovare il tuo nome host, un utente supportato deve rispondere all’e-mail inviata da Adobe e indicare che intendi continuare a utilizzare il nome host in scadenza per la raccolta dei dati. A questo punto, Adobe acquisterà e installerà automaticamente un nuovo certificato.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito dall&#39;Adobe è più sicuro del nostro metodo legacy, in quanto nessun certificato o chiave privata cambia le mani al di fuori dell&#39;Adobe e dell&#39;autorità di certificazione che lo rilascia. |
| **In che modo Adobe può acquistare un certificato per il mio dominio?** | Il certificato può essere acquistato solo dopo aver puntato il nome host specificato (ad esempio `telemetry.example.com`) a un nome host di proprietà di Adobe. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato a tuo nome. |
| **Posso richiedere la revoca del certificato?** | Sì, come proprietario del dominio, hai diritto di richiedere la revoca del certificato. Per completare il processo, dovrai solo aprire un ticket con l’Assistenza clienti. |
| **Il certificato utilizzerà la cifratura SHA-2?** | Sì, Adobe collaborerà con DigiCert per emettere un certificato SHA-2. |
| **Sono previsti costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti attuali di Analytics senza costi aggiuntivi. |

## Creazione di record CNAME

Il team delle operazioni di rete della tua organizzazione deve configurare i server DNS creando record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC ti fornisce il nome host configurato e il CNAME a cui deve puntare. Ad esempio:

* **Nome host SSL**: `smetrics.mysite.com`
* **CNAME SSL**: `mysite.com.adobedc.net`

>[!NOTE]
> Se utilizzi ancora non protetto, avrà un aspetto simile al seguente:
> * **Nome host non SSL**: `metrics.mysite.com`
> * **CNAME non SSL**: `mysite.com.adobedc.net`


Fintanto che il codice di implementazione non viene modificato, questo passaggio non influisce sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l’aggiornamento del codice di implementazione.

>[!NOTE]
>
>Il servizio ID visitatore di Experience Cloud fornisce un’alternativa alla configurazione di un CNAME per abilitare i cookie di prime parti.

## Convalida dell’inoltro nome host {#validate}

Per la convalida sono disponibili i seguenti metodi:

### Convalida tramite browser

Se hai configurato un CNAME e hai installato il certificato, puoi utilizzare il browser per la convalida:

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>Se non è installato un certificato, viene visualizzato un avviso di protezione.

### Convalida tramite [!DNL curl]

Adobe consiglia di utilizzare [[!DNL curl]](https://curl.se/) dalla riga di comando. Gli utenti [!DNL Windows] possono eseguire l’installazione di [!DNL curl] da: <https://curl.se/windows/>

Se disponi di un CNAME ma non è installato alcun certificato, esegui:
`curl -k https://smetrics.adobe.com/_check`
Risposta: `SUCCESS`

Il valore `-k` disattiva l’avviso di protezione.

Se hai configurato un CNAME e il certificato è installato, esegui:
`curl https://smetrics.adobe.com/_check`
Risposta: `SUCCESS`

### Convalida tramite [!DNL nslookup]

È possibile utilizzare `nslookup` per la convalida. Utilizzando `smetrics.adobe.com` come esempio, apri un prompt dei comandi e digita `nslookup smetrics.adobe.com`

Se tutto è stato configurato correttamente, viene visualizzata una restituzione simile a:

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## Aggiorna il codice di implementazione {#update}

Prima di modificare il codice sul sito per utilizzare i cookie di prime parti, completa i prerequisiti seguenti:

* Richiedi un certificato SSL seguendo i passaggi descritti in precedenza nella sezione *Implementa* del [Programma di certificazione gestito da Adobe](#adobe-managed-certificate-program).
* Crea record CNAME (vedi sopra).
* Convalida i nomi host (vedi sopra).

Dopo aver verificato che i nomi host rispondano e inoltrino ai server di raccolta dati di Adobe, puoi modificare la tua implementazione in modo che punti ai nomi host della tua raccolta dati.

1. Apri il tuo file JavaScript di base (`s_code.js/AppMeasurement.js`).
1. Se vuoi aggiornare la versione del codice, sostituisci l’intero file `s_code.js/AppMeasurement.js` con la versione più recente e sostituisci eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo per i cookie di prime parti, individua le variabili s.trackingServer e s.trackingServerSecure (se utilizzi SSL) e puntale ai nuovi nomi host della tua raccolta dati. Usiamo ilmiosito.com come esempio: `s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Carica il file JavaScript di base aggiornato sul sito.

1. Se stai passando ai cookie di prime parti da un’implementazione di lunga data o a un nome host di raccolta di prima parte diverso, Adobe consiglia di migrare i visitatori dal dominio precedente al nuovo dominio.

Consulta la sezione [Migrazione dei visitatori](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en) nella Guida all’implementazione di Analytics.

Dopo che hai caricato il file JavaScript, tutto è configurato per la raccolta dati di cookie di prime parti. L’Adobe consiglia di monitorare i rapporti di Analytics per le prossime ore per garantire che la raccolta dei dati continui come normale. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e fai contattare l’Assistenza clienti da uno degli utenti supportati dalla tua organizzazione.
