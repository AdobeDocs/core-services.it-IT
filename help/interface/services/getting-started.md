---
description: Abilita le applicazioni Adobe Analytics e Adobe Target per i servizi tra più applicazioni. Scopri come iniziare a utilizzare i servizi Experience Cloud.
solution: Experience Cloud
title: Guida introduttiva ai servizi Experience Cloud
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: ddb3bc39e3b8d9b96de7602e29b3b7acddd6ed52
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 78%

---

# Guida introduttiva ai servizi Experience Cloud

Se hai implementato Experience Cloud di recente utilizzando i tag di Experience Platform, disponi già della configurazione per gli attributi del cliente e i tipi di pubblico di Experience Cloud. Inoltre puoi gestire utenti e prodotti in Admin Console.

I clienti esistenti possono modernizzare l’esecuzione delle applicazioni e implementare Experience Cloud. In questo modo puoi utilizzare gli attributi del cliente e le funzioni relative al pubblico in Adobe Analytics, Audience Manager e Adobe Target.

## Partecipazione a Experience Cloud per diventare un amministratore

Come partecipare a Experience Cloud:

1. Verifica di disporre degli SKU Adobe Analytics o Adobe Target appropriati.

   * **Adobe Analytics:** Standard o Premium (non lo SKU legacy di [!DNL SiteCatalyst]).
   * **Adobe Target:** Standard o Premium.

   >[!NOTE]
   >
   >Ad [!DNL Target] esempio, effettua la migrazione a at.js da `mbox.js`. Consulta [Aggiornamento da at.js 1. x a at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=it).

1. Gestire utenti e prodotti in [!UICONTROL Admin Console].

### Accesso amministratore

