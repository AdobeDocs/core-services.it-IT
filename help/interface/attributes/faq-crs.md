---
description: Domande frequenti e best practice per attributi cliente in Analytics e Target.
keywords: customer attributes
seo-description: Domande frequenti e best practice per attributi cliente in Analytics e Target.
seo-title: Domande frequenti, limitazioni e best practice
solution: Experience Cloud
title: Domande frequenti, limitazioni e best practice
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: f89a6c6704c9f499e6aa2ab38b2f5f9496ccdda5

---


# Domande frequenti, limitazioni e best practice

Domande frequenti e best practice per attributi cliente in Analytics e Target.

## Best practice e limitazioni {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Guida e limitazioni per l&#39;uso degli attributi cliente

| Problema | Descrizione |
|--- |--- |
| Limitazioni della sottoscrizione attributi cliente | Quando si esegue l&#39;aggiornamento ad Analytics Premium, si verifica un ritardo di 24 ore prima che gli attributi aggiuntivi siano disponibili. Potresti visualizzare un errore Sottoscrizione attributi max durante questo ritardo. |
| Più accessi sullo stesso dispositivo | Quando si utilizzano gli attributi del cliente per caricare i profili del cliente in un&#39;origine dati, Adobe consiglia agli utenti che condividono lo stesso dispositivo (ossia lo stesso Experience Cloud ID). In questo modo il servizio ECID, che persiste sul dispositivo, potrebbe collegare più utenti con lo stesso Experience Cloud ID, dando origine a risultati imprevisti [!DNL Target]. **** Nota: Per Mobile, l&#39;ECID è permanente dopo l&#39;installazione dell&#39;app Mobile e devi reinstallare l&#39;app per generare un nuovo ECID. Per Web, viene generato un nuovo ECID dopo che il cookie del browser viene cancellato. |
| Limitazione del caricamento giornaliero delle frequenze | Adobe consiglia di aggiornare gli attributi del cliente una sola volta al giorno. Devi aspettare almeno 24 ore per caricare un altro file di dati del profilo cliente per lo stesso set di profili. |
| Custom Analytics ID (`s.visitorID`) | L&#39;impostazione di un ID cliente usando `s.visitorID` è un metodo di identificazione degli utenti in Analytics. Tuttavia, le integrazioni in cui i dati di Analytics vengono esportati o importati tramite il servizio ID non funzioneranno quando un visitatore viene identificato utilizzando `s.visitorID.`<br>Questo include, ma non è limitato, audience condivise, Analytics for Target (A4T) e Attributi del cliente.<br>Per queste integrazioni, l&#39;impostazione di un ID Analytics personalizzato non è supportata. |
| Limitazioni della lunghezza di caratteri in Analytics | Quando si crea una sottoscrizione Analytics, le lunghezze dei campi per i file caricati vengono troncate a 255. |

