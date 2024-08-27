---
title: Raccolta di dati regionali
description: Scopri la raccolta dati regionali in Experience Cloud.
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Raccolta di dati regionali

Adobe Experience Cloud utilizza la raccolta dati regionali (RDC) in modo che le interazioni tra i visitatori e l’Adobe avvengano il più vicino possibile ai visitatori. I dati raccolti localmente in un sito Edge vengono inoltrati in modo sicuro a un sito core per l’elaborazione. Una volta elaborati, i dati sono disponibili per i prodotti e i servizi Adobe Experience Cloud.

Il flusso di lavoro di raccolta dati regionali offre diversi vantaggi:

* **Prestazioni**: con RDC, i visitatori si connettono al sito Edge più vicino. Questa ottimizzazione fornisce il tempo di risposta più veloce, con conseguente tracciamento più preciso e tempi di caricamento più rapidi.
* **Ridondanza**: in caso di interruzione delle comunicazioni tra un sito Edge e un sito Core, l&#39;infrastruttura di Adobe salva i dati localmente e li inoltra al sito Core al ripristino delle comunicazioni. Adobe può anche indirizzare il traffico ad altri siti edge se in una posizione specifica si verificano interruzioni.

Attualmente RDC include le seguenti posizioni (soggette a modifica):

## Raccolta di dati di prime parti

| Tipo RDC | Data Collection Center |
| --- | --- |
| Globale (impostazione predefinita) | Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Globale + Cina* | Pechino*, Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Solo Americhe | Oregon, Virginia |
| Solo Europa | Irlanda, Parigi |
| Solo Asia Pacifico | Mumbai, Singapore, Tokyo, Sydney |
| Solo Cina* | Pechino |

{style="table-layout:auto"}

_*China RDC richiede il pacchetto del componente aggiuntivo China Performance Optimization e si applica solo ad Adobe Analytics utilizzando la raccolta dati di AppMeasurement. Altri servizi Experience Cloud e la raccolta dati dell’SDK per web non sono supportati. Per ulteriori informazioni sul pacchetto del componente aggiuntivo di ottimizzazione delle prestazioni per la Cina, contatta il tuo account Adobe._

## Raccolta di dati di terze parti

La raccolta dati di terze parti include domini di cookie che non corrispondono al dominio del sito Web. Gli esempi includono `adobedc.net`, `omtrdc.net` e `2o7.net`.

| Tipo RDC | Data Collection Center |
| --- | --- |
| Predefinito | Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Predefinito + Cina* | Pechino*, Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |

{style="table-layout:auto"}
