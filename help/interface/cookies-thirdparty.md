---
description: Scopri come il supporto dei cookie di terze parti viene sempre più limitato nei vari browser.
solution: Experience Cloud,Analytics,Target
title: Effetti delle modifiche al supporto dei cookie di terze parti sui clienti
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 100%

---

# Effetti delle modifiche al supporto dei cookie di terze parti sui clienti {#how-changes-to-third-party-cookie-support-impacts-customers}

Il supporto per i cookie di terze parti è diventato più limitato in tutti i browser. Adobe sta mettendo a punto nuove applicazioni che bilanciano con attenzione i requisiti dei clienti con il diritto alla privacy dei consumatori, per tutte le applicazioni Experience Cloud.

L’elenco seguente illustra l’effetto dei cookie di terze parti sulle implementazioni correnti delle applicazioni di Adobe Experience Cloud:

## Adobe Analytics e Adobe Target

* Analytics e Target non subiranno modifiche poiché le attività sullo stesso sito si basano solo sui cookie di prime parti. I cookie di terze parti sono necessari per comprendere l’attività dell’utente su più domini. Per i browser in cui i cookie di terze parti vengono bloccati, il tracciamento tra domini diversi non sarà possibile utilizzando i cookie.

## Adobe Experience Manager

* Poiché Adobe Experience Manager funziona interamente all’interno del dominio del cliente, l’interazione con i cookie di terze parti è minima e, di conseguenza, anche l’impatto è minimo.

## Adobe Social

* Social non dovrebbe subire modifiche se il cliente dispone della versione più recente del codice.

## Adobe Advertising Cloud

* Cerca:

   * Se la ricerca è ottimizzata in base ai dati di Adobe Analytics, viene influenzata nello stesso modo di Adobe Analytics.
   * La raccolta dei dati di conversione non dovrebbe subire modifiche.

* Visualizzazione:

   * La visualizzazione quotidiana del remarketing dipende completamente dall’utilizzo dei cookie di terze parti.
   * La visualizzazione dipende inoltre fortemente dalla disponibilità di vari cookie della rete pubblicitaria per la sincronizzazione.
   * L’impatto generale è sconosciuto. Tuttavia, per quanto riguarda il primo punto, la visualizzazione è interessata più di altri servizi.
   * Stiamo lavorando internamente e con i nostri partner pubblicitari per valutare appieno l’impatto sulla distribuzione degli annunci.
