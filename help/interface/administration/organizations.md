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
TQID: https://experienceleague.adobe.com/DCb0MQWwB0MOGALSDbLD-d4ik4B0C249xncB9eZbZMU
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: bdea9bc8-5600-45db-b85e-d74bb59dfcffid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 573
ht-degree: 48%

---

# Organizzazioni e collegamento di account

Un *organizzazione* (ID organizzazione) è l&#39;entità che consente all&#39;amministratore di configurare gruppi e utenti e di controllare il single sign-on in Experience Cloud.

L’organizzazione funziona come un’azienda che può effettuare un log-in che comprende tutti i prodotti e le applicazioni Experience Cloud. Nella maggior parte dei casi, un’organizzazione è il nome dell’azienda. Tuttavia, un’azienda può avere più organizzazioni.

![Organizzazioni Experience Cloud](../assets/organizations-menu.png)

Per verificare di aver effettuato l&#39;accesso all&#39;organizzazione corretta, fare clic su **[!UICONTROL Profile]** per visualizzare il nome dell&#39;organizzazione predefinita. Se hai accesso a più organizzazioni, puoi anche visualizzare e passare a un’altra organizzazione nella barra dell’intestazione.

>[!NOTE]
>
>Il passaggio tra le organizzazioni consente di accedere ad Admin Console per quell’organizzazione specifica. Se l’organizzazione desiderata non viene visualizzata nell’elenco, potrebbe essere necessario richiedere l’accesso a un amministratore dell’organizzazione. Se hai bisogno di unire più istanze di Admin Console, contatta l’Assistenza clienti di Adobe per ricevere assistenza.

## Federated ID

Se la tua organizzazione usa Federated ID, Experience Cloud ti consente accedere in modalità single sign-on, senza inserire l’indirizzo e-mail e la password. Aggiungi `#/sso:@domain` all’URL di Experience Cloud (`https://experience.adobe.com`) per eseguire questa attività.

Ad esempio, per un’organizzazione con Federated ID e il dominio `example.com`, imposta il link dell’URL su `https://experience.adobe.com/#/sso:@example.com`. Puoi anche passare direttamente a una specifica applicazione salvando come segnalibro o preferito l’URL seguito dal percorso dell’applicazione. Ad esempio, per Adobe Analytics: `https://experience.adobe.com/#/sso:@example.com/analytics`.

## Visualizza l&#39;ID organizzazione

Puoi individuare l’ID organizzazione assegnato a scopo di supporto. Puoi verificare di essere nell&#39;organizzazione corretta o cambiare organizzazione utilizzando il selettore **[!UICONTROL Organization]** nell&#39;intestazione.

L’ID organizzazione è l’ID associato all’azienda con provisioning di Experience Cloud. Questo ID è una stringa alfanumerica composta da 24 caratteri, seguita da (deve includere) `@AdobeOrg`.

Per visualizzare l&#39;ID organizzazione e altre informazioni sull&#39;account, utilizzare la scelta rapida da tastiera **Ctrl+i** da qualsiasi pagina in `https://experience.adobe.com`.

**Per visualizzare l&#39;ID organizzazione**

1. In [Experience Cloud](https://experience.adobe.com), premi **Ctrl+i** sulla tastiera.

   ![ID delle organizzazioni assegnate](../assets/assigned-organization.png)

1. In **[!UICONTROL User Information]**, cerca **[!UICONTROL Current Org ID]** e puoi individuare l&#39;ID organizzazione.

   In alternativa, gli amministratori possono accedere ad Admin Console (passare a [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) e visualizzare l&#39;ID organizzazione nell&#39;URL.

   Ad esempio, nell’URL seguente:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   L’ID è:

   `C538193582390300A495CC9@AdobeOrg`

## Collegamento di un account applicazione a un Adobe ID

In genere, gli amministratori di Experience Cloud concedono l’accesso ad applicazioni e servizi. In rare circostanze, è possibile collegare le credenziali dell’applicazione a un Adobe ID.

1. Segui i passaggi contenuti nell’invito e-mail ad Experience Cloud.

1. Accedi utilizzando il tuo Adobe ID o Enterprise ID.

1. Fare clic su **[!UICONTROL Application selector]**. ( ![menu](../assets/apps-icon.png)).

   ![Collegare un account applicazione a un Adobe ID](../assets/solutions-active.png)

   Le applicazioni a cui hai accesso sono colorate.

1. Fai clic sull’applicazione desiderata.

   ![Fai clic sull&#39;applicazione](../assets/analytics-link-accounts.png)

   Questo tipo di messaggio mostra se fai parte del gruppo appropriato (e disponi dell’autorizzazione per l’applicazione) ma non hai ancora collegato le credenziali del tuo account al tuo Adobe ID.

1. Fare clic su **[!UICONTROL Link Account]**, quindi fornire le credenziali.

## Specificare un&#39;organizzazione predefinita

È possibile specificare un&#39;organizzazione predefinita da utilizzare al momento dell&#39;accesso.

1. Nell&#39;intestazione fare clic su **[!UICONTROL Profile]**, quindi su Preferenze.

1. In [!UICONTROL General], selezionare un&#39;organizzazione predefinita.


![Modifica profilo](../assets/edit-profile.png)

## Risoluzione dei problemi di collegamento dell&#39;account

Assistenza per problemi derivanti dal collegamento dell’account.

In genere, il collegamento dell’account ha esito negativo perché l’Adobe ID è collegato a un utente precedente. Quando non è possibile eseguire il collegamento, prova le seguenti operazioni:

* [Contatta l’Assistenza Adobe](https://experienceleague.adobe.com/?support-solution=General&lang=it#support).
* Durante la risoluzione del problema, accedi all’applicazione con la procedura standard.

