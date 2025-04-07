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
source-git-commit: 7f852f0f3b4943cad28c2db2bb65f438a3f5a54a
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 4%

---


# IA nelle applicazioni Experience Cloud

Questa pagina ti aiuta a capire come le applicazioni Experience Cloud utilizzano l’intelligenza artificiale generativa e dove trovare informazioni specifiche per l’applicazione. Scopri le classi di domande, prompt e modelli di input e output.

## Informazioni sull’intelligenza artificiale generativa e sull’assistente di intelligenza artificiale

Generative AI è un tipo di intelligenza artificiale in grado di _creare_ nuovi contenuti e _rispondere_ alle tue affermazioni e domande (prompt):

* **Crea:** si riferisce alla capacità dell&#39;intelligenza artificiale di generare nuovi contenuti (testo, immagini, musica o video) da zero, in base ai prompt di apprendimento e input. Questa capacità è l&#39;aspetto _generative_ dell&#39;intelligenza artificiale generativa.

* **Risposta:** fa riferimento all&#39;intelligenza artificiale fornendo una risposta o una reazione a una domanda, un&#39;istruzione o un prompt specifico, in genere basandosi sulle sue capacità di conoscenza o di ragionamento.

Alcune applicazioni Experience Cloud sfruttano l’intelligenza artificiale generativa, consentendo ai nuovi utenti di acquisire rapidamente le conoscenze sui prodotti e agli utenti esperti di scoprire informazioni operative in pochi secondi anziché in poche ore.

### Assistente IA

