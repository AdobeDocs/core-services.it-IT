---
description: Scopri come caricare i dati degli attributi del cliente tramite FTP in Experience Cloud.
solution: Experience Cloud
title: Caricare il file di dati di attributi cliente tramite FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 163dc8ef83fb83a0e51879520bcb3ae697c95144
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 76%

---

# Facoltativo - Caricamento del file di dati tramite FTP

Se non effettui il caricamento trascinando la selezione, puoi caricare i dati di Attributi del cliente ad Experience Cloud tramite FTP.

Puoi caricare i dati dopo aver creato un’origine di attributi cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per ogni sorgente attributo. I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv`, con un secondo file `.fin` che indica il completamento del caricamento.

>[!IMPORTANT]
>
>Controlla i [requisiti del file di dati per caricare Attributi del cliente](crs-data-file.md) prima di caricare il file.

È possibile caricare i file sul sito FTP degli Attributi del cliente tramite FTP o SFTP:

* È necessario un client che supporti le connessioni SFTP.
* Puoi connetterti con SFTP utilizzando nome utente/password o senza utilizzare alcuna password, come descritto [qui](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=it).

**Per caricare il file di dati tramite FTP**

1. [Creazione di una sorgente attributo cliente e caricamento del file di dati...](t-crs-usecase.md).

   Verifica di aver effettuato l’accesso al tuo sito FTP su `ftp.adobe.com/<sftpname>`.

1. Fai clic su **[!UICONTROL Azioni]** > **[!UICONTROL Caricamento file]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi `crs123.csv`, carica anche `crs123.fin`.

   Se il caricamento ha esito positivo, entrambi i file vengono spostati in una cartella denominata **elaborati**.

   Consulta i [requisiti del file di dati per caricare Attributi del cliente](crs-data-file.md) per informazioni importanti sui nomi e sulla struttura dei file.
