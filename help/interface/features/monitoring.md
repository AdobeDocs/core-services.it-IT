---
title: Monitoraggio dell’utilizzo di IA per l’agente
description: Scopri le dashboard per il monitoraggio dell’utilizzo dell’intelligenza artificiale in CX Enterprise. Tieni traccia dell’adozione, rivedi le conversazioni e i feedback, e gestisci i crediti IA per l’utilizzo, la qualità e la visibilità dei costi.
solution: Experience Cloud, Experience Platform
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
autotag-review: '2026-05-27T16:30:16.764Z'
TQID: 'https://experienceleague.adobe.com/J74yr0gGkFu1bzTmMvhrQ8TNaRX6nRjWY9WAwd3uydk'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87id: e1971122-7081-4556-9222-8a31bd71800c
feature_v2: id: f84b2906-3ce9-4ef0-86f6-cda249273937
subfeature_v2: id: cda95149-19e1-4cfa-a57e-751283a32378
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: c3e850d9398b5439a45fd493036776b729bec7e9
workflow-type: tm+mt
source-wordcount: 948
ht-degree: 2%

---

# Monitoraggio dell’IA agente

CX Enterprise fornisce due dashboard per monitorare l&#39;utilizzo di IA per l&#39;agente nelle applicazioni CX Enterprise esistenti. Queste dashboard consentono di comprendere l&#39;adozione, il coinvolgimento, la qualità del feedback e il consumo di credito AI per [!DNL Experience Platform Agents] a cui gli utenti accedono tramite [!DNL AI Assistant] e altre superfici conversazionali.

Gli agenti nell&#39;ambito del monitoraggio dell&#39;utilizzo sono elencati in [Agenti di IA nelle app CX Enterprise esistenti](agentic-ai.md#existing-apps-table) nella [Agentic AI nella documentazione di Adobe CX Enterprise](agentic-ai.md).

## Dashboard utilizzo licenze

Il dashboard Utilizzo licenze di [!DNL Adobe Experience Platform] mostra i crediti AI concessi in licenza della tua organizzazione e il totale dei crediti AI utilizzati dagli utenti che eseguono [!DNL Experience Platform Agents].

Gli amministratori utilizzano questo dashboard per tenere traccia dell’utilizzo delle licenze in base all’adesione. Per accedere al dashboard, vedi [Dashboard di utilizzo della licenza](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/guides/license-usage) nella documentazione di [!DNL Experience Platform].

## Dashboard di monitoraggio di IA agente

Il dashboard di monitoraggio di IA per l’analisi dell’agente offre ai membri del Centro di eccellenza (COE) e ad altre parti interessate alla governance visibilità sull’utilizzo e l’adozione di IA per l’analisi dell’agente. È possibile visualizzare le tendenze per periodi di 7 o 30 giorni per vedere chi utilizza [!DNL AI Assistant] o altre superfici di conversazione (ad esempio [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms)) per interagire con [!DNL Experience Platform Agents], le operazioni eseguite in tali interazioni e il valore ricevuto.

Il dashboard di monitoraggio di IA per l’agente include le visualizzazioni seguenti:

| Dashboard di | Scopo |
| --- | --- |
| **Panoramica** | Metriche aggregate per utenti, conversazioni, feedback e consumo di credito |
| **Utenti** | Frequenza di utilizzo, distribuzione e coinvolgimento per utente |
| **Feedback** | Segnali sulla qualità della risposta e sulla soddisfazione degli utenti |
| **Crediti IA** | Andamenti dei consumi di credito e saldo residuo |

Insieme, queste visualizzazioni ti aiutano a guidare l’adozione degli agenti con dati anziché presupposti.

## Dashboard panoramica

La dashboard Panoramica è il punto centrale per le metriche di adozione e coinvolgimento in tutta l’organizzazione. Collega le tendenze di alto livello ad analisi più approfondite. Da qualsiasi metrica, puoi approfondire singole conversazioni per vedere cosa guida i numeri.

### Metriche nel dashboard Panoramica

* **Richieste nel tempo:** Tendenze generali di crescita dell&#39;utilizzo e di adozione.
* **Utenti e conversazioni attivi:** numero di utenti che interagiscono con [!DNL Experience Platform Agents].
* **Numero medio di richieste per conversazione:** Profondità di coinvolgimento per conversazione.
* **Feedback:** Distribuzione dei commenti degli utenti (solo per [!DNL AI Assistant] interazioni).

### Ripetizione conversazione

La ripetizione della conversazione mostra singole interazioni, non solo aggregati. Puoi analizzare i pattern in molte conversazioni e passare da tendenze di alto livello a una conversazione specifica.

* **Cronologia richieste e risposte:** La richiesta dell&#39;utente e le risposte inviate.
* **Segnali di feedback:** Interazioni contrassegnate da pollici in alto o in basso per identificare attriti, blocchi o esigenze di attivazione. Queste informazioni aiutano la tua organizzazione a migliorare la rilevanza dei messaggi immediati e consentono ad Adobe di migliorare la qualità della risposta nel tempo.

## Dashboard utenti

