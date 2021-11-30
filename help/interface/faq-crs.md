---
description: Domande frequenti su Attributi del cliente in Adobe Experience Cloud, per Adobe Analytics e Adobe Target.
keywords: Attributi del cliente
solution: Experience Cloud
title: 'Risposte alle domande frequenti su Attributi del cliente '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: ht
source-wordcount: '1178'
ht-degree: 100%

---

# Domande frequenti su [!UICONTROL Attributi del cliente]

Domande frequenti e best practice per [!UICONTROL Attributi del cliente] in Adobe Analytics e Adobe Target.

## Best practice e limitazioni {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Assistenza e limitazioni durante l&#39;utilizzo degli [!UICONTROL attributi del cliente].

| Problema | Descrizione |
|--- |--- |
| Limiti di sottoscrizione degli [!UICONTROL attributi del cliente] | Quando si esegue l’aggiornamento ad Analytics Premium, si verifica un ritardo di 24 ore prima che gli attributi aggiuntivi diventano disponibili. Durante questo lasso di tempo potresti ricevere un errore di tipo [!UICONTROL Limite di attributi massimo per abbonamento]. |
| Più accessi sullo stesso dispositivo | Quando si utilizza la funzione [!UICONTROL Attributi del cliente] per caricare i profili dei clienti in un’origine di dati, Adobe consiglia di non condividere i dispositivi (ovvero di non usare lo stesso Experience Cloud ID). L’Experience Cloud ID (ECID) persiste sul dispositivo. Se si condivide un dispositivo, lo stesso ECID verrà collegato a più utenti e questo può causare risultati imprevisti in [!DNL Target]. **Nota:** per Mobile, l’ECID è permanente dopo l’installazione dell’app Mobile. È quindi necessario reinstallare l’app per generare un nuovo ECID. Per il web, viene generato un nuovo ECID dopo che il cookie del browser viene cancellato. |
| Limitazione della frequenza giornaliera di caricamento | Adobe consiglia di aggiornare la funzione Attributi del cliente solo una volta al giorno. Devi aspettare almeno 24 ore per caricare un altro file di dati di profilo cliente per lo stesso set di profili. |
| ID Analytics personalizzato (`s.visitorID`) | L&#39;impostazione di un ID cliente usando `s.visitorID` è un metodo di identificazione degli utenti in Analytics. Tuttavia, le integrazioni in cui i dati [!DNL Analytics] vengono esportati o importati utilizzando il servizio ID non funzioneranno quando un visitatore viene identificato mediante `s.visitorID.`<br>Ciò include, ad esempio, tipi di pubblico condivisi, [!DNL Analytics] for Adobe Target (A4T) e [!UICONTROL Attributi del cliente].<br>Per queste integrazioni, l&#39;impostazione di un ID Analytics personalizzato non è supportata. |
| Limitazioni del numero di caratteri in [!DNL Analytics] | Quando crei un abbonamento [!DNL Analytics], le lunghezze dei campi per i file caricati vengono troncate a 255 caratteri. |

{style=&quot;table-layout:auto&quot;}

## Domande frequenti sugli attributi del cliente {#section_E47866EEA83348E09FE43CEC5E44C461}

