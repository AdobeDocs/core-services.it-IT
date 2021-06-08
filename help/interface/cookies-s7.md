---
description: Come Adobe Scene7 utilizza i cookie per memorizzare informazioni utili per inviare contenuti Dynamic Media al browser.
keywords: cookie;privacy
solution: Experience Cloud,Analytics,Target
title: 'Cookie di Scene7 '
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
feature: Cookie
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: ecb8d17f-f752-44ca-8877-44752c28dc70
source-git-commit: c7ed1324015beb7ebcf7a4ee21b05601e36e608f
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 85%

---

# Cookie di Scene7{#scene-cookies}

Scene7 utilizza i cookie per memorizzare informazioni utili che possono essere utilizzate per inviare contenuti multimediali dinamici al browser.

Scene7 memorizza le informazioni in locale per alcuni visualizzatori AS2 basati su Flash precedenti.

Per i visualizzatori AS2, i cookie:

* Monitora lo stato della sessione di un utente, ad esempio la pagina corrente e l&#39;immagine visualizzata, il livello di zoom corrente e così via.
* Determinano quanto tempo è trascorso dalla sessione precedente dell’utente. Il visualizzatore utilizza queste informazioni per decidere se continuare una sessione precedente o avviarne una nuova. Queste informazioni vengono inviate anche ai server di Scene7, che tuttavia non vengono utilizzati.

Per i visualizzatori AS2 Flash eCatalog, i cookie:

* Archiviano il contenuto generato dall’utente (in particolare il contenuto immesso dall’utente nella funzione “note” del visualizzatore ecatalog). Questo contenuto viene ripristinato quando l’utente riprende una sessione.
* Quando l&#39;utente avvia un&#39;e-mail per condividere l&#39;ecatalog con un altro utente, il contenuto delle note del secondo elenco dei visualizzatori AS2 viene copiato nei server di Adobe per fornirlo al destinatario. Quando il destinatario avvia la sessione come visualizzatore, il contenuto delle note viene recuperato dal server e copiato in un cookie. Questa funzione è poco usata, pertanto non scade e il contenuto non aggiornato non viene rimosso. Al momento, persiste sui server a tempo indefinito.

I visualizzatori AS3 successivi non implementano la persistenza della sessione.

**Nome cookie: VatLogin.jsp**

| Attributo | Descrizione |
|---|---|
| Informazioni memorizzate | Imposta il cookie della sessione. AuthFilter, incorporato in IPS ImageServer (IS, IR, e anche i contesti SWF/interfacce e video) utilizza il cookie per l’autorizzazione degli accessi. Se presente, consente la trasmissione delle richieste HTTP. Altrimenti restituisce non autorizzato. |
| Scadenza | Questo cookie è un cookie di sessione. La scadenza della sessione corrente è impostata su 45 minuti nell’IPS di Scene7 [!DNL web.xml]. |

**Nome cookie: s7js.flyout.InfoMessage.displayed `assetId`.state**

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Informazioni memorizzate </td> 
   <td colname="col2"> <p>&lt;assetId&gt; è il nome della risorsa che il visualizzatore sta utilizzando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Scadenza </td> 
   <td colname="col2"> Questo cookie è un cookie di sessione e scade quando il browser viene chiuso. </td> 
  </tr> 
 </tbody> 
</table>

**Nome cookie: s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

I cookie del browser vengono utilizzati dai visualizzatori DHTML precedenti per memorizzare informazioni sullo stato e dati sulle note. Vengono anche utilizzati dal riquadro a comparsa DHTML multischermo per rendere l’indicatore dei messaggi specifico per la sessione.

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attributo </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Informazioni memorizzate </td> 
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; è il nome della risorsa che il visualizzatore sta utilizzando &lt;id&gt; è l’indice della nota basato su 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Scadenza </td> 
   <td colname="col2"> Questo cookie è un cookie di sessione e scade quando il browser viene chiuso. </td> 
  </tr> 
 </tbody> 
</table>
