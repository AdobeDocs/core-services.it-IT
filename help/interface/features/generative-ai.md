---
title: IA nelle applicazioni Experience Cloud
description: Scopri in che modo le applicazioni Experience Cloud utilizzano IA generativa e l’Assistente AI.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: d54af09033b1a0727e9b7aa3dbf4a9be6003a8ea
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 3%

---

# IA nelle applicazioni Experience Cloud

Questa pagina ti aiuta a comprendere l’intelligenza artificiale generativa e come utilizzarla nelle applicazioni Experience Cloud. Scopri quali funzioni del prodotto utilizzano IA generativa, Assistente AI e se Adobe Firefly è supportato.

## Informazioni sull’intelligenza artificiale generativa e sull’assistente di intelligenza artificiale

L’intelligenza artificiale generativa è un tipo di intelligenza artificiale che non si limita a rispondere alle domande. _crea_ contenuto e _risponde_ alle _richieste_ (domande e istruzioni).

* **Crea:** si riferisce alla capacità dell&#39;intelligenza artificiale di generare nuovi contenuti (testo, immagini, musica o video) da zero, in base ai prompt di apprendimento e input. Questa capacità è l&#39;aspetto _generative_ dell&#39;intelligenza artificiale generativa.

* **Risposta:** fa riferimento all&#39;IA che fornisce una risposta o una reazione a un prompt specifico, in genere basandosi sulle sue capacità di conoscenza o ragionamento.

Se sei un nuovo utente di Experience Cloud, puoi utilizzare l’intelligenza artificiale generativa per acquisire rapidamente conoscenze sul prodotto. In qualità di utente esperto, puoi scoprire le informazioni operative in pochi secondi anziché in ore.

### Assistente IA

