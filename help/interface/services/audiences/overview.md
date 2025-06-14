---
title: '[!DNL Audience Library]'
description: Scopri come gestire la trasformazione dei dati dei visitatori in segmentazione del pubblico in Experience Cloud  [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: b257260bdbb7870dd6da807bceddfcddd2aef779
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 90%

---

# Tipi di pubblico di Experience Cloud {#topic_679810123CAA4E0CA4FA3417FB0100C7}

[!DNL Audience Library] mostra i tipi di pubblico in Experience Cloud. I tipi di pubblico sono raccolte di visitatori (un elenco di ID [!DNL Experience Cloud]). Puoi gestire la trasformazione dei dati dei visitatori in segmentazione del pubblico. La creazione e la gestione dei tipi di pubblico è simile alla creazione e all’utilizzo di segmenti. Puoi anche condividere il segmento di pubblico con i prodotti e i servizi di [!DNL Experience Cloud].

![Tipi di pubblico di Experience Cloud](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create in [!DNL Experience Cloud]
* Segmenti [!DNL Analytics] pubblicati in [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Tipi di pubblico in tempo reale o basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per l’uso in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics a Audience Manager non sono accessibili per il targeting in tempo reale. Il sistema valuta i tipi di pubblico in due modi:

* I tipi di pubblico storici di Analytics vengono valutati ogni quattro ore. Il tempo totale di elaborazione e condivisione può richiedere fino a otto ore. I tipi di pubblico storici includono sempre i visitatori di ritorno.
* I tipi di pubblico in tempo reale provengono dal servizio Experience Cloud Audiences e sono valutati in tempo reale.

## Utilizzo dei tipi di pubblico da parte delle applicazioni {#concept_01EB9345C5344597BC94A864EDD38EE1}

La tabella seguente descrive come vengono utilizzati i tipi di pubblico nelle applicazioni Experience Cloud:

| Soluzione | Descrizione |
|--- |--- |
| Experience Cloud Audiences | Crea, gestisci e condividi tipi di pubblico in modo nativo mediante la Libreria tipi di pubblico. È possibile:<ul><li>Utilizzare tipi di pubblico in tempo reale tramite gli attributi di analisi non elaborati</li><li>Combinare tipi di pubblico per creare tipi di pubblico compositi, unendo dati storici e in tempo reale</li><li>Visualizzare graficamente le dimensioni stimate dei tipi di pubblico</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consulta: [Opzioni di creazione dei tipi di pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=it). |
| Analytics | Durante l’attività di segmentazione, puoi costruire un segmento, combinarlo con una suite di rapporti e quindi pubblicarlo in Experience Cloud. La pubblicazione di un segmento viene mostrata nella pagina [!DNL Audience Library] di Experience Cloud. Per ulteriori informazioni, vedere [Segmenti di Publish all&#39;Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=it) nella Guida di [!DNL Analytics]. Il pubblico è inoltre disponibile come pubblico di destinazione per un&#39;esperienza di campagna in [!DNL Adobe Target] e in [!DNL Audience Manager]. Dopo aver condiviso un pubblico da [!DNL Adobe Analytics] e averlo selezionato per l’utilizzo in una campagna attiva, i profili visitatore che soddisfano i criteri di definizione del segmento per gli ultimi 90 giorni vengono inviati a [!UICONTROL Audience Services]. Il limite per i tipi di pubblico condivisi è stato aumentato a 75. I tipi di pubblico condivisi con Experience Cloud da [!DNL Analytics] non possono superare i 20 milioni di membri univoci. Inoltre, a causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud. |
| Mobile Services | Analizza il traffico dei dispositivi mobili utilizzando la visualizzazione radiale nel rapporto [!UICONTROL Tipi di dispositivi]. |
| [!DNL Target] | Il [servizio ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) unisce ID e dati dei visitatori in un singolo profilo actionable da utilizzare nelle applicazioni. La casella di controllo [!UICONTROL Pubblica in Experience Cloud], selezionabile in fase di creazione del segmento in Adobe Analytics, permette di rendere disponibile il segmento nella libreria di tipi di pubblico personalizzata di Adobe Target. Un segmento creato in [!DNL Analytics] o [!DNL Audience Manager] può essere utilizzato per attività in [!DNL Target]. Ad esempio, puoi creare campagne sulla base delle metriche di conversione di [!DNL Analytics] e sui segmenti di pubblico creati in [!DNL Analytics]. |
| [!DNL Audience Manager] | I tipi di pubblico condivisi sono disponibili nella segmentazione di [!DNL Audience Manager]. Tutti i tipi di pubblico di Experience Cloud sono disponibili in formato nativo in [!DNL Audience Manager], che fornisce:<ul><li>Automazione incorporata riguardo il modo in cui vengono condivisi e utilizzati nei flussi di lavoro delle applicazioni</li><li>Destinazioni esterne</li><li>Modellazione lookalike</li></ul> |
| Campaign | <ul><li>Importa i tipi di pubblico condivisi da diverse applicazioni Adobe Experience Cloud in Adobe Campaign.</li><li>Esporta gli elenchi dei destinatari sotto forma di tipi di pubblico condivisi. I tipi di pubblico condivisi possono essere utilizzati nelle diverse applicazioni Adobe Experience Cloud che utilizzi.</li></ul> |
| Advertising Cloud | Utilizza il pubblico come target. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Quando un visitatore diventa idoneo per il pubblico condiviso da Analytics, trascorrono 4-8 ore prima che tale informazione sia utilizzabile in [!DNL Target], Ad Cloud e Campaign Standard.

## Elementi dell&#39;interfaccia libreria di tipi di pubblico {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL Persone]** > **[!UICONTROL Libreria pubblico]**

![Aggiungere un pubblico nella libreria Pubblico](assets/audience_library.png)


| Elemento | Descrizione |
|--- |--- |
| Nuovo | [Creazione di un pubblico](create.md). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | La persona che ha creato il segmento di pubblico. |
| Origine | Identifica la posizione in cui è stato creato il pubblico.<ul><li>**Analytics:** segmento creato in Adobe Analytics e pubblicato in Experience Cloud.</li><li>**Experience Cloud:** un nuovo pubblico [creato in Experience Cloud Audiences](create.md).</li><li>**Audience Manager:** i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in Experience Cloud Audiences.</li></ul> |
| Dimensione attuali | Dimensione attuale del pubblico. |
| Attivo | Lo stato attivo del segmento. |

{style="table-layout:auto"}

## Tipi di pubblico di Publish da Adobe Analytics

Per ulteriori informazioni, consulta [Segmenti di Publish all&#39;Experience Cloud](https://experienceleague.adobe.com/it/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) nella documentazione di Adobe Analytics.
