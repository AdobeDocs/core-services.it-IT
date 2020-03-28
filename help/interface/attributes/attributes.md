---
description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
keywords: core services;customer attributes
seo-description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
seo-title: Attributi cliente
solution: Experience Cloud
title: Attributi cliente
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Attributi cliente

To locate [!UICONTROL customer attributes] navigate to **[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

![](assets/custom_reports.png)

## Prerequisiti per il caricamento di attributi del cliente {#section_BD38693AFBF34926BA28E964963B4EA0}

* **Abilitazione della soluzione:** [Abilitare le soluzioni per i servizi principali](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Iscrizione al gruppo:** per caricare i dati degli attributi cliente, gli utenti devono essere membri del gruppo  [Attributi del cliente](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9). Devi anche appartenere a un gruppo Adobe Analytics o Adobe Target.

   Per verificare se la società dispone dell’accesso agli attributi del cliente, l’amministratore di [!DNL Experience Cloud] deve effettuare l’accesso a [!DNL Experience Cloud]. Navigate to **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]** > **[!UICONTROL Groups]**. Se *Attributi cliente* è visualizzato come uno dei gruppi, è pronto per iniziare.

   Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi cliente] presente sul lato sinistro dell&#39;interfaccia Experience Cloud.

* **Per gli attributi del cliente è necessario Adobe Target** (qualsiasi versione) o [!DNL at.js] [!DNL mbox.js] versione 58 o successiva.

   Consultate [Come distribuire l&#39;implementazione at.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) o [Mbox.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html).

## What is enterprise customer data? {#section_6F34C29F11414842AA57D2B1248FA3C6}

I dati Enterprise risiedono in altri sistemi. Può essere complesso e significare cose diverse per persone diverse. Questi dati possono includere informazioni quali appartenenze, livello di fedeltà, età, genere, prodotti posseduti, interessi e lifetime value.

L&#39;immagine seguente è un esempio di un file di dati che mostra i dati dell&#39;utente iscritto per i prodotti, inclusi gli ID membro, i prodotti autorizzati, i prodotti più lanciati e così via.

![](assets/01_crs_usecase.png)

After you create the data file, you can upload it to the customer attribute source that you create in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

Consulta [Caricamento dei dati degli attributi del cliente](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) per conoscere questo flusso di lavoro.

## Casi d’utilizzo della soluzione {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Dopo che i dati si trovano in Experience Cloud, puoi personalizzarli e condividerli con le soluzioni per reporting, segmentazione, attività e campagne.

Ad esempio:

| Soluzione | Vantaggi e casi di utilizzo |
|--- |--- |
| Adobe Analytics | Gli esperti di marketing e gli analisti possono comprendere:<ul><li>Campagne online più efficaci con i clienti di livello gold.</li><li>I prodotti cercati dai clienti di livello gold rispetto ai prodotti cercati dai clienti di livello platinum.</li><li>Se la riprogettazione del sito ha un impatto positivo sui tassi di conversione per i clienti meno recenti.</li><li>Quali sono i prodotti che i clienti con un lifetime value basso tendono a cercare sul sito.</li></ul> |
| Adobe Target | I dati attributo consentono agli utenti di Adobe Target di:<ul><li>Mostra sconti e offerte speciali ai membri del club fedeltà.</li><li>Consiglia prodotti più costosi ai clienti di lusso.</li><li>Per i clienti che già ricevono le e-mail, visualizzate un&#39;offerta up-sell nello spazio normalmente riservato alle registrazioni e-mail</li></ul> |
