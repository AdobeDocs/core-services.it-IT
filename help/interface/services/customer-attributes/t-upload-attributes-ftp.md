---
description: Scopri come caricare i dati degli attributi del cliente tramite FTP in Experience Cloud.
solution: Experience Cloud
title: Caricare file di dati di attributi cliente tramite FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 67%

---

# Caricare il file di dati tramite FTP (opzionale)

Se non effettui il caricamento trascinando la selezione, puoi caricare l’attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo aver creato un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per ogni sorgente attributo. I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

>[!IMPORTANT]
>
>Rivedi [Requisiti del file di dati per il caricamento degli attributi del cliente](crs-data-file.md) prima di caricare il file.

È possibile caricare i file sul sito FTP degli attributi del cliente tramite FTP o SFTP:

* È necessario un client che supporti le connessioni SFTP.
* Puoi connetterti con SFTP utilizzando nome utente/password o senza utilizzare alcuna password, come descritto [qui](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=it).

**Per caricare il file di dati tramite FTP**

1. [Crea un&#39;origine attributo del cliente e carica il file di dati...](t-crs-usecase.md).

   Verifica di aver effettuato l’accesso al tuo sito FTP su `ftp.adobe.com/<sftpname>`.

1. Fai clic su **[!UICONTROL Azioni]** > **[!UICONTROL Caricamento file]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi `crs123.csv`, carica anche `crs123.fin`.

   Se il caricamento ha esito positivo, entrambi i file vengono spostati in una cartella denominata **elaborati**.

   Consulta [Requisiti dei file di dati per il caricamento di attributi del cliente](crs-data-file.md) per importanti informazioni sulla struttura e i nomi dei file.

## Configurare un account FTP

Imposta un account FTP per origine attributo.

Nella pagina [!UICONTROL Caricamento file e convalida schema], fare clic su **[!UICONTROL Configurazione FTP]**.

![Modificare uno schema](assets/ftp-account.png)

I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

I nomi applicati a stringhe, interi e numeri vengono utilizzati per creare metriche di [!DNL Analytics].

* **[!UICONTROL attributo:]** dati attributo letti dal file `.csv` caricato.

* **[!UICONTROL Tipo:]** il tipo di dati, ad esempio:

   * **Stringa:** una sequenza di caratteri.

   * **Interi:** numeri interi.

   * **Numeri:** possono contenere fino a due posizioni decimali.

* **[!UICONTROL Nome visualizzato:]** un nome descrittivo per l&#39;attributo. Ad esempio, puoi rinominare l&#39;attributo *customer age* in *customer Since*.

* **[!UICONTROL Descrizione:]** una descrizione dell&#39;attributo.