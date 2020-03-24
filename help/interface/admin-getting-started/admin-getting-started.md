---
description: Scopri come accedere ad Admin Console, gestire le autorizzazioni utente e i profili di prodotto di Experience Cloud e il supporto del browser.
keywords: core services
seo-description: Scopri come accedere ad Admin Console, gestire le autorizzazioni utente e i profili di prodotto di Experience Cloud e il supporto del browser.
seo-title: Gestione di utenti e prodotti Experience Cloud
solution: Experience Cloud
title: Gestione di utenti e prodotti Experience Cloud
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: b6bd75d92ce96e852a6e548362988a9b4d529fb9

---


# Gestione di utenti e prodotti Experience Cloud {#topic_3FCB4099640647E3B2411ADBFCE81909}

Scopri come accedere ad Admin Console, gestire le autorizzazioni utente e i profili di prodotto di Experience Cloud e il supporto del browser.

>[!IMPORTANT]
>
>La gestione degli utenti in Admin Console prevede l’utilizzo di nuovi termini, interfacce e modalità di navigazione. Le informazioni riportate di seguito descrivono questi nuovi aspetti e contengono collegamenti a ulteriori risorse di aiuto. This help supplements the information in the [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) for all Adobe cloud products.

## Novità nella gestione degli utenti in Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Scopri le nuove funzioni nella gestione degli utenti di Experience Cloud.

<!--

### Business ID type

Adobe is now introducing a new identity type: **Business ID**. This identity type, improves the control of user and product management, and content, while increasing the flexibility of Experience Cloud and Creative Cloud storage usage among your team. With the introduction of this new identity type, Adobe is migrating all Adobe IDs (owned by the individual) used for business to the new Business IDs (owned by the organization).

If you're an existing Creative Cloud for enterprise or teams customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you're a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID. 

Beginning May 89, 2020, enterprise admins cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.)
-->

### Strumenti di amministrazione

Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti Experience Cloud e dei loro dettagli in Admin Tool. Consulta [Visualizzare gli utenti Experience Cloud in Admin Tool](admin-tool-experience-cloud.md).

## Accesso ad Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Gli amministratori non gestiscono più gli utenti nelle soluzioni. La gestione di utenti e prodotti per Experience Cloud ora si verifica nell&#39;Admin Console.

**Per accedere ad Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Digita il tuo [Adobe ID o Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) e la relativa password.

Alternatively, from the Experience Cloud menu ( ![](assets/menu-icon.png)), click **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**Argomenti correlati**

