---
description: Scopri come le soluzioni e i servizi di Adobe Experience Cloud utilizzano i cookie.
title: Utilizzo dei cookie in Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 58%

---


# Cookie utilizzati in Experience Cloud

Molti servizi all’interno di Adobe Experience Cloud utilizzano i cookie. Un cookie è una piccola parte di dati presentata da un sito Web a un browser Web. Il browser memorizza questi dati, consentendo a un sito web di fare riferimento ai propri dati quando necessario. Questa azione viene eseguita per ogni richiesta successiva di pagine e immagini.

I cookie sono forniti per mantenere le informazioni durante e talvolta tra le visite a un sito Web. I cookie consentono ai dispositivi di essere differenziati in modo univoco dagli altri browser che visualizzano il sito.

Leggi, normative e principi di autoregolamentazione richiedono di ottenere il consenso dei visitatori prima di poter archiviare o recuperare informazioni su un computer o su un altro dispositivo connesso al web. L’Adobe suggerisce di verificare con il consulente legale della tua organizzazione quali leggi, regolamenti e principi controllano l’utilizzo dei cookie da parte tua.

## Informazioni sui cookie di prime parti

I servizi Adobe Experience Cloud utilizzano i cookie per fornire informazioni su variabili e componenti che non permangono tra richieste di immagini e sessioni del browser. Laddove possibile, Adobe utilizza cookie di prime parti per registrare le attività sul sito. Per registrare l’attività su siti diversi, ad esempio su altri domini di tua proprietà, sono necessari cookie di terze parti.

Molti browser e applicazioni antispyware sono progettati per rifiutare ed eliminare i cookie di terze parti. Adobe garantisce che i cookie possano sempre essere impostati anche se i cookie di terze parti sono bloccati. Il comportamento specifico varia a seconda che si utilizzi il servizio Experienci Platform Identity (servizio ECID) o gli identificatori legacy di Analytics (come `s_vi` cookie):

* Il [Servizio Experienci Platform Identity (servizio ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) imposta automaticamente i cookie di prime parti indipendentemente dal fatto che il dominio di raccolta corrisponda o meno al dominio del sito. Se non corrispondono, il servizio Identity utilizza JavaScript per impostare i cookie sul dominio del sito.
* Se usa [Identificatori legacy di Analytics](analytics.md) (ad esempio `s_vi` cookie), dipende da come hai configurato il server di raccolta dati. Se il server di raccolta dati corrisponde al dominio del sito, i cookie verranno impostati come cookie di prime parti. Se il server di raccolta non corrisponde al dominio corrente, i cookie vengono impostati come di terze parti. In questo caso, se i cookie di terze parti sono bloccati, Analytics imposta un ID di fallback di prime parti (`s_fid`) invece dello standard `s_vi` cookie.

Se desideri che il server di raccolta corrisponda al dominio del sito, puoi utilizzare un’implementazione CNAME che consente l’inoltro da un dominio personalizzato specificato nell’implementazione CNAME ai server di raccolta Adobe. Questa attività comporta modifiche alle impostazioni DNS della tua azienda per configurare un alias CNAME che punti a un dominio ospitato da un Adobe. Sebbene diversi prodotti Adobe supportino l’uso di un CNAME, in tutti i casi questo viene utilizzato per creare un endpoint di prima parte affidabile per un cliente specifico e rimane di proprietà di tale cliente. Se controlli più domini, è possibile utilizzare un singolo endpoint CNAME per monitorare gli utenti nei loro domini, ma nei casi in cui il sito non corrisponde ai cookie del dominio CNAME vengono impostati come di terze parti.

>[!NOTE]
>
>Indipendentemente dal fatto che il dominio di raccolta corrisponda al dominio del sito, il programma ITP (Intelligent Tracking Prevention) di Apple rende di breve durata i cookie di prime parti impostati da Adobe sui browser gestiti da ITP, che includono Safari su macOS e tutti i browser su iOS e iPadOS. A partire da novembre 2020, anche i cookie impostati tramite CNAME hanno la stessa scadenza dei cookie impostati tramite JavaScript. Questa scadenza è soggetta a modifiche.

## Cookie e privacy

Garantire la privacy dei clienti e la sicurezza dei dati sono le principali priorità di Adobe. Adobe partecipa a più organizzazioni sulla privacy e collabora con le autorità di regolamentazione della privacy e i principi di autoregolamentazione. Questa cooperazione include il programma Digital Advertising Alliance AdChoices per fornire ai clienti informazioni su come vengono usati i loro dati personali e sulle scelte relative al loro utilizzo.

La maggior parte dei cookie impostati dai prodotti Experience Cloud non contiene informazioni personali identificabili. Questi cookie e i dati associati sono protetti e utilizzati solo per i report della tua azienda e per fornire contenuti e annunci pertinenti. I dati non sono disponibili per terze parti o altri clienti Adobe, a meno che non siano utilizzati nei report aggregati sul settore. Ad esempio, [!DNL Digital Marketing Insight Report] analizza dati aggregati e anonimi attraverso i rivenditori.

Adobe non unisce le informazioni del browser all’interno delle aziende. Per proteggere la privacy e la sicurezza dei dati dei clienti, alcuni servizi all’interno di Experience Cloud offrono alle aziende la possibilità di utilizzare un set separato di cookie per ciascun sito tracciato. Alcune offerte offrono anche ai clienti la possibilità di utilizzare il proprio nome di dominio come proprietario del cookie. Questa procedura crea un ulteriore livello di privacy e sicurezza, in quanto rende i cookie di Experience Cloud *cookie di prime parti*, che appartengono definitivamente al sito dell’azienda.

I cookie possono memorizzare e fornire solo le informazioni precedentemente archiviate. Non sono in grado di eseguire codice o di accedere ad altre informazioni memorizzate nel computer. Inoltre, i browser web limitano l’accesso ai dati dei cookie. I browser impongono una policy di sicurezza dei cookie che rende tutti i dati dei cookie disponibili solo per il sito Web che ha inizialmente impostato le informazioni.

Ad esempio, i dati contenuti nei cookie impostati dal sito Web Adobe.com non possono essere visualizzati da siti Web diversi da Adobe.com.

Il diagramma seguente illustra l’utilizzo dei cookie per una richiesta di immagine standard:

![Utilizzo di cookie per una richiesta immagine standard](assets/CookiesProcessGraphic-01.png)

Il diagramma seguente illustra l’utilizzo dei cookie per una richiesta di immagini diretta (utilizzata negli scenari in cui non viene caricato un file JS):

![Utilizzo di cookie per una richiesta immagine diretta](assets/CookiesProcessGraphic2.png)
