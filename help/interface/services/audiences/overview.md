---
title: '[!DNL Audience Library]'
description: Scopri come gestire la conversione dei dati dei visitatori in segmentazione del pubblico in CX Enterprise [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
TQID: https://experienceleague.adobe.com/QEAfCWPNI-JhDw-HjZwBGv0TlqyctIqSwz8eVQqS6Gg
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 745
ht-degree: 44%

---

# Pubblico CX Enterprise

[!DNL Audience Library] visualizza il pubblico in CX Enterprise. I tipi di pubblico sono raccolte di visitatori (un elenco di ID [!DNL CX Enterprise]). Puoi gestire la trasformazione dei dati dei visitatori in segmentazione del pubblico. La creazione e la gestione dei tipi di pubblico sono simili alla creazione e all’utilizzo dei segmenti. Puoi anche condividere il segmento di pubblico con i prodotti e i servizi di [!DNL CX Enterprise].

![Tipi di pubblico di CX Enterprise](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create in [!DNL CX Enterprise]
* [!DNL Analytics] segmenti pubblicati in [!DNL CX Enterprise]
* [!DNL Audience Manager]

**Tipi di pubblico in tempo reale o basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per casi d’uso con targeting in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics a Audience Manager non sono accessibili per il targeting in tempo reale. Il sistema valuta i tipi di pubblico in due modi:

* I tipi di pubblico storici di Analytics vengono valutati ogni quattro ore. Il tempo totale di elaborazione e condivisione può richiedere fino a otto ore. I tipi di pubblico storici includono sempre i visitatori di ritorno.
* I tipi di pubblico in tempo reale provengono dai tipi di pubblico di CX Enterprise e sono valutati in tempo reale.

## Utilizzo dei tipi di pubblico da parte delle applicazioni

La tabella seguente descrive come i tipi di pubblico vengono utilizzati nelle applicazioni CX Enterprise:

| Soluzione | Descrizione |
| --- | --- |
| Pubblico CX Enterprise | Crea, gestisci e condividi tipi di pubblico in modo nativo mediante la Libreria tipi di pubblico. Puoi eseguire le seguenti operazioni:<ul><li>Utilizza il pubblico in tempo reale utilizzando gli attributi di analisi non elaborati.</li><li>Combina i tipi di pubblico per creare tipi di pubblico compositi, unendo dati storici e in tempo reale.</li><li>Visualizzare graficamente le dimensioni stimate dei tipi di pubblico.</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consulta: [Opzioni di creazione dei tipi di pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=it). |
| Analytics | Nella segmentazione, puoi creare un segmento, combinarlo con una suite di rapporti e quindi pubblicare il segmento in CX Enterprise. Quando si pubblica un segmento, questo viene visualizzato nella pagina [!DNL Audience Library] di CX Enterprise. Per informazioni dettagliate, vedere [Pubblicare segmenti in CX Enterprise](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html) nella Guida di [!DNL Analytics]. Il pubblico è inoltre disponibile come pubblico di destinazione per un&#39;esperienza di campagna in [!DNL Adobe Target] e in [!DNL Audience Manager]. Dopo aver condiviso un pubblico da [!DNL Adobe Analytics] e averlo selezionato per l&#39;utilizzo in una campagna attiva, i profili visitatore che soddisfano i criteri di definizione del segmento per gli ultimi 90 giorni vengono inviati a [!UICONTROL Audience Services]. Il limite per i tipi di pubblico condivisi è stato aumentato a 75. Il pubblico condiviso con CX Enterprise da [!DNL Analytics] non può superare i 20 milioni di membri univoci. Inoltre, a causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in CX Enterprise. |
| Mobile Services | Analizzare il traffico mobile utilizzando la visualizzazione sunburst nel rapporto [!UICONTROL Device Types]. |
| [!DNL Target] | Il [servizio ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) unisce ID e dati dei visitatori in un singolo profilo actionable da utilizzare nelle applicazioni. La casella di controllo [!UICONTROL Publish to CX Enterprise] nel processo di creazione dei segmenti in Adobe Analytics consente di rendere disponibile il segmento nella libreria dei tipi di pubblico personalizzati di Adobe Target. Un segmento creato in [!DNL Analytics] o [!DNL Audience Manager] può essere utilizzato per attività in [!DNL Target]. Ad esempio, puoi creare campagne sulla base delle metriche di conversione di [!DNL Analytics] e sui segmenti di pubblico creati in [!DNL Analytics]. |
| [!DNL Audience Manager] | I tipi di pubblico condivisi sono disponibili nella segmentazione di [!DNL Audience Manager]. Tutti i tipi di pubblico di CX Enterprise sono disponibili in modalità nativa in [!DNL Audience Manager], che fornisce:<ul><li>Automazione incorporata riguardo il modo in cui vengono condivisi e utilizzati nei flussi di lavoro delle applicazioni</li><li>Destinazioni esterne</li><li>Modellazione lookalike</li></ul> |
| Campaign | <ul><li>Importare i tipi di pubblico condivisi da diverse applicazioni Adobe CX Enterprise in Adobe Campaign.</li><li>Esporta gli elenchi dei destinatari sotto forma di tipi di pubblico condivisi. Questi tipi di pubblico condivisi possono essere utilizzati nelle diverse applicazioni Adobe CX Enterprise che utilizzi.</li></ul> |
| Advertising Cloud | Utilizza il pubblico come target. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Quando un visitatore diventa idoneo per il pubblico condiviso da Analytics, trascorrono 4-8 ore prima che tale informazione sia utilizzabile in [!DNL Target], Ad Cloud e Campaign Standard.

## Elementi dell&#39;interfaccia libreria di tipi di pubblico

[!DNL CX Enterprise] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL CX Enterprise]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![Aggiungere un pubblico nella libreria Pubblico](assets/audience_library.png)


| Elemento | Descrizione |
| --- | --- |
| Nuovo | [Creazione di un pubblico](https://experienceleague.adobe.com/en/docs/core-services/interface/services/audiences/create). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | La persona che ha creato il segmento di pubblico. |
| Origine | Identifica la posizione in cui è stato creato il pubblico.<ul><li>**Analytics:** segmento creato in Adobe Analytics e quindi pubblicato in CX Enterprise.</li><li>**CX Enterprise:** Un nuovo pubblico [è stato creato in CX Enterprise Audiences](https://experienceleague.adobe.com/en/docs/core-services/interface/services/audiences/create).</li><li>**Audience Manager:** i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in CX Enterprise Audiences.</li></ul> |
| Dimensione attuali | Dimensione attuale del pubblico. |
| Attivo | Lo stato attivo del segmento. |

{style="table-layout:auto"}

## Pubblicare tipi di pubblico da Adobe Analytics

Per ulteriori informazioni, consulta [Pubblicare i segmenti in CX Enterprise](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) nella documentazione di Adobe Analytics.
