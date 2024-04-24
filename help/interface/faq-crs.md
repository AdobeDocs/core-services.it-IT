---
description: Domande frequenti su  [!DNL Customer Attributes]  in Adobe Experience Cloud, per Adobe Analytics e Adobe Target.
solution: Experience Cloud
title: Domande frequenti su  [!DNL Customer Attributes]
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: ht
source-wordcount: '1102'
ht-degree: 100%

---

# Domande frequenti su [!DNL Customer Attributes]

Domande frequenti e best practice di [!DNL Customer Attributes] in Adobe Analytics e Adobe Target.

## Best practice e limitazioni {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Assistenza e limitazioni per l’utilizzo di [!DNL Customer Attributes].

| Problema | Descrizione |
|--- |--- |
| Limiti di sottoscrizione degli [!UICONTROL attributi del cliente] | Quando si esegue l’aggiornamento ad Analytics Premium, si verifica un ritardo di 24 ore prima che gli attributi aggiuntivi diventano disponibili. Durante questo lasso di tempo potresti ricevere un errore di tipo [!UICONTROL Limite di attributi massimo per abbonamento]. |
| Più accessi sullo stesso dispositivo | Quando si utilizza [!DNL Customer Attributes] per caricare i profili dei clienti in un’origine dati, Adobe consiglia di non condividere i dispositivi (ovvero di non usare lo stesso ID di Experience Cloud). L’Experience Cloud ID (ECID) persiste sul dispositivo. Se si condivide un dispositivo, lo stesso ECID verrà collegato a più utenti e questo può causare risultati imprevisti in [!DNL Target]. **Nota:** per Mobile, l’ECID è permanente dopo l’installazione dell’app Mobile. È quindi necessario reinstallare l’app per generare un nuovo ECID. Per il web, viene generato un nuovo ECID dopo che il cookie del browser viene cancellato. |
| Limitazione della frequenza giornaliera di caricamento | Adobe consiglia di aggiornare gli [!DNL Customer Attributes] solo una volta al giorno. Devi aspettare almeno 24 ore per caricare un altro file di dati di profilo cliente per lo stesso set di profili. |
| ID Analytics personalizzato (`s.visitorID`) | L&#39;impostazione di un ID cliente usando `s.visitorID` è un metodo di identificazione degli utenti in Analytics. Tuttavia, le integrazioni in cui i dati di [!DNL Analytics] vengono esportati o importati utilizzando il servizio ID non funzioneranno quando un visitatore viene identificato mediante `s.visitorID.`<br>. Ciò include, tra l’altro, tipi di pubblico condivisi, [!DNL Analytics] for Adobe Target (A4T) e [!DNL Customer Attributes].<br>Per queste integrazioni, l&#39;impostazione di un ID Analytics personalizzato non è supportata. |
| Limitazioni del numero di caratteri in [!DNL Analytics] | Quando crei un abbonamento [!DNL Analytics], le lunghezze dei campi per i file caricati vengono troncate a 255 caratteri. |

{style="table-layout:auto"}