## Domande frequenti sugli attributi cliente {#section_E47866EEA83348E09FE43CEC5E44C461}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Domanda </th> 
   <th colname="col2" class="entry"> Risposta </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Posso ricevere notifiche sullo stato di caricamento per gli attributi cliente? </p> </td> 
   <td colname="col2"> <p>Sì. Vedi <a href="../admin-getting-started/organizations.md#concept_0105453AD71847B8BFCAF4A40915F157" format="dita" scope="local">Gestione delle notifiche</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Cosa devo fare per iniziare a usare gli attributi del cliente? </p> </td> 
   <td colname="col2"> 
    <ol id="ol_1FACEF0990B6486B8DE86245D17695A8"> 
     <li id="li_F0C1542853684F8591FDC1B441D31A56"> <p>Effettua il provisioning. </p> <p>Se sei cliente di <b>Analytics</b>, il provisioning degli attributi dei clienti è effettuato da Adobe. Se usi solo <b>Target</b> e non hai Analytics, devi contattare l'Assistenza clienti per richiedere il provisioning per i servizi di base. </p> </li> 
     <li id="li_444FEDEE4B7244F79BA847662F5B17CB"> <p>Parla con il nostro team CRM. Scopri i tipi di dati cliente disponibili e quali potrebbero essere interessanti per l'utilizzo in Analytics e in Experience Cloud. </p> </li> 
     <li id="li_32D4AAF8C29748A78801A0E1BFB37AF5"> <p>Implementa i servizi di base. </p> <p>Consulta <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">Guida introduttiva: Abilitare le soluzioni per i servizi principali</a> per i passaggi su come modernizzare la tua implementazione per i servizi principali. (Consulta la sezione sulla sincronizzazione di ID cliente per informazioni importanti.) </p> </li> 
    </ol> <p> <b>Nota:</b> sono disponibili le domande frequenti di amministratori sull'implementazione dei servizi di base di <a href="../admin-getting-started/faq.md#concept_13219B4E51784577B6FF78AAA203DE91" format="dita" scope="local">qui</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Quanti attributi del cliente posso usare? </p> </td> 
   <td colname="col2"> <p>Nel servizio attributo cliente puoi caricare centinaia di colonne <span class="filepath">.csv</span>. Tuttavia, durante la configurazione delle sottoscrizioni e la selezione degli attributi, si applicano i seguenti limiti (per suite di rapporti), a seconda delle soluzioni che possedete:</p> <p> 
     <ul>
     <li>Foundation: 0</li>
     <li>Select: 3</li>
     <li>Prime: 15</li>
     <li>Ultimate: 200</li>
     <li>Standard: 3 totali</li>
     <li>Premium: 200</li>
     <li>Target Standard: 5</li>
     <li>Target Premium: 200</li></ul>
     </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>È necessario effettuare la migrazioni al servizio Experience Cloud ID? </p> </td> 
   <td colname="col2"> <p>Dipende dalla soluzione in uso. </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics</b>: fortemente consigliato </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target:</b> Richiesto. </li> 
     </ul> </p> <p>Il servizio ID ottimizza le funzionalità e permette di utilizzare le funzionalità Experience Cloud più recenti, tra cui dati sui tipi di pubblico in tempo reale, modernizzazione di Target, integrazione di Analytics e un nuovo modello di misurazioni per i video. </p> <p>Per ulteriori dettagli vedi <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">Servizi di base - Come abilitare le soluzioni</a> </p> <p> <b>Nota</b>: il servizio <span class="term">Experience Cloud ID</span> è l’implementazione moderna del servizio precedentemente noto come <span class="term">ID visitatore di Analytics</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Che rapporto c'è tra la funzionalità degli attributi del cliente e Adobe Audience Manager? </p> </td> 
   <td colname="col2"> <p>Audience Manager può ricevere dati per effettuare un'identificazione degli utenti, ma non può effettuare funzionalità di analisi che lega attributi a dati comportamentali storici o fornire report, analisi e funzionalità di segmentazione che sono invece disponibili in Adobe Analytics. Il servizio core persone consente di collegare e associare i dati avanzati delle soluzioni con un unico ID da usare in Experience Cloud. </p> <p> In Adobe Target, gli attributi del cliente compaiono come attributi individuali che possono essere combinati con altre regole per creare un pubblico. Il pubblico condiviso nel servizio core persone è un pubblico completo che non può essere modificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Analytics) </b>Cosa cambia in questa funzionalità rispetto a quella fornita in Analytics Premium? </p> </td> 
   <td colname="col2"> <p>Nel passato, i clienti interessati a combinare i dati degli attributi del cliente con i dati di Analytics avevano trovato molto utile lo strumento Data Workbench. La funzione Attributi del cliente rende questa funzionalità disponibile a un pubblico più vasto fornendo gli attributi del cliente come dimensioni e metriche in Reports &amp; Analytics, Ad Hoc Analysis e Report Builder. I clienti di Analytics Standard potranno accedere agli attributi del cliente, ma con funzionalità limitate. La funzionalità completa sarà disponibile per i clienti Analytics Premium. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> posso precaricare o caricare dati per clienti che Target non ha mai visto? </p> </td> 
   <td colname="col2"> <p> Sì. Quando i visitatori effettuano la loro prima richiesta a Target, il sistema raccoglierà le informazioni di cui disponiamo su di loro grazie agli Attributi del cliente, e le utilizzerà per effettuare il targeting. </p> <p> <p>Nota: il recupero di questi dati può richiedere fino a 20 minuti dalla prima interazione del visitatore con Target. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> Posso creare un super pubblico combinando i dati attributi del cliente con i dati di tipi di pubblico condivisi? </p> </td> 
   <td colname="col2"> <p>No. I dati di tipi di pubblico condivisi rappresentano un pubblico completato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target) </b>In che modo la funzionalità degli attributi del cliente può essere confrontata all'API per profilo in massa di Target? </p> </td> 
   <td colname="col2"> <p> L'<a href="https://www.adobe.io/apis/experiencecloud/target.html" format="https" scope="external">API per profilo in massa</a> consente ai profili Target di essere aggiornati direttamente tramite l'API, sia singolarmente che in modalità collettiva. La funzionalità è simile agli attributi del cliente, con le seguenti differenze chiave: </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">L'API di profilo è una chiamata REST API e gli attributi del cliente usano l'FTP. </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">L'API del profilo di Target invia solamente dati a Target e non all'intero Experience Cloud. </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">Gli attributi del cliente forniscono una semplice interfaccia per creare e gestire questi dati esterni. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> Il caricamento di dati dagli attributi del cliente su Adobe Target, estende la durata del profilo del visitatore di Target? </p> </td> 
   <td colname="col2"> <p>Sì. Consulta <a href="https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html" format="https" scope="external">Durata del profilo del visitatore</a> nell'Aiuto di Adobe Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> (Solo Target)</b> Posso utilizzare i dati caricati negli attributi del cliente, subito dopo l'identificazione del visitatore da parte dell'ID cliente? </p> </td> 
   <td colname="col2"> <p>Sì. </p> <p>Nella chiamata del server a Target, che include l'ID terza parte mbox, tutti i dati dell'attributo del cliente saranno disponibili. </p> </td> 
  </tr> 
    <tr> 
   <td colname="col1"> <p> <b> (Solo Target)</b> Cosa rappresenta la colonna "Stato sincronizzazione" per i file caricati in Origine attributo del cliente? </p> </td> 
   <td colname="col2"> <p> Il numero di record pubblicati e sincronizzati da Target può essere visualizzato facendo clic sull'icona Stato sincronizzazione rispetto a un file attributo specifico. "Sync %" è una metrica in tempo reale che specifica la percentuale di profili sincronizzati in Target. </p> <p> <b></b> Nota: La sincronizzazione degli attributi con Target potrebbe richiedere fino a 24 ore. </p>
 </td> 
  </tr> 
 </tbody> 
</table>
