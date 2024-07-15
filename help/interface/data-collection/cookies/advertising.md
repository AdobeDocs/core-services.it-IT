---
description: Scopri alcuni cookie di Adobe Advertising per la mappatura degli eventi di coinvolgimento e di conversione e, potenzialmente, come utilizzarli per ottimizzare le offerte di annunci.
title: Cookie di Adobe Advertising
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 4d2dc1e6126e26f61475efbd33efe98bd47153d5
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 13%

---

# Cookie di Adobe Advertising

Adobe Advertising (precedentemente Adobe Advertising Cloud) utilizza i cookie per mappare gli eventi di coinvolgimento pubblicitario su eventi di conversione e, potenzialmente, per ottimizzare le offerte pubblicitarie.

>[!NOTE]
>
>Il tag JavaScript di Adobe Advertising beta che utilizza il servizio [Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) crea cookie [Experience Cloud](experience-cloud.md) di prime parti `s_ecid`, non cookie Adobe Advertising.

| Nome cookie | Scadenza | Dimensione | Posizione | Descrizione |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 minuti | 52 byte | `everesttech.net` | Memorizza ID e timestamp dei clic di visualizzazione. Determina se un evento di clic su un annuncio visualizzato si applica a un hit di Adobe Analytics. |
| **`_tmae`** | 1 anno | 1 KB | `everesttech.net` | Memorizza ID codificati e marche temporali per il coinvolgimento degli annunci utilizzando il tracciamento DSP. Include il coinvolgimento degli utenti con gli annunci, come ad esempio l’ultimo annuncio visto |
| **`_tmid`** | 1 anno | ~ 20 byte | `everesttech.net` | Memorizza l’ID del Demand Side Platform DSP (Adobe Advertising). Corrisponde all&#39;ID visitatore nel cookie `everest_g_v2`. |
| **`adcloud`** | 1 anno | 50-150 byte | Prime parti | I timestamp dell’ultima visita del visitatore al sito web e l’ultimo clic di ricerca del visitatore. Memorizza anche `ef_id` creato quando il visitatore ha fatto clic su un annuncio. Associa l’ID visitatore ai segmenti di pubblico e alle conversioni rilevanti. Consente di ottimizzare i tempi di caricamento delle pagine evitando inutili richieste di Adobe. |
| **`ev_sync_*`** |  | 8 byte | `everesttech.net` | Data di esecuzione della sincronizzazione nel formato `yyymmdd`. Sincronizza l’ID visitatore dell’Adobe Advertising con lo scambio di annunci partner. Viene creato per i nuovi visitatori e invia una richiesta di sincronizzazione quando è scaduto. Include i cookie `ev_sync_ax`, `ev_sync_bk`, `ev_sync_dd`, `ev_sync_fs`, `ev_sync_ix`, `ev_sync_nx`, `ev_sync_ox`, `ev_sync_pm`, `ev_sync_rc`, `ev_sync_tm` e `ev_sync_yh`. |
| **`everest_g_v2`** | 1 anno | ~ 27 byte | `everesttech.net` | Memorizza il browser e l’ID visitatore. Creato quando un utente fa clic inizialmente su un annuncio. Utilizzato per mappare i clic correnti e successivi con altri eventi sul sito web. |
| **`everest_session_v2`** | Session | ~ 16 byte | `everesttech.net` | Memorizza l&#39;ID sessione corrente. |
| **`id_adcloud`** | 91 giorni | 16 byte | Prime parti | Memorizza l&#39;ID visitatore. |

{style="table-layout:auto"}
