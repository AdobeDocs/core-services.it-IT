---
description: Scopri come utilizzare le offerte e condividere i campi in Adobe Campaign Standard.
seo-description: Scopri come utilizzare le offerte e condividere i campi in Adobe Campaign Standard.
seo-title: Campaign
title: Campaign
uuid: ceeec50c-6441-4ced-915b-c73f349f7a21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a0e0b51d731343d5cd4226ab29d917aca63317c2

---


# Campaign{#campaign}

Scopri come utilizzare le offerte e condividere i campi in Adobe Campaign Standard.

Dopo aver creato almeno un&#39;offerta di fallback e un&#39;offerta generale, potete creare un&#39;attività di offerta utilizzando un messaggio e-mail in Campaign Standard. Un&#39;attività di offerta può essere creata solo in una campagna e-mail regolare. Non può essere aggiunto a una campagna e-mail transazionale (ad esempio, un&#39;e-mail ricorrente attivata da un evento, ad esempio un messaggio e-mail di abbandono del carrello).

Un&#39;attività di offerta vi chiederà di selezionare un gruppo di offerte e un&#39;offerta di fallback che potrebbero essere visualizzate in una posizione in un modello e-mail. L&#39;offerta migliore da distribuire è selezionata tra quelle offerte al momento della preparazione delle e-mail, in base al posizionamento, alla data, allo stato dell&#39;offerta e ai dati del profilo cliente.

## Condivisione di attributi da Campaign a [!UICONTROL Offer Management]{#task_4DFA9A20D7B04E1F9AFF4774D67B6EBC}

Quando create un&#39;offerta in Gestione offerta, potete impostare regole di idoneità che limitano i profili che possono ricevere determinate offerte. Queste regole di idoneità possono essere impostate in base agli attributi (o ai campi) presenti nel profilo Campaign. Questi campi devono essere condivisi da Campaign prima che vengano visualizzati nel generatore di regole di idoneità di [!UICONTROL Gestione] offerte.

>[!NOTE]
>
>Per condividere gli attributi, è necessario disporre dei diritti di amministratore in Campaign.

1. Fai clic su **[!UICONTROL Adobe Campaign]**per accedere alla navigazione.
1. Andate a **[!UICONTROL Amministrazione]**> Impostazioni**** istanza > Gestione ****offerta e fate clic su**[!UICONTROL  Attributi]**.

   Questa pagina mostra gli attributi che sono già stati condivisi. Potete modificare o eliminare questi attributi.

   ![](assets/campaign-share5.png)

   >[!NOTE]
   >
   >Se un attributo è attualmente utilizzato da [!UICONTROL Offer Management] in una regola di idoneità, non può essere eliminato.

1. Fai clic su **[!UICONTROL Crea]**.

1. Fate clic sull&#39;icona della cartella per definire l&#39;origine dati Campaign e selezionate l&#39;elemento da condividere.

   ![](assets/campaign-share7.png)

1. Selezionare un&#39;etichetta dati di destinazione.

   Questo è il nome dell&#39;attributo che verrà visualizzato nel generatore di regole di idoneità in Gestione offerta.

1. Fai clic su **[!UICONTROL Crea]**.

   L&#39;attributo viene visualizzato nel generatore di regole di idoneità di [!UICONTROL Gestione] offerte al momento della creazione e della modifica delle offerte.

   ![](assets/campaign-share2.png)

## Creare un&#39;attività di offerta {#task_F63ADDA52BD949779DB491E4D56E664E}

Inserite un&#39;attività di offerta in qualsiasi immagine o blocco di testo all&#39;interno di un modello e-mail in Campaign Standard.

1. Per inserire un&#39;attività offerta in una posizione immagine, fate clic una volta sull&#39;immagine per visualizzare l&#39;icona Inserisci offerta.

   ![](assets/insert-offer-activity.png)

1. (Alternativa): Per inserire un&#39;attività di offerta in un blocco di testo, fate clic due volte sul blocco di testo per visualizzare l&#39;icona Inserisci offerta.

1. Compila i dettagli nella scheda Dettagli  attività della schermata [!UICONTROL Crea attività] offerta:

   | Campo | Descrizione |
   |---|---|
   | Nome attività | Assegna un nome all’attività. Non potete immettere un nome di attività già utilizzato in un&#39;altra attività di offerta. |
   | Inserimento | Selezionare la posizione da utilizzare per la posizione. In questo modo si garantisce che solo le offerte con una rappresentazione di contenuto corrispondente a quella fornita a un utente vengano servite per il posizionamento. Solo le offerte con questo posizionamento vengono visualizzate negli elenchi delle offerte per tutto il resto della creazione dell&#39;attività. |

