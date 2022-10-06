---
description: Scopri come Adobe Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser.
solution: Experience Cloud,Analytics
title: "Cookie di prime parti "
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 52796154e260648eb2fc57cc2b45453e9cb3227a
workflow-type: tm+mt
source-wordcount: '1615'
ht-degree: 79%

---

# Informazioni sui cookie di prime parti

Analytics utilizza i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Laddove possibile, Adobe ricorre a cookie di prime parti per registrare le attività sul sito. Per registrare l’attività su siti diversi, ad esempio su altri domini di tua proprietà, sono necessari cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti. Adobe garantisce che i cookie possano sempre essere impostati anche se i cookie di terze parti sono bloccati. Il comportamento specifico varia a seconda che si utilizzi il servizio Experience Platform Identity (servizio ECID) o gli identificatori legacy di Analytics (ovvero il cookie s_vi):

* Il [servizio Experience Platform Identity (servizio ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) imposterà automaticamente i cookie di prime parti indipendentemente dal fatto che il dominio di raccolta corrisponda o meno al dominio del sito. Se non corrispondono, il servizio Identity utilizza JavaScript per impostare i cookie nel dominio del sito.
* Se utilizzi gli [identificatori precedenti di Analytics ](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=it) (o cookie `s_vi`), dipenderà da come hai configurato il server di raccolta dati. Se il server di raccolta dati corrisponde al dominio del sito, i cookie verranno impostati come cookie di prime parti. Se il server di raccolta non corrisponde al dominio attuale, verranno impostati come cookie di terze parti. In questo caso, se i cookie di terze parti sono bloccati, Analytics imposterà un [ID di fallback (s_fid)](cookies-analytics.md) di prime parti invece del cookie standard “s_vi”.

Se desideri che il server di raccolta corrisponda al dominio del sito, puoi utilizzare un’implementazione CNAME che abilita l’inoltro da un dominio personalizzato specificato nell’implementazione CNAME ai server di raccolta Adobe. Ciò comporta modifiche alle impostazioni DNS della tua azienda per configurare un alias CNAME che punti a un dominio ospitato da Adobe. Sebbene diversi prodotti Adobe supportino l’uso di un CNAME, in tutti i casi questo viene utilizzato per creare un endpoint di prima parte affidabile per un cliente specifico e rimane di proprietà di tale cliente. Se controlli più domini, è possibile utilizzare un singolo endpoint CNAME per monitorare gli utenti nei vari domini; tuttavia, nei casi in cui il sito non corrisponde ai cookie del dominio CNAME, verrà impostato come di terze parti.

>[!NOTE]
>
>Indipendentemente dal fatto che il dominio di raccolta corrisponda al dominio del sito, il programma ITP (Intelligent Tracking Prevention) di Apple rende di breve durata i cookie di prime parti impostati da Adobe su browser gestiti da ITP, che includono Safari su macOS e tutti i browser su iOS e iPadOS. A partire da novembre 2020, anche i cookie impostati tramite CNAME hanno la stessa scadenza dei cookie impostati tramite JavaScript. Questa scadenza è soggetta a modifiche.

Se desideri stabilire un CNAME per la raccolta dati e se il tuo sito dispone di pagine sicure utilizzando il protocollo HTTPS, puoi richiedere l’assistenza di Adobe per ottenere un certificato SSL.

Spesso il processo di rilascio del certificato SSL crea confusione e richiede tempo. Di conseguenza, Adobe ha stabilito una partnership con DigiCert, un’autorità di certificazione (CA) leader del settore, e ha sviluppato un processo integrato per automatizzare l’acquisto e la gestione di tali certificati.

Con la tua autorizzazione, collaboriamo con la nostra CA per rilasciare, distribuire e gestire un nuovo certificato SSL SHA-2 per tuo conto. Adobe continua a gestire questo certificato e fa in modo che, in caso di scadenza, revoca o problemi di sicurezza imprevisti, la raccolta sicura delle organizzazioni non venga compromessa.

## Programma di certificazione gestito da Adobe

Il programma Adobe Managed Certificate è il processo consigliato per l’impostazione del certificato SSL di prima parte necessario per un’implementazione CNAME che garantisca che il server di raccolta Adobe corrisponde al dominio del sito.

Il programma Adobe Managed Certificate consente di implementare un nuovo certificato SSL di prima parte senza costi aggiuntivi (per i primi 100 CNAME). Se al momento disponi di un tuo certificato SSL gestito dal cliente, chiama l’Assistenza clienti Adobe per informazioni su come effettuare la migrazione al programma di certificazione gestito da Adobe.

### Implementazione

Per implementare un nuovo certificato SSL di prima parte per la raccolta dati di prima parte:

1. Compila il [modulo di richiesta per dominio di prima parte](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) e apri un ticket presso l’Assistenza clienti per richiedere la configurazione della raccolta dati di prima parte nel programma gestito da Adobe.

   Ogni campo è descritto all’interno del documento con esempi.

1. Crea record CNAME (consulta le istruzioni riportate di seguito).

   Quando viene ricevuto il ticket, un rappresentante dell’assistenza clienti ti fornirà un record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. Il CNAME ha un aspetto simile a quanto segue:

   **Protetto**: ad esempio, il nome host `smetrics.example.com` punta a: `example.com.adobedc.net`.

   >[!NOTE]
   > In passato, Adobe consigliava ai clienti di impostare due CNAME, uno per HTTPS e uno per HTTP. Poiché è buona prassi crittografare il traffico e la maggior parte dei browser scoraggia fortemente HTTP, si sconsiglia più di impostare un CNAME per HTTP. Contatta l’Assistenza clienti Adobe per configurare il tuo CNAME per HTTP.

1. Una volta impostato il CNAME, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di produzione di Adobe.

   Se disponi già di un’implementazione, prendi in considerazione Migrazione visitatori per mantenere i visitatori esistenti. Dopo il push live del certificato all’ambiente di produzione di Adobe, puoi aggiornare le variabili del server di tracciamento ai nuovi nomi host. Ciò significa che, se il sito non è protetto (HTTP), devi aggiornare `s.trackingServer`. Se il sito è protetto (HTTPS), aggiorna sia la variabile `s.trackingServer` che la variabile `s.trackingServerSecure`.

1. [Convalida dell’inoltro nome host](#validate) (vedi di seguito).

1. [Aggiorna il codice di implementazione](#update) (vedi di seguito).

### Manutenzione e rinnovi

Trenta giorni prima della scadenza del certificato di prima parte, l’Adobe verifica se il CNAME è ancora valido e in uso. In questo caso, Adobe presuppone che si desideri continuare a utilizzare il servizio e rinnova automaticamente il certificato per suo conto.

Al momento, se il CNAME è stato rimosso e non è più valido, Adobe non rinnova il certificato e la voce nel nostro sistema viene contrassegnata per la rimozione. Se il CNAME è stato rimosso, l’Adobe sa che il tracciamento non si verifica utilizzando tale URL e che è quindi sicuro da rimuovere.

### Domande frequenti

| Domanda | Risposta |
|---|---|
| **Il processo è sicuro?** | Sì, il programma gestito da Adobe è più sicuro del metodo legacy, in quanto nessun certificato o chiave privata vengono trasmessi al di fuori di Adobe e dell’autorità di certificazione emittente. |
| **In che modo Adobe può acquistare un certificato per il mio dominio?** | Il certificato può essere acquistato solo dopo aver puntato il nome host specificato (ad esempio `telemetry.example.com`) a un nome host di proprietà di Adobe. In pratica questo nome host viene delegato ad Adobe e consente ad Adobe di acquistare il certificato a tuo nome. |
| **Posso richiedere la revoca del certificato?** | Sì, in qualità di proprietario del dominio, hai il diritto di richiedere la revoca del certificato. Apri un ticket con l’Assistenza clienti per completare l’operazione. |
| **Il certificato utilizzerà la cifratura SHA-2?** | Sì, Adobe funziona con DigiCert per rilasciare un certificato SHA-2. |
| **Sono previsti costi aggiuntivi?** | No, Adobe offre questo servizio a tutti i clienti attuali di Analytics senza costi aggiuntivi. |

{style=&quot;table-layout:auto&quot;}

## Creazione di record CNAME

Il team che gestisce la rete della tua organizzazione deve configurare i server DNS creando nuovi record CNAME. Ciascun nome host comunica i dati ai server di raccolta dati di Adobe.

Lo specialista FPC ti fornisce il nome host configurato e il CNAME a cui deve puntare. Esempio:

* **Nome host SSL**: `smetrics.mysite.com`
* **CNAME SSL**: `mysite.com.adobedc.net`

>[!NOTE]
> Se utilizzi ancora un CNAME non protetto, si presenterà come il seguente:
> * **Nome host non SSL**: `metrics.mysite.com`
> * **CNAME non SSL**: `mysite.com.adobedc.net`


Fintanto che il codice di implementazione non viene modificato, questo passaggio non influisce sulla raccolta dei dati e può essere eseguito in qualsiasi momento dopo l’aggiornamento del codice di implementazione.

## Convalida dell’inoltro nome host {#validate}

Per la convalida sono disponibili i seguenti metodi:

### Convalida tramite browser

Se hai configurato un CNAME e hai installato il certificato, puoi utilizzare il browser per la convalida:

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>Se non è installato un certificato, verrà visualizzato un avviso di protezione.

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

È possibile utilizzare `nslookup` per la convalida. Utilizzando `smetrics.adobe.com`come esempio, apri un prompt dei comandi e digita `nslookup smetrics.adobe.com`

Se tutto è configurato correttamente, verrà visualizzata una restituzione simile a:

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

Prima di modificare il codice sul sito per utilizzare la raccolta dati di prima parte, completa i seguenti prerequisiti:

* Richiedi un certificato SSL seguendo i passaggi descritti in precedenza nella sezione sull’*implementazione* in [Programma di certificazione gestito di Adobe](#adobe-managed-certificate-program).
* Crea record CNAME (vedi sopra).
* Convalida i nomi host (vedi sopra).

Dopo aver verificato che i nomi host rispondano e trasmettano ai server di raccolta dati di Adobe, puoi modificare l’implementazione in modo che punti ai nomi host della tua raccolta dati.

1. Apri il tuo file JavaScript di base (`s_code.js/AppMeasurement.js`).
1. Se vuoi aggiornare la versione del codice, sostituisci l’intero file `s_code.js/AppMeasurement.js` con la versione più recente e sostituisci eventuali plug-in o personalizzazioni (se presenti). **Oppure**, se desideri aggiornare il codice solo per la raccolta dati di prima parte pertinente, individua le variabili s.trackingServer e s.trackingServerSecure (se utilizzi SSL) e impostale sui nuovi nomi host per la raccolta dati. Usiamo ilmiosito.com come esempio:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Carica il file JavaScript di base aggiornato sul sito.

1. Se stai passando alla raccolta dati di prima parte da un’implementazione di lunga data o a un nome host di raccolta di prima parte diverso, Adobe consiglia di migrare i visitatori dal dominio precedente al nuovo.

Consulta la sezione [Migrazione dei visitatori](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=it) nella Guida all’implementazione di Analytics.

Dopo che hai caricato il file JavaScript, tutto è configurato per la raccolta dati di prime parti. Per le prime ore, Adobe consiglia di monitorare i report di Analytics per verificare che la raccolta dei dati continui come previsto. In caso contrario, verifica che tutti i passaggi precedenti siano stati completati e fai contattare l’Assistenza clienti da uno degli utenti supportati dalla tua organizzazione.
