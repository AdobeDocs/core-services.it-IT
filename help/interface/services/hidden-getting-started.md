---
description: Abilita le applicazioni Adobe Analytics e Adobe Target per i servizi tra più applicazioni. Scopri come iniziare a utilizzare i servizi CX Enterprise.
solution: Experience Cloud
title: Guida introduttiva ai servizi Experience Cloud
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: '2092'
ht-degree: 46%

---

# Guida introduttiva ai servizi aziendali CX

Se CX Enterprise è stato implementato di recente utilizzando i tag di Experience Platform, significa che è già stata impostata la funzione Attributi del cliente e tipi di pubblico aziendali di CX. Inoltre puoi gestire utenti e prodotti in Admin Console.

I clienti esistenti possono modernizzare le implementazioni delle applicazioni e implementare CX Enterprise. In questo modo puoi sfruttare le funzioni Attributi del cliente e tipi di pubblico in Adobe Analytics, Audience Manager e Adobe Target.

## Partecipazione a CX Enterprise per diventare un amministratore {#section_2423F0BD3DF642658103310EE5EA6154}

Come partecipare a CX Enterprise:

1. Verifica di disporre degli SKU Adobe Analytics o Adobe Target appropriati.

   * **Adobe Analytics:** Standard o Premium (non lo SKU legacy di [!DNL SiteCatalyst]).
   * **Adobe Target:** Standard o Premium.

   >[!NOTE]
   >
   >Ad [!DNL Target] esempio, effettua la migrazione a at.js da `mbox.js`. Consulta [Aggiornamento da at.js 1. x in at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=it).

1. Gestire utenti e prodotti in [!UICONTROL Admin Console].

### Accesso amministratore