1. Nella scheda [!UICONTROL Seleziona offerte] , selezionate le offerte che desiderate includere nell&#39;attività.

   Potete selezionare gruppi di offerte utilizzando etichette o singole offerte una per una.

   * **Selezione di gruppi di offerte tramite etichette:**

      Per selezionare gruppi di offerte utilizzando le etichette, fate clic sulla scheda Generatore **[!UICONTROL di]**regole, quindi fate clic su**[!UICONTROL  Aggiungi regola]**etichetta. Per creare regole per determinare quali offerte includere nell&#39;attività dell&#39;offerta, selezionate l&#39;etichetta. Tra le etichette appare un operatore _AND_ . Per cambiare l&#39;operatore da _AND_ a _OR_, fare clic sull&#39;operatore.

      ![](assets/offer-actvity-rule-builder.png)

   * **Selezione di singole offerte:**

      Per selezionare singole offerte, fate clic sulla scheda **[!UICONTROL Inventario]**offerte. Un utente può effettuare ricerche all’interno dell’elenco delle offerte per nome, ID offerta o etichette aggiunte all’offerta.

      Fate clic sul segno più per aggiungere le offerte alla sezione Offerte selezionate dell&#39;elenco.

      ![](assets/create-offer2.png)

      Affinché un&#39;offerta sia disponibile sia nel generatore di regole che nell&#39;inventario delle offerte, deve:

   * Corrispondenza con la data odierna.
   * Avere uno stato di approvazione.
   * Una rappresentazione del contenuto con una posizione corrispondente a quella selezionata al Passaggio 1.

      >[!NOTE]
      >
      >Le offerte elencate nella scheda Inventario offerte vengono filtrate solo in base al posizionamento e allo stato di approvazione. Non sono stati filtrati in modo che corrispondano ai criteri di targeting impostati per l&#39;e-mail in Adobe Campaign.

1. Nella scheda [!UICONTROL Offerta] di fallback, selezionate un&#39;offerta di fallback. L&#39;offerta di fallback viene inviata solo a un cliente che non è idoneo per altre offerte. Potete selezionare un&#39;unica offerta di fallback dall&#39;elenco.
1. Visualizzate il riepilogo dell&#39;attività dell&#39;offerta e fate clic su **[!UICONTROL Fine]**.

   L&#39;offerta migliore per ogni utente sarà determinata al momento della preparazione dell&#39;e-mail valutando quanto segue:

* **** Controllo posizionamento: Tutte le offerte devono avere una rappresentazione del contenuto che corrisponda alla posizione selezionata come parte dell&#39;attività dell&#39;offerta. Se una posizione per un&#39;offerta viene eliminata tra il tempo di creazione dell&#39;attività e il tempo di preparazione (se il tempo è superiore a tre minuti), tale offerta non viene considerata.
* **** Controllo data: Tutte le offerte devono essere valide per la data corrente ( _non_ è la data di invio dell&#39;offerta). La data in cui preparate la campagna e-mail è la data in cui viene determinata l’offerta da distribuire. Ad esempio, se preparate una campagna e-mail il 15/15/17 e una delle offerte selezionate non è valida fino al 16/17, l&#39;offerta non viene servita.

* **** Controllo regola di idoneità: Tutte le offerte devono soddisfare le regole di [ammissibilità](offers.md).

* **** Controllo prioritario: Se un utente è idoneo per più offerte, [!UICONTROL Gestione] offerte utilizza la priorità impostata dall&#39;utente per determinare quale offerta mostrare a ciascun utente.

   Il messaggio e-mail è pronto per essere inviato. Selezionate la scheda [!UICONTROL Rapporti] nella [!DNL Adobe Campaign] home page per verificare le prestazioni delle offerte.

   Per ulteriori informazioni sull&#39;utilizzo di Adobe Campaign, consulta le guide seguenti:

* [Creazione di un&#39;e-mail](https://docs.campaign.adobe.com/doc/standard/en/CHA_Email_messages_Creating_an_email.html)
* [Invio di un messaggio e-mail](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/about-sending-messages-with-campaign.html)
* [Informazioni sui report dinamici](https://docs.campaign.adobe.com/doc/standard/en/RPT_About_reporting_About_dynamic_reports.html)

## Rapporti sulle offerte

Adobe Campaign offre tre dimensioni di offerta (offerta, attività di offerta, posizionamento delle offerte) e una metrica (clic sulle offerte) che consentono di monitorare le offerte e misurarne l&#39;impatto. Per visualizzare i rapporti, visita la scheda Rapporti in Adobe Campaign Standard. Potete creare il rapporto e trascinare e rilasciare diverse dimensioni di offerta nel pannello del rapporto per iniziare a filtrare i dati.

![](assets/offers-reports.png)

Per ulteriori informazioni su come creare i rapporti dinamici in Campaign, consulta [I rapporti](https://docs.campaign.adobe.com/doc/standard/en/RPT_About_reporting_About_dynamic_reports.html)dinamici.