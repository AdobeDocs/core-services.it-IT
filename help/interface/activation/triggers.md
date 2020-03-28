---
description: Come configurare Experience Cloud Triggers.
keywords: integrations;Triggers
seo-description: Come configurare Experience Cloud Triggers.
seo-title: Triggers
solution: Marketing Cloud
title: Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Triggers

## Panoramica di Triggers {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

*Triggers* consente di identificare, definire e monitorare i comportamenti chiave dei consumatori, quindi di generare comunicazioni tra più soluzioni per coinvolgere nuovamente i visitatori. Puoi utilizzare i trigger nelle decisioni in tempo reale e nella personalizzazione.

* Configurare la ricommercializzazione rapida per carrelli abbandonati o carrelli abbandonati con la rimozione dei prodotti
* Moduli e applicazioni incompleti
* Qualsiasi azione o sequenza di azioni sul sito

![](assets/trigger-abandonment-2.png)

### Tipi di Triggers

In genere, un trigger può richiedere dai 15 ai 90 minuti per avviare una campagna di marketing. Questo varia a seconda dell’implementazione della raccolta di dati, del caricamento sulla pipeline, della configurazione personalizzata del trigger definito e del flusso di lavoro in Adobe Campaign.

* **Abbandono:** puoi creare un trigger che si attiva quando un visitatore visualizza un prodotto ma non aggiunge nulla al carrello. Configura il [Punteggio tendenza](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334) per capire la tendenza dei clienti dopo l’abbandono di un carrello.
* **Azione:** puoi creare trigger, ad esempio, che si attivano dopo che un utente ha effettuato un’iscrizione a una newsletter, un’iscrizione e-mail o ha usato applicazioni per le carte di credito (conferme). Se sei un rivenditore, puoi creare un trigger per un visitatore che si iscrive a un programma fedeltà. Nei contenuti multimediali e di intrattenimento, crea trigger per i visitatori che guardano un determinato show e che desideri rispondere con un sondaggio.
* **Avvio e fine sessione:** Creare un trigger per gli eventi di inizio e fine sessione.

## Creare un trigger di Experience Cloud {#task_821F37183AC045E5AC8EED20317598FE}

Crea un attivatore di abbandono e configurane le condizioni e il punteggio di propensione. Ad esempio, puoi specificare i criteri per le regole di un attivatore durante una visita, come metriche quali abbandono del carrello o dimensioni quali il nome del prodotto. Quando le regole sono soddisfatte, l&#39;attivatore viene eseguito.

>[!NOTE]
>
>Esiste attualmente un limite tecnico di 100 trigger.

1. In Experience Cloud, fai clic su ![](assets/menu-icon.png), quindi su **[!UICONTROL Activation]**.
1. Trova la scheda [!UICONTROL Triggers] e fai clic su **[!UICONTROL Avvia]**.

   ![Risultato passaggio](assets/activation-triggers.png)

1. Fai clic su **[!UICONTROL Nuovo trigger]** e specifica il tipo di trigger:

   ![Risultato passaggio](assets/add-trigger.png)

1. Configura il trigger completando i campi seguenti e trascinando metriche ed elementi dimensione nei contenitori della regola:

   | Elemento | Descrizione |
   |--- |--- |
   | Nome | Nome intuitivo per il trigger. |
   | Descrizione | Descrizione di questo attivatore, modalità di utilizzo e così via. |
   | Suite di rapporti | La suite [di](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-reports-report-suites.html) rapporti di Analytics utilizzata per questo trigger. Questa impostazione identifica i dati di reporting da utilizzare. |
   | Visit must include<br>Visit must not include<br>Trigger after no action<br>Include meta data | Puoi definire i criteri o i comportamenti del visitatore desiderati e i comportamenti indesiderati.  Ad esempio, regole per un semplice trigger di abbandono carrello potrebbero essere:<ul><li>La visita deve includere: Aggiunta carrello (metrica) ed Esiste. (puoi definire ulteriormente la regola con una visualizzazione di prodotto specifica o con dimensioni come Tipi di browser).</li><li>La visita non deve includere: Pagamento.</li><li>Trigger dopo nessuna azione per: 10 minuti.</li><li>Includi metadati: ti consente di aggiungere una dimensione Campaign particolare o variabili rilevanti per il comportamento di un visitatore. Questo campo può essere utile per Adobe Campaign per creare l&#39;e-mail di ricommercializzazione corretta.</li></ul><br>Puoi specificare un operatore logico ANY, AND oppure OR all’interno o tra contenitori, a seconda dei criteri che ritieni importanti per la regola. |
   | Contenitore | Nei contenitori vengono impostati e archiviati regole, condizioni o filtri che definiscono un trigger. Se vuoi far verificare gli eventi contemporaneamente, inseriscili nello stesso contenitore. Ciò significa che ogni contenitore elabora indipendentemente a livello di risultato.  Ad esempio, in caso di due contenitori uniti dall’operatore AND, le regole saranno idonee quando due risultati soddisfano i requisiti. |
   | Avvia nuova sessione dopo | Creare un trigger per gli eventi di inizio e fine sessione. |

