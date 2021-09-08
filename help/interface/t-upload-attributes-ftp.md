---
description: Scopri come caricare i dati degli attributi del cliente tramite FTP in Experience Cloud.
keywords: Attributi del cliente;servizi core
solution: Experience Cloud
title: 'Caricare il file di dati di attributi cliente tramite FTP '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
feature: Attributi del cliente
topic: Amministrazione
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '271'
ht-degree: 100%

---

# Facoltativo - Caricamento del file di dati tramite FTP

Se non effettui il caricamento trascinando la selezione, puoi caricare i dati di attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo aver creato un’origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per ogni sorgente attributo. I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv`, con un secondo file `.fin` che indica il completamento del caricamento.

>[!IMPORTANT]
>
>Controlla i [requisiti del file di dati per caricare Attributi del cliente](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) prima di caricare il file.

È possibile caricare i file sul sito FTP degli Attributi del cliente tramite FTP o SFTP:

* È necessario un client che supporti le connessioni SFTP.
* Puoi connetterti con SFTP utilizzando nome utente/password o senza utilizzare alcuna password, come descritto [qui](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=it).

**Per caricare il file di dati tramite FTP**

1. [Creazione di una sorgente attributo cliente e caricamento del file di dati...](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Verifica di aver effettuato l’accesso al tuo sito FTP su `ftp.adobe.com/<sftpname>`.

1. Seleziona **[!UICONTROL Azioni]** > **[!UICONTROL Caricamento file]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi [!DNL crs123.csv], carica anche [!DNL crs123.fin].

   Se il caricamento ha esito positivo, entrambi i file vengono spostati in una cartella denominata **elaborati**.

   Consulta i [requisiti del file di dati per caricare Attributi del cliente](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) per informazioni importanti sui nomi e sulla struttura dei file.
