---
description: Scopri i componenti dell’interfaccia centrale di Experience Cloud. Questa guida tratta argomenti quali l’amministrazione di utenti e prodotti da Admin Console, l’abilitazione delle applicazioni per i servizi Experience Cloud e ti permette di accedere alla documentazione per Libreria tipi di pubblico, Attributi del cliente, Experience Cloud Assets e altro ancora.
title: Guida e documentazione dell’interfaccia di Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: a4e0461791cd676365857c2dd4ef28c0e40c3430
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 99%

---

# Panoramica dell’interfaccia centrale di Experience Cloud

[Experience Cloud](https://experience.adobe.com) è un insieme integrato di applicazioni, prodotti e servizi Adobe per il marketing digitale. L’interfaccia intuitiva consente di accedere rapidamente alle applicazioni cloud, alle funzionalità dei prodotto e ai servizi.

![Experience Cloud](assets/landing.png)

Dall’area dell’intestazione di Experience Cloud, è possibile:

* Accedere alle applicazioni e ai servizi
* Dal menu Aiuto, cercare la documentazione del prodotto, i tutorial e i post della community. Visualizzare i risultati in Experience League.
* Eseguire ricerche globali sugli oggetti business utilizzando la ricerca globale (solo per gli utenti di Experience Platform) nel campo Ricerca.
* Gestire le preferenze dell’account (avvisi, notifiche e abbonamenti)

## Accedere a Experience Cloud {#signin}

Accedi e verifica di essere nell&#39;[organizzazione](administration/organizations.md) corretta.

1. Passa ad [Adobe Experience Cloud](https://experience.adobe.com).
1. Digita il tuo indirizzo e-mail Adobe, quindi seleziona **[!UICONTROL Continua]**.
1. Seleziona un account.
1. Digita la tua password.
1. Verifica di essere nell’organizzazione giusta.

   ![Verifica di essere nell’organizzazione corretta](assets/organizations-menu.png)

   **Verifica l’organizzazione**

   Per verificare di aver eseguito l’accesso all’[organizzazione](administration/organizations.md) giusta, fai clic sull’avatar del tuo profilo per visualizzarne il nome. Se ha accesso a più organizzazioni, puoi anche vedere le altre e passare a un’altra organizzazione direttamente dalla barra dell’intestazione.

   Se la tua organizzazione usa Federated ID, Experience Cloud ti consente accedere in modalità single sign-on, senza inserire l’indirizzo e-mail e la password. Aggiungi `#/sso:@domain` all’URL di Experience Cloud (`https://experience.adobe.com`) per eseguire questa attività.

   Ad esempio, per un’organizzazione con Federated ID e il dominio `adobecustomer.com`, imposta il link dell’URL su `https://experience.adobe.com/#/sso:@adobecustomer.com`. Puoi anche passare direttamente a una specifica applicazione salvando come segnalibro o preferito l’URL seguito dal percorso dell’applicazione. Ad esempio, per Adobe Analytics: `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.

## Accedere alle applicazioni di Experience Cloud {#navigation}

Dopo aver effettuato l’accesso ad Experience Cloud, è possibile accedere rapidamente a tutte le applicazioni, i servizi e le organizzazioni dall’lintestazione unificata.

Per accedere alle applicazioni e ai servizi Experience Cloud per i quali disponi dei diritti di accesso nella tua organizzazione, passa al selettore delle applicazioni ![menu](assets/menu-icon.png).

![Accedere alle applicazioni Experience Cloud](assets/platform-core-services.png)

## Ottenere assistenza e supporto {#support}

Dall’icona Aiuto (![risorsa](assets/help-icon.png)) nell’intestazione puoi accedere ai contenuti di apprendimento e alla guida, compresi i contenuti dell’Aiuto (documentazione, tutorial e corsi) disponibili in [Experience League](https://experienceleague.adobe.com/?lang=it#home), nonché risorse aggiuntive per le singole applicazioni. Puoi anche inviare feedback aperti e creare ticket di supporto con priorità.

![Ottenere assistenza e supporto](assets/search-menu.png)

Il menu [!UICONTROL Aiuto] consente inoltre di accedere a:

* **[!UICONTROL Supporto]:** crea un ticket di supporto o contatta il [!UICONTROL Supporto] tramite Twitter.
* **[!UICONTROL Feedback]:** invia feedback sulla tua esperienza nell’uso di Experience Cloud. Il tuo feedback viene utilizzato per migliorare i prodotti e i servizi di Adobe.
* **[!UICONTROL Stato]:** passa a `https://status.adobe.com/experience_cloud` per controllare lo stato operativo del prodotto e [!UICONTROL gestire gli abbonamenti].
* **[!UICONTROL Developer Connection]:** naviga in `adobe.io` e accedi alla documentazione per gli sviluppatori.

## Profilo utente e preferenze account {#preferences}

Le preferenze di Experience Cloud includono notifiche, abbonamenti e avvisi. Nel menu delle preferenze dell’account puoi effettuare le seguenti operazioni:

* Specificare un tema scuro (non tutte le applicazioni supportano questo tema)
* Cercare le [organizzazioni](administration/organizations.md)
* Uscire
* Configurare preferenze, notifiche e abbonamenti dell’account

Per gestire le preferenze, seleziona **[!UICONTROL Preferenze]** nel menu dell’account ![preferenze](assets/preferences-icon-sm.png).

![Profilo utente e preferenze account](assets/preferences-page.png)

Nelle [!UICONTROL preferenze di Experience Cloud], è possibile configurare le seguenti funzioni:

| Funzione | Descrizione |
|--- |--- |
| [Organizzazione](administration/organizations.md) predefinita | Seleziona l’organizzazione da visualizzare all’avvio di Experience Cloud. |
| [!UICONTROL Raccolta dati sui prodotto] | Seleziona le tecnologie che Adobe può utilizzare per raccogliere i dati sul modo in cui utilizzi i suoi prodotti. |
| [!UICONTROL Promozioni e consigli personalizzati per l’apprendimento] | Scegli dove desideri ricevere informazioni personalizzate sui tuoi prodotti Adobe. Puoi riceverle tramite e-mail, nel prodotto stesso e nelle community Experience League. [Ulteriori informazioni.](features/personalized-learning.md) |
| [!UICONTROL Abbonamenti] | Seleziona i prodotti e le categorie a cui desideri abbonarti. Notifiche nel riquadro a comparsa [!UICONTROL Notifiche] e via e-mail. |
| [!UICONTROL Priorità] | Seleziona le categorie a cui vuoi assegnare la priorità alta. Queste categorie sono contrassegnate con il tag Alta e possono essere configurate per la distribuzione come avvisi. |
| [!UICONTROL Avvisi] | Seleziona le notifiche per le quali desideri visualizzare gli avvisi nel browser. Gli avvisi vengono visualizzati per alcuni secondi nell’angolo in alto a destra della finestra. |
| E-mail | Specifica la frequenza con cui desideri ricevere le e-mail di notifica: Non inviata, Immediata, Giornaliera o Settimanale. |

{style="table-layout:auto"}

## Notifiche e annunci {#notifications}

Seleziona **[!UICONTROL Notifiche]** per ricevere avvisi sugli aggiornamenti rilevanti e fruibili, inclusi rilasci di prodotto, avvisi di manutenzione, elementi condivisi e richieste di approvazione.

![Notifiche e annunci](assets/notifications-menu-small.png)