1. (Optional) In [!UICONTROL Abandonment triggers], you can apply [Propensity Scoring](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334).

   ![Risultato passaggio](assets/propensity-scoring.png)

1. Fai clic su **[!UICONTROL Salva]**.
1. Use triggers for [real-time remarketing](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) in [!DNL Adobe Campaign].

### Esempio di trigger

Esempi di Experience Cloud Triggers:

#### Trigger abbandono carrello

Ad esempio, nella pagina seguente sono illustrate le regole che è possibile utilizzare per un trigger di abbandono carrello, in base ai prodotti visualizzati durante una visita.

![](assets/abandonment-trigger.png)

#### Trigger referente

Il trigger seguente si attiva quando viene visualizzato un risultato con il prodotto Stivali da uomo e il referrer Facebook. Per valutare i due criteri (*products* e *referrer*) nello stesso risultato, devono essere aggiunti allo stesso contenitore.

![](assets/fb-boots-promo.png)

## Punteggio tendenza {#concept_A506150674AD45DB98D3CC07E560D334}

Scopri la tendenza dei clienti a tornare dopo l&#39;abbandono di un carrello. Il punteggio tendenza è integrato in Experience Cloud Triggers ed è disponibile per i trigger di abbandono.

![Risultato passaggio](assets/propensity-scoring.png)

Ad esempio, alcuni clienti abbandonato i carrelli per usufruire di incentivi e-mail proposti per tornare al carrello. Per ridurre la perdita di ricavi, l&#39;algoritmo Punteggio tendenza aiuta a identificare i pertinenti abbandonatori del carrello che probabilmente non torneranno senza l&#39;incentivo.

È possibile:

* Evitare di esporre eccessivamente i clienti alla ricommercializzazione.
* Identificare i clienti giusti che abbandonano il carrello e mappare la loro attività al messaggio giusto.
* Aumenta i ricavi conoscendo quali clienti torneranno e quali non torneranno.

### Valore del punteggio tendenza {#section_CA99874A25434CC0BF01D0DA61608889}

Puoi eseguire il rilevamento dei dati per identificare i comportamenti o gli schemi nascosti esistenti nei tuoi dati. In particolare, il punteggio di propensione ti aiuta a identificare cluster di clienti simili utilizzando metodi più focalizzati e obiettivi al posto dei semplici filtri o segmentazione. Inoltre, il punteggio di propensione ti consente di impostare funzionalità predittive per identificare il comportamento del cliente di alto valore della tua azienda.

Una volta identificato il pubblico di alto valore, puoi coinvolgerlo per il massimo risultato. Ad esempio, se la tua attività è di tipo business-to-business, i commericali potrebbero chiamare i lead e questo potrebbe permetterti di valutare i lead e identificarne la probabilità di conversione offline. Poiché ogni lead aumenta i costi, creare un incentivo per identificare potenziali clienti con la massima probabilità di conversione di una vendita è il modo più efficace e meno costoso per concentrare le risorse.

Il punteggio tendenza consente di identificare i fattori più predittivi di un punteggio particolare o di aumentare la probabilità che si verifichi un evento, ma può anche essere applicato per rispondere a domande specifiche:

* Il cliente eseguirà la conversione?
* Il cliente risponderà a un&#39;e-mail?
* Il cliente riacquisterà?

Il punteggio tendenza consente di rispondere a queste domande e identificare i visitatori con un&#39;inclinazione all&#39;azione che può essere impostata e valutata.
