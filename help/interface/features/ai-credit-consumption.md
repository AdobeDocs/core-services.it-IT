---
title: Processi agente e consumo credito IA
description: Scopri i processi degli agenti e i tassi di consumo di credito AI nelle applicazioni Experience Cloud.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: d4734c4b43defedb20b7eb65556f56987dce02ae
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 4%

---

# Processi dell’agente Adobe Experience Platform e consumo di crediti AI

Ultimo aggiornamento: **mercoledì 3 marzo 2026**

Scopri i processi di intelligenza artificiale e il consumo di crediti di intelligenza artificiale nelle applicazioni Experience Cloud. Per informazioni sull&#39;abilitazione delle funzionalità di IA per l&#39;agente nelle applicazioni Experience Cloud esistenti, vedere [IA per l&#39;agente in Experience Cloud](agentic-ai.md#existing-apps).

## Processi agente

Un _processo agente_ è una serie di attività e azioni eseguite da un agente per ottenere un risultato specifico, come indicato dagli input del cliente.

Utilizzando i prompt del linguaggio naturale tramite l’Assistente AI, puoi chiedere agli agenti di eseguire lavori specifici. In base a tali input, Agent Orchestrator coordina gli agenti appropriati per eseguire ogni passaggio all’interno delle applicazioni Experience Cloud pertinenti.

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
| Agente Audience | Ideazione di pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>_Visualizza campi per acquirenti benestanti_</li><li>_Trova tutti i campi relativi alle preferenze del cliente_</li></ul> |
| Agente Audience | Pubblico basato sulla conoscenza/creazione di account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>_Crea un pubblico composto da persone che vivono in California_</li><li>_Genera un pubblico di membri di VIP che hanno speso più di $ 1.000 questo trimestre_</li><li>_Crea un pubblico di utenti che hanno acquistato articoli di abbigliamento ma non hanno effettuato un acquisto negli ultimi 60 giorni_</li></ul> |
| Agente Audience | Gestione di audience e account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_Sono presenti tipi di pubblico duplicati?_</li><li>_Mostra i 5 tipi di pubblico più grandi._</li><li>_Mostra tipi di pubblico non attivati in alcuna destinazione_</li><li>_Elenca tutti i tipi di pubblico utilizzati nei percorsi live_</li></ul> |
| Agente Audience | Analisi del pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_Quali tipi di pubblico sono aumentati di oltre il 20% nell&#39;ultima settimana?_</li><li>_Quanto è cambiato il pubblico &quot;Loyal Platinum&quot; rispetto al valore di 30 giorni fa?_</li><li>_Qual è il pubblico che cresce più velocemente?_</li></ul> |
| Agente Audience | Ideazione gruppo di acquisto | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_Quali account mostrano l&#39;intento per questi prodotti?_</li><li>_Visualizza le persone principali in base all&#39;intento del prodotto per XYZ._</li><li>_Quali gruppi di acquisto hanno più di 5 membri?_</li></ul> |
| Data Insights Agent | Analisi e visualizzazione dei dati | <ul><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 25 | <ul><li>_Trend ordini in luglio_</li><li>_Mostra ricavi per area._</li><li>_Mostra gli ordini per genere, da marzo a giugno._</li><li>_Quali sono stati i 10 SKU principali in base al profitto nel mese di giugno_</li><li>_Percentuale di acquisti per mese dell&#39;anno_</li><li>_Quota di ricavi per categoria di prodotto_</li></ul> |
| Journey Agent | ideazione percorso | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_Crea un percorso per gli account con spazi vuoti con l&#39;intento per la soluzione, concentrandosi sulle persone coinvolte nel contenuto del sito Web_</li></ul> |
| Journey Agent | Creazione percorso | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 30 | <ul><li>_Genera un percorso per inviare un promemoria agli utenti che non hanno completato il primo acquisto negli ultimi 7 giorni_</li><li>_Quando gli utenti completano il loro primo acquisto, invia una conferma SMS e una spiegazione dei vantaggi tramite e-mail dopo 3 giorni_</li></ul> |
| Journey Agent | Analisi del percorso | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 50 | <ul><li>_Desidero analizzare l&#39;abbandono per nodo per la campagna del 4 luglio percorso._</li><li>_Si sono verificati conflitti di pianificazione per il percorso X_</li><li>_Mostra conflitti di sovrapposizione del pubblico per il percorso X_</li></ul> |
| Journey Agent | Gestione dei percorsi | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 25 | <ul><li>_Quanti percorsi di vita ho?_</li><li>_Elenca tutti i percorsi che utilizzano il pubblico X._</li><li>_Elenca tutti i percorsi attualmente in modalità di test_</li></ul> |
| Agente di supporto prodotto | Risoluzione dei problemi basata su Knowledge Base | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2C e B2B)</li><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 0 | <ul><li>_Perché il conteggio dei profili differisce nel dashboard utilizzo licenze e nella home page di Experience Platform?_</li><li>_Quali sono i motivi per cui un percorso non viene attivato?_</li><li>_In che modo Adobe Experience Platform crea esperienze in tempo reale?_</li><li>_Come si configurano e utilizzano gli avvisi in Adobe Experience Platform?_</li><li>_Qual è il limite di ricchezza media per il profilo in Adobe Experience Platform Activation?_</li></ul> |
| Agente di supporto prodotto | Creazione e tracciamento dei casi di supporto | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li>Adobe Journey Optimizer (edizioni B2C e B2B)<li>Customer Journey Analytics (edizioni B2C e B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>_Crea un nuovo ticket di supporto per il processo di segmentazione non riuscito_</li><li>_Qual è lo stato del ticket E-001772068?_</li></ul> |
| Agente di Content Advisor | Individuazione dei contenuti | <ul><li>Adobe Experience Manager Assets</li></ul> | 5 | <ul><li>_Mostra frammenti di contenuto per la creazione della campagna di offerte WKND._</li><li>_Trova immagini PNG per la creazione di pacchetti di prodotti._</li><li>_Mostra le immagini con tag office nella cartella WKND._</li><li>_Nella cartella WKND sono presenti svg?_</li><li>_Mostra tutti i moduli per la richiesta di prestito._</li><li>_Sto cercando i moduli di onboarding dei dipendenti._</li></ul> |
| Agente di Content Advisor | <ul><li>Ottimizzazione dei contenuti</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul> | 10 | <ul><li>_Crea una copia trasformata di 2.000 px come JPEG con qualità dell&#39;80%._</li><li>_Crea una rappresentazione per una storia Instagram._</li><li>_Sovrapponi l&#39;immagine con il 30% di grafica di sconto rispetto al banner promozionale, posizionandola a 100 px dal centro._</li><li>_Cambia il colore di sfondo del file PNG in #ff8932._</li></ul> |
| Brand Experience Agent | <ul><li>Aggiornamento del contenuto</li><li>Creazione di Forms</li><li>Risoluzione dei problemi relativi alla pipeline</li></ul> | <ul><li>Servizi cloud Adobe Experience Manager</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li>_Risoluzione dei problemi relativi alla pipeline non riuscita_</li><li>_Elencare le pipeline non riuscite per il programma principale._</li><li>_Analizza la pipeline non riuscita denominata &quot;Pipeline di sviluppo&quot;_</li><li>_Risoluzione dei problemi di esecuzione della pipeline 1234567_</li></ul> |
| Brand Experience Agent | Modernizzazione del sito | Servizi cloud Adobe Experience Manager | 100 | <ul><li>_Esegui migrazione pagina`https://wknd-trendsetters.site`_</li></ul> |

>[!NOTE]
>
>Il consumo effettivo di credito IA può variare in base al numero di passaggi eseguiti e di iterazioni per passaggio.

## Ulteriori informazioni su questo argomento

* [IA per l’agente in Experience Cloud](/help/interface/features/agentic-ai.md)
* [Versione di prova associata all&#39;utilizzo degli agenti Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