[L&#39;Assistente AI](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) è uno strumento di conversazione supportato in Experience Platform e nelle applicazioni correlate. Utilizzala per accelerare i flussi di lavoro, migliorare la conoscenza dei prodotti, risolvere i problemi o eseguire ricerche tra le informazioni. In alcune applicazioni, l’Assistente AI consente di scoprire immediatamente le informazioni operative.

Le risposte di Experience League relative alla conoscenza del prodotto sono verificabili e citate insieme ai collegamenti. Scopri i tipi di [prompt basati su obiettivi](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home) per ottenere il massimo dall&#39;Assistente IA.

## Applicazioni con funzioni che supportano l’intelligenza artificiale

* [GenStudio for Performance Marketing](#gspm)
* [Generare varianti in AEM Sites (Cloud Service)](#aem-sites)
* [Assistente IA in Journey Optimizer](#journey-optimizer)
* [ADOBE JOURNEY OPTIMIZER PRIME e ULTIMATE](#ajo-prime-ultimate)
* [Journey Optimizer B2B Edition](#ajo-b2b)
* [Assistente AI in Journey Optimizer Prime e Ultimate](#ajo-prime-ultimate)
* [Assistente AI in Journey Optimizer B2B edition](#ajo-b2b)
* [Assistente AI in Campaign Managed Cloud Services](#campaign-cs)
* [Assistente AI in Customer Journey Analytics](#cja)
* [Sottotitoli intelligenti in Customer Journey Analytics](#cja-captions)
* [Assistente AI in Real-Time CDP](#rtcdp)
* [Dynamic Chat in Marketo](#marketo)
* [Assistente AI in Workfront](#workfront)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home) non è una funzionalità ma una piattaforma generativa basata sull&#39;intelligenza artificiale. Le sue funzionalità di intelligenza artificiale generative trasformano il modo in cui i contenuti di marketing vengono creati, revisionati, condivisi e analizzati.

Nella home di [Create](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview) puoi creare esperienze on-brand dalle prestazioni elevate. Genera contenuto per:

* E-mail
* Meta annunci
* Annunci LinkedIn
* Visualizza annunci
* Banner

Puoi anche addestrare GenStudio for Performance Marketing al tuo marchio utilizzando esempi, descrizioni di utenti tipo e prodotti, e linee guida per il marchio. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Compatibile con Adobe Firefly:** Pianificato

### Generare varianti in Experience Manager Sites {#aem-sites}

[Genera varianti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) in AEM Sites utilizza l&#39;intelligenza artificiale generativa per creare varianti di contenuto in base alle richieste. Questi prompt sono forniti da [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) oppure creati e gestiti da [utenti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt).

Dopo aver creato le varianti, puoi utilizzare il contenuto del sito web e misurarne il successo utilizzando la funzione Sperimentazione di Edge Delivery Services.

### Campi di input e output

**Input:** I campi di input includono:

* Numero di varianti da generare
* Audience Source
* Destinazione pubblico
* Contesto aggiuntivo
* Richieste guidate dal cliente

**Output:** Contenuto generato/Copia di mercato. Puoi anche generare immagini in Adobe Express utilizzando le funzionalità di intelligenza artificiale generative di Firefly.

Per ulteriori informazioni, consulta [Genera immagine](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image).

**Compatibile con Adobe Firefly:** Sì

## Assistente IA in Journey Optimizer {#journey-optimizer}

In Journey Optimizer, l’Assistente AI può aiutarti a ottenere conoscenze sul prodotto e informazioni operative.

**Conoscenza del prodotto:** l&#39;Assistente all&#39;intelligenza artificiale interroga gli archivi dati di Adobe (ad esempio la documentazione del prodotto di Experience League) per insight. L’output è indipendente dal cliente.

Esempio:

* _Quante attività live posso avere in una sandbox Adobe Journey Optimizer?_

**Operational Insights (Beta)** - L&#39;Assistente AI esegue una query in un archivio dati di approfondimenti operativi specifici del cliente che contiene dati operativi centralizzati sui Percorsi, partizionati per la sandbox del cliente. Questa funzione richiama i metadati solo dagli oggetti business e non accede ai dati all’interno della sandbox.

Esempio di prompt:

* _Quanti Percorsi sono stati creati negli ultimi sette giorni?_

L&#39;output di Operational Insights dipende dai metadati estratti dagli oggetti aziendali del cliente. Questo output è indipendente dal cliente.

_Percorsi_ è l&#39;unico oggetto disponibile per l&#39;Assistente IA in Journey Optimizer e i metadati vengono estratti dalla sandbox corrente. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

**Compatibile con Adobe Firefly:** No

## Assistente AI in Journey Optimizer Prime e Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime e Ultimate utilizzano [AI Assistant per Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) per portare suggerimenti proattivi di varianti di contenuto per testo e immagini.

Questa funzionalità è disponibile per [e-mail](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email), [notifiche push](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push), [pagina Web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web), [contenuto](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation) e [SMS](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) canali. Fornisce la generazione di testo e immagini basati su prompt.

**Nota:** l&#39;output di Content Accelerator in AJO Prime e Ultimate è indennizzato.

**Compatibile con Adobe Firefly:** Sì

## Assistente AI in Journey Optimizer B2B edition {#ajo-b2b}

Journey Optimizer B2B edition utilizza [Assistente AI](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) per aiutarti con la conoscenza del prodotto, in base ai tuoi prompt di conoscenza del prodotto.

**Conoscenza del prodotto** - Esegue query sugli archivi dati di Adobe (ad esempio la documentazione del prodotto di Experience League) per il prodotto insight. Questo output è indipendente dal cliente.

* **Input:** Come si invia un&#39;e-mail in un percorso di account?

* **Output:** la conoscenza del prodotto viene richiamata da Experience League (documentazione pubblica). [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/question-guidance)

**Compatibile con Adobe Firefly:** No

## Assistente AI in Campaign Managed Cloud Services {#campaign-cs}

Campaign Managed Cloud Services utilizza l&#39;[Assistente IA per l&#39;acceleratore dei contenuti](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs). Questa funzione consente di generare automaticamente contenuti personalizzati, coinvolgenti ed efficaci in base agli obiettivi di marketing, con contenuti ottimizzati per stili, layout, toni e altro ancora. Puoi utilizzarlo tra canali come [email](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content), [SMS](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) e [push](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push).

**Nota:** l&#39;output di Content Accelerator in Campaign Managed Cloud Services è indennizzato.

**Compatibile con Adobe Firefly:** Sì

## Assistente AI in Customer Journey Analytics {#cja}

Customer Journey Analytics utilizza l&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) per aiutarti a scoprire le conoscenze e le informazioni sul prodotto da Experience League.

**Esempio di prompt:** Come si crea una metrica calcolata?

I nuovi utenti possono utilizzarlo per apprendere i concetti di Customer Journey Analytics e per integrare se stessi in prodotti e funzionalità che non conosci.

Gli utenti esperti possono utilizzare l’Assistente per l’intelligenza artificiale per presentare casi d’uso più avanzati o suggerimenti e trucchi ed eseguire attività a ritmo veloce. Comprendere i concetti, risolvere i problemi o cercare informazioni. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**Compatibile con Adobe Firefly:** No

## Sottotitoli intelligenti in Customer Journey Analytics {#cja-captions}

Le [didascalie intelligenti](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) in Customer Journey Analytics forniscono informazioni in linguaggio naturale per le visualizzazioni di Workspace utilizzate più di frequente.

**Compatibile con Adobe Firefly:** No

## Assistente AI in Real-Time CDP {#rtcdp}

Real-Time CDP utilizza l&#39;[Assistente AI](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home) per aiutarti a scoprire le conoscenze e le informazioni sul prodotto da Experience League. [Suggerimenti](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions) su come porre domande.

Offre inoltre informazioni operative (in versione beta). Ai Assistant esegue una query su un archivio dati di approfondimenti operativi specifici del cliente che contiene dati operativi centralizzati, partizionati per la sandbox AEP del cliente. Estrae metadati solo da Attributi, Tipi di pubblico, Flussi di dati, Set di dati, Destinazioni, Schemi e Origini e non accede ai dati all’interno della sandbox.

Ad esempio, per una query su un pubblico, [!DNL AI Assistant] può accedere al nome del pubblico e ad altri metadati associati, ma non può accedere ai profili all&#39;interno di tale pubblico.

Ad esempio:

* Input: _Quanti set di dati sono disponibili?_

* Risposta: _L&#39;output di Operational Insights dipende dai metadati estratti dagli oggetti business del cliente (attributi, tipi di pubblico, flussi di dati, set di dati, destinazioni, schemi e origini) e include un collegamento a una pagina dell&#39;interfaccia utente specifica contenente i dati interrogati._

Per altri esempi, vedi le tabelle di input _Conoscenza del prodotto_ e _Informazioni operative_ in [Assistente IA in Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home)

**Compatibile con Firefly:** No

## Dynamic Chat in Marketo {#marketo}

[Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) crea conversazioni basate sull&#39;intelligenza artificiale con domande e risposte personalizzate e preapprovate, nonché riepilogo delle conversazioni |<ul><li> **Genera domande:** Fornisci gli URL da cui il contenuto viene estratto e utilizzato per generare domande/risposte. </li><li> **Riepilogo conversazioni:** genera un riepilogo di una conversazione chat. </li></ul> [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |

## Assistente AI in Workfront {#workfront}

L&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront ti aiuta a svolgere il tuo lavoro offrendo informazioni e suggerimenti in-app in una conversazione in lingua naturale. L’Assistente AI offre le seguenti funzionalità: riepiloga progetti/attività/problemi/documenti, fornisce istruzioni o informazioni di riferimento ricavate dalla documentazione di Workfront su Experience League, genera o perfeziona formule per i campi personalizzati calcolati.  | <ul><li>**Riepiloga input progetto:** Riepiloga il progetto </li><li> **Riepiloga output progetto:** Restituisce brevi descrizioni dello scopo e dello stato del progetto, fornisce esempi di attività completate e ancora in sospeso e fornisce ulteriori dettagli e note.</li><li> **Generare/Perfezionare l&#39;input della formula:** &quot;Riscrivere la formula per rimuovere l&#39;errore di espressione non valida.&quot; </li><li> **Genera/Perfeziona output formula:** Formula generata o raffinata. </li></ul>**Nota:** la generazione della formula rivista da parte dell&#39;Assistente IA potrebbe richiedere alcuni minuti, a seconda delle dimensioni e della complessità della formula. | No  |


<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
