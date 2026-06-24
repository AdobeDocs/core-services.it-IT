---
description: Scopri come configurare CX Enterprise Triggers.
solution: Experience Cloud
title: Panoramica di Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 9dc26e2f-479b-49a5-93ce-b877559fea43
TQID: https://experienceleague.adobe.com/1R70ZEmKiP9VhhSRVCXHjGoJbOb7Mh8spKRm4FgNRPc
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e56a5463246fe74bd7393de446687b6464760db1
workflow-type: tm+mt
source-wordcount: 817
ht-degree: 61%

---

# Trigger di CX Enterprise

[!UICONTROL Triggers] in CX Enterprise consente di identificare, definire e monitorare i comportamenti chiave dei consumatori, per poi generare comunicazioni tra le diverse applicazioni per coinvolgere nuovamente i visitatori. Puoi utilizzare i trigger nelle decisioni in tempo reale e nella personalizzazione. Per ulteriori informazioni sull&#39;utilizzo di [!UICONTROL Triggers] con Adobe Campaign, vedere [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html).

Ad esempio:

* Configura il remarketing rapido di carrelli abbandonati o di carrelli abbandonati con i prodotti rimossi
* Applicazioni e moduli incompleti
* Qualsiasi azione o sequenza di azioni sul sito

![Esempio di trigger](../assets/trigger-abandonment-2.png)

>[!NOTE]
>
>Gli attivatori non sono di natura deterministica. Quando più utenti condividono un browser o un dispositivo, ad esempio un dispositivo condiviso o pubblico, potrebbe non essere possibile mappare un trigger sull’ID visitatore corretto.

## Tipi di trigger

In genere, un trigger può richiedere dai 15 ai 90 minuti per avviare una campagna di marketing. Questo varia a seconda dell’implementazione della raccolta di dati, del caricamento sulla pipeline, della configurazione personalizzata del trigger definito e del flusso di lavoro in Adobe Campaign.

* **Abbandono:** puoi creare un trigger che si attiva quando un visitatore visualizza un prodotto ma non aggiunge nulla al carrello.
* **Azione:** puoi creare trigger, ad esempio, che si attivano dopo che un utente ha effettuato un&#39;iscrizione a una newsletter, un&#39;iscrizione e-mail o ha usato applicazioni per le carte di credito (conferme). Se sei un rivenditore, puoi creare un trigger per un visitatore che si iscrive a un programma fedeltà. Nei contenuti multimediali e di intrattenimento, crea trigger per i visitatori che guardano un determinato show e che vorresti rispondessero a un sondaggio.
* **Avvio e fine sessione:** crea un trigger per gli eventi di inizio e fine sessione.

## Creare un trigger CX Enterprise

Crea un trigger e configurane le condizioni. Ad esempio, puoi specificare i criteri per le regole di un attivatore durante una visita, come metriche quali abbandono del carrello o dimensioni quali il nome del prodotto. Quando le regole sono soddisfatte, il trigger viene eseguito.

>[!NOTE]
>
>Esiste attualmente un limite tecnico di 100 trigger.

1. In CX Enterprise, fai clic sul ![menu](../assets/menu-icon.png), quindi fai clic su **[!UICONTROL Raccolta dati/Launch]**.
1. Nella scheda [!UICONTROL Triggers], fai clic su **[!UICONTROL Gestisci trigger]**.
1. Fai clic su **[!UICONTROL Nuovo trigger]**, quindi specifica il tipo di trigger:

   ![Risultato passaggio](../assets/add-trigger.png)

1. Configura il trigger completando i campi seguenti e trascinando metriche ed elementi dimensione nei contenitori della regola:

   | Elemento | Descrizione |
   | --- | --- |
   | [!UICONTROL Nome] | Nome intuitivo per il trigger. |
   | [!UICONTROL Descrizione] | La descrizione di questo attivatore, come utilizzarlo e così via. |
   | [!UICONTROL Suite di rapporti] | La [suite di rapporti](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=it) di Analytics utilizzata per questo trigger. Questa impostazione identifica i dati di reporting da utilizzare. |
   | La visita deve includere<br>La visita non deve includere<br>Trigger dopo nessuna azione<br>Includi metadati | Puoi definire i criteri o i comportamenti del visitatore desiderati e i comportamenti indesiderati. Ad esempio, le regole per un semplice attivatore di abbandono carrello potrebbero essere:<ul><li>La visita deve includere: [!UICONTROL Aggiunta carrello] (metrica) e [!UICONTROL Esiste]. (puoi definire ulteriormente la regola con una visualizzazione di prodotto specifica o con dimensioni come Tipi di browser).</li><li>La visita non deve includere: [!UICONTROL Estrazione].</li><li>Trigger dopo nessuna azione per: 10 minuti.</li><li>[!UICONTROL Includi dati Meta]: consente di aggiungere una dimensione [!DNL Campaign] particolare o variabili rilevanti per il comportamento di un visitatore. Questo campo può essere utile per Adobe Campaign per creare l&#39;e-mail di ricommercializzazione corretta.</li></ul><br>È possibile specificare la logica [!UICONTROL Any], [!UICONTROL And] o [!UICONTROL Or] all&#39;interno o tra contenitori, a seconda dei criteri che ritieni importanti per la regola. |
   | [!UICONTROL Contenitore] | [!UICONTROL Nei contenitori] vengono impostati e archiviati regole, condizioni o filtri che definiscono un trigger. Se vuoi far verificare gli eventi contemporaneamente, inseriscili nello stesso contenitore. Ciò significa che ogni contenitore elabora indipendentemente a livello di risultato. Ad esempio, in caso di due contenitori uniti dall&#39;operatore AND, le regole saranno idonee quando due risultati soddisfano i requisiti. |
   | Start new session after (Avvia nuova sessione dopo) | Crea un trigger per gli eventi di inizio e fine sessione. |

   {style="table-layout:auto"}

1. Fai clic su **[!UICONTROL Salva]**.
1. Usa i trigger per la [commercializzazione in tempo reale](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/about-adobe-experience-cloud-triggers.html?lang=it) in [!DNL Adobe Campaign].

## Esempio di trigger

Esempi di CX Enterprise Triggers:

### Trigger di abbandono del carrello

Ad esempio, nella pagina seguente sono illustrate le regole che è possibile utilizzare per un trigger [!UICONTROL Abbandono carrello], in base ai prodotti visualizzati durante una visita.

![Trigger di abbandono del carrello](../assets/abandonment-trigger.png)

### Trigger referrer

Il trigger seguente si attiva quando viene visualizzato un risultato con il prodotto Stivali da uomo e il referrer Facebook. Affinché i due criteri (*prodotti* e *referrer*) vengano valutati nello stesso hit, è necessario aggiungerli allo stesso contenitore.

![Trigger referrer](../assets/fb-boots-promo.png)

## Verifica dell&#39;attività del trigger

Per verificare che un trigger sia stato attivato, utilizzare l&#39;interfaccia [!UICONTROL Triggers] per esaminare le attività recenti relative al trigger. L’interfaccia visualizza un numero limitato di eventi di trigger recenti, pertanto per le implementazioni con volumi di dati elevati potrebbe non mostrare tutta l’attività di trigger. La verifica programmatica tramite un’API non è attualmente supportata.
