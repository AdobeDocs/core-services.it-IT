---
description: Scopri i requisiti e cosa aspettarsi dall’aggiornamento ad Analytics Premium.
keywords: Aggiornamento ad Adobe Analytics Premium
solution: Experience Cloud
title: 'Aggiornamento ad Analytics Premium e Experience Cloud '
topic: Amministrazione
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Amministratore
level: Esperienza
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 95%

---


# Aggiornamento ad Analytics Premium e Experience Cloud

Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall&#39;aggiornamento ad Analytics Premium, oltre a dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

L&#39;aggiornamento ad Adobe Analytics Premium offre tutte le funzionalità o i prodotti disponibili in Analytics Standard, inclusi Data Warehouse, Ad Hoc Analysis, Report Builder e Data Connectors. Questi prodotti sono stati venduti separatamente ai clienti che utilizzano la soluzione a punti, SiteCatalyst.

Analytics Premium offre:

* Accesso a 250 variabili di conversione (eVar)
* [Analytics per app mobili](https://docs.adobe.com/content/help/it-IT/mobile-services/using/home.html)
* Data Workbench (query di dati visivi; attribuzione sulle regole; analisi tra canali)

>[!NOTE]
>
>Durante l&#39;aggiornamento non è necessaria alcuna migrazione, ma occorre tenere presenti alcune considerazioni:
>
>* Le eVar 76-250 (SiteCatalyst) e 100-250 (Standard) saranno visibili in Strumenti di amministrazione, ma non saranno già abilitate.>
>* Analisi contributi è attivata da Adobe. Non cambierà posizione (è ancora disponibile nella pagina Rilevazione delle anomalie), ma adesso inizierà automaticamente l&#39;analisi di tutti i punti dati.>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

All&#39;interno di Analytics Premium Complete, avrai a disposizione tutte le funzionalità di [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre ai seguenti aggiornamenti:

| Prodotto | Aggiornamenti |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Analisi contributi](https://docs.adobe.com/content/help/it-IT/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Fino a 200)</li></ul> |
| Data Workbench | <ul><li>Algorithmic Attribution</li><li>Aree di lavoro predefinite</li></ul> |
| Platform Analytics | [Streaming live](https://helpx.adobe.com/it/analytics/kb/getting-started-with-livestream-api.html) (dati non elaborati, dashboard, trigger) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

L&#39;aggiornamento a Predictive Intelligence abilita [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|---|---|
| Reports &amp; Analytics | [Analisi contributi](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | Aree di lavoro predefinite per le qualifiche del pubblico e il marketing predittivo |
| Platform Analytics | Streaming live (dashboard e trigger) |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

L&#39;aggiornamento a Customer 360 offre [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|--- |--- |
| [Attributi del cliente](../attributes/attributes.md) | Attributi del cliente (analisi e condivisione del segmento) |
| Data Workbench | <ul><li>Attributi del cliente derivati</li><li>Aree di lavoro predefinite per il rilevamento del pubblico</li></ul> |
| Platform Analytics | [Attributi del cliente](../attributes/attributes.md) |

## Advanced Attribution {#section_9E4986A8389946CCAA7D003268343296}

Advanced Attribution offre l&#39;accesso ad [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre alla funzionalità Algorithmic Attribution in Data Workbench (25% del volume di chiamate al server).

## Requisiti Data Workbench  {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Gli utenti supportati possono richiedere che tutte le licenze dei clienti siano aggiornate per riflettere la versione Premium scrivendo un&#39;e-mail all&#39;indirizzo `dwb@adobe.com`. In tal modo, si abilitano funzioni come Algorithmic Attribution.

TechOps esaminerà il tuo impegno contrattuale e determinerà l&#39;infrastruttura gestita adatta, aumentando o riducendo la capacità di conseguenza. Infine si coordinerà insieme a te per la distribuzione di eventuali modifiche, tramite Account Manager o consultandoti direttamente.

Qualsiasi software in esecuzione locale deve essere disattivato. Tra di essi rientra Sensor, il che significa che dovrai garantire il corretto tracciamento attraverso i tag di Analytics.

## Experience Cloud - Amministrazione utenti e prodotti {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud e i servizi principali sono disponibili per gli utenti di Analytics Standard e Premium, purché sia stata eseguita la modernizzazione dell&#39;implementazione descritta in [Guida introduttiva: Abilitare le soluzioni per i servizi di base](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (questa procedura consente di modernizzare la propria implementazione e di diventare amministratori in Experience Cloud).

Dopo aver effettuato l&#39;iscrizione a Experience Cloud, puoi accedere tramite Experience Cloud dalla pagina [!DNL experiencecloud.adobe.com] e iniziare a utilizzare i servizi core (tra cui attributi del cliente, tipi di pubblico e analisi delle app mobile).

### Amministrare utenti e gruppi

La gestione degli utenti viene eseguita all&#39;interno di [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/help/aedash.html) (collegamento al prodotto).

Puoi impostare una mappatura 1:1 tra un gruppo creato in Adobe Admin Console e un gruppo della soluzione (come Adobe Analytics). Successivamente, viene aggiunto un nuovo utente al gruppo Admin Console, il quale disporrà di un account della soluzione di analisi creato in automatico e collegato al relativo Adobe ID. Per accedere alle soluzioni tramite Experience Cloud, gli utenti esistenti devono effettuare il collegamento manuale delle credenziali dell&#39;account della soluzione.

>[!NOTE]
>
>Puoi mappare più gruppi della soluzione a un gruppo Admin Console. Tuttavia, Adobe consiglia di effettuare la mappatura 1:1. Grazie al caricamento di un file CSV, la mappatura anticipata dei gruppi consente di invitare, creare, concedere autorizzazioni e aggiungere più utenti.
