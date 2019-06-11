---
description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per funzionalità di servizi di base come gli attributi dei clienti e i tipi di pubblico.
keywords: servizi di base; attributi del cliente
seo-description: Implementa Experience Cloud e diventa amministratore. Questa procedura consente di modernizzare le soluzioni per funzionalità di servizi di base come gli attributi dei clienti e i tipi di pubblico.
seo-title: Abilitare le soluzioni Experience Cloud per i servizi di base
solution: Experience Cloud
title: Abilita le tue soluzioni per i servizi di base
uuid: 5820060 f -9 b 18-4339-81 e 0-401 d 964 f 7 a 03
translation-type: tm+mt
source-git-commit: b4809ff0b4546f105ac6270eca1bfce2b6467876

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
>Per Target, [migrate a. js da mbox. js](https://marketing.adobe.com/resources/help/en_US/target/ov2/t_target-migrate-atjs.html).


![](assets/step2_icon.png) Modernizza la tua implementazione ed effettua il provisioning di un amministratore.


1. Segui i passaggi riportati di seguito in [Distribuzione del servizio Experience Cloud ID](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
1. Contatta il tuo account manager e inizia il processo di provisioning per Experience Cloud.

![](assets/step3_icon.png) Gestisci utenti e prodotti in Admin Console.

**Accesso amministratore**

Se hai il ruolo di amministratore, puoi accedere a [marketing.adobe.com](https://marketing.adobe.com).

Dovresti visualizzare il collegamento **[!UICONTROL Amministrazione]nel menu di navigazione di Experience Cloud.**

Consulta [l&#39;Aiuto di Experience Cloud per utenti e](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) prodotti.

**Accesso utente**

Per accedere a Experience Cloud i tuoi utenti devono:


1. Avere un Adobe ID.
1. Sign in at [!DNL marketing.adobe.com].
1. Appartenere a un gruppo di una soluzione mappato su un gruppo enterprise.
1. Se necessario, collegare i loro account soluzione ai loro Adobe ID (come descritto di seguito).

![](assets/step4_icon.png) Facoltativo: collega gli account utente esistenti.

Probabilmente hai degli utenti che sono già membri di gruppi di soluzioni, come un gruppo Analytics gestito in Analytics &gt; Strumenti di amministrazione.

Quando mappi questi gruppi su gruppi aziendali di Experience Cloud, questi utenti devono collegare manualmente le credenziali account della loro soluzione al loro Adobe ID.

Consulta [Collegamento di account in Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> Dopo la mappatura dei gruppi aziendali e delle soluzioni, i nuovi utenti vengono collegati automaticamente. (le credenziali della soluzione vengono automaticamente create e collegate al proprio Adobe ID).

Le sezioni seguenti descrivono come modernizzare la propria implementazione per abilitare i servizi di base in Experience Cloud.

## Passaggio 2: Implementazione del servizio Experience Cloud ID tramite Dynamic Tag Manager o Launch, di Adobe {#section_3C9F6DF37C654D939625BB4D485E4354}

Il metodo più semplice per abilitare i servizi di base di Experience Cloud è quello di attivarli automaticamente per Analytics e Target, mediante lo [strumento del servizio Experience Cloud ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-dtm-implement.html) in Dynamic Tag Manager (o Launch, di Adobe).

![](assets/menu-activation-shell.png)

Per il servizio completo Experience Cloud ID (già ID visitatore), passa a [questa pagina](https://marketing.adobe.com/resources/help/en_US/mcvid/).

Inoltre, la gestione tag di nuova generazione è [Launch, di Adobe](https://marketing.adobe.com/resources/help/en_US/experience-cloud/launch/).

**Non utilizzi Dynamic Tag Management o Launch?**

Se non utilizzi Dynamic Tag Management, implementa manualmente il servizio ID tramite la distribuzione JavaScript ([!DNL VisitorAPI.js]), come segue:

1. Effettua i passaggi descritti in [Implementazione del sevizio Experience Cloud ID per Analytics](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html).

   Adobe consiglia inoltre di impostare [ID cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) aggiuntivi. Tali ID sono associati a ciascun visitatore e abilitano le funzionalità attuali e future dei servizi di base di Experience Cloud.

1. Aggiorna il file [!DNL s_code] esistente alla versione H.27.3 o successiva oppure il file [!DNL AppMeasurement.js] esistente alla versione 1.4 o successiva.

   Tali file sono disponibili per il download in [Gestore codice](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=code_manager_admin) in Strumenti amministratore di Analytics.

   (La guida [Implementazione di JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html) è disponibile per ulteriori informazioni su [!DNL AppMeasurement.js]).

1. Sincronizza l&#39;ID cliente per Analytics. Consulta [Analytics - Sincronizzazione dell&#39;ID cliente](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (di seguito).

## Analytics e Target - Sincronizzazione dell&#39;ID cliente {#section_AD473A6A21C1446498E700363F9A8437}

In qualità di parte dell&#39;impostazione del servizio Experience Cloud ID, per Analytics e Target Adobe consiglia di sincronizzare gli [ID cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) con Experience Cloud.

In Target, [!DNL mbox3rdpartyid] deve ottenere l&#39;ID cliente e inviarlo a Target (consulta [Utilizzo degli attributi cliente](https://marketing.adobe.com/resources/help/en_US/target/target/c_working-with-customer-attributes.html) in Target).

Quando un visitatore si autentica su un tuo sito Web o in generale si identifica, l&#39;implementazione deve esporre l&#39;ID cliente CRM della persona nella pagina o nell&#39;applicazione. Puoi quindi utilizzare la funzionalità appropriata per sincronizzare l&#39;ID cliente a Experience Cloud. La sincronizzazione archivia l&#39;ID cliente CRM del visitatore in Experience Cloud e attiva gli attributi del cliente per l&#39;utilizzo in Experience Cloud.

Ad esempio, si supponga che Bob sia associato all&#39;ID cliente `52mc210tr42` nel sistema CRM in uso. Quando Bob si autentica sul sito Web, devi esporre tale ID sulla pagina e utilizzarlo per sincronizzarlo in uno dei due modi:

* Chiama `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` il servizio ID visitatore. oppure
* Compilazione di *`Customer ID (52mc210tr42)`* una prop o evar.


L&#39;ID cliente deve essere impostato su ciascuna chiamata al server di [!DNL Analytics] in cui è noto l&#39;ID cliente.

**SDK per dispositivi mobili**

Consulta *la sezione del servizio* Experience Cloud ID per esempi di sintassi su come impostare ID cliente aggiuntivi nelle [applicazioni mobili Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods) e [iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods) .

**Abilitazione degli attributi per i dati presenti nella cronologia**

I dati dell&#39;attributo cliente sono disponibili dopo l&#39;accesso dei visitatori. Se non hai ancora implementato l&#39;ultimo servizio Experience Cloud ID e se stai tenendo traccia degli ID cliente in una prop o eVar, puoi richiedere un procedimento che invia gli accessi cronologici a Experience Cloud. Tale procedimento consente di iniziare a usare gli attributi del cliente immediatamente.

Contatta l&#39;Assistenza clienti per abilitare i dati presenti nella cronologia.

## Passaggio 3: Mappatura di suite di rapporti per un’organizzazione Experience Cloud {#section_7B08516B01BA421681DF03D0E86CE3BA}

I servizi Experience Cloud (come Experience Cloud ID e persone) sono associati con una suite di rapporti di un&#39;organizzazione invece che con una sola suite di rapporti. Per garantire il funzionamento corretto di questi servizi, ogni suite di rapporti di Analytics deve essere mappata su un&#39;organizzazione Experience Cloud.

Consultate [Mappare suite di rapporti su un&#39;organizzazione](report-suite-mapping.md).

## Passaggio 4: (Adobe Analytics) Modernizzazione del codice AppMeasurement di Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Verifica di essere nella raccolta dati regionale (RDC). Se il dominio della raccolta dati è [!DNL omtrdc.net] o se il CNAME è mappato a [!DNL omtrdc.net] sei all&#39;interno dell&#39;RDC. Consulta [Passaggio all&#39;RDC](https://marketing.adobe.com/resources/help/en_US/whitepapers/rdc/?f=rdc_transition) per ulteriori informazioni. Se stai utilizzando cookie di terze parti, fai riferimento a [CNAME e servizio ID visitatore](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname) per informazioni sulla raccolta dei dati e sul tracciamento tra domini.

Si consiglia di modernizzare l&#39;implementazione di Analytics aggiornando le librerie JavaScript, incluso l&#39;API visitatore. Il modo più semplice per farlo consiste nell&#39;aggiungere uno [!DNL Adobe Analytics] strumento in Gestione tag dinamica, specificando *`Automatic`* come metodo di configurazione.

In Gestione tag dinamica, fai clic su **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Panoramica]**&gt;**[!UICONTROL Aggiungi uno strumento]**&gt;**[!UICONTROL Adobe Analytics]**. Consulta[Impostazioni Adobe Analytics](https://marketing.adobe.com/resources/help/en_US/dtm/?f=analytics_dtm)in Dynamic Tag Management per informazioni sulla distribuzione.

## Passaggio 5: (Adobe Target) Modernizzazione dell&#39;implementazione di Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Si consiglia di aggiungere uno [strumento Adobe Target](https://marketing.adobe.com/resources/help/en_US/dtm/target.html) in Dynamic Tag Management per rendere automatico il recupero della libreria. In Gestione tag dinamica, fai clic su **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Panoramica]**&gt;**[!UICONTROL Aggiungi uno strumento]**&gt;**[!UICONTROL Adobe Target]**.** Nota:**puoi anche utilizzare Dynamic Tag Management per distribuire il servizio Experience Cloud ID per Target (e altre soluzioni). Per poter utilizzare i servizi di base** è necessario **aggiornare il servizio Experience Cloud ID per Target.
* Se non utilizzi Dynamic Tag Management, [aggiorna la tua libreria mbox](https://marketing.adobe.com/resources/help/en_US/target/ov/?f=t_mbox_download) manualmente.
* Richiedi l&#39;accesso per utilizzare Adobe Analytics come fonte di reporting per Adobe Target. I dati di Target e Analytics sono combinati nella stessa chiamata al server durante l&#39;elaborazione affinché i visitatori siano collegati tra le due soluzioni. Consulta [Analytics per implementazione di Target](https://marketing.adobe.com/resources/help/en_US/target/a4t/?f=a4t).
* 
   >[!IMPORTANT]
   >
   >Tutti i clienti Analytics hanno già il provisioning per i servizi di base come gli attributi del cliente. Se non sei cliente Analytics, contatta l&#39;Assistenza clienti per richiedere il provisioning.

## Passaggio 6: Verifica dell&#39;implementazione dei servizi di base {#section_E641782A0F4F44AF8C9C91216BE330D5}

Utilizza il seguente procedimento per assicurarti che il servizio Experience Cloud ID sia correttamente implementato sul sito.

1. Elimina i cookie dal sito in uso affinché sia possibile visualizzare la richiesta al Experience Cloud ID (la richiesta viene effettuata alla prima visita, quindi circa una volta a settimana per ciascun visitatore).1. Using a packet analyzer or the network panel in a web browser debugger, look for a request going to [!DNL dpm.demdex.net].
1. Verificate che la risposta contenga `d_mid` e un valore, ad esempio: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verifica che la richiesta di Analytics contenga il parametro di mezzo (il Experience Cloud ID). Nel periodo di prova (se disponibile) dovrebbe essere visibile un parametro d&#39;aiuto (l&#39;ID visitatore di Analytics).

Risposta prevista contenente il Experience Cloud ID:

![](assets/mac_id_response.png)

Immagine della richiesta di Analytics contenente il Experience Cloud ID (mid):

![](assets/mid.png)

Experience Cloud ID nella richiesta mbox:

![](assets/mbox_request.png)

**Cos&#39;è il periodo di prova?**

Dopo la distribuzione del servizio ID visitatore, i nuovi visitatori non ricevono più un ID visitatore di Analytics dal server di raccolta dati. Se le sezioni del sito non hanno ancora implementato il servizio ID visitatore, quando i visitatori accedono a tali sezioni, Experience Cloud ID non viene riconosciuto e ai visitatori viene assegnato un ID visitatore legacy di Analytics. Ciò può causare potenziali problemi, tra cui visite duplicate e attribuzione errata.

Ad esempio, se la sezione di assistenza del sito viene gestita in un CMS separato, dovresti avere un file JavaScript di Analytics separato per tale sezione. Se distribuisci l&#39;ID visitatore sul sito principale prima di distribuire l&#39;Analytics ID al sito di assistenza, i nuovi visitatori riceveranno un ID legacy di Analytics al momento della visita della sezione di assistenza e le visite che si estendono a entrambe le sezioni saranno riportate come visite diverse.

La distribuzione del servizio ID visitatore su siti che utilizzano file JavaScript multipli o altre tecnologie (come Flash) può causare problemi di coordinazione in quanto è necessario abilitare il servizio ID visitatore su tutte le parti del sito contemporaneamente. Configurando un periodo di prova, i nuovi visitatori continuano a ricevere un ID visitatore di Analytics dal servizio ID visitatore affinché i visitatori possano essere costantemente identificati nelle sezioni del sito non aggiornate all&#39;utilizzo del servizio ID visitatore.

## Passaggio 7: Gestione di utenti e prodotti {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Dopo aver effettuato l&#39;accesso, passa a **[!UICONTROL Amministrazione]** &gt; **[!UICONTROL Avvia Admin Console]**, dove puoi gestire gli utenti e i profili di prodotto.

![](assets/menu-administration-shell.png)

Consulta [la gestione di utenti e prodotti Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

**Attributi del cliente**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi cliente] presente sul lato sinistro dell&#39;interfaccia Experience Cloud

## Passaggio 8: Utilizzare i servizi di base {#section_960C06093623462E8EA247B3E97274A1}

Utilizza le seguenti funzionalità del servizio di base.

![](assets/menu-audiences-shell.png)

**Persone &gt; Attributi del cliente**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta caricati, utilizzate i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

Consulta [Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**Persone &gt; Libreria Pubblico**

Experience Cloud Audiences è l&#39;interfaccia che consente di creare tipi di pubblico, o audience, combinare quelli esistenti per creare un pubblico composito e visualizzare quelli condivisi.

Consulta [Audiences](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## Archivio dei dati e informativa sulla privacy

Se si usa la profilazione del pubblico in tempo reale e altri servizi core in Adobe [!DNL Experience Cloud], l’uso di questi servizi potrebbe influire sul datacenter (e sul paese) in cui si trovano i dati. In particolare, poiché i servizi core di Adobe [!DNL Experience Cloud] usano Adobe Audience Manager, i dati utilizzati nel servizio core persone devono trovarsi nei server di Audience Manager negli Stati Uniti.

Quando si usano i servizi core resi disponibili tramite il servizio core persone, i tipi di dati inviati da altri prodotti Adobe alla gestione dell&#39;audience sono:

* Coppie chiave/valore di [!DNL Analytics] (proprietà, eVars, variabili elenco e così via). Per impostazione predefinita, le righe del registro contengono l&#39;indirizzo IP, incluso l&#39;ultimo ottetto dell&#39;IP (partendo dal presupposto che l&#39;indirizzo IP non sia stato modificato dalle impostazioni di offuscamento dell&#39;IP di Adobe [!DNL Analytics]).
* Caratteristiche e segmenti per i quali i visitatori si qualificano in base a regole impostate in Audience Manager.
* (Facoltativo) Uno o più degli ID. In base al tipo di implementazione del servizio ID, puoi effettuare invii mediante uno o più degli ID, come ID CRM o indirizzi e-mail con hash. Se tali dati vengono inviati ad Adobe [!DNL Analytics], vengono trasferiti ad Adobe Gestione dell&#39;audience. Adobe consiglia di non fornire informazioni personali ad Adobe [!DNL Analytics]. Consiglia invece di utilizzare hash univoci per creare uno pseudonimo dei dati prima di inviarli ad Adobe.
* Segmenti originati in [!DNL Analytics] mediante la funzionalità back-end di condivisione del segmento.
* Il cookie demdex.net viene impostato se i cookie di terze parti non sono bloccati. Il cookie di prime parti `AMCV_###@AdobeOrg` è sempre impostato con Experience Cloud ID (già ID visitatore).


Tutti gli elementi di questi dati vengono inviati ad Adobe Audience Manager sotto forma di file di log. Audience Manager elabora e archivia tali dati negli Stati Uniti. Audience Manager non fornisce un&#39;opzione per archiviare o elaborare tali dati al di fuori degli Stati Uniti.

**Cookie e rinunce**

L&#39;utilizzo di profili in tempo reale sfrutta il cookie di Audience Manager oltre ai cookie utilizzati per [!DNL Analytics] e [!DNL Target].

Se desideri fornire ai visitatori del sito la funzionalità di rinuncia, devi aggiungere la rinuncia a Audience Manager nel processo di rinuncia esistente.

Per le istruzioni vedi [Adobe Experience Cloud - Implementazione rinunce Adobe](https://marketing.adobe.com/resources/help/en_US/sc/implement/opt_out.html).

Per abilitare il tracciamento tra domini vedi [CNAME raccolta dati e tracciamento tra domini](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname).
