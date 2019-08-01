---
description: Scene 7 utilizza i cookie per memorizzare le informazioni utili che possono essere utilizzate per consegnare gli elementi multimediali dinamici al browser.
keywords: cookie; privacy
seo-description: Scene 7 utilizza i cookie per memorizzare le informazioni utili che possono essere utilizzate per consegnare gli elementi multimediali dinamici al browser.
seo-title: Cookie Scene 7
solution: Marketing Cloud, Analytics, Target, Social
title: Cookie Scene 7
uuid: f 9 b 9 d 13 a -17 e 5-4139-8 c 84-6 fe 5 d 22 c 4196
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Scene7 Cookies{#scene-cookies}

Scene 7 utilizza i cookie per memorizzare le informazioni utili che possono essere utilizzate per consegnare gli elementi multimediali dinamici al browser.

Scene 7 memorizza localmente le informazioni per alcuni visualizzatori basati su Flash precedenti a 2.

Per visualizzatori AS 2, cookie:

* Monitora lo stato della sessione di un utente, ad esempio pagina corrente e immagine visualizzata, livello di zoom corrente ecc.
* Determina quanto tempo è trascorso dalla sessione precedente dell'utente. Il visualizzatore utilizza queste informazioni per decidere se continuare una sessione precedente o avviarne una nuova. Queste informazioni vengono inviate anche ai server Scene 7, che tuttavia non vengono utilizzati.

Per visualizzatore di ecatalog AS 2, cookie:

* Archiviate il contenuto generato dall'utente (in particolare il contenuto immesso dall'utente nella funzione "note" del visualizzatore ecatalog). Questo contenuto viene ripristinato quando l'utente riprende una sessione.
* Quando l'utente avvia un messaggio e-mail per condividere l'ecatalog con un altro utente, il contenuto delle note del secondo elenco visualizzatori AS 2 viene copiato sui nostri server per fornire al destinatario. Quando il destinatario avvia la sessione del visualizzatore, viene recuperato dal server il contenuto delle note fisso e copiato in un cookie. Questa funzione è ridotta e non scade e il contenuto non viene rimosso. Al momento, persiste sui server a tempo indeterminato.

I successivi visualizzatori AS 3 non implementano la persistenza della sessione.

* [Nome cookie: Vatlogin. jsp](../cookies-overview/cookies-s7.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nome cookie: s 7 js. flyout. infomessage. displayed. state](../cookies-overview/cookies-s7.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Nome cookie: s 7 js. flyout. infomessage. displayed_ idx. ant](../cookies-overview/cookies-s7.md#section-05d1c52c478541609f4a18a9c1eb032f)

## Cookie Name: VatLogin.jsp {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Attributo | Descrizione |
|---|---|
| Informazioni memorizzate | Imposta il cookie della sessione. Il cookie authfilter incorporato in IPS imageserver (IS, IR, e anche i file SWF/skins e video) utilizza il cookie per l'autorizzazione di accesso. Se presente, consente la trasmissione delle richieste HTTP. Altrimenti restituisce non autorizzato. |
| Scadenza | Questo cookie è un cookie di sessione. Current session expiration is set to 45 minutes in the Scene7 IPS [!DNL web.xml]. |

## Nome cookie: s 7 js. flyout. infomessage. display<assetId>.state {#section-14ad50dfcd7342f9ac80283b1f0d3400}

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
   <td colname="col2"> <p>&lt; ID risorsa &gt; è il nome della risorsa con cui il visualizzatore sta lavorando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Scadenza </td> 
   <td colname="col2"> Questo cookie è un cookie di sessione e scade quando il browser viene chiuso. </td> 
  </tr> 
 </tbody> 
</table>

## Nome cookie: s 7 js. flyout. infomessage. display<assetId>_ idx<id>.ant {#section-05d1c52c478541609f4a18a9c1eb032f}

I cookie del browser vengono utilizzati dai visualizzatori DHTML precedenti per memorizzare informazioni sullo stato e dati fissi. Vengono anche utilizzate dal menu a comparsa DHTML multischermo per rendere l'indicatore dei messaggi specifico della sessione.

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
   <td colname="col2"> <p> </p> <p> &lt; ID risorsa &gt; è il nome della risorsa con cui il visualizzatore sta lavorando e &lt; id &gt; è l'indice della nota basato su 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Scadenza </td> 
   <td colname="col2"> Questo cookie è un cookie di sessione e scade quando il browser viene chiuso. </td> 
  </tr> 
 </tbody> 
</table>

