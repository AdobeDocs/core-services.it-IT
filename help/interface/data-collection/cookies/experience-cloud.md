---
description: Scopri come il Servizio ID visitatore viene memorizzato e utilizzato nelle applicazioni CX Enterprise.
solution: Experience Cloud,Analytics,Target
title: Cookie di Experience Cloud
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bd9bea58-9987-40d6-84e0-da185388bbbb
TQID: https://experienceleague.adobe.com/2i8AyRTW37TGYTpcLBh-ZMTyET0NvpRweTnUuk8Nnis
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7bfc22e90d727d1743c2b6b7bc645033d5d38f1b
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 67%

---

# Cookie di CX Enterprise

Adobe CX Enterprise utilizza i cookie per memorizzare un ID visitatore utilizzato nelle applicazioni CX Enterprise. Questi cookie sono specifici per l&#39;accesso alle applicazioni Adobe CX Enterprise in [experience.adobe.com](https://experience.adobe.com).

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
   <td colname="col2"> <p> Contiene una copia di CX Enterprise ID (ECID) o MID. Il MID viene memorizzato in una coppia chiave/valore con sintassi s_ecid=MCMID|&lt;ECID&gt; </p> </td> 
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

Il servizio ID [visitatore](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) utilizza JavaScript per memorizzare un ID visitatore univoco in un cookie `AMCV_###@AdobeOrg` sul dominio del sito Web corrente, dove `###` rappresenta una stringa casuale di caratteri, ad esempio `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

Consulta anche [Cookie e il servizio ID visitatori](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html).

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
   <td colname="col2"> <p> ID visitatore univoci utilizzati dalle soluzioni aziendali CX. </p> </td> 
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

