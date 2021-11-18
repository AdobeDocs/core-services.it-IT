---
description: Scopri i requisiti dei file di dati e le diverse origini dei dati per caricare Attributi del cliente in Experience Cloud.
keywords: Attributi del cliente;servizi core
solution: Experience Cloud
title: 'Scopri come usare file e sorgenti dati per Attributi del cliente '
uuid: 9dd0e364-889b-45db-b190-85c0930a101e
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: e2dfe10d-7003-4afa-a5e6-57703d74efd4
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 98%

---

# Informazioni su file di dati e origini dati per Attributi del cliente

Requisiti dei file di dati e diverse origini dati per caricare Attributi del cliente in Experience Cloud.

Devi poter accedere ai dati del sistema CRM, o simili, della tua azienda. I dati da caricare in Experience Cloud devono essere un file `.csv`. Se effettui il caricamento mediante FTP o sFTP, puoi caricare anche un file `.fin`.

La funzione Attributi del cliente è progettata per gestire alcuni file al giorno. Per evitare che numerosi file di piccole dimensioni possano ritardare l’elaborazione, i file inviati entro 30 minuti da un batch precedente della stessa organizzazione vengono indirizzati a una coda di priorità inferiore.

## Tipi di file consentiti e requisiti per la denominazione {#section_6F64FA02ACCC4215B0862CB6A1821FBF}

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tipo di file </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>Un file di valori separati da virgole (ad esempio un file creato in Excel). Questo file contiene i dati di attributi cliente. </p> <p> <b>Requisiti di denominazione:</b> verifica che le estensioni dei nomi dei file non contengano spazi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Necessario) Il file <span class="filepath">.fin</span> informa il sistema che il caricamento dei dati è terminato. Il nome del file <span class="filepath">.fin</span> deve corrispondere al nome del file <span class="filepath">.csv</span>. </p> <p>Adobe consiglia di creare un file di testo vuoto con estensione <span class="filepath">.fin</span>. Un file vuoto consente di risparmiare spazio e tempi per il caricamento. </p> <p> <p>Nota: non puoi rinominare un file <span class="filepath">.fin</span> dopo averlo caricato. Devi caricare il file <span class="filepath">.fin</span> separatamente e non può essere un file caricato precedentemente e rinominato. </p> </p> <p>Dopo aver caricato il file <span class="filepath">.fin</span> nell'FTP degli Attributi del cliente, il sistema restituisce velocemente i dati (entro un minuto). In questo si distingue da altri sistemi Adobe basati su FTP, che raccolgono i dati meno frequentemente (una volta all'ora circa). </p> <p>Il file <span class="filepath">.fin</span> non è necessario quando si utilizza il metodo di caricamento di trascinamento della selezione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz</span> o <span class="filepath">.zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz</span> (gzip) o <span class="filepath">.zip</span> - per file compressi. Un file <span class="filepath">.zip</span> non può contenere più di un file nell'archivio. </p> <p> <b>Requisiti per la denominazione:</b> il nome del file <span class="filepath">.zip</span> o <span class="filepath">.gz</span> deve corrispondere al nome del file <span class="filepath">.csv</span>. Ad esempio, se il nome del file <span class="filepath">.csv</span> è <span class="filepath">crm_small.csv</span>, il file <span class="filepath">.zip</span> deve essere denominato <span class="filepath">crm_small.csv.zip</span>. </p> <p>Il file .fin deve corrispondere al file .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti per i file di dati degli attributi {#section_169FBF5B7BBA47CE825B7A330CF3FE98}

**Esempio di CSV**

Il file CSV deve rispettare il seguente formato:

![Requisiti per i file di dati degli attributi](assets/cvs.png)

Lo stesso file visualizzato in un editor di testo:

![Requisiti per i file di dati degli attributi](assets/csv_txt.png)

**Linee guida**

