---
description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per funzionalità di servizi di base come gli attributi dei clienti e i tipi di pubblico.
keywords: servizi principali;attributi del cliente
seo-description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per funzionalità di servizi di base come gli attributi dei clienti e i tipi di pubblico.
seo-title: Abilitare le soluzioni Experience Cloud per i servizi di base
solution: Experience Cloud
title: Abilita le tue soluzioni per i servizi di base
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: c0ba39895218769e27ab99568387eb91310a574c

---


# Abilita le tue soluzioni per i servizi di base

Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per funzionalità di servizi di base come gli attributi dei clienti e i tipi di pubblico.

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## Passaggio 1: Partecipazione a Experience Cloud per diventare un amministratore {#section_2423F0BD3DF642658103310EE5EA6154}

Cosa devi fare per partecipare a Experience Cloud:

![](assets/step1_icon.png) Verifica di disporre degli SKU Adobe Analytics o Adobe Target appropriati.

* **Adobe Analytics:** Standard o Premium (non lo SKU legacy di SiteCatalyst).
* **Adobe Target**: Standard o Premium.

>[!NOTE]
>
>For Target, [migrate to at.js from mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov2/t_target-migrate-atjs.html).

![](assets/step2_icon.png) Modernizza la tua implementazione ed effettua il provisioning di un amministratore.


