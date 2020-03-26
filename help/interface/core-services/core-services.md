---
description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per le funzioni del servizio di base come gli attributi del cliente e le audience.
keywords: core services;customer attributes
seo-description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per le funzioni del servizio di base come gli attributi del cliente e le audience.
seo-title: Abilitare le soluzioni Experience Cloud per i servizi di base
solution: Experience Cloud
title: Abilita le tue soluzioni per i servizi di base
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Abilita le tue soluzioni per i servizi di base

Per i clienti esistenti, scopri come modernizzare le implementazioni della soluzione e implementare Experience Cloud in modo da poter utilizzare funzionalità come gli attributi del cliente e i tipi di pubblico. A tal fine, effettuerete le seguenti operazioni:

1. [Partecipazione a Experience Cloud per diventare un amministratore](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementazione del servizio Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Mappatura delle suite di rapporti su un&#39;organizzazione Experience Cloud](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Aggiorna il codice AppMeasurement di Analytics](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Aggiornamento dell&#39;implementazione di Adobe Target](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifica dell&#39;implementazione dei servizi di base](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Gestione di utenti e prodotti](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Utilizzo dei servizi di base](#section_960C06093623462E8EA247B3E97274A1)

## Passaggio 1: Partecipazione a Experience Cloud per diventare un amministratore {#section_2423F0BD3DF642658103310EE5EA6154}

Cosa devi fare per partecipare a Experience Cloud:

![](assets/step1_icon.png) Verifica di disporre degli SKU Adobe Analytics o Adobe Target appropriati.

* **Adobe Analytics:** Standard o Premium (non lo [!DNL SiteCatalyst] SKU legacy).
* **Adobe Target:** Standard o Premium.

>[!NOTE]
>
>Ad [!DNL Target]esempio, effettuare la migrazione a at.js da [!DNL mbox.js]. See [Upgrading from at.js 1. x to at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) Modernizza la tua implementazione ed effettua il provisioning di un amministratore.

1. Segui i passaggi indicati in [Distribuzione del servizio ](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)Experience Cloud ID.
1. Contatta il tuo Account Manager e avvia il processo di provisioning per Experience Cloud.

![](assets/step3_icon.png)[!UICONTROL  Gestisci utenti e prodotti in Admin Console].

### Login amministratore

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Dovresti visualizzare il collegamento **[!UICONTROL Amministrazione]** nel menu di navigazione di Experience Cloud.

Per assistenza, consulta [Amministrazione di utenti e prodotti Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Login utente

Per accedere a Experience Cloud, i tuoi utenti devono:

1. Avere un Adobe ID (o Enterprise ID per la società).
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Appartiene a un gruppo di soluzioni mappato a un gruppo enterprise.
1. Se necessario, collegate i loro account della soluzione al loro Adobe ID (descritto di seguito).

![](assets/step4_icon.png) Facoltativo: collega gli account utente esistenti.

Probabilmente hai degli utenti che sono già membri di gruppi di soluzioni, come un gruppo Analytics precedentemente gestito in [!UICONTROL Analytics] > [!UICONTROL Strumenti]di amministrazione.

Quando mappate questi gruppi a gruppi aziendali Experience Cloud, questi utenti devono collegare manualmente le credenziali account della loro soluzione al loro Adobe ID.

Consulta [Collegamento di account in Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>Dopo aver mappato gruppi aziendali e di soluzioni, i nuovi utenti sono automaticamente collegati. (Le credenziali della soluzione vengono create automaticamente e collegate al relativo Adobe ID.)

Le sezioni seguenti descrivono come modernizzare l’implementazione. Modernizzazione dell&#39;implementazione abilita i servizi di base in Experience Cloud.

## Passaggio 2: Implementazione del servizio  Experience Cloud ID tramite [!UICONTROL Experience Platform Launch]o Gestione [!UICONTROL tag] dinamica {#section_3C9F6DF37C654D939625BB4D485E4354}

Il servizio  Experience Cloud ID fornisce un ID comune per l&#39;integrazione tra più soluzioni. Fornisce l&#39;identificazione dei visitatori tra domini e un percorso per il targeting e la personalizzazione tra dispositivi e browser basati sui dati CRM caricati tramite attributi cliente.

Il metodo più semplice per abilitare i servizi di base di Experience Cloud è quello di attivarli automaticamente per Analytics e Adobe Target tramite l’estensione [del servizio](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) Experience Cloud ID in [!UICONTROL Experience Platform Launch]o tramite lo strumento ECID in Gestione [!UICONTROL tag]dinamica. (Si consiglia vivamente di avviare Experience Platform).

![](assets/menu-activation-shell.png)

Per l’aiuto completo del servizio Experience Cloud ID (già ID visitatore), visita [qui](https://docs.adobe.com/content/help/en/id-service/using/home.html).

**Non utilizzate[!UICONTROL Experience Platform Launch]o Gestione[!UICONTROL tag]dinamica?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| Attività | Descrizione |
| -----------| ---------- |  
| [Implementazione del servizio Experience Cloud ID per Analytics](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe consiglia inoltre di impostare ID [cliente](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html)aggiuntivi. Tali ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future in Experience Cloud. |
| Aggiorna il file [!DNL s_code] esistente alla versione H.27.3 o successiva oppure il file [!DNL AppMeasurement.js] esistente alla versione 1.4 o successiva. | Questi file sono disponibili per il download in [Code Manager](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html) in Analytics Admin Tools.  (La guida Implementazione [](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript è disponibile per ulteriori informazioni su [!DNL AppMeasurement.js]). |
| Sincronizzazione dell&#39;ID cliente per Analytics | See [Analytics - synching the customer ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (below). |

## Analytics &amp; Adobe Target - synching the customer ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (vedere [Uso degli attributi](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) cliente in [!DNL Target].)

Quando un visitatore si autentica sul tuo sito Web o in altro modo si identifica, la tua implementazione deve esporre l&#39;ID cliente CRM della persona alla pagina o all&#39;app. Puoi quindi utilizzare la funzionalità appropriata per sincronizzare l&#39;ID cliente a Experience Cloud. Questa sincronizzazione archivia l&#39;ID cliente CRM del visitatore in Experience Cloud e attiva gli attributi del cliente per l&#39;uso in Experience Cloud.

Ad esempio, si supponga che Bob sia associato all&#39;ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiamando `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante il servizio ID visitatore. oppure
* Popolare il *`Customer ID (52mc210tr42)`* in una prop o eVar.

L&#39;ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l&#39;ID cliente.

### SDK per dispositivi mobili

Consulta la sezione Servizio *Experience Cloud ID per esempi di sintassi per l’impostazione di ID cliente aggiuntivi nelle applicazioni mobili* Android [e](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html) iOS [](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) .

### Abilitazione degli attributi per i dati presenti nella cronologia

I dati dell&#39;attributo del cliente vengono resi disponibili dopo l&#39;accesso dei visitatori. Se non hai ancora implementato l’ultimo servizio Experience Cloud ID e se hai tracciato storicamente gli ID cliente in una prop o eVar, puoi richiedere un processo che invia gli accessi cronologici a Experience Cloud. Questo processo consente di iniziare a utilizzare gli attributi del cliente immediatamente.

Contatta l’Assistenza clienti per abilitare i dati della cronologia.

## Passaggio 3: Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud services (such as Experience Cloud ID Service and the [!UICONTROL People service]) are associated with an Experience Cloud organization instead of an individual Analytics report suite. Per garantire il corretto funzionamento di questi servizi, ogni suite di rapporti di Analytics deve essere mappata su un&#39;organizzazione Experience Cloud.

Consulta [Mappatura di suite di rapporti per un’organizzazione](report-suite-mapping.md).

## Passaggio 4: (Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Verifica di essere nella raccolta dati regionale (RDC). Se il dominio della raccolta dati è [!DNL omtrdc.net] o se il CNAME è mappato a [!DNL omtrdc.net] sei all&#39;interno dell&#39;RDC. Per ulteriori informazioni, consulta [Passaggio all’RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) . Se utilizzi cookie di prime parti, fai riferimento a [CNAME e al servizio](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) Experience Cloud ID per informazioni sulla raccolta dei dati e sul tracciamento tra domini.

Si consiglia di modernizzare l&#39;implementazione di Analytics aggiornando le librerie JavaScript, incluso l&#39;API visitatore. Il modo più semplice per farlo è aggiungere uno strumento [!DNL Adobe Analytics] in Dynamic Tag Management specificando *`Automatic`* come metodo di configurazione.

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**>**[!UICONTROL  Panoramica ]**>**[!UICONTROL  Aggiungi uno strumento ]**>**[!UICONTROL  Adobe Analytics ]**. See[Adobe Analytics Settings](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)in Dynamic Tag Management for deployment information.

## Passaggio 5: (Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* È consigliabile aggiungere un&#39;estensione [](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) Adobe Target in [!UICONTROL Experience Platform Launch], in modo che il recupero della libreria sia automatico. Puoi anche impostare l’estensione [del servizio](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) Experience Cloud ID per Adobe Target (e altre soluzioni) tramite [!UICONTROL Experience Platform Launch]. L&#39;aggiornamento del servizio  Experience Cloud ID **è richiesto** per Adobe Target per utilizzare i servizi di base. (Se utilizzi Gestione [!UICONTROL tag]dinamica, aggiungi uno strumento [](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)Adobe Target. Puoi anche utilizzare Gestione [!UICONTROL tag] dinamica per distribuire il servizio Experience Cloud ID per Adobe Target.
* Se non utilizzate [!UICONTROL Experience Platform Launch] o Gestione [!UICONTROL tag]dinamica, [aggiornate manualmente la libreria](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) mbox.
* Richiedi l&#39;accesso per utilizzare Adobe Analytics come fonte di reporting per [!DNL Adobe Target]. [!DNL Target]I dati di e sono combinati nella stessa chiamata al server durante l&#39;elaborazione affinché i visitatori siano collegati tra le due soluzioni. [!DNL Analytics] See [Analytics for Target Implementation](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >Tutti i clienti Analytics dispongono già del provisioning per i servizi di base come gli attributi del cliente. Se non sei cliente Analytics, contatta l&#39;Assistenza clienti per richiedere il provisioning.

## Passaggio 6: Verifica dell&#39;implementazione dei servizi di base {#section_E641782A0F4F44AF8C9C91216BE330D5}

Utilizza il seguente procedimento per assicurarti che il servizio Experience Cloud ID sia correttamente implementato sul tuo sito.

1. Cancella i cookie del tuo sito per visualizzare la richiesta al servizio Experience Cloud ID (la richiesta viene effettuata alla prima visita, quindi circa una volta a settimana per ogni visitatore).
1. Utilizzando un analizzatore di pacchetti o il pannello di rete in un debugger del browser Web, cerca una richiesta indirizzata a [!DNL dpm.demdex.net].
1. Verifica che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verify that the Analytics request contains the `mid` parameter (the Experience Cloud ID). Durante il periodo di tolleranza (se è attivato), dovresti vedere anche un `aid` parametro (l’ID visitatore di Analytics).

Risposta prevista contenente il Experience Cloud ID:

![](assets/mac_id_response.png)

Immagine della richiesta di Analytics contenente l’Experience Cloud ID (noto anche come `mid` ID _visitatore_):

![](assets/mid.png)

Experience Cloud ID nella richiesta mbox:

![](assets/mbox_request.png)

### Qual è il periodo di tolleranza?

Dopo aver distribuito il servizio Experience Cloud ID, i nuovi visitatori non ricevono più un ID Experience Cloud di Analytics dal server di raccolta dati. Se le sezioni del sito non hanno ancora implementato il servizio Experience Cloud ID, quando i visitatori accedono a tali sezioni, Experience Cloud ID non viene riconosciuto e ai visitatori viene assegnato un ID visitatore Analytics legacy. Ciò può causare potenziali problemi, tra cui visite duplicate e attribuzione errata.

Ad esempio, se la sezione di supporto del sito è gestita in un CMS separato, potresti avere un file JavaScript di Analytics diverso per questa sezione. Se distribuisci l’Experience Cloud ID sul tuo sito principale prima di distribuire il servizio ID al sito di supporto, i nuovi visitatori riceveranno un ID Analytics legacy quando visitano la sezione di supporto, e le visite che si estendono su entrambe le sezioni del sito saranno segnalate come visite diverse.

La distribuzione del servizio Experience Cloud ID su siti che utilizzano più file JavaScript o altre tecnologie (come Flash) può causare problemi di coordinazione, perché è necessario abilitare il servizio Experience Cloud ID su tutte le porzioni del sito contemporaneamente. Configurando un periodo di tolleranza, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID, in modo che i visitatori possano essere costantemente identificati nelle sezioni del sito che non sono state aggiornate per utilizzare il servizio ID visitatore.

## Passaggio 7: Gestione di utenti e prodotti {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

Consulta [Gestione di utenti e prodotti Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Attributi cliente

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Adobe Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

## Passaggio 8: Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

Utilizza le seguenti funzionalità del servizio di base.

![](assets/menu-audiences-shell.png)

### [!UICONTROL Persone] > [!UICONTROl Attributi del cliente]

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Consulta [Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL Persone] > Libreria [!UICONTROL Pubblico]

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

Consulta [Audiences](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## Archivio dei dati e informativa sulla privacy

Se si usa la profilazione del pubblico in tempo reale e altri servizi core in Adobe [!DNL Experience Cloud], l’uso di questi servizi potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché i servizi di Adobe [!DNL Experience Cloud] usano Adobe Audience Manager, i dati utilizzati nel servizio core persone devono trovarsi nei server di Audience Manager negli Stati Uniti.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l&#39;indirizzo IP, incluso l&#39;ultimo ottetto dell&#39;IP (partendo dal presupposto che l&#39;indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell&#39;IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base alle regole configurate in Audience Manager.
* (Facoltativo) Uno o più ID. A seconda dell’implementazione del servizio ID, potresti inviare anche uno o più ID, ad esempio ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti ad Adobe Gestione dell&#39;audience. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Piuttosto, utilizzate un hash unidirezionale per mascherare i dati prima che vengano inviati ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia questi dati negli Stati Uniti. Audience Manager non fornisce un&#39;opzione per archiviare o elaborare questi dati al di fuori degli Stati Uniti.

### Cookie e rinunce

L&#39;utilizzo di profili in tempo reale sfrutta il cookie di Audience Manager oltre ai cookie utilizzati per [!DNL Analytics] e [!DNL Target].

Se desideri fornire ai visitatori del sito la funzionalità di rinuncia, devi aggiungere la rinuncia a Audience Manager nel processo di rinuncia esistente.

Consulta [Adobe Experience Cloud - Implementazione rinunce Adobe](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html) per le istruzioni.

Per abilitare il tracciamento tra domini, vedi CNAME di raccolta [dati e tracciamento](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) tra domini.
