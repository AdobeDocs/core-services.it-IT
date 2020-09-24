---
description: Gestisci come tradurre i dati sui visitatori in segmentazione del pubblico, con Libreria tipi di pubblico di Experience Cloud.
seo-description: Gestisci come tradurre i dati sui visitatori in segmentazione del pubblico, con Libreria tipi di pubblico di Experience Cloud.
seo-title: Panoramica di Experience Cloud Audiences
solution: Experience Cloud
title: Panoramica di Experience Cloud Audiences
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: 1809543ce26ed0e6dc2bf973de46384a2ef13c32
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 95%

---


# Panoramica di Experience Cloud Audiences {#topic_679810123CAA4E0CA4FA3417FB0100C7}

I tipi di pubblico sono raccolte di visitatori (un elenco di ID visitatore).  Adobe  Libreria Pubblico consente di gestire la conversione dei dati dei visitatori in segmenti di pubblico. As such, creating and managing audiences is similar to creating and using segments, with the added ability to share the audience segment to products and services in [!DNL Experience Cloud].

![](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create in [!DNL Experience Cloud]
* Da segmenti di [!DNL Analytics] pubblicati in [!DNL Experience Cloud]
* Da [!DNL Audience Manager]

**Tipi di pubblico in tempo reale e basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per l&#39;uso in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics ad Audience Manager non sono accessibili per il targeting in tempo reale. Il sistema valuta i pubblici in due modi:

* I pubblici storici di Analytics vengono valutati ogni 4 ore. Il tempo totale di elaborazione e condivisione può richiedere fino a 8 ore. I pubblici storici includono sempre i visitatori di ritorno.
* I dati in tempo reale provengono dal servizio Experience Cloud Audiences e sono valutati in tempo reale.

## Utilizzo dei tipi di pubblico da parte delle soluzioni {#concept_01EB9345C5344597BC94A864EDD38EE1}

La tabella seguente descrive come i pubblici vengono utilizzati nelle soluzioni Experience Cloud:

| Soluzione | Descrizione |
|--- |--- |
| Experience Cloud Audiences | Crea, gestisci e condividi tipi di pubblico in modo nativo mediante l’interfaccia della [Libreria Pubblico](../audience-library/audience-library.md). È possibile:<ul><li>Utilizzare pubblici in tempo reale tramite gli attributi di analisi non elaborati</li><li>Combinare pubblici per creare pubblici compositi, unendo dati storici e in tempo reale</li><li>Visualizzare graficamente le dimensioni stimate dei pubblici</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consulta: [Pubblici di Experience Cloud](https://helpx.adobe.com/it/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analytics | Durante l’attività di segmentazione, puoi costruire un segmento, combinarlo con una suite di rapporti e quindi  pubblicarlo in Experience Cloud. Quando si pubblica un segmento, questo viene visualizzato nella pagina [!UICONTROL Libreria tipi di pubblico] di Experience Cloud. Per informazioni dettagliate, consulta [Pubblicare segmenti in Experience Cloud](https://docs.adobe.com/content/help/it-IT/analytics/components/segmentation/segmentation-workflow/seg-publish.html) nell’Aiuto di Analytics. Il pubblico è inoltre disponibile come pubblico di destinazione per un’esperienza di campagna in Adobe Target e in Audience Manager. Una volta che un pubblico viene condiviso da Adobe Analytics e selezionato per essere utilizzato in una campagna attiva, tutti i profili di visitatori che hanno soddisfatto i criteri di definizione del segmento nei precedenti 90 giorni vengono inviati alla piattaforma [!UICONTROL Servizi di pubblico] di Experience Cloud. Il limite per i tipi di pubblico condivisi è stato aumentato a 75. Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri unici. Inoltre, a causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud. |
| Mobile Services | Analizza il traffico dei dispositivi mobili utilizzando la visualizzazione radiale nel rapporto [!UICONTROL Tipi di dispositivi]. |
| [!DNL Target] | Il [servizio ID](https://docs.adobe.com/content/help/it-IT/id-service/using/home.html) unisce ID e dati dei visitatori in un singolo profilo actionable da utilizzare nelle soluzioni. La casella di controllo [Pubblica in Experience Cloud](../audience-library/audience-library.md), selezionabile in fase di creazione del segmento in Adobe Analytics, permette di rendere disponibile il segmento nella libreria di tipi di pubblico personalizzata di Adobe Target. Un segmento creato in Analytics o Audience Manager può essere utilizzato per attività in [!DNL Target]. Ad esempio, puoi creare campagne sulla base delle metriche di conversione di [!DNL Analytics] e sui segmenti di pubblico creati in [!DNL Analytics]. |
| Audience Manager | I pubblici condivisi sono disponibili nella segmentazione di Audience Manager. Tutti i tipi di pubblico di Experience Cloud sono disponibili in formato nativo in Audience Manager, che fornisce:<ul><li>Automazione incorporata riguardo il modo in cui vengono condivisi e utilizzati nei flussi di lavoro delle soluzioni</li><li>Destinazioni esterne</li><li>Modellazione lookalike</li></ul> |
| Campaign | <ul><li>importare i tipi di pubblico condivisi da diverse soluzioni Adobe Experience Cloud in Adobe Campaign;</li><li>Esporta gli elenchi dei destinatari sotto forma di pubblici condivisi. Questi pubblici condivisi possono essere utilizzati nelle diverse soluzioni Adobe Experience Cloud che utilizzi.</li></ul> |
| Media Optimizer | Utilizza il pubblico come target. |

>[!IMPORTANT]
>
>Quando un visitatore diventa idoneo per il pubblico condiviso da Analytics, trascorrono 4-8 ore prima che tale informazione sia utilizzabile in [!DNL Target], Ad Cloud e Campaign Standard.

## Ulteriore aiuto: domande, guida e casi di utilizzo {#section_C7F151644D8A45F7B6FC54F58845635D}

| Aiuto con | Risorsa |
|--- |--- |
| Non riesci a trovare Pubblico? | Verifica di avere il provisioning. Consulta   [Guida introduttiva: Abilitare le soluzioni per i servizi principali](../core-services/core-services.md).<br>Fai clic [qui](https://www.adobe.com/go/audiences) per richiedere l’accesso a Profili e pubblico (modulo di provisioning integrazioni). |
| Casi di utilizzo | Per maggiori informazioni sulla soluzione da utilizzare, vai in [Opzioni di creazione pubblico](https://helpx.adobe.com/it/marketing-cloud-core/kb/People/Audience-Creation-Options.html) nella Knowledge Base. |
| Forum | Il [forum di Audiences](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) è un’ulteriore risorsa per ottenere aiuto sui tipi di pubblico. |

## Elementi dell&#39;interfaccia libreria di tipi di pubblico {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL Persone]** > **[!UICONTROL Libreria pubblico]**

![](assets/audience_library.png)

| Elemento | Descrizione |
|--- |--- |
| Nuovo | [Creazione di un pubblico](../audience-library/audience-library.md). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | La persona che ha creato il segmento di pubblico. |
| Origine | Identifica la posizione in cui è stato creato il pubblico.<ul><li>**Analytics:** un segmento creato in Reports &amp; Analytics o Ad Hoc Analysis e [pubblicato in Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud:** un nuovo pubblico [creato in Experience Cloud Audiences](../audience-library/audience-library.md).</li><li>**Audience Manager:** i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in Experience Cloud Audiences.</li></ul> |
| Dimensione attuali | Dimensione attuale del pubblico. |
| Attivo | Lo stato attivo del segmento. |
