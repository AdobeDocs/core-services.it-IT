---
description: Se non effettui il caricamento trascinando la selezione, puoi caricare l'attributo del cliente in Experience Cloud tramite FTP.
keywords: attributi del cliente; servizi di base
seo-description: Se non effettui il caricamento trascinando la selezione, puoi caricare l'attributo del cliente in Experience Cloud tramite FTP.
seo-title: Facoltativo - Caricamento del file di dati tramite FTP
solution: Experience Cloud
title: Facoltativo - Caricamento del file di dati tramite FTP
uuid: 5 df 565 dd-b 6 f 8-420 e -981 f -4 b 6 fc 6 f 7 d 0 e 4
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Facoltativo - Caricamento del file di dati tramite FTP

Se non effettui il caricamento trascinando la selezione, puoi caricare l&#39;attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo la creazione di un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per origine attributo. I file caricati vengono archiviati nella cartella principale di quell&#39;account. I dati devono essere in [!DNL .csv] formato, con un secondo [!DNL .fin] file che indica che il caricamento è completo.

>[!IMPORTANT]
>
>Requisiti [del file di dati Rivedi i requisiti del cliente per caricare gli attributi](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) del cliente prima di caricare il file.


Puoi effettuare i caricamenti di file al sito FTP degli attributi del cliente tramite FTP o SFTP.

* Dovere disporre di un client che supporta le connessioni SFTP.
* Puoi effettuare la connessione con SFTP utilizzando nome utente/password oppure senza utilizzare la password, come spiegato [qui](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/?f=ftp_sftp_cert_auth).



<!-- <p>Error states - get with Matt and Dave </p> 
<p>What are the most common reasons for doing this? Retail? Do a use case example, then show an AN example. </p> 
<p>You create one FTP per attribute source. Files go to the root folder in that account. The file type .fin is user-created. (For example, upload a .csv then a .fin of the same name, which signals you have completed the upload. https://wiki.corp.adobe.com/display/marketingcloud/Customer+Record+Services#CustomerRecordServices-FileFormats (leverage for doc). Possibly link from FTP File Reqs page to a help file about naming conventions. Need a new file type page for this. Similar content here: https://marketing.adobe.com/resources/help/en_US/reference/c_general_file_structure.html and here: https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_datasources.html </p> 
<p>Drag-n-drop and zip functionality for uploads - 1/21/2015. S/b less than 100 megs for drag and drop zip file. Fin file not required for drag/drop. </p> 
<p>Preview Data - shows the last upload (?) </p> 
<p>Need a link to the "instructions" on that information icon with the image. </p> 
<p>Workflow: Drag and drop, validate schema, configure subscription, save/activate. </p> -->
**Per caricare il file di dati tramite FTP**

1. [Crea un&#39;origine attributo del cliente e carica il file di dati...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Verifica di aver effettuato l&#39;accesso al tuo sito FTP in [!DNL ftp. adobe. com/<sftpname>].

1. Fate clic su **[!UICONTROL Azioni]** &gt; **[!UICONTROL Caricamento file]**.

1. Caricate un [!DNL .fin] file per recuperare il file.

   Il tipo [!DNL .fin] di file viene creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se caricate [!DNL crs123.csv], [!DNL crs123.fin]caricate anche.

   Se il caricamento viene eseguito correttamente, entrambi i file vengono spostati in una cartella denominata **processed (elaborati)**.


   Consulta [Requisiti del file dati per il caricamento degli attributi cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) per informazioni importanti sulla denominazione e sulla struttura del file.
