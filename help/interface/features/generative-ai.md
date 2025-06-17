---
title: IA generativa nelle applicazioni Experience Cloud
description: Scopri l'intelligenza artificiale generativa (GenAI) e come le applicazioni Experience Cloud utilizzano GenAI e [!UICONTROL l'Assistente AI].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Artificial Intelligence
role: Admin, User
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 00f614ae4df0a20989e242ce28b036d9eaf9a0f4
workflow-type: tm+mt
source-wordcount: '2006'
ht-degree: 5%

---

# IA generativa nei prodotti Experience Cloud

L’intelligenza artificiale generativa (genAI) in Experience Cloud consente di automatizzare le attività creative e cognitive e di migliorare la produttività. Questa pagina descrive dove le applicazioni Experience Cloud supportano genAI e AI Assistant e fornisce collegamenti per ulteriori informazioni su queste funzioni.

**Cos&#39;è genAI?**

L’intelligenza artificiale generativa è un tipo di intelligenza artificiale che può creare contenuti originali. Ad esempio, può creare testo, immagini, video, audio o codice software in risposta a una richiesta o a un prompt dell’utente.

* **Crea:** la possibilità di generare contenuti (testo, immagini, musica o video) da zero, in base ai relativi prompt di formazione e input. Questa capacità è l&#39;aspetto _generative_ dell&#39;intelligenza artificiale generativa.

* **Generare una risposta:** L&#39;IA fornisce una risposta o una reazione a un prompt, in genere utilizzando i dati e gli archivi delle conoscenze disponibili.

Questo tipo di IA è in contrasto con [IA agente](agentic-ai.md) (framework agente di Adobe), che fa riferimento a IA che opera in modo autonomo.

**Che cos&#39;è [!UICONTROL Assistente IA]?**

