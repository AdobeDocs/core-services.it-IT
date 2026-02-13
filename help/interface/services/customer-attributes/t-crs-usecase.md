---
description: Scopri come creare un’origine dati  [!DNL Customer Attributes]  e caricarla in Experience Cloud.
solution: Experience Cloud
title: 'Creazione e caricamento di un file di Data Source  [!DNL Customer Attributes] '
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
TQID: https://experienceleague.adobe.com/tnqjX4iY7OQx4XW9MjHNg8LaXB1Of6MrtLX-7efyz-E
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 1061
ht-degree: 47%

---

# Creare e caricare i dati degli attributi cliente

Creare l&#39;origine attributo del cliente (`.csv` e `.fin` file) e caricare i dati. Puoi attivare l&#39;origine dati quando lo desideri. Dopo che l&#39;origine dati è attiva, condividere i dati attributo in [!DNL Analytics] e [!DNL Target].

**[!DNL Customer Attributes]flusso di lavoro**

![Flusso di lavoro per attributi cliente](assets/crs.png)

## Prerequisiti per l&#39;utilizzo di [!DNL Customer Attributes] {#prerequisites}

* **Appartenenza al gruppo:** Per caricare i dati, gli utenti devono essere membri del gruppo [!DNL Customer Attributes]. Devi anche appartenere a un gruppo Adobe Analytics o Adobe Target.

  Per sapere se l&#39;azienda ha accesso a Attributi del cliente, l&#39;amministratore [!DNL Experience Cloud] deve effettuare l&#39;accesso a [Experience Cloud](https://experience.adobe.com). Passa a **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. Se *[!DNL Customer Attributes]* viene visualizzato come uno dei [!UICONTROL product profiles], è possibile iniziare.

  Gli utenti aggiunti a [!DNL Customer Attributes] visualizzano la voce di menu [!DNL Customer Attributes] sul lato sinistro dell&#39;interfaccia di Experience Cloud.

* Per Attributi del cliente è necessaria qualsiasi versione **Adobe Target** di `at.js` o la versione 5.8 di `mbox.js` o successive.

  Consulta [Come distribuire at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html).

## Creazione di un file di dati

Questi dati sono dati aziendali dei clienti provenienti dal tuo sistema CRM. Possono includere i dati degli utenti con sottoscrizione relativi ai prodotti, inclusi ID membro, prodotti autorizzati, prodotti più lanciati e così via.

1. Crea un file `.csv`.

   >[!NOTE]
   >
   >Successivamente in questa procedura, trascinare e rilasciare il file `.csv` per caricare il file. Tuttavia, se [effettui il caricamento tramite FTP](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B), serve anche un file `.fin` con la stessa denominazione del file `.csv`.

   Esempio di un file di dati di un cliente aziendale:

   ![Esempio di un file di dati di un cliente aziendale](assets/01_crs_usecase.png)

