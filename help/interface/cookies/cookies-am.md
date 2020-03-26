---
description: Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse, come l’assegnazione di ID, la registrazione delle chiamate dati, il tracciamento degli errori e test per verificare se è possibile impostare i cookie. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.
keywords: cookies
seo-description: Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse, come l’assegnazione di ID, la registrazione delle chiamate dati, il tracciamento degli errori e test per verificare se è possibile impostare i cookie. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.
seo-title: Cookie di Audience Manager
solution: Marketing Cloud,Audience Manager
title: Cookie di Audience Manager
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Cookie di Audience Manager{#audience-manager-cookies}

Audience Manager si avvale di alcuni cookie semplici per eseguire funzioni diverse, come l’assegnazione di ID, la registrazione delle chiamate dati, il tracciamento degli errori e test per verificare se è possibile impostare i cookie. Questa sezione elenca e descrive i vari cookie impostati da Audience Manager.

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
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie per assegnare un ID univoco a un visitatore del sito. Il cookie <span class="wintitle"> demdex </span> aiuta <span class="keyword"> Audience Manager </span> a eseguire funzioni di base come l’identificazione dei visitatori, la sincronizzazione degli ID, la segmentazione, la modellazione, il reporting, ecc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p>Il cookie <span class="wintitle"> demdex </span> contiene un ID utente univoco (UUID) come mostrato nell’esempio di seguito: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>Vedi anche <a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/ids-in-aam.html" format="https" scope="external"> Indice degli ID in Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri Attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Durata: il cookie <span class="wintitle"> demdex </span> ha un intervallo time-to-live (TTL) di 180 giorni. Il TTL viene reimpostato su 180 giorni a ogni interazione dell’utente con un sito Web partner. Il cookie scade se un utente non torna al sito entro l’intervallo TTL. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. In questo caso, il TTL del cookie è impostato su 10 anni. </li> 
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
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie per registrare l’ultima volta che ha eseguito una chiamata di sincronizzazione dati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p>Il cookie <span class="wintitle"> dextp </span> contiene il nome o l’ID di un provider di dati e un timestamp UNIX UTC formattati come stringhe delimitate da barre verticali. In questi esempi, il <i>corsivo</i> rappresenta un segnaposto variabile. </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Stile precedente: <span class="codeph"> <span class="varname"> nome del provider dati qui </span>-1490307822097| <span class="varname"> nome del provider dati qui </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">Nuovo stile: <span class="codeph"> 21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>Vedi anche la sezione sulla sintassi dei dati di dextp di seguito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri Attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Durata: il cookie <span class="wintitle"> dextp </span> ha un intervallo time-to-live (TTL) di 180 giorni. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. In questo caso, il TTL del cookie è impostato su 10 anni. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Sintassi dei dati del cookie dextp:

La tabella seguente elenca e definisce gli elementi di un cookie [!DNL dextp] in base alla posizione nella stringa di dati.

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Posizione variabile </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Primo o secondo</b> </p> </td> 
   <td colname="col2"> <p>La posizione del nome o dell’ID del provider di dati varia in base al formato utilizzato dal cookie. </p> <p> <b>Formato precedente:</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Sintassi: <span class="codeph"> <span class="varname"> nome provider dati </span> - <span class="varname"> timestamp UNIX UTC </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Esempio: <span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Il cookie con il formato precedente identifica il provider di dati con un nome leggibile. </p> <p> <b>Nuovo formato:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Sintassi: <span class="codeph"> <span class="varname"> ID provider dati </span> - 1|2 - <span class="varname"> timestamp UNIX UTC </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Esempio: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Il cookie con il nuovo formato: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">Sostituisce il nome del provider di dati leggibile con un ID numerico. </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">Identifica il tipo di chiamata con l’ ID 1 o l’ID 2. L’ID 1 indica una chiamata di sincronizzazione degli ID. L’ID 2 indica una chiamata obsoleta non più utilizzata. Non dovresti visualizzare molti (o in assoluto) cookie dextp con ID 2. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Last (Ultimo)</b> </p> </td> 
   <td colname="col2"> <p>L’ultima posizione contiene uno timestamp UNIX UTC. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie dst**

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
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> imposta questo cookie in caso di errore durante l’invio di dati a una <a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html#purposes" format="https" scope="external"> destinazione </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenuto</b> </p> </td> 
   <td colname="col2"> <p> Il cookie <span class="wintitle"> DST </span> contiene set di ID di destinazione e timestamp UNIX formattati come stringhe delimitate da barre verticali. In questi esempi, il <i>corsivo</i> rappresenta un segnaposto variabile. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Sintassi: <span class="codeph"> <span class="varname"> ID destinazione </span> - <span class="varname"> Timestamp UNIX UTC </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Esempio: <span class="codeph"> 067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Altri Attributi</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Durata: il cookie <span class="wintitle"> dst </span> ha un intervallo time-to-live (TTL) di 180 giorni. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie _dp**

Questo è un cookie temporaneo. [!DNL Audience Manager] tenta di impostare il cookie [!DNL _dp] per determinare se può impostare altri cookie nel dominio demdex.net in un contesto di terze parti. Quando [!DNL _dp] è impostato, contiene un valore pari a 1. [!DNL Audience Manager] legge questo valore e rimuove immediatamente il cookie. Se il cookie [!DNL _dp] non è presente, [!DNL Audience Manager] sa che non può impostare cookie.