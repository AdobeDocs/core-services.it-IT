---
description: Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Uno schema viene creato in base a queste impostazioni. Lo schema viene utilizzato per convalidare tutti i dati futuri caricati in questa origine dati. Questo processo di mappatura non altera i dati originali.
keywords: customer attributes;core services
seo-description: Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Uno schema viene creato in base a queste impostazioni. Lo schema viene utilizzato per convalidare tutti i dati futuri caricati in questa origine dati. Questo processo di mappatura non altera i dati originali.
seo-title: Convalida dello schema
solution: Experience Cloud
title: Convalida dello schema
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Convalida dello schema

Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Uno schema viene creato in base a queste impostazioni. Lo schema viene utilizzato per convalidare tutti i dati futuri caricati in questa origine dati. Questo processo di mappatura non altera i dati originali.

>[!NOTE]
>
>L’aggiornamento dello schema dopo la convalida elimina gli attributi del cliente. Consulta [Aggiornare lo schema (elimina anche gli attributi)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

**[!UICONTROL Origine]** attributo del cliente > **[!UICONTROL Crea nuova origine]** attributo del cliente > **[!UICONTROL Visualizza/modifica schema]**

![](assets/view_edit_schema.png)

Nella pagina [!UICONTROL Convalida schema] ciascuna riga dello schema rappresenta una colonna del file CSV caricato.

![](assets/06_crs_usecase.png)

* **[!UICONTROL Aggiungi dati:]** consente di caricare nuovi dati dell’attributo in questa origine dati.

* **[!UICONTROL Visualizza/Modifica schema:]** consente di mappare i nomi visualizzati ai dati attributo come descritto nel passaggio successivo.

* **[!UICONTROL Configurazione FTP:]**[ carica i dati tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).

* **[!UICONTROL Ricerca ID:]** immetti un ID cliente dal file `.csv` per ricercare informazioni di Experience Cloud per l’ID. Questa funzionalità è utile per risolvere i problemi relativi alla mancata visualizzazione dei dati attributo di un visitatore:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Visualizza se utilizzi il servizio Experience Cloud ID più recente. Se ti trovi nel servizio MCID ma non è visualizzato alcun ID, significa che Experience Cloud non ha ricevuto un alias per quel CID. Ciò significa che il visitatore non ha effettuato l&#39;accesso o la tua implementazione non trasmette quell&#39;ID.

   * **[!UICONTROL CID (ID cliente):]** gli attributi associati a questo CID. Se stai usando una prop o un&#39;eVar per caricare CID (AVID) e sono visualizzati degli attributi ma nessun AVID, significa che il visitatore non ha effettuato l&#39;accesso al tuo sito.

   * **[!UICONTROL AVID (ID visitatore di Analytics):]** mostra se utilizzi una prop o eVar per caricare CID. Se tali ID vengono passati a Experience Cloud, tutti gli ID visitatore associati al CID immesso vengono visualizzati qui.

Puoi caricare i dati tramite FTP anche dopo la creazione di un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Potete creare un account FTP per origine attributo. I file caricati vengono memorizzati nella cartella principale di tale account. I dati devono essere in formato .csv, con un secondo file .fin per indicare il completamento del caricamento

I nomi applicati a stringhe, interi e numeri vengono utilizzati per creare metriche di [!DNL Analytics]. Per ulteriori informazioni, consulta Report [sugli attributi](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html) del cliente nella [!DNL Analytics] guida.

* **[!UICONTROL Attributo:]** dati degli attributi letti dal file `.csv` caricato.

* **[!UICONTROL Tipo:]** il tipo di dati, ad esempio:

   * **Stringa:** Una sequenza di caratteri.

   * **Integer:** Numeri interi.

   * **Numeri:** Può contenere fino a due posizioni decimali.

* **[!UICONTROL Nome visualizzato:]** un nome descrittivo per l’attributo. Ad esempio, puoi rinominare l’attributo *customer age* in *Cliente dal*.

* **[!UICONTROL Descrizione:]** una descrizione dell’attributo.
