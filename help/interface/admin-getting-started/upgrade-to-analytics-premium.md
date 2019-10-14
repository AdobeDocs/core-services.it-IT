---
description: Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall'aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.
keywords: aggiornamento
seo-description: Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall'aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.
seo-title: Aggiornamento ad Analytics Premium e Experience Cloud
solution: Experience Cloud
title: Aggiornamento ad Analytics Premium e Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: c0ba39895218769e27ab99568387eb91310a574c

---


# Aggiornamento ad Analytics Premium e Experience Cloud

Gli amministratori possono scoprire i requisiti e cosa aspettarsi dall'aggiornamento ad Analytics Premium e dove trovare le informazioni necessarie in qualità di amministratore Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Con l'aggiornamento ad Adobe Analytics Premium hai accesso a tutte le funzionalità e prodotti disponibili in Analytics Standard, inclusi Data Warehouse, Ad Hoc Analysis, Report Builder e Data Connectors (questi prodotti erano venduti separatamente ai clienti tramite la soluzione SiteCatalyst).

Analytics Premium fornisce:

* Accesso a 250 variabili di conversione (eVars)
* [Mobile App Analytics](https://marketing.adobe.com/resources/help/en_US/mobile/)
* Data Workbench (query di dati visivi; attribuzione sulle regole; analisi tra canali)

>[!NOTE]
>
>Durante l'aggiornamento non è necessario effettuare alcuna migrazione, ma vi sono alcune considerazioni di cui tenere conto:
>
>* Le eVar 76-250 (SiteCatalyst) e 100-250 (Standard) saranno visibili in Strumenti, ma non saranno ancora abilitate.&gt;
>* Contribution Analysis viene avviato da Adobe. Non cambia posizione (è ancora disponibile nella pagina Rilevamento anomalie) ma ora verrà avviato automaticamente analizzando tutti i punti di dati.&gt;


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

In Analytics Premium Complete, puoi utilizzare tutte le funzionalità di [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), più i seguenti aggiornamenti:

| Prodotto | Aggiornamenti |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Analisi di contributo](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[Attributi del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Fino a 200)</li></ul> |
| Data Workbench | <ul><li>Attribuzione algoritmica</li><li>Aree di lavoro pre-costruite</li></ul> |
| Piattaforma Analytics | [Flusso live](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) (dati non elaborati, dashboard, attivatori) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

L'aggiornamento a Predictive Intelligence abilita [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) più:

| Prodotto | Aggiornamenti |
|---|---|
| Reports &amp; Analytics | [Analisi di contributo](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | Aree di lavoro pre-costruite per le qualifiche dei tipi di pubblico e il marketing predittivo. |
| Piattaforma Analytics | Flusso live (dashboard e attivatori) |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

L'aggiornamento a Customer 360 offre [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) più:

| Prodotto | Aggiornamenti |
|--- |--- |
| [Attributi del cliente](../attributes/attributes.md) | Attributi del cliente (analisi e condivisione del segmento) |
| Data Workbench | <ul><li>Attributi del cliente derivati</li><li>Aree di lavoro pre-costruite per l'individuazione di tipi di pubblico</li></ul> |
| Piattaforma Analytics | [Attributi del cliente](../attributes/attributes.md) |

## Advanced Attribution {#section_9E4986A8389946CCAA7D003268343296}

Advanced Attribution offre l'accesso ad [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), più Algorithmic Attribution in Data Workbench (25% del volume chiamate server).

## Requisiti Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Gli utenti supportati possono richiedere che tutte le licenze dei clienti siano aggiornate per riflettere la versione Premium scrivendo un'e-mail all'indirizzo `dwb@adobe.com`. Ciò abilita funzioni come Attribuzione algoritmica.

TechOps controllerà il tuo impegno contrattuale e determinerà l'infrastruttura gestita, aumentando o diminuendo la capacità; quindi si coordinerà con te tramite l'Account Manager o consultandoti, per distribuire eventuali modifiche.

Qualsiasi software avviato localmente deve essere disattivato. Questo include Sensor, il che significa che dovrai garantire il corretto tracciamento tramite i tag di Analytics.

## Experience Cloud - Amministrazione utenti e prodotti {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud e i servizi principali sono disponibili per gli utenti di Analytics Standard e Premium, purché sia stata eseguita la modernizzazione dell’implementazione descritta in [Guida introduttiva: Abilitare le soluzioni per i servizi di base](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (questa procedura consente di modernizzare la propria implementazione e di diventare amministratori in Experience Cloud).

Dopo l’iscrizione a Experience Cloud, puoi accedere tramite Experience Cloud all’indirizzo [!DNL marketing.adobe.com] e iniziare a usare i servizi di base (inclusi gli attributi del cliente, pubblico e analisi app dispositivi mobili).

**Amministrare utenti e gruppi**

La gestione utenti viene eseguita in [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) (collegamento prodotto).

Puoi impostare una mappatura 1:1 tra un gruppo creato in Adobe Admin Console e un gruppo della soluzione (come Adobe Analytics). Quindi, per un nuovo utente aggiunto al gruppo Admin Console verrà automaticamente creato un account soluzione Analytics che sarà collegato all'Adobe ID dell'utente (gli utenti esistenti devono collegare manualmente le credenziali dell'account della soluzione per accedere alle soluzioni tramite l'accesso a Experience Cloud).

>[!NOTE]
>
>Puoi mappare più gruppi della soluzione a un gruppo Admin Console. Tuttavia, Adobe consiglia una mappatura 1:1. La mappatura preventiva dei gruppi consente di invitare, creare, assegnare autorizzazioni e aggiungere più utenti caricando un CSV.
