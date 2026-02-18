---
title: Processi agente e consumo credito IA
description: Scopri i processi degli agenti e i tassi di consumo di credito AI nelle applicazioni Experience Cloud.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: bb6adf13bed37d4a885b5baec28199efade592e1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Processi dell’agente Adobe Experience Platform e consumo di crediti AI

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
| ------ |-----|------------------------|----------------------|----------------|
| Agente Audience | Ideazione di pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>Mostra campi per acquirenti benestanti</li><li>Trova tutti i campi relativi alle preferenze del cliente</li></ul> |
| Agente Audience | Pubblico basato sulla conoscenza/creazione di account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>Crea un pubblico composto da persone che vivono in California</li><li>Genera un pubblico di membri di VIP che hanno speso più di $ 1.000 questo trimestre</li><li>Crea un pubblico di utenti che hanno acquistato articoli di abbigliamento ma che non hanno effettuato un acquisto negli ultimi 60 giorni</li></ul> |
| Agente Audience | Gestione di audience e account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>Ho dei tipi di pubblico duplicati?</li><li>Mostrami i miei 5 tipi di pubblico più grandi.</li><li>Mostra i tipi di pubblico non attivati in alcuna destinazione</li><li>Elenca tutti i tipi di pubblico utilizzati nei percorsi live</li></ul> |
| Agente Audience | Analisi del pubblico/account | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>Quali tipi di pubblico sono aumentati di oltre il 20% nell’ultima settimana?</li><li>Quanto è cambiato il pubblico &quot;Loyal Platinum&quot; rispetto al valore di 30 giorni fa?</li><li>Qual è il mio pubblico in più rapida crescita?</li></ul> |
| Agente Audience | Ideazione gruppo di acquisto | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>Quali account mostrano l&#39;intento per questi prodotti?</li><li>Visualizza le persone principali per intento di prodotto per XYZ.</li><li>Quali gruppi di acquisto hanno più di 5 membri?</li></ul> |
| Data Insights Agent | Analisi e visualizzazione dei dati | <ul><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 25 | <ul><li>Andamento ordini in luglio</li><li>Mostra ricavi per area geografica.</li><li>Mostra gli ordini per genere, da marzo a giugno.</li><li>Quali sono stati i miei 10 SKU principali in base al profitto a giugno</li><li>Percentuale di acquisti per mese dell&#39;anno</li><li>Quota di ricavi per categoria di prodotto</li></ul> |
| Journey Agent | ideazione percorso | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>Crea un percorso per gli account con spazi vuoti con l’intento per la mia soluzione, concentrandosi sulle persone coinvolte nel contenuto del sito web</li></ul> |
| Journey Agent | Creazione percorso | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 30 | <ul><li>Genera un percorso per inviare un promemoria agli utenti che non hanno completato il primo acquisto negli ultimi 7 giorni</li><li>Quando gli utenti completano il primo acquisto, invia una conferma SMS e una spiegazione dei vantaggi tramite e-mail dopo 3 giorni</li></ul> |
| Journey Agent | Analisi del percorso | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 50 | <ul><li>Voglio analizzare l’abbandono per nodo per la campagna del 4 luglio percorso.</li><li>Esistono conflitti di pianificazione per il percorso X</li><li>Mostra conflitti di sovrapposizione del pubblico per il percorso X</li></ul> |
| Journey Agent | Gestione dei percorsi | <ul><li>Adobe Journey Optimizer (edizioni B2B e B2C)</li></ul> | 25 | <ul><li>Quanti percorsi di vita ho?</li><li>Elenca tutti i percorsi utilizzando il pubblico X.</li><li>Elenca tutti i percorsi attualmente in modalità di test</li></ul> |
| Agente di supporto prodotto | Risoluzione dei problemi basata su Knowledge Base | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li><li>Adobe Journey Optimizer (edizioni B2C e B2B)</li><li>Customer Journey Analytics (edizioni B2C e B2B)</li></ul> | 0 | <ul><li>Perché il conteggio dei miei profili differisce in License Usage Dashboard (Dashboard di utilizzo della licenza) e nella home page di Experience Platform?</li><li>Quali sono i motivi per cui un percorso non si attiva?</li><li>In che modo Adobe Experience Platform crea esperienze in tempo reale?</li><li>Come si configurano e utilizzano gli avvisi in Adobe Experience Platform?</li><li>Qual è il limite medio di ricchezza dei profili in Adobe Experience Platform Activation?</li></ul> |
| Agente di supporto prodotto | Creazione e tracciamento dei casi di supporto | <ul><li>Real-Time CDP (edizioni B2B, B2C e B2P)</li>Adobe Journey Optimizer (edizioni B2C e B2B)<li>Customer Journey Analytics (edizioni B2C e B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>Crea un nuovo ticket di supporto per il processo di segmentazione non riuscito</li><li>Qual è lo stato del ticket E-001772068?</li></ul> |
| Agente di Content Advisor | Individuazione dei contenuti | <ul><li>Servizi cloud Adobe Experience Manager</li></ul> | 5 | <ul><li>Mostra frammenti di contenuto per la creazione di una campagna di offerte WKND.</li><li>Trova il pacchetto del prodotto PNG images.</li><li>Mostra le immagini con tag office nella cartella WKND.</li><li>Sono presenti file SVG nella cartella WKND?</li><li>Mostrami tutti i moduli di richiesta di prestito.</li><li>Sto cercando i moduli di onboarding dei dipendenti.</li></ul> |
| Agente di Content Advisor | <ul><li>Aggiornamento del contenuto</li><li>Ottimizzazione dei contenuti</li><li>Creazione di Forms</li></ul> | <ul><li>Servizi cloud Adobe Experience Manager</li></ul> | 10 | <ul><li>Crea una rappresentazione 2000px come JPEG con qualità 80%.</li><li>Crea una rappresentazione di una storia Instagram.</li><li>Sovrapponi l&#39;immagine con il 30% di sconto grafico sul banner promozionale, posizionandolo 100px dal centro.</li><li>Cambia il colore di sfondo del file PNG in #ff8932.</li></ul> |
| Brand Experience Agent | <ul><li>Supporto Experience</li><li>Supporto per l’implementazione</li></ul> | <ul><li>Servizi cloud Adobe Experience Manager</li></ul> | 5 | <ul><li>Risolvere i problemi relativi alla pipeline non riuscita</li><li>Elencare le pipeline non riuscite per il programma principale.</li><li>Analizza la pipeline non riuscita denominata &quot;Pipeline di sviluppo&quot;.</li><li>Risolvere i problemi dei 1234567 di esecuzione della pipeline</li></ul> |
| Brand Experience Agent | Modernizzazione del sito | Servizi cloud Adobe Experience Manager | 100 | <ul><li>Migrare la pagina https://wknd-trendsetters.site</li></ul> |

>[!NOTE]
>
>Il consumo effettivo di credito IA può variare in base al numero di passaggi eseguiti e di iterazioni per passaggio.

## Ulteriori informazioni su questo argomento

* [IA per l’agente in Experience Cloud](/help/interface/features/agentic-ai.md)
* [Versione di prova associata all&#39;utilizzo degli agenti Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)