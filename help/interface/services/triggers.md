---
description: Scopri come configurare Experience Cloud Triggers.
solution: Experience Cloud
title: Panoramica di Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 9dc26e2f-479b-49a5-93ce-b877559fea43
source-git-commit: 163dc8ef83fb83a0e51879520bcb3ae697c95144
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 94%

---

# Experience Cloud Triggers

[!UICONTROL Triggers] in Experience Cloud consente di identificare, definire e monitorare i comportamenti chiave dei consumatori, per poi generare comunicazioni tra le diverse soluzioni in modo da coinvolgere nuovamente i visitatori.

## Panoramica di Triggers {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

Puoi utilizzare i trigger nelle decisioni in tempo reale e nella personalizzazione. Esempio:

* Configura il remarketing rapido di carrelli abbandonati o di carrelli abbandonati con i prodotti rimossi
* Applicazioni e moduli incompleti
* Qualsiasi azione o sequenza di azioni sul sito

![Esempio di trigger](../assets/trigger-abandonment-2.png)

>[!NOTE]
>
>Ulteriori informazioni sull’utilizzo di [!UICONTROL Triggers] sono disponibili in [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html).

### Tipi di Triggers

In genere, un trigger può richiedere dai 15 ai 90 minuti per avviare una campagna di marketing. Questo varia a seconda dell’implementazione della raccolta di dati, del caricamento sulla pipeline, della configurazione personalizzata del trigger definito e del flusso di lavoro in Adobe Campaign.

* **Abbandono:** puoi creare un trigger che si attiva quando un visitatore visualizza un prodotto ma non aggiunge nulla al carrello.
* **Azione:** puoi creare trigger, ad esempio, che si attivano dopo che un utente ha effettuato un&#39;iscrizione a una newsletter, un&#39;iscrizione e-mail o ha usato applicazioni per le carte di credito (conferme). Se sei un rivenditore, puoi creare un trigger per un visitatore che si iscrive a un programma fedeltà. Nei contenuti multimediali e di intrattenimento, crea trigger per i visitatori che guardano un determinato show e che vorresti rispondessero a un sondaggio.
* **Avvio e fine sessione:** crea un trigger per gli eventi di inizio e fine sessione.

## Creare un trigger di Experience Cloud {#task_821F37183AC045E5AC8EED20317598FE}

Crea un trigger e configurane le condizioni. Ad esempio, puoi specificare i criteri per le regole di un attivatore durante una visita, come metriche quali abbandono del carrello o dimensioni quali il nome del prodotto. Quando le regole sono soddisfatte, il trigger viene eseguito.

>[!NOTE]
>
>Esiste attualmente un limite tecnico di 100 trigger.

1. In Experience Cloud, fai clic su ![menu](../assets/menu-icon.png), quindi su **[!UICONTROL Raccolta dati/Launch]**.
2. Individua la scheda [!UICONTROL Triggers], quindi fai clic su **[!UICONTROL Gestione attivatori]**.
3. Fai clic su **[!UICONTROL Nuovo trigger]** e specifica il tipo di trigger:

   ![Risultato passaggio](../assets/add-trigger.png)

4. Configura il trigger completando i campi seguenti e trascinando metriche ed elementi dimensione nei contenitori della regola:

   | Elemento | Descrizione |
   |--- |--- |
   | [!UICONTROL Nome] | Nome intuitivo per il trigger. |
   | [!UICONTROL Descrizione] | La descrizione di questo attivatore, come utilizzarlo e così via. |
   | [!UICONTROL Suite di rapporti] | La [suite di rapporti](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=it) di Analytics utilizzata per questo trigger. Questa impostazione identifica i dati di reporting da utilizzare. |
   | La visita deve includere<br>La visita non deve includere<br>Trigger dopo nessuna azione<br>Includi metadati | Puoi definire i criteri o i comportamenti del visitatore desiderati e i comportamenti indesiderati. Ad esempio, le regole per un semplice attivatore di abbandono carrello potrebbero essere:<ul><li>La visita deve includere: [!UICONTROL Aggiunta a carrello] (metrica) ed [!UICONTROL Esiste]. (puoi definire ulteriormente la regola con una visualizzazione di prodotto specifica o con dimensioni come Tipi di browser).</li><li>La visita non deve includere: [!UICONTROL Pagamento].</li><li>Trigger dopo nessuna azione per: 10 minuti.</li><li>[!UICONTROL Includi metadati]: consente di aggiungere una dimensione [!DNL Campaign] particolare o variabili rilevanti per il comportamento di un visitatore. Questo campo può essere utile per Adobe Campaign per creare l&#39;e-mail di ricommercializzazione corretta.</li></ul><br>Puoi specificare un operatore logico [!UICONTROL Any], [!UICONTROL And] oppure [!UICONTROL Or] all’interno o tra contenitori, a seconda dei criteri che ritieni importanti per la regola. |
   | [!UICONTROL Contenitore] | [!UICONTROL Nei contenitori] vengono impostati e archiviati regole, condizioni o filtri che definiscono un trigger. Se vuoi far verificare gli eventi contemporaneamente, inseriscili nello stesso contenitore. Ciò significa che ogni contenitore elabora indipendentemente a livello di risultato. Ad esempio, in caso di due contenitori uniti dall&#39;operatore AND, le regole saranno idonee quando due risultati soddisfano i requisiti. |
   | Start new session after (Avvia nuova sessione dopo) | Crea un trigger per gli eventi di inizio e fine sessione. |

   {style="table-layout:auto"}

5. Fai clic su **[!UICONTROL Salva]**.
6. Usa i trigger per la [commercializzazione in tempo reale](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/about-adobe-experience-cloud-triggers.html?lang=it) in [!DNL Adobe Campaign].

### Esempio di trigger

Esempi di Experience Cloud Triggers:

#### Trigger di abbandono del carrello

Ad esempio, nella pagina seguente sono illustrate le regole che è possibile utilizzare per un attivatore di [!UICONTROL abbandono del carrello], in base ai prodotti visualizzati durante una visita.

![Trigger di abbandono del carrello](../assets/abandonment-trigger.png)

#### Trigger referrer

Il trigger seguente si attiva quando viene visualizzato un risultato con il prodotto Stivali da uomo e il referrer Facebook. Affinché i due criteri (*prodotti* e *referrer*) vengano valutati nello stesso hit, è necessario aggiungerli allo stesso contenitore.

![Trigger referrer](../assets/fb-boots-promo.png)
