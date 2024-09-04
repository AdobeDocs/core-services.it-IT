---
title: Preferenze account e notifiche
description: Scopri i profili utente e le preferenze dell’account in Experience Cloud. Iscriviti alle notifiche sui prodotti per e-mail e  [!DNL Slack] e configura gli avvisi sui prodotti.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: b42a942deb91f3fb68ff1195b94df248763f5122
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 22%

---

# Preferenze e notifiche dell’account {#preferences}

L&#39;Experience Cloud [preferenze](https://experience.adobe.com/preferences) include notifiche (in-app, e-mail e [!DNL Slack]), abbonamenti e avvisi.

Nelle preferenze, puoi effettuare le seguenti operazioni:

* Cercare le [organizzazioni](../administration/organizations.md)
* Specifica un tema scuro (non tutte le applicazioni supportano questo tema).
* Configura le preferenze utente, le notifiche e le sottoscrizioni.
* Disconnettiti da Experience Cloud.

## Gestione preferenze

Per gestire le preferenze, seleziona **[!UICONTROL Preferenze]** nel menu dell’account ![preferenze](../assets/preferences-icon-sm.png).

Nelle [!UICONTROL preferenze di Experience Cloud], è possibile configurare le seguenti funzioni:

| Funzione | Descrizione |
|--- |--- |
| [Organizzazione](../administration/organizations.md) predefinita | Seleziona l’organizzazione da visualizzare all’avvio di Experience Cloud. |
| [!UICONTROL Raccolta dati sui prodotto] | Seleziona le tecnologie che Adobe può utilizzare per raccogliere i dati sul modo in cui utilizzi i suoi prodotti. |
| [Notifiche](#notifications-and-announcements) | Abilita [!UICONTROL notifiche in-app], [!UICONTROL e-mail] o [Slack](#slack-notifications). |
| [!UICONTROL Promozioni e consigli personalizzati per l’apprendimento] | Seleziona il punto in cui desideri ricevere [aiuto personalizzato](personalized-learning.md) per i tuoi prodotti di Adobe. Questa guida è disponibile tramite e-mail, nel prodotto e nelle community di Experienci League. |
| [!UICONTROL Abbonamenti] | Seleziona i prodotti e le categorie a cui desideri abbonarti. Notifiche nel popover [!UICONTROL Notifiche] e nell&#39;e-mail. |
| [!UICONTROL Priorità] | Seleziona le categorie a cui vuoi assegnare la priorità alta. Queste categorie sono contrassegnate con un tag [!UICONTROL Elevato] e possono essere configurate per la consegna come avvisi. |
| [!UICONTROL Avvisi] | Seleziona le notifiche per le quali desideri visualizzare gli avvisi nel browser. Gli avvisi vengono visualizzati per alcuni secondi nell’angolo in alto a destra della finestra. |
| E-mail | Specifica la frequenza con cui desideri ricevere le e-mail di notifica: Non inviata, Immediata, Giornaliera o Settimanale. |

## Abbonati alle notifiche in Experience Cloud {#notifications}

Puoi selezionare i prodotti e le categorie a cui desideri abbonarti. Le notifiche vengono visualizzate nel popover [!UICONTROL Notifiche] (in-app), nell&#39;e-mail o nello [Slack](#slack-notifications) (a seconda degli abbonamenti).

Le notifiche e-mail e di Slack sono utili nelle situazioni in cui non hai effettuato l’accesso a Experience Cloud.

### Abbonati per ricevere notifiche in-app ed e-mail

1. Passa all&#39;Experience Cloud [preferenze](https://experience.adobe.com/preferences).

1. In **[!UICONTROL Notifiche]**, abilita **[!UICONTROL In-app]** o **[!UICONTROL E-mail]**.

   Le modifiche alle notifiche vengono salvate automaticamente.

### Iscriviti a [!DNL Slack] notifiche {#slack}

>[!NOTE]
>
>Le notifiche di Slack verranno rilasciate: **11 settembre 2024**


Puoi configurare le preferenze del tuo account per inviare notifiche Experience Cloud a un canale [!DNL Slack].

**Prerequisiti**

* Devi avere un account di Experience Cloud.
* Devi avere un account [!DNL Slack]. L’amministratore di Slack abilita l’integrazione di Experience Cloud con Slack.
* È necessario far parte di almeno un&#39;area di lavoro [!DNL Slack].

**Per iscriversi alle notifiche di Slack**

1. Passa all&#39;Experience Cloud [preferenze](https://experience.adobe.com/preferences)

1. Individua [!DNL Slack], quindi fai clic su **[!UICONTROL Aggiungi allo Slack]**.

   ![Aggiungi allo Slack](../assets/add-to-slack.png)

   Se [!DNL Slack] è installato, l&#39;applicazione viene aperta e viene visualizzato un messaggio di richiesta di autorizzazione.

   * Fare clic su **[!UICONTROL Consenti]**.

   Se [!DNL Slack] non è installato, viene visualizzato un messaggio di _richiesta di installazione_:

   ![Integrazione Slack richieste](../assets/slack-request.png)

   * In Slack, scegli l’area di lavoro dall’angolo in alto a destra dell’applicazione.

   * Per richiedere l&#39;approvazione dell&#39;applicazione per il gestore dell&#39;area di lavoro di Slack, fare clic su **[!UICONTROL Invia]**.

   * Riceverai una notifica in [!DNL Slack] dopo l&#39;approvazione della richiesta di applicazione.

   * Dopo aver ricevuto [!DNL Slack] approvazione, torna all&#39;Experience Cloud **[!UICONTROL Notifiche]**, quindi fai clic su **[!UICONTROL Aggiungi allo Slack]**.

1. In **[!UICONTROL Notifiche]**, abilita [!DNL Slack] notifiche per i prodotti e le categorie desiderati.

   ![Notifiche di Slack](../assets/slack.png)

   Gli aggiornamenti alle notifiche vengono salvati automaticamente.

### Elementi visualizzati in [!DNL Slack]

Le notifiche di Slack visualizzano le seguenti informazioni:

* Il messaggio personale verrà ricevuto dal nome applicazione _Adobe Experience Cloud_.
* Il messaggio include il logo del prodotto per l’applicazione specifica, ad esempio Adobe Experience Platform, Adobe Experience Manager e così via.
* Un collegamento per visualizzare tutte le notifiche su Experience Cloud.
* Un collegamento per gestire le preferenze di notifica su Experience Cloud.

## Visualizza [!UICONTROL notifiche] e annunci in Experience Cloud {#view-notifications}

Nell&#39;intestazione dell&#39;Experience Cloud puoi visualizzare le notifiche alle quali hai [effettuato l&#39;abbonamento](#notifications), nonché gli annunci.

1. Fai clic sull’icona a forma di campana nell’intestazione. ![Notifiche e annunci](../assets/bell-icon.png)

1. Fai clic su **[!UICONTROL Notifiche]** o **[!UICONTROL Annunci]**.

   In questa posizione puoi ricevere informazioni importanti sui prodotti, sulla collaborazione con altri utenti e su altri aggiornamenti rilevanti. Gli aggiornamenti includono versioni di prodotto, avvisi di manutenzione, elementi condivisi e richieste di approvazione.