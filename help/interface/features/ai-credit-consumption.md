---
title: Processi agente e consumo credito IA
description: Scopri i processi degli agenti e i tassi di consumo dei crediti IA nelle applicazioni CX Enterprise.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
source-git-commit: 5b2b81c029b81b9f0689a012cb2a9ca8714c0b40
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 6%

---

# Processi dell’agente Adobe Experience Platform e consumo di crediti AI

Scopri i processi di intelligenza artificiale e il consumo di crediti di intelligenza artificiale nelle applicazioni aziendali CX. Per informazioni sull&#39;abilitazione delle funzionalità di IA per l&#39;agente nelle applicazioni CX Enterprise esistenti, vedere [IA per l&#39;agente in CX Enterprise](agentic-ai.md#existing-apps).

## Processi agente

Un _processo agente_ è una serie di attività e azioni eseguite da un agente per ottenere un risultato specifico, come indicato dagli input del cliente.

Utilizzando i prompt del linguaggio naturale tramite l’Assistente AI, puoi chiedere agli agenti di eseguire lavori specifici. In base a questi input, Agent Orchestrator coordina gli agenti appropriati per eseguire ogni passaggio all&#39;interno delle applicazioni aziendali CX.

## Crediti IA

Un credito _AI_ è una metrica basata sull&#39;utilizzo che quantifica l&#39;esecuzione di processi agente. I crediti IA non si applicano alle [applicazioni AI-first](/help/interface/features/agentic-ai.md).

## Consumo credito IA

L’utilizzo del credito di IA può variare a seconda della complessità e del valore del processo eseguito:

* Le attività semplici (spesso in un unico passaggio) richiedono meno crediti
* Le attività complesse (spesso con più passaggi) richiedono più crediti
* Le attività che comportano ragionamento avanzato, convalida, coordinamento di più agenti o integrazione richiedono più crediti

### Tassi di consumo del credito di IA stimati

