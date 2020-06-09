---
description: Scopri come accedere ad Admin Console e gestire le autorizzazioni degli utenti e i profili di prodotto di Experience Cloud e il supporto del browser.
keywords: core services
seo-description: Scopri come accedere ad Admin Console e gestire le autorizzazioni degli utenti e i profili di prodotto di Experience Cloud e il supporto del browser.
seo-title: Gestione di utenti e prodotti Experience Cloud
solution: Experience Cloud
title: Gestione di utenti e prodotti Experience Cloud
index: true
translation-type: tm+mt
source-git-commit: 01277057733cb921ebfbb7e66a3e34cdd1e21829
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 95%

---


# Gestione di utenti e prodotti Experience Cloud {#topic_3FCB4099640647E3B2411ADBFCE81909}

Scopri come accedere ad Admin Console e gestire le autorizzazioni degli utenti e i profili di prodotto di Experience Cloud e il supporto del browser.

>[!IMPORTANT]
>
>La gestione degli utenti in Admin Console prevede l’utilizzo di nuovi termini, interfacce e modalità di navigazione. Le informazioni riportate di seguito descrivono questi nuovi aspetti e contengono collegamenti a ulteriori risorse di aiuto. Questa guida integra le informazioni contenute nella [Guida utente per l’amministrazione di Enterprise](https://helpx.adobe.com/it/enterprise/managing/user-guide.html) per tutti i prodotti cloud di Adobe.

## Novità nella gestione degli utenti in Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Scopri le nuove funzioni nella gestione degli utenti di Experience Cloud.

<!-- ### Business ID type

Adobe is introducing an identity type called _Business ID_. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.) -->

### Admin Tool

Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti Experience Cloud e dei relativi dettagli in Admin Tool. Consulta [Visualizzare gli utenti Experience Cloud in Admin Tool](admin-tool-experience-cloud.md).

## Accesso ad Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Gli amministratori non gestiscono più gli utenti nelle soluzioni. La gestione di utenti e prodotti Experience Cloud ora avviene in Admin Console.

Per accedere ad Admin Console:

