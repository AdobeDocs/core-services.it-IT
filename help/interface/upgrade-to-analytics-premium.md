---
description: Scopri i requisiti e cosa aspettarsi dall’aggiornamento ad Analytics Premium.
solution: Experience Cloud
title: Aggiornamento ad Analytics Premium e Experience Cloud
topic: Administration
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Admin
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 90%

---

# Aggiornamento ad Analytics Premium e Experience Cloud

Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall&#39;aggiornamento ad Analytics Premium, oltre a dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

L&#39;aggiornamento ad Adobe Analytics Premium offre tutte le funzionalità o i prodotti disponibili in Analytics Standard, inclusi Data Warehouse, Ad Hoc Analysis, Report Builder e Data Connectors.

Analytics Premium offre:

* Accesso a 250 variabili di conversione (eVar)
* [Analytics per app mobili](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=it)
* Data Workbench (query di dati visivi; attribuzione sulle regole; analisi tra canali)

>[!NOTE]
>
>Durante l&#39;aggiornamento non è necessaria alcuna migrazione, ma occorre tenere presenti alcune considerazioni:
>
>* Le eVar 76-250 e 100-250 (Standard) sono visibili in Admin Tools, ma non sono abilitate.
>* Analisi contributi è attivata da Adobe. Non cambierà posizione (resta disponibile nella pagina di rilevamento delle anomalie), ma adesso inizierà automaticamente ad analizzare tutti i punti dati.

## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

All&#39;interno di Analytics Premium Complete, avrai a disposizione tutte le funzionalità di [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre ai seguenti aggiornamenti:

| Prodotto | Aggiornamenti |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Analisi contributi](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=it)</li><li>[Attributi del cliente](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Fino a 200)</li></ul> |
| Data Workbench | <ul><li>Algorithmic Attribution</li><li>Aree di lavoro predefinite</li></ul> |
| Platform Analytics | [Streaming live](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md) (dati non elaborati, dashboard, trigger) |

{style="table-layout:auto"}

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

L&#39;aggiornamento a Predictive Intelligence abilita [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|---|---|
| Reports &amp; Analytics | [Analisi contributi](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=it) |
| Data Workbench | Aree di lavoro predefinite per le qualifiche del pubblico e il marketing predittivo |
| Platform Analytics | Streaming live (dashboard e trigger) |

{style="table-layout:auto"}

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

L&#39;aggiornamento a Customer 360 offre [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|--- |--- |
| [Attributi del cliente](attributes.md) | Attributi del cliente (analisi e condivisione del segmento) |
| Data Workbench | <ul><li>Attributi del cliente derivati</li><li>Aree di lavoro predefinite per il rilevamento del pubblico</li></ul> |
| Platform Analytics | [Attributi del cliente](attributes.md) |

{style="table-layout:auto"}

## Advanced Attribution {#section_9E4986A8389946CCAA7D003268343296}

Advanced Attribution offre l&#39;accesso ad [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre alla funzionalità Algorithmic Attribution in Data Workbench (25% del volume di chiamate al server).

## Requisiti Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Gli utenti supportati possono richiedere che tutte le licenze dei clienti siano aggiornate per riflettere la versione Premium scrivendo un&#39;e-mail all&#39;indirizzo `dwb@adobe.com`. In tal modo, si abilitano funzioni come Algorithmic Attribution.

In base al tuo contratto, il team TechOps determinerà l’infrastruttura gestita applicabile, aumentando o riducendo la capacità di conseguenza. Infine, tramite il tuo Account Manager o consultandoti direttamente, coordinerà l’implementazione di eventuali modifiche.

Qualsiasi software in esecuzione locale deve essere disattivato. Questo software include Sensor e devi quindi assicurare il corretto tracciamento tramite i tag [!DNL Analytics].

## Experience Cloud - Amministrazione utenti e prodotti {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud e i servizi principali sono disponibili per gli utenti di Analytics Standard e Premium, purché sia stata eseguita la modernizzazione dell’implementazione come descritto in [Guida introduttiva: abilitare le applicazioni per i servizi principali](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). Questa procedura consente di modernizzare l’implementazione e di diventare amministratori in Experience Cloud.

Dopo aver partecipato a Experience Cloud, puoi accedere tramite Experience Cloud all’indirizzo [!DNL experience.adobe.com] e inizia a utilizzare i servizi core (tra cui Attributi del cliente, Audiences e analisi delle app mobili).

### Amministrare utenti e gruppi

La gestione degli utenti viene eseguita all&#39;interno di [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html) (collegamento al prodotto).

Puoi impostare una mappatura 1:1 tra un gruppo creato in Adobe Admin Console e un gruppo della soluzione (come Adobe Analytics). Successivamente, viene aggiunto un nuovo utente al gruppo Admin Console, il quale disporrà di un account dell’applicazione Analytics creato in automatico e collegato al relativo Adobe ID. Per accedere alle applicazioni tramite Experience Cloud, gli utenti esistenti devono effettuare il collegamento manuale delle credenziali dell’account dell’applicazione.

>[!NOTE]
>
>Puoi mappare più gruppi dell’applicazione a un gruppo Admin Console. Tuttavia, Adobe consiglia di effettuare la mappatura 1:1. Grazie al caricamento di un file CSV, la mappatura anticipata dei gruppi consente di invitare, creare, concedere autorizzazioni e aggiungere più utenti.
