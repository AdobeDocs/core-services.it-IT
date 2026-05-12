---
title: Raccolta di dati regionali
description: Scopri la raccolta dati regionali in CX Enterprise.
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 0%

---

# Raccolta di dati regionali

Adobe CX Enterprise utilizza la raccolta dati regionali (Regional Data Collection, RDC), in modo che le interazioni tra i visitatori e Adobe si verifichino il più vicino possibile ai visitatori. I dati raccolti localmente in un sito Edge vengono inoltrati in modo sicuro a un sito core per l’elaborazione. Una volta elaborati, i dati sono disponibili per i prodotti e i servizi aziendali di Adobe CX.

Il flusso di lavoro di raccolta dati regionali offre diversi vantaggi:

* **Prestazioni**: con RDC, i visitatori si connettono al sito Edge più vicino. Questa ottimizzazione fornisce il tempo di risposta più veloce, con conseguente tracciamento più preciso e tempi di caricamento più rapidi.
* **Ridondanza**: in caso di interruzione delle comunicazioni tra un sito Edge e un sito Core, l&#39;infrastruttura Adobe salva i dati localmente e li inoltra al sito Core al ripristino delle comunicazioni. Adobe può anche indirizzare il traffico ad altri siti edge se in una posizione specifica si verificano interruzioni.

## Raccolta di dati di prime parti

La raccolta dati di prime parti utilizza un’implementazione CNAME per indirizzare i dati ad Adobe tramite il tuo dominio. Il tipo di RDC è selezionato come parte del processo di installazione di [Programma di certificazione gestito da Adobe](adobe-managed-cert.md). Per verificare o aggiornare il tipo di RDC, contatta il team del tuo account Adobe. Sono disponibili i seguenti tipi di RDC e i centri dati associati:

| Tipo RDC | Data Collection Center |
| --- | --- |
| Globale (impostazione predefinita) | Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Globale + Cina* | Pechino*, Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Solo Americhe | Oregon, Virginia |
| Solo Europa | Irlanda, Parigi |
| Solo Asia Pacifico | Mumbai, Singapore, Tokyo, Sydney |
| Solo Cina* | Pechino |

_*China RDC richiede il pacchetto aggiuntivo China Performance Optimization e si applica solo ad Adobe Analytics che utilizza la raccolta dati di AppMeasurement. Altri servizi aziendali CX e la raccolta dati Web SDK non sono supportati. Contatta il team del tuo account Adobe per ulteriori informazioni sul pacchetto del componente aggiuntivo di ottimizzazione delle prestazioni per la Cina._

## Raccolta di dati di terze parti

La raccolta dati di terze parti utilizza domini di cookie che non corrispondono al dominio del sito Web. Gli esempi includono `adobedc.net`, `omtrdc.net` e `2o7.net`.

| Tipo RDC | Data Collection Center |
| --- | --- |
| Predefinito | Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |
| Predefinito + Cina* | Pechino*, Oregon, Virginia, Irlanda, Parigi, Mumbai, Singapore, Tokyo, Sydney |

_*Richiede il pacchetto aggiuntivo China Performance Optimization. Per ulteriori dettagli, vedere la sezione precedente relativa alla raccolta dati di prime parti._