[L&#39;Assistente AI](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) è uno strumento di conversazione supportato in Experience Platform e nelle applicazioni correlate. Utilizzala per accelerare i flussi di lavoro, migliorare la conoscenza dei prodotti, risolvere i problemi o eseguire ricerche tra le informazioni. L’Assistente AI consente di scoprire informazioni operative in pochi secondi, anziché in ore.

Tutte le risposte relative alla conoscenza del prodotto sono verificabili e citate con collegamenti alla documentazione del prodotto in Experience League. [Scopri l&#39;Assistente AI](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) e i tipi di prompt basati su obiettivi per ottenere il massimo dall&#39;Assistente AI.

## Applicazioni Experience Cloud che utilizzano IA

>[!TIP]
>
>Versione sottotitolo (solo un inizio)...


* [GenStudio for Performance Marketing](#gspm)
* [Experience Manager Sites (Cloud Service)](#aem-sites)
* Altri contenuti in arrivo...

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home) è una piattaforma generativa basata su IA. Infonde il ciclo di vita della creazione dei contenuti con funzionalità di intelligenza artificiale generative che trasformano il modo in cui i contenuti di marketing vengono creati, revisionati, condivisi e analizzati.

_GenStudio for Performance Marketing Create_ sfrutta la potenza di Adobe GenAI per consentire agli addetti al marketing e ai team distribuiti di creare esperienze on-brand ad alte prestazioni. Genera contenuto per:

* E-mail
* Meta annunci
* Annunci LinkedIn
* Visualizza annunci
* Banner

Puoi formare GenStudio for Performance Marketing sul tuo marchio utilizzando esempi, descrizioni di utenti tipo e prodotti, e linee guida per il marchio. [Ulteriori informazioni.](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Compatibilità con Adobe Firefly:** pianificata

### Experience Manager Sites {#aem-sites}

AEM Sites utilizza [Genera varianti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). Genera varianti utilizza l’intelligenza artificiale generativa per creare varianti di contenuto in base alle richieste. Questi prompt sono forniti da [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) oppure creati e gestiti da [utenti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt).

Dopo aver creato le varianti, puoi utilizzare il contenuto del sito web e misurarne il successo utilizzando la funzionalità Sperimentazione di Edge Delivery Services.

**Input:** I campi di input includono:

* Numero di varianti da generare
* Audience Source
* Destinazione pubblico
* Contesto aggiuntivo
* Richieste guidate dal cliente

**Output:** Contenuto generato/Copia di mercato. Puoi anche generare immagini in Adobe Express utilizzando le funzionalità di intelligenza artificiale generative di Firefly.

Vedi [Genera immagine](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image).

**Compatibilità con Adobe Firefly:** Sì



## Applicazioni Experience Cloud che utilizzano IA

>[!TIP]
>
>Versione tabella...


Scopri in che modo le applicazioni Experience Cloud utilizzano l’intelligenza artificiale generativa o l’Assistente all’intelligenza artificiale e se Adobe Firefly è supportato.

| Applicazione | Come viene utilizzata l’intelligenza artificiale generativa | Esempi | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/it/docs/genstudio-for-performance-marketing/user-guide/home) è una piattaforma generativa basata su IA. Infonde il ciclo di vita della creazione dei contenuti con funzionalità di intelligenza artificiale generative che trasformano il modo in cui i contenuti di marketing vengono creati, revisionati, condivisi e analizzati.<br>Puoi addestrare GenStudio for Performance Marketing per il tuo marchio utilizzando esempi, descrizioni di utenti tipo e prodotti, nonché linee guida per il marchio. | _GenStudio for Performance Marketing Create_ consente di generare contenuti per e-mail, annunci Meta, annunci LinkedIn, annunci di visualizzazione e banner. <br>**Input:** <ul><li>Utilizza i modelli per avviare il processo di creazione dei contenuti. </li><li>Aggiungi parametri come Marchi, Prodotti e Personas (linee guida) e Contenuto (risorse) per modellare l’esperienza generata. </li><li>Inserisci prompt descrittivi che descrivono il contesto o l’esperienza che intendi generare. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | Sì |
| Adobe Experience Manager Sites (Cloud Service) | AEM Sites utilizza [Genera varianti](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Genera varianti utilizza IA generativa per creare varianti di contenuto in base alle richieste. Questi prompt vengono forniti da Adobe o creati e gestiti dagli utenti. | Dopo aver creato le varianti, puoi utilizzare il contenuto del sito web e misurarne il successo utilizzando la funzionalità Sperimentazione di Edge Delivery Services. <br>**Input:** I campi di input includono il numero di varianti da generare, Audience Source/Audience Target, Contesto aggiuntivo e prompt guidati dal cliente. <ul><li>[Modello di richiesta Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[Prompt generato dall&#39;utente](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Contenuto generato/Copia di mercato. Puoi anche generare immagini in Adobe Express utilizzando le funzionalità di intelligenza artificiale generative di Firefly. Vedi [Genera immagine](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Sì |
| Adobe Journey Optimizer | Journey Optimizer utilizza [Assistente AI](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) con due classi di domande:<ul><li>**Conoscenza del prodotto** - Esegue query sugli archivi dati di Adobe (ad esempio la documentazione del prodotto di Experience League) per il prodotto insight. Questo output è indipendente dal cliente. </li><li>**Operational Insights (Beta)**: esegue una query in un archivio dati di approfondimenti operativi specifico per il cliente che contiene dati operativi centralizzati sui Percorsi, partizionati per la sandbox del cliente. Estrae metadati solo da oggetti business e non accede ai dati all’interno della sandbox.</li></ul> | <ul><li>**Input conoscenza del prodotto:** quante attività live posso avere in una sandbox Adobe Journey Optimizer?</li><li>**Output della conoscenza del prodotto:** La conoscenza del prodotto viene richiamata da Experience League (documentazione pubblica). </li><li>**Input approfondimenti operativi:** quanti Percorsi sono stati creati negli ultimi sette giorni? </li><li>**Output di Operational Insights:** l&#39;output di Operational Insights dipende dai metadati estratti dagli oggetti business del cliente. Percorsi è l’unico oggetto disponibile in AJO e i metadati vengono estratti dalla sandbox corrente. </li></ul> Consulta [Utilizzare l&#39;Assistente AI](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) e [Preparazione campi](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ e _Ultimate_ | [L&#39;Assistente di IA per l&#39;acceleratore dei contenuti](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) offre suggerimenti proattivi per varianti di contenuto per testo e immagini. È disponibile per i canali e-mail, push, web e SMS. Questa nuova funzionalità fornisce la generazione di testo e immagini basati su prompt. | <ul><li> **E-mail** - genera un&#39;e-mail completa, solo testo o solo immagine. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Notifica push** - Genera una notifica push completa, solo testo o solo immagine. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Genera un SMS completo o solo testo. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Pagina Web** - Genera immagini di pagine Web o testo di pagine Web. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Contenuto** - Genera contenuti per varie campagne di messaggistica. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Nota:** l&#39;output di Content Accelerator in AJO Prime e Ultimate è indennizzato. | Sì |
| Journey Optimizer B2B Edition | Utilizza [Assistente IA](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) con una classe di domande: <br> **Conoscenza del prodotto** - Esegue query sugli archivi dati di Adobe (ad esempio la documentazione del prodotto di Experience League) per il prodotto insight. Questo output è indipendente dal cliente. | <ul><li>**Input:** Come si invia un&#39;e-mail in un percorso di account?</li><li>**Output:** la conoscenza del prodotto viene richiamata da Experience League (documentazione pubblica). [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | No |
| Servizi cloud gestiti di Campaign | [L&#39;Assistente AI per l&#39;acceleratore dei contenuti](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) genera automaticamente contenuti personalizzati, coinvolgenti ed efficaci in base all&#39;obiettivo di marketing con contenuti ottimizzati per stili, layout, toni e altro del brand, tramite canali quali e-mail, SMS e push. | <ul><li> **E-mail** - Genera un messaggio e-mail completo, solo testo o solo immagine. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Genera solo SMS o testo completo. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Crea messaggi convincenti e genera contenuti. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Nota:** l&#39;output di Content Accelerator in Campaign Managed Cloud Services è indennizzato. | Sì |
| Customer Journey Analytics | CJA utilizza l&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) per aiutarti a scoprire le conoscenze e le informazioni sul prodotto da Experience League. <br>I nuovi utenti, ad esempio, possono utilizzarlo per apprendere i concetti di Customer Journey Analytics e per eseguire autonomamente l&#39;onboarding di prodotti e funzionalità che non conosci. <br>Gli utenti esperti possono utilizzare l&#39;Assistente all&#39;intelligenza artificiale per presentare casi d&#39;uso più avanzati o suggerimenti ed eseguire attività a ritmo veloce. Comprendere i concetti, risolvere i problemi o cercare informazioni. [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Input conoscenza del prodotto:** Come si crea una metrica calcolata? </li><li> **Output della conoscenza del prodotto:** La conoscenza del prodotto viene richiamata da Experience League (documentazione pubblica). </li></ul> | No |
| Customer Journey Analytics | [Didascalie intelligenti](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) fornisce informazioni in linguaggio naturale per le visualizzazioni delle linee nelle visualizzazioni di Workspace. | <ul><li>**Input:** visualizzazioni a linee. I sottotitoli vengono generati automaticamente in base a tali visualizzazioni di linee quando fai clic su **Sottotitoli intelligenti**. </li><li> **Output:** sottotitoli in linguaggio naturale generati automaticamente.</li></ul> | No |
| Real-Time CDP | Utilizza l&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) per aiutarti a scoprire le conoscenze e gli approfondimenti sul prodotto da Experience League. Interroga un database e traduce i dati da esso in una risposta leggibile. Due classi di domande: <br> **Conoscenza del prodotto** - Esegue query sugli archivi dati di Adobe (ad esempio la documentazione del prodotto di Experience League) per il prodotto insight. Questo output è indipendente dal cliente. <br> **Operational Insights (Beta)** - Esegue una query in un archivio dati di approfondimenti operativi specifico per il cliente che contiene dati operativi centralizzati, partizionati dalla sandbox AEP del cliente. Estrae metadati solo da Attributi, Tipi di pubblico, Flussi di dati, Set di dati, Destinazioni, Schemi e Origini e non accede ai dati all’interno della sandbox. <br>Ad esempio, per una query su un pubblico [!DNL AI Assistant] può accedere al nome del pubblico e ad altri metadati associati, ma non ai profili all&#39;interno di tale pubblico. | <ul><li>**Input conoscenza prodotto:** Come viene calcolata la ricchezza del profilo? </li><li>**Output della conoscenza del prodotto:** La conoscenza del prodotto viene richiamata da Experience League (documentazione pubblica). </li><li> **Input approfondimenti operativi:** quanti set di dati sono disponibili? </li><li> **Output di Operational Insights:** l&#39;output di Operational Insights dipende dai metadati estratti dagli oggetti business del cliente (Attributi, tipi di pubblico, flussi di dati, set di dati, destinazioni, schemi e origini) e include un collegamento a una pagina specifica dell&#39;interfaccia utente contenente i dati interrogati. </li></ul>Per esempi, consulta le tabelle di input _Conoscenza del prodotto_ e _Informazioni operative_ in [Assistente IA in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) | No |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) crea conversazioni basate sull&#39;intelligenza artificiale con domande e risposte personalizzate e preapprovate, nonché riepilogo delle conversazioni | <ul><li> **Genera domande:** Fornisci gli URL da cui il contenuto viene estratto e utilizzato per generare domande/risposte. </li><li> **Riepilogo conversazioni:** genera un riepilogo di una conversazione chat. </li></ul> [Ulteriori informazioni...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | No |
| Workfront | L&#39;[Assistente AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront ti aiuta a svolgere il tuo lavoro offrendo informazioni e suggerimenti in-app in una conversazione in lingua naturale. L’Assistente AI offre le seguenti funzionalità: riepiloga progetti/attività/problemi/documenti, fornisce istruzioni o informazioni di riferimento ricavate dalla documentazione di Workfront su Experience League, genera o perfeziona formule per i campi personalizzati calcolati. | <ul><li>**Riepiloga input progetto:** Riepiloga il progetto </li><li> **Riepiloga output progetto:** Restituisce brevi descrizioni dello scopo e dello stato del progetto, fornisce esempi di attività completate e ancora in sospeso e fornisce ulteriori dettagli e note.</li><li> **Generare/Perfezionare l&#39;input della formula:** &quot;Riscrivere la formula per rimuovere l&#39;errore di espressione non valida.&quot; </li><li> **Genera/Perfeziona output formula:** Formula generata o raffinata. </li></ul>**Nota:** la generazione della formula rivista da parte dell&#39;Assistente IA potrebbe richiedere alcuni minuti, a seconda delle dimensioni e della complessità della formula. | No |
