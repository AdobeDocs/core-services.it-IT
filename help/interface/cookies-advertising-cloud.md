---
description: Scopri alcuni cookie di Adobe Advertising per la mappatura degli eventi di coinvolgimento e di conversione e, potenzialmente, come utilizzare tali informazioni per ottimizzare le offerte di annunci.
title: Cookie Adobi Advertising
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 5d0e02713ec4b233e06ecd3ac0234d1526b947f1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 75%

---

# Cookie Adobi Advertising{#advertising-cloud-cookies}

Adobi Advertising (precedentemente Adobe Advertising Cloud) utilizza i cookie per mappare gli eventi di coinvolgimento pubblicitario su eventi di conversione e, potenzialmente, per ottimizzare le offerte pubblicitarie.

>[!NOTE]
>
>Il tag JavaScript di Adobe Advertising beta che utilizza [Servizio Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) crea [cookie s_ecid di Experience Cloud di prime parti](cookies-first-party.md), non cookie di Adobe Advertising.

## Nome cookie: _lcc

<table id="table_821F8EBE91F244CBA72B0975B961B908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID e timestamp (nel formato aaaammgg) dei clic di visualizzazione</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>15 minuti</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Un cookie di terze parti utilizzato per determinare se un evento di clic su un annuncio visualizzato si applica a un hit di Adobe Analytics </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>52 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: _tmae

<table id="table_28C2B62595E240D5A3C3E0BE147748C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID codificati e timestamp del coinvolgimento degli annunci tramite il tracciamento degli Adobi Advertising DSP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>1 anno </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Un cookie di terze parti che memorizza il livello di coinvolgimento degli annunci da parte degli utenti, ad esempio “ultima visualizzazione annuncio xyz123 il 30 giugno 2016” </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>Variabile; i dati vengono codificati e generalmente le dimensioni sono inferiori a 1 KB </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: adcloud

<table id="table_D7CD238736BC4571883F92F47673F57C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>Le marche temporali dell’ultima visita del surfista al sito web dell’inserzionista, l’ultimo clic di ricerca del surfista e l’ef_id creato quando il surfista ha fatto clic su un annuncio</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>1 anno</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Un cookie di prime parti che associa l’ID surfista a segmenti e conversioni rilevanti </p> <p> Le informazioni sull’ultima visita vengono utilizzate per ottimizzare i tempi di caricamento delle pagine evitando inutili richieste a [!DNL Adobe] server. </p> <p>Le informazioni sull’ultimo clic di ricerca consentono di determinare se un evento di conversione è il risultato di un clic o di una visualizzazione view-through (conversione derivante da impressioni, ma nessun clic). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>Dominio di livello principale dell’inserzionista (come esempio.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>Variabile, ma in genere 50-150 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: ev_sync_&#42;

(ev_sync_ax, ev_sync_bk, ev_sync_dd, ev_sync_fs, ev_sync_ix, ev_sync_nx, ev_sync_ox, ev_sync_pm, ev_sync_rc, ev_sync_tm, ev_sync_yh)

<table id="table_A05C02AB261946E0AABAD78259392D81"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>Data di esecuzione della sincronizzazione nel formato aaaammgg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>Data di esecuzione della sincronizzazione nel formato aaaammgg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Cookie di terze parti specifico per uno scambio di annunci che sincronizza l’ID surfista Adobe Advertising con lo scambio di annunci partner. Viene creato per i nuovi surfisti e invia una richiesta di sincronizzazione quando è scaduto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>8 caratteri </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: everest_g_v2

<table id="table_04043292A43B41B69EAF17AF4E217C69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID browser e surfista </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>1 anno </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Creato quando un utente ha fatto clic inizialmente su un annuncio del client e utilizzato per mappare il clic corrente e quelli successivi con altri eventi sul sito Web del client </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>~27 caratteri </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: everest_session_v2

<table id="table_1A3AE4CA71304ADB943CB1F64BE695F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID sessione </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>Quando il browser viene chiuso </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Cookie di sessione browser di terze parti; un cookie viene utilizzato per tutti gli account </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>~16 caratteri </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: ev_tm

<table id="table_6C4D9DCFA4BF4FB2BD445E027550955F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID Adobe Advertising DSP (Demand Side Platform) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>2 anni </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Cookie di terze parti che memorizza l’ID DSP corrispondente all’ID surfista nel cookie everest_g_v2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>~ 20 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: id_adcloud

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Informazioni memorizzate </p> </td> 
   <td colname="col2"> <p>ID surfista </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scadenza </p> </td> 
   <td colname="col2"> <p>91 giorni </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizzo </p> </td> 
   <td colname="col2"> <p>Il cookie è impostato nel dominio di prime parti ma non è ancora utilizzato </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Posizione </p> </td> 
   <td colname="col2"> <p>Dominio di livello principale dell’inserzionista (come esempio.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensione </p> </td> 
   <td colname="col2"> <p>16 byte </p> </td> 
  </tr> 
 </tbody> 
</table>
