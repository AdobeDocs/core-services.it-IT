---
description: Scopri i componenti dell’interfaccia centrale di Experience Cloud. Per assistenza sull’amministrazione di utenti e prodotti, consulta Admin Console e abilita le applicazioni per i servizi di Experience Cloud. Ottieni assistenza per libreria Pubblico, Attributi del cliente, Risorse Experience Cloud e altro ancora.
title: Documentazione dell’ interfaccia di Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 0740361094aac0e63207e5e60aa666a1613d0e94
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 82%

---

# Panoramica sull’interfaccia centrale di Experience Cloud

[Experience Cloud](https://experience.adobe.com) è un insieme integrato di applicazioni, prodotti e servizi Adobe per il marketing digitale. L’interfaccia intuitiva consente di accedere rapidamente alle applicazioni cloud, alle funzionalità dei prodotto e ai servizi.

![Experience Cloud](assets/landing.png)

Dall’area dell’intestazione di Experience Cloud, è possibile:

* Accedi a tutte le applicazioni e i servizi Experience Cloud
* Dal menu Aiuto, cercare la documentazione del prodotto, i tutorial e i post della community. Visualizzare i risultati in Experience League.
* Eseguire ricerche globali sugli oggetti business utilizzando la ricerca globale (solo per gli utenti di Experience Platform) nel campo Ricerca.
* Gestire le [preferenze](features/account-preferences.md) dell’account (avvisi, notifiche e abbonamenti)


Estratto da GSPM:

## Esplora le funzionalità

<table style="table-layout:fixed">
<tr style="border: 0;">
   <td valign="top">
      <a href="../user-guide/effective-prompts.md">
      <img alt="Cursore a destra" src="../assets/icons/icon-chevronRight.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/effective-prompts.md">
         <strong>Scrivi Prompt Effettivi</strong>
         </a>
      </div>
      <p>
         <em>Creare prompt descrittivi che generano esperienze digitali nel marchio.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/create/overview.md">
      <img alt="Pennello" src="../assets/icons/icon-create.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/create/overview.md">
         <strong>Crea esperienze</strong>
         </a>
      </div>
      <p>
         <em>Creare e-mail e annunci Meta performanti, on-brand.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/approvals/overview.md">
      <img alt="Segno Di Spunta" src="../assets/icons/icon-checkmarkCircle.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/approvals/overview.md">
         <strong>Rivedi e approva</strong>
         </a>
      </div>
      <p>
         <em>Organizza la revisione e l'approvazione semplificate delle risorse di marketing.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/content/overview.md">
      <img alt="Griglia" src="../assets/icons/icon-images.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/content/overview.md">
         <strong>Gestione contenuto</strong>
         </a>
      </div>
      <p>
         <em>Trova, gestisci e ridefinisci i contenuti mantenendo le linee guida del brand.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/insights/overview.md">
      <img alt="Grafico" src="../assets/icons/icon-dataAnalytics.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/insights/overview.md">
         <strong>Visualizza approfondimenti</strong>
         </a>
      </div>
      <p>
         <em>Analizzare l'efficacia dei contenuti dei canali multimediali a pagamento.</em>
      </p>
   </td>
</tr>
</table>

## Scopri come

<table style="table-layout:fixed">
<td valign="top">
   <div>
      <a href="/help/user-guide/guidelines/add-guidelines.md">
      <img alt="Aggiungi linee guida" src="../assets/card-guidelines.png">
      <strong>Aggiungi linee guida</strong>
      </a>
   </div>
   <p>
      <em>Scopri come aggiungere linee guida - Marchi, prodotti e utenti tipo - a GenStudio for Performance Marketing.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-email-experience.md">
      <img alt="Idee, libri, matita, computer" src="../assets/card-create-assets.png">
      <strong>Creare un'esperienza e-mail</strong>
      </a>
   </div>
   <p>
      <em>Scopri come creare un'esperienza e-mail nel brand.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-meta-ad.md">
      <img alt="Persone che spostano file in una cartella" src="../assets/card-manage-content.png">
      <strong>Creare un'esperienza di annuncio multimediale</strong>
      </a>
   </div>
   <p>
      <em>Scopri come creare un'esperienza di annunci multimediali allineata al brand.</em>
   </p>
</td>
</table>


(Fine del GSPM)







## Accedere a Experience Cloud {#signin}

Accedi e verifica di essere nell&#39;[organizzazione](administration/organizations.md) corretta.

1. Passa ad [Adobe Experience Cloud](https://experience.adobe.com).
1. Digita il tuo indirizzo e-mail Adobe, quindi fai clic su **[!UICONTROL Continua]**.
1. Seleziona un account.
1. Digita la tua password.
1. Verifica di essere nell’organizzazione giusta.

   ![Verifica di essere nell’organizzazione corretta](assets/organizations-menu.png)

   **Verifica l’organizzazione**

   L’[organizzazione](administration/organizations.md) viene visualizzata nell’intestazione dell’interfaccia.

   Se la tua organizzazione usa Federated ID, Experience Cloud ti consente accedere in modalità single sign-on, senza inserire l’indirizzo e-mail e la password. Aggiungi `#/sso:@domain` all’URL di Experience Cloud (`https://experience.adobe.com`) per eseguire questa attività.

   Ad esempio, per un’organizzazione con Federated ID e il dominio `adobecustomer.com`, imposta il link dell’URL su `https://experience.adobe.com/#/sso:@adobecustomer.com`. Puoi anche passare direttamente a una specifica applicazione salvando come segnalibro o preferito l’URL seguito dal percorso dell’applicazione. Ad esempio, per Adobe Analytics: `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.

## Accedere alle applicazioni di Experience Cloud {#navigation}

Dopo aver effettuato l’accesso ad Experience Cloud, è possibile accedere rapidamente a tutte le applicazioni, i servizi e le organizzazioni dall’lintestazione unificata.

Per accedere alle applicazioni e ai servizi Experience Cloud per i quali disponi dei diritti di accesso nella tua organizzazione, passa al selettore delle applicazioni ![menu](assets/menu-icon.png).

![Accedere alle applicazioni Experience Cloud](assets/platform-core-services.png)

## Ottenere assistenza e supporto {#support}

Accedi ai contenuti di apprendimento e alla guida utilizzando il **[!UICONTROL Centro assistenza]** (![risorsa](assets/help-icon.png)) nell’intestazione, dove sono inclusi contenuti guida (documentazione, tutorial e corsi) su [Experience League](https://experienceleague.adobe.com/it?lang=it#home), nonché le risorse aggiuntive per le singole applicazioni. Puoi anche inviare feedback aperti e creare ticket di supporto con priorità.

![Ottenere assistenza e supporto](assets/search-menu.png)

Il menu [!UICONTROL Aiuto] consente inoltre di accedere a:

* **[!UICONTROL Supporto]:** crea un ticket di supporto o contatta il [!UICONTROL Supporto] tramite Twitter.
* **[!UICONTROL Feedback]:** invia feedback sulla tua esperienza nell’uso di Experience Cloud. Il tuo feedback viene utilizzato per migliorare i prodotti e i servizi di Adobe.
* **[!UICONTROL Stato]:** passa a `https://status.adobe.com/experience_cloud` per controllare lo stato operativo del prodotto e [!UICONTROL gestire gli abbonamenti].
* **[!UICONTROL Developer Connection]:** naviga in `adobe.io` e accedi alla documentazione per gli sviluppatori.

## Gestione del profilo utente

Nel menu [!UICONTROL Profilo] è possibile:

* Specificare un tema scuro (non tutte le applicazioni supportano questo tema)
* Gestire le [preferenze](features/account-preferences.md) di Experience Cloud
* Selezionare o cercare un’[Organizzazione](administration/organizations.md)
* Visualizzare [!UICONTROL Note legali]
* Uscire
* Configurare preferenze, notifiche e abbonamenti dell’account

## Visualizzare notifiche e annunci interni al prodotto {#notifications}

Fai clic sull’icona a forma di campana per visualizzare notifiche e annunci. Gli annunci possono riferirsi ad aggiornamenti rilevanti e fruibili, inclusi rilasci di prodotto, avvisi di manutenzione, elementi condivisi e richieste di approvazione.

![Notifiche e annunci](assets/notifications-menu-small.png)

Per gestire notifiche e avvisi, vedere [Preferenze account e notifiche](features/account-preferences.md)


## Novità

Scopri gli ultimi miglioramenti dei componenti dell’interfaccia centrale di Experience Cloud.

>[!BEGINTABS]
>[!TAB Integrazione di  Slack con Experience Cloud]

Puoi configurare le preferenze del tuo account per inviare notifiche Experience Cloud a un canale [!DNL Slack].

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/it/docs/core-services/interface/features/account-preferences#notifications" tooltip="Informazioni su Slack"}


>[!TAB Nuova interfaccia utente di Campaign Web]

Scopri la nuova interfaccia utente di Adobe Campaign. Più moderna, intuitiva e dinamica.

[![immagine](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB Prossime modifiche del canale di notifica push]

Alcune importanti modifiche al servizio Android Firebase Cloud Messaging (FCM) verranno rilasciate nel 2024 e potranno influenzare la tua implementazione di Adobe Campaign. Per supportare questa modifica, potrebbe essere necessario aggiornare la configurazione dei servizi di abbonamento per i messaggi push Android. Puoi già verificare e intervenire.

[![immagine](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## Inizia con le nozioni di base

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>Funzionalità principali</strong><br/>: scopri le funzionalità chiave di Adobe Campaign v8 per la gestione delle campagne cross-channel.</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>Connessione a Campaign v8</strong><br/>: scopri come connetterti ad Adobe Campaign v8 e avviare il percorso di gestione delle campagne installando e configurando la console client.</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>Inviare messaggi</strong><br/>: scopri come inviare messaggi attraverso vari canali come ad esempio e-mail, SMS e notifiche push.
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>Importare i profili</strong><br/>: esplora con facilità la creazione dei profili nel database di Adobe Campaign v8. Aggiungi profili manualmente o tramite importazioni, perfezionando i dati dei clienti e personalizzando le campagne in modo semplice.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## Esplora la documentazione

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>Introduzione</strong><br/><a href="start/campaign-ui.md">Interfaccia utente</a> - <a href="start/ac-components.md">Componenti e processi</a> - <a href="start/v7-to-v8.md">Da Classic v7 a v8</a> - <a href="start/campaign-faq.md">Domande frequenti</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>Esperienza cliente</strong><br/> <a href="../automation/workflow/about-workflows.md" target="_blank">Automatizza con i flussi di lavoro</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">Orchestrazione della campagna</a> - <a href="interaction/interaction.md">Gestione delle decisioni</a> - <a href="send/personalize.md">Personalizzazione</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>Inviare messaggi</strong><br/><a href="start/create-message.md">Introduzione</a> - <a href="send/preview-and-proof.md">Anteprima e bozze</a> - <a href="send/predictive.md">Ottimizzazione del tempo di invio</a> - <a href="reporting/gs-reporting.md">Reporting e analisi</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>Profili e tipi di pubblico</strong><br/> <a href="audiences/create-profiles.md">Aggiungere profili</a> - <a href="audiences/create-audiences.md">Creare tipi di pubblico</a> - <a href="start/subscriptions.md">Gestiire gli abbonamenti</a> - <a href="start/privacy.md">Privacy</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>Architettura e configurazione</strong><br/><a href="architecture/architecture.md">Architettura</a> - <a href="start/implement.md">Implementazione di Campaign v8</a> - <a href="connect/integration.md">Connessione con altre soluzioni</a> - <a href="start/gs-permissions.md">Utenti e autorizzazioni</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>Risorse per sviluppatori</strong><br/><a href="dev/datamodel.md">Modello dati Campaign v8</a> - <a href="dev/schemas.md">Schemi</a> - <a href="dev/api.md">API</a>
    </td>
  </tr>
</table>

## Risorse aggiuntive

[Descrizione del prodotto Adobe Campaign v8](https://helpx.adobe.com/it/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Documentazione dell’interfaccia utente web di Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=it){target="_blank"} - [Tutorial](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=it){target="_blank"} - [[!DNL Adobe Campaign] Guida all’automazione](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=it){target="_blank"} - [Pannello di controllo per Campaign v8](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=it){target="_blank"}