1. Segui i passaggi riportati di seguito in [Distribuzione del servizio Experience Cloud ID](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
1. Contatta il tuo account manager e inizia il processo di provisioning per Experience Cloud.

![](assets/step3_icon.png) Gestisci utenti e prodotti in Admin Console.

**Accesso amministratore**

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Dovresti visualizzare il collegamento **[!UICONTROL Amministrazione]** nel menu di navigazione di Experience Cloud.

Per assistenza, consulta [Amministrazione di utenti e prodotti Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

**Accesso utente**

Per accedere a Experience Cloud i tuoi utenti devono:


1. Avere un Adobe ID.
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Appartenere a un gruppo di una soluzione mappato su un gruppo enterprise.
1. Se necessario, collegare i loro account soluzione ai loro Adobe ID (come descritto di seguito).

![](assets/step4_icon.png) Facoltativo: collega gli account utente esistenti.

Probabilmente hai degli utenti che sono già membri di gruppi di soluzioni, come un gruppo Analytics gestito in Analytics &gt; Strumenti di amministrazione.

Quando mappi questi gruppi su gruppi aziendali di Experience Cloud, questi utenti devono collegare manualmente le credenziali account della loro soluzione al loro Adobe ID.

Consulta [Collegamento di account in Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> Dopo aver mappato gruppi aziendali e di soluzioni, i nuovi utenti sono automaticamente collegati. (le credenziali della soluzione vengono automaticamente create e collegate al proprio Adobe ID).

Le sezioni seguenti descrivono come modernizzare la propria implementazione per abilitare i servizi di base in Experience Cloud.

## Passaggio 2: Implementazione del servizio Experience Cloud ID tramite Dynamic Tag Manager o Experience Platform Launch {#section_3C9F6DF37C654D939625BB4D485E4354}

Il metodo più semplice per abilitare i servizi di base di Experience Cloud è quello di attivarli automaticamente per Analytics e Target, mediante lo [strumento del servizio Experience Cloud ID](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/standard.html) in Dynamic Tag Manager (o Experience Platform Launch).

![](assets/menu-activation-shell.png)

For complete Experience Cloud ID service help (formerly, visitor ID), go [here](https://docs.adobe.com/content/help/en/id-service/using/home.html).

Inoltre, la gestione tag di nuova generazione è [Launch, di Adobe](https://docs.adobelaunch.com/getting-started).

**Non utilizzi Dynamic Tag Management o Launch?**

Se non utilizzi Dynamic Tag Management, implementa manualmente il servizio ID tramite la distribuzione JavaScript ([!DNL VisitorAPI.js]), come segue:

1. Effettua i passaggi descritti in [Implementazione del sevizio Experience Cloud ID per Analytics](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-analytics.html).

   Adobe consiglia inoltre di impostare [ID cliente](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) aggiuntivi. Tali ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future dei servizi di base di Experience Cloud.

1. Aggiorna il file [!DNL s_code] esistente alla versione H.27.3 o successiva oppure il file [!DNL AppMeasurement.js] esistente alla versione 1.4 o successiva.

   Tali file sono disponibili per il download in [Gestore codice](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html) in Strumenti amministratore di Analytics.

   (La guida [Implementazione di JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) è disponibile per ulteriori informazioni su [!DNL AppMeasurement.js]).

1. Sincronizza l'ID cliente per Analytics. Consulta [Analytics - Sincronizzazione dell'ID cliente](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (di seguito).

## Analytics e Target - Sincronizzazione dell'ID cliente {#section_AD473A6A21C1446498E700363F9A8437}

In qualità di parte dell'impostazione del servizio Experience Cloud ID, per Analytics e Target Adobe consiglia di sincronizzare gli [ID cliente](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) con Experience Cloud.

In Target, [!DNL mbox3rdpartyid] deve ottenere l'ID cliente e inviarlo a Target (consulta [Utilizzo degli attributi cliente](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) in Target).

Quando un visitatore si autentica su un tuo sito Web o in generale si identifica, l'implementazione deve esporre l'ID cliente CRM della persona nella pagina o nell'applicazione. Puoi quindi utilizzare la funzionalità appropriata per sincronizzare l'ID cliente a Experience Cloud. La sincronizzazione archivia l'ID cliente CRM del visitatore in Experience Cloud e attiva gli attributi del cliente per l'utilizzo in Experience Cloud.

Ad esempio, si supponga che Bob sia associato all'ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiamando `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante il servizio ID visitatore. oppure
* Popolare il *`Customer ID (52mc210tr42)`* in una prop o eVar.


L'ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l'ID cliente.

**SDK per dispositivi mobili**

Consulta la sezione del servizio *Experience Cloud ID per esempi di sintassi per l’impostazione di ID cliente aggiuntivi nelle applicazioni mobili* Android [e](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html) iOS [](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) .

**Abilitazione degli attributi per i dati presenti nella cronologia**

I dati dell'attributo cliente sono disponibili dopo l'accesso dei visitatori. Se non hai ancora implementato l'ultimo servizio Experience Cloud ID e se stai tenendo traccia degli ID cliente in una prop o eVar, puoi richiedere un procedimento che invia gli accessi cronologici a Experience Cloud. Tale procedimento consente di iniziare a usare gli attributi del cliente immediatamente.

Contatta l'Assistenza clienti per abilitare i dati presenti nella cronologia.

## Passaggio 3: Mappatura di suite di rapporti per un’organizzazione Experience Cloud {#section_7B08516B01BA421681DF03D0E86CE3BA}

I servizi Experience Cloud (come Experience Cloud ID e persone) sono associati con una suite di rapporti di un'organizzazione invece che con una sola suite di rapporti. Per garantire il funzionamento corretto di questi servizi, ogni suite di rapporti di Analytics deve essere mappata su un'organizzazione Experience Cloud.

Consulta [Mappatura di suite di rapporti per un’organizzazione](report-suite-mapping.md).

## Passaggio 4: (Adobe Analytics) Modernizzazione del codice AppMeasurement di Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Verifica di essere nella raccolta dati regionale (RDC). Se il dominio della raccolta dati è [!DNL omtrdc.net] o se il CNAME è mappato a [!DNL omtrdc.net] sei all'interno dell'RDC. Consulta [Passaggio all'RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) per ulteriori informazioni. If you are using first-party cookies, refer to [CNAME and the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) for information about data collection CNAMEs and cross-domain tracking.

Si consiglia di modernizzare l'implementazione di Analytics aggiornando le librerie JavaScript, incluso l'API visitatore. Il modo più semplice per farlo è aggiungere uno strumento [!DNL Adobe Analytics] in Dynamic Tag Management specificando *`Automatic`* come metodo di configurazione.

In Dynamic Tag Management, fai clic su **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Panoramica]**&gt;**[!UICONTROL Aggiungi uno strumento]**&gt;**[!UICONTROL Adobe Analytics]**. Consulta[Impostazioni Adobe Analytics](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)in Dynamic Tag Management per informazioni sulla distribuzione.

## Passaggio 5: (Adobe Target) Modernizzazione dell'implementazione di Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Si consiglia di aggiungere uno [strumento Adobe Target](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html) in Dynamic Tag Management per rendere automatico il recupero della libreria. In Dynamic Tag Management, fai clic su **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Panoramica]**&gt;**[!UICONTROL Aggiungi uno strumento]**&gt;**[!UICONTROL Adobe Target]**.** Nota:**puoi anche utilizzare Dynamic Tag Management per distribuire il servizio Experience Cloud ID per Target (e altre soluzioni). Per poter utilizzare i servizi di base**&#x200B;è necessario **aggiornare il servizio Experience Cloud ID per Target.
* Se non utilizzi Dynamic Tag Management, [aggiorna la tua libreria mbox](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) manualmente.
* Richiedi l'accesso per utilizzare Adobe Analytics come fonte di reporting per Adobe Target. I dati di Target e Analytics sono combinati nella stessa chiamata al server durante l'elaborazione affinché i visitatori siano collegati tra le due soluzioni. Consulta [Analytics per implementazione di Target](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html).
* 
   >[!IMPORTANT]
   >
   >Tutti i clienti Analytics dispongono già del provisioning per i servizi di base, come Attributi del cliente. Se non sei cliente Analytics, contatta l'Assistenza clienti per richiedere il provisioning.

## Passaggio 6: Verifica dell'implementazione dei servizi di base {#section_E641782A0F4F44AF8C9C91216BE330D5}

Utilizza il seguente procedimento per assicurarti che il servizio Experience Cloud ID sia correttamente implementato sul sito.

1. Elimina i cookie dal sito in uso affinché sia possibile visualizzare la richiesta al Experience Cloud ID (la richiesta viene effettuata alla prima visita, quindi circa una volta a settimana per ciascun visitatore).1. Utilizzando un analizzatore di pacchetti o il pannello di rete in un debugger del browser Web, cerca una richiesta indirizzata a [!DNL dpm.demdex.net].
1. Verifica che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verifica che la richiesta di Analytics contenga il parametro di mezzo (il Experience Cloud ID). Nel periodo di prova (se disponibile) dovrebbe essere visibile un parametro d'aiuto (l'ID visitatore di Analytics).

Risposta prevista contenente il Experience Cloud ID:

![](assets/mac_id_response.png)

Immagine della richiesta di Analytics contenente il Experience Cloud ID (mid):

![](assets/mid.png)

Experience Cloud ID nella richiesta mbox:

![](assets/mbox_request.png)

**Cos'è il periodo di prova?**

Dopo la distribuzione del servizio ID visitatore, i nuovi visitatori non ricevono più un ID visitatore di Analytics dal server di raccolta dati. Se le sezioni del sito non hanno ancora implementato il servizio ID visitatore, quando i visitatori accedono a tali sezioni, Experience Cloud ID non viene riconosciuto e ai visitatori viene assegnato un ID visitatore legacy di Analytics. Ciò può causare potenziali problemi, tra cui visite duplicate e attribuzione errata.

Ad esempio, se la sezione di assistenza del sito viene gestita in un CMS separato, dovresti avere un file JavaScript di Analytics separato per tale sezione. Se distribuisci l'ID visitatore sul sito principale prima di distribuire l'Analytics ID al sito di assistenza, i nuovi visitatori riceveranno un ID legacy di Analytics al momento della visita della sezione di assistenza e le visite che si estendono a entrambe le sezioni saranno riportate come visite diverse.

La distribuzione del servizio ID visitatore su siti che utilizzano file JavaScript multipli o altre tecnologie (come Flash) può causare problemi di coordinazione in quanto è necessario abilitare il servizio ID visitatore su tutte le parti del sito contemporaneamente. Configurando un periodo di prova, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID visitatore affinché i visitatori possano essere costantemente identificati nelle sezioni del sito non aggiornate all'utilizzo del servizio ID visitatore.

## Passaggio 7: Gestione di utenti e prodotti {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Quando tutto è pronto, vai a **[!UICONTROL Amministrazione]** &gt; **[!UICONTROL Avvia Admin Console]** per gestire gli utenti e i profili di prodotto.

![](assets/menu-administration-shell.png)

Consulta [Gestione di utenti e prodotti Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

**Attributi del cliente**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi cliente] presente sul lato sinistro dell'interfaccia Experience Cloud

## Passaggio 8: Utilizzare i servizi di base {#section_960C06093623462E8EA247B3E97274A1}

Utilizza le seguenti funzionalità del servizio di base.

![](assets/menu-audiences-shell.png)

**Persone &gt; Attributi del cliente**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta effettuato l'aggiornamento, sfrutta i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Consulta [Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**Persone &gt; Libreria Pubblico**

Experience Cloud Audiences è l'interfaccia che consente di creare tipi di pubblico, o audience, combinare quelli esistenti per creare un pubblico composito e visualizzare quelli condivisi.

Consulta [Audiences](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## Archivio dei dati e informativa sulla privacy

Se si usa la profilazione del pubblico in tempo reale e altri servizi core in Adobe [!DNL Experience Cloud], l’uso di questi servizi potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché i servizi core di Adobe [!DNL Experience Cloud] usano Adobe Audience Manager, i dati utilizzati nel servizio core persone devono trovarsi nei server di Audience Manager negli Stati Uniti.

Quando si usano i servizi core resi disponibili tramite il servizio core persone, i tipi di dati inviati da altri prodotti Adobe alla gestione dell'audience sono:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l'indirizzo IP, incluso l'ultimo ottetto dell'IP (partendo dal presupposto che l'indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell'IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base a regole impostate in Audience Manager.
* (Facoltativo) Uno o più degli ID. In base al tipo di implementazione del servizio ID, puoi effettuare invii mediante uno o più degli ID, come ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti ad Adobe Gestione dell'audience. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Consiglia invece di utilizzare hash univoci per creare uno pseudonimo dei dati prima di inviarli ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. Il cookie di prime parti `AMCV_###@AdobeOrg` è sempre impostato con Experience Cloud ID (già ID visitatore).


Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia tali dati negli Stati Uniti. Audience Manager non fornisce un'opzione per archiviare o elaborare tali dati al di fuori degli Stati Uniti.

**Cookie e rinunce**

L'utilizzo di profili in tempo reale sfrutta il cookie di Audience Manager oltre ai cookie utilizzati per [!DNL Analytics] e [!DNL Target].

Se desideri fornire ai visitatori del sito la funzionalità di rinuncia, devi aggiungere la rinuncia a Audience Manager nel processo di rinuncia esistente.

Per le istruzioni vedi [Adobe Experience Cloud - Implementazione rinunce Adobe](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html).

Per abilitare il tracciamento tra domini vedi [CNAME raccolta dati e tracciamento tra domini](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html).
