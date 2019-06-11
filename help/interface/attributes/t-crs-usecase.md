---
description: Creazione della sorgente attributo e caricamento del file di dati.
keywords: attributi del cliente; servizi di base
seo-description: Creazione della sorgente attributo e caricamento del file di dati.
seo-title: Creazione di una sorgente attributo cliente e caricamento del file di dati
solution: Experience Cloud
title: Creazione di una sorgente attributo cliente e caricamento del file di dati
uuid: 53 dca 789-9 a 91-4385-839 d-c 9 d 1 aa 36 b 9 be
translation-type: tm+mt
source-git-commit: b6058194725c3ad50d280a3daad737cd53416204

---


# Creazione di una sorgente attributo cliente e caricamento del file di dati

Creazione della sorgente attributo e caricamento del file di dati. Potete attivare l&#39;origine dati quando siete pronti. Quando la sorgente dati è attiva, condividi i dati attributo in Analytics e Target.

## Flusso di lavoro degli attributi del cliente {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [Creazione di un file di dati](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [Creazione di una sorgente attributo e caricamento del file di dati](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Convalida dello schema](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


Dopo l&#39;attivazione dell&#39;origine dati puoi:

* [Uso degli attributi del cliente in Adobe Analytics](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Uso degli attributi del cliente in Adobe Target](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>Per accedere a questa funzione, gli utenti devono essere assegnati al profilo di prodotto Attributi cliente (Attributi cliente - Accesso predefinito). **[!UICONTROL (Amministrazione]** &gt; **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Utenti]** &gt;). Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi del cliente] presente in [!UICONTROL Audiences], sul lato sinistro dell&#39;interfaccia Experience Cloud.
>
>L&#39;iscrizione al gruppo della soluzione è necessaria.

Per utilizzare la funzione Attributi cliente, gli utenti devono appartenere al gruppo Attributi cliente Adobe nella gestione utenti e ai gruppi a livello di soluzione (Analytics o Target).

