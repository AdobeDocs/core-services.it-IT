---
solution: Experience Cloud
type: Documentation
title: Adobe Experience Cloud Audiences
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
description: Scopri come gestire la traduzione dei dati dei visitatori in segmentazione del pubblico, con il servizio Experience Cloud Audiences.
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 100%

---

# Tipi di pubblico di Experience Cloud {#topic_679810123CAA4E0CA4FA3417FB0100C7}

I tipi di pubblico sono raccolte di visitatori (un elenco di ID visitatore). Con la funzione Libreria tipi di pubblico di Adobe puoi gestire come tradurre i dati sui visitatori in segmentazione del pubblico. La creazione e la gestione dei tipi di pubblico è simile alla creazione e all’utilizzo di segmenti. Puoi anche condividere il segmento di pubblico con i prodotti e i servizi di [!DNL Experience Cloud].

![Tipi di pubblico di Experience Cloud](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create in [!DNL Experience Cloud]
* Segmenti [!DNL Analytics] pubblicati in [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Tipi di pubblico in tempo reale o basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per l’uso in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics a Audience Manager non sono accessibili per il targeting in tempo reale. Il sistema valuta i tipi di pubblico in due modi:

* I tipi di pubblico storici di Analytics vengono valutati ogni quattro ore. Il tempo totale di elaborazione e condivisione può richiedere fino a otto ore. I tipi di pubblico storici includono sempre i visitatori di ritorno.
* I dati in tempo reale provengono dal servizio Experience Cloud Audiences e sono valutati in tempo reale.

## Utilizzo dei tipi di pubblico da parte delle applicazioni {#concept_01EB9345C5344597BC94A864EDD38EE1}

La tabella seguente descrive come vengono utilizzati i tipi di pubblico nelle applicazioni Experience Cloud:

| Soluzione | Descrizione |
|--- |--- |
| Experience Cloud Audiences | Crea, gestisci e condividi tipi di pubblico in modo nativo mediante l’interfaccia della [Libreria tipi di pubblico](audience-library.md). È possibile:<ul><li>Utilizzare tipi di pubblico in tempo reale tramite gli attributi di analisi non elaborati</li><li>Combinare tipi di pubblico per creare tipi di pubblico compositi, unendo dati storici e in tempo reale</li><li>Visualizzare graficamente le dimensioni stimate dei tipi di pubblico</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consulta: [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=it). |
| Analytics | Durante l’attività di segmentazione, puoi costruire un segmento, combinarlo con una suite di rapporti e quindi pubblicarlo in Experience Cloud. Quando si pubblica un segmento, questo viene visualizzato nella pagina [!UICONTROL Libreria tipi di pubblico] di Experience Cloud. Per informazioni dettagliate, consulta [Pubblicare segmenti in Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=it) nell’Aiuto di Analytics. Il pubblico è inoltre disponibile come pubblico di destinazione per un’esperienza di campagna in Adobe Target e in Audience Manager. Dopo aver condiviso un pubblico da Adobe Analytics e averlo selezionato per l’utilizzo in una campagna attiva, i profili visitatore che soddisfano i criteri di definizione del segmento per gli ultimi 90 giorni vengono inviati a [!UICONTROL Audience Services]. Il limite per i tipi di pubblico condivisi è stato aumentato a 75. Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri univoci. Inoltre, a causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud. |
| Mobile Services | Analizza il traffico dei dispositivi mobili utilizzando la visualizzazione radiale nel rapporto [!UICONTROL Tipi di dispositivi]. |
| [!DNL Target] | Il [servizio ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) unisce ID e dati dei visitatori in un singolo profilo actionable da utilizzare nelle applicazioni. La casella di controllo [Pubblica in Experience Cloud](audience-library.md), selezionabile in fase di creazione del segmento in Adobe Analytics, permette di rendere disponibile il segmento nella libreria di tipi di pubblico personalizzata di Adobe Target. Un segmento creato in Analytics o Audience Manager può essere utilizzato per attività in [!DNL Target]. Ad esempio, puoi creare campagne sulla base delle metriche di conversione di [!DNL Analytics] e sui segmenti di pubblico creati in [!DNL Analytics]. |
| Audience Manager | I tipi di pubblico condivisi sono disponibili nella segmentazione di Audience Manager. Tutti i tipi di pubblico di Experience Cloud sono disponibili in formato nativo in Audience Manager, che fornisce:<ul><li>Automazione incorporata riguardo il modo in cui vengono condivisi e utilizzati nei flussi di lavoro delle applicazioni</li><li>Destinazioni esterne</li><li>Modellazione lookalike</li></ul> |
| Campaign | <ul><li>Importa i tipi di pubblico condivisi da diverse applicazioni Adobe Experience Cloud in Adobe Campaign.</li><li>Esporta gli elenchi dei destinatari sotto forma di tipi di pubblico condivisi. I tipi di pubblico condivisi possono essere utilizzati nelle diverse applicazioni Adobe Experience Cloud che utilizzi.</li></ul> |
| Advertising Cloud | Utilizza il pubblico come target. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Quando un visitatore diventa idoneo per il pubblico condiviso da Analytics, trascorrono 4-8 ore prima che tale informazione sia utilizzabile in [!DNL Target], Ad Cloud e Campaign Standard.

## Ulteriore aiuto: domande, guida e casi di utilizzo {#section_C7F151644D8A45F7B6FC54F58845635D}

| Aiuto con | Risorsa |
|--- |--- |
| Non riesci a trovare Pubblico? | Verifica di avere il provisioning. Consulta [Guida introduttiva: abilitare le applicazioni per i servizi principali](core-services.md).<br>Fai clic [qui](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES) per richiedere l’accesso ai servizi per profili e tipi di pubblico (modulo di provisioning integrazioni). |
| Casi di utilizzo | Per maggiori informazioni sull’applicazione da utilizzare, consulta la sezione sulle [opzioni di creazione del pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=it) nella Knowledge Base. |
| Forum | Il [forum di Audiences](https://experienceleaguecommunities.adobe.com/t5/Adobe-Experience-Cloud-Audiences/ct-p/experience-cloud-audiences-community) è un’ulteriore risorsa utile quando si lavora sui tipi di pubblico. |

{style="table-layout:auto"}

## Elementi dell&#39;interfaccia libreria di tipi di pubblico {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL Persone]** > **[!UICONTROL Libreria pubblico]**

![Aggiungere un pubblico nella libreria Pubblico](assets/audience_library.png)

| Elemento | Descrizione |
|--- |--- |
| Nuovo | [Creazione di un pubblico](audience-library.md). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | La persona che ha creato il segmento di pubblico. |
| Origine | Identifica la posizione in cui è stato creato il pubblico.<ul><li>**Analytics:** un segmento creato in Adobe Analytics e poi [pubblicato in Experience Cloud](audience-library.md).</li><li>**Experience Cloud:** un nuovo pubblico [creato in Experience Cloud Audiences](audience-library.md).</li><li>**Audience Manager:** i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in Experience Cloud Audiences.</li></ul> |
| Dimensione attuali | Dimensione attuale del pubblico. |
| Attivo | Lo stato attivo del segmento. |

{style="table-layout:auto"}
