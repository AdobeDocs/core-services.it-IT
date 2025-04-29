---
title: IA nelle applicazioni Experience Cloud
description: Scopri l’intelligenza artificiale generativa e come le applicazioni Experience Cloud utilizzano genAI e  [!DNL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: d84fcf64b7019f0146340a423e8e20a932cd7874
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 3%

---

# IA nei prodotti Experience Cloud

Questa pagina ti aiuta a scoprire quali prodotti supportano l&#39;intelligenza artificiale generativa, [!DNL AI Assistant], e se Adobe Firefly è compatibile. Puoi anche trovare collegamenti a risorse di aiuto specifiche per il prodotto su come utilizzare l’intelligenza artificiale in Experience Cloud.

**Informazioni su IA generativa**

L’intelligenza artificiale generativa è un tipo di intelligenza artificiale che non si limita a rispondere alle domande. Può _creare_ contenuto e _generare una risposta_ alle tue domande o istruzioni (noti come _prompt_).

* **Crea:** la possibilità di generare contenuti (testo, immagini, musica o video) da zero, in base ai relativi prompt di formazione e input. Questa capacità è l&#39;aspetto _generative_ dell&#39;intelligenza artificiale generativa.

* **Generare una risposta:** L&#39;IA fornisce una risposta o una reazione a un prompt, in genere utilizzando i dati e gli archivi delle conoscenze disponibili.

**Che cosa è[!DNL AI Assistant]?**

[!DNL AI Assistant] è uno strumento di conversazione supportato in Experience Platform e nelle applicazioni correlate. Utilizzala per acquisire rapidamente _conoscenze sul prodotto_ e, nelle applicazioni supportate, ottenere _informazioni operative_ quasi immediatamente.

* **Conoscenza del prodotto:** La conoscenza del prodotto si riferisce a concetti e argomenti basati sulla documentazione di Experience League. Le risposte di Experience League sono verificabili e citate con collegamenti. Scopri i tipi di [prompt basati su obiettivi](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home) per ottenere il massimo da [!DNL AI Assistant].

* **Informazioni operative:** Le informazioni operative fanno riferimento alle risposte che l&#39;Assistente AI genera sugli oggetti metadati (attributi, tipi di pubblico, flussi di dati, set di dati, destinazioni, percorsi, schemi e origini), inclusi i conteggi, le ricerche e l&#39;impatto sulla derivazione. Utilizzando AI Assistant, puoi scoprire le informazioni operative in pochi secondi anziché in ore.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company.
 -->

## Disponibilità di IA nei prodotti Experience Cloud

Scopri il supporto per l’intelligenza artificiale generativa o [!DNL AI Assistant] nei prodotti Experience Cloud. È inoltre indicato il supporto per Adobe Firefly.

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] servizi cloud gestiti](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## Adobe GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] è una piattaforma basata sull&#39;intelligenza artificiale che ti consente di generare e gestire contenuti di marketing conformi agli standard del tuo marchio e conformi alle politiche aziendali. Genera contenuti per e-mail, annunci Meta, annunci LinkedIn, annunci di visualizzazione e banner.

Puoi anche addestrare GenStudio for Performance Marketing al tuo marchio utilizzando esempi, descrizioni di utenti tipo e prodotti, e linee guida per il marchio.

[Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home)

Compatibilità con Adobe Firefly: **Sì**

## Adobe [!DNL Experience Manager Sites] {#aem-sites}

In AEM Sites puoi utilizzare _[!UICONTROL Genera varianti]_. Questa funzione utilizza l’intelligenza artificiale generativa per creare varianti di contenuto in base alle richieste di input. I prompt vengono forniti da Adobe o creati e gestiti dall’utente.

Dopo aver creato le varianti, puoi utilizzare il contenuto del tuo sito web e misurarne il successo utilizzando la funzione [Sperimentazione](https://www.aem.live/docs/experimentation) in Edge Delivery Services. Puoi anche generare immagini in Adobe Express utilizzando le funzionalità di intelligenza artificiale generative di Firefly.

**Esempi di input e output**

I campi di input includono:

* Numero di varianti da generare
* Audience Source
* Destinazione pubblico
* Contesto aggiuntivo
* Richieste guidate dal cliente

Il risultato è contenuto generato o copia di mercato.

[Ulteriori informazioni su Genera varianti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

Compatibilità con Adobe Firefly: **Sì**

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

In [!DNL Journey Optimizer] (AJO) è possibile utilizzare [Assistente AI](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) per acquisire _conoscenze sul prodotto_ e _informazioni operative_ (beta).

### Esempi di utilizzo dell’Assistente IA in AJO

Di seguito è riportato un esempio di input per la conoscenza del prodotto:

* _Quante attività live posso avere in una sandbox Journey Optimizer?_

  L’output viene generato da Experience League e da altri archivi dati di Adobe.

Di seguito è riportato un esempio di input per approfondimenti operativi:

* _Quanti Percorsi sono stati creati negli ultimi sette giorni?_

  Per l’output, l’Assistente AI esegue una query in un archivio dati specifico del cliente. L&#39;archivio dati contiene dati operativi centralizzati di circa [!UICONTROL Percorsi]. Questa funzione è indipendente dal cliente e richiama i metadati solo dagli oggetti business. Non accede ai dati all’interno della sandbox.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

Compatibilità con Adobe Firefly: **No**

### Assistente AI per la generazione di contenuti (AJO Prime e Ultimate) {#ajo-prime}

In AJO _Prime_ e _Ultimate_, puoi utilizzare la [generazione di contenuti](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) per la generazione di contenuti per portare suggerimenti di varianti di contenuti proattivi per testo e immagini.

Questa funzione è disponibile per e-mail, notifiche push, pagine web, contenuti e canali SMS. Fornisce la generazione di testo e immagini basati su prompt. L’output della generazione di contenuti in AJO Prime e Ultimate è indennizzato.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Compatibilità con Adobe Firefly: **Sì**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition utilizza [!DNL AI Assistant] per aiutarti con la conoscenza del prodotto.

Esempio di input:

* _Come si invia un&#39;e-mail in un percorso di account?_

  L’output della conoscenza del prodotto viene estratto da Experience League.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Compatibilità con Adobe Firefly: **No**

## [!DNL Campaign] servizi cloud gestiti {#campaign-cs}

Campaign Managed Cloud Services utilizza [!DNL AI Assistant] per la generazione di contenuti. Questa funzione consente di generare automaticamente contenuti personalizzati, coinvolgenti ed efficaci in base agli obiettivi di marketing, con contenuti ottimizzati per stili, layout, toni e altro ancora. Puoi utilizzarlo tra canali quali e-mail, SMS e push.

**Nota:** l&#39;output della generazione di contenuti in Campaign Managed Cloud Services è indennizzato.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Compatibilità con Adobe Firefly: **Sì**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics utilizza [!DNL AI Assistant] per aiutarti a scoprire le conoscenze e le informazioni sul prodotto da Experience League.

Se sei un nuovo utente, scopri rapidamente i concetti di Customer Journey Analytics e impara a utilizzare i prodotti e le funzionalità. Ad esempio:

* _Come si invia un&#39;e-mail in un percorso di account?_

Gli utenti esperti ottengono casi d’uso avanzati o apprendono strategie per eseguire attività a ritmo veloce. È possibile comprendere rapidamente i concetti, risolvere i problemi o cercare informazioni.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Compatibilità con Adobe Firefly: **No**

## [!DNL Customer Journey Analytics] {#cja-captions}

È possibile utilizzare _Didascalie intelligenti_ in [!DNL Customer Journey Analytics] per ottenere informazioni sul linguaggio naturale per le visualizzazioni di Workspace più utilizzate. I sottotitoli intelligenti sono ideali per gli analisti che hanno bisogno di narrazioni e contesto da condividere con altri utenti. Gli utenti aziendali possono utilizzarlo per scoprire rapidamente soluzioni di alto livello.

Ad esempio:

* **Input:** In CJA, esegui una visualizzazione supportata (inclusi grafico a linee, ad area, a barre, Flusso o Abbandono), quindi fai clic su **[!UICONTROL Didascalie intelligenti]**.

* **Output:** Visualizza didascalie generate automaticamente in linguaggio naturale che mostrano il contesto e le principali operazioni da eseguire. Puoi quindi eseguire azioni sui dati generati, ad esempio rivederli, copiarli e condividerli con la tua organizzazione. [Scopri come](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Compatibilità con Adobe Firefly: **No**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP utilizza [!DNL AI Assistant] per aiutarti con la conoscenza del prodotto da Experience League. Offre inoltre informazioni operative (in versione beta). [!DNL AI Assistant] esegue una query su un archivio dati di approfondimenti operativi specifico per il cliente che contiene dati operativi centralizzati, partizionati nella sandbox di AEP. Il sistema richiama i metadati solo da Attributi, Tipi di pubblico, Flussi di dati, Set di dati, Destinazioni, Schemi e Origini e non accede ai dati all’interno della sandbox.

Ad esempio, se si esegue una query su un pubblico, [!DNL AI Assistant] può accedere al nome del pubblico e ad altri metadati associati, ma non ai profili all&#39;interno di tale pubblico.

[Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home)

Compatibilità con Adobe Firefly: **No**

## [!DNL Marketo] {#marketo}

Le funzionalità generative basate sull’intelligenza artificiale di Adobe Dynamic Chat consentono di ottimizzare la produttività per gli agenti di vendita, ottenere informazioni sulle intenzioni dei visitatori del sito web e rispondere alle domande dei visitatori in modo sicuro. Puoi pre-approvare le domande, le risposte e il riepilogo della conversazione.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Compatibilità con Adobe Firefly: **No**

## [!DNL Workfront] {#workfront}

[!DNL AI Assistant] in [!DNL Workfront] ti aiuta a svolgere il tuo lavoro offrendo informazioni e suggerimenti in-app. Puoi eseguire le seguenti operazioni:

* Ottenere riepiloghi di alcuni oggetti, fornendo una visualizzazione di alto livello dell&#39;intento o dei dettagli dell&#39;oggetto.
* Fai domande e lascia che [!DNL AI Assistant] trovi le risposte su Experience League.
* Ottieni formule generate in base alle tue richieste. Puoi anche risolvere gli errori nelle espressioni personalizzate non valide nei campi calcolati.
* Individuare progetti, attività e problemi.

[Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Compatibilità con Adobe Firefly: **No**
