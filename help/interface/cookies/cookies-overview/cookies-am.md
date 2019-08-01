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
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Audience Manager Cookies{#audience-manager-cookies}

Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse. Questi includono elementi come assegnazione di ID, chiamate dati di registrazione, tracciamento degli errori e test per verificare se i cookie possono essere impostati. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.

Sommario:

<ul class="simplelist"> 
 <li> <a href="../cookies-overview/cookies-am.md#section-089407f3e2fe4f489b97164df3cd036c" format="dita" scope="local"> Cookie demdex </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-a71050d788d54350adc6b3f6ebf32398" format="dita" scope="local"> Cookie dextp </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-670ae9e671874576b528b46e8a1d24ac" format="dita" scope="local"> Cookie dstjs </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-0d1fea09c83249dfa944cc028a8ef840" format="dita" scope="local"> cookie_ dp </a> </li> 
</ul>

## demdex Cookie {#section-089407f3e2fe4f489b97164df3cd036c}

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
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie per assegnare un ID univoco a un visitatore del sito. The <span class="wintitle"> demdex </span> cookie helps <span class="keyword"> Audience Manger </span> perform basic functions such as visitor identification, ID synchronization, segmentation, modeling, reporting, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p>The <span class="wintitle"> demdex </span> cookie contains a Unique User ID (UUID) as shown in the example below: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>See also, <a href="https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html" format="https" scope="external"> Index of IDs in Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Lifetime: The <span class="wintitle"> demdex </span> cookie has a time-to-live (TTL) interval of 180-days. Il TTL viene reimpostato su 180 giorni su ogni interazione dell'utente con un sito Web partner. Il cookie scade se un utente non torna al sito entro l'intervallo TTL. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Target </span> string if a user opts-out of data collection. In questo caso, il cookie TTL è impostato come 10 anni. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## dextp Cookie {#section-a71050d788d54350adc6b3f6ebf32398}

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
   <td colname="col2"> <p>The <span class="wintitle"> dextp </span> cookie contains a data provider name or ID and a UNIX UTC timestamp formatted as pipe-delimited strings. In the examples, <i>italics</i> represents a variable placeholder. </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Old style: <span class="codeph"> <span class="varname"> data provider name here </span>-1490307822097| <span class="varname"> data provider name here </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">New style: <span class="codeph"> 21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>Vedere anche la sezione di sintassi dati dextp di seguito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Lifetime: The <span class="wintitle"> dextp </span> cookie has a time-to-live (TTL) interval of 180-days. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Target </span> string if a user opts-out of data collection. In questo caso, il cookie TTL è impostato come 10 anni. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Dextp Cookie Data Syntax**

The following table lists and defines the elements in a [!DNL dextp] cookie by location in the data string.

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
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Syntax: <span class="codeph"> <span class="varname"> data provider name </span> - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Example: <span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Il cookie di stile precedente identifica il provider di dati con un nome leggibile. </p> <p> <b>Nuova formattazione stile:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Syntax: <span class="codeph"> <span class="varname"> data provider ID </span> - 1|2 - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Example: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
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

## dst Cookie {#section-670ae9e671874576b528b46e8a1d24ac}

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
   <td colname="col2"> <p> The <span class="wintitle"> DST </span> cookie contains sets of destination IDs and UNIX time-stamps formatted as pipe-delimited strings. In the examples, <i>italics</i> represents a variable placeholder. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Syntax: <span class="codeph"> <span class="varname"> destination ID </span> - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Example: <span class="codeph"> 067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Lifetime: The <span class="wintitle"> dst </span> cookie has a time-to-live (TTL) interval of 180-days. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Target </span> string if a user opts-out of data collection. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## _dp Cookie {#section-0d1fea09c83249dfa944cc028a8ef840}

Questo è un cookie temporaneo. [!DNL Audience Manager] tenta di impostare il [!DNL _dp] cookie per determinare se può impostare altri cookie nel dominio demdex. net in un contesto di terze parti. When [!DNL _dp] is set it contains a value of 1. [!DNL Audience Manager] legge questo valore e rimuove immediatamente il cookie. If the [!DNL _dp] cookie is not present, [!DNL Audience Manager] knows it cannot set cookies.

>[!MORE_LIKE_THIS]
>
>* [Informazioni sulle chiamate al dominio demdex](https://marketing.adobe.com/resources/help/en_US/aam/demdex-calls.html)
>* [Centro per la privacy Adobe](http://www.adobe.com/privacy.html)
>* [Protezione dei dati e privacy di Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/c_data_security_and_privacy.html)
>* [Domande frequenti sulla privacy e sulla conservazione dei dati di Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/faq_privacy.html)

