---
title: IA per l’agente nelle applicazioni Experience Cloud
description: Scopri dove l’IA per l’agente è disponibile nelle applicazioni Experience Cloud.
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
hidefromtoc: true
index: false
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: da7a2a9e9aa8365288fa6e05afb6485e4c33ccb2
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 2%

---

# IA agente in Adobe Experience Cloud

Aggiornato: **29 gennaio 2026**

Gli agenti Adobe Experience Platform utilizzano Experience Platform [Agent Orchestrator](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home) per aggiungere funzionalità basate su agenti alle applicazioni Experience Cloud.

Questi agenti consentono di automatizzare le attività, fornire informazioni più rapidamente e semplificare i flussi di lavoro. Di conseguenza, i team possono lavorare in modo più efficiente e ottenere più valore da Experience Cloud.

L’accesso agli agenti di intelligenza artificiale in Experience Cloud è disponibile in:

* [Applicazioni Experience Cloud esistenti](#existing-apps)
* [Applicazioni AI-first Experience Cloud](#ai-first-apps)

Le sezioni seguenti descrivono come abilitare l’intelligenza artificiale agentica in Experience Cloud.

## Applicazioni Experience Cloud esistenti {#existing-apps}

Nelle applicazioni esistenti, è possibile utilizzare il linguaggio naturale per istruire gli agenti Adobe Experience Platform tramite l&#39;interfaccia conversazionale [Assistente AI](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home). L’Assistente AI è disponibile sia nella visualizzazione a schermo intero che nella barra a destra.

Gli agenti possono essere abilitati nelle app Experience Cloud esistenti per i clienti in una delle seguenti categorie:

* È stata acquistata una licenza Adobe Experience Platform Agents AI Credits
* Sono inclusi in una versione di prova con limite di utilizzo (sono forniti crediti IA limitati)
* È stata eseguita la transazione dello SKU promozionale di Agent Orchestrator (licenza di prova limitata nel tempo)

Quando si utilizzano gli agenti di IA per eseguire _processi agente_, si utilizzano crediti di IA. Scopri di più in [Processi agente e consumo di credito IA](/help/interface/features/ai-credit-consumption.md).

Gli agenti di IA seguono _l&#39;input, la supervisione_ e rispettano i controlli di accesso a livello di prodotto. Puoi eseguire processi o accedere solo ai dati che sei autorizzato a utilizzare nel prodotto Experience Cloud sottostante.

### Agenti di intelligenza artificiale nelle app Experience Cloud esistenti {#existing-apps-table}

Nella tabella seguente sono elencati gli agenti Experience Platform disponibili nelle applicazioni Experience Cloud esistenti.

| Nome agente | Funzionalità | Applicazioni supportate |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | Dai ai tuoi team la possibilità di creare, gestire e ottimizzare i tipi di pubblico utilizzando le indicazioni del linguaggio naturale per commercializzarli in modo più semplice, efficiente e rapido. | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> |
| **Agente di Content Advisor** | <ul><li>[Rilevamento dei contenuti](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/discovery/overview): velocizza l&#39;authoring e migliora l&#39;individuazione con richieste semplificate in linguaggio naturale per trovare e rendere immediatamente visibile il contenuto Experience Manager in immagini, video, documenti basati su testo, frammenti di contenuto e moduli.</li><li>[Ottimizzazione dei contenuti](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-optimization/overview): semplifica la creazione di varianti di contenuti visivi dalle risorse di origine utilizzando prompt in linguaggio naturale.</li><li>[Produzione esperienza](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview): automatizza le attività a grande sforzo e a volume elevato in CMS. Questo agente trasforma processi manuali e lunghi in flussi di lavoro rapidi e basati sull’intelligenza artificiale che mantengono ogni esperienza aggiornata e coerente, aiutando la tua azienda a raggiungere gli obiettivi.</li></ul> | <ul><li>Adobe Experience Manager (individuazione contenuti)</li></ul><ul><li>Adobe Experience Manager con Dynamic Media con OpenAPI (ottimizzazione dei contenuti)</li></ul><ul><li>Servizi cloud Adobe Experience Manager e Edge Delivery Services (Experience Production) </li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Risponde rapidamente alle domande sui dati. Crea visualizzazioni rilevanti in Analysis Workspace utilizzando i componenti della visualizzazione dati e utilizzando i dati effettivi. | <ul><li>Customer Journey Analytics (edizioni B2B e B2C)</li></ul> |
| **Agente esperienza marchio** | [Supporto della distribuzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/development/overview): consente agli sviluppatori di AEM CS e agli amministratori tecnici di risolvere i problemi relativi ai passaggi di compilazione nella pipeline di Cloud Manager analizzando la causa principale e suggerendo correzioni. | <ul><li>Assistente AI in AEM Cloud Service e Adobe Managed Services</li></ul> |
| **Agente per la governance dei marchi*** | [Brand Governance](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview): tutela dell&#39;integrità e della conformità del brand attraverso l&#39;applicazione di regole di sicurezza, normative e brand in Experience Manager. Questo agente applica la governance del brand per mantenere gli standard visivi e di messaggistica. Utilizza autorizzazioni granulari per gestire l’accesso e le modifiche ai contenuti e incorpora DRM per mantenere i vincoli di licenza e utilizzo. | <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | Consente ai team di creare, analizzare e ottimizzare rapidamente percorsi di clienti multi-touch su larga scala. | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> |
| [Agente di supporto del prodotto](https://experienceleague.adobe.com/it/docs/experience-platform/ai-assistant/new-features/customer-support) | Risolvi i problemi di supporto senza uscire dai flussi di lavoro, crea ticket di assistenza clienti e tieni traccia dell’avanzamento del caso tramite l’Assistente AI. | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li><li>Adobe Journey Optimizer B2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

Asterisco (*): questo agente è accessibile ai clienti nel programma Explorer. Il programma Explorer è un programma per soli inviti che fornisce accesso anticipato alle più recenti funzionalità di Adobe per agenti. Per ulteriori informazioni, contatta il rappresentante del tuo account.

## Applicazioni AI-first Experience Cloud {#ai-first-apps}

Le applicazioni AI-first sono progettate con Al generativo o agente al centro. Utilizzano generative o agentic Al per le attività chiave e le funzioni agentiche sono già incluse nella licenza dell&#39;applicazione Al-first. Di conseguenza, non richiedono la licenza Experience Platform Agent Orchestrator.

Nella tabella seguente sono elencati gli agenti Experience Platform disponibili come applicazioni Al-first. Sono abilitati concedendo in licenza le seguenti applicazioni Al-first:

| Nome agente | Funzionalità | Applicazioni supportate |
|---|----------|----------|
| [Agente di sperimentazione](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Automatizza, analizza e sintetizza le informazioni, in modo da identificare rapidamente esperimenti ad alto impatto e opportunità di crescita da un&#39;area di lavoro centralizzata, riducendo al contempo i processi manuali. | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [Agente di ottimizzazione LLM](https://experienceleague.adobe.com/it/docs/llm-optimizer/using/home) | Migliora la visibilità, l’accuratezza e l’influenza negli ambienti di ricerca basati sull’intelligenza artificiale, fornisci informazioni sulla presenza del brand nelle risposte generate dall’intelligenza artificiale, offre consigli sui contenuti prescrittivi e automatizza le correzioni di ottimizzazione. | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/it/docs/experience-manager-sites-optimizer/content/home) | Ottimizza l’impatto aziendale rilevando e implementando automaticamente i miglioramenti apportati al sito web. Utilizzando l’intelligenza artificiale generativa e più tecnologie di monitoraggio, puoi aumentare l’acquisizione del traffico del sito, il coinvolgimento e altro ancora | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/it/docs/brand-concierge/content/documentation/overview) | Incrementa la conversione e il coinvolgimento attraverso un’individuazione intelligente dei prodotti in base al contesto, personalizzata in base alle preferenze e ai comportamenti individuali. | <ul><li>Adobe Brand Concierge</li></ul> |

## Ulteriori informazioni su questo argomento

* [IA nella pagina principale della documentazione di Experience Cloud](https://experienceleague.adobe.com/it/docs/ai)
* [Panoramica degli agenti in AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Ulteriori informazioni su Adobe for Business]{type=Informative url="https://business.adobe.com/it/products/experience-platform/agent-orchestrator.html" tooltip="Vai a Business.adobe.com"}
