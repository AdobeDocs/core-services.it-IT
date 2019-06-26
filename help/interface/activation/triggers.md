---
description: Come configurare Experience Cloud Triggers.
keywords: integrazioni;Triggers
seo-description: Come configurare Experience Cloud Triggers.
seo-title: Triggers
solution: Marketing Cloud
title: Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: ht
source-git-commit: 8ec57774743e8c32a17f18ae6dfe98c0767297a6

---


# Triggers

## Panoramica di Triggers {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

*Triggers* consente di identificare, definire e monitorare i comportamenti chiave dei consumatori, e quindi generare comunicazioni tra diverse soluzioni per coinvolgere nuovamente i visitatori. Puoi utilizzare i trigger nelle decisioni in tempo reale e nella personalizzazione.

* Configura la ricommercializzazione per carrelli abbandonati o carrelli abbandonati con la rimozione dei prodotti.
* Moduli e richieste incompleti.
* Qualsiasi azione o sequenza di azioni nel sito.

![](assets/trigger-abandonment-2.png)

**Tipi di Triggers**

In genere, un trigger può richiedere dai 15 ai 90 minuti per avviare una campagna di marketing. Questo varia a seconda dell’implementazione della raccolta di dati, del caricamento sulla pipeline, della configurazione personalizzata del trigger definito e del flusso di lavoro in Adobe Campaign.

* **Abbandono:** puoi creare un trigger che si attiva quando un visitatore visualizza un prodotto ma non aggiunge nulla al carrello. Configura il [Punteggio tendenza](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334) per capire la tendenza dei clienti dopo l’abbandono di un carrello.
* **Azione:** puoi creare trigger, ad esempio, che si attivano dopo che un utente ha effettuato un’iscrizione a una newsletter, un’iscrizione e-mail o ha usato applicazioni per le carte di credito (conferme). Se sei un rivenditore, puoi creare un trigger per un visitatore che si iscrive a un programma fedeltà. Nel settore di media e intrattenimento, crea trigger per i visitatori che guardano un determinato show e che desideri rispondano a un sondaggio.
* **Avvio e fine di sessione:** crea un trigger per eventi di avvio e fine di sessione.

## Creare un trigger di Experience Cloud {#task_821F37183AC045E5AC8EED20317598FE}

Crea un attivatore di abbandono e configurane le condizioni e il punteggio di propensione. Ad esempio, puoi specificare i criteri per le regole di un attivatore durante una visita, come metriche quali abbandono del carrello o dimensioni quali il nome del prodotto. Quando le regole non vengono rispettate, l&#39;attivatore entra in azione.

