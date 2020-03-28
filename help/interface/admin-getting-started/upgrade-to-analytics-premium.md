---
description: Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall'aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.
keywords: upgrading
seo-description: Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall'aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.
seo-title: Aggiornamento ad Analytics Premium e Experience Cloud
solution: Experience Cloud
title: Aggiornamento ad Analytics Premium e Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Aggiornamento ad Analytics Premium e Experience Cloud

Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall&#39;aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

L&#39;aggiornamento ad Adobe Analytics Premium offre tutte le funzionalità o i prodotti disponibili in Analytics Standard, inclusi Data Warehouse, Analisi ad hoc, Generatore di report e Connettori dati. (Questi prodotti sono stati venduti separatamente ai clienti che utilizzano la soluzione SiteCatalyst.)

Analytics Premium offre:

* Accesso a 250 variabili di conversione (eVar)
* [Mobile App Analytics](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)
* Data Workbench (query di dati visivi; attribuzione sulle regole; analisi tra canali)

>[!NOTE]
>
>Durante l&#39;aggiornamento non è necessaria alcuna migrazione, ma è necessario tenere presenti alcune considerazioni:
>
>* Le eVar 76-250 (SiteCatalyst) e 100-250 (Standard) saranno visibili in Strumenti di amministrazione, ma non saranno già abilitate.>
>* Contribution Analysis è attivato da Adobe. Non cambierà posizione (è ancora disponibile nella pagina Rilevamento anomalie), ma ora inizierà automaticamente l&#39;analisi di tutti i punti dati.>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

In Analytics Premium Complete, avrai a disposizione tutte le funzionalità di [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), più i seguenti aggiornamenti:

| Prodotto | Aggiornamenti |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Analisi contributi](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Fino a 200)</li></ul> |
| Data Workbench | <ul><li>Attribuzione algoritmica</li><li>Aree di lavoro pre-costruite</li></ul> |
| Piattaforma Analytics | [Flusso](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) live (dati non elaborati, dashboard, attivatori) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

L&#39;aggiornamento a Predictive Intelligence abilita [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) più:

| Prodotto | Aggiornamenti |
|---|---|
| Reports &amp; Analytics | [Analisi contributi](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | Aree di lavoro pre-costruite per le qualifiche del pubblico e il marketing predittivo. |
| Piattaforma Analytics | Flusso live (dashboard e attivatori) |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

L&#39;aggiornamento a Customer 360 offre [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) più:

| Prodotto | Aggiornamenti |
|--- |--- |
| [Attributi del cliente](../attributes/attributes.md) | Attributi del cliente (analisi e condivisione del segmento) |
| Data Workbench | <ul><li>Attributi del cliente derivati</li><li>Aree di lavoro pre-costruite per la scoperta dell&#39;audience</li></ul> |
| Piattaforma Analytics | [Attributi del cliente](../attributes/attributes.md) |

## Advanced Attribution {#section_9E4986A8389946CCAA7D003268343296}

Advanced Attribution offre l&#39;accesso ad [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), più Algorithmic Attribution in Workbench dati (25% del volume di chiamate server).

## Requisiti Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Gli utenti supportati possono richiedere che tutte le licenze dei clienti siano aggiornate per riflettere la versione Premium scrivendo un&#39;e-mail all&#39;indirizzo `dwb@adobe.com`. Questo abilita funzioni come Attribuzione algoritmica.

TechOps controllerà il tuo impegno contrattuale e determinerà l&#39;infrastruttura gestita corretta, aumentando o riducendo la capacità, e poi si coordinerà con te, tramite Account Manager o consultandoti, per distribuire eventuali modifiche.

Qualsiasi software in esecuzione in sede deve essere disattivato. Questo include Sensor, il che significa che dovrai garantire il corretto tracciamento attraverso i tag di Analytics.

## Experience Cloud - Amministrazione utenti e prodotti {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud e i servizi principali sono disponibili per gli utenti di Analytics Standard e Premium, purché sia stata eseguita la modernizzazione dell’implementazione descritta in [Guida introduttiva: Abilitare le soluzioni per i servizi di base](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (questa procedura consente di modernizzare la propria implementazione e di diventare amministratori in Experience Cloud).

Dopo l’iscrizione a Experience Cloud, puoi accedere tramite Experience Cloud all’indirizzo [!DNL experiencecloud.adobe.com] e iniziare a usare i servizi di base (inclusi gli attributi del cliente, pubblico e analisi app dispositivi mobili).

### Amministrare utenti e gruppi

La gestione degli utenti viene eseguita in [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) (collegamento prodotto).

Puoi impostare una mappatura 1:1 tra un gruppo creato in Adobe Admin Console e un gruppo della soluzione (come Adobe Analytics). Successivamente, un nuovo utente aggiunto al gruppo Admin Console avrà un account soluzione Analytics automaticamente creato e collegato all&#39;Adobe ID dell&#39;utente. (Gli utenti esistenti devono collegare manualmente le credenziali dell&#39;account della soluzione per accedere alle soluzioni tramite l&#39;accesso a Experience Cloud.)

>[!NOTE]
>
>Puoi mappare più gruppi della soluzione a un gruppo Admin Console. Tuttavia, Adobe consiglia la mappatura 1:1. La mappatura dei gruppi in anticipo consente di invitare, creare, concedere autorizzazioni e aggiungere più utenti caricando un CSV.