## Domande frequenti su [!DNL Customer Attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| Domanda | Risposta |
|--- |--- |
| Posso ricevere notifiche sullo stato di caricamento degli [!DNL Customer Attributes]? | Sì. |
| Cosa devo fare per iniziare a utilizzare [!DNL Customer Attributes]? | <ol><li>Richiedi il provisioning. Se sei un cliente Analytics, Adobe fornisce il provisioning per gli [!DNL Customer Attributes]. Se utilizzi solo Adobe Target e non disponi di Analytics, devi richiedere il provisioning dei servizi core contattando l’Assistenza clienti.</li> <li>Parla con il team interno addetto al CRM. Scopri i tipi di dati cliente disponibili e quali vorresti utilizzare in Analytics ed Experience Cloud.</li><li>Implementa i servizi principali. Consulta [Abilitare le applicazioni per i servizi principali](core-services.md) per informazioni su come modernizzare l&#39;implementazione. (per informazioni importanti, consulta la sezione sulla sincronizzazione degli ID cliente).</li></ol> **Nota:** le domande frequenti di un amministratore sull&#39;implementazione dei servizi di core sono disponibili [qui](faq.md). |
| Quanti [!DNL Customer Attributes] posso utilizzare? | Puoi caricare centinaia di colonne `.csv` nel servizio Attributi del cliente. Tuttavia, quando configuri le sottoscrizioni e selezioni gli attributi, si applicano i seguenti limiti (per suite di rapporti), a seconda delle applicazioni che possiedi:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totali</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| È richiesta la migrazione al servizio Experience Cloud ID? | La migrazione dipende dalle applicazioni che utilizzi. <ul><li>Adobe Analytics: fortemente consigliata </li><li>Adobe Target: obbligatoria. </li></ul><br>L’utilizzo del servizio Experience Cloud ID consente di utilizzare le funzionalità di Experience Cloud più recenti, tra cui i tipi di pubblico in tempo reale, la modernizzazione di Adobe Target, l’integrazione con Analytics e il tracciamento degli heartbeat video. <br> Per ulteriori dettagli, consulta [Abilitare le applicazioni per i servizi principalii](core-services.md). <br>**Nota:** il [servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it) è l’implementazione modernizzata di quello che in precedenza era noto come _servizio ID visitatore di Analytics._ |
| In che modo la funzionalità Attributi del cliente si relaziona con Adobe Audience Manager? | Anche se Audience Manager può ricevere dati per l’identificazione del pubblico, non può eseguire funzionalità di analisi in cui gli attributi vengono associati ai dati comportamentali storici. Inoltre, non fornisce le funzionalità di reporting, analisi e segmentazione che sono disponibili in Adobe Analytics. [!UICONTROL People] consente di legare insieme dati complessi provenienti da più applicazioni e di associarli a un singolo ID da utilizzare in Experience Cloud. <br> In Adobe Target, [!DNL Customer Attributes] vengono visualizzati come attributi individuali che possono essere combinati con altre regole per creare tipi di pubblico. I pubblici condivisi con il servizio [!UICONTROL Persone] sono pubblici completi che non possono essere modificati. |
| **Solo per Analytics:** In che modo questa funzionalità è diversa da quella fornita in Analytics Premium? | In passato, i clienti interessati a combinare i dati di Attributi del cliente con i dati di Analytics si sono affidati in larga misura allo strumento Data Workbench per questa funzionalità. La funzionalità [!DNL Customer Attributes] si estende a un pubblico più ampio, fornendo [!DNL Customer Attributes] come dimensioni e metriche in Reports &amp; Analytics, Ad Hoc Analysis e Report Builder. I clienti Analytics Standard avranno accesso agli [!DNL Customer Attributes], ma con funzionalità limitate. La funzionalità completa è disponibile per i clienti Analytics Premium. |
| **Solo per Adobe Target:** è possibile precaricare o caricare dati per clienti che Adobe Target non ha mai visto? | Sì. Quando il visitatore effettua la sua prima richiesta ad Adobe Target, il sistema recupera le informazioni esistenti disponibili dagli [!DNL Customer Attributes] e utilizza tali dati per il targeting. **Nota:** il recupero di tali dati può richiedere fino a 20 minuti dalla prima interazione del visitatore con Adobe Target. |
| **(Solo per Adobe Target)** Posso creare un super pubblico combinando i dati Attributi del cliente con i dati di pubblico condiviso? | No. I dati di pubblico condiviso costituiscono un pubblico completo. |
| **(Solo per Adobe Target)** Come si confronta la funzionalità degli [!DNL Customer Attributes] con l’API di profilo di massa di Adobe Target? | L’API di profilo di massa consente di aggiornare i profili Adobe Target direttamente tramite l’API, sia singolarmente che in massa. La funzionalità è simile agli [!DNL Customer Attributes], ma con le seguenti differenze fondamentali:<ul><li>L’API di profilo è una chiamata API REST e [!DNL Customer Attributes] utilizza FTP.</li><li>L’API di profilo di Adobe Target invia dati solo ad Adobe Target invece che all&#39;intero Experience Cloud.</li><li>[!DNL Customer Attributes] fornisce una semplice interfaccia per creare e gestire questi dati esterni.</li></ul> |
| **(Solo per Adobe Target)** Il caricamento dei dati dagli [!DNL Customer Attributes] in Adobe Target estende la durata del profilo del visitatore di Adobe Target? | Sì. Consulta [Durata del profilo del visitatore](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=it) nella Guida di Adobe Target. |
| **(Solo per Adobe Targe)** Posso eseguire il targeting dei dati caricati negli [!DNL Customer Attributes] subito dopo che il visitatore è identificato dall’ID cliente? | Sì. Nella chiamata del server ad Adobe Target, che include l’ID di terze parti mbox, saranno disponibili tutti i dati di Attributi del cliente. |
| **(Solo per Adobe Target)** Cosa rappresenta la colonna **[!UICONTROL Stato di sincronizzazione]** per i file caricati nell’origine Attributi del cliente? | Puoi visualizzare il numero di record pubblicati e sincronizzati da Adobe Target selezionando l’icona Stato di sincronizzazione in corrispondenza di un file di attributi specifico. `Sync %` è una metrica in tempo reale che specifica la percentuale di profili sincronizzati in Adobe Target.<br> **Nota:** la sincronizzazione degli attributi con Adobe Target potrebbe richiedere fino a 24 ore. |
| Cosa rappresentano le metriche di caricamento dei file nell’origine [!DNL Customer Attributes]? | Puoi verificare lo stato degli attributi caricati negli [!DNL Customer Attributes] con l’aiuto delle metriche seguenti: <ul><li>Record: numero di record nel file degli attributi.</li><li>**Nuovi record:** numero di nuovi record presenti nel file degli attributi.</li> <li>**Record aggiornati:** numero di record già presenti negli [!DNL Customer Attributes] con valori aggiornati nel file.</li><li>**Tutti i dati (record):** numero totale di record caricati correttamente in [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}