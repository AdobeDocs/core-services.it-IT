---
title: Gestione di utenti e prodotti
description: Scopri come accedere all’Admin Console e gestire le autorizzazioni utente e i profili prodotto di Experience Cloud. Scopri come delegare i diritti amministrativi agli utenti di Experience Cloud e il supporto del browser, ad Experience Cloud.
solution: Admin
index: true
feature: Admin Console
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: 2f315b2daa4e9d73b0adb1cf75fd7ff2417fd0c2
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 47%

---

# Gestione di utenti e prodotti Experience Cloud

Scopri come accedere ad Admin Console e gestire le autorizzazioni degli utenti e i profili di prodotto di Experience Cloud e il supporto del browser.

>[!IMPORTANT]
>
>Le seguenti informazioni sono specifiche per le applicazioni di Experience Cloud. Queste informazioni integrano le informazioni amministrative più ampie contenute nella [Guida utente per l&#39;amministrazione dell&#39;organizzazione](https://helpx.adobe.com/it/enterprise/admin-guide.html) per tutti i prodotti cloud di Adobe.

Puoi visualizzare un elenco ordinabile e filtrabile di tutti gli utenti di Experience Cloud e dei relativi dettagli in Admin Tool. Consulta [Visualizzare gli utenti Experience Cloud in Admin Tool](admin-tool-experience-cloud.md).

## Che cos’è un profilo di prodotto? {#section_AB50558124D541CF80A0D3D76D35A4BF}

[!UICONTROL I ] profili di prodotto sono gruppi di prodotti e servizi che puoi assegnare agli utenti. Ad Experience Cloud, le autorizzazioni si basano sul profilo di un prodotto, non sull’utente. Tuttavia, puoi delegare i diritti amministrativi a utenti specifici.

Ad esempio, in Analytics puoi configurare una raccolta di strumenti di reporting, come Analysis Workspace e Report Builder, insieme a suite di rapporti, metriche e dimensioni. Puoi concedere l’autorizzazione a un profilo di prodotto aggiungendo utenti al profilo.

* Consulta [Assegnare le autorizzazioni di accesso Analytics a un profilo di prodotto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391), in questa pagina.
* Consulta [Delega di ruoli amministrativi a utenti](#delegate-rights) in questa pagina

## Gestire i profili di prodotto di Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Puoi creare un profilo di prodotto e assegnarlo a un gruppo di autorizzazioni.

Quando inviti un utente in un&#39;organizzazione, puoi concedergli l&#39;accesso a prodotti e profili di prodotto, Puoi anche delegare autorizzazioni amministrative limitate a un utente. Allo stesso modo, puoi creare gruppi di utenti, quindi aggiungere il gruppo a un profilo di prodotto per permettere l&#39;accesso.

1. In [Admin Console](https://adminconsole.adobe.com/enterprise/), fai clic su **[!UICONTROL Prodotti]**.
1. Fai clic sul nome della tua organizzazione.
1. Fai clic su **[!UICONTROL Nuovo profilo]**.
1. Configura i dettagli del profilo, quindi fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni (e per assistenza sulla gestione dei prodotti di Creative Cloud e Document Cloud), consulta [Identità](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html) nella [Guida utente per l&#39;amministrazione](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/users.ug.html).

**Argomenti correlati**

* [Gestisci prodotti e ](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html) profili nella Guida utente di amministrazione.
* [Autorizzazioni di utenti Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en) nella guida di Adobe Target per maggiori informazioni
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe Admin Console](https://helpx.adobe.com/it/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

<!-- ## What's new in Experience Cloud user management {#concept_06A0A13362F644FB90F947238407637A}

Learn about the latest features in Experience Cloud user and product management.

### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

## Delega di ruoli amministrativi a utenti {#delegate-rights}

In Admin Console, puoi delegare diritti amministrativi limitati ad altre persone nell&#39;organizzazione. I ruoli delegati consentono agli utenti di fornire l&#39;accesso software agli utenti finali, fornire le funzionalità di distribuzione dell&#39;accesso e fungere da delegati di supporto.

Sarà possibile, ad esempio:

* Consentire al tuo direttore creativo di concedere l&#39;accesso a Creative Cloud.
* Consentire al tuo direttore marketing di concedere l&#39;accesso a Experience Cloud.
* Mantenere questi due ruoli separati in modo che non possano sovrapporsi.

Utilizzando questi ruoli, puoi delegare simultaneamente la gestione ad altri senza fornire più funzionalità di quelle necessarie.

1. In Admin Console, fai clic su **[!UICONTROL Utenti]**, quindi fai clic sul nome dell&#39;utente.

   ![](assets/edit-admin-rights.png)

1. Fai clic su **[!UICONTROL Modifica diritti di amministratore]**.

   ![](assets/edit-admin-rights-page.png)

1. Specifica i diritti di amministrazione dell’utente.
1. Fai clic su **[!UICONTROL Salva]**.

## Gestione di utenti e prodotti Analytics {#section_97DE101F92CD494AB073893680992F1A}

Puoi assegnare le autorizzazioni di accesso ai rapporti di Analytics (suite di rapporti, metriche, dimensioni e così via) a un profilo di prodotto.

Ad esempio, puoi creare un profilo di prodotto contenente più strumenti di Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] e [!UICONTROL Report Builder]). Questi profili contengono l’autorizzazione a metriche e dimensioni specifiche (comprese le eVar) e funzionalità come segmenti o creazione di metriche calcolate.

1. Accedi a [Admin Console](https://adminconsole.adobe.com/enterprise), quindi fai clic su **[!UICONTROL Prodotti]**.
1. Nella pagina [!UICONTROL Prodotti], fai clic sul prodotto, quindi fai clic su **[!UICONTROL Autorizzazioni]** (disponibile solo per gli amministratori).
1. Configura le autorizzazioni del profilo:

| Elemento | Descrizione |
|--- |--- |
| Suite di rapporti | Attiva le autorizzazioni per suite di rapporti specifiche. |
| Metriche | Attiva le autorizzazioni per traffico, conversione, eventi personalizzati, eventi delle soluzioni, in base al contenuto e così via. |
| Dimensioni | Personalizza l&#39;accesso degli utenti a un livello granulare, inclusi eVar, rapporti sul traffico, rapporti sulle soluzioni e rapporti sui percorsi. |
| Strumenti delle suite di rapporti | Attiva le autorizzazioni degli utenti per servizi web, gestione delle suite di rapporti, strumenti, rapporti ed elementi del dashboard. |
| Strumenti di Analytics | Attiva le autorizzazioni degli utenti per l&#39;integrazione a Elementi generali (fatturazione, registri e così via), Gestione società, Strumenti, Accesso al servizio Web, Report Builder e Connettori dati. Le impostazioni aziendali della categoria Personalizza di Admin Console sono state trasferite negli strumenti di Analytics. |

**Migrazione degli account utente**

È disponibile uno strumento di migrazione degli ID utente di Analytics che permette agli amministratori di trasferire gli account utente da Gestione utenti di Analytics ad [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migrazione diventerà disponibile per i clienti in più fasi. Adobe ti invierà una notifica e ti fornirà assistenza quando arriverà il tuo momento di trasferire gli account utente esistenti da **[!UICONTROL Strumenti di amministrazione]** > **[!UICONTROL Gestione utenti]** all&#39;Admin Console.

Dopo la migrazione, gli utenti effettueranno l’accesso utilizzando il proprio Adobe ID (o Enterprise ID) e si autenticheranno nelle soluzioni e nei servizi di Experience Cloud all’indirizzo [experience.adobe.com](https://experience.adobe.com). Se gli utenti tentano di accedere tramite gli accessi legacy ([!DNL my.omniture.com], [!DNL sc.omniture.com] e [!DNL experiencecloud.adobe.com]) vengono reindirizzati a [!DNL experience.adobe.com].

**Argomenti correlati**

Per ulteriori informazioni, consulta [Migrazione degli ID utente di Analytics](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=en)

## Gestione di Adobe Target: profili di prodotto e aree di lavoro {#section_3860AF177C9E4C7E9C390D36A414F353}

In Adobe Target, un&#39;area di lavoro è un profilo di prodotto. Consente a un&#39;organizzazione di assegnare una serie di utenti specifica a una serie di proprietà specifica. In vari modi, un&#39;area di lavoro è simile a una suite di rapporti in Adobe Analytics.

Vedi:

* [Autorizzazioni per gli utenti Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [Gestire prodotti e profili](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* Video: [Come configurare le aree di lavoro di Adobe Target in Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Gestire profili di prodotto, tenant e gruppi di sicurezza Campaign {#section_09CDF75366444CF5810CF321B7C712F3}

Un *tenant* in Campaign viene visualizzato come *prodotto* nella pagina Prodotti di Admin Console.

Un *gruppo di sicurezza* viene visualizzato come un profilo di prodotto.

Consulta [Gestione di gruppi e utenti](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=en) per informazioni sui gruppi di sicurezza e sull&#39;assegnazione di utenti ai gruppi di sicurezza.

## Gestire la raccolta dati di Experience Platform (Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

L&#39;Experience Platform [!UICONTROL Raccolta dati] ([!UICONTROL Launch]) viene visualizzato nella pagina [!UICONTROL Prodotti] nell&#39;Admin Console . Puoi includere altre soluzioni e altri servizi in un profilo di prodotto Launch.

Invita gli utenti in [!UICONTROL Platform Launch] e assegna ruoli utente e autorizzazioni.

Consulta [Autorizzazioni utente](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=it#admin) per informazioni sulle autorizzazioni utente nell&#39;Admin Console e sulla configurazione di opzioni specifiche per Launch, tra cui l&#39;assegnazione di diritti ai profili.

## Experience Manager as a Cloud Service

I clienti Adobe Enterprise sono rappresentati come organizzazioni nell&#39;Adobe [!UICONTROL Admin Console]. I clienti di Experience Manager possono utilizzare l&#39;Adobe [!UICONTROL Admin Console] per gestire le adesioni ai prodotti e l&#39;autenticazione IMS per Experience Manager come [!UICONTROL Cloud Service].

Consulta [Supporto IMS per Experience Manager come Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=en).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Crea utenti Audience Manager e assegnali a gruppi. Puoi anche visualizzare i limiti (caratteristiche, segmenti, destinazioni e [!DNL AlgoModel]).

Consulta [Amministrazione](https://experienceleague.adobe.com/docs/dtm/using/admin/users.html?lang=en) nella guida di Audience Manager.

## Browser supportati in Experience Cloud

* [!DNL Microsoft® Edge] (Microsoft® ha  [terminato ](https://www.microsoft.com/it-it/WindowsForBusiness/End-of-IE-support) il supporto per Internet Explorer 8, 9 e 10. Di conseguenza, Adobe non risolve i problemi segnalati relativi a queste versioni specifiche di Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** anche se l&#39;interfaccia di Experience Cloud supporta questi browser, le singole applicazioni non supportano tutti i browser. (per esempio, [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en) non supporta [!DNL Opera] e [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en) non supporta [!DNL Safari]).

### Requisiti di soluzioni e prodotti

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
