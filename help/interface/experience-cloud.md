---
description: Scopri i componenti dell’interfaccia centrale di Experience Cloud. Questa guida tratta argomenti quali l’amministrazione di utenti e prodotti da Admin Console, l’abilitazione delle applicazioni per i servizi Experience Cloud e ti permette di accedere alla documentazione per Libreria tipi di pubblico, Attributi del cliente, Experience Cloud Assets e altro ancora.
solution: Experience Cloud
title: Guida e documentazione dell’interfaccia di Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 0de9f9d62dcb3e6c32e841de1663704475805315
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 100%

---

# Guida dei componenti dell’interfaccia centrale di Experience Cloud

[Experience Cloud](https://experience.adobe.com) è un insieme integrato di applicazioni, prodotti e servizi Adobe per il marketing digitale. L’interfaccia intuitiva consente di accedere rapidamente alle applicazioni cloud, alle funzionalità dei prodotto e ai servizi.

![Experience Cloud](assets/landing.png)

Dall’area dell’intestazione di Experience Cloud, è possibile:

* Accedere alle applicazioni e ai servizi
* Cercare documentazione di prodotto, tutorial e post della community
* Eseguire ricerche globali sugli oggetti business (solo per gli utenti di Experience Platform)
* Gestire le preferenze dell’account (avvisi, notifiche e abbonamenti)

## Accedere a Experience Cloud {#signin}

Accedi e verifica di essere nell&#39;[organizzazione](organizations.md) corretta.

1. Passa ad [Adobe Experience Cloud](https://experience.adobe.com).
1. Digita il tuo indirizzo e-mail Adobe, quindi seleziona **[!UICONTROL Continua]**.

   Se sei un Amministratore, consulta [Autenticazione utente di Experience Cloud](admin-getting-started.md#migration) per importanti aggiornamenti ai tipi di identità (Business ID).

1. Seleziona un account.
1. Digita la tua password.
1. Verifica di essere nell’organizzazione giusta.

   ![Verifica di essere nell’organizzazione corretta](assets/organizations-menu.png)

   **Verifica l’organizzazione**

   Per verificare di aver eseguito l’accesso all’[organizzazione](organizations.md) giusta, fai clic sull’avatar del tuo profilo per visualizzarne il nome. Se ha accesso a più organizzazioni, puoi anche vedere le altre e passare a un’altra organizzazione direttamente dalla barra dell’intestazione.

   Se la tua organizzazione usa Federated ID, Experience Cloud ti consente accedere in modalità single sign-on, senza inserire l’indirizzo e-mail e la password. Aggiungi `#/sso:@domain` all’URL di Experience Cloud (`https://experience.adobe.com`) per eseguire questa attività.

   Ad esempio, per un’organizzazione con Federated ID e il dominio `adobecustomer.com`, imposta il link dell’URL su `https://experience.adobe.com/#/sso:@adobecustomer.com`. Puoi anche passare direttamente a una specifica applicazione salvando come segnalibro o preferito l’URL seguito dal percorso dell’applicazione. Ad esempio, per Adobe Analytics: `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.

## Accedere alle applicazioni di Experience Cloud {#navigation}

Dopo aver effettuato l’accesso ad Experience Cloud, è possibile accedere rapidamente a tutte le applicazioni, i servizi e le organizzazioni dall’lintestazione unificata.

Per accedere alle applicazioni e ai servizi Experience Cloud per i quali disponi dei diritti di accesso nella tua organizzazione, passa al selettore delle applicazioni ![menu](assets/menu-icon.png).

![Accedere alle applicazioni Experience Cloud](assets/platform-core-services.png)

## Supporto dei browser in Experience Cloud {#browser}

Per prestazioni ottimali, Experience Cloud è stato ottimizzato per i browser più diffusi, comprese l’ultima versione e le due versioni precedenti.

* Chrome
* Edge
* Firefox
* Opera
* Safari

Se il tuo browser non è elencato, potrebbe comunque essere supportato, ma si consiglia di usare uno dei browser elencati.

>[!NOTE]
>
>Non tutte le applicazioni in esecuzione nel dominio Experience Cloud supportano tutti i browser. In caso di dubbi, consulta la documentazione delle specifiche applicazioni.

## Supporto delle lingue in Experience Cloud {#languages}

Experience Cloud supporta le lingue preferite per ciascun utente, impostate nelle preferenze del proprio account utente Adobe. Sono supportate le seguenti lingue:

* Cinese
* Inglese
* Francese
* Tedesco
* Italiano
* Giapponese
* Coreano
* Portoghese
* Spagnolo
* Taiwanese

Tutti i team delle applicazioni sono orientati al supporto globale delle lingue; tuttavia, non tutte le applicazioni sono disponibili in tutte le lingue sopraelencate. Se la tua lingua principale non è supportata in un’applicazione Experience Cloud, puoi impostare una lingua secondaria che, all’occorrenza, verrà usata per impostazione predefinita. Puoi impostare queste opzioni nelle [preferenze utente di Experience Cloud](https://experience.adobe.com/preferences).

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
* Cercare le [organizzazioni](organizations.md)
* Uscire
* Configurare preferenze, notifiche e abbonamenti dell’account

Per gestire le preferenze, seleziona **[!UICONTROL Preferenze]** nel menu dell’account ![preferenze](assets/preferences-icon-sm.png).

![Profilo utente e preferenze account](assets/preferences-page.png)

Nelle [!UICONTROL preferenze di Experience Cloud], è possibile configurare le seguenti funzioni:

| Funzione | Descrizione |
|--- |--- |
| [Organizzazione](organizations.md) predefinita | Seleziona l’organizzazione da visualizzare all’avvio di Experience Cloud. |
| [!UICONTROL Raccolta dati sui prodotto] | Seleziona le tecnologie che Adobe può utilizzare per raccogliere i dati sul modo in cui utilizzi i suoi prodotti. |
| [!UICONTROL Promozioni e consigli personalizzati per l’apprendimento] | Scegli dove desideri ricevere informazioni personalizzate sui tuoi prodotti Adobe. Puoi riceverle tramite e-mail, nel prodotto stesso e nelle community Experience League. [Ulteriori informazioni.](personalized-learning-preferences.md) |
| [!UICONTROL Abbonamenti] | Seleziona i prodotti e le categorie a cui desideri abbonarti. Notifiche nel riquadro a comparsa [!UICONTROL Notifiche] e via e-mail. |
| [!UICONTROL Priorità] | Seleziona le categorie a cui vuoi assegnare la priorità alta. Queste categorie sono contrassegnate con il tag Alta e possono essere configurate per la distribuzione come avvisi. |
| [!UICONTROL Avvisi] | Seleziona le notifiche per le quali desideri visualizzare gli avvisi nel browser. Gli avvisi vengono visualizzati per alcuni secondi nell’angolo in alto a destra della finestra. |
| E-mail | Specifica la frequenza con cui desideri ricevere le e-mail di notifica: Non inviata, Immediata, Giornaliera o Settimanale. |

{style=&quot;table-layout:auto&quot;}

## Notifiche e annunci {#notifications}

Seleziona **[!UICONTROL Notifiche]** per ricevere avvisi sugli aggiornamenti rilevanti e fruibili, inclusi rilasci di prodotto, avvisi di manutenzione, elementi condivisi e richieste di approvazione.

![Notifiche e annunci](assets/notifications-menu-small.png)

## Domini di Experience Cloud {#domains}

Experience Cloud usa i seguenti host per fornire l’applicazione e migliorare le prestazioni e l’esperienza di utilizzo del prodotto. Per un’esperienza ottimale, Adobe consiglia di aggiungere questi domini all’elenco Consentiti del tuo firewall. Specifiche applicazioni Experience Cloud, ad esempio Adobe Analytics, potrebbero utilizzare domini aggiuntivi. Per informazioni, consulta la documentazione delle singole applicazioni.

| Tecnologia | Domini |
|--- |--- |
| Domini di Adobe Experience Cloud | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Identity Management Service (IMS) | `adobelogin.com` |
| Font di Experience Cloud | `typekit.net` |
| Raccolta dati di Adobe (per informazioni e guida del prodotto) | `adobedtm.com` |
| Gainsight (per l’Aiuto e le guide dei prodotti) | `esp.aptrinsic.com` |

## Ottenere aiuto per l’amministrazione e i servizi tra diverse applicazioni

Questa guida fornisce informazioni utili per l’amministrazione di utenti e prodotti Experience Cloud tramite Admin Console e l’abilitazione delle applicazioni per i servizi Platform. Puoi anche accedere all’Aiuto per Libreria tipi di pubblico, Attributi del cliente, Experience Cloud Assets e altro ancora:

* [[!UICONTROL Libreria pubblico]](audience-library.md)
* [[!UICONTROL Attributi del cliente]](attributes.md)
* [[!UICONTROL Triggers]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Cookie di Experience Cloud](cookies-privacy.md)
* [Gestione di utenti e prodotti](admin-getting-started.md) (Admin Console)
* [Abilitare le applicazioni per i servizi principali](core-services.md)
* [Domande frequenti](admin-getting-started.md)
* [Organizzazioni e collegamento di account](organizations.md)
* [Integrazioni](marketing-cloud-integrations.md)
* [Integrazione di Adobe Target con Experience Cloud](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=it)
* [Panoramica sulla privacy e sulla sicurezza di Experience Cloud](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [Recupero preventivo del DNS](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## Guide

Le guide correlate a Experience Cloud includono:

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=it)
* [Grafico Co-op di Experience Platform](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=it)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it)
* [Experience Platform Data Collection/Launch](https://experienceleague.adobe.com/docs/launch.html?lang=it)
* [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=it)
* [[!UICONTROL Dynamic Tag Management]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=it)

## Tutorial

Sfrutta i tutorial e le guide pratiche disponibili in Experience League:

* [Tutti i tutorial in Experience League](https://experienceleague.adobe.com/?lang=it#quick-how-tos)
* [Tutorial su Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=it)
* [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=it)

## Note sulla versione e guide relative a Experience Cloud

* [Documentazione del prodotto per tutte le applicazioni Experience Cloud](https://experienceleague.adobe.com/docs/home.html?lang=it): cerca aiuto nella sezione Informazioni e supporto di Experience Cloud
* [Note sulla versione e aggiornamenti dei prodotti](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it): le novità di Experience Cloud, tutti gli aggiornamenti per chi si abbona
* [Esercitazioni per l&#39;implementazione dei servizi core](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=en): video ed esercitazioni sui servizi core
* [Assistenza degli esperti di Experience League](https://experienceleague.adobe.com/?lang=it): ottieni informazioni guidate dagli esperti e dalla community
* [Formazione e training](https://helpx.adobe.com/it/learning.html?promoid=KAUDK): interagisci con Adobe per trarre il massimo dai nostri prodotti.
* [Blog sull&#39;esperienza dei clienti](https://blog.adobe.com/it/topics/digital-transformation): leggi il blog Experience Cloud
* [Assistenza clienti](https://experienceleague.adobe.com/?support-solution=General&amp;lang=it#support): contatta l&#39;Assistenza clienti Adobe
