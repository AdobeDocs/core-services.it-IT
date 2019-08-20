---
description: Creazione della sorgente attributo e caricamento del file di dati.
keywords: attributi del cliente;servizi principali
seo-description: Creazione della sorgente attributo e caricamento del file di dati.
seo-title: Creazione di una sorgente attributo cliente e caricamento del file di dati
solution: Experience Cloud
title: Creazione di una sorgente attributo cliente e caricamento del file di dati
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# Creazione di una sorgente attributo cliente e caricamento del file di dati

Crea l'origine attributo del cliente (file CSV e FIN) e carica i dati. Puoi attivare l’origine dati quando lo desideri. Quando la sorgente dati è attiva, condividi i dati attributo in Analytics e Target.

## Flusso di lavoro attributi cliente {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [Creazione di un file di dati](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [Creazione di una sorgente attributo e caricamento del file di dati](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Convalida dello schema](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Configurazione delle sottoscrizioni e attivazione dell'origine attributo](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


Dopo l'attivazione dell'origine dati puoi:

* [Uso degli attributi del cliente in Adobe Analytics](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Uso degli attributi del cliente in Adobe Target](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>Per accedere a questa funzione, gli utenti devono essere assegnati al profilo di prodotto Attributi cliente (Attributi cliente - Accesso standard). ( **[!UICONTROL Amministrazione]** &gt; **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Utenti]** &gt; ). Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi del cliente] presente in [!UICONTROL Audiences], sul lato sinistro dell'interfaccia Experience Cloud.
>
>L'iscrizione al gruppo della soluzione è necessaria.

Per utilizzare la funzione Attributi cliente, gli utenti devono appartenere al gruppo Attributi cliente Adobe nella gestione utenti e ai gruppi a livello di soluzione (Analytics o Target).

