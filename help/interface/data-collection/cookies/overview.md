---
description: Scopri come le soluzioni e i servizi di Adobe Experience Cloud utilizzano i cookie.
title: Utilizzo dei cookie in Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: d6dc659104b3b24b60495cd97adb21ebb3962fc7
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 10%

---

# Cookie utilizzati in Experience Cloud

Adobe Experience Cloud utilizza i cookie. Un cookie è una piccola parte di dati che un sito Web invia al browser, che lo memorizza per un uso successivo. I cookie aiutano il sito a ricordare le cose quando visiti di nuovo o passi da una pagina all’altra. I cookie aiutano a tenere traccia delle visite e a distinguere un dispositivo dall’altro.

Le leggi richiedono spesso di ottenere l’autorizzazione prima di memorizzare o utilizzare i cookie sul dispositivo di qualcuno. Adobe consiglia di consultare il team legale per comprendere le regole applicabili.

## Informazioni sui cookie di prime parti

Adobe Experience Cloud utilizza i cookie per tenere traccia delle informazioni che non durano tra le visualizzazioni di pagina o le sessioni del browser. Quando possibile, Adobe utilizza cookie di prime parti (associati al tuo sito web). Per monitorare l’attività su più siti o domini di tua proprietà, sono necessari cookie di terze parti.

Alcuni browser e strumenti antispyware bloccano i cookie di terze parti. Adobe dispone di modi per garantire che i cookie continuino a funzionare anche se i cookie sono bloccati. Il funzionamento dipende dall&#39;utilizzo del servizio Experience Platform Identity (ECID) o dei cookie Analytics precedenti (come il cookie `s_vi`):

* [Servizio Experience Cloud Identity](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview): il servizio ECID imposta sempre i cookie di prime parti, indipendentemente dal fatto che il dominio di raccolta corrisponda al dominio del sito. Utilizza JavaScript per inserire il cookie nel dominio del sito.

* [Identificatori legacy di Analytics](analytics.md) (ad esempio il cookie `s_vi`): se i cookie sono di prima parte o di terze parti dipende dalla configurazione:

   * Se il server di raccolta dati corrisponde al dominio del sito, i cookie sono di prime parti.
   * Se non corrisponde, i cookie sono di terze parti. Se i cookie di terze parti sono bloccati, Adobe imposta un cookie di fallback (`s_fid`) invece del solito.

Per assicurarsi che il server di raccolta corrisponda al dominio del sito, puoi utilizzare una **configurazione CNAME**. Ciò comporta l’aggiornamento delle impostazioni DNS in modo che un dominio personalizzato (di tua proprietà) punti ai server di Adobe. In questo modo il cookie di tracciamento viene visualizzato come di prime parti. Anche se un CNAME può funzionare tra più domini, qualsiasi dominio che non corrisponde al CNAME imposterà comunque i cookie di terze parti.

>[!NOTE]
>
>La funzione Intelligent Tracking Prevention (ITP) di Apple limita la durata dei cookie di prime parti di Adobe, anche se il dominio di raccolta corrisponde al dominio del sito. ITP riguarda Safari su macOS e tutti i browser su iOS e iPadOS. Da novembre 2020, i cookie impostati con CNAME scadono con la stessa rapidità dei cookie impostati con JavaScript. Questo termine può cambiare in futuro.

Ecco una versione semplificata del testo:

## Cookie e privacy

Adobe prende sul serio la privacy e la sicurezza dei dati. Funziona con organizzazioni per la privacy, enti normativi e programmi come AdChoices per dare alle persone il controllo su come vengono utilizzati i loro dati.

La maggior parte dei cookie di Adobe Experience Cloud non memorizza informazioni personali. Sono sicure e utilizzate solo dalla tua azienda, per reportistica, contenuti e pubblicità. Adobe non condivide questi dati con altri clienti o terze parti, ad eccezione dei rapporti anonimi a livello di settore (come i rapporti di Digital Marketing Insight).

Adobe non combina i dati del browser tra diverse aziende. Per proteggere la privacy, alcuni strumenti di Adobe consentono a ogni sito web di utilizzare il proprio set di cookie. Alcuni consentono anche di utilizzare il tuo dominio per i cookie, rendendoli di prima parte e più sicuri.

I cookie possono memorizzare solo le informazioni salvate in precedenza. Non possono eseguire codice o leggere altri dati sul dispositivo. Inoltre, i browser web consentono solo la lettura dei cookie da parte del sito web che li ha impostati. Ad esempio, solo Adobe.com può leggere i cookie impostati.

Il diagramma seguente illustra l’utilizzo dei cookie per una richiesta di immagine standard:

![Utilizzo di cookie per una richiesta immagine standard](assets/CookiesProcessGraphic-01.png)

Il diagramma seguente illustra l’utilizzo dei cookie per una richiesta di immagini diretta (utilizzata negli scenari in cui non viene caricato un file JS):

![Utilizzo di cookie per una richiesta immagine diretta](assets/CookiesProcessGraphic2.png)
