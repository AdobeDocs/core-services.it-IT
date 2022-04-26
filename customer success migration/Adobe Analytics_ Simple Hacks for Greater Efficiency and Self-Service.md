---
source-git-commit: b7cf0832b1c2524abc6775f015b9ec8f508ae799
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---
**Adobe Analytics: Hack semplici per una maggiore efficienza e self-service**

**[Parte 1: Fuori dall’interfaccia utente]**

In questo articolo discuteremo le principali sfide che i team di analytics devono affrontare oggi e le nostre raccomandazioni per superarle utilizzando strategie al di fuori dell’interfaccia utente di Adobe Analytics. Per ulteriori informazioni sulle strategie in-tool / demo dal vivo, fai clic qui: [link a demo o articolo aggiuntivo con strategie in-tool]

**Sfide chiave per i team di Analytics**

Molti team di Analytics si trovano con una distribuzione del lavoro non equilibrata. Invece di un mix di analisi all&#39;80% e implementazione al 20%, molte organizzazioni si trovano al contrario, con la maggior parte dei loro sforzi spesi per l&#39;impostazione, il reporting e il supporto, invece di produrre analisi che guidano informazioni di alto valore.

I team di Analytics stanno trovando la loro produttività ed efficienza prosciugata per una serie di motivi: implementazioni in continua evoluzione, che cercano di mantenere la fiducia organizzativa nei dati e riducono il turnover degli analisti per evitare il lungo processo di formazione dei nuovi membri del team su strumenti di implementazione personalizzati non familiari.

Altre sfide chiave affrontate dagli analisti:

- **Concorrenza -** le aziende retail online e multicanale diventano più competitive
- **Aspettative dei clienti -** le esperienze dei clienti e le strategie di marketing diventano più complesse
- **Valore dati -** il valore di dati e informazioni accurati per promuovere un vantaggio competitivo diventa sempre più importante
- **Aspettative delle parti interessate -** partner commerciali, parti interessate e dirigenti richiedono sempre più dati prima dell&#39;approvazione
- **Gestione dei progetti -** il team di analytics soddisfa le richieste di implementazione della raccolta dati per un flusso infinito di nuove funzioni, producendo allo stesso tempo report accurati, aggiungendo nuovi analisti e scoprendo le nuove informazioni successive

**Tasti per l&#39;efficienza: Fuori dall’interfaccia utente**

1. Aggiorna i tuoi riferimenti di progettazione della soluzione (SDR)
1. Il DSP è la principale fonte di verità per la definizione e l’uso previsto di tutte le variabili all’interno dell’implementazione di Analytics
2. Il DSP è il riferimento principale con cui gli utenti diretti avranno bisogno di familiarità per trarre valore dall’interfaccia utente di Adobe Analytics
3. Mantenere l’aggiornamento e le versioni (è possibile utilizzare un formato data semplice) è molto importante

1. Documentazione e governance sulla raccolta dei dati - Tech Specs

Tech Spec ha un pubblico più limitato rispetto al DSP, ma è importante, se non di più, per un&#39;implementazione pienamente funzionale. Una buona specifica tecnica dovrebbe essere costituita da tutte le risorse di sviluppo, controllo qualità e gestione tag necessarie per implementare la soluzione. Assicurati di conservare tutti i documenti necessari per disporre di architetture di implementazione univoche.

Specifiche tecniche:

1. Caso d’uso: Istruzioni che descrivono come creare script per la raccolta di dati
2. Utenti principali: Sviluppatori
3. Altre note:
1. Documento altamente tecnico creato appositamente per gli ambienti di distribuzione
2. Utile sia per l&#39;implementazione iniziale che per la successiva manutenzione/riferimento
3. Organizzato per tipo di soluzione (ad esempio tracciamento campagna, metadati pagina, ecc.)
4. Il documento primario deve essere aggiornato e mantenuto in quanto vengono apportate modifiche al DSP
5. Archivio centrale
6. Numeri di versione sincronizzati per SDR e Tech Spec

1. Comunicare e documentare le finalità di progettazione della soluzione al lancio
1. Comunicare con l&#39;utente in mente
2. Quando avvii o aumenti la raccolta di dati, crea riepiloghi semplici da condividere con le parti interessate.
3. Rafforzare l&#39;uso corretto della variabile fuori dal cancello
4. Invia un messaggio e-mail di annuncio di riepilogo alle principali parti interessate e analisti
5. Crea una libreria che può essere utilizzata per supportare le ore di ufficio, le sessioni di abilitazione del team o per l’onboarding specifico per il team

1. Documentazione sulla raccolta dei dati, governance e igiene dei dati - AHD

Il dashboard di Analytics Health (AHD) si tuffa profondamente in un _singolo_ suite di rapporti e

fornisce una visualizzazione dei dati raccolti in ogni componente (eVar, prop ed evento). Questo può

aiuta a indicare se i dati hanno interrotto la raccolta in un componente in modo da poter intervenire per risolvere il problema. Puoi eseguire questo dashboard in qualsiasi momento in futuro per qualsiasi suite di rapporti.

Dashboard di stato di Analytics (AHD):

1. Caso d’uso: Snapshot di ogni metrica e dimensione acquisito da una singola suite di rapporti
2. Utenti principali: PMI e/o sviluppo principali di Analytics
3. Altre note:
1. Fornito tramite Excel utilizzando un’integrazione personalizzata dell’API di reporting di Adobe
2. Gli utenti devono avere accesso API ai servizi web di Analytics
3. Sono disponibili opzioni per la semiautomazione

5. Vincere con l&#39;espansione del mondo delle PMI

1. Creare PMI all&#39;interno delle varie squadre dell&#39;organizzazione
2. Costruire la loro presenza aiutando a socializzare rilasci e vittorie
3. Sfruttare le ore regolari di ufficio per aiutare i formatori e ridurre le domande ad hoc

In questo articolo abbiamo rivisto i modi per migliorare l’efficienza al di fuori dell’interfaccia utente di Adobe Analytics. Per ulteriori informazioni sulle strategie in-tool, fai clic qui: [link a demo o articolo aggiuntivo con strategie in-tool]