[Guida](https://helpx.adobe.com/enterprise/using/users.html) utente di amministrazione per Creative Cloud e Document Cloud. Alcune informazioni sono relative alla gestione degli utenti di Experience Cloud, ad esempio la [gestione dei tipi](https://helpx.adobe.com/enterprise/help/identity.html)di identità.

[Accedi e gestisci le impostazioni](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) del tuo profilo per gestire password, organizzazioni e notifiche.

## Profili di prodotto e gruppi {#section_AB50558124D541CF80A0D3D76D35A4BF}

L&#39;aggiunta dei profili di prodotto rappresenta un cambiamento rispetto al modo in cui i prodotti e i servizi delle soluzioni sono stati gestiti in precedenza (utilizzando i gruppi). In Admin Console, le autorizzazioni si basano sui profili di prodotto, ovvero gruppi di prodotti e servizi che puoi assegnare agli utenti.

In Analytics, ad esempio, puoi configurare una serie di strumenti di reporting, quali Analysis Workspace e Report Builder, insieme a suite di rapporti, metriche, dimensioni e così via. Puoi autorizzare gli utenti a un profilo di prodotto aggiungendoli al profilo. See [Assign Analytics access permissions to a product profile](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Argomenti correlati**

[Delegare diritti amministrativi limitati](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Le autorizzazioni relative a utenti e prodotti Analytics vengono gestite in Admin Console.

[Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (in questa pagina).

**Migrazione degli account utente**

È disponibile uno strumento di migrazione degli ID utente di Analytics che permette agli amministratori di trasferire gli account utente da Gestione utenti di Analytics ad [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migrazione diventerà disponibile per i clienti in più fasi. Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). Gli utenti che tenteranno di accedere con i metodi precedenti ([!DNL my.omniture.com] e [!DNL sc.omniture.com]) verranno reindirizzati a [!DNL experiencecloud.adobe.com].

**Argomenti correlati**

[Migrazione degli ID utente di Analytics](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target: profili di prodotto e aree di lavoro {#section_3860AF177C9E4C7E9C390D36A414F353}

In Target, un&#39;area di lavoro è un profilo di prodotto. Consente a un&#39;organizzazione di assegnare una serie di utenti specifica a una serie di proprietà specifica. In vari modi, un&#39;area di lavoro è simile a una suite di rapporti in Adobe Analytics.

Vedi:
* [Autorizzazioni per gli utenti Enterprise](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [Gestione di prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Video: [Come configurare aree di lavoro Target in Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign: profili di prodotto, tenant e gruppi di sicurezza {#section_09CDF75366444CF5810CF321B7C712F3}

Un *tenant* in Campaign viene visualizzato come *prodotto* nella pagina Prodotti di Admin Console.

*Il gruppo* di sicurezza viene visualizzato come profilo di prodotto.

Consultate [Gestione di gruppi e utenti](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) per informazioni sui gruppi di sicurezza e assegnazione di utenti ai gruppi di sicurezza.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch viene visualizzato nella pagina Prodotti di Admin Console. Puoi includere altre soluzioni e altri servizi in un profilo di prodotto Launch.

Consulta Gestione [](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) utente per informazioni sulle autorizzazioni degli utenti in Admin Console e configura opzioni specifiche per Launch, tra cui l’assegnazione di diritti ai profili.

## Dynamic Tag Manager {#section_3A41CF2BD5994B9891537D063571D4ED}

Invita gli utenti in Dynamic Tag Management, assegna i ruoli utente e aggiungi gli utenti ai gruppi.

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Creazione di utenti Audience Manager e loro assegnazione a gruppi. Puoi anche visualizzare i limiti (caratteristiche, segmenti, destinazioni e modelli algoritmici).

Consulta [Amministrazione](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) nell&#39;aiuto di Audience Manager.

## Gestire i prodotti Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Crea un profilo di prodotto e assegnalo a un gruppo di autorizzazioni.

Quando inviti un utente in un’organizzazione, puoi concedergli l’accesso a prodotti e profili di prodotto, Potete anche delegare autorizzazioni amministrative limitate a un utente. Allo stesso modo, potete creare gruppi di utenti, quindi aggiungere il gruppo a un profilo di prodotto per abilitare l&#39;accesso.

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. Fai clic su **[!UICONTROL Nuovo profilo]**.
1. Configura i dettagli del profilo, quindi fai clic su **[!UICONTROL Avanti]**.
1. Fai clic su **[!UICONTROL Fine]**.

Ulteriore assistenza è disponibile all&#39;indirizzo:

* [Gestione di prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Autorizzazioni](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) utente Enterprise nell&#39;Aiuto di Target per ulteriori informazioni.
* Video: [Come configurare aree di lavoro Target in Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto {#task_040673FE3E3E429B9531FBCB8B6A4391}

Assegna le autorizzazioni di accesso ai rapporti di Analytics (suite di rapporti, metriche, dimensioni e così via) a un profilo di prodotto.

Ad esempio, puoi creare un profilo di prodotto che contiene più strumenti di Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] e [!UICONTROL Report Builder]) e autorizzarlo ad accedere a determinate metriche e dimensioni (comprese le eVar) e a creare segmenti o metriche calcolate.

1. Sign in to the [Admin Console](https://adminconsole.adobe.com/enterprise), then click **[!UICONTROL Products]** (or click your product name).
1. Nel profilo del prodotto, fai clic su **[!UICONTROL Autorizzazioni]** (opzione disponibile solo per gli amministratori).
1. Configura le autorizzazioni del profilo:

| Elemento | Descrizione |
|--- |--- |
| Suite di rapporti | Abilita le autorizzazioni per suite di rapporti specifiche. |
| Metrics (Metriche) | Attiva le autorizzazioni per il traffico, la conversione, gli eventi personalizzati, gli eventi delle soluzioni, in base al contenuto e così via. |
| Dimensioni | Personalizza l&#39;accesso degli utenti a un livello granulare, comprese eVar, rapporti sul traffico, rapporti sulle soluzioni e rapporti sui percorsi. |
| Strumenti delle suite di rapporti | Attiva le autorizzazioni utente per i servizi Web, la gestione delle suite di rapporti, gli strumenti e i rapporti e gli elementi del dashboard. |
| Strumenti di analisi | Attiva le autorizzazioni degli utenti per gli elementi generali (fatturazione, registri ecc.), gestione società, strumenti, accesso ai servizi Web, Report Builder e integrazione dei Data Connectors. Le impostazioni aziendali della categoria Personalizza di Admin Console sono state trasferite negli strumenti di Analytics. |

## Delega di ruoli amministrativi a utenti {#task_3A072C4AA9734BC59FFA7E015271BC7E}

In Admin Console, puoi delegare diritti amministrativi limitati ad altre persone nell&#39;organizzazione. I ruoli delegati consentono agli utenti di amministrare l&#39;accesso software agli utenti finali, fornire le funzionalità di distribuzione dell&#39;accesso e fungere da delegati di supporto.

Sarà possibile, ad esempio:

* Consentite al vostro direttore creativo di concedere l&#39;accesso a Creative Cloud.
* Consenti al direttore marketing di concedere l&#39;accesso a Experience Cloud.
* Mantenete questi due ruoli separati in modo che non possano sovrapporsi ai rispettivi ruoli.

Utilizzando questi ruoli, potete delegare simultaneamente la gestione ad altri senza fornire più funzionalità di quelle necessarie.

1. In Admin Console, fai clic su **[!UICONTROL Utenti]**, quindi fai clic sul nome dell’utente.
1. Fai clic su **[!UICONTROL Modifica diritti di amministratore]**.
1. Configura i diritti di amministrazione dell&#39;utente.
1. Fai clic su **[!UICONTROL Avanti]** per controllare le impostazioni, quindi fai clic su **[!UICONTROL Salva]**.

## Browser supportati e requisiti di sistema {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Browser supportati in Experience Cloud.

I browser supportati da Experience Cloud includono:

* [!DNL Microsoft Edge] Microsoft ha [cessato il supporto](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) per Internet Explorer 8, 9 e 10. Di conseguenza, Adobe non risolverà i problemi segnalati a fronte di tali versioni specifiche di Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** sebbene l’interfaccia di Experience Cloud supporti questi browser, le singole soluzioni potrebbero non supportare tutti i browser. Ad esempio, [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) non supporta [!DNL Opera] e [Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) non supporta [!DNL Safari].

**Requisiti di soluzione e di prodotto**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder ](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