<table id="table_A9849CC9AA784763921DE057F0F61515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Elemento </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Trascinamento della selezione </p> </td> 
   <td colname="col2"> <p>Il file da trascinare deve essere inferiore a 100 MB. </p> <p>Il file <span class="filepath">.fin</span> non è necessario quando si utilizza il metodo di caricamento di trascinamento della selezione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Colonna ID cliente </p> </td> 
   <td colname="col2"> <p> La prima colonna deve essere un ID cliente univoco. L'ID usato deve corrispondere all'ID che viene passato al servizio Experience Cloud ID. </p> <p>Per Analytics, l'ID archiviato in una prop o eVar. </p> <p>Per Target, il valore setCustomerID. (Consulta <a href="core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local"> Analytics e Adobe Target: sincronizzazione dell'ID cliente </a>) </p> <p> Questo ID cliente è l’identificatore univoco che il sistema CRM utilizza per ogni persona nel database. Le colonne rimanenti sono attributi provenienti dai dati del sistema CRM. Puoi scegliere quanti attributi caricare. </p> <p>Per le intestazioni delle colonne sono consigliati nomi descrittivi e leggibili, ma non sono obbligatori. Quando convalidi lo schema dopo il caricamento, puoi mappare i nomi descrittivi alle righe e alle colonne caricate. </p> <p> <b>Informazioni sugli ID cliente</b> </p> <p>In genere, un'azienda utilizza un ID cliente proveniente da un sistema di gestione delle relazioni con i clienti (CRM). Tale ID viene impostato usando la chiamata <span class="codeph">setCustomerIDs</span> quando una persona effettua l'accesso. Questo ID viene anche usato come chiave nel file CRM che viene caricato in Experience Cloud. Un <a href="t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local"> ID alias</a> è un nome semplificato per i dati archiviati in Audience Manager, dove vengono archiviati i dati alias. Il sistema invia alias a questo archivio di dati (tramite setCustomerIDs). Il file di gestione delle relazioni con i clienti viene applicato ai dati in tale archivio di dati. </p> <p>Per informazioni su <span class="codeph">setCustomerIDs</span> consulta <a href="https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en" format="https" scope="external">ID cliente e stati di autenticazione</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Intestazioni e colonne successive </p> </td> 
   <td colname="col2"> <p>Le intestazioni successive devono rappresentare il nome di ciascun attributo. </p> <p> Queste colonne devono contenere gli Attributi del cliente provenienti dal CRM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limiti degli attributi </p> </td> 
   <td colname="col2"> <p>In Experience Cloud, nel servizio attributo cliente puoi caricare centinaia di colonne <span class="filepath">.csv </span>. Tuttavia, durante la configurazione delle sottoscrizioni e la selezione degli attributi, si applicano i seguenti limiti a seconda delle applicazioni che possiedi: </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard</b>: 3 totali </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>: 200 per suite di rapporti </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Adobe Target Standard:</b> 5 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Adobe Target Premium:</b> 200 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limiti delle righe </p> </td> 
   <td colname="col2"> <p>Non esiste alcun limite noto al numero di righe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limiti delle colonne </p> </td> 
   <td colname="col2"> <p>Per praticità, limita il numero di colonne a circa 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limiti dei caratteri </p> </td> 
   <td colname="col2"> <p>Quando crei una sottoscrizione Analytics, le lunghezze dei campi per i file caricati vengono troncate a 255. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Linee guida FTP e limiti di dimensione </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E157EE6F98914EADA0C103D1D1E705D3"> 
      <li id="li_84FBD455DD164A28AC16F4A5AB19E4B3">La dimensione massima del file per l'FTP è 4 GB per ciascun caricamento. </li> 
      <li>La dimensione minima del file è di 10 MB per ogni caricamento. </li>
      <li>puoi caricare un file ogni mezz'ora. </li>
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> Devi rilasciare il file <span class="filepath">.csv</span> (e <span class="filepath">.fin</span>) nella cartella root del sito FTP. </li> 
     </ul> </p> <p> <p>Importante: lo spazio totale consentito per l'account FTP è 40 GB. È tua responsabilità eliminare i file elaborati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Requisiti dei file </p> </td> 
   <td colname="col2"> <p> Ciascuna sorgente attributo deve contenere lo stesso numero di campi separati da virgola. </p> <p> I campi contenenti un'interruzione di riga, virgolette o virgole devono essere tra virgolette. </p> <p> Le virgolette doppie in un campo devono essere precedute da una barra inversa (\). </p> <p> Le colonne vuote vengono archiviate come <span class="term">nulle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>File multipli </p> </td> 
   <td colname="col2"> <p>Durante il caricamento dei dati di attributi clienti, se devi caricare diversi file in rapida successione, in particolare se sono di grandi dimensioni, accertati che il file precedente sia stato elaborato prima di caricare quello successivo. Puoi monitorare questo passaggio controllando se il file precedente è stato spostato nella cartella dei file elaborati o non riusciti, nel tuo account FTP per [!UICONTROL Attributi del cliente]. </p> <p> Considera inoltre che la suddivisione di un file di grandi dimensioni in file più piccoli inviandoli in rapida successione potrebbe rallentare l’elaborazione, se non ti assicuri che ogni file sia stato elaborato prima di inviare quello successivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Codifica caratteri </p> </td> 
   <td colname="col2"> <p>Per il Giappone, è obbligatoria la codifica UTF-8. </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>Dati storici </p> </td> 
   <td colname="col2"> <p> Gli attributi del cliente sono associati al profilo del visitatore sottostante in [!DNL Analytics]. Pertanto, gli [!UICONTROL Attributi del cliente] sono associati al visitatore per l’intero ciclo di vita del suo profilo in [!DNL Analytics]. Questo profilo include il comportamento precedente al primo accesso del cliente. </p> <p> Se utilizzi il metodo di recupero dati Data Warehouse, i dati vengono associati a un valore post_visid_high/low basato sull’ID di Analytics (AID). Se utilizzi il servizio Experience Cloud ID, i dati sono legati a un post_visid_high/low basato sull'Experience Cloud ID (MID). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed di dati </p> </td> 
   <td colname="col2"> <p>Gli attributi del cliente non sono disponibili nei feed di dati. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Utilizzo di più origini dati {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

Quando crei, modifichi o elimini sorgenti di attributi del cliente, si verifica un ritardo di circa un’ora prima della effettiva sincronizzazione degli ID con la nuova origine dati.

L’ID alias per ogni origine di attributi del cliente deve essere univoco. Se hai più sorgenti di dati che utilizzano lo stesso ID, puoi impostarle come segue:

**In VisitorAPI.js o nello strumento Experience Cloud ID in Dynamic Tag Management:**

Imposta due ID cliente corrispondenti alle origini dati appropriate:

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

(Consulta [ID cliente e stati di autenticazione](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=it) per ulteriori informazioni.)

In **[!UICONTROL Experience Cloud]** > **[!UICONTROL Persone]** > **[!UICONTROL Attributi del cliente]**:

Crea due origini di attributi del cliente utilizzando ID alias univoci corrispondenti agli ID cliente qui sopra. Questo metodo consente di inviare lo stesso ID di riferimento a più origini di attributi del cliente.