Se hai il ruolo di amministratore, puoi accedere da [experience.adobe.com](https://experience.adobe.com).

Il collegamento **[!UICONTROL Admin Console]** è disponibile nel menu di navigazione di CX Enterprise.

### Accesso utente

Per accedere a CX Enterprise, gli utenti devono:

* Disporre di un Adobe ID (o Enterprise ID per l’azienda).
* Accedi da [experience.adobe.com](https://experience.adobe.com).
* Appartenere a un gruppo di applicazioni mappato su un gruppo aziendale.
* Se necessario, collega gli account applicazione al rispettivo Adobe ID (procedura descritta di seguito).

### Facoltativo: collega gli account utente esistenti.

Probabilmente alcuni utenti sono già membri di gruppi di applicazioni, ad esempio di un gruppo Analytics che hai precedentemente gestito in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

Quando si mappano questi gruppi ai gruppi aziendali CX Enterprise, gli utenti devono collegare manualmente le credenziali dell&#39;account dell&#39;applicazione al proprio Adobe ID.

Visualizza [Collega account in CX Enterprise](../administration/organizations.md)

>[!NOTE]
>
>Dopo aver mappato gruppi aziendali e di applicazioni, i nuovi utenti sono automaticamente collegati. Le credenziali della soluzione vengono create e collegate automaticamente al relativo Adobe ID.

Le sezioni seguenti descrivono come poter modernizzare l&#39;implementazione. La modernizzazione dell&#39;implementazione abilita i servizi principali in CX Enterprise.

## Implementare [!UICONTROL CX Enterprise ID Service] {#section_3C9F6DF37C654D939625BB4D485E4354}

[!UICONTROL CX Enterprise ID Service] fornisce un ID comune per l&#39;integrazione tra più applicazioni. Fornisce l&#39;identificazione dei visitatori tra domini, oltre a un percorso per il targeting e la personalizzazione tra dispositivi e browser basati sui dati CRM caricati tramite [!DNL Customer Attributes].

Il metodo più semplice per abilitare i servizi core CX Enterprise è quello di attivarli automaticamente per Analytics e Adobe Target tramite l&#39;[estensione del servizio CX Enterprise ID](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=it) in [!UICONTROL Experience Platform Launch].

Per ricevere la guida completa sul servizio CX Enterprise ID (già ID visitatore), vai [qui](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it#intro).

**Non Utilizzo Di [!UICONTROL Experience Platform tags]?**

Se non utilizzi [!UICONTROL Experience Platform tags], implementa manualmente il servizio ID tramite la distribuzione JavaScript (`VisitorAPI.js`), come segue:

| Attività | Descrizione |
| -----------| ---------- |
| [Implementazione del servizio CX Enterprise ID per Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=it) | Adobe consiglia inoltre di impostare [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=it) aggiuntivi. Questi ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future di CX Enterprise. |
| Aggiorna il file `s_code` esistente alla versione H.27.3 o successiva oppure il file `AppMeasurement.js` esistente alla versione 1.4 o successiva. | Tali file sono disponibili per il download in [Gestore codice](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=it) in Strumenti amministratore di Analytics. Puoi consultare la [Guida all&#39;implementazione JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=it#js) per ulteriori informazioni su `AppMeasurement.js`. |

{style="table-layout:auto"}

### Analytics &amp; Adobe Target - Sincronizzazione dell&#39;ID cliente {#section_AD473A6A21C1446498E700363F9A8437}

In qualità di parte dell&#39;impostazione del servizio CX Enterprise ID, Adobe consiglia per Analytics e [!DNL Target] di sincronizzare i [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=it) con CX Enterprise.

In Adobe Target, `mbox3rdpartyid` deve ottenere l’ID cliente e inviarlo a [!DNL Target]. Consulta [Uso degli attributi del cliente](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=it) in [!DNL Target].

Quando un visitatore si autentica sul tuo sito web, o in generale si identifica, l’implementazione deve esporne l’ID cliente del sistema CRM nella pagina o nell’applicazione. È quindi possibile utilizzare la funzione appropriata per sincronizzare l&#39;ID cliente a CX Enterprise. Questa sincronizzazione memorizza l&#39;ID cliente CRM del visitatore in CX Enterprise e attiva gli attributi del cliente per l&#39;utilizzo in CX Enterprise.

Ad esempio, si supponga che Bob sia associato all&#39;ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiamando `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante il servizio ID visitatore. oppure
* Popolare il *`Customer ID (52mc210tr42)`* in una prop o eVar.

L&#39;ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l&#39;ID cliente.

#### Analytics: sincronizzazione dell’ID cliente con il metodo di retrocompilazione di Data Warehouse

Quando gli attributi del cliente sono diventati disponibili per la prima volta, alcuni clienti non avevano ancora implementato il servizio CX Enterprise ID e non potevano utilizzare facilmente gli attributi del cliente. Per contribuire a ovviare a questo problema, Adobe ha creato un mezzo per eseguire una retrocompilazione delle sincronizzazioni ID utilizzando il Data Warehouse di Adobe Analytics. Questa funzione è nota come retrocompilazione di Data Warehouse. Generalmente, la retrocompilazione di Data Warehouse non è necessaria e di conseguenza non sarà più disponibile a partire da ottobre 2022.


### SDK per dispositivi mobili

Consulta la sezione *Servizio CX Enterprise ID* per esempi di sintassi per l&#39;impostazione di ID cliente aggiuntivi nelle [applicazioni mobili Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=it) e [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=it).

### Abilitazione degli attributi per i dati presenti nella cronologia

I dati dell&#39;attributo del cliente sono disponibili dopo l&#39;accesso dei visitatori. Se non hai ancora implementato il servizio ID e se stai tenendo traccia degli ID cliente in una prop o eVar, puoi richiedere un processo che invia gli accessi cronologici a CX Enterprise. Questo processo ti consente di iniziare a utilizzare Attributi del cliente immediatamente.

Contatta l&#39;Assistenza clienti per abilitare i dati presenti nella cronologia.

## Mappatura di suite di rapporti per un&#39;organizzazione CX Enterprise {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>La funzionalità di mappatura di suite di rapporti è diventata obsoleta a novembre 2020. Per eventuali domande, rivolgiti al servizio di assistenza clienti.

I servizi aziendali CX (come il servizio CX Enterprise ID) sono associati a una suite di rapporti aziendale CX anziché a una sola suite di rapporti Analytics. Per garantire il corretto funzionamento di questi servizi, ogni suite di rapporti di Analytics deve essere mappata su un&#39;organizzazione CX Enterprise.

## Aggiornamento del codice AppMeasurement di Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Se stai utilizzando cookie di prime parti, fai riferimento a [CNAME e al servizio CX Enterprise ID](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=it) per informazioni sui CNAME per la raccolta dati e sul tracciamento tra domini.

Si consiglia di modernizzare l&#39;implementazione di Analytics aggiornando le librerie JavaScript, incluso l&#39;API visitatore. Un modo semplice per eseguire questa operazione è aggiungere un’[estensione Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=it) nella funzionalità di Raccolta dati di Experience Platform.

## Aggiornamento dell’implementazione di Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* È consigliabile aggiungere un&#39;estensione [Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html?lang=it) nei tag [!UICONTROL Experience Platform] in modo che il recupero della libreria sia automatico. È inoltre possibile impostare l&#39;estensione del servizio [CX Enterprise ID](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=it) per Adobe Target (e altre applicazioni) utilizzando i tag [!UICONTROL Experience Platform]. È necessario l&#39;aggiornamento **di [!UICONTROL CX Enterprise ID Service]** affinché Adobe Target possa utilizzare i servizi People.
* Se non utilizzi i tag [!UICONTROL Experience Platform], [aggiorna manualmente la libreria mbox](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html?lang=it).
* Richiedi l’accesso per utilizzare Adobe Analytics come origine di reporting per [!DNL Adobe Target]. I dati di [!DNL Target] e [!DNL Analytics] sono combinati nella stessa chiamata al server durante l’elaborazione affinché i visitatori siano collegati tra le due applicazioni. Consulta [Implementazione di Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=it).

  >[!IMPORTANT]
  >
  >Tutti i clienti Analytics dispongono già del provisioning per i servizi principali quali Attributi del cliente. Se non sei cliente Analytics, contatta l&#39;Assistenza clienti per richiedere il provisioning.

## Verificare l’implementazione {#section_E641782A0F4F44AF8C9C91216BE330D5}

Attenersi alla procedura seguente per assicurarsi che il servizio CX Enterprise ID sia correttamente implementato sul sito.

1. Elimina i cookie dal sito in uso in modo da poter visualizzare la richiesta al servizio CX Enterprise ID (la richiesta viene effettuata alla prima visita, quindi una volta a settimana per ciascun visitatore).
1. Utilizzando un analizzatore di pacchetti o il pannello di rete in un debugger del browser web, cerca una richiesta indirizzata a [!DNL dpm.demdex.net].
1. Verifica che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verificare che la richiesta di Analytics contenga il parametro `mid` (CX Enterprise ID). Nel periodo di prova (se disponibile) dovrebbe essere visibile un parametro `aid` (l&#39;ID visitatore di Analytics).

Risposta prevista contenente CX Enterprise ID:

![Risposta prevista contenente CX Enterprise ID](../assets/mac_id_response.png)

Richiesta immagine di Analytics contenente CX Enterprise ID (noto anche come `mid` o _ID visitatore_):

![Richiesta immagine di Analytics contenente CX Enterprise ID](../assets/mid.png)

CX Enterprise ID nella richiesta mbox:

![CX Enterprise ID nella richiesta mbox](../assets/mbox_request.png)

### Cos&#39;è il periodo di prova?

Dopo aver implementato il servizio CX Enterprise ID, i nuovi visitatori non ricevono più un Enterprise ID CX di Analytics dal server di raccolta dati. Se il Servizio ID non è stato ancora implementato nelle sezioni del sito, quando i visitatori accedono a tali sezioni, l&#39;Enterprise ID CX non viene riconosciuto e ai visitatori viene assegnato un ID visitatore Analytics legacy. Ciò può causare potenziali problemi, incluse visite duplicate e attribuzioni non corrette.

Ad esempio, se la sezione di assistenza del sito viene gestita in un CMS separato, dovresti avere un file JavaScript di Analytics separato per tale sezione. Se distribuisci CX Enterprise ID sul sito principale prima di distribuire il servizio ID al sito di assistenza, i nuovi visitatori riceveranno un ID legacy di Analytics al momento della visita della sezione di assistenza. Le visite che si estendono su entrambe le sezioni del sito vengono riportate come visite diverse.

L&#39;implementazione del servizio CX Enterprise ID in siti che utilizzano più file JavaScript o altre tecnologie (come Flash) può causare problemi di coordinazione. Questi problemi si verificano perché è necessario attivare il servizio CX Enterprise ID su tutte le parti del sito contemporaneamente. Configurando un periodo di tolleranza, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID. I visitatori possono essere identificati in modo coerente nelle sezioni del sito che non sono state aggiornate per utilizzare il servizio ID visitatore.

## Gestione di utenti e prodotti {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Quando è tutto pronto, passa a [Admin Console](https://adminconsole.adobe.com/) per gestire gli utenti e i profili di prodotto.

![Accedere ad Admin Console](../assets/menu-administration-shell.png)

### Attributi cliente

Gli utenti aggiunti al gruppo [!DNL Customer Attributes] possono visualizzare la voce di menu [!DNL Customer Attributes] sul lato sinistro di CX Enterprise.

## Inizio della condivisione dei dati degli attributi e dei tipi di pubblico {#section_960C06093623462E8EA247B3E97274A1}

Utilizza le seguenti funzionalità.

### [!UICONTROL Customer Attributes]

Se si acquisiscono dati di clienti aziendali in un database CRM (Customer Relationship Management), è possibile caricarli in un&#39;origine dati di attributi cliente in CX Enterprise. Una volta caricati, puoi usare i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Per ulteriori informazioni, consulta [Attributi del cliente](customer-attributes/attributes.md).

### [!UICONTROL People] > [!UICONTROL Audience Library]

CX Enterprise [!UICONTROL Audiences] è l&#39;interfaccia che consente di creare tipi di pubblico, o audience, combinare quelli esistenti per creare un pubblico composito e visualizzare quelli condivisi.

Per ulteriori informazioni, consulta [Tipi di pubblico](audiences/overview.md).

## Archivio dei dati e informativa sulla privacy

L’utilizzo dei servizi di profilazione del pubblico in tempo reale e altri servizi core in Adobe [!DNL CX Enterprise] potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché [!DNL CX Enterprise] utilizza Audience Manager, i dati utilizzati nel servizio [!UICONTROL People] devono trovarsi nei server di Audience Manager negli Stati Uniti.

Quando si utilizzano i servizi resi disponibili tramite il servizio [!UICONTROL People], i tipi di dati inviati da altri prodotti Adobe a Gestione dell&#39;audience sono:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l&#39;indirizzo IP, incluso l&#39;ultimo ottetto dell&#39;IP (partendo dal presupposto che l&#39;indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell&#39;IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base a regole impostate in Audience Manager.
* (Facoltativo) Uno o più degli ID. In base al tipo di implementazione del servizio ID, puoi effettuare invii mediante uno o più degli ID, come ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti a al modulo Gestione del pubblico di Adobe. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Consiglia invece di utilizzare hash univoci per mascherare i dati prima di inviarli ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. Il cookie di prime parti `AMCV_###@AdobeOrg` è sempre impostato con il servizio CX Enterprise ID.

Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia tali dati negli Stati Uniti. Audience Manager non fornisce un&#39;opzione per archiviare o elaborare tali dati al di fuori degli Stati Uniti.
