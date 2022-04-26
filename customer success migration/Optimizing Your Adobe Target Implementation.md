---
source-git-commit: b7cf0832b1c2524abc6775f015b9ec8f508ae799
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---
**Ottimizzazione dell’implementazione Adobe Target**

Se sei nuovo nell’organizzazione e vuoi acquisire familiarità con ciò che è in vigore da una pratica di test e ottimizzazione, in questo articolo ti guidi dove iniziare. Inizieremo con una panoramica dell’implementazione e della struttura di Adobe Target. Scoprirai come comprendere e controllare la configurazione della tua organizzazione. Infine, discuteremo le tecniche comuni per la risoluzione dei problemi e i suggerimenti sulla creazione di un archivio delle conoscenze per il tuo team.

Adobe Target è uno strumento che consente di testare e indirizzare contenuti univoci a visitatori diversi. Per una panoramica delle funzioni disponibili, [visita questa guida](https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en).

**Implementazione e struttura di Target**

Prima di passare al processo di implementazione per Adobe Target o alla sua struttura, è utile comprendere alcuni aspetti fondamentali del software.

Adobe Target è uno strumento che consente di testare e indirizzare contenuti univoci a visitatori diversi senza modificare il codice nativo del sito web. Target modifica temporaneamente l’esperienza utente finale e tiene traccia del comportamento degli utenti dopo la visualizzazione della modifica. Target offre anche la possibilità di modificare l’esperienza per gli utenti finali in base alle informazioni sul profilo o alle azioni precedenti.

Esistono tre tipi di attività fondamentali di Target:

1. Test A/B
2. Test multivariato (MVT)
3. Test esperienza

**Test A/B** confronta due o più esperienze per vedere quale migliora maggiormente le conversioni durante un periodo di test pre-specificato. Il test A/B è un esperimento altamente controllato con le misurazioni del traffico, suddiviso per percentuali anziché per una regola, che consente di:

- analizzare i dati del test.
- per ottenere informazioni sul pubblico.
- per determinare quale esperienza funziona meglio.

**Test multivariato** (MVT) confronta le combinazioni di offerte tra gli elementi di una pagina per vedere quale combinazione funziona meglio per un pubblico specifico. Questo test identifica inoltre quale elemento della pagina migliora maggiormente le conversioni durante un periodo di test pre-specificato. MVT fornisce:

- Un modo per visualizzare più offerte in più elementi.
- Un metodo per testare l’esperienza univoca risultante rispetto a un obiettivo specifico.
- Informazioni su quali elementi hanno il maggiore impatto negativo o positivo sulle interazioni dei visitatori.

**Test esperienza** (Targeting esperienza) fornisce contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall’addetto al marketing. Questo metodo fornisce un modo per eseguire il targeting di contenuti specifici per un pubblico specifico in base a un set di regole di allocazione definite.

Come funziona Target?

Ecco un esempio di alto livello di funzionamento di Target:

1. Un visitatore richiede una pagina dal server e la visualizza nel browser.
2. Nel browser del visitatore viene impostato un cookie di prima parte per memorizzare il comportamento.
3. La pagina chiama quindi Adobe Target.
4. Il contenuto viene visualizzato in base alle regole dell’attività dell’utente.
5. Adobe Target acquisisce metriche specifiche definite nella configurazione dell’attività per misurare l’impatto delle esperienze di test.

Target è basato su una &quot;mbox globale&quot; che consente di avere un impatto qualsiasi sulla pagina. Questa funzione viene implementata al caricamento della pagina come collegamento codificato al file at.js o tramite un Tag Manager come Adobe Launch.

**Comprendere l’implementazione corrente**

Per comprendere l’implementazione corrente, l’Adobe consiglia di rivedere l’implementazione dell’interfaccia utente di Target insieme all’implementazione di Tag Manager e Caricamento pagina.

1. 

Per rivedere l&#39;interfaccia utente di Target:

1. Inizia la tua revisione sull’interfaccia utente di Target:
- Rivedi lo stack di tecnologia di Target
- Conferma le funzioni disponibili
- Identifica dove è live la distribuzione
2. Attività di revisione per le best practice:

- Analisi delle campagne storiche per la maturità del programma

1. Disattiva le attività precedenti:
- Archiviare e ripulire le risorse Target che non sono più utilizzate in modo corrente o futuro
2. Pubblico di revisione
3. Esamina le definizioni dell’ambiente e i domini associati
4. Revisione degli script di profilo per l&#39;applicabilità
- Tutti gli script di profilo vengono eseguiti su ogni chiamata di destinazione
- Gestisci efficienza delle chiamate rimuovendo gli script non applicabili

