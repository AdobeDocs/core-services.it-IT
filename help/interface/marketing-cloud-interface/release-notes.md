---
description: Funzionalità, note sulla versione e problemi noti per l’interfaccia Experience Cloud.
keywords: core services
seo-description: Funzionalità, note sulla versione e problemi noti per l’interfaccia Experience Cloud.
seo-title: Note sulla versione cumulative
solution: Experience Cloud
title: Note sulla versione cumulative
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
translation-type: tm+mt
source-git-commit: 1f7672f43e870c7ab66d68f451c031ea2c5af15b
workflow-type: tm+mt
source-wordcount: '3929'
ht-degree: 67%

---


# Note sulla versione cumulative

Funzionalità, note sulla versione e problemi noti per l’interfaccia Experience Cloud.

Per un elenco degli aggiornamenti della documentazione, consulta [Experience Cloud](../doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784).

Per le note sulla versione comprensive di tutte le soluzioni, consulta Note [sulla versione di](https://docs.adobe.com/content/help/it-IT/release-notes/experience-cloud/current.html)Experience Cloud.

## Aprile - 2020

* La pagina [!UICONTROL Feed] di Experience Cloud è stata dichiarata obsoleta. (EXC-8505)
* La pagina di accesso di Experience Cloud è stata aggiornata con nuovi elementi di branding. (EXC-10747)

## Febbraio - 2020

| Funzione | Descrizione |
| -----------| ---------- |
| Admin Tool - visualizza dettagli utente | Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti Experience Cloud e dei relativi dettagli nel nuovo Admin Tool. I dettagli utente includono l’accesso ai prodotti, i ruoli e le informazioni sull’ultimo accesso. Consulta la guida [Admin Tool di Experience Cloud](https://docs.adobe.com/content/help/it-IT/core-services/interface/manage-users-and-products/admin-tool-experience-cloud.html) per ulteriori dettagli. |

**Correzioni**

* **Customer Attributes (Attributi del cliente)**: l&#39;interfaccia utente Customer Attributes (Attributi del cliente) adesso mostra nel target gli stati aggiuntivi di profili sincronizzati. (MCUI-10231)
* **Triggers servizio core:** per mancanza di utilizzo, è stato rimosso il punteggio di propensione &quot;Probabilità di tornare tra 30 giorni&quot; durante la creazione di un trigger di tipo Abandonment (Abbandono). (MCUI-10056)

## Gennaio - 2020

* La pagina Feed è stata rimossa a dicembre 2019. Nel prodotto verrà visualizzato un avviso di funzione rimossa. (MCUI-10039)

## Agosto - 2019

* È stato risolto un problema critico nell’accesso a Experience Cloud che per alcuni utenti causava l’uscita dalla sessione. (MCUI-6908)
* È stato aggiornato l’accesso a Experience Cloud per migliorarne le prestazioni e ridurne la latenza. (MCUI-6854, MCUI-6869, MCUI-6883)
* Sono state apportate modifiche cosmetiche all’interfaccia. (MCUI-6861, MCUI-6911, MCUI-6862)
* È stato risolto un problema a causa del quale la funzione [!UICONTROL Triggers] di Experience Cloud generava un’interpretazione errata della clausola _Like_ nella definizione dell’[!UICONTROL attivatore]. (MCUI-6611)

## Aprile - 2019

* Lo switcher dell’app è stato aggiornato per includere la suite di soluzioni Marketo in Experience Cloud e gli aggiornamenti di branding in Experience Platform. (MCUI-6529)
* La pagina Home di Experience Cloud è stata aggiornata per includere i link di navigazione per le pagine Feed e Amministrazione. (MCUI-6682)
* È stato risolto un problema nella definizione [!UICONTROL Trigger] per l’uso corretto della clausola “like”. (MCUI-6611)
* Sono stati introdotti miglioramenti relativi agli attributi del cliente per migliorare la registrazione nel servizio di abbonamento. (MCUI-6519)

## Rilascio 19.1.1 - 17 gennaio 2019

**Nota:** a marzo 2019, l’interfaccia di Experience Cloud non supporterà Internet Explorer 11.

* È stato risolto un problema che impediva alla ricerca della guida di restituire i risultati. (MCUI-1670)
* Gestione eVar corretta e migliorata negli attivatori. (MCUI-6400)

## Versione 16.5.1 - 26 maggio 2016 {#section_3785F182BC13493F84903CA69EB6D0A8}

**Funzioni e miglioramenti**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Configurazioni di prodotto preconfigurate in Admin Console </p> </td> 
   <td colname="col2"> <p>Gli amministratori di clienti Experience Cloud possono utilizzare configurazioni di prodotto pre-create e mappate a gruppi di autorizzazioni predefiniti per Analytics e Gestione tag dinamica. </p> <p>Questa ottimizzazione è disponibile per le nuove organizzazioni con provisioning e riduce il tempo necessario alle organizzazioni per gestire gli utenti in Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Miglioramento dei feed </p> </td> 
   <td colname="col2"> <p> Quando si crea un nuovo post in Experience Cloud Feed, la riga A ora utilizza l'argomento attualmente attivo al posto dell'organizzazione, come impostazione predefinita.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* È stato risolto un problema che impediva la visualizzazione delle miniature per le risorse condivise da Assets on Demand a Experience Cloud Feed. (MAC-29955)

## Rilascio 16.2 - 18 febbraio 2016 {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti a Experience Cloud Assets </p> </td> 
   <td colname="col2"> <p>In Experience Cloud Assets puoi archiviare, condividere e sincronizzare le risorse digitali da una singola posizione centrale. Experience Cloud Assets sfrutta alcune funzioni disponibili in <span class="keyword">Adobe Experience Manager</span> (AEM). </p> <p>Consulta <a href="../experience-cloud-assets/experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local">Experience Cloud</a></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti al collegamento dell'account </p> </td> 
   <td colname="col2"> <p>È stato migliorato il flusso di lavoro dell'interfaccia per collegare gli account della soluzione con Experience Cloud (Adobe ID). Questo nuovo flusso di lavoro individua tutti gli account dell'utente associati a un'organizzazione e consente di scegliere gli account da collegare. Abbiamo anche semplificato l'esperienza di collegamento dell'account, in modo che non sia più necessario accedere alla pagina Gestisci organizzazioni per collegare manualmente gli account. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* È stato risolto un problema che impediva il collegamento e SSO per Analytics. Questo problema mostrava &quot;Avviso: Messaggio di errore: ERRORE IMS SSO: Impossibile trovare la società collegata.&quot;

**Problema noto**

If you access Dynamic Tag Management via the **[!UICONTROL Experience Cloud]** > **[!UICONTROL Activation]** interface, but your Dynamic Tag Management account is not linked to the Experience Cloud (Adobe ID), you will not be able to log in to Dynamic Tag Management. Per evitare questo problema, accedi direttamente a [!DNL dtm.adobe.com] aprendo una nuova scheda del browser.

## Rilascio 16.1 - 21 gennaio 2016 {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Messaggi Libreria Pubblico </td> 
   <td colname="col2"> <p> Libreria Pubblico è stata migliorata per includere utili messaggi durante la creazione dei destinatari o quando si verifica un timeout. </p> <p>Ad esempio, quando aggiungete più di cinque regole, viene visualizzato un messaggio che indica che avete superato il numero massimo di regole consentito. (MAC-27376, MAC-27375) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft cesserà [il supporto](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) per Internet Explorer 8, 9 e 10. In quanto tale, i problemi segnalati a fronte di tali versioni specifiche di Internet Explorer non verranno corretti.

## Rilascio 15.10 - 14 ottobre 2015  {#section_68123833D3634BD3A473C12862BF9606}

**Problemi noti**

* Gli utenti non sono in grado di accedere a Report Builder se effettuano un&#39;autenticazione unica (SSO) in Analytics tramite Experience Cloud. Questo problema non interessa i clienti che utilizzano credenziali Analytics legacy.
* Errore noto con la funzione &quot;Link to Report&quot; (Collega a report) in Analytics. I clienti che accedono ad Analytics tramite Experience Cloud vengono indirizzati a una pagina di accesso non SSO per Analytics quando cercano di condividere un report.

## Rilascio 15.9 - 10 settembre 2015 {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* È stato risolto un problema di prestazioni dell&#39;API Audience Manager che causava timeout intermittenti durante il caricamento dei dati degli attributi cliente. (MAC-26305)
* È stato risolto un problema che impediva agli utenti di aggiungere fino a 200 attributi cliente a una sottoscrizione. (MAC-26188)
* È stato risolto un problema relativo alla libreria Audience che impediva la condivisione dell&#39;audience dalla segmentazione di Analytics. Questo problema causava la visualizzazione di &quot;Raccolta di dati&quot; (0 audience). Per evitare questo problema, Adobe consiglia di mantenere le dimensioni del segmento al di sotto dei 50 k membri del pubblico per segmento. (MAC-25788)
* È stato risolto un problema precedentemente noto sulla pagina Attributi del cliente - Modifica schema che causava un errore in base al contenuto, che si verificava durante la modifica di un nome visualizzato. (MAC-25589, AN-103834)

## Rilascio 15.7 - 22 luglio 2015  {#section_2683A152176944E48EF6C943892975B7}

* È stato risolto un problema che impediva l&#39;aggiornamento nei report di Analytics delle descrizioni degli attributi specificate nella pagina Visualizza/Modifica schema (in Attributi cliente). (MAC-25985)
* È stato risolto un problema che impediva il rendering delle miniature per le risorse caricate. (MAC-25863)
* È stato risolto un problema che impediva ai nuovi segmenti creati in Reports &amp; Analytics di essere disponibili in Experience Cloud Audiences. (MAC-25817)
* È stato risolto un problema che impediva al pubblico di eseguire condivisioni da Analytics se si utilizzava il servizio ID visitatore. (MAC-25788, MAC-25747)
* È stato aggiunto il supporto per i caratteri multibyte negli attributi del cliente. (MAC-25552)

**Problema noto**

Un problema noto crea la duplicazione di account automaticamente generati in Audience Manager e li collega automaticamente a un&#39;identità Experience Cloud del cliente. Il problema si verifica quando si tenta di passare ad Audience Manager prima di collegare i propri account. Adobe consiglia di collegare gli account Audience Manager a Experience Cloud prima di spostarsi ad Audience Manager. (MAC-25640)

## Rilascio 15.6.1 - 11 giugno 2015  {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

Nessuna informazione disponibile

## Rilascio 15.5.1 - 13 maggio 2015 {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>I menu di navigazione a sinistra sono stati aggiornati e disposti per fornire accesso a tutti i servizi e le soluzioni di base. Le modifiche principali includono: </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">The <span class="term"> Audience Library</span> and <span class="term"> Customer Attributes</span> menu selections are now located under <span class="term"> Audiences</span>. </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4">La selezione del menu <span class="term"> Exchange </span> è stata spostata dal menu a discesa Aiuto nel riquadro di navigazione a sinistra. </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> <span class="term">Soluzioni</span> è stato rimosso. Ora puoi avviare tutte le soluzioni dalla parte inferiore del riquadro di navigazione. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* È stato risolto un problema che impediva la sincronizzazione degli attributi cliente per alcuni clienti.
* Fixed an issue preventing [Adobe Target Product Documentation](https://docs.adobe.com/content/help/it-IT/target/using/integrate/a4t/a4t.translate.html) page from displaying in Japanese.
* È stato risolto un problema che impediva l’utilizzo di testo in giapponese nei commenti tra [!DNL Creative Cloud] e [!DNL Experience Cloud].

## Rilascio 15.4.1 - 8 aprile 2015 {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Miglioramenti dell'amministrazione: </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle"> Admin Console</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">Supporto Enterprise ID e Federated ID </li> 
    </ul> </td> 
   <td colname="col2"> <p>La funzionalità Gestione dei gruppi e degli utenti si trova ora in Admin Console. Il nuovo percorso di navigazione è: </p> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Amministrazione</span> &gt; <span class="uicontrol">Avvia Admin Console</span></p> <p> Inoltre, è stato aggiunto il supporto per Enterprise ID e Federated ID. Potete utilizzare gli Enterprise ID, i Federated ID e l'Adobe ID nella stessa implementazione enterprise. Ad esempio, utilizza gli Adobe ID per gli utenti che possono usare altri prodotti e servizi Adobe. Utilizzate gli Enterprise ID o Federated ID per gli utenti per i quali desiderate gestire rigorosamente i loro account. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* È stato risolto un problema che impediva il Single Sign-On tra [!DNL Experience Cloud] e [!DNL Media Optimizer].

**Problemi noti**

* Il collegamento e lo scollegamento dell’organizzazione Dynamic Tag Management con Experience Cloud non funziona per le nuove organizzazioni Experience Cloud create dall&#39;utente. Stiamo lavorando per risolvere questo problema e ripristinare le normali funzionalità con il rilascio di maggio. Se rilevi dei problemi durante l’accesso single sign-on in Dynamic Tag Management tramite Experience Cloud, utilizza l’accesso precedente all’indirizzo [!DNL dtm.adobe.com].
* Un problema noto sta impedendo la condivisione dell&#39;audience dalle suite di rapporti che non sono di proprietà dell&#39;account Analytics collegato. Stiamo cercando di risolvere il problema

## Rilascio 15.3.2 - 19 marzo 2015 {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Attributi cliente </p> </td> 
   <td colname="col2"> <p>Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Dopo il caricamento dei dati, puoi effettuare i rapporti <span class="uicontrol">Visitor Profile (Profilo visitatore)</span> &gt; <span class="uicontrol">Attributi del cliente</span> in Analytics. </p> <p>Inoltre, puoi utilizzare i dati caricati come segmento del pubblico in <span class="keyword">Adobe Target</span>. </p> <p>Consulta la documentazione del prodotto relativa agli <a href="../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local"> Attributi del cliente</a>. </p> <p> Per informazioni sulla modernizzazione delle soluzioni per i servizi principali, consulta <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Abilitare le soluzioni per i servizi principali</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rilascio 15.3.1 - 4 marzo 2015 {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mappatura gruppo </p> </td> 
   <td colname="col2"> <p>La pagina Gestione dei gruppi è stata riprogettata come un'interfaccia amministrativa che consente di creare gruppi, aggiungere utenti ai gruppi e applicare autorizzazioni nelle soluzioni Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mappatura uno-molti </p> </td> 
   <td colname="col2"> <p>Quando si collegano account di soluzioni Experience Cloud, se si dispone di più soluzioni e organizzazioni, ora è possibile mappare più prodotti e servizi a un'unica organizzazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation </p> </td> 
   <td colname="col2"> <p> <a href="../activation/activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local">Activation</a> ora viene visualizzato nella barra di navigazione a sinistra in <span class="keyword">Experience Cloud</span>. <span class="wintitle"> Activation</span> è un servizio <span class="keyword"> Experience Cloud</span> attualmente caratterizzato dalla tecnologia di gestione tag dinamica e vi indirizza quando viene fatto clic. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aggiornamenti documentazione - Servizi di base </p> </td> 
   <td colname="col2"> <p>Added the topic <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Enable your solutions for core services</a> to assist you with implementing core services. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rilascio 15.2.1 - 19 febbraio 2015 {#section_BC694D5AE16A4E16B44B353ED67947F3}

Correzioni:

* È stato migliorato il flusso di lavoro dell&#39;invito e-mail dell&#39;utente per il provisioning dell&#39;account.
* È stato risolto un problema relativo alla cartella di risorse che impediva alle risorse [!DNL Experience Cloud] e [!DNL Adobe Campaign] di visualizzare gerarchie di cartelle identiche.
* È stato risolto un problema che impediva di eliminare i gruppi di destinazione che facevano parte delle attività di [!DNL Target] disattivate.
* È stato risolto un problema che impediva la visualizzazione dell&#39;icona Aggiungi (simbolo più) in [!UICONTROL Regole] della pagina [!UICONTROL Crea nuovo pubblico].
* È stato migliorato il supporto all&#39;interfaccia di Experience Cloud per Internet Explorer 9.

## Rilascio 15.1.1 - 15 gennaio 2015  {#section_F1A352E928AF432E94CC0A289C345184}

Nuove funzioni, problemi noti e correzioni nella [!DNL Adobe Experience Cloud] collaborazione e nell&#39;interfaccia di condivisione.

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Accesso in sola lettura. </p> </td> 
   <td colname="col2"> <p>Adesso, gli amministratori possono concedere agli utenti non amministratori l'accesso in sola lettura. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* È stato corretto un problema in seguito al quale non era possibile eseguire il rendering dei file PNG su una scheda.
* È stato risolto un problema relativo al caricamento di file in Experience Cloud Assets tramite trascinamento.

**Problemi noti**

* Gli utenti non possono condividere file PowerPoint sulle bacheche.
* Le modifiche apportate a gruppi e adesioni in Gestione utente hanno effetto solo dopo un nuovo accesso.
* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento di file di grosse dimensioni sulle risorse di Experience Cloud.
* Gli utenti potrebbero perdere collegamenti sulle schede Experience Cloud da Media Optimizer.
* Alcuni utenti amministratori potrebbero rilevare dei problemi durante il collegamento degli account dopo l&#39;accettazione di un invito a iscriversi a Experience Cloud.
* L&#39;interfaccia di Experience Cloud può diminuire le prestazioni se usata in parallelo da più utenti.
* Alcuni utenti possono eliminare una vecchia risorsa invece di ricevere una notifica di errore.
* Alcuni utenti potrebbero rilevare dei problemi durante l&#39;accesso in due browser contemporaneamente con lo stesso Adobe ID.
* Alcuni utenti potrebbero non riuscire ad aggiungere nuovamente un utente di Creative Cloud a una cartella condivisa dopo che l&#39;utente di Creative Cloud è stato eliminato.
* Alcuni utenti potrebbero rilevare un ritardo nella notifica che si verifica quando una cartella viene condivisa da Experience Cloud a Creative Cloud.
* Alcuni utenti potrebbero rilevare un problema durante la condivisione di una cartella tra Experience Cloud e Creative Cloud.
* Alcuni utenti potrebbero rilevare dei problemi durante la creazione di un&#39;audience all&#39;interno di una suite di rapporti di Analytics dopo l&#39;abilitazione dell&#39;audience condivisa.
* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento delle risorse su una bacheca.

## Rilascio 14.11.1 - 13 novembre 2014  {#section_A6CF1D4F27B9496892A89C983EB39102}

Problemi noti:

* Alcuni utenti possono eliminare una vecchia risorsa invece di ricevere una notifica di errore.
* Non è possibile eseguire il rendering di alcuni file [!DNL .png] su una scheda.
* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento delle risorse su una bacheca.
* Le modifiche apportate al gruppo e all’adesione nella gestione utente hanno effetto solamente all’accesso successivo.
* Per visualizzare le modifiche apportate alle Impostazioni account, gli amministratori devono disconnettersi e accedere di nuovo.
* Gli utenti non riescono a condividere file di PowerPoint sulle bacheche.
* L&#39;interfaccia di [!DNL Experience Cloud] può diminuire le prestazioni se usata in parallelo da molti utenti.
* La sincronizzazione di Adobe Experience Manager con Creative Cloud non funziona correttamente.

## Rilascio 14.10.1 - 16 ottobre 2014  {#section_E3A0F4423B814707AA3745E083500835}

Nuove funzioni, problemi noti e correzioni nella [!DNL Adobe Experience Cloud] collaborazione e nell&#39;interfaccia di condivisione.

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Modifica autorizzazioni utente </p> </td> 
   <td colname="col2"> <p>I proprietari di una bacheca ora possono modificare le autorizzazioni degli utenti sulla bacheca in questione. </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">Sulla bacheca, fare clic su <span class="uicontrol">Impostazioni</span>. </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">Accanto a ogni proprietario specificare <span class="uicontrol">Proprietario</span>, <span class="uicontrol">Visualizzatore</span> o <span class="uicontrol">Editor</span>. </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* La creazione di una scheda da un PDF e la condivisione sulla bacheca restituivano un messaggio di errore.

**Problemi noti**

* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento delle risorse su una bacheca.
* Non è possibile eseguire il rendering di alcuni file [!DNL .png] su una scheda.
* Le modifiche apportate al gruppo e all’adesione nella gestione utente hanno effetto solamente all’accesso successivo.
* Alcuni utenti potrebbero non essere in grado di creare una scheda da un PDF e di condividerla su una bacheca.
* Alcuni utenti possono eliminare una vecchia risorsa invece di ricevere una notifica di errore.
* Gli utenti non riescono a condividere file di PowerPoint sulle bacheche.
* L&#39;interfaccia di [!DNL Experience Cloud] può diminuire le prestazioni se usata in parallelo da molti utenti.
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].

## Rilascio 14.9.1 - 18 settembre 2014 {#section_20F156A9CC2F4FC59C4970075C181D3A}

**Correzioni e miglioramenti**

* Quando visiti il sito [!DNL experiencecloud.adobe.com], l&#39;esperienza di accesso ora è coerente con l&#39;accesso di Adobe Creative Cloud.
* Nella pagina Gestisci organizzazioni, l&#39;esperienza di collegamento (dopo aver ricevuto un invito) ora è coerente per ogni soluzione.

**Problemi noti**

* Le modifiche apportate al gruppo e all’adesione nella gestione utente hanno effetto solamente all’accesso successivo.
* Alcuni utenti potrebbero non essere in grado di creare una scheda da un PDF e di condividerla su una bacheca.
* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento delle risorse su una bacheca.
* Alcuni utenti possono eliminare una vecchia risorsa invece di ricevere una notifica di errore.
* Gli utenti non riescono a condividere file di PowerPoint sulle bacheche.
* Non è possibile eseguire il rendering di alcuni file [!DNL .png] su una scheda.
* L&#39;interfaccia di [!DNL Experience Cloud] può diminuire le prestazioni se usata in parallelo da molti utenti.
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* Alcuni utenti potrebbero vedere i propri contenuti di [!DNL Creative Cloud] rimossi dalla propria cartella se il contenuto in questione non è condiviso in [!DNL Experience Cloud].

## Rilascio 14.8.1 - 21 agosto 2014 {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

Nuove funzioni, problemi noti e correzioni nella collaborazione [!DNL Adobe Experience Cloud] e nell&#39;interfaccia di condivisione.

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Ora è possibile accedere ad <span class="keyword">Adobe Mobile Services</span> dalla navigazione a sinistra. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi noti**

* Le modifiche apportate al gruppo e all’adesione nella gestione utente hanno effetto solamente all’accesso successivo.
* Alcuni utenti potrebbero non essere in grado di creare una scheda da un PDF e di condividerla su una bacheca.
* Alcuni utenti potrebbero rilevare dei problemi durante il caricamento delle risorse su una bacheca.
* Alcuni utenti potrebbero non riuscire a effettuare l&#39;accesso da [!DNL Target] a [!DNL Experience Cloud].
* Alcuni utenti di Audience Manager non possono effettuare l&#39;accesso a [!DNL Experience Cloud].
* Alcuni utenti possono eliminare una vecchia risorsa invece di ricevere una notifica di errore.
* I file eliminati da [!DNL Experience Cloud] non vengono eliminati da [!DNL Digital Asset Management].
* Gli utenti non riescono a condividere file di PowerPoint sulle bacheche.
* Non è possibile eseguire il rendering di alcuni file [!DNL .png] su una scheda.
* L&#39;interfaccia di [!DNL Experience Cloud] può diminuire le prestazioni se usata in parallelo da molti utenti.
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* Alcuni utenti potrebbero vedere i propri contenuti di [!DNL Creative Cloud] rimossi dalla propria cartella se il contenuto in questione non è condiviso in [!DNL Experience Cloud].

## Rilascio 14.7.1 - 24 luglio 2014 {#section_B22D4F830756463DB27BB4D508D9ADD5}

Nuove funzioni, problemi noti e correzioni nella [!DNL Adobe Experience Cloud] collaborazione e nell&#39;interfaccia di condivisione.

**Problemi noti**

* I file eliminati da [!DNL Experience Cloud] non vengono eliminati da [!DNL Digital Asset Management].
* Alcuni utenti di [!UICONTROL Exchange] potrebbero trovare nei commenti i propri nomi come una lunga stringa ID invece dei loro nomi.
* Non è possibile eseguire il rendering di alcuni file [!DNL .png] su una scheda
* Puoi caricare più file mediante il metodo di caricamento rispetto al trascinamento della selezione. Per risultati ottimali, caricate utilizzando [!UICONTROL Risorse].
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* Gli utenti di [!DNL Exchange] per migliorare la propria esperienza devono cancellare i loro cookie.
* [!DNL Experience Cloud]L&#39;interfaccia di può subire rallentamenti se usata in parallelo da più utenti.
* Alcuni utenti potrebbero vedere i propri contenuti di [!DNL Creative Cloud] rimossi dalla propria cartella se il contenuto in questione non è condiviso in [!DNL Experience Cloud].
* Dopo 15 minuti di inattività verrai disconnesso. La disconnessione in una località comporta anche la disconnessione da [!DNL Experience Cloud].
* Alcuni utenti potrebbero avere dei problemi a collegare i loro account di Audience Manager e a [!DNL Experience Cloud].
* [!UICONTROL Gli utenti di Exchange] possono visualizzare solo l&#39;inglese nel selettore della lingua.

**Correzioni**

Nessuno da segnalare.

## Rilascio 14.6.1 - 19 giugno 2014  {#marketing_cloud_interface}

Nuove funzioni, problemi noti e correzioni nella [!DNL Adobe Experience Cloud] collaborazione e nell&#39;interfaccia di condivisione.

**Miglioramento**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Pulsante <span class="wintitle">Salva</span> in Audiences </p> </td> 
   <td colname="col2"> <p>Quando crei un pubblico, il pulsante <span class="wintitle">Salva</span> presente nella pagina <span class="wintitle">Crea nuovo pubblico</span> rimane disattivato fino a quando tutti i campi obbligatori non sono stati completati. 
     <!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemi noti**

* I file eliminati da [!DNL Experience Cloud] non vengono eliminati da [!DNL Digital Asset Management].
* Puoi caricare più file mediante il metodo di caricamento rispetto al trascinamento della selezione. Per risultati ottimali, caricate utilizzando le risorse.
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* I filtri applicati ai report con tendenze [!DNL Analytics] sono applicati alle schede in [!DNL Experience Cloud].
* Alcuni utenti non possono collegare il loro account di Gestione dell&#39;audience all&#39;account di [!DNL Experience Cloud].
* Dopo 15 minuti di inattività verrai disconnesso. Inoltre, la disconnessione in una località comporta la disconnessione da Experience Cloud.
* Alcuni utenti di Exchange potrebbero trovare nei commenti i propri nomi come una lunga stringa ID invece dei loro nomi.

**Correzioni**

* È stato risolto un problema che impediva il caricamento di video nelle app.

## Rilascio 14.5.1 - 22 maggio 2014  {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Aiuto</span> &gt; <span class="uicontrol">Exchange</span></p> <p><span class="keyword">Experience Cloud</span><span class="wintitle">Exchange</span> è un'unica destinazione in cui è possibile eseguire ricerche, sfogliare, selezionare, pagare e scaricare estensioni Digital Marketing tramite app. </p> <p>Le app includono Data Connectors, configurazioni personalizzate per il prodotto di base di Adobe, applicazioni di terze parti, rapporti e schede di <span class="keyword">Experience Cloud</span>. </p> <p>Consulta <a href="../exchange.md#concept_E07F16F070544B82B56527A845C41D59" format="dita" scope="local"> Marketplace di Exchange</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Audiences </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Audiences</span></p> <p> In <span class="wintitle">Audiences</span> puoi creare, modificare e gestire i diversi tipi di pubblico (o audience), nello stesso modo in cui lavori con i segmenti. Ad esempio, puoi creare un segmento nei reporting e analisi, quindi condividerlo con <span class="wintitle">Experience Cloud</span> <span class="wintitle">Audience</span>. Una volta condiviso, il pubblico è disponibile in <span class="keyword">Adobe Target</span> per attività di campagna e in Adobe Audience Manager per la segmentazione. </p> <p> <p>Nota: per richiedere l’abilitazione in Target, visita <a href="https://www.adobe.com/go/audiences" format="http" scope="external">https://www.adobe.com/go/audiences</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Gli utenti indicati nelle schede di <span class="keyword">Experience Cloud</span> ora dispongono delle autorizzazioni su tali schede. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>I nuovi utenti Adobe possono collegare i loro account Scene7 all’Adobe ID così come i membri del loro team. Gli amministratori possono scollegare gli utenti anche dagli account di Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sincronizzazione delle risorse. </p> </td> 
   <td colname="col2"> <p> Puoi condividere risorse in Adobe Experience Manager (AEM) con Adobe Experience Cloud e Adobe Creative Cloud affinché qualsiasi modifica apportata a tali risorse si riflettano sulle copie condivise delle risorse in Adobe Experience Cloud e Adobe Creative Cloud. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* [!DNL Experience Cloud] non si collegava ad [!DNL Adobe Target]. Questo problema si verificava se l&#39;accesso ad [!DNL Adobe Target] poteva essere usato su più server di [!DNL Target].
* [!DNL Adobe Media Optimizer] non creava gli utenti in maniera automatica quando l&#39;utente veniva creato in [!DNL Experience Cloud].
* Le opzioni nelle caselle combinate utilizzate per aggiungere nuovi utenti scomparivano temporaneamente durante la digitazione.
* Non era possibile fare clic sul collegamento Commenti sulla vista della scheda della risorsa.
* Dopo l’aggiunta di un tag personalizzato a una risorsa, nessun’altra modifica ai metadati era persistente.
* Durante l&#39;eliminazione di un&#39;immagine, il servizio di base delle risorse non avvisa se l&#39;immagine è utilizzata nelle funzioni di base di Adobe Target.
* Prestazione lenta dell&#39;interfaccia [!UICONTROL Experience Cloud] se usata in parallelo da più utenti.
* In caso di eliminazione di un’immagine nelle [!UICONTROL Experience Cloud Assets] non compariva un’avvertenza se l’immagine era utilizzata in [!DNL Adobe Target Essentials].
* Quando **[!UICONTROL Ricorda utente]** non era selezionato durante l&#39;accesso, l&#39;utente veniva scollegato dopo 15 minuti.
* Gli utenti dovevano disconnettersi ed effettuare nuovamente l&#39;accesso per far diventare effettive tutte le modifiche ad autorizzazioni e iscrizioni.
* L&#39;accesso a [!DNL Experience Cloud] durava più di un secondo.
* Per alcuni utenti, l’eliminazione dei file da [!DNL Experience Cloud] non si sincronizzava con [!DNL Digital Asset Management].
* Gli utenti venivano disconnessi dopo soli 15 minuti di inattività del browser.
* Gli utenti non erano in grado di condividere file PowerPoint sulle bacheche.
* Alcuni utenti avevano un layout visivo scadente in Internet Explorer 10 rispetto ad altri browser.

## Rilascio 14.4.1 - 22 aprile 2014  {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Creazione di schede dagli argomenti dell'Aiuto </p> </td> 
   <td colname="col2"> <p>Dopo aver attivato la funzione Condividi su Adobe Experience Cloud nella barra degli strumenti Segnalibri del browser in uso, ora puoi condividere le pagine dell'Aiuto dall'URL del microsito. </p> <p> <b>Condivisione di un argomento della guida</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p>In <span class="keyword">Experience Cloud</span> fai clic su <span class="uicontrol">Amministrazione</span>. </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>Trascina il pulsante <span class="uicontrol">Condividi su Adobe Experience Cloud</span> nella barra degli strumenti Segnalibri. </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>Passa a una pagina dell'Aiuto (o rimani in quella attuale), quindi fai clic su <span class="uicontrol">Condividi su Adobe Experience Cloud</span> presente nella barra degli strumenti Segnalibri. </p> <p>Questo passaggio crea una scheda che puoi visualizzare in <span class="wintitle">Experience Cloud</span>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* Dopo l’aggiunta di un tag personalizzato a una risorsa, non sarà più possibile salvare in modo definitivo nessun’altra modifica ai metadati.
* Gli utenti devono aggiornare la bacheca per far scomparire dalla vista le schede eliminate.
* Quando **[!UICONTROL Ricorda utente]** non era selezionato durante l&#39;accesso, l&#39;utente veniva scollegato dopo 15 minuti.
* La pagina di destinazione della soluzione [!DNL Analytics] ha degli errori di formattazione.
* Gli utenti devono disconnettersi ed effettuare nuovamente l&#39;accesso per far diventare effettive tutte le modifiche ad autorizzazioni e iscrizioni.
* Durante l’eliminazione di un’immagine, il servizio di base delle [!UICONTROL risorse] non avvisa se l’immagine è utilizzata in [!DNL Adobe Target Essentials].
* Non è possibile fare clic sul collegamento Commenti sulla vista della scheda della risorsa.
* Le opzioni in caselle combinate utilizzate per aggiungere nuovi utenti scompaiono temporaneamente durante la digitazione.
* L&#39;accesso a [!DNL Experience Cloud] dura più di un secondo.
* I dati condivisi da [!DNL Media Optimizer] non sono correttamente rappresentati in [!DNL Experience Cloud].
* Adobe [!DNL Media Optimizer] non crea gli utenti in maniera automatica quando l&#39;utente viene creato in [!DNL Experience Cloud].
* Non è possibile collegare [!DNL Experience Cloud] ad [!DNL Adobe Target] se l&#39;accesso ad [!DNL Adobe Target] può essere utilizzato su più server di [!DNL Target].
* [!DNL Experience Cloud]L&#39;interfaccia di può subire rallentamenti se usata in parallelo da più utenti.
* Il collegamento [!DNL Search&Promote] non è disponibile dalla pagina [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* Sulle schede di simulazione di [!DNL Adobe Media Optimizer] non viene eseguito il rendering in maniera corretta.
* I filtri applicati ai report con tendenze [!DNL Analytics] sono applicati alle schede in [!DNL Experience Cloud].
* I filtri applicati ai report con tendenze Analytics sono applicati alle schede in Experience Cloud.
* Non è possibile caricare su una bacheca alcun file Excel o CSV.
* Alcuni utenti non possono collegare il loro account di Gestione dell&#39;audience a [!DNL Experience Cloud].
* Alcuni utenti rilevano degli errori durante la condivisione dei segmenti di [!DNL Analytics] in [!DNL Experience Cloud].
* Alcuni utenti non possono eseguire il drill-down alle sottocartelle in [!UICONTROL Asset Selector (Selettore risorse)].
* Alcuni utenti non possono condividere gadget AdLens in [!DNL Experience Cloud].

## Rilascio 14.3.1 - 13 marzo 2014 {#section_5D142E3225E3477A84DC01B8197D39BC}

La versione 14.3.1 è una versione di manutenzione che si concentra su velocità, stabilità e sicurezza. Non include le nuove funzioni principali.

**Correzioni**

* Aggiunta la possibilità di rimuovere l&#39;immagine avatar.
* È stato risolto un problema che impediva lo scollegamento dagli account di [!DNL Adobe Media Optimizer].

**Problemi noti**

* Durante l&#39;eliminazione di un&#39;immagine in Experience Cloud Assets non compare alcun avviso se l&#39;immagine è utilizzata nelle funzioni di base di Adobe Target.
* Durante l&#39;aggiornamento di una scheda da [!DNL Analytics] è possibile visualizzare, a volte, un grafico vuoto nella scheda espansa.
* Gli utenti devono disconnettersi ed effettuare nuovamente l&#39;accesso per far diventare effettive tutte le modifiche ad autorizzazioni e iscrizioni.
* Se *`Remember me`* non è selezionato durante l’accesso, l’utente verrà disconnesso dopo 15 minuti.
* La pagina di destinazione della soluzione [!DNL Analytics] ha degli errori di formattazione.
* Non è possibile fare clic sul collegamento Commenti sulla vista della scheda della risorsa.
* L&#39;interfaccia di Experience Cloud può subire rallentamenti se usata in parallelo da più utenti.
* Non è possibile collegare [!DNL Adobe Target]Experience Cloud ad [!DNL Adobe Target] se l&#39;accesso ad può essere utilizzato su più server di Target.
* L&#39;accesso a Experience Cloud dura più di un secondo.
* Dopo l’aggiunta di un tag personalizzato a una risorsa, non sarà più possibile salvare in modo definitivo nessun’altra modifica ai metadati.
* [!DNL Adobe Media Optimizer] non crea gli utenti in maniera automatica quando l&#39;utente viene creato in Experience Cloud.
* Le opzioni in caselle combinate utilizzate per aggiungere nuovi utenti scompaiono temporaneamente durante la digitazione.
* I dati condivisi da [!DNL Media Optimizer] non sono correttamente rappresentati in Experience Cloud.
* La condivisione di immagini di Flickr non viene eseguita correttamente.
* I filtri applicati ai report con tendenze [!DNL Analytics] sono applicati alle schede in Experience Cloud.
* Le modifiche apportate al gruppo e all’adesione nella gestione utente hanno effetto solamente all&#39;accesso successivo.
* Il collegamento [!DNL Search&Promote] non è disponibile da [!UICONTROL Organizations &amp; Product Access (Organizzazione e accesso ai prodotti)].
* L&#39;utente deve aggiornare la bacheca per far scomparire dalla vista le schede eliminate.
* Non è possibile caricare su una bacheca alcun file Excel o CSV.
* Sulle schede di simulazione di [!DNL Adobe Media Optimizer] non viene eseguito il rendering in maniera corretta.
* Non è possibile eseguire il rendering di alcuni file PNG su una scheda.
* Non è possibile inviare feedback beta.

## Rilascio 14.2.1 - 24 febbraio 2014  {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>OEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aggiorna dati </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->L'icona <span class="uicontrol">Aggiorna dati</span> per un grafico su una scheda ora è nascosta se la soluzione non consente l'aggiornamento dei dati. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correzioni**

* È stato risolto un problema che impediva l&#39;applicazione di filtri si segmenti di rapporti condivisi di [!DNL Analytics].
* È stato risolto un problema che causava la visualizzazione della pagina [!UICONTROL Soluzioni Experience Cloud] come collegata, anche se gli account delle soluzioni non erano collegati.
* È stato risolto un problema che impediva ai clienti di [!DNL Adobe Target] in Asia di fare clic sul pulsante **[!UICONTROL Continua su Experience Cloud]** presente nella pagina di collegamento.
* È stato risolto un problema che impediva la condivisione di video di YouTube.
