---
description: Scopri come il supporto dei cookie di terze parti viene sempre più limitato nei vari browser.
keywords: cookie;privacy
solution: Experience Cloud,Analytics,Target
title: 'Effetti delle modifiche al supporto dei cookie di terze parti sui clienti  '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookie
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: c7ed1324015beb7ebcf7a4ee21b05601e36e608f
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 59%

---

# Effetti delle modifiche al supporto dei cookie di terze parti sui clienti {#how-changes-to-third-party-cookie-support-impacts-customers}

Il supporto per i cookie di terze parti è diventato più limitato tra i vari browser. In quanto tale, Adobe ha lavorato a nuove soluzioni che bilanciano con attenzione i requisiti dei clienti con il diritto alla privacy del consumatore in tutte le applicazioni Experience Cloud.

L’elenco seguente illustra l’impatto del supporto dei cookie di terze parti sulle implementazioni correnti delle applicazioni Experience Cloud:

## Adobe Analytics e Adobe Target

* Analytics e Target non sono in gran parte interessati, in quanto la stessa attività del sito si basa solo sui cookie di prime parti. I cookie di terze parti sono necessari per comprendere l’attività dell’utente su più domini. Per i browser in cui i cookie di terze parti sono bloccati, il tracciamento tra domini diversi non è possibile utilizzando i cookie.

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
   * Adobe sta lavorando internamente e con i partner pubblicitari di Adobe per valutare appieno l’impatto sulla distribuzione degli annunci.