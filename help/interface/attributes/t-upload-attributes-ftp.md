---
description: Se non effettui il caricamento trascinando la selezione, puoi caricare l’attributo del cliente in Experience Cloud tramite FTP.
keywords: attributi del cliente;servizi principali
seo-description: Se non effettui il caricamento trascinando la selezione, puoi caricare l’attributo del cliente in Experience Cloud tramite FTP.
seo-title: Facoltativo - Caricamento del file di dati tramite FTP
solution: Experience Cloud
title: Facoltativo - Caricamento del file di dati tramite FTP
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# Facoltativo - Caricamento del file di dati tramite FTP

Se non effettui il caricamento trascinando la selezione, puoi caricare l’attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo la creazione di un'origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per origine attributo. I file caricati vengono archiviati nella cartella principale di quell'account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

>[!IMPORTANT]
>
>Rivedi [Requisiti del file di dati per il caricamento degli attributi del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) prima di caricare il file.

Puoi effettuare i caricamenti di file al sito FTP degli attributi del cliente tramite FTP o SFTP.

* Dovere disporre di un client che supporta le connessioni SFTP.
* Puoi effettuare la connessione con SFTP utilizzando nome utente/password oppure senza utilizzare la password, come spiegato [qui](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html).

**Per caricare il file di dati tramite FTP**

1. [Crea un'origine attributo del cliente e carica il file di dati...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Verifica di aver effettuato l’accesso al tuo sito FTP all’indirizzo [!DNL ftp.adobe.com/<sftpname>].

1. Fai clic su **[!UICONTROL Azioni]** &gt; **[!UICONTROL Caricamento file]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall’utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi [!DNL crs123.csv], carica anche [!DNL crs123.fin].

   Se il caricamento viene eseguito correttamente, entrambi i file vengono spostati in una cartella denominata **processed (elaborati)**.

   Consulta [Requisiti del file dati per il caricamento degli attributi cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) per informazioni importanti sulla denominazione e sulla struttura del file.
