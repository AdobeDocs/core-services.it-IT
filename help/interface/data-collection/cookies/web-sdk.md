---
title: Cookie di Adobe Experience Platform Web SDK
description: Scopri in che modo l’SDK web utilizza i cookie applicabili alla tua implementazione.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: d69af76f6deff4f2b73e67ee7b69b9fee1ee3a2e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Cookie di Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utilizza i cookie per memorizzare valori specifici dell’implementazione.

| Nome | Età massima | Dimensione | Descrizione |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000 (395 giorni) | 100-120 byte (variabile) | Memorizza l’ECID, così come altre informazioni relative all’ECID. |
| **kndctr_&lt;ORG_ID>_consent** | 15552000 (180 giorni) | 10-11 byte | Memorizza le preferenze di consenso dell&#39;utente per il sito Web. |
| **kndctr_&lt;ORG_ID>_cluster** | 1800 (30 minuti) | 3-5 byte | Memorizza l&#39;area dell&#39;Edge Network che soddisfa le richieste dell&#39;utente corrente. L’area viene utilizzata nel percorso URL in modo che l’Edge Network possa indirizzare la richiesta all’area corretta. Se un utente si connette con un indirizzo IP diverso o in una sessione diversa, la richiesta viene nuovamente indirizzata all’area più vicina. |
| **mbox** | 63072000 (2 anni) | | Presente quando l’impostazione di migrazione di Target è impostata su true. Consente al cookie [mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) di destinazione di essere impostato dall&#39;SDK Web. |
| **mboxEdgeCluster** | 1800 (30 minuti) | | Presente quando l’impostazione di migrazione di Target è impostata su true. Consente all&#39;SDK Web di comunicare il cluster Edge corretto a `at.js` in modo che i profili di Target possano rimanere sincronizzati mentre gli utenti navigano attraverso un sito. |
| **AMCV_###@AdobeOrg** | 34128000 (395 giorni) | | Presente quando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) è abilitato. È utile per la transizione a Web SDK quando alcune parti del sito utilizzano ancora `visitor.js`. |

L&#39;Edge Network imposta tutti i cookie con gli attributi `secure` e `sameSite="none"`. Se al momento sul sito web sono presenti sezioni protette e non protette, l’identificazione dell’utente potrebbe non essere accurata. Quando un utente passa da una sezione protetta del sito a una sezione non protetta, l&#39;Edge Network genera un nuovo `ECID` con la richiesta.
