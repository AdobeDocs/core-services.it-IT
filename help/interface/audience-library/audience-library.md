---
description: Gestisci la trasformazione dei dati dei visitatori in segmenti di pubblico.
seo-description: Gestisci la trasformazione dei dati dei visitatori in segmenti di pubblico.
seo-title: Tipi di pubblico
solution: Experience Cloud
title: Audiences
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: 14d6e0ae15b023ad4dd3f8aca0606f26b39a21e9

---


# Tipi di pubblico {#topic_679810123CAA4E0CA4FA3417FB0100C7}

Le audience sono raccolte di visitatori (un elenco di ID visitatore). I servizi di audience di Adobe gestiscono la conversione dei dati dei visitatori in segmenti di pubblico. La creazione e la gestione dei tipi di pubblico sono simili alla creazione e all&#39;uso dei segmenti, e in più permettono di condividere i segmenti di pubblico in [!DNL Experience Cloud].

![](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create in [!DNL Experience Cloud]
* Da segmenti di [!DNL Analytics] pubblicati in [!DNL Experience Cloud]
* Da [!DNL Audience Manager]

**Tipi di pubblico in tempo reale e basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per l&#39;uso in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics ad Audience Manager non sono accessibili per il targeting in tempo reale. Il sistema valuta il pubblico in due modi:

* Le audience storiche di Analytics vengono valutate ogni 4 ore. Il tempo totale di elaborazione e condivisione può richiedere fino a 8 ore.  Le audience storiche includono sempre i visitatori di ritorno.
* I dati in tempo reale provengono dal servizio Experience Cloud Audiences e sono valutati in tempo reale.

## Utilizzo dei tipi di pubblico da parte delle soluzioni {#concept_01EB9345C5344597BC94A864EDD38EE1}

La tabella seguente descrive come i tipi di pubblico vengono utilizzati nelle soluzioni Experience Cloud:

| Soluzione | Descrizione |
|--- |--- |
| Experience Cloud Audiences | Crea, gestisci e condividi tipi di pubblico in modo nativo mediante l’interfaccia della [Libreria Pubblico](../audience-library/audience-library.md). È possibile:<ul><li>Utilizzo di audience in tempo reale tramite gli attributi di analisi non elaborati</li><li>Combinazione di tipi di pubblico per creare un pubblico composito, unire dati storici e in tempo reale</li><li>Vedere visualizzazioni grafiche delle dimensioni stimate dell&#39;audience</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consulta: Audience [Experience Cloud](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analytics | Durante l&#39;attività di segmentazione, puoi costruire un segmento, combinarlo con una suite di rapporti e quindi  [ pubblicarlo in Experience Cloud](../audience-library/audience-library.md). Il segmento pubblicato viene visualizzato nella pagina [Audiences](../audience-library/audience-library.md). Il tipo di pubblico è inoltre disponibile come pubblico di destinazione per un&#39;esperienza di campagna in Adobe Target e in Audience Manager.   Quando un pubblico viene condiviso da Analytics e selezionato per l&#39;utilizzo in una campagna attiva, tutti i profili visitatore che soddisfano i requisiti di definizione del segmento per i precedenti 90 giorni vengono inviati alla piattaforma dei servizi Audiences di Experience Cloud.   Il limite per i tipi di pubblico condivisi è stato aumentato a 75.  Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri unici. Inoltre, a causa della cache, sono necessarie 12 ore prima che l&#39;eliminazione delle suite di rapporti in Analytics possa essere visibile in Experience Cloud. |
| Mobile Services | Analizzare il traffico mobile utilizzando la visualizzazione sunburst nel rapporto Tipi [!UICONTROL di] dispositivi. |
| Target | The [ID service](https://docs.adobe.com/content/help/en/id-service/using/home.html) unifies visitor IDs and data into a single, actionable profile for use across solutions. La casella di controllo [Pubblica in Experience Cloud](../audience-library/audience-library.md), selezionabile in fase di creazione del segmento in Adobe Analytics, permette di rendere disponibile il segmento nella libreria di tipi di pubblico personalizzata di Adobe Target. Puoi utilizzare un segmento creato in Analytics o Audience Manager per attività in Target.  Ad esempio, puoi creare campagne sulla base delle metriche di conversione di Analytics e sui segmenti di pubblico creati in Analytics. |
| Audience Manager | Le audience condivise sono disponibili nella segmentazione di Audience Manager. Tutti i tipi di pubblico di Experience Cloud sono disponibili in formato nativo in Audience Manager, che fornisce:<ul><li>Automazione incorporata per quanto riguarda il modo in cui vengono condivisi e utilizzati nei flussi di lavoro delle soluzioni</li><li>Destinazioni fuori sede</li><li>Modellazione simile</li></ul> |
| Campaign | <ul><li>importare i tipi di pubblico condivisi da diverse soluzioni Adobe Experience Cloud in Adobe Campaign;</li><li>Esportare gli elenchi dei destinatari sotto forma di audience condivise. Questi tipi di pubblico condivisi possono essere utilizzati nelle diverse soluzioni Adobe Experience Cloud che utilizzi.</li></ul> |
| Media Optimizer | Utilizzate l&#39;audience come target. |

>[!IMPORTANT]
>
>Quando un visitatore si qualifica per l&#39;audience condivisa da Analytics, si verifica un ritardo di 4-8 ore prima che tali informazioni siano fruibili in Target, Ad Cloud e Campaign Standard.

## Ulteriore aiuto: domande, guida e casi di utilizzo {#section_C7F151644D8A45F7B6FC54F58845635D}

| Assistenza con | Risorsa |
|--- |--- |
| Non riesci a trovare Audiences? | Verifica di avere il provisioning. Consulta  [Guida introduttiva: Abilitare le soluzioni per i servizi principali](../core-services/core-services.md).<br>Fate clic [qui](https://www.adobe.com/go/audiences) per richiedere l&#39;accesso a Profili e pubblico (modulo di provisioning integrazioni). |
| Casi di utilizzo | Per maggiori informazioni sulla soluzione da utilizzare, vai a Opzioni [di creazione](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) pubblico nella Knowledge Base. |
| Forum | The [Audiences forum](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) is an additional resource to get help with audiences. |

## Elementi dell&#39;interfaccia libreria di tipi di pubblico {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL Persone]** > Libreria **[!UICONTROL Pubblico]**

![](assets/audience_library.png)

| Elemento | Descrizione |
|--- |--- |
| Nuovo | [Creazione di un pubblico](../audience-library/audience-library.md). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | Persona che ha creato il segmento di pubblico. |
| Origine | Identifica la posizione in cui è stata creata l&#39;audience.<ul><li>**Analytics:** un segmento creato in Reports &amp; Analytics o Ad Hoc Analysis e [pubblicato in Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud:** un nuovo pubblico [creato in Experience Cloud Audiences](../audience-library/audience-library.md).</li><li>**Audience Manager:** i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in Experience Cloud Audiences.</li></ul> |
| Dimensioni attuali | Dimensione corrente del pubblico. |
| Attivo | Lo stato attivo del segmento. |
