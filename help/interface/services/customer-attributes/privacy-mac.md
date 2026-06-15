---
description: Scopri le considerazioni e le best practice sui dati personali (PII, personally identifiable information) caricati e utilizzati in CX Enterprise.
solution: Experience Cloud
title: Considerazioni sulla privacy per  [!DNL Customer Attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 27c026ff-198b-4f49-9718-f25f77a9e716
TQID: https://experienceleague.adobe.com/4L-qz0n3h97DduJvPGGoJPl1VvrPAKJTeUnkJGs6xvc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 511
ht-degree: 92%

---

# Considerazioni sulla privacy per [!DNL Customer Attributes]

Considerazioni e best practice sui dati personali caricati e utilizzati in Adobe CX Enterprise.

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
