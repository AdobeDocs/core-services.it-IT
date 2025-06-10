---
description: Scopri come il servizio ID viene memorizzato e utilizzato nelle applicazioni di Experience Cloud.
solution: Experience Cloud,Analytics,Target
title: Cookie di Experience Cloud
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bd9bea58-9987-40d6-84e0-da185388bbbb
source-git-commit: 2073400a04933226bd036c1fcd729df70f101df3
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 88%

---

# Cookie di Experience Cloud

Adobe Experience Cloud utilizza i cookie per memorizzare un ID visitatore utilizzato nelle applicazioni Experience Cloud. Questi cookie sono specifici per l&#39;accesso alle applicazioni Adobe Experience Cloud in [experience.adobe.com](https://experience.adobe.com).

**Nome cookie: s_ecid**

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p> Contiene una copia dell’Experience Cloud ID (ECID) o del MID. Il MID viene memorizzato in una coppia chiave/valore con sintassi s_ecid=MCMID|&lt;ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Scadenza </p> </td> 
   <td colname="col2"> <p>2 anni, anche se la maggior parte dei browser moderni troncano a 13 mesi</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Utilizzo </p> </td> 
   <td colname="col2"> <p>Questo cookie viene impostato dal dominio del cliente dopo che il cookie AMCV è stato impostato dal client. Questo cookie ha lo scopo di consentire il tracciamento degli ID permanenti nello stato di prima parte e viene utilizzato come ID di riferimento se il cookie AMCV è scaduto. Vedi Cookie AMCV qui per ulteriori dettagli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Posizione </p> </td> 
   <td colname="col2"> <p>Solo clienti CNAME. Non applicabile in caso di terze parti. Il cookie è memorizzato nel tuo dominio, lo stesso utilizzato dal CNAME e dalla richiesta di immagine Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimensione </p> </td> 
   <td colname="col2"> <p>45 byte </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> SameSite=Lax </p> </td> 
   <td colname="col2"> <p>I cookie con questa impostazione vengono inviati solo quando il dominio visualizzato nell’URL del browser corrisponde al dominio del cookie. Questa è la nuova impostazione predefinita per i cookie in Chrome.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Nome cookie: AMCV_###@AdobeOrg**

Il [servizio ID di Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) utilizza JavaScript per memorizzare un ID visitatore univoco in un cookie `AMCV_###@AdobeOrg` sul dominio del sito web corrente, dove `###` rappresenta una stringa casuale di caratteri come `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

Consulta anche [Cookie e il servizio ID](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=it).

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p> ID visitatore univoci utilizzati dalle soluzioni Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Scadenza </p> </td> 
   <td colname="col2"> <p> 13 mesi </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Utilizzo </p> </td> 
   <td colname="col2"> <p> Questo cookie viene usato per identificare un visitatore univoco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Posizione </p> </td> 
   <td colname="col2"> <p> Questo cookie viene memorizzato nel dominio del sito Web (non nel dominio della richiesta di immagine). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimensione </p> </td> 
   <td colname="col2"> <p> Può variare, nella maggior parte dei casi questo cookie è lungo circa 200 byte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nessun valore aggiunto. Chrome utilizza Lax per impostazione predefinita. </p> </td> 
   <td colname="col2"> <p> I cookie con questa impostazione vengono inviati solo quando il dominio visualizzato nell’URL del browser corrisponde al dominio del cookie. Questa è la nuova impostazione predefinita per i cookie in Chrome. </p> </td> 
  </tr> 
 </tbody> 
</table>