| Agente | Processo | Applicazioni supportate | Stima crediti IA | Prompt di esempio |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Agente Audience | Ideazione di pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li><em>Visualizza campi per acquirenti benestanti</em></li><li><em>Trova tutti i campi relativi alle preferenze del cliente</em></li></ul> |
| Agente Audience | Gestione di audience e account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>Sono presenti tipi di pubblico duplicati?</em></li><li><em>Mostra i 5 tipi di pubblico più grandi.</em></li><li><em>Mostra tipi di pubblico non attivati in alcuna destinazione</em></li><li><em>Elenca tutti i tipi di pubblico utilizzati nei percorsi live</em></li></ul> |
| Agente Audience | Analisi del pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>Quali tipi di pubblico sono aumentati di oltre il 20% nell&#39;ultima settimana?</em></li><li><em>Quanto è cambiato il pubblico &quot;Loyal Platinum&quot; rispetto al valore di 30 giorni fa?</em></li><li><em>Qual è il pubblico che cresce più velocemente?</em></li></ul> |
| Agente Audience | Ideazione gruppo di acquisto | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>Quali account mostrano l&#39;intento per questi prodotti?</em></li><li><em>Visualizza le persone principali in base all&#39;intento del prodotto per XYZ.</em></li><li><em>Quali gruppi di acquisto hanno più di 5 membri?</em></li></ul> |
| Data Insights Agent | Analisi e visualizzazione dei dati | <ul><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 25 | <ul><li><em>Trend ordini in luglio</em></li><li><em>Mostra ricavi per area.</em></li><li><em>Mostra gli ordini per genere, da marzo a giugno.</em></li><li><em>Quali sono stati i 10 SKU principali in base al profitto nel mese di giugno</em></li><li><em>Percentuale di acquisti per mese dell&#39;anno</em></li><li><em>Quota di ricavi per categoria di prodotto</em></li></ul> |
| Journey Agent | ideazione percorso | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>Crea un percorso per gli account con spazi vuoti con l&#39;intento per la soluzione, concentrandosi sulle persone coinvolte nel contenuto del sito Web</em></li></ul> |
| Journey Agent | Analisi del percorso | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 50 | <ul><li><em>Desidero analizzare l&#39;abbandono per nodo per la campagna del 4 luglio percorso.</em></li><li><em>Si sono verificati conflitti di pianificazione per il percorso X</em></li><li><em>Mostra conflitti di sovrapposizione del pubblico per il percorso X</em></li></ul> |
| Journey Agent | Gestione dei percorsi | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 25 | <ul><li><em>Quanti percorsi di vita ho?</em></li><li><em>Elenca tutti i percorsi che utilizzano il pubblico X.</em></li><li><em>Elenca tutti i percorsi attualmente in modalità di test</em></li></ul> |
| Agente di supporto prodotto | Risoluzione dei problemi basata su Knowledge Base | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2C e B2B)</li><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 0 | <ul><li><em>Perché il conteggio dei profili differisce nel dashboard utilizzo licenze e nella home page di Experience Platform?</em></li><li><em>Quali sono i motivi per cui un percorso non viene attivato?</em></li><li><em>In che modo Adobe Experience Platform crea esperienze in tempo reale?</em></li><li><em>Come si configurano e utilizzano gli avvisi in Adobe Experience Platform?</em></li><li><em>Qual è il limite di ricchezza media per il profilo in Adobe Experience Platform Activation?</em></li></ul> |
| Agente di supporto prodotto | Creazione e tracciamento dei casi di supporto | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2C e B2B)</li><li>Customer Journey Analytics (edizioni B2C e B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>Crea un nuovo ticket di supporto per il processo di segmentazione non riuscito</em></li><li><em>Qual è lo stato del ticket E-001772068?</em></li></ul> |
| Agente di Content Advisor | Individuazione dei contenuti | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>Mostra frammenti di contenuto per la creazione della campagna di offerte WKND.</em></li><li><em>Trova immagini PNG per la creazione di pacchetti di prodotti.</em></li><li><em>Mostra le immagini con tag office nella cartella WKND.</em></li><li><em>Nella cartella WKND sono presenti svg?</em></li><li><em>Mostra tutti i moduli per la richiesta di prestito.</em></li><li><em>Sto cercando i moduli di onboarding dei dipendenti.</em></li></ul> |
| Agente di Content Advisor | <ul><li>Ottimizzazione dei contenuti</li></ul> | <ul><li>Adobe Experience Manager Assets e Dynamic Media</li></ul> | 10 | <ul><li><em>Crea una copia trasformata di 2.000 px come JPEG con qualità dell&#39;80%.</em></li><li><em>Crea una rappresentazione per una storia Instagram.</em></li><li><em>Sovrapponi l&#39;immagine con il 30% di grafica di sconto rispetto al banner promozionale, posizionandola a 100 px dal centro.</em></li><li><em>Cambia il colore di sfondo del file PNG in #ff8932.</em></li></ul> |
| Agente di governance del brand | <ul><li>Controlli della policy del brand</li></ul><ul><li>Autorizzazioni con Content Hub</li></ul><ul><li>Scadenza risorsa</li></ul> | <ul><li>Adobe Experience Manager Sites (criteri del marchio)</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>La pagina è allineata al mio marchio? `https://www.website/en.html`</em></li><li><em>Mostra tutte le regole ABAC di Content Hub esistenti</em></li><li><em>Le risorse dell&#39;utente scadono a breve?</em></li></ul> |
| Brand Experience Agent | <ul><li>Aggiornamento del contenuto</li><li>Creazione di Forms</li><li>Risoluzione dei problemi relativi alla pipeline</li></ul> | <ul><li>Servizi cloud Adobe Experience Manager</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>Il `URL`, aggiorna il titolo a Hello world</em></li><li><em>Crea un modulo per i contatti con i campi nome, e-mail e messaggio</em></li><li><em>Risoluzione dei problemi relativi alla pipeline non riuscita</em></li><li><em>Elencare le pipeline non riuscite per il programma principale.</em></li></ul> |
| Brand Experience Agent | Modernizzazione del sito | Servizi cloud Adobe Experience Manager | 100 | <ul><li><em>Esegui migrazione pagina `https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>Il consumo effettivo di credito IA può variare in base al numero di passaggi eseguiti e di iterazioni per passaggio.

## Ulteriori informazioni su questo argomento

* [GenAI in CX Enterprise](/help/interface/features/generative-ai.md)
* [Agentic AI in CX Enterprise](/help/interface/features/agentic-ai.md)
* [Versione di prova per agenti Adobe Experience Platform associata all&#39;utilizzo](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