1. Prima di continuare, controlla le informazioni importanti in [Requisiti dei file di dati](crs-data-file.md) e dopo carica il file.
1. [Crea un&#39;origine attributo del cliente e carica il di dati](t-crs-usecase.md#create-source) come descritto.

## Creare un’origine di attributi e caricare il file di dati

Eseguire questi passaggi sulla pagina _[!UICONTROL Create Customer Attribute Source]_&#x200B;in Experience Cloud.

>[!IMPORTANT]
>
>Quando crei, modifichi o elimini origini attributo del cliente, si verifica un ritardo di circa un&#39;ora prima della effettiva sincronizzazione degli ID con la nuova origine dati. Devi disporre di diritti di amministratore in Audience Manager per creare o modificare origini degli attributi del cliente. Per ottenere i diritti di amministratore, contatta l’Assistenza clienti o la consulenza di Audience Manager.

1. Per aprire [!UICONTROL Customer Attributes], fare clic su **[!UICONTROL Apps]** ![menu](assets/menu-icon.png) > **[!DNL Customer Attributes]**.

   ![Pagina attributi cliente](assets/cust-attr.png)

1. Fai clic su **[!UICONTROL New]**.

   ![Risultato del passaggio](assets/new-customer-attribute-source.png)

1. Nella pagina [!UICONTROL Create Customer Attribute Source] configurare i campi seguenti:

   * **[!UICONTROL Name:]** Nome descrittivo per l&#39;origine attributo dati. In [!DNL Adobe Target], i nomi degli attributi non possono includere spazi. Se viene passato un attributo con uno spazio, [!DNL Target] lo ignora. Altri caratteri non supportati sono: `< , >, ', "`.

   * **[!UICONTROL Description:]** (facoltativo) descrizione dell&#39;origine attributo dei dati.

   * **[!UICONTROL Alias ID:]** Rappresenta un&#39;origine dei dati attributo del cliente, ad esempio un sistema CRM specifico. [!UICONTROL Alias ID] è un ID univoco utilizzato nel codice [!UICONTROL customer attribute Source]. L&#39;ID deve essere univoco, in lettere minuscole e non deve comprendere spazi. Il valore immesso nel campo [!UICONTROL Alias ID] per l&#39;origine attributi del cliente in Experience Cloud deve corrispondere ai valori ricevuti dall&#39;implementazione (tramite Raccolta dati di Platform o JavaScript del SDK mobile).

     >[!IMPORTANT]
     >
     >L’eliminazione di un’origine dati associata a un ID alias non rende disponibile l’ID alias, in quanto viene salvato in più servizi e utilizzato per mappare i profili tra di essi.

     L’ID alias corrisponde ad alcune aree in cui puoi impostare valori ID cliente aggiuntivi. Ad esempio:

      * **Tag:** L&#39;ID alias corrisponde al valore *Integration Code* in [!UICONTROL customer Settings], nello strumento [Servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=it).

      * **API visitatore:** l&#39;ID alias corrisponde agli ulteriori [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) che è possibile associare a ogni visitatore.

        Ad esempio, *“crm_ id”* in:

        ```
        "crm_id":"67312378756723456"
        ```

      * **iOS:** l&#39;ID alias corrisponde a *&quot;idType&quot;* in [visitorSyncIdentifiers:identifiers](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=it).

        Ad esempio:

        `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™:** l’ID alias corrisponde a *“idType”* in [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=it).

        Ad esempio:

        `identifiers.put(`**`"idType"`**`, "idValue");`

        Consulta [Utilizzo di più origini dati](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) per ulteriori informazioni sull&#39;elaborazione dei dati relativi al campo ID alias e agli ID cliente.

   * **[!UICONTROL Namespace Code:]** Utilizzare questo valore per identificare l&#39;origine attributo del cliente quando si utilizza [IdentityMap](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/identity/overview) come parte di un&#39;implementazione di AEP WebSDK.

1. Fai clic su **[!UICONTROL Save]**.

## Carica il file {#upload-customer-attributes}

Viene creato il record di attributi cliente, che puoi caricare modificando l’attributo cliente.

1. Nella pagina [!DNL Customer Attributes] fare clic sull&#39;origine attributo.

1. Nella pagina [!UICONTROL Edit Customer Data Source], fare clic su **[!UICONTROL File Upload]**.

   ![Caricamento file e convalida schema](assets/file-upload-schema-validation.png)

1. Trascinare e rilasciare il file di dati `.csv` o `.zip` o `.gzip` nella finestra di trascinamento.

>[!IMPORTANT]
>
>Esistono dei requisiti del file di dati specifici. Consulta [Requisiti dei file di dati](crs-data-file.md) per ulteriori informazioni.

Dopo aver caricato il file, i dati della tabella vengono visualizzati nell&#39;intestazione [!UICONTROL File Upload] di questa pagina. È possibile convalidare lo schema, configurare sottoscrizioni o impostare l&#39;FTP.

![attributi](assets/file_upload_attributes.png)

* **[!UICONTROL Unique customer ID:]** mostra quanti ID univoci hai caricato in questa origine attributo.

* **[!UICONTROL customer-Provided IDs Aliased to Experience Cloud Visitor IDs:]** mostra quanti ID sono impostati come alias degli ID visitatore di Experience Cloud.

* **[!UICONTROL customer-Provided IDs with High Alias Counts:]** Visualizza il numero di ID forniti dal cliente con 500 o più ID visitatore di Experience Cloud con alias. Questi ID forniti dal cliente non rappresentano individui ma accessi condivisi. Il sistema distribuisce gli attributi associati a questi ID ai 500 ID visitatore di Experience Cloud con alias più recenti, fino a raggiungere la soglia di 10.000. Quindi, il sistema invalida l’ID fornito dal cliente e non distribuisce più gli attributi associati. —>

## Convalida dello schema {#validate-schema}

Il procedimento di convalida consente di mappare i nomi visualizzati e le descrizioni agli attributi caricati (stringhe, interi, numeri e così via). Puoi anche eliminare gli attributi aggiornando lo schema.

Consulta [Convalida dello schema](validate-schema.md).

Per eliminare gli attributi, consulta [(Facoltativo) Aggiornare lo schema (eliminare gli attributi)](t-crs-usecase.md).

## (Facoltativo) Aggiornare lo schema (eliminare gli attributi)

Informazioni su come eliminare e sostituire gli attributi nello schema.

1. Nella pagina [!UICONTROL Edit Customer Attribute Source], rimuovere la sottoscrizione **[!UICONTROL Target]** o **[!UICONTROL Analytics]** (in **[!UICONTROL Configure Subscriptions]**).

1. [Carica un nuovo file di dati con campi aggiornati](t-crs-usecase.md).

## Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo

La configurazione di una sottoscrizione imposta il flusso di dati tra Experience Cloud e le applicazioni. L’attivazione dell’origine degli attributi consente il flusso dei dati verso le applicazioni sottoscritte. I record cliente che hai caricato vengono associati ai segnali ID in entrata provenienti dal sito web o dall&#39;applicazione.

Consulta [Configurare le sottoscrizioni e attivare l&#39;origine dati](subscription.md).

## Usa i dati di [!DNL Customer Attributes] in Adobe Analytics

Con i dati ora disponibili in applicazioni come Adobe Analytics, puoi creare rapporti sui dati, analizzarli e intraprendere azioni appropriate nelle campagne di marketing.

L’esempio seguente mostra un segmento di [!DNL Analytics] basato sugli attributi caricati. Questo segmento mostra gli utenti con sottoscrizione a [!DNL Photoshop Lightroom] il cui prodotto maggiormente lanciato è Photoshop.

![Segmento di Analytics basato sugli attributi caricati](assets/08_crs_usecase.png)

Quando pubblichi un segmento in Experience Cloud, diventa disponibile in Experience Cloud Audiences e Audience Manager.

## Usa i dati di [!DNL Customer Attributes] in Adobe Target

In [!DNL Target] è possibile selezionare un attributo del cliente dalla sezione [!UICONTROL Visitor Profile] durante la creazione di un pubblico. Tutti gli attributi del cliente hanno il prefisso `crs.` nell&#39;elenco. Per creare dei tipi di pubblico, combina questi attributi con altri attributi di dati.

![Utilizzo degli Attributi del cliente in Adobe Target](assets/crs-add-attribute-target.png)

Consulta [Creare un pubblico](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=it) nella guida di [!DNL Target].
