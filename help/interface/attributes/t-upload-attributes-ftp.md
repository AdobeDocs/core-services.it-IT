---
description: Scopri come caricare i dati degli attributi del cliente tramite FTP in Experience Cloud.
keywords: Attributi del cliente;servizi core
solution: Experience Cloud
title: 'Caricare il file di dati di attributi cliente tramite FTP '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
feature: Attributi del cliente
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
translation-type: ht
source-git-commit: f4add6d5e64678c6b578237c18ceda9ee2245033
workflow-type: ht
source-wordcount: '269'
ht-degree: 100%

---

# Facoltativo - Caricamento del file di dati tramite FTP

Se non effettui il caricamento trascinando la selezione, puoi caricare l&#39;attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo la creazione di un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per ogni sorgente attributo. I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

>[!IMPORTANT]
>
>Controlla i [requisiti del file di dati per caricare Attributi del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) prima di caricare il file.

È possibile caricare i file sul sito FTP degli Attributi del cliente tramite FTP o SFTP:

* È necessario un client che supporti le connessioni SFTP.
* Puoi connetterti con SFTP utilizzando nome utente/password o senza utilizzare alcuna password, come descritto [qui](https://docs.adobe.com/help/it-IT/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html).

**Per caricare il file di dati tramite FTP**

1. [Crea un&#39;origine attributo del cliente e carica il file di dati...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Verifica di aver effettuato l’accesso al tuo sito FTP su `ftp.adobe.com/<sftpname>`.

1. Fai clic su **[!UICONTROL Azioni]** > **[!UICONTROL Caricamento file]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi [!DNL crs123.csv], carica anche [!DNL crs123.fin].

   Se il caricamento ha esito positivo, entrambi i file vengono spostati in una cartella denominata **elaborati**.

   Consulta i [requisiti del file di dati per caricare Attributi del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) per informazioni importanti sui nomi e sulla struttura dei file.
