---
title: IA per l’agente nelle applicazioni Experience Cloud
description: Scopri dove è disponibile l’IA per l’agente nelle applicazioni aziendali CX.
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
source-git-commit: 5b2b81c029b81b9f0689a012cb2a9ca8714c0b40
workflow-type: tm+mt
source-wordcount: 1130
ht-degree: 10%

---

# IA agente in Adobe CX Enterprise

Gli agenti Adobe Experience Platform sono basati su [Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home) per abilitare le funzionalità di IA per l&#39;agente nelle applicazioni aziendali CX.

Questi agenti consentono di automatizzare le attività, fornire informazioni più rapidamente e semplificare i flussi di lavoro. Di conseguenza, i team possono lavorare in modo più efficiente e ottenere più valore da CX Enterprise.

L&#39;accesso agli agenti di IA in CX Enterprise è disponibile in:

* [Applicazioni aziendali CX esistenti](#existing-apps)
* [Applicazioni AI-first CX Enterprise](#ai-first-apps)

Le sezioni seguenti descrivono questi due modi per abilitare l&#39;intelligenza artificiale agente in CX Enterprise.

## Applicazioni aziendali CX esistenti {#existing-apps}

Nelle applicazioni esistenti, è possibile utilizzare il linguaggio naturale per istruire gli agenti Adobe Experience Platform tramite l&#39;interfaccia conversazionale [Assistente AI](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home). L’Assistente AI è disponibile sia nella visualizzazione a schermo intero che nella barra a destra.

Gli agenti possono essere abilitati nelle app CX Enterprise esistenti per i clienti in una delle seguenti categorie:

* Hai acquistato una licenza di Adobe Experience Platform Agents AI Credits
* Sei incluso in una versione di prova vincolata all’utilizzo (sono forniti crediti IA limitati)
* Hai effettuato una transazione con Agent Orchestrator Promo SKU (licenza di prova limitata nel tempo)

L&#39;utilizzo di agenti di IA per l&#39;esecuzione di _processi agente_ comporta l&#39;utilizzo di crediti di IA. Ulteriori informazioni sui processi agente e sui crediti IA in _[Processi agente e consumo credito IA](/help/interface/features/ai-credit-consumption.md)_.

Gli agenti di IA seguono _l&#39;input, la supervisione_ e rispettano i controlli di accesso a livello di prodotto. È possibile eseguire solo job o accedere a dati che sono autorizzati a utilizzare nell&#39;applicazione CX Enterprise sottostante.

### Agenti di intelligenza artificiale nelle app CX Enterprise esistenti {#existing-apps-table}

Nella tabella seguente sono elencati gli agenti Experience Platform disponibili nelle applicazioni CX Enterprise esistenti.

| Nome agente | Funzionalità | Applicazioni supportate | Dati sanitari/pronti per HIPAA |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | Dai ai tuoi team la possibilità di gestire e ottimizzare i tipi di pubblico utilizzando le indicazioni del linguaggio naturale per commercializzarli in modo più semplice, efficiente e rapido. | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | |
| [Agente di Content Advisor](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>Consente ai team di trovare rapidamente i contenuti più rilevanti all&#39;interno dell&#39;azienda utilizzando il linguaggio naturale, riducendo il tempo impiegato per le ricerche e velocizzando le decisioni e l&#39;esecuzione.</li><li>Semplifica la creazione di varianti di contenuti visivi dalle risorse sorgente utilizzando prompt in linguaggio naturale.</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media (Cloud Services)</li></ul> | |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Risponde rapidamente alle domande sui dati. Crea visualizzazioni pertinenti in Analysis Workspace utilizzando i componenti della visualizzazione dati e i tuoi dati effettivi. | <ul><li>Customer Journey Analytics (edizioni B2B e B2C)</li></ul> | Sì |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>Accelera la migrazione e la modernizzazione delle esperienze digitali attraverso la ristrutturazione, l’arricchimento e la convalida automatici dei siti esistenti, in modo che i team possano passare più rapidamente a esperienze moderne e pronte per l’intelligenza artificiale, con meno rischi e sforzi manuali.</li><li>Consente di creare e aggiornare grandi volumi di esperienze, riducendo notevolmente l&#39;impegno manuale e il tempo di ciclo, in modo che i team possano spostarsi più rapidamente senza sacrificare qualità o coerenza.</li><li>Accelera la creazione di moduli ottimizzati per il marchio generando, strutturando e convalidando automaticamente le esperienze dei moduli, consentendo ai team di avviarsi più rapidamente e di acquisire dati di qualità superiore con il minimo sforzo manuale.</li><li>Aiuta gli sviluppatori e gli amministratori tecnici di AEM CS a risolvere i problemi di errore delle fasi di build nella pipeline di Cloud Manager analizzando la causa principale e suggerendo correzioni.</li></ul> | <ul><li>Servizi cloud Adobe Experience Manager Sites (modernizzazione delle esperienze)</li></ul><ul><li>Adobe Experience Manager Sites (Experience Production)</li></ul><ul><li>Adobe Experience Manager Forms (Creazione modulo)</li></ul><ul><li>Tutte le applicazioni Adobe Experience Manager basate su cloud (supporto allo sviluppo)</li></ul> | |
| [Agente per la governance dei marchi](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | Garantire l&#39;integrità del brand e la conformità con le regole del brand automatizzate, controlli, autorizzazioni e informazioni per supportare DRM con la governance in tempo reale. | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites (politica del marchio)</li></ul> | |
| [Journey Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent) | Consente ai team di analizzare e ottimizzare rapidamente e su larga scala i percorsi di clienti multi-touch. | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | |
| [Agente di supporto del prodotto](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/product-support) | Risolvi i problemi di supporto senza uscire dai flussi di lavoro, crea ticket di assistenza clienti e tieni traccia dell’avanzamento del caso tramite l’Assistente AI. | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li><li>Customer Journey Analytics (edizioni B2B e B2C)</li><li>Adobe Experience Manager</li></ul> | |
| [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms) | Collega Experience Platform direttamente al Copilot Microsoft 365. È possibile porre domande in linguaggio naturale nelle applicazioni Microsoft 365, ad esempio Team, Word, Powerpoint ed Excel, per recuperare immediatamente informazioni di marketing da Experience Platform senza interrompere il flusso di lavoro. | <ul><li> Adobe Agent Orchestrator con supporto per Audience Agent, Journey Agent, Customer Journey Analytics Data Insights, Experience Platform Operational Insights</li></ul> | |

## Applicazioni AI-first CX Enterprise {#ai-first-apps}

Le applicazioni AI-first sono progettate con Al generativo o agente al centro. Utilizzano generative o agentic Al per le attività chiave e le funzioni agentiche sono già incluse nella licenza dell&#39;applicazione Al-first. Di conseguenza, non richiedono la licenza Experience Platform Agent Orchestrator.

Nella tabella seguente sono elencati gli agenti Experience Platform disponibili come applicazioni Al-first. Sono abilitati concedendo in licenza le seguenti applicazioni Al-first:

| Nome agente | Funzionalità | Applicazioni supportate |
|---|----------|----------|
| [Agente di sperimentazione](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Automatizza, analizza e sintetizza le informazioni, in modo da identificare rapidamente esperimenti ad alto impatto e opportunità di crescita da un&#39;area di lavoro centralizzata, riducendo al contempo i processi manuali. | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [Agente di ottimizzazione LLM](https://experienceleague.adobe.com/it/docs/llm-optimizer/using/home) | Migliora la visibilità, l’accuratezza e l’influenza negli ambienti di ricerca basati sull’intelligenza artificiale, fornisci informazioni approfondite sulla presenza dei brand nelle risposte generate dall’intelligenza artificiale, offre consigli sui contenuti prescrittivi e automatizza le correzioni di ottimizzazione. | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/it/docs/experience-manager-sites-optimizer/content/home) | Ottimizza l’impatto aziendale rilevando e implementando automaticamente i miglioramenti apportati al sito web. Utilizzando l’intelligenza artificiale generativa e più tecnologie di monitoraggio, puoi aumentare l’acquisizione del traffico del sito, il coinvolgimento e altro ancora | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | Incrementa la conversione e il coinvolgimento attraverso un’individuazione intelligente dei prodotti in base al contesto, personalizzata in base alle preferenze e ai comportamenti individuali. | <ul><li>Adobe Brand Concierge</li></ul> |

## Ulteriori informazioni su questo argomento

* [Processi agente e consumo credito IA](/help/interface/features/ai-credit-consumption.md)
* [AI nella pagina principale della documentazione di CX Enterprise](https://experienceleague.adobe.com/en/docs/ai)
* [Panoramica degli agenti in AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Ulteriori informazioni su Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Vai a Business.adobe.com"}