Consulta [Utenti e gruppi](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## Creazione di un file di dati {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

Questi dati sono dati aziendali del cliente dal CRM. I dati includono i dati dell'utente con sottoscrizione per prodotti, inclusi ID membro, prodotti autorizzati, prodotti più lanciati e così via.


1. Crea un `.csv`.


   >[!NOTE]
   >
   >Successivamente in questa procedura, trascinerai il `.csv` per caricare il file. Tuttavia, se [effettui il caricamento tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B), serve anche un file `.fin` con la stessa denominazione del file `.csv`.



   Esempio di un file di dati di un cliente aziendale:

   ![](assets/01_crs_usecase.png)

1. Prima di continuare, controlla le informazioni importanti in [Requisiti dei file di dati](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) prima di caricare il file.
1. [Crea un'origine attributo del cliente e carica il di dati](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) come descritto.

## Creazione di una sorgente attributo cliente e caricamento del file di dati {#task_09DAC0F2B76141E491721C1E679AABC8}

Segui questi passaggi nella pagina Crea nuova origine attributo del cliente in Experience Cloud.


>[!IMPORTANT]
>
>Quando crei, modifichi o elimini origini attributo del cliente, si verifica un ritardo di circa un’ora prima della effettiva sincronizzazione degli ID con la nuova origine dati. Devi disporre di diritti di amministratore in Audience Manager per creare o modificare origini degli attributi del cliente. Contatta l’Assistenza clienti o la consulenza di Audience Manager per ottenere i diritti di amministratore.


1. In [!DNL Experience Cloud], fate clic sull’icona Menu ![](assets/menu-icon.png).
1. In **[!DNL Experience Platform]**, fai clic **[!UICONTROL su Persone]** &gt; **[!UICONTROL Attributi del cliente]**.

   La pagina [!UICONTROL Attributi del cliente] è il luogo in cui puoi gestire e modificare l'origine dati degli attributi esistenti.

   ![Risultato passaggio](assets/03_crs_usecase.png)
1. Fai clic su **[!UICONTROL Nuovo]**.

   ![Risultato passaggio](assets/04_crs_usecase.png)
1. Nella pagina [!UICONTROL Modifica origine attributo del cliente] configura i campi seguenti:


   * **[!UICONTROL Nome:]** un nome descrittivo per l’origine dell’attributo dei dati. In [!DNL Adobe Target], i nomi degli attributi non possono includere spazi. Se viene passato un attributo con uno spazio, [!DNL Target] lo ignora. Altri caratteri non supportati sono: `< , >, ', "`.

   * **[!UICONTROL Descrizione:]** (facoltativo) una descrizione per l’origine dell’attributo dei dati.

   * **[!UICONTROL ID alias:]** rappresenta un’origine dei dati attributo del cliente come specificato nel sistema CRM. Un ID univoco utilizzato nel codice origine attributo del cliente. L'ID deve essere univoco, in lettere minuscole e non deve comprendere spazi. Il valore immesso nel campo ID alias per l’origine attributo del cliente nell’interfaccia utente Experience Cloud deve corrispondere ai valori ottenuti dall’implementazione (tramite sia Dynamic Tag Management sia JavaScript del Mobile SDK).

      L'ID alias corrisponde ad alcune aree in cui imposti valori ID cliente aggiuntivi. Ad esempio:

      * **Gestione tag dinamica:** L'ID alias corrisponde al *valore Codice* integrazione in [!UICONTROL Impostazioni cliente], nello [strumento Experience](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) Cloud ID Service.

      * **API visitatore:** l'ID alias corrisponde agli [ID cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids) aggiuntivi che puoi associare a ciascun visitatore.

         Ad esempio, *“crm_ id”* in:


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS:** L'ID alias corrisponde a *"idtype"* in [visitorsyncidentifiers: identificatori](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods).

         Ad esempio:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android:** l'ID alias corrisponde a *" Idtype "* in [syncidentifiers](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods).

         Ad esempio:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         Consulta [Utilizzo di più origini dati](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) per ulteriori informazioni sull’elaborazione dei dati in merito al campo ID alias e agli ID cliente.
   * **[!UICONTROL Caricamento file:]** puoi trascinare il file di dati `.csv` o caricare i dati tramite FTP. (Con un FTP serve anche un file `.fin`.) Consulta [Caricamento dei dati tramite FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).


      >[!IMPORTANT]
      >
      >Esistono dei requisiti del file di dati specifici. Consulta [Requisiti dei file di dati](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) per ulteriori informazioni.


      Dopo avere effettuato il caricamento del file, i dati della tabella vengono visualizzati nell'intestazione [!UICONTROL Caricamento file] in questa pagina. Puoi convalidare lo schema, configurare sottoscrizioni o impostare l'FTP.



      **Grafico caricamento del file**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL ID cliente univoco:]** mostra quanti ID univoci hai caricato in questa origine attributo.

   * **[!UICONTROL ID forniti dal cliente come alias degli ID visitatore di Experience Cloud:]** mostra quanti ID sono impostati come alias degli ID visitatore di Experience Cloud.

   * **[!UICONTROL ID forniti dal cliente con soglia degli alias elevata:]** visualizza il numero di ID forniti dal cliente con 500 o più ID visitatore di Experience Cloud con alias. Questi ID forniti dal cliente non rappresentano individui ma accessi condivisi. Il sistema distribuisce gli attributi associati a questi ID ai 500 ID visitatore di Experience Cloud con alias più recenti, fino a raggiungere la soglia di 10.000. Una volta raggiunto tale numero, il sistema invalida l'ID fornito dal cliente e non distribuisce più attributi associati.










## Convalida dello schema {#task_404AAC411B0D4E129AB3AC8B7BE85859}

Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Puoi anche eliminare gli attributi aggiornando lo schema.

Consulta [Convalida dello schema](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043).

Per eliminare gli attributi, consulta [(Facoltativo) Aggiornare lo schema (eliminare gli attributi)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

## (Facoltativo) Aggiornare lo schema (eliminare gli attributi) {#task_6568898BB7C44A42ABFB86532B89063C}

Informazioni su come eliminare e sostituire gli attributi nello schema.


1. Nella pagina [!UICONTROL Modifica origine attributo del cliente], rimuovi la sottoscrizione a **[!UICONTROL Target]** o **[!UICONTROL Analytics]** (in [!UICONTROL Configura sottoscrizioni]).
1. [Carica un nuovo file di dati con campi aggiornati](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8).

## Configurazione delle sottoscrizioni e attivazione dell'origine attributo {#task_1ACA21198F0E46A897A320C244DFF6EA}

La configurazione di una sottoscrizione imposta il flusso di dati tra Experience Cloud e le soluzioni. Attivando l'origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web e dall'applicazione.

Consulta [Configurazione delle sottoscrizioni](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF).

**Per attivare un'origine attributo**

Nella pagina [!UICONTROL Crea nuova [o Modifica] origine attributo del cliente], individua l’intestazione [!UICONTROL Attiva], quindi fai clic su **[!UICONTROL Attivo]**.

![Risultato passaggio](assets/activate_attribute_source.png)

## Usare gli attributi del cliente in Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Con i dati ora disponibili in soluzioni come
<keyword>
Adobe Analytics
</keyword>, puoi generare rapporti sui dati, analizzarli e intraprendere le azioni necessarie nelle campagne di marketing.

L'esempio seguente mostra un segmento di [!DNL Analytics] basato su attributi multipli. Questo segmento mostra utenti con sottoscrizione di Photoshop Lightroom il cui prodotto maggiormente lanciato è Photoshop.

![](assets/08_crs_usecase.png)

Quando pubblichi un segmento in Experience Cloud, diventa disponibile in Experience Cloud Audiences e Audience Manager.

Consulta [Rapporto attributi cliente](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes) nell'Aiuto di Analytics per ulteriori informazioni.

## Usare gli attributi del cliente in Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

In Target puoi selezionare un attributo del cliente dalla sezione Profilo visitatore al momento della creazione di un tipo di pubblico. Tutti gli attributi del cliente avranno il prefisso [!DNL crs.] nell’elenco. Per creare di tipi di pubblico combina questi attributi con altri attributi di dati.

![](assets/crs-add-attribute-target.png)

Consulta [Creazione di un nuovo pubblico](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience) nell'Aiuto di Target.