| Domanda | Risposta |
|--- |--- |
| Posso ricevere notifiche sullo stato di caricamento degli attributi del cliente? | Sì. |
| Cosa devo fare per iniziare a utilizzare attributi del cliente? | <ol><li>Richiedi il provisioning. Se sei un cliente Analytics, Adobe fornisce il provisioning per gli attributi del cliente. Se utilizzi solo Adobe Target e non disponi di Analytics, devi richiedere il provisioning dei servizi core contattando l’Assistenza clienti.</li> <li>Parla con il team interno addetto al CRM. Scopri i tipi di dati cliente disponibili e quali vorresti utilizzare in Analytics ed Experience Cloud.</li><li>Implementa i servizi principali. Consulta [Abilitare le applicazioni per i servizi principali](core-services.md) per informazioni su come modernizzare l&#39;implementazione. (per informazioni importanti, consulta la sezione sulla sincronizzazione degli ID cliente).</li></ol> **Nota:** sono disponibili le domande frequenti di amministratori sull&#39;implementazione dei servizi di base di [qui](faq.md). |
| Quanti attributi del cliente posso utilizzare? | Puoi caricare centinaia di colonne `.csv` nel servizio Attributi del cliente. Tuttavia, quando configuri le sottoscrizioni e selezioni gli attributi, si applicano i seguenti limiti (per suite di rapporti), a seconda delle applicazioni che possiedi:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totali</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| È richiesta la migrazione al servizio Experience Cloud ID? | La migrazione dipende dalle applicazioni che utilizzi. <ul><li>Adobe Analytics: fortemente consigliata </li><li>Adobe Target: obbligatoria. </li></ul><br>L’utilizzo del servizio Experience Cloud ID consente di utilizzare le funzionalità di Experience Cloud più recenti, tra cui i tipi di pubblico in tempo reale, la modernizzazione di Adobe Target, l’integrazione con Analytics e il tracciamento degli heartbeat video. <br> Per ulteriori dettagli, consulta [Abilitare le applicazioni per i servizi principalii](core-services.md). <br>**Nota:** il [servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) è l’implementazione modernizzata di quello che in precedenza era noto come _servizio ID visitatore di Analytics._ |
| In che modo la funzionalità Attributi del cliente si relaziona con Adobe Audience Manager? | Anche se Audience Manager può ricevere dati per l’identificazione del pubblico, non può eseguire funzionalità di analisi in cui gli attributi vengono associati ai dati comportamentali storici. Inoltre, non fornisce le funzionalità di reporting, analisi e segmentazione che sono disponibili in Adobe Analytics. [!UICONTROL People] consente di correlare tra loro dati dettagliati provenienti da più applicazioni e associarli a un singolo ID da utilizzare in Experience Cloud. <br>In Adobe Target gli attributi del cliente vengono visualizzati come attributi individuali che possono essere combinati con altre regole per creare tipi di pubblico. I pubblici condivisi con il servizio [!UICONTROL Persone] sono pubblici completi che non possono essere modificati. |
| **Solo per Analytics:** In che modo questa funzionalità è diversa da quella fornita in Analytics Premium? | In passato, i clienti interessati a combinare i dati di Attributi del cliente con i dati di Analytics si sono affidati in larga misura allo strumento Data Workbench per questa funzionalità. La funzionalità [!UICONTROL Attributi del cliente] si estende a un pubblico più ampio, fornendo gli attributi dei clienti come dimensioni e metriche in Reports &amp; Analytics, Ad Hoc Analysis e Report Builder. I clienti Analytics Standard avranno accesso agli Attributi del cliente, ma con funzionalità limitate. La funzionalità completa è disponibile per i clienti Analytics Premium. |
| **Solo per Adobe Target:** è possibile precaricare o caricare dati per clienti che Adobe Target non ha mai visto? | Sì. Quando il visitatore effettua la sua prima richiesta ad Adobe Target, il sistema ne recupera le informazioni esistenti disponibili da Attributi del cliente e le utilizza per il targeting. **Nota:** il recupero di tali dati può richiedere fino a 20 minuti dalla prima interazione del visitatore con Adobe Target. |
| **(Solo per Adobe Target)** Posso creare un super pubblico combinando i dati Attributi del cliente con i dati di pubblico condiviso? | No. I dati di pubblico condiviso costituiscono un pubblico completo. |
| **Solo per Adobe Target:** come si confronta la funzionalità degli [!UICONTROL attributi del cliente] con l&#39;API di profilo di massa di Adobe Target? | L&#39;API di profilo di massa consente di aggiornare i profili Adobe Target direttamente tramite l&#39;API, sia singolarmente che in massa. La funzionalità è simile agli attributi del cliente, ma con le seguenti differenze fondamentali:<ul><li>L&#39;API di profilo è una chiamata API REST e gli attributi del cliente utilizzano FTP.</li><li>L&#39;API di profilo di Adobe Target invia dati solo ad Adobe Target invece che all&#39;intero Experience Cloud.</li><li>La funzionalità Attributi del cliente fornisce una semplice interfaccia per creare e gestire questi dati esterni.</li></ul> |
| **Solo per Adobe Target:** il caricamento di dati dagli attributi del cliente ad Adobe Target estende la durata del profilo del visitatore di Adobe Target? | Sì. Consulta [Durata del profilo del visitatore](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=it) nella Guida di Adobe Target. |
| **Solo per Adobe Target:** posso eseguire il targeting sui dati caricati negli Attributi del cliente subito dopo che il visitatore è stato identificato dall&#39;ID cliente? | Sì. Nella chiamata del server ad Adobe Target, che include l’ID di terze parti mbox, saranno disponibili tutti i dati di Attributi del cliente. |
| **(Solo per Adobe Target)** Cosa rappresenta la colonna **[!UICONTROL Stato di sincronizzazione]** per i file caricati nell’origine Attributi del cliente? | Puoi visualizzare il numero di record pubblicati e sincronizzati da Adobe Target selezionando l’icona Stato di sincronizzazione in corrispondenza di un file di attributi specifico. `Sync %` è una metrica in tempo reale che specifica la percentuale di profili sincronizzati in Adobe Target.<br> **Nota:** la sincronizzazione degli attributi con Adobe Target potrebbe richiedere fino a 24 ore. |
| Cosa rappresentano le metriche di caricamento dei file nell&#39;origine attributi del cliente? | Puoi controllare lo stato degli attributi caricati in Attributi del cliente con l&#39;aiuto delle metriche seguenti: <ul><li>Record: numero di record nel file degli attributi.</li><li>**Nuovi record:** numero di nuovi record presenti nel file degli attributi.</li> <li>**Record aggiornati:** numero di record già presenti in Attributi del cliente con valori aggiornati nel file.</li><li>**Tutti i dati (record):** numero totale di record caricati correttamente in Attributi del cliente.</li></ul> |

{style=&quot;table-layout:auto&quot;}