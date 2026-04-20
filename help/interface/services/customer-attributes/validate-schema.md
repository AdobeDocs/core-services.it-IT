---
description: Scopri come convalidare lo schema  [!DNL Customer Attributes]  in Adobe CX Enterprise.
solution: Experience Cloud
title: 'Convalida dello schema  [!DNL Customer Attributes] '
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
TQID: https://experienceleague.adobe.com/J-AaDn4HtD1bS-VCPn2XiPLVBbTnYyl5o1NpJ9HFj1g
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 43%

---

# Convalidare lo schema

Il procedimento di convalida consente di mappare i nomi visualizzati e le descrizioni agli attributi caricati (stringhe, interi, numeri e così via).

Uno schema viene creato in base a queste impostazioni. Lo schema viene utilizzato per convalidare tutti i dati futuri caricati in questa sorgente dati. Il processo di mappatura non altera i dati originali.

>[!NOTE]
>
>L’aggiornamento dello schema dopo la convalida elimina gli attributi del cliente. Consulta [Aggiornare lo schema (elimina anche gli attributi)](t-crs-usecase.md).

**Per convalidare lo schema**

1. In [!DNL Customer Attributes], fare clic sull&#39;origine attributo da modificare.

1. In **[!UICONTROL Edit Customer Attribute Source]**, fare clic su **[!UICONTROL File Upload]**.

1. Nella pagina [!UICONTROL File Upload and Schema Validation], fare clic su **[!UICONTROL Actions]** > **[!UICONTROL View/Edit Schema]**

   ![Modificare uno schema](assets/actions.png)

   Nella pagina [!UICONTROL Edit Schema], ogni riga dello schema rappresenta una colonna del file CSV caricato.

   ![Modifica pagina schema in CX Enterprise](assets/schema-edit.png)

**Azioni**

* **[!UICONTROL Add Data:]** Carica nuovi dati attributo in questa origine dati.

* **[!UICONTROL View/Edit Schema:]** Mappare i nomi visualizzati ai dati attributo come descritto nel passaggio successivo.

* **[!UICONTROL FTP Setup:]** Crea il tuo account FTP per [caricare i tuoi dati tramite FTP](t-upload-attributes-ftp.md) (facoltativo).

* **[!UICONTROL ID Lookup:]** Immetti un ID cliente (CID) da `.csv` per cercare informazioni di CX Enterprise per l&#39;ID. Questa funzionalità è utile per risolvere i problemi relativi alla mancata visualizzazione dei dati attributo di un visitatore:

   * **[!UICONTROL ECID (CX Enterprise ID):]** Indica se stai utilizzando il servizio CX Enterprise ID più recente. Se ti trovi nel servizio MCID ma non è elencato alcun ID, CX Enterprise non ha ricevuto un alias per quel CID. Ciò significa che il visitatore non ha effettuato l&#39;accesso o la tua implementazione non trasmette quell&#39;ID.

   * **[!UICONTROL CID (customer ID):]** Attributi associati a questo CID. Se stai usando una prop o un&#39;eVar per caricare CID (AVID) e sono visualizzati degli attributi ma nessun AVID, significa che il visitatore non ha effettuato l&#39;accesso al tuo sito.

   * **[!UICONTROL AVID (Analytics visitor ID):]** mostra se utilizzi una prop o eVar per caricare CID. Se questi ID vengono passati a CX Enterprise, tutti gli ID visitatore associati al CID che hai inserito vengono visualizzati qui.
