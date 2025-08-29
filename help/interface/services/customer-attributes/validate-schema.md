---
description: Scopri come convalidare lo schema  [!DNL Customer Attributes]  in Adobe Experience Cloud.
solution: Experience Cloud
title: 'Convalida dello schema  [!DNL Customer Attributes] '
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: d2244e249c7af27bc1b4fc7bfe628bc25b37f4d4
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 49%

---

# Convalida dello schema

Il processo di convalida consente di mappare i nomi visualizzati e le descrizioni agli attributi caricati (stringhe, interi, numeri e così via).

Uno schema viene creato in base a queste impostazioni. Lo schema viene utilizzato per convalidare tutti i dati futuri caricati in questa sorgente dati. Il processo di mappatura non altera i dati originali.

>[!NOTE]
>
>L’aggiornamento dello schema dopo la convalida elimina gli attributi del cliente. Consulta [Aggiornare lo schema (elimina anche gli attributi)](t-crs-usecase.md).

**Per convalidare lo schema**

1. In [!DNL Customer Attributes], fare clic sull&#39;origine attributo da modificare.

1. In **[!UICONTROL Modifica attributo cliente Source]**, fare clic su **[!UICONTROL Caricamento file]**.

1. Nella pagina [!UICONTROL Caricamento file e convalida schema], fai clic su **[!UICONTROL Azioni]** > **[!UICONTROL Visualizza/Modifica schema]**

   ![Modificare uno schema](assets/actions.png)

   Nella pagina [!UICONTROL Modifica schema], ogni riga dello schema rappresenta una colonna del file CSV caricato.

   ![Modifica pagina schema in Experience Cloud](assets/schema-edit.png)

**Azioni**

* **[!UICONTROL Aggiungi dati:]** consente di caricare nuovi dati dell&#39;attributo in questa origine dati.

* **[!UICONTROL Visualizza/Modifica schema:]** consente di mappare i nomi visualizzati ai dati attributo come descritto nel passaggio successivo.

* **[!UICONTROL Configurazione FTP:]** Crea il tuo account FTP per [caricare i tuoi dati tramite FTP](t-upload-attributes-ftp.md) (facoltativo).

* **[!UICONTROL Ricerca ID:]** Immetti un ID cliente (CID) da `.csv` per cercare informazioni di Experience Cloud per l&#39;ID. Questa funzionalità è utile per risolvere i problemi relativi alla mancata visualizzazione dei dati attributo di un visitatore:

   * **[!UICONTROL ECID (Experience Cloud ID):]** indica se stai utilizzando il servizio Experience Cloud ID più recente. Se ti trovi nel servizio MCID ma non è elencato alcun ID, Experience Cloud non ha ricevuto un alias per quel CID. Ciò significa che il visitatore non ha effettuato l&#39;accesso o la tua implementazione non trasmette quell&#39;ID.

   * **[!UICONTROL CID (ID cliente):]** gli attributi associati a questo CID. Se stai usando una prop o un&#39;eVar per caricare CID (AVID) e sono visualizzati degli attributi ma nessun AVID, significa che il visitatore non ha effettuato l&#39;accesso al tuo sito.

   * **[!UICONTROL AVID (ID visitatore di Analytics):]** mostra se utilizzi una prop o eVar per caricare CID. Se tali ID vengono passati ad Experience Cloud, tutti gli ID visitatore associati al CID inserito vengono visualizzati qui.