Se hai il ruolo di amministratore, puoi accedere da [experience.adobe.com](https://experience.adobe.com).

Il collegamento **[!UICONTROL Admin Console]** è disponibile nella navigazione del menu di Experience Cloud.

### Accesso utente

Per accedere a Experience Cloud, gli utenti devono:

* Disporre di un Adobe ID (o Enterprise ID per l’azienda).
* Accedi da [experience.adobe.com](https://experience.adobe.com).
* Appartenere a un gruppo di applicazioni mappato su un gruppo aziendale.
* Se necessario, collega gli account applicazione al rispettivo Adobe ID (procedura descritta di seguito).

### Facoltativo: collega gli account utente esistenti.

Probabilmente alcuni utenti sono già membri di gruppi di applicazioni, ad esempio di un gruppo Analytics che hai precedentemente gestito in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

Quando mappi questi gruppi ai gruppi aziendali Experience Cloud, gli utenti devono collegare manualmente le credenziali del propio account applicazione al rispettivo Adobe ID.

Consulta [Collegare glu account in Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations)

>[!NOTE]
>
>Dopo aver mappato gruppi aziendali e di applicazioni, i nuovi utenti sono automaticamente collegati. Le credenziali della soluzione vengono create e collegate automaticamente al relativo Adobe ID.

Le sezioni seguenti descrivono come poter modernizzare l&#39;implementazione. La modernizzazione dell’implementazione abilita i servizi core in Experience Cloud.

## Implementare [!UICONTROL Experience Cloud ID Service]

[!UICONTROL Experience Cloud ID Service] fornisce un ID comune per l&#39;integrazione tra più applicazioni. Fornisce l&#39;identificazione dei visitatori tra domini, oltre a un percorso per il targeting e la personalizzazione tra dispositivi e browser basati sui dati CRM caricati tramite [!DNL Customer Attributes].

Il metodo più semplice per abilitare i servizi core di Experience Cloud è quello di attivarli automaticamente per Analytics e Adobe Target tramite l&#39;[estensione del servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) in [!UICONTROL Experience Platform Launch].

Per ricevere assistenza completa sul servizio Experience Cloud ID (già ID visitatore), visita [qui](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html#intro).

**Non Utilizzo Di [!UICONTROL Experience Platform tags]?**

Se non utilizzi [!UICONTROL Experience Platform tags], implementa manualmente il servizio ID tramite la distribuzione JavaScript (`VisitorAPI.js`), come segue:

| Attività | Descrizione |
|--- |--- |  
| [Implementazione del servizio Experience Cloud ID per Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview) | Adobe consiglia inoltre di impostare [ID cliente](https://experienceleague.adobe.com/en/docs/id-service/using/reference/authenticated-state) aggiuntivi. Tali ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future di base di Experience Cloud. |
| Aggiorna il file `s_code` esistente alla versione H.27.3 o successiva oppure il file `AppMeasurement.js` esistente alla versione 1.4 o successiva. | Tali file sono disponibili per il download in [Gestore codice](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html) in Strumenti amministratore di Analytics. Puoi consultare la [Guida all&#39;implementazione JavaScript](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview#js) per ulteriori informazioni su `AppMeasurement.js`. |

{style="table-layout:auto"}

### Analytics &amp; Adobe Target - Sincronizzazione dell&#39;ID cliente

In qualità di parte dell&#39;impostazione del servizio Experience Cloud ID, Adobe consiglia per Analytics e [!DNL Target] la sincronizzazione degli [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) con Experience Cloud.

In Adobe Target, `mbox3rdpartyid` deve ottenere l’ID cliente e inviarlo a [!DNL Target]. (Vedi [Utilizzo degli attributi del cliente](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) in [!DNL Target].)

Quando un visitatore si autentica sul tuo sito web, o in generale si identifica, l’implementazione deve esporne l’ID cliente del sistema CRM nella pagina o nell’applicazione. Puoi quindi utilizzare la funzionalità appropriata per sincronizzare l’ID cliente a Experience Cloud. La sincronizzazione archivia l’ID cliente CRM del visitatore in Experience Cloud e attiva gli attributi cliente per l’utilizzo in Experience Cloud.

Ad esempio, si supponga che Bob sia associato all&#39;ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiamando `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante il servizio ID visitatore. oppure
* Popolare il *`Customer ID (52mc210tr42)`* in una prop o eVar.

L&#39;ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l&#39;ID cliente.

#### Analytics: sincronizzazione dell’ID cliente con il metodo di retrocompilazione di Data Warehouse

Quando gli attributi del cliente sono diventati disponibili per la prima volta, alcuni clienti non avevano ancora implementato il servizio Experience Cloud ID e non potevano utilizzare facilmente gli attributi del cliente. Per contribuire a ovviare a questo problema, Adobe ha creato un mezzo per eseguire una retrocompilazione delle sincronizzazioni ID utilizzando il Data Warehouse di Adobe Analytics. Questa funzione è nota come retrocompilazione di Data Warehouse. Generalmente, la retrocompilazione di Data Warehouse non è necessaria e di conseguenza non sarà più disponibile a partire da ottobre 2022.


### SDK per dispositivi mobili

Consulta la sezione su *Experience Cloud ID Service* per esempi di sintassi per l’impostazione di ID cliente aggiuntivi nelle applicazioni mobili [Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=it) e [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=it).

### Abilitazione degli attributi per i dati presenti nella cronologia

I dati dell&#39;attributo del cliente sono disponibili dopo l&#39;accesso dei visitatori. Se non hai ancora implementato ID Service e se stai tenendo traccia della cronologia degli ID cliente in una prop o eVar, puoi richiedere un processo che invia gli accessi cronologici a Experience Cloud. Tale procedimento consente di iniziare a usare gli attributi del cliente immediatamente.

Contatta l’Assistenza clienti per abilitare i dati presenti nella cronologia.

## Mappare le suite di rapporti per un’organizzazione Experience Cloud

>[!NOTE]
>
>La funzionalità di mappatura di suite di rapporti è diventata obsoleta a novembre 2020. Per eventuali domande, rivolgiti al servizio di assistenza clienti.

I servizi di Experience Cloud (come Experience Cloud ID) sono associati a una suite di rapporti di un&#39;organizzazione Experience Cloud, anziché a una sola suite di rapporti di Analytics. Per garantire il corretto funzionamento di questi servizi, ogni suite di rapporti di Analytics deve essere mappata a un&#39;organizzazione Experience Cloud.

## Aggiornamento del codice AppMeasurement di Analytics

Se stai utilizzando cookie di terze parti, fai riferimento a [CNAME e servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html) per informazioni sulla raccolta dei dati CNAME e sul tracciamento tra domini.

Si consiglia di modernizzare l&#39;implementazione di Analytics aggiornando le librerie JavaScript, incluso l&#39;API visitatore. Un modo semplice per eseguire questa operazione è aggiungere un’[estensione Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html) nella funzionalità di Raccolta dati di Experience Platform.

## Aggiornamento dell’implementazione di Adobe Target

* È consigliabile aggiungere un&#39;estensione [Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html) nei tag [!UICONTROL Experience Platform] in modo che il recupero della libreria sia automatico. Puoi anche impostare l&#39;estensione del servizio [Experience Cloud ID](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) per Adobe Target (e altre applicazioni) utilizzando i tag [!UICONTROL Experience Platform]. È necessario l&#39;aggiornamento [!UICONTROL Experience Cloud ID Service] di **&#x200B;**&#x200B;affinché Adobe Target possa utilizzare i servizi People.
* Se non utilizzi i tag [!UICONTROL Experience Platform], [aggiorna manualmente la libreria mbox](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html).
* Richiedi l’accesso per utilizzare Adobe Analytics come origine di reporting per [!DNL Adobe Target]. I dati di [!DNL Target] e [!DNL Analytics] sono combinati nella stessa chiamata al server durante l’elaborazione affinché i visitatori siano collegati tra le due applicazioni. Consulta [Implementazione di Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html).

  >[!IMPORTANT]
  >
  >Tutti i clienti Analytics dispongono già del provisioning per i servizi di base, come Attributi del cliente. Se non sei cliente Analytics, contatta l&#39;Assistenza clienti per richiedere il provisioning.

## Verificare l’implementazione

Utilizza il seguente procedimento per assicurarti che il Servizio Experience Cloud ID sia correttamente implementato sul tuo sito.

1. Elimina i cookie dal sito in uso in modo da poter visualizzare la richiesta a Experience Cloud ID Service (la richiesta viene effettuata alla prima visita, quindi una volta a settimana per ciascun visitatore).
1. Utilizzando un analizzatore di pacchetti o il pannello di rete in un debugger del browser web, cerca una richiesta indirizzata a [!DNL dpm.demdex.net].
1. Verifica che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verifica che la richiesta di Analytics contenga il parametro `mid` (Experience Cloud ID). Nel periodo di prova (se disponibile) dovrebbe essere visibile un parametro `aid` (l&#39;ID visitatore di Analytics).

Risposta prevista contenente Experience Cloud ID:

![Risposta prevista contenente l’ID Experience Cloud](../assets/mac_id_response.png)

Richiesta immagine di Analytics contenente l’ID Experience Cloud (noto anche come `mid` o _ID visitatore_):

![Richiesta immagine di Analytics contenente l’ID Experience Cloud](../assets/mid.png)

ID Experience Cloud nella richiesta mbox:

![ID Experience Cloud nella richiesta mbox](../assets/mbox_request.png)

### Cos&#39;è il periodo di prova?

Dopo la distribuzione del servizio ID Experience Cloud, i nuovi visitatori non ricevono più un Experience Cloud ID di Analytics dal server di raccolta dati. Se il Servizio ID non è stato ancora implementato nelle sezioni del sito, quando i visitatori accedono a tali sezioni, l&#39;Experience Cloud ID non viene riconosciuto e ai visitatori viene assegnato un ID visitatore Analytics legacy. Ciò può causare potenziali problemi, incluse visite duplicate e attribuzioni non corrette.

Ad esempio, se la sezione di assistenza del sito viene gestita in un CMS separato, dovresti avere un file JavaScript di Analytics separato per tale sezione. Se implementi Experience Cloud ID sul sito principale prima di aver distribuito il servizio ID al sito di assistenza, i nuovi visitatori riceveranno un ID legacy di Analytics al momento della visita della sezione di assistenza e le visite che si estendono a entrambe le sezioni saranno riportate come visite diverse.

La distribuzione di Experience Cloud ID Service su siti che utilizzano più file JavaScript o altre tecnologie (come Flash) può causare problemi di coordinazione. Questi problemi si verificano perché devi abilitare Experience Cloud ID Service su tutte le parti del sito contemporaneamente. Configurando un periodo di tolleranza, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID e possono essere identificati correttamente nelle sezioni del sito che non sono state aggiornate per l’uso del servizio ID.

## Gestione di utenti e prodotti

Quando è tutto pronto, passa a [Admin Console](https://adminconsole.adobe.com/) per gestire gli utenti e i profili di prodotto.

![Accedere ad Admin Console](../assets/menu-administration-shell.png)

### Attributi del cliente

Gli utenti aggiunti al gruppo [!DNL Customer Attributes] possono visualizzare la voce di menu [!DNL Customer Attributes] sul lato sinistro di Experience Cloud.

## Inizio della condivisione dei dati degli attributi e dei tipi di pubblico

Utilizza le seguenti funzionalità.

### [!UICONTROL Customer attributes]

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in un’origine dati di attributi cliente in Experience Cloud. Una volta caricati, puoi usare i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Per ulteriori informazioni, consulta [attributi cliente](https://experienceleague.adobe.com/en/docs/core-services/interface/services/customer-attributes/attributes).

### [!UICONTROL People] > [!UICONTROL Audience Library]

Experience Cloud [!UICONTROL Audiences] è l&#39;interfaccia che consente di creare tipi di pubblico, o audience, combinare quelli esistenti per creare un pubblico composito e visualizzare quelli condivisi.

Per ulteriori informazioni, consulta [Tipi di pubblico](https://experienceleague.adobe.com/en/docs/core-services/interface/services/audiences/overview).

## Archivio dei dati e informativa sulla privacy

L’utilizzo dei servizi di profilazione del pubblico in tempo reale e altri servizi core in Adobe [!DNL Experience Cloud] potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché [!DNL Experience Cloud] utilizza Audience Manager, i dati utilizzati nel servizio [!UICONTROL People] devono trovarsi nei server di Audience Manager negli Stati Uniti.

Quando si utilizzano i servizi resi disponibili tramite il servizio [!UICONTROL People], i tipi di dati inviati da altri prodotti Adobe a Gestione dell&#39;audience sono:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l&#39;indirizzo IP, incluso l&#39;ultimo ottetto dell&#39;IP (partendo dal presupposto che l&#39;indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell&#39;IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base a regole impostate in Audience Manager.
* (Facoltativo) Uno o più degli ID. In base al tipo di implementazione del servizio ID, puoi effettuare invii mediante uno o più degli ID, come ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti a al modulo Gestione del pubblico di Adobe. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Consiglia invece di utilizzare hash univoci per mascherare i dati prima di inviarli ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. Il cookie di prime parti `AMCV_###@AdobeOrg` è sempre impostato con il servizio Experience Cloud ID.

Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia tali dati negli Stati Uniti. Audience Manager non fornisce un&#39;opzione per archiviare o elaborare tali dati al di fuori degli Stati Uniti.

