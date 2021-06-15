---
description: Modernizza le tue soluzioni Adobe Analytics e Adobe Target per i servizi tra più soluzioni. Scopri come iniziare a utilizzare i servizi Experience Cloud.
keywords: servizi core; Attributi del cliente
solution: Experience Cloud
title: Abilita le soluzioni per i servizi tra più soluzioni
index: true
feature: Attributi del cliente
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: eef7326f9f04f68eefb60b5d9fd4cc91cbe52119
workflow-type: tm+mt
source-wordcount: '2334'
ht-degree: 71%

---

# Abilitare l’implementazione per i servizi Experience Cloud

Se hai implementato Experience Cloud di recente utilizzando Experience Platform Launch, disponi già della configurazione per Attributi del cliente e Tipi di pubblico di Experience Cloud. Inoltre puoi gestire utenti e prodotti nell’Admin Console.

I clienti esistenti possono modernizzare le implementazioni delle soluzioni e implementare Experience Cloud. In questo modo puoi utilizzare le funzioni Attributi del cliente e tipi di pubblico in Adobe Analytics, Audience Manager e Adobe Target. A tal fine, effettuerai le seguenti operazioni:

1. [Partecipazione a Experience Cloud per diventare un amministratore](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementa il servizio Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Mappatura di suite di rapporti per un&#39;organizzazione Experience Cloud](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Aggiornamento del codice AppMeasurement di Analytics](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Aggiornamento dell&#39;implementazione di Adobe Target](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verificare l’implementazione](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Gestione di utenti e prodotti](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Inizio della condivisione dei dati degli attributi e dei tipi di pubblico](#section_960C06093623462E8EA247B3E97274A1)

## Partecipazione a Experience Cloud per diventare un amministratore {#section_2423F0BD3DF642658103310EE5EA6154}

Come partecipare a Experience Cloud:

1. Verifica di disporre degli SKU Adobe Analytics o Adobe Target appropriati.

   * **Adobe Analytics:** Standard o Premium (non lo SKU legacy di [!DNL SiteCatalyst]).
   * **Adobe Target:** Standard o Premium.

   >[!NOTE]
   >
   >Ad [!DNL Target] esempio, effettua la migrazione a at.js da [!DNL mbox.js]. Consulta [Aggiornamento da at.js 1. x a at.js 2. x](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=en).

1. Modernizza la tua implementazione ed effettua il provisioning di un amministratore.

   * Segui i passaggi indicati in [Implementazione del [!UICONTROL Servizio Experience Cloud ID]](core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
   * Contatta il tuo Account Manager e avvia il processo di provisioning per Experience Cloud.

1. Gestisci utenti e prodotti in [!UICONTROL Admin Console].

### Accesso amministratore

Se hai il ruolo di amministratore, puoi accedere a [experience.adobe.com](https://experience.adobe.com).

Il collegamento **[!UICONTROL Admin Console]** è disponibile nella navigazione del menu di Experience Cloud.

Per assistenza, consulta [Amministrazione di utenti e prodotti Experience Cloud](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Accesso utente

Per accedere a Experience Cloud, i tuoi utenti devono:

* Disporre di un Adobe ID (o Enterprise ID per un&#39;azienda).
* Accedi a [experience.adobe.com](https://experience.adobe.com).
* Appartenere a un gruppo di soluzioni mappato a un gruppo enterprise.
* Se necessario, collega i loro account della soluzione al rispettivo Adobe ID (procedura descritta di seguito).

### Facoltativo: collega gli account utente esistenti.

Probabilmente alcuni dei tuoi utenti sono già membri di gruppi di soluzioni, ad esempio di un gruppo Analytics che hai precedentemente gestito in [!UICONTROL Analytics] > [!UICONTROL Strumenti di amministrazione].

Quando mappi questi gruppi ai gruppi aziendali Experience Cloud, gli utenti devono collegare manualmente le credenziali dell&#39;account della loro soluzione al rispettivo Adobe ID.

Consulta [Collegamento di account in Experience Cloud](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>Dopo aver mappato gruppi aziendali e di soluzioni, i nuovi utenti sono automaticamente collegati. Le credenziali della soluzione vengono create e collegate automaticamente al relativo Adobe ID.

Le sezioni seguenti descrivono come poter modernizzare l&#39;implementazione. La modernizzazione dell&#39;implementazione abilita i servizi core in Experience Cloud.

## Implementa il [!UICONTROL servizio Experience Cloud ID] {#section_3C9F6DF37C654D939625BB4D485E4354}

Il [!UICONTROL Servizio Experience Cloud ID] fornisce un ID comune per l&#39;integrazione tra diverse soluzioni. Fornisce l&#39;identificazione dei visitatori tra domini, oltre a un percorso per il targeting e la personalizzazione tra dispositivi e browser basati sui dati CRM che sono stati caricati tramite gli [!UICONTROL Attributi del cliente].

Il metodo più semplice per abilitare i servizi core di Experience Cloud è quello di attivarli automaticamente per Analytics e Adobe Target tramite l&#39;[estensione del servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html?lang=it#extensions-ref) all’interno di [!UICONTROL Experience Platform Launch].

Per ricevere un aiuto completo sul Servizio Experience Cloud ID (già ID visitatore), visita [qui](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=it#intro).

**Non usi [!UICONTROL Experience Platform Launch] o [!UICONTROL Dynamic Tag Management]?**

Se non utilizzi [!UICONTROL Experience Platform Launch] o [!UICONTROL Dynamic Tag Management], implementa manualmente il servizio ID tramite la distribuzione JavaScript ([!DNL VisitorAPI.js]), come segue:

| Attività | Descrizione |
| -----------| ---------- |  
| [Implementazione del servizio Experience Cloud ID per Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=en) | Adobe consiglia inoltre di impostare [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en) aggiuntivi. Tali ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future di base di Experience Cloud. |
| Aggiorna il file [!DNL s_code] esistente alla versione H.27.3 o successiva oppure il file [!DNL AppMeasurement.js] esistente alla versione 1.4 o successiva. | Tali file sono disponibili per il download in [Gestore codice](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=en) in Strumenti amministratore di Analytics. Puoi consultare la [Guida all&#39;implementazione JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=en#js) per ulteriori informazioni su [!DNL AppMeasurement.js]. |
| Sincronizzazione dell&#39;ID cliente per Analytics | Consulta [Analytics - Sincronizzazione dell&#39;ID cliente](core-services.md#section_AD473A6A21C1446498E700363F9A8437) (di seguito). |

### Analytics &amp; Adobe Target - Sincronizzazione dell&#39;ID cliente {#section_AD473A6A21C1446498E700363F9A8437}

In qualità di parte dell&#39;impostazione del servizio Experience Cloud ID, Adobe consiglia per Analytics e [!DNL Target] la sincronizzazione degli [ID cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en) con Experience Cloud.

In Adobe Target, il `mbox3rdpartyid` deve ottenere l&#39;ID cliente e inviarlo a [!DNL Target]. Consulta [Uso degli attributi del cliente](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=en) in [!DNL Target].

Quando un visitatore si autentica sul tuo sito web o in generale si identifica, l&#39;implementazione deve esporre l&#39;ID cliente CRM della persona alla pagina o all&#39;app. Puoi quindi utilizzare la funzionalità appropriata per sincronizzare l&#39;ID cliente a Experience Cloud. La sincronizzazione archivia l&#39;ID cliente CRM del visitatore in Experience Cloud e attiva gli attributi del cliente per l&#39;utilizzo in Experience Cloud.

Ad esempio, si supponga che Bob sia associato all&#39;ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiamando `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante il servizio ID visitatore. oppure
* Popolare il *`Customer ID (52mc210tr42)`* in una prop o eVar.

L&#39;ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l&#39;ID cliente.

### SDK per dispositivi mobili

Consulta la sezione *Servizio ID Experience Cloud* per esempi di sintassi per l&#39;impostazione di ID cliente aggiuntivi nelle applicazioni mobili [Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=en) e [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=en) .

### Abilitazione degli attributi per i dati presenti nella cronologia

I dati dell&#39;attributo del cliente sono disponibili dopo l&#39;accesso dei visitatori. Se non hai ancora implementato il servizio ID e se stai tenendo traccia degli ID cliente in una prop o in un eVar, puoi richiedere un processo che invia ad Experience Cloud gli accessi cronologici. Questo processo ti consente di iniziare a utilizzare Attributi del cliente immediatamente.

Contatta l&#39;Assistenza clienti per abilitare i dati presenti nella cronologia.

## Mappatura di suite di rapporti per un&#39;organizzazione Experience Cloud {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>La funzionalità di mappatura di suite di rapporti è diventata obsoleta a novembre 2020. Per eventuali domande, rivolgiti al servizio di assistenza clienti.

I servizi Experience Cloud (come Experience Cloud ID e il servizio [!UICONTROL People]) sono associati a una suite di rapporti di un&#39;organizzazione Experience Cloud, anziché a una sola suite di rapporti di Analytics. Per garantire il corretto funzionamento di questi servizi, ogni suite di rapporti di Analytics deve essere mappata a un&#39;organizzazione Experience Cloud.

## Aggiornamento del codice AppMeasurement di Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Se utilizzi Analytics, verifica di essere nella raccolta dati regionale (RDC). Se il dominio della raccolta dati è [!DNL omtrdc.net] o se il CNAME è mappato a [!DNL omtrdc.net] sei all&#39;interno dell&#39;RDC. Consulta [Passaggio all&#39;RDC](https://experienceleague.adobe.com/docs/analytics/technotes/rdc/regional-data-collection.html?lang=en) per ulteriori informazioni. Se stai utilizzando cookie di terze parti, fai riferimento a [CNAME e servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=en) per informazioni sulla raccolta dei dati CNAME e sul tracciamento tra domini.

Si consiglia di modernizzare l&#39;implementazione di Analytics aggiornando le librerie JavaScript, incluso l&#39;API visitatore. Il modo più semplice per eseguire +632581 è aggiungere uno strumento [!DNL Adobe Analytics] in Dynamic Tag Management specificando *`Automatic`* come metodo di configurazione.

In [!UICONTROL Dynamic Tag Management], fai clic su **`<Web Property Name>`** > **[!UICONTROL Panoramica]** > **[!UICONTROL Aggiungi uno strumento]** > **[!UICONTROL Adobe Analytics]**. Per informazioni sulla distribuzione, consulta [Impostazioni di Adobe Analytics](https://experienceleague.adobe.com/docs/dtm/using/tools/analytics-dtm.html?lang=en) in Dynamic Tag Management.

## Aggiornamento dell&#39;implementazione di Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* È consigliabile aggiungere un&#39;[estensione Adobe Target](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html?lang=it) in [!UICONTROL Experience Platform Launch] per rendere automatico il recupero della libreria. Puoi anche impostare l&#39;[estensione del servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html?lang=en) per Adobe Target (e altre soluzioni) tramite [!UICONTROL Experience Platform Launch]. **È necessario** l&#39;aggiornamento del [!UICONTROL Servizio Experience Cloud ID] per consentire ad Adobe Target di utilizzare i servizi core. Se utilizzi [!UICONTROL Dynamic Tag Management], aggiungi uno [strumento Adobe Target](https://experienceleague.adobe.com/docs/dtm/using/tools/target.html?lang=en). Puoi anche utilizzare [!UICONTROL Dynamic Tag Management] per distribuire il servizio Experience Cloud ID per Adobe Target.
* Se non utilizzi [!UICONTROL Experience Platform Launch] o [!UICONTROL Dynamic Tag Management], [aggiorna manualmente la libreria mbox](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html?lang=en).
* Richiedi l&#39;accesso per utilizzare Adobe Analytics come fonte di reporting per [!DNL Adobe Target]. I dati di [!DNL Target] e [!DNL Analytics] sono combinati nella stessa chiamata al server durante l&#39;elaborazione affinché i visitatori siano collegati tra le due soluzioni. Consulta [Analytics per implementazione di Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=en).

   >[!IMPORTANT]
   >
   >Tutti i clienti Analytics dispongono già del provisioning per i servizi principali quali Attributi del cliente. Se non sei cliente Analytics, contatta l&#39;Assistenza clienti per richiedere il provisioning.

## Verificare l’implementazione {#section_E641782A0F4F44AF8C9C91216BE330D5}

Utilizza il seguente procedimento per assicurarti che il servizio Experience Cloud ID sia correttamente implementato sul tuo sito.

1. Elimina i cookie dal sito in uso affinché sia possibile visualizzare la richiesta al servizio Experience Cloud ID (la richiesta viene effettuata alla prima visita, quindi una volta a settimana per ogni visitatore).
1. Utilizzando un analizzatore di pacchetti o il pannello di rete in un debugger del browser web, cerca una richiesta indirizzata a [!DNL dpm.demdex.net].
1. Verifica che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verifica che la richiesta di Analytics contenga il parametro `mid` (Experience Cloud ID). Nel periodo di prova (se disponibile) dovrebbe essere visibile un parametro `aid` (l&#39;ID visitatore di Analytics).

Risposta prevista contenente Experience Cloud ID:

![](assets/mac_id_response.png)

Immagine della richiesta di Analytics contenente l&#39;Experience Cloud ID (noto anche come `mid` o _ID visitatore_):

![](assets/mid.png)

Experience Cloud ID nella richiesta mbox:

![](assets/mbox_request.png)

### Cos&#39;è il periodo di prova?

Dopo la distribuzione del servizio ID Experience Cloud, i nuovi visitatori non ricevono più un Experience Cloud ID di Analytics dal server di raccolta dati. Se il Servizio ID non è stato ancora implementato nelle sezioni del sito, quando i visitatori accedono a tali sezioni, l&#39;Experience Cloud ID non viene riconosciuto e ai visitatori viene assegnato un ID visitatore Analytics legacy. Ciò può causare potenziali problemi, incluse visite duplicate e attribuzioni non corrette.

Ad esempio, se la sezione di assistenza del sito viene gestita in un CMS separato, dovresti avere un file JavaScript di Analytics separato per tale sezione. Se distribuisci l&#39;ID Experience Cloud sul sito principale prima di distribuire il servizio ID al sito di supporto, i nuovi visitatori riceveranno un ID Analytics legacy quando visitano la sezione di supporto. Le visite che si estendono su entrambe le sezioni del sito sono indicate come visite diverse.

La distribuzione del servizio Experience Cloud ID su siti che utilizzano più file JavaScript o altre tecnologie (come il Flash) può causare problemi di coordinazione. Questi problemi si verificano perché devi attivare il servizio Experience Cloud ID su tutte le parti del sito contemporaneamente. Configurando un periodo di tolleranza, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID. I visitatori possono essere identificati in modo coerente nelle sezioni del sito che non sono state aggiornate per l&#39;uso del servizio ID visitatore.

## Gestione di utenti e prodotti {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Quando è tutto pronto, vai a [Admin Console](https://adminconsole.adobe.com/), per gestire gli utenti e i profili di prodotto.

![](assets/menu-administration-shell.png)

Consulta [Gestione di utenti e prodotti Experience Cloud](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Attributi del cliente

Gli utenti che vengono aggiunti al gruppo [!UICONTROL Attributi del cliente] possono vedere la voce di menu [!UICONTROL Attributi del cliente] sul lato sinistro dell&#39;Experience Cloud.

## Inizio della condivisione dei dati degli attributi e dei tipi di pubblico {#section_960C06093623462E8EA247B3E97274A1}

Utilizza le seguenti funzionalità.

### [!UICONTROL Persone] > [!UICONTROL Attributi del cliente]

Se acquisisci dati del cliente di livello Enterprise in un database di gestione delle relazioni con i clienti (Customer Relationship Management, CRM), puoi caricare tali dati in un&#39;origine dati Attributi del cliente nell&#39;Experience Cloud. Una volta effettuato l’aggiornamento, utilizza i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Consulta [Attributi del cliente](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL Persone] > [!UICONTROL Libreria Audience]

[!UICONTROL Audiences] di Experience Cloud è l&#39;interfaccia che consente di creare tipi di pubblico, o audience, combinare quelli esistenti per creare un pubblico composito e visualizzare quelli condivisi.

Consulta [Audiences](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## Archivio dei dati e informativa sulla privacy

Se utilizzi la profilazione del pubblico in tempo reale e altri servizi core nell&#39;Adobe [!DNL Experience Cloud], l&#39;utilizzo di questi servizi potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché [!DNL Experience Cloud] utilizza Audience Manager, i dati utilizzati nel servizio [!UICONTROL Persone] devono trovarsi nei server di Audience Manager negli Stati Uniti.

Quando si utilizzano i servizi resi disponibili tramite il servizio [!UICONTROL Persone], i tipi di dati inviati da altri prodotti Adobe alla gestione dell&#39;audience sono:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l&#39;indirizzo IP, incluso l&#39;ultimo ottetto dell&#39;IP (partendo dal presupposto che l&#39;indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell&#39;IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base a regole impostate in Audience Manager.
* (Facoltativo) Uno o più degli ID. In base al tipo di implementazione del servizio ID, puoi effettuare invii mediante uno o più degli ID, come ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti ad Adobe Gestione dell&#39;audience. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Consiglia invece di utilizzare hash univoci per mascherare i dati prima di inviarli ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. Il cookie di prime parti `AMCV_###@AdobeOrg` è sempre impostato con il servizio Experience Cloud ID.

Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia tali dati negli Stati Uniti. Audience Manager non fornisce un&#39;opzione per archiviare o elaborare tali dati al di fuori degli Stati Uniti.

### Cookie e rinunce

L&#39;utilizzo di profili in tempo reale utilizza il cookie di Audience Manager, oltre ai cookie utilizzati per [!DNL Analytics] e [!DNL Target].

Se desideri fornire ai visitatori del sito la funzionalità di rinuncia, devi aggiungere la rinuncia a Audience Manager nel processo di rinuncia esistente.

Per le istruzioni, consulta [Adobe Experience Cloud - Implementazione rinunce Adobe](https://experienceleague.adobe.com/docs/analytics/implementation/js/opt-out.html).

Per abilitare il tracciamento tra domini, consulta [CNAME raccolta dati e tracciamento tra domini](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=en).