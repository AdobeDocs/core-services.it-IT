---
description: Scopri le considerazioni e le best practice sui dati di identificazione personale (PII) caricati e utilizzati in Experience Cloud.
solution: Experience Cloud
title: Considerazioni sulla privacy per gli attributi del cliente
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 27c026ff-198b-4f49-9718-f25f77a9e716
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 99%

---

# Considerazioni sulla privacy per [!DNL customer attributes]

Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.

* Nome e cognome
* Indirizzo dell&#39;abitazione o altro indirizzo fisico
* Indirizzo e-mail
* Numero di telefono
* Numero di previdenza sociale
* Altro identificatore che consente di contattare fisicamente o online un individuo (varia in base alla posizione geografica. Verifica e rispetta le leggi e i regolamenti locali relativi alla privacy e ai dati PII per tutti i luoghi in cui si svolge la tua attività).

Adobe fornisce strumenti che consentono agli inserzionisti di raccogliere informazioni comportamentali sui consumatori che visitano i loro siti o utilizzano le loro applicazioni. Adobe fornisce inoltre strumenti che consentono agli inserzionisti di migliorare tali informazioni con rapporti offline o esterni sui clienti che l&#39;inserzionista potrebbe avere all&#39;interno di altri sistemi di gestione delle informazioni.

Uno dei motivi comuni per cui gli inserzionisti fanno ciò è migliorare le informazioni disponibili quando prendono decisioni su marketing e pubblicità adeguate ai consumatori. Adobe Analytics e Target consentono agli inserzionisti di caricare personalmente dati personali (personally identifiable information, PII) come indirizzi e-mail solo dopo aver aggiunto l&#39;hash per non renderne più possibile l&#39;utilizzo per contattare la persona. Le informazioni con hash possono essere comunque utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe, ad esempio cartelle cliniche, informazioni finanziarie e sui minori.

Adobe è consapevole del fatto che questi tipi di decisioni su marketing e pubblicità possono avere implicazioni sulla privacy dei consumatori ed è per questo che offre dei controlli integrati sulla privacy per aiutare gli inserzionisti a soddisfare le aspettative dei consumatori. Adobe consiglia agli inserzionisti di considerare attentamente quali informazioni utilizzare a fini di marketing e le circostanze in cui sia lecito utilizzarle, in base alle autorizzazioni acquisite.

## Best practice

Quando si caricano dati PII su Adobe Analytics o Adobe Target, Adobe consiglia al cliente di aggiungere hash di tali dati prima di caricarli su Adobe. Le informazioni con hash possono essere comunque utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe Analytics e Adobe Target, ad esempio cartelle cliniche, informazioni finanziarie e sui minori.

Adobe consiglia agli inserzionisti di considerare attentamente quali informazioni utilizzare a fini di marketing e le circostanze in cui sia lecito utilizzarle, in base alle autorizzazioni acquisite.

Poiché la normativa sulla privacy dei consumatori è in continuo mutamento, Adobe consiglia agli inserzionisti di rispettare tre principi comuni:

1. Fai ciò che dici (nell&#39;informativa sulla privacy).
1. Di&#39; ciò che fai (nell&#39;informativa sulla privacy).
1. Non fare avere sorprese ai consumatori.

Tenendo presenti queste aspettative, Adobe consiglia agli inserzionisti che associano le attività di ricerca ai dati PII di fornire un avviso o una personalizzazioni che indichi che il consumatore è autenticato. Un esempio è includere un saluto all&#39;interno dell&#39;intestazione del sito web. Adobe consiglia inoltre agli inserzionisti di descrivere nell&#39;informativa sulla privacy il tipo di informazioni di navigazione associate ai dati PII e in quali circostanze le informazioni di navigazione sono associate ai dati PII. Infine, Adobe consiglia vivamente agli inserzionisti di esaminare le opzioni di opt-out fornite ai consumatori, per capire se e come sia possibile utilizzare eventuali informazioni di profilo non autenticate in seguito alla rinuncia del comsumatore.
