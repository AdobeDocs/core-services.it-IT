---
description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
keywords: servizi principali;attributi del cliente
seo-description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
seo-title: Attributi cliente
solution: Experience Cloud
title: Attributi cliente
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# Attributi cliente

## Panoramica

Per individuare [!UICONTROL gli attributi] del cliente su **[!DNL Experience Platform]****[!UICONTROL &gt; Persone]** &gt; **[!UICONTROL Attributi cliente]**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta effettuato l'aggiornamento, sfrutta i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

![](assets/custom_reports.png)

## Prerequisiti per il caricamento di attributi del cliente {#section_BD38693AFBF34926BA28E964963B4EA0}


* **Abilitazione della soluzione:** [Abilitare le soluzioni per i servizi principali](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Iscrizione al gruppo:** per caricare i dati degli attributi cliente, gli utenti devono essere membri del gruppo [Attributi del cliente](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9). Devi far parte di un gruppo Adobe Analytics o Adobe Target.

   Per verificare se la società dispone dell’accesso agli attributi del cliente, l’amministratore di [!DNL Experience Cloud] deve effettuare l’accesso a [!DNL Experience Cloud]. Passa a **[!UICONTROL Amministrazione]** &gt; **[!UICONTROL Avvia Admin Console]** &gt; **[!UICONTROL Gruppi]**. Se *Attributi cliente* è visualizzato come uno dei gruppi, è pronto per iniziare.

   Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi cliente] presente sul lato sinistro dell'interfaccia Experience Cloud.

* **Mbox target:** per gli attributi cliente è richiesto mbox.js versione 58 o superiore.


   Consulta [Implementazione di mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov/t_mbox_download.html).

* **at.js:** qualsiasi versione.




## Cosa sono i dati del cliente aziendale? {#section_6F34C29F11414842AA57D2B1248FA3C6}

I dati Enterprise risiedono in altri sistemi. Può essere una cosa complessa e diversa a seconda delle persone. Questi dati includono informazioni come appartenenze, livello di fedeltà, età, genere, prodotti posseduti, interessi e lifetime value.

L'immagine seguente è un esempio di un file di dati che mostra i dati dell'utente con sottoscrizione per prodotti, inclusi ID membro, prodotti autorizzati, prodotti avviati più spesso e così via.

![](assets/01_crs_usecase.png)

Dopo aver creato il file di dati, puoi caricarlo nell’origine degli attributi cliente che hai creato in **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Attributi del cliente]**.

Consulta [Caricamento dei dati degli attributi del cliente](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) per conoscere questo flusso di lavoro.

## Casi d’utilizzo della soluzione {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Quando i dati si trovano in Experience Cloud, puoi personalizzarli e condividerli con le soluzioni per reporting, segmentazioni, attività e campagne.

Ad esempio:

| Soluzione | Vantaggi e casi di utilizzo |
|--- |--- |
| Adobe Analytics | I responsabili di marketing e gli analisti possono comprendere:<ul><li>Qual è la campagna online più efficace con i clienti di livello gold.</li><li>I prodotti cercati dai clienti di livello gold rispetto a quelli cercati dai clienti di livello platinum.</li><li>Se il nuovo sito Web ha un impatto positivo sui tassi di conversione per i clienti meno recenti.</li><li>Quali sono i prodotti più cercati nel sito dai clienti con un lifetime value basso.</li></ul> |
| Adobe Target | I dati degli attributi consentono agli utenti di Target di:<ul><li>Offrire sconti e offerte speciali ai membri del club più fedeli.</li><li>Consigliare prodotti più costosi ai clienti di lusso.</li><li>Proporre offerte di upselling ai clienti che già ricevono le e-mail nello spazio normalmente riservato alle registrazioni delle e-mail.</li></ul> |
