---
description: Scene7 utilizza i cookie per memorizzare informazioni utili che possono essere utilizzate per inviare contenuti multimediali dinamici al browser.
keywords: cookies;privacy
seo-description: Scene7 utilizza i cookie per memorizzare informazioni utili che possono essere utilizzate per inviare contenuti multimediali dinamici al browser.
seo-title: Cookie di Scene7
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Cookie di Scene7
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Cookie di Scene7{#scene-cookies}

Scene7 utilizza i cookie per memorizzare informazioni utili che possono essere utilizzate per inviare contenuti multimediali dinamici al browser.

Scene7 memorizza le informazioni in locale per alcuni visualizzatori AS2 basati su Flash precedenti.

Per i visualizzatori AS2, i cookie:

* Monitorano lo stato della sessione di un utente, ad esempio la pagina corrente e l’immagine visualizzata, il livello di zoom corrente ecc.
* Determinano quanto tempo è trascorso dalla sessione precedente dell’utente. Il visualizzatore utilizza queste informazioni per decidere se continuare una sessione precedente o avviarne una nuova. Queste informazioni vengono inviate anche ai server di Scene7, che tuttavia non vengono utilizzati.

Per i visualizzatori AS2 Flash eCatalog, i cookie:

* Archiviano il contenuto generato dall’utente (in particolare il contenuto immesso dall’utente nella funzione “note” del visualizzatore ecatalog). Questo contenuto viene ripristinato quando l’utente riprende una sessione.
* Quando l’utente avvia un messaggio e-mail per condividere l’ecatalog con un altro utente, il contenuto delle note del secondo elenco dei visualizzatori di AS2 viene copiato sui nostri server e fornito al destinatario. Quando il destinatario avvia la sessione come visualizzatore, il contenuto delle note viene recuperato dal server e copiato in un cookie. Questa funzione è poco usata, pertanto non scade e il contenuto non aggiornato non viene rimosso. Al momento, persiste sui server a tempo indeterminato.

I visualizzatori AS3 successivi non implementano la persistenza della sessione.

**Nome cookie: VatLogin.jsp**

| Attributo | Descrizione |
|---|---|
| Informazioni memorizzate | Imposta il cookie della sessione. AuthFilter, incorporato in IPS ImageServer (IS, IR, e anche i contesti SWF/interfacce e video) utilizza il cookie per l’autorizzazione degli accessi. Se presente, consente la trasmissione delle richieste HTTP. Altrimenti restituisce non autorizzato. |
| Scadenza | Questo cookie è un cookie di sessione. La scadenza della sessione corrente è impostata su 45 minuti nell’IPS di Scene7 [!DNL web.xml]. |

**Nome cookie: s7js.flyout.InfoMessage.displayed`assetId`.state**

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

