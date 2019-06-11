---
description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
keywords: servizi di base; attributi del cliente
seo-description: Panoramica e prerequisiti sul caricamento degli attributi del cliente in Experience Cloud.
seo-title: Attributi cliente
solution: Experience Cloud
title: Attributi cliente
uuid: 1621402 d -990 f -46 f 9-981 a -473280559069
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Attributi cliente

## Panoramica

La [!UICONTROL funzionalità degli attributi] del cliente in Experience Cloud si trova qui.

**[!UICONTROL Persone]** &gt; **[!UICONTROL Attributi del cliente]**

Se acquisisci dati del cliente di livello Enterprise in un database CRM (Customer Relationship Management), puoi caricare tali dati in una sorgente dati di attributi cliente in Experience Cloud. Una volta caricati, utilizzate i dati in [!DNL Adobe Analytics] e [!DNL Adobe Target].

![](assets/custom_reports.png)

## Prerequisiti per caricare attributi del cliente {#section_BD38693AFBF34926BA28E964963B4EA0}


* **Abilitazione della soluzione:**[Abilita le soluzioni per i servizi di base](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Iscrizione al gruppo:** per caricare i dati degli attributi cliente, gli utenti devono essere membri del gruppo    [Attributi del cliente](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9). Devi far parte di un gruppo Adobe Analytics o Adobe Target.

   Per verificare se la società ha accesso agli attributi del cliente, l&#39; [!DNL Experience Cloud] amministratore deve effettuare l&#39;accesso [!DNL Experience Cloud]. Passa **[!UICONTROL a Amministrazione]** &gt; **[!UICONTROL Avvia Admin Console]** &gt; **[!UICONTROL Gruppi]**. Se *gli attributi del cliente* sono visualizzati come uno dei gruppi, sei pronto per iniziare.

   Gli utenti che vengono aggiunti al gruppo Attributi del cliente visualizzeranno la voce di menu [!UICONTROL Attributi cliente] presente sul lato sinistro dell&#39;interfaccia Experience Cloud.

* **Mbox target:** per gli attributi cliente è richiesto mbox.js versione 58 o superiore.


   Consulta [Implementazione di mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov/t_mbox_download.html).

* **at.js:** qualsiasi versione.




## Cosa sono i dati dei clienti Enterprise? {#section_6F34C29F11414842AA57D2B1248FA3C6}

I dati Enterprise risiedono in altri sistemi. Può essere una cosa complessa e diversa a seconda delle persone. Questi dati includono informazioni come appartenenze, livello di fedeltà, età, genere, prodotti posseduti, interessi e lifetime value.

L&#39;immagine seguente è un esempio di un file di dati che mostra i dati dell&#39;utente con sottoscrizione per prodotti, inclusi ID membro, prodotti autorizzati, prodotti avviati più spesso e così via.

![](assets/01_crs_usecase.png)

Dopo aver creato il file di dati, puoi caricarlo nell&#39;origine attributo del cliente che hai creato in **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Attributi del cliente]**.

Consultate [Caricare i dati attributo del cliente](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) per apprendere questo flusso di lavoro.

## Casi d&#39;uso della soluzione {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Quando i dati si trovano in Experience Cloud, puoi personalizzarli e condividerli con le soluzioni per reporting, segmentazioni, attività e campagne.

Ad esempio:

| Soluzione | Vantaggi e casi di utilizzo |
|--- |--- |
| Adobe Analytics | I responsabili di marketing e gli analisti possono comprendere:<ul><li>Qual è la campagna online più efficace con i clienti di livello gold.</li><li>I prodotti cercati dai clienti di livello gold rispetto a quelli cercati dai clienti di livello platinum.</li><li>Se il nuovo sito Web ha un impatto positivo sui tassi di conversione per i clienti meno recenti.</li><li>Quali sono i prodotti più cercati nel sito dai clienti con un lifetime value basso.</li></ul> |
| Adobe Target | I dati degli attributi consentono agli utenti di Target di:<ul><li>Offrire sconti e offerte speciali ai membri del club più fedeli.</li><li>Consigliare prodotti più costosi ai clienti di lusso.</li><li>Proporre offerte di upselling ai clienti che già ricevono le e-mail nello spazio normalmente riservato alle registrazioni delle e-mail.</li></ul> |
