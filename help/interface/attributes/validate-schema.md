---
description: Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Sulla base delle impostazioni viene creato uno schema. Puoi usare lo schema per convalidare tutti i dati futuri caricati in questa origine dati. Questa procedura di mappatura non altera i dati originali.
keywords: attributi del cliente; servizi di base
seo-description: Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Sulla base delle impostazioni viene creato uno schema. Puoi usare lo schema per convalidare tutti i dati futuri caricati in questa origine dati. Questa procedura di mappatura non altera i dati originali.
seo-title: Convalida dello schema
solution: Experience Cloud
title: Convalida dello schema
uuid: 163 a 4 dbe-d 60 b -4089-8 ff 8-65 f 7461 fbdf 7
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Convalida dello schema

Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Sulla base delle impostazioni viene creato uno schema. Puoi usare lo schema per convalidare tutti i dati futuri caricati in questa origine dati. Questa procedura di mappatura non altera i dati originali.


>[!NOTE]
>
>L&#39;aggiornamento dello schema dopo la convalida elimina gli attributi del cliente. Consultate [Aggiornare lo schema (eliminare anche gli attributi)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).


**[!UICONTROL Origine attributo del cliente]** &gt; **[!UICONTROL Crea nuova origine attributo del cliente]** &gt; **[!UICONTROL Visualizza/Modifica schema]**

![](assets/view_edit_schema.png)

Nella pagina [!UICONTROL Convalida schema] ciascuna riga dello schema rappresenta una colonna del file CSV caricato.

![](assets/06_crs_usecase.png)

* **[!UICONTROL Aggiungi dati:]** Carica nuovi dati attributo in questa origine dati.

* **[!UICONTROL Visualizza/Modifica schema:]** Mappa i nomi visualizzati sui dati degli attributi, come descritto nel passaggio successivo.

* **[!UICONTROL Configurazione FTP:]**[Caricare i dati tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).

* **[!UICONTROL Ricerca ID:]** Immetti un ID cliente (CID) dal tuo [!DNL .csv] per cercare informazioni Experience Cloud per l&#39;ID. Questa funzionalità è utile per risolvere i problemi relativi alla mancata visualizzazione dei dati attributo di un visitatore:

   * **[!UICONTROL MCID (Experience Cloud ID):]** Viene visualizzato se stai utilizzando il servizio Experience Cloud ID più recente. Se ti trovi nel servizio MCID ma non è visualizzato alcun ID, significa che Experience Cloud non ha ricevuto un alias per quel CID. Ciò significa che il visitatore non ha effettuato l&#39;accesso o la tua implementazione non trasmette quell&#39;ID.

   * **[!UICONTROL CID (ID cliente):]** Gli attributi associati a questo CID. Se stai usando una prop o un&#39;eVar per caricare CID (AVID) e sono visualizzati degli attributi ma nessun AVID, significa che il visitatore non ha effettuato l&#39;accesso al tuo sito.

   * **[!UICONTROL AVID (ID visitatore di Analytics):]** Visualizza se utilizzate una prop o evar per caricare CID. Se questi ID sono trasmessi a Experience Cloud, qualsiasi ID visitatore associato al CID immesso viene visualizzato qui.






Puoi caricare i dati tramite FTP anche dopo la creazione di un&#39;origine attributo del cliente e un account FTP in Experience Cloud. Puoi creare un account FTP per origine attributo. I file caricati vengono archiviati nella cartella principale di quell&#39;account. I dati devono essere in formato .csv e un secondo file .fin deve indicare il completamento del caricamento.

I nomi applicati a stringhe, integer e numeri vengono utilizzati per creare [!DNL Analytics] metriche. Consulta [Rapporto attributi cliente](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes) nell&#39;Aiuto di per ulteriori informazioni.[!DNL Analytics]

* **[!UICONTROL Attributo:]** Dati attributo letti dal [!DNL .csv] file caricato.

* **[!UICONTROL Tipo:]** Tipo di dati, ad esempio:

   * **Stringa:** una sequenza di caratteri.

   * **Integer:** numeri interi.

   * **Numeri:** fino a due numeri decimali.




* **[!UICONTROL Nome visualizzato:]** Un nome descrittivo per l&#39;attributo. Ad esempio, puoi cambiare un&#39;età *cliente attributo* in *Cliente da*.

* **[!UICONTROL Descrizione:]** Una descrizione descrittiva dell&#39;attributo.



