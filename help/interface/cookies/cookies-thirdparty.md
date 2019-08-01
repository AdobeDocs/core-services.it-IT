---
description: Poiché il supporto dei cookie di terze parti è diventato sempre più limitato tra i vari browser, Adobe sta lavorando su nuove soluzioni che bilanciano con attenzione i requisiti del cliente, con il diritto del consumatore alla privacy tra le soluzioni Adobe Experience Cloud.
keywords: cookie; privacy
seo-description: Poiché il supporto dei cookie di terze parti è diventato sempre più limitato tra i vari browser, Adobe sta lavorando su nuove soluzioni che bilanciano con attenzione i requisiti del cliente, con il diritto del consumatore alla privacy tra le soluzioni Adobe Experience Cloud.
seo-title: Informazioni sulle modifiche al supporto dei cookie di terze parti influiscono sui clienti
solution: Marketing Cloud, Analytics, Target, Social
title: Informazioni sulle modifiche al supporto dei cookie di terze parti influiscono sui clienti
uuid: 27332 e 0 d -6932-4 a 6 e-b 97 b -0 adeced 0 b 050
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# How Changes to Third Party Cookie Support Impacts Customers{#how-changes-to-third-party-cookie-support-impacts-customers}

Poiché il supporto dei cookie di terze parti è diventato sempre più limitato tra i vari browser, Adobe sta lavorando su nuove soluzioni che bilanciano con attenzione i requisiti del cliente, con il diritto del consumatore alla privacy tra le soluzioni Adobe Experience Cloud.

L'elenco seguente illustra in che modo il supporto dei cookie di terze parti influisce su implementazioni correnti delle soluzioni Adobe Experience Cloud:

**Adobe Analytics e Target**

<!--
Test
-->

* I clienti con implementazione di prime parti rimangono in gran parte inalterati.
* Customers that are not using first-party implementation can implement the [Visitor ID service](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=visid_service) to store the ID cookie as a first-party cookie without a first-party implementation.

**Adobe Experience Manager**

* Poiché Adobe Experience Manager funziona interamente all'interno del dominio del cliente, c'è un'interazione minima con i cookie di terze parti e, di conseguenza, minimo.

**Adobe Social**

* Social non viene interessato se il cliente dispone della versione più recente del codice.

**Adobe Media Optimizer**

* Cerca:

   * Dove la ricerca è ottimizzata in base ai dati di Adobe Analytics, la ricerca viene influenzata nello stesso modo di Adobe Analytics.
   * La raccolta dei dati di conversione non deve essere modificata.

* Visualizzazione:

   * La visualizzazione di remarketing oggi dipende completamente dall'utilizzo dei cookie di terze parti.
   * La visualizzazione dipende anche dalla disponibilità di vari cookie di rete pubblicitari per la sincronizzazione.
   * L'impatto generale è sconosciuto. Tuttavia, per il primo punto, la visualizzazione è interessata più di altri servizi.
   * Stiamo lavorando internamente e con i nostri partner pubblicitari per valutare appieno l'impatto sulla distribuzione degli annunci.

* Social:

   * Non c'è alcun impatto sugli annunci marketplace di Facebook.
   * Facebook Exchange (FBX) verrà modificato come la distribuzione degli annunci visualizzati.

