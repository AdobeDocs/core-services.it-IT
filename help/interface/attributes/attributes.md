---
description: Panoramica e prerequisiti per il caricamento di attributi cliente in Experience Cloud.
keywords: core services;Customer Attributes
seo-description: Panoramica e prerequisiti per il caricamento di attributi cliente in Experience Cloud.
seo-title: Attributi cliente
solution: Experience Cloud
title: Attributi cliente
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 75d3d045964aa42f7ac6b32b25cfd77aa7f663a9
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 71%

---


# Attributi cliente

Passa a **[!DNL Experience Platform]** > **[!UICONTROL Persone]** > Attributi **[!UICONTROL cliente]**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

![](assets/custom_reports.png)

## Prerequisiti per il caricamento di attributi del cliente {#section_BD38693AFBF34926BA28E964963B4EA0}

* **Abilitazione della soluzione:** [Abilita le tue soluzioni per i servizi](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)Experience Platform.

* **Appartenenza al gruppo:** Per caricare i dati attributo del cliente, gli utenti devono essere membri del gruppo [Attributi](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)cliente. Devi anche appartenere a un gruppo Adobe Analytics o Adobe Target.

   To know whether your company has access to Customer Attributes, your [!DNL Experience Cloud] administrator should log into the [Experience Cloud](https://experience.adobe.com). Navigate to **[!UICONTROL Administration]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. If *Customer Attributes* displays as one of the [!UICONTROL Product Profiles], you are ready to begin.

   Users that are added to the Customer Attributes will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

* **Per gli attributi del cliente è necessario Adobe Target**[!DNL at.js] (qualsiasi versione) o [!DNL mbox.js] versione 58 o successiva.

   Consulta [Come distribuire l’implementazione at.js](https://docs.adobe.com/content/help/it-IT/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) o [Mbox.js](https://docs.adobe.com/content/help/it-IT/target/using/implement-target/client-side/mbox-implement/mbox-download.html).

## Cosa sono i dati cliente Enterprise? {#section_6F34C29F11414842AA57D2B1248FA3C6}

I dati Enterprise risiedono in altri sistemi. Possono risultare complessi e diversi a seconda delle persone. Questi dati includono informazioni come appartenenze, livello di fedeltà, età, genere, prodotti posseduti, interessi e lifetime value.

L’immagine seguente è un esempio di un file di dati che mostra i dati dell’utente con sottoscrizione per prodotti, inclusi gli ID membro, i prodotti autorizzati, i prodotti più lanciati e così via.

![](assets/01_crs_usecase.png)

Dopo aver generato il file dati, puoi caricarlo nella fonte dell’attributo cliente che si crea in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Attributi del cliente]**.

Consulta [Caricamento dei dati degli attributi del cliente](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) per conoscere questo flusso di lavoro.

## Casi d’utilizzo della soluzione {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Quando i dati si trovano in Experience Cloud, puoi personalizzarli e condividerli con soluzioni per reporting, segmentazioni, attività e campagne.

Ad esempio:

| Soluzione | Vantaggi e casi d’uso |
|--- |--- |
| Adobe Analytics | Gli esperti di marketing e gli analisti sono pienamente consapevoli dei seguenti fatti:<ul><li>Le campagne online sono più efficaci con i tuoi clienti di livello Gold.</li><li>Quali sono i prodotti ricercati dai clienti di livello gold rispetto a clienti di livello platinum.</li><li>Se la nuova progettazione del tuo sito web sta avendo un impatto positivo sui tassi di conversione per i clienti meno recenti.</li><li>Quali sono i prodotti più ricercati nel mio sito dai clienti con un lifetime value basso.</li></ul> |
| Adobe Target | I dati attributo consentono agli utenti di Adobe Target di:<ul><li>Mostrare sconti e offerte speciali ai membri del club fedeltà.</li><li>Consigliare prodotti più costosi ai clienti di lusso.</li><li>Per i clienti che già ricevono le e-mail, inserisci un’offerta di upselling nello spazio normalmente riservato alle iscrizioni e-mail</li></ul> |
