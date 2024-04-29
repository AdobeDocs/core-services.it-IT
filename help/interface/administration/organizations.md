---
description: Scopri cosa sono le organizzazioni (ID organizzazione IMS) e come collegare gli account delle soluzioni a Experience Cloud.
solution: Experience Cloud
title: Organizzazioni e collegamento di account
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Organizations
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: 66f78a04674a82335f5df20c4c15d983b6ebdc66
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 69%

---

# Organizzazioni in Experience Cloud

Un *organizzazione* (ID organizzazione) è l&#39;entità che consente all&#39;amministratore di configurare gruppi e utenti e di controllare, ad Experience Cloud, il single sign-on.

L’organizzazione funziona come un’azienda che può effettuare un log-in che comprende tutti i prodotti e le applicazioni Experience Cloud. Nella maggior parte dei casi, un’organizzazione è il nome dell’azienda. Tuttavia, un’azienda può avere più organizzazioni.

![Experience Cloud organizzazioni](../assets/organizations-menu.png)

Per verificare di aver eseguito l’accesso all’organizzazione giusta, fai clic sull’avatar del tuo profilo per visualizzarne il nome. Se hai accesso a più organizzazioni, puoi anche visualizzare e passare a un’altra organizzazione nella barra dell’intestazione.

## Federated ID

Se la tua organizzazione usa Federated ID, Experience Cloud ti consente accedere in modalità single sign-on, senza inserire l’indirizzo e-mail e la password. Aggiungi `#/sso:@domain` all’URL di Experience Cloud (`https://experience.adobe.com`) per eseguire questa attività.

Ad esempio, per un’organizzazione con Federated ID e il dominio `adobecustomer.com`, imposta il link dell’URL su `https://experience.adobe.com/#/sso:@adobecustomer.com`. Puoi anche passare direttamente a una specifica applicazione salvando come segnalibro o preferito l’URL seguito dal percorso dell’applicazione. Ad esempio, per Adobe Analytics: `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.

## Visualizza l&#39;ID organizzazione {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

Puoi individuare l’ID organizzazione assegnato a scopo di supporto. Puoi verificare di essere nell’organizzazione corretta o cambiare organizzazione utilizzando il menu **[!UICONTROL Organizzazione]**.

L’ID organizzazione è l’ID associato all’azienda con provisioning di Experience Cloud. Questo ID è una stringa alfanumerica composta da 24 caratteri, seguita da (deve includere) `@AdobeOrg`.

Per visualizzare l’ID organizzazione e altre informazioni sull’account, utilizza la scelta rapida da tastiera **Ctrl+i** da qualsiasi pagina in `https://experience.adobe.com`.

**Per visualizzare l’ID organizzazione**

1. In entrata [Experience Cloud](https://experience.adobe.com), premere **Ctrl+i** sulla tastiera.

   ![ID delle organizzazioni assegnate](../assets/assigned-organization.png)

1. Sotto **[!UICONTROL Informazioni utente]**, cerca **[!UICONTROL ID organizzazione corrente]** e visualizzerai l’ID organizzazione.

   In alternativa, gli amministratori possono accedere all’Admin Console (passare a [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) e visualizzare l’ID organizzazione nell’URL.

   Ad esempio, nell’URL seguente:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   L’ID è:

   `C538193582390300A495CC9@AdobeOrg`

## Collegamento di un account applicazione a un Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

In genere, gli amministratori di Experience Cloud concedono l’accesso ad applicazioni e servizi. In rare circostanze, è possibile collegare le credenziali dell’applicazione a un Adobe ID.

1. Segui i passaggi contenuti nell’invito e-mail all’Experience Cloud.

1. Accedi utilizzando il tuo Adobe ID o Enterprise ID.

1. Seleziona il selettore delle applicazioni. ( ![menu](../assets/menu-icon.png)).

   ![Collegare un account applicazione a un Adobe ID](../assets/solutions-active.png)

   Le applicazioni a cui hai accesso sono colorate.

1. Seleziona l’applicazione desiderata:

   ![Selezionare l’applicazione desiderata](../assets/analytics-link-accounts.png)

   Questo tipo di messaggio mostra se fai parte del gruppo appropriato (e disponi dell’autorizzazione per l’applicazione) ma non hai ancora collegato le credenziali del tuo account al tuo Adobe ID.

1. Seleziona **[!UICONTROL Collega account]**, quindi immetti le tue credenziali.

## Specificare una organizzazione e una pagina di destinazione predefinite {#concept_6A191B42A9874A9780882903BA18F071}

Puoi specificare un&#39;organizzazione predefinita e una pagina di destinazione da usare al momento dell&#39;accesso.

Nel tuo profilo, seleziona **[!UICONTROL Modifica profilo]**.

![Modifica profilo](../assets/edit-profile.png)

In Organizzazione e pagina di destinazione predefinite puoi personalizzare la tua esperienza di accesso.

![Organizzazione e pagina di destinazione predefinite](../assets/default-organization.png)

## Risoluzione dei problemi di collegamento dell&#39;account {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Assistenza per problemi derivanti dal collegamento dell’account.

In genere, il collegamento dell’account ha esito negativo perché l’Adobe ID è collegato a un utente precedente. Quando non è possibile eseguire il collegamento, prova le seguenti operazioni:

* [Contatta l’Assistenza Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=it#support).
* Durante la risoluzione del problema, accedi all’applicazione con la procedura standard.