1. Vai su [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Digita il tuo [Adobe ID o Enterprise ID](https://helpx.adobe.com/it/enterprise/help/identity.html) e la relativa password.

In alternativa, dal menu Experience Cloud ( ![](assets/menu-icon.png)), fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Avvia Admin Console]**.

**Argomenti correlati**

[Guida utente all’amministrazione](https://helpx.adobe.com/it/enterprise/using/users.html) per Creative Cloud e Document Cloud. Alcune informazioni riguardano la gestione degli utenti di Experience Cloud, ad esempio la [gestione dei tipi di identità](https://helpx.adobe.com/it/enterprise/help/identity.html).

[Accedi e gestisci le impostazioni del tuo profilo](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) per gestire password, organizzazioni e notifiche.

## Profili di prodotto e gruppi  {#section_AB50558124D541CF80A0D3D76D35A4BF}

L’aggiunta dei profili di prodotto rappresenta un cambiamento rispetto al modo in cui i prodotti e i servizi delle soluzioni erano gestiti in precedenza (utilizzando i gruppi). In Admin Console, le autorizzazioni si basano sui profili di prodotto, ovvero gruppi di prodotti e servizi che puoi assegnare agli utenti.

In Analytics, ad esempio, puoi configurare una serie di strumenti di reporting, quali Analysis Workspace e Report Builder, insieme a suite di rapporti, metriche, dimensioni e così via. Puoi autorizzare gli utenti ad accedere a un profilo di prodotto aggiungendoli al profilo. Consulta [Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Argomenti correlati**

[Delegare diritti amministrativi limitati](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Le autorizzazioni relative a utenti e prodotti Analytics vengono gestite in Admin Console.

[Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (in questa pagina).

**Migrazione degli account utente**

È disponibile uno strumento di migrazione degli ID utente di Analytics che permette agli amministratori di trasferire gli account utente da Gestione utenti di Analytics ad [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migrazione diventerà disponibile per i clienti in più fasi. Adobe ti invierà una notifica e ti fornirà assistenza quando arriverà il tuo momento di trasferire gli account utente esistenti da **[!UICONTROL Strumenti di amministrazione]** > **[!UICONTROL Gestione utenti]** all’Admin Console.

Dopo la migrazione, gli utenti effettueranno l’accesso utilizzando il proprio Adobe ID (o Enterprise ID) e si autenticheranno nelle soluzioni e nei servizi Experience Cloud nella pagina [experiencecloud.adobe.com](https://experiencecloud.adobe.com). Gli utenti che tenteranno di accedere con i metodi precedenti ([!DNL my.omniture.com] e [!DNL sc.omniture.com]) verranno reindirizzati a [!DNL experiencecloud.adobe.com].

**Argomenti correlati**

[Migrazione degli ID utente di Analytics](https://docs.adobe.com/content/help/it-IT/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target: profili di prodotto e aree di lavoro {#section_3860AF177C9E4C7E9C390D36A414F353}

In Adobe Target, un’area di lavoro è un profilo di prodotto. Consente a un&#39;organizzazione di assegnare una serie di utenti specifica a una serie di proprietà specifica. In vari modi, un’area di lavoro è simile a una suite di rapporti in Adobe Analytics.

Vedi:
* [Autorizzazioni per gli utenti Enterprise](https://docs.adobe.com/content/help/it-IT/target/using/administer/manage-users/enterprise/property-channel.html)
* [Gestire prodotti e profili](https://helpx.adobe.com/it/enterprise/using/manage-products-and-profiles.html)
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe Admin Console](https://helpx.adobe.com/it/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign: profili di prodotto, tenant e gruppi di sicurezza {#section_09CDF75366444CF5810CF321B7C712F3}

Un *tenant* in Campaign viene visualizzato come *prodotto* nella pagina Prodotti di Admin Console.

Un *gruppo di sicurezza* viene visualizzato come un profilo di prodotto.

Consulta [Gestione di gruppi e utenti](https://docs.adobe.com/content/help/it-IT/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html) per informazioni sui gruppi di sicurezza e sull’assegnazione di utenti ai gruppi di sicurezza.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch viene visualizzato sulla pagina Prodotti in Admin Console. Puoi includere altre soluzioni e altri servizi in un profilo di prodotto Launch.

Consulta [User Management](https://docs.adobe.com/content/help/it-IT/launch/using/reference/admin/user-permissions.html) per informazioni sulle autorizzazioni degli utenti in Admin Console e configura opzioni specifiche per Launch, tra cui l’assegnazione di diritti ai profili.

## Experience Manager as a Cloud Service

I clienti Adobe Enterprise sono rappresentati come organizzazioni IMS in Adobe Admin Console. Questo è il portale utilizzato dai clienti Adobe per gestire le adesioni dei prodotti per i loro utenti e gruppi. I clienti AEM possono utilizzare Adobe Admin Console per gestire le adesioni ai prodotti e l&#39;autenticazione IMS per AEM come servizio Cloud.

See [IMS Support for AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/ims-support.html#managing-products-and-user-access-in-admin-console).

## Dynamic Tag Manager {#section_3A41CF2BD5994B9891537D063571D4ED}

Invita gli utenti in Dynamic Tag Management, assegna i ruoli utente e aggiungi gli utenti ai gruppi.

Consulta [Utenti e autorizzazioni](https://docs.adobe.com/content/help/it-IT/dtm/using/admin/users.html) per informazioni su come invitare utenti in Dynamic Tag Management, assegnargli ruoli e aggiungerli ai gruppi.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Crea utenti Audience Manager e assegnali a gruppi. Puoi anche visualizzare i limiti (caratteristiche, segmenti, destinazioni e [!DNL AlgoModel]).

Consulta [Amministrazione](https://docs.adobe.com/content/help/it-IT/dtm/using/admin/users.html) nella guida di Audience Manager.

## Gestire i prodotti Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Crea un profilo di prodotto e assegnalo a un gruppo di autorizzazioni.

Quando inviti un utente in un’organizzazione, puoi concedergli l’accesso a prodotti e profili di prodotto, Puoi anche delegare autorizzazioni amministrative limitate a un utente. Allo stesso modo, puoi creare gruppi di utenti, quindi aggiungere il gruppo a un profilo di prodotto per permettere l’accesso.

1. In [Admin Console](https://adminconsole.adobe.com/enterprise/), fai clic su **[!UICONTROL Prodotti]**.
1. Fai clic su **[!UICONTROL Nuovo profilo]**.
1. Configura i dettagli del profilo, quindi fai clic su **[!UICONTROL Avanti]**.
1. Fai clic su **[!UICONTROL Fine]**.

Ulteriore aiuto è disponibile in:

* [Gestire prodotti e profili](https://helpx.adobe.com/it/enterprise/using/manage-products-and-profiles.html)
* [Autorizzazioni di utenti Enterprise](https://docs.adobe.com/content/help/it-IT/target/using/administer/manage-users/enterprise/property-channel.html) nella guida di Adobe Target per maggiori informazioni.
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe Admin Console](https://helpx.adobe.com/it/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto {#task_040673FE3E3E429B9531FBCB8B6A4391}

Assegna le autorizzazioni di accesso ai rapporti di Analytics (suite di rapporti, metriche, dimensioni e così via) a un profilo di prodotto.

Ad esempio, puoi creare un profilo di prodotto che contiene più strumenti di Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] e [!UICONTROL Report Builder]) e autorizzarlo ad accedere a determinate metriche e dimensioni (comprese le eVar) e a creare segmenti o metriche calcolate.

1. Accedi ad [Admin Console](https://adminconsole.adobe.com/enterprise), quindi fai clic su **[!UICONTROL Prodotti]** (o sul nome del tuo prodotto).
1. Nel profilo del prodotto, fai clic su **[!UICONTROL Autorizzazioni]** (opzione disponibile solo per gli amministratori).
1. Configura le autorizzazioni del profilo:

| Elemento | Descrizione |
|--- |--- |
| Suite di rapporti | Attiva le autorizzazioni per suite di rapporti specifiche. |
| Metriche | Attiva le autorizzazioni per traffico, conversione, eventi personalizzati, eventi delle soluzioni, in base al contenuto e così via. |
| Dimensioni | Personalizza l’accesso degli utenti a un livello granulare, inclusi eVar, rapporti sul traffico, rapporti sulle soluzioni e rapporti sui percorsi. |
| Strumenti delle suite di rapporti | Attiva le autorizzazioni degli utenti per servizi web, gestione delle suite di rapporti, strumenti, rapporti ed elementi del dashboard. |
| Strumenti di Analytics | Attiva le autorizzazioni degli utenti per gli elementi generali (fatturazione, registri ecc.), gestione società, strumenti, accesso ai servizi Web, Report Builder e integrazione dei Data Connectors. Le impostazioni aziendali della categoria Personalizza di Admin Console sono state trasferite negli strumenti di Analytics. |

## Delega di ruoli amministrativi a utenti {#task_3A072C4AA9734BC59FFA7E015271BC7E}

In Admin Console, puoi delegare diritti amministrativi limitati ad altre persone nell&#39;organizzazione. I ruoli delegati consentono agli utenti di fornire l’accesso software agli utenti finali, fornire le funzionalità di distribuzione dell’accesso e fungere da delegati di supporto.

Sarà possibile, ad esempio:

* Consentire al tuo direttore creativo di concedere l’accesso a Creative Cloud.
* Consentire al tuo direttore marketing di concedere l’accesso a Experience Cloud.
* Mantenere questi due ruoli separati in modo che non possano sovrapporsi.

Utilizzando questi ruoli, puoi delegare simultaneamente la gestione ad altri senza fornire più funzionalità di quelle necessarie.

1. In Admin Console, fai clic su **[!UICONTROL Utenti]**, quindi fai clic sul nome dell’utente.
1. Fai clic su **[!UICONTROL Modifica diritti di amministratore]**.
1. Configura i diritti di amministrazione dell’utente.
1. Fai clic su **[!UICONTROL Avanti]** per controllare le impostazioni, quindi fai clic su **[!UICONTROL Salva]**.

## Browser supportati e requisiti di sistema {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Browser supportati in Experience Cloud.

* [!DNL Microsoft Edge] (Microsoft ha [terminato il supporto](https://www.microsoft.com/it-it/microsoft-365/windows/end-of-ie-support) per Internet Explorer 8, 9 e 10. Di conseguenza, Adobe non correggerà i problemi segnalati riguardanti queste versioni specifiche di Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** sebbene l’interfaccia di Experience Cloud supporti questi browser, le singole soluzioni potrebbero non supportare tutti i browser (per esempio, [Analytics](https://docs.adobe.com/content/help/it-IT/analytics/admin/sys-reqs.html) non supporta [!DNL Opera] e [Adobe Target](https://docs.adobe.com/help/it-IT/target/using/implement-target/before-implement/supported-browsers.html) non supporta [!DNL Safari]).

### Requisiti di soluzioni e prodotti

* [Analytics](https://docs.adobe.com/content/help/it-IT/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/it-IT/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/it-IT/target/using/implement-target/before-implement/supported-browsers.html)
