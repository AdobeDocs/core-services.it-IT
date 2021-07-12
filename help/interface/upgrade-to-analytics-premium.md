---
description: Scopri i requisiti e cosa aspettarsi dall’aggiornamento ad Analytics Premium.
keywords: Aggiornamento ad Adobe Analytics Premium
solution: Experience Cloud
title: 'Aggiornamento ad Analytics Premium ed Experience Cloud '
topic: Amministrazione
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Admin
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 72%

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
>* Le eVar 76-250 e 100-250 (Standard) sono visibili in Strumenti di amministrazione, ma non sono abilitate.
>* Analisi contributi è attivata da Adobe. Non cambia posizione (è ancora disponibile nella pagina Rilevamento anomalie), ma inizia automaticamente l&#39;analisi di tutti i punti dati.


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

All&#39;interno di Analytics Premium Complete, avrai a disposizione tutte le funzionalità di [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre ai seguenti aggiornamenti:

| Prodotto | Aggiornamenti |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Analisi contributi](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en)</li><li>[Attributi del cliente](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Fino a 200)</li></ul> |
| Data Workbench | <ul><li>Algorithmic Attribution</li><li>Aree di lavoro predefinite</li></ul> |
| Platform Analytics | [Streaming live](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md) (dati non elaborati, dashboard, trigger) |

{style=&quot;table-layout:auto&quot;}

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

L&#39;aggiornamento a Predictive Intelligence abilita [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|---|---|
| Reports &amp; Analytics | [Analisi contributi](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en) |
| Data Workbench | Aree di lavoro predefinite per le qualifiche del pubblico e il marketing predittivo |
| Platform Analytics | Streaming live (dashboard e trigger) |

{style=&quot;table-layout:auto&quot;}

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

L&#39;aggiornamento a Customer 360 offre [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre a:

| Prodotto | Aggiornamenti |
|--- |--- |
| [Attributi del cliente](attributes.md) | Attributi del cliente (analisi e condivisione del segmento) |
| Data Workbench | <ul><li>Attributi del cliente derivati</li><li>Aree di lavoro predefinite per il rilevamento del pubblico</li></ul> |
| Platform Analytics | [Attributi del cliente](attributes.md) |

{style=&quot;table-layout:auto&quot;}

## Advanced Attribution {#section_9E4986A8389946CCAA7D003268343296}

Advanced Attribution offre l&#39;accesso ad [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), oltre alla funzionalità Algorithmic Attribution in Data Workbench (25% del volume di chiamate al server).

## Requisiti Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Gli utenti supportati possono richiedere che tutte le licenze dei clienti siano aggiornate per riflettere la versione Premium scrivendo un&#39;e-mail all&#39;indirizzo `dwb@adobe.com`. Questo aggiornamento abilita funzioni come Algorithmic Attribution.

TechOps esamina il tuo impegno contrattuale e determina l&#39;infrastruttura gestita corretta, aumentando o riducendo la capacità, e poi si coordinano con te, tramite Account Manager o consultandoti, per implementare eventuali modifiche.

Qualsiasi software in esecuzione locale deve essere disattivato. Questo software include Sensor, il che significa che devi garantire il corretto tracciamento attraverso i tag [!DNL Analytics] .

## Experience Cloud - Amministrazione utenti e prodotti {#section_6471C54454024301B2E0B687F79F6738}

Gli utenti di Analytics Standard e Premium possono accedere ad Experienci Cloud e servizi di base se hai seguito la modernizzazione dell&#39;implementazione descritta in [Guida introduttiva: Abilitare le soluzioni per i servizi di base](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (questa procedura consente di modernizzare la propria implementazione e di diventare amministratori in Experience Cloud).

Dopo aver effettuato l&#39;iscrizione a Experience Cloud, puoi accedere tramite Experience Cloud dalla pagina [!DNL experience.adobe.com] e iniziare a utilizzare i servizi core (tra cui attributi del cliente, tipi di pubblico e analisi delle app mobile).

### Amministrare utenti e gruppi

La gestione degli utenti viene eseguita all&#39;interno di [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html) (collegamento al prodotto).

Puoi impostare una mappatura 1:1 tra un gruppo creato in Adobe Admin Console e un gruppo della soluzione (come Adobe Analytics). Successivamente, un nuovo utente aggiunto al gruppo di Admin Console mappato ha un account soluzione Analytics creato automaticamente e collegato all&#39;Adobe ID dell&#39;utente. Per accedere alle soluzioni tramite Experience Cloud, gli utenti esistenti devono effettuare il collegamento manuale delle credenziali dell&#39;account della soluzione.

>[!NOTE]
>
>Puoi mappare più gruppi della soluzione a un gruppo Admin Console. Tuttavia, Adobe consiglia di effettuare la mappatura 1:1. Grazie al caricamento di un file CSV, la mappatura anticipata dei gruppi consente di invitare, creare, concedere autorizzazioni e aggiungere più utenti.
