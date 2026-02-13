---
description: Scopri come caricare i dati degli attributi del cliente tramite FTP in Experience Cloud.
solution: Experience Cloud
title: Caricare file di dati di attributi cliente tramite FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
TQID: https://experienceleague.adobe.com/jI2dWXMmrrWxceVi-sZtzF5cTF11iy4d7QKkx71vF-I
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 55%

---

# Caricare il file di dati tramite FTP (opzionale)

Se non effettui il caricamento trascinando la selezione, puoi caricare l’attributo del cliente in Experience Cloud tramite FTP.

Puoi caricare i dati dopo aver creato un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per ogni sorgente attributo. I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

>[!IMPORTANT]
>
>Rivedi [Origini e file di dati degli attributi del cliente](crs-data-file.md) prima di caricare il file.

È possibile caricare i file sul sito FTP degli attributi del cliente tramite FTP o SFTP:

* È necessario un client che supporti le connessioni SFTP.
* Puoi connetterti con SFTP utilizzando nome utente/password o senza utilizzare alcuna password, come descritto [qui](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=it).

**Per caricare il file di dati tramite FTP**

1. [Crea un&#39;origine attributo del cliente e carica il file di dati...](t-crs-usecase.md).

   Verifica di aver effettuato l’accesso al tuo sito FTP su `ftp.adobe.com/<sftpname>`.

1. Fare clic su **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Carica un file `.fin` in modo che possa essere recuperato.

   Il tipo di file `.fin` è creato dall&#39;utente e segnala che il caricamento è terminato. Può essere un file del blocco note vuoto. Ad esempio, se carichi `crs123.csv`, carica anche `crs123.fin`.

   Se il caricamento ha esito positivo, entrambi i file vengono spostati in una cartella denominata **elaborati**.

   Per informazioni importanti sui nomi e sulla struttura dei file, vedere [File di dati degli attributi del cliente](crs-data-file.md).

## Configurare un account FTP

Imposta un account FTP per origine attributo.

Nella pagina [!UICONTROL File Upload and Schema Validation], fare clic su **[!UICONTROL FTP Setup]**.

![Modificare uno schema](assets/ftp-account.png)

I file caricati vengono memorizzati nella cartella root di tale account. I dati devono essere in formato `.csv` e un secondo file `.fin` deve indicare il completamento del caricamento.

I nomi applicati a stringhe, interi e numeri vengono utilizzati per creare metriche di [!DNL Analytics].

* **[!UICONTROL attribute:]** dati attributo letti dal file `.csv` caricato.

* **[!UICONTROL Type:]** Il tipo di dati, ad esempio:

   * **Stringa:** una sequenza di caratteri.

   * **Interi:** numeri interi.

   * **Numeri:** possono contenere fino a due posizioni decimali.

* **[!UICONTROL Display Name:]** Nome descrittivo per l&#39;attributo. Ad esempio, puoi rinominare l&#39;attributo *customer age* in *customer Since*.

* **[!UICONTROL Description:]** Una descrizione dell&#39;attributo.