Il dashboard Utenti mostra come l’adozione e il coinvolgimento degli agenti variano nel tempo tra gli utenti. Puoi vedere chi utilizza attivamente [!DNL Experience Platform Agents], quale superficie utilizzano e con quale frequenza interagiscono. Gli amministratori e i membri del CDE possono approfondire le attività e le conversazioni dei singoli utenti per comprendere i modelli di coinvolgimento e il comportamento di utilizzo.

### Metriche nel dashboard Utenti

* **Tendenze di adozione e coinvolgimento nel tempo:** Tieni traccia del cambiamento dei segmenti utente durante il periodo selezionato. Gli utenti sono classificati come:
   * **Nuova:** prima attività nel periodo selezionato, senza attività nei 12 mesi precedenti.
   * **Ripeti:** attività nel periodo selezionato e nel periodo precedente.
   * **Restituzione:** attività nel periodo selezionato, ma non nel periodo precedente.
   * **Inattiva:** Nessuna attività nel periodo selezionato, ma attività nel periodo precedente.
* **Modelli di coinvolgimento degli utenti:** con quale frequenza gli utenti interagiscono con gli agenti e come il coinvolgimento cambia nel tempo.
* **Attività conversazione:** Numero di conversazioni e prompt per utente.
* **Utenti attivi principali:** Utenti e team altamente coinvolti che hanno adottato l&#39;agente motore.

## Dashboard feedback

Il dashboard Feedback mostra il feedback degli utenti inviato per le interazioni degli agenti. Puoi vedere quali conversazioni gli utenti hanno contrassegnato in modo positivo o negativo e indagare le interazioni dietro il feedback. Dai riepiloghi dei feedback, approfondisci le singole conversazioni per rivedere prompt, risposte, dettagli dei motivi e note di feedback.

### Metriche nel dashboard Feedback

* **Tendenze del feedback nel tempo:** come cambia il feedback degli utenti nel tempo.
* **Miniature in alto e miniature in basso feedback:** segnali di interazione positivi e negativi.
* **Categorie di feedback:** Motivazione dietro ogni pollice verso l&#39;alto e verso il basso.
* **Cronologia richieste e risposte:** i prompt utente e le risposte associate ai feedback inviati.
* **Dettagli e note del feedback:** Contesto e commenti aggiuntivi degli utenti durante l&#39;invio del feedback.

## Dashboard crediti IA

Il dashboard Crediti AI mostra come l&#39;utilizzo di [!DNL Experience Platform Agents] da parte dell&#39;organizzazione si traduce nel consumo di crediti AI.

### Metriche nel dashboard Crediti AI

* **Totale crediti IA utilizzati:** Utilizzo complessivo dell&#39;agente nei crediti IA.
* **Tendenze giornaliere e mensili:** picchi, cali e cambiamenti nei modelli di consumo.
* **Crediti AI rimanenti:** Saldo rimanente per consentire una pianificazione proattiva ed evitare interruzioni.

## Accesso e governance

Le dashboard di monitoraggio dell’utilizzo dell’intelligenza artificiale agente espongono l’attività dell’Assistente AI, inclusi modelli di utilizzo, approfondimenti a livello di conversazione, segnali di feedback e metriche operative. Alcune di queste informazioni possono includere dati sensibili sul contesto aziendale, sull’attività immediata o sull’interazione dell’utente.

L’accesso è basato su autorizzazioni ed è destinato solo agli amministratori di COE autorizzati e agli utenti di governance approvati. Nella sezione seguente viene descritto come concedere le autorizzazioni del dashboard.

## Abilita autorizzazioni dashboard

Concedi l&#39;accesso al dashboard in [!DNL Adobe Experience Platform] aggiornando il profilo o il ruolo di prodotto per ogni utente autorizzato.

1. Vai a [!DNL Experience Platform] **Amministrazione** > **Autorizzazioni**.

1. Apri il profilo di prodotto o il ruolo che desideri aggiornare.

   ![Abilita autorizzazioni dashboard](../features/assets/dashboards-permissions.png)

1. In **[!UICONTROL AI Assistant]** autorizzazioni, fare clic su **[!UICONTROL Add Resource]**, quindi abilitare **[!UICONTROL View AI Assistant usage dashboard]**.

   Questa autorizzazione consente di accedere alle dashboard di monitoraggio dell’utilizzo di IA per l’agente.

1. Nelle autorizzazioni **[!UICONTROL Dashboards]**, configura l&#39;accesso al dashboard in base alle responsabilità di ogni utente.

   ![Abilita autorizzazioni dashboard](../features/assets/dashboards-add-resource.png)

   Autorizzazioni consigliate per gli utenti di governance autorizzati:

   * **[!UICONTROL View License Usage Dashboard]**
   * **[!UICONTROL View Standard Dashboards]**
   * **[!UICONTROL Export Dashboard Data]** (facoltativo, solo per utenti di governance approvati)

   Se necessario, puoi concedere altre autorizzazioni:

   * **[!UICONTROL Manage Custom Dashboards]**
   * **[!UICONTROL View Custom Dashboards]**
   * **[!UICONTROL Manage Standard Dashboards]**

## Ulteriori informazioni su questo argomento

* [IA agente in Adobe CX Enterprise](agentic-ai.md)
* [Processi agente e consumo credito IA](ai-credit-consumption.md)
* [Dashboard utilizzo licenze](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/guides/license-usage) (Experience Platform)
