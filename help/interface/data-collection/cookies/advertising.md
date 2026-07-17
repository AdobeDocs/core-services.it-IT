---
description: Scopri i cookie di Adobe Advertising per la mappatura degli eventi di coinvolgimento e di conversione e, potenzialmente, come utilizzarli per ottimizzare le offerte di annunci.
title: Cookie di Adobe Advertising
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
TQID: 'https://experienceleague.adobe.com/jr9RwaF63elDUN-XewIdrPNsGb6T5wo98vktP5U6jIM'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9c2010694b8bb32c3922dd65f846375e43b2caac
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 15%

---

# Cookie di Adobe Advertising

Adobe Advertising (precedentemente Adobe Advertising Cloud) utilizza i cookie per mappare gli eventi di coinvolgimento pubblicitario su eventi di conversione e, potenzialmente, per ottimizzare le offerte pubblicitarie.

>[!NOTE]
>
>Il tag JavaScript beta di Adobe Advertising che utilizza il servizio [Adobe CX Enterprise ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) crea cookie [CX Enterprise](experience-cloud.md) `s_ecid` di prime parti, non cookie di Adobe Advertising.

| Nome cookie | Scadenza | Dimensione | Posizione | Descrizione |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 minuti | 52 byte | `everesttech.net` | Memorizza ID e timestamp dei clic di visualizzazione. Determina se un evento di clic su un annuncio visualizzato si applica a un hit di Adobe Analytics. |
| **`_tmae`** | 1 anno | 1 KB | `everesttech.net` | Memorizza ID codificati e marche temporali per il coinvolgimento degli annunci utilizzando il tracciamento di DSP. Include il coinvolgimento degli utenti con gli annunci, come ad esempio l’ultimo annuncio visto |
| **`_tmid`** | 1 anno | ~ 20 byte | `everesttech.net` | Memorizza l&#39;ID di Adobe Advertising Demand Side Platform (DSP). Corrisponde all&#39;ID visitatore nel cookie `everest_g_v2`. |
| **`adcloud`** | 1 anno | 50-150 byte | Prime parti | I timestamp dell’ultima visita del visitatore al sito web e l’ultimo clic di ricerca del visitatore. Memorizza anche `ef_id` creato quando il visitatore ha fatto clic su un annuncio. Associa l’ID visitatore ai segmenti di pubblico e alle conversioni rilevanti. Consente di ottimizzare i tempi di caricamento delle pagine evitando richieste non necessarie ad Adobe. |
| **`ev_sync_*`** |  | 8 byte | `everesttech.net` | Data di esecuzione della sincronizzazione nel formato `yyymmdd`. Sincronizza l’ID visitatore di Adobe Advertising con il partner ad exchange. Viene creato per i nuovi visitatori e invia una richiesta di sincronizzazione quando è scaduto. Include i cookie `ev_sync_ax`, `ev_sync_bk`, `ev_sync_dd`, `ev_sync_fs`, `ev_sync_ix`, `ev_sync_nx`, `ev_sync_ox`, `ev_sync_pm`, `ev_sync_rc`, `ev_sync_tm` e `ev_sync_yh`. |
| **`everest_g_v2`** | 1 anno | ~ 27 byte | `everesttech.net` | Memorizza il browser e l’ID visitatore. Creato quando un utente fa clic inizialmente su un annuncio. Utilizzato per mappare i clic correnti e successivi con altri eventi sul sito web. |
| **`everest_session_v2`** | Session | ~ 16 byte | `everesttech.net` | Memorizza l&#39;ID sessione corrente. |
| **`id_adcloud`** | 91 giorni | 16 byte | Prime parti | Memorizza l&#39;ID visitatore. |

{style="table-layout:auto"}