[!UICONTROL L&#39;Assistente AI] è uno strumento di conversazione supportato in Experience Platform e nelle applicazioni correlate. Utilizzala per acquisire rapidamente _conoscenze sul prodotto_ e _informazioni operative_ nei prodotti supportati.

* **Conoscenza del prodotto:** La conoscenza del prodotto si riferisce a concetti e argomenti basati sulla documentazione di Experience League. Scopri come creare [prompt basati su obiettivi](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home) efficaci per ottenere il massimo da [!UICONTROL Assistente IA]. Tutte le risposte di Experience League sono verificabili e citate con collegamenti.

* **Informazioni operative:** [Informazioni operative](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/questions#objects-questions) si riferiscono a risposte generate sui tuoi oggetti metadati (attributi, tipi di pubblico, flussi di dati, set di dati e così via). Con [!UICONTROL Assistente AI], puoi eseguire in secondi ciò che altrimenti potrebbe richiedere ore o giorni.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/landing" tooltip="Vai a Assistente AI"}

## Disponibilità di IA nei prodotti Experience Cloud

Di seguito è riportato un elenco delle applicazioni Experience Cloud che utilizzano GenAI, AI Assistant o AI agente. È indicata la compatibilità con Adobe Firefly.

| **Nome prodotto** | **IA generativa** | **Assistente IA** | **Compatibilità Firefly** |
|------------------|-------------------------|------------------|---------------------------|
| [Adobe GenStudio for Performance Marketing](#gspm) | Un’applicazione GenAI che consente ai team creativi e di marketing di creare contenuti personalizzati sul brand. | Non applicabile | Sì |
| [Adobe Experience Manager Sites](#aem) | Utilizzato in [Genera varianti](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor?lang=en) per creare varianti di contenuto in base all&#39;input. | Non applicabile | Sì |
| [Sites Optimizer](#aem) | Consente di analizzare e migliorare le prestazioni e l’efficacia delle esperienze web. | Non applicabile | No |
| [Adobe Experience Manager Assets](#aem) | Utilizzato in [Content Hub](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview?lang=en) e [Tag avanzati](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/manage/smart-tags?lang=en#ai-smart-tags) generati dall&#39;intelligenza artificiale. | Non applicabile | Sì |
| [Adobe Journey Optimizer](#journey-optimizer) | Non applicabile | Disponibile per approfondimenti operativi e di prodotto. | No |
| | | _AJO Prime_ e _Ultimate_ offrono [Generazione di contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative?lang=en) per portare suggerimenti di varianti di contenuti proattivi per testo e immagini. | Sì |
| [[!DNL Adobe Journey Optimizer] B2B edition](#ajo-b2b) | Non applicabile | Disponibile per fornire assistenza con la conoscenza del prodotto. | No |
| [[!DNL Campaign] Servizi cloud gestiti](#campaign-cs) | Non applicabile | Utilizza IA Assistant per Content Accelerator per generare automaticamente contenuti personalizzati, coinvolgenti ed efficaci in base agli obiettivi di marketing su canali diversi, come e-mail, SMS e push | Sì |
| [[!DNL Customer Journey Analytics]](#cja) | Utilizzato con:<ul><li> [Didascalie intelligenti](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions?lang=en): per approfondimenti sulle visualizzazioni di Workspace più utilizzate.</li><li>[Content Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/content-analytics/report/report?lang=en#template): per assegnare automaticamente i metadati delle risorse.</li></ul> | L’Assistente AI può aiutarti con:<ul><li>[Conoscenza del prodotto](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant?lang=en) (Experience League)</li><li>[Agente di supporto del prodotto](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/new-features/customer-support?lang=en) </li><li>[Data Insights Agent](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)</li></ul> | No |
| [[!DNL Real-Time CDP]](#rtcdp) | Non applicabile | Conoscenza del prodotto da Experience League. Offre inoltre informazioni operative (in versione beta). | No |
| [[!DNL Marketo]](#marketo) | Disponibile in [Dynamic Chat](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview?lang=en) e [webinar interattivi](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai?lang=en). | Non applicabile | No |
| [[!DNL Workfront]](#workfront) | Utilizzato con [informazioni e suggerimenti in-app](https://experienceleague.adobe.com/it/docs/workfront/using/basics/ai-assistant/ai-assistant-overview?lang=en). | Non applicabile | Sì |

## Esempi di utilizzo di GenAI in Experience Cloud {#products}

Nelle sezioni seguenti vengono fornite informazioni più dettagliate su come utilizzare genAI o AI Assistant in applicazioni specifiche. Vengono forniti collegamenti per saperne di più.

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] servizi cloud gestiti](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] è un&#39;applicazione di intelligenza artificiale generativa progettata per consentire ai team di marketing aziendali di creare, attivare e ottimizzare contenuti per campagne nel brand su canali diversi, come media a pagamento, e-mail e annunci di visualizzazione.

Gli addetti al marketing delle prestazioni possono utilizzare prompt in linguaggio naturale per generare risorse personalizzate e conformi al brand. GenStudio for Performance Marketing accelera l’esecuzione della campagna, scala la produzione dei contenuti senza compromettere l’integrità del marchio e fornisce analisi delle prestazioni per migliorare il ROI complessivo.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home" tooltip="Vai a GenStudio for Performance Marketing"}

## [!DNL Experience Manager] {#aem}

Le sezioni seguenti descrivono brevemente l’intelligenza artificiale generativa nelle applicazioni AEM.

### Experience Manager Sites

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

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor" tooltip="Vai a Genera varianti su Experience League"}

### Sites Optimizer {#sites-optimizer}

AEM Sites Optimizer utilizza l’intelligenza artificiale generativa per analizzare e migliorare le prestazioni e l’efficacia delle esperienze web. Queste informazioni sono raggruppate in aree di opportunità chiave: Coinvolgimento, Acquisizione del traffico, Posizione di sicurezza e Integrità del sito. Ogni categoria evidenzia modi specifici per migliorare il sito, aumentando l’interazione con i visitatori, migliorando la reperibilità, rafforzando la sicurezza o mantenendo la stabilità del sito.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-manager-sites-optimizer/content/opportunity-types/overview" tooltip="Vai a Sites Optimizer su Experience League"}

### Experience Manager Assets {#aem-assets}

In AEM Assets, puoi utilizzare l&#39;intelligenza artificiale generativa in **Content Hub** e **Tag avanzati generati dall&#39;intelligenza artificiale**.

**Content Hub**

[!UICONTROL Content Hub] è disponibile come parte di [!DNL Experience Manager Assets as a Cloud Service] per la democratizzazione dell&#39;accesso ai contenuti del brand per le organizzazioni e i loro partner commerciali. Si concentra sulla distribuzione delle risorse per l’attivazione su larga scala e la creazione di varianti di contenuti sul brand per una maggiore agilità di marketing.

In Content Hub, puoi creare contenuti con Adobe Express (se disponi di adesioni Adobe Express). Puoi modificare i contenuti esistenti con strumenti semplici, produrre varianti on-brand con modelli ed elementi brand e creare contenuti con le funzionalità GenAI più recenti da [!DNL Adobe Firefly].

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview" tooltip="Vai a Content Hub su Experience League"}

**Tag avanzati**

Invece di fare affidamento sull’input manuale, l’intelligenza artificiale può assegnare automaticamente tag descrittivi alle risorse digitali. Questi tag generati dall’intelligenza artificiale migliorano la qualità dei metadati, rendendo le risorse più facili da cercare, classificare e consigliare.

Ad esempio, se la risorsa è un’immagine, l’intelligenza artificiale può identificare oggetti, scene, emozioni o anche i loghi del brand. Può generare tag rilevanti come _tramonto_, _spiaggia_, _vacanza_ o _sorriso_.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags" tooltip="Scopri i tag avanzati"}

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

In [!DNL Journey Optimizer] (AJO) è possibile utilizzare [Assistente AI](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/get-started/ai-assistant) per acquisire _conoscenze sul prodotto_ e _informazioni operative_ (beta).

### Esempi di utilizzo dell’Assistente IA in AJO

Di seguito è riportato un esempio di input per la conoscenza del prodotto:

* _Quante attività live posso avere in una sandbox Journey Optimizer?_

  L’output viene generato da Experience League e da altri archivi dati di Adobe.

Di seguito è riportato un esempio di input per approfondimenti operativi:

* _Quanti Percorsi sono stati creati negli ultimi sette giorni?_

  Per l’output, l’Assistente AI esegue una query in un archivio dati specifico del cliente. L&#39;archivio dati contiene dati operativi centralizzati di circa [!UICONTROL Percorsi]. Questa funzione è indipendente dal cliente e richiama i metadati solo dagli oggetti business. Non accede ai dati all’interno della sandbox.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/get-started/ai-assistant" tooltip="Scopri l’Assistente IA in AJO"}

### Assistente AI per la generazione di contenuti (AJO Prime e Ultimate) {#ajo-prime}

In AJO _Prime_ e _Ultimate_, puoi utilizzare la [generazione di contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) per la generazione di contenuti per portare suggerimenti di varianti di contenuti proattivi per testo e immagini.

Questa funzione è disponibile per e-mail, notifiche push, pagine web, contenuti e canali SMS. Fornisce la generazione di testo e immagini basati su prompt. L’output della generazione di contenuti in AJO Prime e Ultimate è indennizzato.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative" tooltip="Scopri l’Assistente IA in AJO"}

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition utilizza l&#39;[!UICONTROL Assistente AI] per aiutarti con la conoscenza del prodotto.

Esempio di input:

* _Come si invia un&#39;e-mail in un percorso di account?_

  L’output della conoscenza del prodotto viene estratto da Experience League.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview" tooltip="Scopri l’Assistente IA in AJO"}

## [!DNL Campaign] servizi cloud gestiti {#campaign-cs}

Campaign Managed Cloud Services utilizza [!UICONTROL L&#39;Assistente AI] per la generazione di contenuti. Questa funzione consente di generare automaticamente contenuti personalizzati, coinvolgenti ed efficaci in base agli obiettivi di marketing, con contenuti ottimizzati per stili, layout, toni e altro ancora. Puoi utilizzarlo tra canali quali e-mail, SMS e push.

**Nota:** l&#39;output della generazione di contenuti in Campaign Managed Cloud Services è indennizzato.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/campaign-web/v8/content/ai-assistant/generative-gs" tooltip="Scopri l’Assistente IA in AJO"}

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics consente di utilizzare l’assistente AI o AI generativo nei seguenti modi:

* [Assistente AI](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) per informazioni sul prodotto.
* [Didascalie intelligenti](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) per fornire informazioni chiave per le visualizzazioni di Workspace più utilizzate nel linguaggio naturale.
* [Content Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/content-analytics/report/report#template) per assegnare automaticamente ogni metadati di risorsa.

**Assistente IA**

Scopri le nozioni di prodotto di Experience League. Se sei un nuovo utente, scopri rapidamente i concetti di Customer Journey Analytics e impara a utilizzare i prodotti e le funzionalità. Ad esempio:

* _Come si invia un&#39;e-mail in un percorso di account?_

Gli utenti esperti ottengono casi d’uso avanzati o apprendono strategie per eseguire attività a ritmo veloce. È possibile comprendere rapidamente i concetti, risolvere i problemi o cercare informazioni.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant" tooltip="Informazioni sull’Assistente all’intelligenza artificiale in CJA"}

**Didascalie intelligenti**

È possibile utilizzare _Didascalie intelligenti_ in [!DNL Customer Journey Analytics] per ottenere informazioni sul linguaggio naturale per le visualizzazioni di Workspace più utilizzate. I sottotitoli intelligenti sono ideali per gli analisti che hanno bisogno di narrazioni e contesto da condividere con altri utenti. Gli utenti aziendali possono utilizzarlo per scoprire rapidamente soluzioni di alto livello.

Ad esempio:

* **Input:** In CJA, esegui una visualizzazione supportata (inclusi grafico a linee, ad area, a barre, Flusso o Abbandono), quindi fai clic su **[!UICONTROL Didascalie intelligenti]**.

* **Output:** Visualizza didascalie generate automaticamente in linguaggio naturale che mostrano il contesto e le principali operazioni da eseguire. Puoi quindi eseguire azioni sui dati generati, ad esempio rivederli, copiarli e condividerli con la tua organizzazione. [Scopri come](https://video.tv.adobe.com/v/3443146/?quality=12&learn=on#_blank&captions=ita)

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions" tooltip="Scopri i sottotitoli intelligenti"}

**Content Analytics**

Content Analytics utilizza l’intelligenza artificiale e GenAI per assegnare automaticamente ogni metadati di risorse, come soggetti, scene, colori di primo piano e così via. Un attributo è un tag di metadati assegnato dall’intelligenza artificiale che descrive cosa c’è in una risorsa o in un’esperienza.

Ad esempio: il primo piano `color: red` è un attributo assegnato automaticamente. Le visualizzazioni consentono di identificare gli attributi delle risorse che contribuiscono maggiormente alla conversione.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/analytics-platform/using/content-analytics/report/report#template" tooltip="Informazioni su Content Analytics"}

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP utilizza [!UICONTROL Assistente AI] per aiutarti con la conoscenza del prodotto da Experience League. Offre inoltre informazioni operative (in versione beta). [!UICONTROL L&#39;Assistente AI] esegue una query in un archivio dati di approfondimenti operativi specifici del cliente che contiene dati operativi centralizzati, partizionati nella sandbox di AEP. Il sistema richiama i metadati solo da Attributi, Tipi di pubblico, Flussi di dati, Set di dati, Destinazioni, Schemi e Origini e non accede ai dati all’interno della sandbox.

Ad esempio, se esegui una query su un pubblico, [!UICONTROL Assistente IA] può accedere al nome del pubblico e agli altri metadati associati, ma non ai profili all&#39;interno di tale pubblico.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home" tooltip="Informazioni su Real-Time CDP"}

## [!DNL Marketo] {#marketo}

In Marketo, l’intelligenza artificiale generativa è disponibile nei webinar interattivi e in Dynamic Chat.

**Webinar interattivi**

Genera automaticamente capitoli e riepiloghi per i webinar registrati, rendendoli più accessibili e facili da consultare per il pubblico. Le caratteristiche includono:

* Generazione automatica dei capitoli
* Riepilogo testo generato da IA
* Contenuto modificabile - Modificare capitoli e riepiloghi generati
* Integrazione semplificata: è possibile aggiungere capitoli e riepiloghi alle pagine di destinazione copiando il codice HTML nell’editor di pagine web desiderato

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai" tooltip="Scopri i webinar interattivi"}

**Dynamic Chat**

Le funzionalità generative basate sull’intelligenza artificiale di Adobe Dynamic Chat consentono di ottimizzare la produttività per gli agenti di vendita, ottenere informazioni sulle intenzioni dei visitatori del sito web e rispondere alle domande dei visitatori in modo sicuro. Puoi pre-approvare le domande, le risposte e il riepilogo della conversazione. Dynamic Chat include sia una versione gratuita che una versione premium.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview" tooltip="Informazioni su Dynamic Chat"}

## [!DNL Workfront] {#workfront}

[!UICONTROL Assistente AI] in [!DNL Workfront] consente di eseguire il lavoro offrendo informazioni e suggerimenti in-app. Puoi eseguire le seguenti operazioni:

* Ottenere riepiloghi di alcuni oggetti, fornendo una visualizzazione di alto livello dell&#39;intento o dei dettagli dell&#39;oggetto.
* Poni le tue domande e lascia che [!UICONTROL L&#39;Assistente AI] trovi le risposte su Experience League.
* Ottieni formule generate in base alle tue richieste. Puoi anche risolvere gli errori nelle espressioni personalizzate non valide nei campi calcolati.
* Individuare progetti, attività e problemi.

[!BADGE Ulteriori informazioni]{type=Informative url="https://experienceleague.adobe.com/it/docs/workfront/using/basics/ai-assistant/ai-assistant-overview" tooltip="Informazioni sull’Assistente all’intelligenza artificiale in Workfront"}

## Risorse aggiuntive

* [Risorse di IA responsabili in Centro affidabilità](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**Dichiarazione di non responsabilità:** Le informazioni in questa pagina sono solo a scopo informativo generale. Anche se ci si adopera per garantire che le informazioni rimangano accurate e attuali, le funzioni software e di intelligenza artificiale generativa possono cambiare frequentemente. Di conseguenza, non garantiamo sempre la completezza, l’accuratezza o l’affidabilità delle informazioni. Verifica eventuali dettagli importanti prima di prendere decisioni basate su questo contenuto.

