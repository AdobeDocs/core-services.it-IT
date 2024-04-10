---
title: Gestione di utenti e prodotti
description: Accedi all’Admin Console e gestisci le autorizzazioni utente e i prodotti Experience Cloud (profili prodotto). Scopri come delegare le autorizzazioni di amministratore agli utenti di Experience Cloud, e i browser supportati da Experience Cloud.
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 74%

---

# Gestire utenti e prodotti in [!DNL Experience Cloud]

Scopri come accedere ad Admin Console e gestire le autorizzazioni degli utenti e i profili di prodotto di Experience Cloud e il supporto del browser.

>[!IMPORTANT]
>
>Le seguenti informazioni sono specifiche per le applicazioni di Experience Cloud. Questa guida integra le informazioni contenute nella [Guida utente per l’amministrazione di Enterprise](https://helpx.adobe.com/it/enterprise/admin-guide.html) per tutti i prodotti cloud di Adobe.

Puoi visualizzare un elenco ordinabile e filtrabile di tutti gli utenti Experience Cloud e dei relativi dettagli in Admin Tool. Consulta [Visualizzare gli utenti Experience Cloud in Admin Tool](admin-tool-experience-cloud.md).

## Avviso di aggiornamento del provisioning{#provisioning}

Aggiornato: **20 luglio 2022**

>[!IMPORTANT]
>
>Consulta il seguente avviso relativo al provisioning di Experience Cloud.

Adobe sta aggiornando il provisioning per fornire a tutti i clienti di Experience Cloud l’accesso alle funzionalità fondamentali che facilitano l’interoperabilità tra alcuni prodotti Experience Cloud. Adobe Experience Platform verrà aggiunto come nuovo diritto alle organizzazioni Experience Cloud, con la funzionalità [!UICONTROL Raccolta dati] inclusa come servizio.

La funzionalità [!UICONTROL Raccolta dati] di Adobe Experience Platform include [tag](https://experienceleague.adobe.com/en/docs/tags) per una gestione dei tag semplificata e universale e offre un’infrastruttura di dati in streaming affidabile, solida e completa. I tag semplificano la raccolta di dati sull’esperienza del cliente e agevolano la distribuzione delle esperienze.

**Modifiche al[!DNL Admin Console]**

Gli amministratori possono visualizzare modifiche o aggiunte al [!DNL Admin Console] come segue:

* La scheda prodotto di Adobe Experience Platform nell’Admin Console include:

   * Places
   * Assurance
   * Spazio dei nomi identità
   * Sandbox
   * Experience Data Model
   * Schemi
   * Stream di dati
   * ID visitatore

  Per le organizzazioni che attualmente non utilizzano Experienci Platform, ora vedrai il _Adobe Experience Platform_ prodotto in [!DNL Admin Console], incluse le funzionalità elencate in precedenza.

  Per le organizzazioni che attualmente utilizzano Experience Platform, _Places_ sarà adesso accorpato nella scheda di Experience Platform.

* Le funzionalità Raccolta dati (in precedenza Launch) e Privacy di Adobe Experience Platform continueranno a essere disponibili come schede di prodotto distinte rispetto alle altre funzionalità di Experience Platform.

Per maggiori dettagli sulle nuove funzionalità, visita le rispettive pagine su Experience League:

* [Raccolta dati](https://experienceleague.adobe.com/docs/discontinued/using/reports-and-analytics.html?lang=it)
* [Places](https://experienceleague.adobe.com/en/docs/places/using/home)
* [Assurance](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance.html?lang=it)
* [Spazio dei nomi identità](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it)
* [Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=it)
* [Experience Data Model](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it)
* [Schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it)
* [Stream di dati](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it)
* [ID visitatore](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html?lang=it#section_3C9F6DF37C654D939625BB4D485E4354)
* [Privacy](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it)

## Autenticazione utente di Experience Cloud (migrazione pianificata){#migration}

A partire da febbraio 2022, Adobe aggiorna il sistema di gestione dei profili per consentire alle organizzazioni di gestire meglio le licenze aziendali per i singoli profili. Di conseguenza, tutti gli utenti con un profilo personale, che corrisponde a un singolo Adobe ID (Type1), verranno migrati a un nuovo profilo Business. Questo profilo corrisponde a un _Business ID_ (Type2e).

Consulta [Tipi di identità nell’Adobe [!DNL Admin Console]](https://helpx.adobe.com/it/enterprise/using/identity.html) per informazioni sui tipi di identità.

### Processo di migrazione

Quando è il momento, gli amministratori dell’organizzazione ricevono un’e-mail di notifica 30 giorni prima della migrazione.

* La migrazione sarà programmata tra le ore 22:00 e le 06:00 in base al fuso orario principale dell’organizzazione o nel fine settimana.
* Durante la migrazione, l&#39;applicazione di Experience Cloud può essere inaccessibile per circa 15 minuti e [!DNL Admin Console] può essere inaccessibile fino a 30 minuti. Per il resto, la migrazione sarà senza soluzione di continuità.

### Modifiche dopo la migrazione

[!DNL Admin Console]

* Gli amministratori con più account possono visualizzare un selettore di profilo al momento dell’accesso [!DNL Admin Console].
* I singoli utenti di Adobe ID vengono aggiornati a Business ID.
* La directory Business ID viene aggiunta in **[!UICONTROL Impostazioni]** > **[!UICONTROL Identità]** > **[!UICONTROL Directory]**.

  ![[!DNL Admin Console] Identità - Business ID](assets/identity-home.png)

### Accesso dopo la migrazione

L’esperienza di accesso non cambia con questo aggiornamento:

1. Accedi a `experience.adobe.com` utilizzando le stesse credenziali.

1. Viene creato un nuovo profilo associato al Business ID. Ti viene chiesto di scegliere tra **[!UICONTROL Iscriviti subito]** o **[!UICONTROL Salta]**.

1. Ciascuna opzione porta a una pagina di destinazione esistente.

1. A ciascun piano aziendale è associato un profilo di Adobe che consente di organizzare le risorse create da ulteriori offerte Adobe Cloud (Creative Cloud e Document Cloud).

Per ulteriori informazioni, consulta [Introduzione ai profili Adobe](https://helpx.adobe.com/it/enterprise/kb/introducing-adobe-profiles.html).

## Che cos’è un profilo di prodotto? {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL Profili di prodotto]_ sono gruppi di prodotti e servizi che puoi assegnare agli utenti. In Experience Cloud, le autorizzazioni si basano sul profilo di un prodotto, non sull’utente. (Tuttavia, puoi delegare i diritti amministrativi a utenti specifici.)

In Analytics, ad esempio, puoi configurare una raccolta di strumenti di reporting, quali Analysis Workspace e Report Builder, insieme a suite di rapporti, metriche e dimensioni. Per assegnare le autorizzazioni per un prodotto puoi aggiungerlo al profilo.

* Consulta [Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391), in questa pagina.
* Consulta la pagina [Delegare i ruoli di amministratore agli utenti](#delegate-rights).

## Gestire i profili di prodotto di Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Puoi creare un profilo di prodotto e assegnarlo a un gruppo di autorizzazioni.

Quando inviti un utente in un&#39;organizzazione, puoi concedergli l&#39;accesso a prodotti e profili di prodotto, Puoi anche delegare autorizzazioni amministrative limitate a un utente. Allo stesso modo, puoi creare gruppi di utenti, quindi aggiungere il gruppo a un profilo di prodotto per permettere l&#39;accesso.

1. In [[!DNL Admin Console]](https://adminconsole.adobe.com/enterprise/), seleziona **[!UICONTROL Prodotti]**.
1. Fai clic sul nome della tua organizzazione.
1. Seleziona **[!UICONTROL Nuovo profilo]**.
1. Configura i dettagli del profilo, quindi seleziona **[!UICONTROL Salva]**.

Per ulteriori informazioni (e per assistenza sulla gestione dei prodotti Creative Cloud e Document Cloud), consulta [Identità](https://helpx.adobe.com/it/enterprise/using/identity.html) nella [Guida utente per l’amministrazione](https://helpx.adobe.com/it/enterprise/using/users.html).

**Argomenti correlati**

* [Gestione utenti](https://helpx.adobe.com/it/enterprise/using/users.html) in [!DNL Admin Console]
* [Gestire prodotti e profili](https://helpx.adobe.com/it/enterprise/using/manage-products.html) in [!DNL Admin Console].
* [Autorizzazioni di utenti Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=it) nella guida di Adobe Target per maggiori informazioni
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe [!DNL Admin Console]](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=it)

## Delega di ruoli amministrativi a utenti {#delegate-rights}

In entrata [!DNL Admin Console], puoi delegare diritti amministrativi limitati ad altri nell’organizzazione. I ruoli delegati consentono agli utenti di fornire l&#39;accesso software agli utenti finali, fornire le funzionalità di distribuzione dell&#39;accesso e fungere da delegati di supporto.

Sarà possibile, ad esempio:

* Consentire al tuo direttore creativo di concedere l&#39;accesso a Creative Cloud.
* Consenti al tuo direttore marketing di concedere l&#39;accesso a Experience Cloud.
* Mantenere questi due ruoli separati in modo che non possano sovrapporsi.

Utilizzando questi ruoli, puoi delegare simultaneamente la gestione ad altri senza fornire più funzionalità di quelle necessarie.

1. In [!DNL Admin Console], seleziona **[!UICONTROL Utenti]**, quindi selezionare il nome dell&#39;utente.

   ![Diritti di amministrazione in [!DNL Admin Console]](assets/edit-admin-rights.png)

1. Seleziona **[!UICONTROL Modifica diritti amministratore]**.

   ![Modificare i diritti di amministrazione in [!DNL Admin Console]](assets/edit-admin-rights-page.png)

1. Specifica i diritti di amministrazione dell’utente.
1. Seleziona **[!UICONTROL Salva]**.

## Gestire utenti e prodotti in Analytics {#section_97DE101F92CD494AB073893680992F1A}

Puoi assegnare le autorizzazioni di accesso ai rapporti di Analytics (suite di rapporti, metriche, dimensioni e così via) a un profilo di prodotto.

Ad esempio, puoi creare un profilo di prodotto contenente più strumenti di Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] e [!UICONTROL Report Builder]). Questi profili contengono l’autorizzazione per metriche e dimensioni specifiche (comprese le eVar) e funzionalità come segmenti o creazione di metriche calcolate.

1. Accedi a [[!DNL Admin Console]](https://adminconsole.adobe.com/enterprise), quindi seleziona **[!UICONTROL Prodotti]**.
1. Nella pagina [!UICONTROL Prodotti], seleziona il prodotto, quindi **[!UICONTROL Autorizzazioni]** (disponibile solo per gli amministratori).
1. Configura le autorizzazioni del profilo:

| Elemento | Descrizione |
|--- |--- |
| Suite di rapporti | Attiva le autorizzazioni per suite di rapporti specifiche. |
| Metriche | Attiva le autorizzazioni per traffico, conversione, eventi personalizzati, eventi delle applicazioni, in base al contenuto e così via. |
| Dimensioni | Personalizza l’accesso degli utenti a un livello granulare, inclusi eVar e rapporti sul traffico, sulle applicazioni e sui percorsi. |
| Strumenti delle suite di rapporti | Attiva le autorizzazioni degli utenti per servizi web, gestione delle suite di rapporti, strumenti, rapporti ed elementi del dashboard. |
| Strumenti di Analytics | Attiva le autorizzazioni degli utenti per elementi generali (fatturazione, registri e così via), gestione società, strumenti, accesso ai servizi web, Report Builder e integrazione con Data Connectors. Impostazioni aziendali da Personalizza [!DNL Admin Console] la categoria è stata spostata in Strumenti di Analytics. |

**Migrazione degli account utente**

È disponibile uno strumento di migrazione degli ID utente di Analytics che permette agli amministratori di trasferire gli account utente da Gestione utenti di Analytics a [Adobe [!DNL Admin Console]](https://adminconsole.adobe.com/enterprise/).

La migrazione diventerà disponibile per i clienti in più fasi. Adobe ti invierà una notifica e ti fornirà assistenza quando arriverà il tuo momento di trasferire gli account utente esistenti da **[!UICONTROL Strumenti di amministrazione]** > **[!UICONTROL Gestione utente]** al [!DNL Admin Console].

Dopo la migrazione, gli utenti potranno accedere con il proprio Adobe ID (o Enterprise ID) e autenticarsi nelle applicazioni e nei servizi Experience Cloud nella pagina [experience.adobe.com](https://experience.adobe.com). Gli utenti che tenteranno di accedere con i metodi precedenti ([!DNL my.omniture.com], [!DNL sc.omniture.com] e [!DNL experiencecloud.adobe.com]) verranno reindirizzati a [!DNL experience.adobe.com].

**Argomenti correlati**

* [Analytics in [!DNL Admin Console]](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=it)
* [Migrazione degli ID utente di Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/migrate-users/c-migration-tool.html?lang=it)

## Gestire Adobe Target: profili di prodotto e aree di lavoro {#section_3860AF177C9E4C7E9C390D36A414F353}

In Adobe Target, un&#39;area di lavoro è un profilo di prodotto. Consente a un&#39;organizzazione di assegnare una serie di utenti specifica a una serie di proprietà specifica. In vari modi, un&#39;area di lavoro è simile a una suite di rapporti in Adobe Analytics.

Vedi:

* [Autorizzazioni per gli utenti Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=it)
* [Gestire prodotti e profili](https://helpx.adobe.com/it/enterprise/using/manage-products.html)
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe [!DNL Admin Console]](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=it)

## Gestire profili di prodotto, tenant e gruppi di sicurezza in Campaign {#section_09CDF75366444CF5810CF321B7C712F3}

Un *tenant* in Campaign viene visualizzato come *prodotto* nella pagina Prodotti di Admin Console.

Un *gruppo di sicurezza* viene visualizzato come un profilo di prodotto.

Consulta [Gestione di gruppi e utenti](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=it) per informazioni sui gruppi di sicurezza e sull&#39;assegnazione di utenti ai gruppi di sicurezza.

## Raccolta dati di Adobe Experience Platform {#section_F2DA6778DD2D48AA8F794041971EE6B1}

La [!UICONTROL Raccolta dati] di Experience Platform (Launch) viene visualizzata sulla pagina[!UICONTROL Prodotti] in [!UICONTROL Admin Console]. Puoi includere altre applicazioni e servizi in un profilo di prodotto Data Collection.

Invita gli utenti in [!UICONTROL Platform Launch] e assegna ruoli utente e autorizzazioni.

Consulta [Autorizzazioni utente](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=it) per informazioni sulle autorizzazioni per gli utenti in [!DNL Admin Console] e sull’impostazione dei diritti per i profili.

## Experience Manager as a Cloud Service

Adobe Nell’Adobe, i clienti Enterprise sono rappresentati come organizzazioni. [!DNL Admin Console]. I clienti Experience Manager possono utilizzare l’Adobe [!DNL Admin Console] per gestire le adesioni ai prodotti e l’autenticazione IMS per Experience Manager as a [!UICONTROL Cloud Service].

Consulta [Supporto IMS per Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/security/ims-support.html?lang=it).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Crea utenti Audience Manager e assegnali a gruppi. Puoi anche visualizzare i limiti (caratteristiche, segmenti, destinazioni e [!DNL AlgoModel]).

Consulta [Amministrazione](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=it) nella guida di Audience Manager.

## Browser supportati in Experience Cloud

* [!DNL Microsoft® Edge] (Microsoft® ha [terminato il supporto](https://www.microsoft.com/it-it/WindowsForBusiness/End-of-IE-support) per Internet Explorer 8, 9 e 10. Di conseguenza, Adobe non corregge i problemi segnalati riguardanti queste versioni specifiche di Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** sebbene l’interfaccia di Experience Cloud supporti questi browser, le singole applicazioni non supportano tutti i browser. (per esempio, [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=it) non supporta [!DNL Opera] e [!DNL Adobe Target] non supporta [!DNL Safari]).

### Requisiti di soluzioni e prodotti

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=it)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=it)