<!-- t_create-trigger.xml -->

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
   | Descrizione | Descrizione del trigger, modalità di utilizzo e così via. |
   | Suite di rapporti | La [suite di rapporti](https://marketing.adobe.com/resources/help/it_IT/analytics/getting-started/?f=report-suites) di Analytics utilizzata per questo trigger. Questa impostazione identifica i dati di reporting da utilizzare. |
   | La visita deve includere<br>La visita non deve includere<br>Trigger dopo nessuna azione<br>Includi metadati | Puoi definire i criteri o i comportamenti del visitatore desiderati e i comportamenti indesiderati.  Ad esempio, regole per un semplice trigger di abbandono carrello potrebbero essere:<ul><li>La visita deve includere: Aggiunta carrello (metrica) ed Esiste. (puoi definire ulteriormente la regola con una visualizzazione di prodotto specifica o con dimensioni come Tipi di browser).</li><li>La visita non deve includere: Pagamento.</li><li>Trigger dopo nessuna azione per: 10 minuti.</li><li>Includi metadati: ti consente di aggiungere una dimensione Campaign particolare o variabili rilevanti per il comportamento di un visitatore. Questo campo può essere utile per Adobe Campaign per creare l&#39;e-mail di ricommercializzazione corretta.</li></ul><br>Puoi specificare un operatore logico ANY, AND oppure OR all’interno o tra contenitori, a seconda dei criteri che ritieni importanti per la regola. |
   | Contenitore | Nei contenitori vengono impostati e archiviati regole, condizioni o filtri che definiscono un trigger. Se vuoi far verificare gli eventi contemporaneamente, inseriscili nello stesso contenitore. Ciò significa che ogni contenitore elabora indipendentemente a livello di risultato.  Ad esempio, in caso di due contenitori uniti dall’operatore AND, le regole saranno idonee quando due risultati soddisfano i requisiti. |
   | Avvia nuova sessione dopo | Crea un trigger per gli eventi di avvio e fine sessione. |

1. (Facoltativo) Nei trigger di abbandono, puoi applicare il [Punteggio tendenza](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334).

   ![Risultato passaggio](assets/propensity-scoring.png)

1. Fai clic su **[!UICONTROL Salva]**.
1. Utilizza i trigger per il [remarketing in tempo reale](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) in [!DNL Adobe Campaign].

### Esempio di trigger

**Trigger di abbandono carrello**

Ad esempio, nella pagina seguente sono illustrate le regole da utilizzare per il trigger di abbandono carrello, in base ai prodotti visualizzati durante una visita.

![](assets/abandonment-trigger.png)

**Trigger referrer**

Il trigger seguente si attiva quando viene visualizzato un risultato con il prodotto Stivali da uomo e il referrer Facebook. Per valutare i due criteri ( *products* e *referrer*) nello stesso risultato, devono essere aggiunti allo stesso contenitore.

![](assets/fb-boots-promo.png)

## Punteggio tendenza {#concept_A506150674AD45DB98D3CC07E560D334}

<!-- propensity-scoring.xml -->

Scopri la tendenza dei clienti a tornare dopo l&#39;abbandono di un carrello. Il punteggio tendenza è integrato in Experience Cloud Triggers ed è disponibile per i trigger di abbandono.

![Risultato passaggio](assets/propensity-scoring.png)

Ad esempio, alcuni clienti abbandonato i carrelli per usufruire di incentivi e-mail proposti per tornare al carrello. Per ridurre la perdita di profitti, l&#39;algoritmo Punteggio tendenza contribuisce a identificare le persone rilevanti che abbandonano il carrello e che probabilmente non torneranno senza l&#39;incentivo.

È possibile:

* Evitare la sovraesposizione dei clienti alla ricommercializzazione.
* Identificare i clienti giusti che abbandonano il carrello e mapparne l&#39;attività al messaggio giusto.
* Aumentare i profitti scoprendo quali clienti torneranno e quali non lo faranno.

## Valore del punteggio tendenza {#section_CA99874A25434CC0BF01D0DA61608889}

Puoi eseguire il rilevamento dei dati per identificare i comportamenti o gli schemi nascosti esistenti nei tuoi dati. In particolare, il punteggio di propensione ti aiuta a identificare cluster di clienti simili utilizzando metodi più focalizzati e obiettivi al posto dei semplici filtri o segmentazione. Inoltre, il punteggio di propensione ti consente di impostare funzionalità predittive per identificare il comportamento per il cliente di alto valore della tua società.

Una volta identificato il pubblico di alto valore, puoi coinvolgerlo per il massimo risultato. Ad esempio, se la tua attività è di tipo business-to-business, i commericali potrebbero chiamare i lead e questo potrebbe permetterti di valutare i lead e identificarne la probabilità di conversione offline. Poiché ogni lead aumenta i costi, la creazione di un incentivo per identificare potenziali clienti con la massima probabilità di conversione di una vendita è il metodo più efficace e conveniente per focalizzare le risorse.

L&#39;assegnazione di un punteggio di probabilità permette di identificare i fattori più predittivi di un punteggio specifico o di aumentare la probabilità del verifciarsi di un evento, ma anche di rispondere a domande specifiche.

* Il cliente eseguirà la conversione?
* Il cliente risponderà a un&#39;e-mail?
* Il cliente eseguirà di nuovo l&#39;acquisto?

Il punteggio tendenza consente di rispondere a queste domande e di identificare i visitatori con un&#39;inclinazione all&#39;azione che potrà essere impostata e valutata.
