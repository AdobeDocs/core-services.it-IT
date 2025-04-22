---
title: IA nelle applicazioni Experience Cloud
description: Scopri in che modo le applicazioni Experience Cloud utilizzano IA generativa e l’Assistente AI.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 7060cc75e06a00dd06475958f94b03ceaf39ae62
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 4%

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

I campi di input includono:

* Numero di varianti da generare
* Audience Source
* Destinazione pubblico
* Contesto aggiuntivo
* Richieste guidate dal cliente

Il risultato è contenuto generato o copia di mercato.

Puoi anche generare immagini in Adobe Express utilizzando le funzionalità di intelligenza artificiale generative di Firefly. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)

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

Customer Journey Analytics utilizza l&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) per aiutarti a scoprire le conoscenze e le informazioni sul prodotto da Experience League.

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

* Risposta: l’output di Operational Insights dipende dai metadati estratti dagli oggetti business del cliente (Attributi, Tipi di pubblico, Flussi di dati, Set di dati, Destinazioni, Schemi e Origini) e include un collegamento a una pagina dell’interfaccia utente specifica contenente i dati oggetto di query.

Per altri esempi, vedi le tabelle di input _Conoscenza del prodotto_ e _Informazioni operative_ in [Assistente IA in Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/home)

**Compatibile con Firefly:** No

## Dynamic Chat in Marketo {#marketo}

Le funzionalità generative basate sull’intelligenza artificiale di Adobe Dynamic Chat consentono di ottimizzare la produttività per gli agenti di vendita, ottenere informazioni sulle intenzioni dei visitatori del sito web e rispondere alle domande dei visitatori in modo sicuro. Puoi pre-approvare le domande, le risposte e il riepilogo della conversazione. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

**Compatibile con Firefly:** No

## Assistente AI in Workfront {#workfront}

L’Assistente AI in Workfront ti aiuta a svolgere il tuo lavoro offrendo informazioni e suggerimenti in-app. Puoi eseguire le seguenti operazioni:

* Ottenere riepiloghi di alcuni oggetti, fornendo una visualizzazione di alto livello dell&#39;intento o dei dettagli dell&#39;oggetto.
* Fai domande e lascia che [!DNL AI Assistant] trovi le risposte su Experience League.
* Ottieni formule generate in base alle tue richieste. Puoi anche risolvere gli errori nelle espressioni personalizzate non valide nei campi calcolati.
* Individuare progetti, attività e problemi.

[Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

**Compatibile con Firefly:** No