Per rivedere Gestione tag e Caricamento pagina:

1. Conferma quanto segue in Tag Manager:
- Distribuzione del codice JavaScript di Target previsto
- Soluzione appropriata per nascondere i contenuti
- Imposta le regole necessarie per popolare le chiamate Target con i parametri previsti
2. Conferma quanto segue durante il caricamento della pagina:
- Numeri di versione corrispondenti per l’URL della richiesta e l’URL della richiesta di Target
- Valore Experience Cloud ID popolato (Cloud Body)
- Valori di integrazione previsti presenti (Cloud Body)
- Parametri di Target compilati nelle pagine appropriate

**Attività di audit di Target**

Per evitare di passare manualmente da una pagina all’altra per controllare le attività di Target, utilizza Adobe Auditor per aiutare a comprendere lo stato tecnico corrente dell’implementazione. Adobe Auditor è basato su ObservePoint e può essere configurato per essere eseguito a livello manuale, per identificare problemi di implementazione di alto livello sul sito.

Adobe Auditor fornisce:

- Un alto livello di salute del sito
- Chiamate rapide per problemi di implementazione

Adobe consiglia di eseguire controlli manuali mensili per:

- Identificare le pagine senza tag
- Identificare le versioni incoerenti
- Scopri le versioni aggiornate
- Fornire informazioni dettagliate che possono essere esportate

**Risoluzione dei problemi comuni**

**Nota generale:** Adobe consiglia di installare Adobe Experience Platform Debugger.

Di seguito sono riportati alcuni suggerimenti generali per la risoluzione dei problemi durante l’accesso a Experience Cloud:

**Cache e cookie**

- Cancellazione della cache e dei cookie
- Presta attenzione utilizzando la modalità privata (ad esempio: La modalità privata in Firefox può bloccare Target)

**Sei qualificato per l’attività?**

- Verifica di aver eseguito gli stessi passaggi utilizzati dal pubblico nell’attività
- Utilizza i token di risposta o mboxTrace per controllare i valori di profilo e segmento

**Di seguito sono riportati alcuni suggerimenti generali per la risoluzione dei problemi durante la convalida di visual/funzionale:**

Se ti trovi nell’esperienza Target e non vedi l’esperienza visiva prevista:

Controlla la risposta di Target:

- Se il codice non viene eseguito:

1. Controllare le attività in conflitto
2. Contattare l’Assistenza clienti

- Se il codice viene eseguito:

1. Rielaborazione del codice in tale scenario

**Mantenimento di un archivio delle conoscenze**

Un Knowledge Repository è una piattaforma online utilizzata per la documentazione e la condivisione di informazioni. L’archivio della conoscenza contiene informazioni specifiche per l’implementazione e può contenere informazioni specifiche per il team.

Idealmente, l’archivio dovrebbe consentire la modifica e il salvataggio automatico all’interno della piattaforma. Una volta configurato inizialmente, è facile da mantenere e mantenere aggiornato. Il contenuto all’interno del Knowledge Repository viene curato in base ai ruoli utente.

I documenti tipici in un archivio della conoscenza includono:

- **Documento introduttivo** - un documento utilizzato per spiegare chiaramente gli obiettivi, gli obiettivi, i processi e la struttura del programma
- **Archivio delle idee** - un documento utilizzato per gestire e assegnare priorità a idee potenziali non pronte per il processo di test
- **Tabella di marcia del programma** - un documento utilizzato per gestire tutti gli aspetti delle attività di test una volta che le idee sono pronte per avviare il processo di test
- **Documento del piano di attività** - un documento utilizzato per delineare le informazioni necessarie per creare e avviare attività
- **Documento del piano di attività** - un documento utilizzato per comunicare i risultati e i passi successivi raccomandati alle parti interessate
- **Dashboard del programma** - un documento utilizzato per tenere traccia delle prestazioni del programma, della cadenza e dei benefici sui ricavi nel tempo.

Per ulteriori informazioni, consulta il nostro webinar con il Consulente Senior, Wilder Freed: [https://adobecustomersuccess.adobeconnect.com/p4p7xlp7dh42mp4/](https://adobecustomersuccess.adobeconnect.com/p4p7xlp7dh42mp4/)