---
description: Crea e gestisci le offerte da utilizzare in Adobe Campaign.
seo-description: Crea e gestisci le offerte da utilizzare in Adobe Campaign.
seo-title: Gestione offerte
title: Gestione offerte
uuid: 83e1d4cd-c5fa-4df0-9603-2914eb4648f8
index: y
translation-type: tm+mt
source-git-commit: a0e0b51d731343d5cd4226ab29d917aca63317c2

---


# Offerte

Crea e gestisci le offerte da utilizzare in Adobe Campaign.

In Gestione [!UICONTROL offerta]sono disponibili due tipi di offerte:

| Tipo | Descrizione |
|---|---|
| Offerta generale | Consente di compilare l&#39;intero modello dati dell&#39;offerta (regole di idoneità, date di inizio e fine e contenuto). |
| Offerta fallback | L&#39;ultima offerta di ricorso se un cliente non è idoneo per nessuna delle altre offerte selezionate. Non è possibile associare regole di idoneità né date di inizio e fine alle offerte di fallback. |

>[!NOTE]
>
>In un&#39;attività di offerta, vi verrà sempre chiesto di selezionare un&#39;offerta di fallback. Pertanto, prima di poter creare un&#39;attività di offerta è necessario disporre di almeno un&#39;offerta di fallback nell&#39;inventario delle offerte.

## Creare un&#39;offerta

Create un&#39;offerta da aggiungere all&#39;inventario delle offerte.

1. Dalla scheda [!UICONTROL Inventory] in Gestione offerta, fate clic su **[!UICONTROL Create New Offer (Crea nuova offerta]**), quindi selezionate**[!UICONTROL  Create Offer (Crea offerta)]**.

   ![](assets/create-offerx.png)

1. Compila i campi seguenti:

   | Campo | Descrizione |
   |--- |--- |
   | Nome offerta | Nome associato all’offerta. Non è possibile avere due offerte nell&#39;inventario con nomi duplicati. |
   | Data di inizio | Data in cui può essere visualizzata l’offerta. Se è selezionata una data di inizio di 1/15/17, l&#39;offerta può essere visualizzata a partire dalle 12:00 del 1/15/17.  La gestione dell&#39;offerta funziona secondo lo standard di ora UTC. Ciò significa che: <ul><li> Le offerte diventano valide alle 00:00 UTC del giorno in cui l&#39;offerta è impostata per iniziare.</li><li> Le offerte scadono alle 00:00 UTC del giorno successivo alla data di fine. Ad esempio, se un&#39;offerta è impostata su una data di fine di 5/14, l&#39;offerta scade alle 00:00 UTC delle 5/15. L&#39;offerta viene quindi archiviata.</li><li>Quando i messaggi e-mail vengono preparati in Adobe Campaign, verranno visualizzate solo le offerte valide in quel momento.</li></ul> |
   | Data di fine | Data in cui termina l&#39;offerta. Se è selezionata una data di fine di 1/20/17, l&#39;offerta non viene più visualizzata dopo le 11:59 del 20/17. Quando un&#39;offerta supera la data di fine, viene automaticamente archiviata. La gestione dell&#39;offerta funziona secondo lo standard di ora UTC. Per ulteriori informazioni, vedi la riga precedente. |
   | Regole di ammissibilità | Potete creare le regole di idoneità per le offerte in base ai dati disponibili nel database Campaign. Le regole di idoneità determinano a chi e quando visualizzare un&#39;offerta.  Ad esempio, potete specificare che desiderate che venga visualizzata solo l&#39;offerta di abbigliamento invernale per le donne quando (Genere = &#39;Femmina&#39;) e (Regione = &#39;Northeast&#39;). Gli attributi utilizzati per creare queste regole provengono dal profilo Campaign Standard.  Nota:  Quando accedete per la prima volta a Gestione offerte, non sono disponibili attributi nel generatore di regole. Devi condividere gli attributi dall&#39;interfaccia utente di Campaign. Una volta condivisi, questi attributi sono disponibili. |
   | Max cap | I tempi massimi per la proposta di un&#39;offerta.  Nota:  Il numero di volte in cui viene proposta un&#39;offerta viene calcolato al momento della preparazione dell&#39;e-mail. Ad esempio, se preparate un&#39;e-mail con una serie di offerte, questi numeri vengono conteggiati per il limite massimo, indipendentemente dal fatto che l&#39;e-mail venga inviata o meno. |
   | Limite massimo per utente | Il numero massimo di volte per cui un&#39;offerta può essere proposta a un determinato utente.  Nota:  Il numero di volte in cui un&#39;offerta viene proposta a un determinato utente viene calcolata al momento della preparazione dell&#39;e-mail. Ad esempio, se preparate un&#39;e-mail con una serie di offerte, questi numeri vengono conteggiati per il limite massimo per utente, indipendentemente dal fatto che l&#39;e-mail venga inviata o meno. |
   | Etichette | Aggiungete etichette a un&#39;offerta per raggrupparle. Potete digitare e premere Invio per creare una nuova etichetta o iniziare a digitare e selezionare un&#39;offerta esistente dall&#39;elenco a discesa. |

1. Compila i dettagli delle rappresentazioni.

   | Campo | Descrizione |
   |---|---|
   | Canale | Canale in cui è possibile distribuire la rappresentazione del contenuto. Le e-mail di Campaign Standard sono l&#39;unico canale attualmente disponibile. |
   | Inserimento | Selezionate la posizione in cui può essere distribuita la rappresentazione del contenuto. I posizionamenti sono precompilati dalla scheda Posizionamenti. È necessario associare ogni rappresentazione di contenuto a una posizione dal menu a discesa. Non potete creare più rappresentazioni di contenuto con lo stesso posizionamento nella stessa offerta. |
   | Tipo di contenuto | Selezionate un tipo di contenuto di immagine, URL immagine, testo o HTML. |
   | Collegamento di reindirizzamento | Questo campo viene visualizzato se selezionate un tipo di contenuto di URL immagine o immagine. Questo è il collegamento a cui verrà reindirizzato l&#39;utente se fa clic su tale offerta in un messaggio e-mail. |

1. Fate clic su **[!UICONTROL Salva e visualizza anteprima]**per esaminare i dettagli dell’offerta prima dell’invio.
1. Fate clic su **[!UICONTROL Approva]**per approvare l&#39;offerta. Una volta che l&#39;offerta è nello stato approvato, può essere utilizzata in un&#39;attività di offerta.

   Se non disponete delle autorizzazioni necessarie per approvare un&#39;offerta, fate clic su **[!UICONTROL Invia]**. L&#39;offerta verrà quindi visualizzata nella libreria delle offerte con uno stato in sospeso. Una volta che un utente con diritti di approvazione lo approva, sarà disponibile per l&#39;uso in un&#39;attività di offerta.
