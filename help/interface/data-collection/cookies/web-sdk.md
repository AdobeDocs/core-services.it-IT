---
title: Cookie di Adobe Experience Platform Web SDK
description: Scopri in che modo il Web SDK utilizza i cookie applicabili alla tua implementazione.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 1%

---

# Cookie di Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utilizza i cookie per memorizzare valori specifici dell’implementazione.

| Nome | Età massima | Dimensione | Descrizione |
|---|---|---|---|
| **`AMCV_###@AdobeOrg`** | 34128000 (395 giorni) | 100-120 byte (variabile) | Presente quando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) è abilitato. Questa funzione risulta utile durante la transizione al Web SDK, mentre alcune parti del sito utilizzano ancora `visitor.js`. Il Web SDK legge e scrive il cookie durante la migrazione. |
| **`demdex`** | 15552000 (180 giorni) | varia | Presente se la sincronizzazione Audience Manager ID è abilitata. Audience Manager imposta questo cookie per assegnare un ID univoco e supportare la sincronizzazione, la segmentazione, la modellazione e il reporting degli ID. Vedi `demdex` in [Cookie di Audience Manager](audience-manager.md). |
| **`kndctr_<orgId>_identity`** | 34128000 (395 giorni) | 100-120 byte (variabile) | Memorizza l’ECID e altre informazioni correlate per quel dispositivo. |
| **`kndctr_<orgId>_cluster`** | 1800 (30 minuti) | 3-5 byte | Memorizza l’area Edge Network (hint di posizione) che risponde alle richieste dell’utente corrente. L’area viene utilizzata nel percorso URL in modo che Edge Network possa indirizzare la richiesta all’area corretta. Se un utente si connette con un indirizzo IP diverso entro la durata del cookie, la richiesta viene nuovamente indirizzata all’area più vicina. |
| **`kndctr_<orgId>_consent`** | 15552000 (180 giorni) | 10-11 byte | Memorizza le preferenze di consenso del visitatore. Imposta sempre indipendentemente dal consenso, in quanto memorizza le preferenze di consenso stesse. |
| **`kndctr_<orgId>_consent_check`** | 7200 (2 ore) | | Helper con ambito di sessione che indica ad Edge Network di ricontrollare il lato server del consenso dopo la scadenza del TTL. Impone un TTL sul consenso memorizzato nella cache. |
| **`kndctr_<orgId>_personalization`** | 34128000 (395 giorni) | | Memorizza le informazioni sulla sessione utilizzate da Adobe Target per personalizzare il contenuto. |
| **`mbox`** | 63072000 (2 anni) | | Presente quando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) è abilitato. Consente di impostare il cookie [mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) di destinazione dal Web SDK. |
| **`mboxEdgeCluster`** | 1800 (30 minuti) | | Presente quando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) è abilitato. Consente al Web SDK di comunicare il cluster Edge corretto a `at.js` in modo che i profili di Target possano rimanere sincronizzati mentre gli utenti navigano in un sito. |
| **`s_ecid`** | 63115200 (2 anni) | ~ 45 byte | Contiene una copia dell&#39;Experience Cloud ID (ECID/MID) nel formato `s_ecid=MCMID\|<ECID>`. Funge da backup di prima parte dell’ECID, principalmente per scenari CNAME (prime parti). |

Edge Network imposta tutti i cookie con gli attributi `secure` e `sameSite="none"`. Se al momento sul sito web sono presenti sezioni protette e non protette, l’identificazione dell’utente potrebbe non essere accurata. Quando un utente passa da una sezione protetta del sito a una non protetta, Edge Network genera un nuovo `ECID` con la richiesta.