Consulta [Utenti e gruppi](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## Creazione di un file di dati {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

Questi dati sono dati aziendali del cliente dal CRM. I dati includono i dati dell&#39;utente con sottoscrizione per prodotti, inclusi ID membro, prodotti autorizzati, prodotti più lanciati e così via.


1. Create un [!DNL .csv].


   >[!NOTE]
   >
   >Successivamente in questa procedura, trascinerai il [!DNL .csv] file per caricare il file. Tuttavia, se caricate [tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B), dovete anche disporre di [!DNL .fin] un file con lo stesso nome del [!DNL .csv]file.



   Esempio di un file di dati di un cliente aziendale:

   ![](assets/01_crs_usecase.png)

1. Prima di continuare, controllate le informazioni importanti in [Requisiti file di dati](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)prima di caricare il file.
1. [Crea un&#39;origine attributo del cliente e carica il di dati](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) come descritto.

## Creazione di una sorgente attributo cliente e caricamento del file di dati {#task_09DAC0F2B76141E491721C1E679AABC8}

Segui questi passaggi nella pagina Crea nuova origine attributo del cliente in Experience Cloud.


>[!IMPORTANT]
>
>Durante la creazione, la modifica o l&#39;eliminazione delle origini attributo del cliente, si verifica un ritardo di circa un&#39;ora prima della effettiva sincronizzazione degli ID con la nuova origine dati. Devi disporre di diritti amministrativi in Audience Manager per creare o modificare origini attributo del cliente. Contatta l&#39;assistenza clienti di Audience Manager o consulta la consulenza per ottenere i diritti amministrativi.


1. In [!DNL Experience Cloud], fate clic ![](assets/menu-icon.png) sull&#39;icona Menu.
1. Fai clic **[!UICONTROL su Persone]**, quindi su **[!UICONTROL Attributi cliente]**.

   La pagina [!UICONTROL Attributi del cliente] è il luogo in cui puoi gestire e modificare l&#39;origine dati degli attributi esistenti.

   ![Risultato passaggio](assets/03_crs_usecase.png)
1. Fate clic **[!UICONTROL su Nuovo]**.

   ![Risultato passaggio](assets/04_crs_usecase.png)
1. Nella pagina [!UICONTROL Modifica origine attributo del cliente] configura i campi seguenti:


   * **[!UICONTROL Nome:]** Un nome descrittivo per l&#39;origine attributo dei dati. Per [!DNL Adobe Target], i nomi degli attributi non possono includere spazi. Se viene passato un attributo con uno spazio, questo viene [!DNL Target] ignorato. Altri caratteri non supportati sono: `< , >, ', "`.

   * **[!UICONTROL Descrizione:]** (Facoltativo) Descrizione dell&#39;origine attributo dei dati.

   * **[!UICONTROL ID alias:]** Rappresenta un&#39;origine dei dati attributo del cliente, ad esempio un sistema CRM specifico. Un ID univoco utilizzato nel codice origine attributo del cliente. L&#39;ID deve essere univoco, in lettere minuscole e non deve comprendere spazi. Il valore immesso nel campo ID alias per l’origine attributo del cliente nell’interfaccia utente Experience Cloud deve corrispondere ai valori ottenuti dall’implementazione (tramite sia Dynamic Tag Management sia JavaScript del Mobile SDK).

      L&#39;ID alias corrisponde ad alcune aree in cui imposti valori ID cliente aggiuntivi. Ad esempio:

      * **Gestione tag dinamica:** L&#39;ID alias corrisponde al *valore Codice* integrazione in [!UICONTROL Impostazioni cliente], nello [strumento Experience](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) Cloud ID Service.

      * **API visitatore:** l&#39;ID alias corrisponde agli [ID cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids) aggiuntivi che puoi associare a ciascun visitatore.

         Ad esempio, *&quot;crm_ id&quot;* in:


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS:** L&#39;ID alias corrisponde a *&quot;idtype&quot;* in [visitorsyncidentifiers: identificatori](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods).

         Ad esempio:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android:** l&#39;ID alias corrisponde a *&quot; Idtype &quot;* in [syncidentifiers](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods).

         Ad esempio:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         Consultate [Utilizzo di più origini dati](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) per ulteriori informazioni sull&#39;elaborazione dei dati in merito al campo ID alias e agli ID cliente.
   * **[!UICONTROL Caricamento file:]** Puoi trascinare il file [!DNL .csv] di dati o caricare i dati tramite FTP. (L&#39;utilizzo dell&#39;FTP richiede anche un [!DNL .fin] file). Consultate [Caricare i dati tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).


      >[!IMPORTANT]
      >
      >Esistono requisiti specifici del file di dati. Per [ulteriori informazioni, consulta Requisiti](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) del file di dati.


      Dopo avere effettuato il caricamento del file, i dati della tabella vengono visualizzati nell&#39;intestazione [!UICONTROL Caricamento file] in questa pagina. Puoi convalidare lo schema, configurare sottoscrizioni o impostare l&#39;FTP.



      **Elemento grafico caricamento file**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL ID cliente univoco:]** Mostra quanti ID univoci hai caricato in questa origine attributo.

   * **[!UICONTROL ID forniti dal cliente con alias agli ID visitatore di Experience Cloud:]** Mostra quanti ID sono stati alias agli ID visitatore di Experience Cloud.

   * **[!UICONTROL ID forniti dal cliente con conteggio alias elevato:]** Visualizza il numero di ID forniti dal cliente con 500 o più ID visitatore di Experience Cloud con alias. Questi ID forniti dal cliente non rappresentano individui ma accessi condivisi. Il sistema distribuisce gli attributi associati a questi ID ai 500 ID visitatore di Experience Cloud con alias più recenti, fino a raggiungere la soglia di 10.000. Una volta raggiunto tale numero, il sistema invalida l&#39;ID fornito dal cliente e non distribuisce più attributi associati.










## Convalida dello schema {#task_404AAC411B0D4E129AB3AC8B7BE85859}

Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). È inoltre possibile eliminare gli attributi aggiornando lo schema.

Vedere [Convalida dello schema](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043).

Per eliminare gli attributi, consultate [(Facoltativo) Aggiornare lo schema (eliminare gli attributi)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

## (Facoltativo) Aggiornare lo schema (attributi eliminazione) {#task_6568898BB7C44A42ABFB86532B89063C}

Come eliminare gli attributi e sostituire gli attributi dello schema.


1. Nella pagina [!UICONTROL Modifica origine] attributo del cliente rimuovi l&#39;iscrizione **[!UICONTROL di Target]** o **[!UICONTROL Analytics]** (in [!UICONTROL Configura iscrizioni]).
1. [Caricare un nuovo file di dati con campi aggiornati](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8).

## Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo {#task_1ACA21198F0E46A897A320C244DFF6EA}

La configurazione di una sottoscrizione imposta il flusso di dati tra Experience Cloud e le soluzioni. Attivando l&#39;origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web e dall&#39;applicazione.

Consultate [Configurare le iscrizioni](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF).

**Per attivare un&#39;origine attributo**

A [! Pagina UICONTROL Crea nuova [o Modifica] origine attributo cliente, individua l&#39;intestazione [!UICONTROL Activate (Attiva] ), quindi fai clic su **[!UICONTROL Active (Attivo]**).

![Risultato passaggio](assets/activate_attribute_source.png)

## Usare gli attributi del cliente in Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Con i dati ora disponibili in soluzioni come
<keyword>
Adobe Analytics
</keyword>, puoi generare rapporti sui dati, analizzarli e intraprendere l&#39;azione appropriata nelle campagne di marketing.

L&#39;esempio seguente mostra un segmento di [!DNL Analytics] basato su attributi multipli. Questo segmento mostra utenti con sottoscrizione di Photoshop Lightroom il cui prodotto maggiormente lanciato è Photoshop.

![](assets/08_crs_usecase.png)

Quando pubblichi un segmento in Experience Cloud, diventa disponibile in Experience Cloud Audiences e Audience Manager.

Consulta [Rapporto attributi cliente](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes) nell&#39;Aiuto di Analytics per ulteriori informazioni.

## Usare gli attributi del cliente in Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

In Target puoi selezionare un attributo del cliente dalla sezione Profilo visitatore al momento della creazione di un tipo di pubblico. Tutti gli attributi del cliente avranno il prefisso [!DNL crs.] nell&#39;elenco. Per creare di tipi di pubblico combina questi attributi con altri attributi di dati.

![](assets/crs-add-attribute-target.png)

Consulta [Creazione di un nuovo pubblico](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience) nell&#39;Aiuto di Target.
