---
title: Gestione licenze utente e prodotto
description: Gestisci utenti e licenze di prodotto in Admin Console per applicazioni Experience Cloud.
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: e2e6c0daf8f765fe76f9c7bd44042d91dce142f2
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 5%

---

# Gestione degli utenti e licenze dei prodotti

Questa pagina fornisce informazioni specifiche per gli amministratori di Experience Cloud, con collegamenti alla documentazione comune per la gestione di utenti e prodotti.

Per informazioni generali sulla gestione delle identità applicabili a tutte le applicazioni Adobe, consulta la [guida per l&#39;amministratore di Enterprise e Team](https://helpx.adobe.com/it/enterprise/admin-guide.html).

Nelle sezioni seguenti sono disponibili collegamenti alle risorse della guida di Admin Console.

## Configurazione di Admin Console

Per gestire le licenze di prodotti e identità per le applicazioni Experience Cloud, passa a [Admin Console](https://adminconsole.adobe.com/enterprise/).

* [Imposta identità e Single Sign-On](https://helpx.adobe.com/it/enterprise/using/set-up-identity.html): scopri come impostare gli account degli utenti con diversi tipi di ID con o senza Single Sign-On (SSO). Configura SSO per il software Adobe, configura le impostazioni SAML e segui le domande e gli errori più comuni.

* [Imposta l&#39;organizzazione tramite il trust tra directory](https://helpx.adobe.com/enterprise/using/directory-trust.html). Utilizzare il trust tra directory per autenticare gli utenti in un dominio già richiesto da un&#39;altra organizzazione.

  Per informazioni sulle organizzazioni, vedere [Organizzazioni in Experience Cloud](organizations.md).

* [Impostazioni di autenticazione (enterprise)](https://helpx.adobe.com/enterprise/using/authentication-settings.html) - Admin Console supporta diversi livelli e criteri di protezione tramite password per garantire la sicurezza. È possibile specificare di utilizzare un livello di protezione tramite password da applicare a tutti gli utenti dell&#39;organizzazione. Tre livelli di sicurezza per l’Assistenza clienti di Adobe.

* [Contatti per la privacy e la sicurezza](https://helpx.adobe.com/enterprise/using/security-contacts.html) - Adobe pone l&#39;accento sulla protezione dei dati dell&#39;organizzazione e degli utenti. In caso di problemi di sicurezza relativi alle nostre soluzioni software, le notifiche vengono inviate ai responsabili della conformità appropriati.

  Le aziende hanno il proprio personale il cui ruolo è specifico per la protezione dei dati, l&#39;integrità e altre questioni relative alla conformità. Pertanto, le informazioni di contatto per tale personale sono essenziali per contribuire a garantire una notifica rapida in caso di incidente di sicurezza.

## Gestione utente

* [Gestione di più utenti](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) Caricamento CSV in blocco: scopri come gestire più utenti tramite il caricamento in blocco CSV su Adobe Admin Console.

* [Tipi di identità](https://helpx.adobe.com/it/enterprise/using/identity.html) - I tipi di identità consentono all&#39;organizzazione diversi livelli di controllo sugli account e sui dati degli utenti. La scelta del modello di identità influisce sul modo in cui l’organizzazione memorizza e condivide le risorse. Mentre i modelli Federated ID e Enterprise ID vengono creati e gestiti dall’organizzazione, gli Adobe ID vengono creati e gestiti dall’utente.

* [Strumento User Sync](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) - Lo strumento User Sync di Adobe è un&#39;applicazione desktop utilizzata per automatizzare il processo di sincronizzazione dei dati utente tra il sistema di gestione delle identità di un&#39;organizzazione (come Active Directory) e Adobe Adobe Admin Console. Lo strumento consente agli amministratori di semplificare il provisioning degli utenti, gli aggiornamenti e la disattivazione tra i prodotti Adobe.

  Lo strumento User Sync consente alle organizzazioni di semplificare la gestione degli account utente e delle licenze sincronizzando automaticamente i dati utente (ad esempio ruoli, gruppi e autorizzazioni di accesso) tra il servizio directory e i sistemi Adobe. Questo strumento è particolarmente utile per le aziende con team di grandi dimensioni. Contribuisce a mantenere la coerenza e la sicurezza, garantendo nel contempo che gli utenti abbiano accesso solo ai prodotti e ai servizi a cui hanno diritto.

* [Visualizza dettagli utente (Admin Tool)](admin-tool-experience-cloud.md) - Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti e i criteri di Experience Cloud con i dettagli in [!UICONTROL Admin Tool].

## Rapporti e registri

* [Registro di controllo](https://helpx.adobe.com/enterprise/using/audit-logs.html) Per tenere traccia di tutte le modifiche apportate in Admin Console.

Per informazioni non descritte nei percorsi precedenti, consultare la [Guida per l&#39;amministrazione di Enterprise e team](https://helpx.adobe.com/it/enterprise/admin-guide.html).

## Risorse specifiche per l’applicazione

Questi collegamenti consentono di trovare informazioni di amministrazione per specifiche applicazioni Experience Cloud.

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/it/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) e [Raccolta dati](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Target](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)