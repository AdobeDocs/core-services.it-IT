---
description: Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse. Questi includono elementi come assegnazione di ID, chiamate dati di registrazione, tracciamento degli errori e test per verificare se i cookie possono essere impostati. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.
keywords: cookie
seo-description: Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse. Questi includono elementi come assegnazione di ID, chiamate dati di registrazione, tracciamento degli errori e test per verificare se i cookie possono essere impostati. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.
seo-title: Cookie Audience Manager
solution: Marketing Cloud, Audience Manager
title: Cookie Audience Manager
uuid: 8 b 384 c 38-b 85 a -4 e 93-b 00 e -41 a 9 d 3 ae 2 b 21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7137e608ddece5bf2a3983b3b18909ba89d607a6

---


# Cookie Audience Manager{#audience-manager-cookies}

Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse. Questi includono elementi come assegnazione di ID, chiamate dati di registrazione, tracciamento degli errori e test per verificare se i cookie possono essere impostati. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.

**Cookie demdex**

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalità</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie per assegnare un ID univoco a un visitatore del sito. Il cookie <span class="wintitle"> demdex </span> aiuta <span class="keyword"> Audience Manager </span> a eseguire funzioni di base come identificazione dei visitatori, sincronizzazione ID, segmentazione, modellazione, reporting ecc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p>Il cookie <span class="wintitle"> demdex </span> contiene un ID utente univoco (UUID) come mostrato nell'esempio di seguito: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>Vedi anche <a href="https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html" format="https" scope="external"> Indice degli ID in Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Durata: Il cookie <span class="wintitle"> demdex </span> ha un intervallo time-to-live (TTL) di 180 giorni. Il TTL viene reimpostato su 180 giorni su ogni interazione dell'utente con un sito Web partner. Il cookie scade se un utente non torna al sito entro l'intervallo TTL. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Rinuncia: <span class="keyword"> Audience Manager </span> ripristina il cookie con una <span class="codeph"> stringa Non Target </span> se un utente rinuncia alla raccolta di dati. In questo caso, il cookie TTL è impostato come 10 anni. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie dextp**

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalità</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie per registrare l'ultima volta che ha eseguito una chiamata di sincronizzazione dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p>Il cookie <span class="wintitle"> dextp </span> contiene un nome provider di dati o un ID e una marca temporale UNIX UTC formattata come stringhe delimitate dal vettore. In questi esempi, <i>il corsivo</i> rappresenta un segnaposto variabile. </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Stile precedente: <span class="codeph"><span class="varname"> nome provider dati </span>-1490307822097| <span class="varname"> nome provider dati </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">Nuovo stile: <span class="codeph"> 21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>Vedere anche la sezione di sintassi dati dextp di seguito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Durata: Il cookie <span class="wintitle"> dextp </span> ha un intervallo time-to-live (TTL) di 180 giorni. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Rinuncia: <span class="keyword"> Audience Manager </span> ripristina il cookie con una <span class="codeph"> stringa Non Target </span> se un utente rinuncia alla raccolta di dati. In questo caso, il cookie TTL è impostato come 10 anni. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

dextp Cookie Data Syntax:

Nella tabella seguente sono elencati e definiti gli elementi di un [!DNL dextp] cookie per posizione nella stringa di dati.

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Posizione variabile </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>First o Second</b> </p> </td> 
   <td colname="col2"> <p>La posizione del nome o dell'ID del fornitore di dati varia a seconda se il cookie utilizza la formattazione di stile nuova o precedente. </p> <p> <b>Formattazione stile precedente:</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Sintassi: <span class="codeph"><span class="varname"> nome provider dati </span> - <span class="varname"> Marca temporale UNIX UTC </span></span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Esempio: <span class="codeph"> Dataprovider 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Il cookie di stile precedente identifica il provider di dati con un nome leggibile. </p> <p> <b>Nuova formattazione stile:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Sintassi: <span class="codeph"><span class="varname"> ID provider dati </span> - 1|2 - <span class="varname"> Marca temporale UNIX UTC </span></span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Esempio: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Il nuovo cookie stile: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">Sostituisce il nome del provider di dati leggibile con un ID numerico. </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">Identifica il tipo di chiamata con ID 1 o ID 2. ID 1 rappresenta una chiamata di sincronizzazione ID. ID 2 rappresenta una chiamata obsoleta non più utilizzata. Non dovresti visualizzare i cookie dextp con ID 2. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Last (Ultimo)</b> </p> </td> 
   <td colname="col2"> <p>L'ultima posizione contiene una marca temporale UNIX UTC. </p> </td> 
  </tr> 
 </tbody> 
</table>

**cookie dst**

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalità</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie in caso di errore durante l'invio di dati a <a href="https://marketing.adobe.com/resources/help/en_US/aam/c_destinations.html" format="https" scope="external"> una destinazione </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p> Il <span class="wintitle"> cookie DST </span> contiene set di ID di destinazione e timbri ora UNIX formattati come stringhe delimitate dal flusso. In questi esempi, <i>il corsivo</i> rappresenta un segnaposto variabile. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Sintassi: <span class="codeph"><span class="varname"> ID di destinazione </span> - <span class="varname"> Marca temporale UNIX UTC </span></span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Esempio: <span class="codeph"> 067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Durata: Il <span class="wintitle"></span> cookie dst ha un intervallo time-to-live (TTL) di 180 giorni. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Rinuncia: <span class="keyword"> Audience Manager </span> ripristina il cookie con una <span class="codeph"> stringa Non Target </span> se un utente rinuncia alla raccolta di dati. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**cookie_ dp**

Questo è un cookie temporaneo. [!DNL Audience Manager] tenta di impostare il [!DNL _dp] cookie per determinare se può impostare altri cookie nel dominio demdex. net in un contesto di terze parti. Quando [!DNL _dp] è impostato, contiene un valore pari a 1. [!DNL Audience Manager] legge questo valore e rimuove immediatamente il cookie. Se il [!DNL _dp] cookie non è presente [!DNL Audience Manager] , sa che non può impostare cookie.