---
description: Scopri come funzionano i cookie di Adobe Analytics in Adobe CX Enterprise.
solution: Analytics
title: Cookie di Adobe Analytics
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
TQID: https://experienceleague.adobe.com/H-N88ygcQUcUIej1Kkwlv9UmIe1qPDYwo-qF3TdDqHg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 10%

---

# Cookie di Adobe Analytics

Adobe Analytics utilizza i cookie per differenziare le richieste di browser diversi e memorizzare informazioni utili che un’applicazione può utilizzare in un secondo momento. Possono inoltre essere utilizzati per associare le informazioni di navigazione ai record dei clienti.

Analytics utilizza i cookie per definire nuovi visitatori in modo anonimo, aiutare ad analizzare i dati di clickstream e monitorare le attività storiche sul sito web, ad esempio la risposta a campagne particolari o la lunghezza del ciclo di vendita.

| Nome cookie | Scadenza | Dimensione | Posizione | Descrizione |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 mesi | 45 byte | Prime parti | Memorizza il CX Enterprise ID (ECID) o MID. Impostato dalla risposta HTTP. Il MID è archiviato nel formato `s_ecid=MCMID`. Impostato dopo che il client ha impostato il cookie AMCV. Consente il tracciamento ID persistente di prime parti e viene utilizzato come ID di riferimento se il cookie AMCV scade. `SameSite` è impostato su &quot;Lax&quot;. Se utilizzi il Web SDK per implementare Adobe Analytics, la scadenza dei cookie è impostata su 2 anni; tuttavia, la maggior parte dei browser moderni tronca la scadenza a 13 mesi. |
| **`s_cc`** | Session | 4 byte | Prime parti | Determina se i cookie sono abilitati. Impostato da JavaScript. |
| **`s_sq`** | Session | 100-200 byte | Prime parti | Utilizzato da Activity Map. Contiene informazioni sul collegamento precedente su cui il visitatore ha fatto clic. Impostato da JavaScript. |
| **`s_vi`** | 2 anni | 44 byte | Prime parti o `*.omtrdc.net` (terze parti) | Memorizza un ID visitatore univoco e una marca temporale. Impostato dalla risposta HTTP. Ogni ID visitatore è associato a un profilo visitatore sui server Adobe. I profili dei visitatori vengono eliminati dopo 1 anno di inattività, indipendentemente dalla scadenza del cookie ID visitatore. Il flag `Secure` è impostato quando `SameSite` è &quot;None&quot; e la connessione è HTTPS. `SameSite` è &quot;Lax&quot; per impostazione predefinita per i cookie di prime parti. `SameSite` è &quot;None&quot; quando si utilizzano cookie di terze parti, ad esempio in `omtrdc.net` o `2o7.net`. Impostare `SameSite` su &quot;None&quot; quando si utilizza un singolo CNAME per tenere traccia di più domini o proprietà. |
| **`s_fid`** | 2 anni | 33 byte | Prime parti | Memorizza l’ID visitatore univoco e la marca temporale di fallback. Impostato da JavaScript se il cookie standard `s_vi` non può essere impostato a causa di restrizioni dei cookie di terze parti. Non utilizzato per le implementazioni di cookie di prime parti. |
| **`s_ac`** | Immediato | 1 byte | Prime parti | Consente di determinare il dominio corretto per impostare i cookie di AppMeasurement. Contiene il valore statico `"1"`. Una volta impostato, il cookie viene eliminato immediatamente. |

Consulta [Identificazione dei visitatori in Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview) per ulteriori informazioni su come Adobe Analytics identifica i visitatori utilizzando i cookie.

## Cookie impostati da plug-in

Alcune implementazioni fanno uso di plug-in, che sono snippet di codice che forniscono funzionalità aggiuntive per Analytics. Questi plug-in possono impostare cookie non elencati sopra. Per un elenco dei plug-in disponibili e dei cookie impostati, vedere [Panoramica dei plug-in di Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins).

## Conseguenze dell’eliminazione dei cookie di Analytics

Se un visitatore elimina i suoi cookie di Analytics, considera quanto segue:

* **Identificazione visitatore persa:** Quando i cookie vengono eliminati, Adobe Analytics non è in grado di riconoscere i visitatori ritornati. La prossima volta che l’utente visita il tuo sito, viene conteggiato come un nuovo visitatore.
* **La continuità della sessione è interrotta:** Qualsiasi analisi basata su sessione o su più visite (come il tracciamento di attribuzione o conversione) è interrotta. Gli eventi e le conversioni che si verificano dopo l’eliminazione dei cookie non possono essere legati alle attività precedenti dello stesso utente.
* **Personalization e segmentazione sono interessati:** i segmenti o le esperienze personalizzate in base alla cronologia o al comportamento del visitatore vengono reimpostati, in quanto i dati precedenti non sono più associati alla visita corrente.
* **Il monitoraggio tra più domini è interrotto:** Per i cookie di terze parti, l&#39;eliminazione impedisce ad Adobe Analytics di collegare l&#39;attività dell&#39;utente tra più domini di cui sei proprietario.

