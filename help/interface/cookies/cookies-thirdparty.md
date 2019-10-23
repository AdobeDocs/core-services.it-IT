---
description: Poiché il supporto dei cookie di terze parti è diventato sempre più limitato nei vari browser, Adobe ha lavorato a nuove soluzioni che bilanciano con attenzione i requisiti dei clienti con il diritto alla privacy del consumatore nelle soluzioni Adobe Experience Cloud.
keywords: cookie;privacy
seo-description: Poiché il supporto dei cookie di terze parti è diventato sempre più limitato nei vari browser, Adobe ha lavorato a nuove soluzioni che bilanciano con attenzione i requisiti dei clienti con il diritto alla privacy del consumatore nelle soluzioni Adobe Experience Cloud.
seo-title: Effetti delle modifiche al supporto dei cookie di terze parti sui clienti
solution: Experience Cloud,Analytics,Target,Social
title: Effetti delle modifiche al supporto dei cookie di terze parti sui clienti
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: 012283d79bda42f9dabb20b25903927b075f6d54

---


# Effetti delle modifiche al supporto dei cookie di terze parti sui clienti{#how-changes-to-third-party-cookie-support-impacts-customers}

Poiché il supporto dei cookie di terze parti è diventato sempre più limitato nei vari browser, Adobe ha lavorato a nuove soluzioni che bilanciano con attenzione i requisiti dei clienti con il diritto alla privacy del consumatore nelle soluzioni Adobe Experience Cloud.

L’elenco seguente illustra l’effetto dei cookie di terze parti sulle implementazioni correnti delle soluzioni Adobe Experience Cloud:

## Adobe Analytics e Adobe Target

* Per i clienti con un’[implementazione di prima parte](/help/interface/cookies/cookies-first-party.md), l’effetto è quasi nullo.
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* Poiché Adobe Experience Manager funziona interamente all’interno del dominio del cliente, l’interazione con i cookie di terze parti è minima e, di conseguenza, anche l’impatto è minimo.

## Adobe Social

* Social non viene interessato se il cliente dispone della versione più recente del codice.

## Adobe Advertising Cloud

* Cerca:

   * Se la ricerca è ottimizzata in base ai dati di Adobe Analytics, viene influenzata nello stesso modo di Adobe Analytics.
   * La raccolta dei dati di conversione non dovrebbe subire modifiche.

* Visualizzazione:

   * La visualizzazione quotidiana del remarketing dipende completamente dall’utilizzo dei cookie di terze parti.
   * La visualizzazione dipende in modo importante anche dalla disponibilità di vari cookie di rete pubblicitari per la sincronizzazione.
   * L’impatto generale è sconosciuto. Tuttavia, per quanto riguarda il primo punto, la visualizzazione è interessata più di altri servizi.
   * Stiamo lavorando internamente e con i nostri partner pubblicitari per valutare appieno l’impatto sulla distribuzione degli annunci.

* Social:

   * Non c’è alcun impatto sugli annunci marketplace di Facebook.
   * L’impatto su Facebook Exchange (FBX) è lo stesso della visualizzazione degli annunci.

