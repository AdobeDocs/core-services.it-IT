---
description: Gestisci la trasformazione dei dati dei visitatori nella segmentazione del pubblico.
seo-description: Gestisci la trasformazione dei dati dei visitatori nella segmentazione del pubblico.
seo-title: Tipi di pubblico
solution: Experience Cloud
title: Tipi di pubblico
uuid: 92 faf 3 a 8-1375-4 e 32-905 b -74 cad 48144 d 3
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Tipi di pubblico {#topic_679810123CAA4E0CA4FA3417FB0100C7}

Un tipo di pubblico, o audience, è un insieme di visitatori (un elenco di ID visitatori). I servizi Adobe permettono di gestire la trasformazione dei dati dei visitatori in segmenti di pubblico. La creazione e la gestione dei tipi di pubblico sono simili alla creazione e all&#39;uso dei segmenti, e in più permettono di condividere i segmenti di pubblico in [!DNL Experience Cloud].

![](assets/audiences.png)

Puoi creare o derivare tipi di pubblico da diverse fonti, come ad esempio:

* Fonti nuove create nel pannello [!DNL Experience Cloud]
* Dai [!DNL Analytics] segmenti pubblicati nella variabile [!DNL Experience Cloud]
* Da [!DNL Audience Manager]

**Tipi di pubblico in tempo reale e basati sullo storico**

Tutti i tipi di pubblico, a prescindere da dove provengono, sono accessibili per l&#39;uso in tempo reale. Tuttavia, i tipi di pubblico condivisi da Analytics ad Audience Manager non sono accessibili per l&#39;analisi in tempo reale. Il sistema valuta il pubblico in due modi:

* I dati storici provengono dalle analisi e vengono valutati ogni 12 ore. Questi includono sempre i visitatori ricorrenti.
* Le audience in tempo reale sono acquisite in Experience Cloud Audiences e sono valutate in tempo reale.


## Utilizzo dei tipi di pubblico da parte delle soluzioni {#concept_01EB9345C5344597BC94A864EDD38EE1}

Nella tabella seguente è descritto l&#39;utilizzo dei tipi di pubblico nelle soluzioni Experience Cloud.

| Soluzione | Descrizione |
|--- |--- |
| Experience Cloud Audiences | Crea, gestisci e condividi i tipi di pubblico in modo nativo utilizzando l&#39; [interfaccia Libreria](../audience-library/audience-library.md) pubblico. È possibile:<ul><li>utilizzare i dati in tempo reale con gli attributi di analisi;</li><li>combinare più tipi di pubblico per creare un pubblico composito, unire dati in tempo reale e dati storici;</li><li>vedere visualizzazioni grafiche della dimensione stimata del pubblico.</li></ul><br>Per suggerimenti sul tipo di pubblico da creare, consultare: [Experience Cloud Audiences](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analytics | Durante l&#39;attività di segmentazione, puoi costruire un segmento, combinarlo con una suite di rapporti e quindi   [ pubblicarlo in Experience Cloud](../audience-library/audience-library.md). Il segmento pubblicato viene visualizzato nella pagina [Audiences](../audience-library/audience-library.md). Il tipo di pubblico è inoltre disponibile come pubblico di destinazione per un&#39;esperienza di campagna in Adobe Target e in Audience Manager.   Quando un pubblico viene condiviso da Analytics e selezionato per l&#39;utilizzo in una campagna attiva, tutti i profili visitatore che soddisfano i requisiti di definizione del segmento per i precedenti 90 giorni vengono inviati alla piattaforma dei servizi Audiences di Experience Cloud.   Importante: devi limitare il numero di tipi di pubblico condivisi da Analytics a 20 per evitare ulteriori ritardi di elaborazione. Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri unici. Inoltre, a causa della cache, sono necessarie 12 ore prima che l&#39;eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud. |
| Mobile Services | Analizza il traffico mobile utilizzando la visualizzazione sunburst in Tipi [di dispositivi](https://marketing.adobe.com/resources/help/en_US/mobile/?f=reports_devices). |
| Target | Il [servizio ID](https://marketing.adobe.com/resources/help/en_US/mcvid/) unisce gli ID visitatore e i dati in un unico profilo utilizzabile tra le varie soluzioni. La [casella di controllo Pubblica in Experience Cloud](../audience-library/audience-library.md) durante il processo di creazione del segmento in Adobe Analytics consente di rendere il segmento disponibile nella libreria audience personalizzata di Adobe Target. Puoi utilizzare un segmento creato in Analytics o Audience Manager per attività in Target.  Ad esempio, puoi creare campagne sulla base delle metriche di conversione di Analytics e sui segmenti di pubblico creati in Analytics. |
| Audience Manager | I tipi di pubblico condivisi sono disponibili nella segmentazione di Audience Manager. Tutti i tipi di pubblico di Experience Cloud sono disponibili in formato nativo in Audience Manager, che fornisce:<ul><li>Automazione incorporata per la modalità di condivisione e consumo nei flussi di lavoro della soluzione</li><li>Destinazioni fuori sede</li><li>Modellazione simile</li></ul> |
| Campaign | <ul><li>importare i tipi di pubblico condivisi da diverse soluzioni Adobe Experience Cloud in Adobe Campaign;</li><li>esportare gli elenchi dei destinatari sotto forma di tipi di pubblico condivisi. I tipi di pubblico condivisi possono essere utilizzati nelle varie soluzioni Adobe Experience Cloud normalmente utilizzate.</li></ul> |
| Media Optimizer | Utilizzo dei tipi di pubblico come destinazioni. |


>[!IMPORTANT]
>
>Una volta che un visitatore è idoneo per il pubblico condiviso da Analytics, si verifica un ritardo di 24 ore prima che le informazioni possano essere sfruttate in Target, Media Optimizer e Campaign.

## Ulteriore aiuto: domande, guida e casi di utilizzo {#section_C7F151644D8A45F7B6FC54F58845635D}


| Aiuto con | Risorsa |
|--- |--- |
| Non riesci a trovare Audiences? | Verifica di avere il provisioning. Consulta  [Guida introduttiva: abilita le soluzioni per i servizi di base](../core-services/core-services.md).<br>Fai clic [qui](https://www.adobe.com/go/audiences) per richiedere l&#39;accesso a Profili e pubblico (modulo di provisioning integrazioni). |
| Casi di utilizzo | Per ulteriore assistenza sulla soluzione da utilizzare, vai a [Opzioni di creazione pubblico](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) nella Knowledge Base. |
| Forum | Il [forum di Audiences](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) è una risorsa aggiuntiva per ricevere aiuto sui tipi di pubblico. |


## Elementi dell&#39;interfaccia libreria di tipi di pubblico {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] fornisce una libreria per la creazione e la gestione dei tipi di pubblico, con identificazione nativa e in tempo reale.

**[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Libreria Pubblico]**

![](assets/audience_library.png)

| Elemento | Descrizione |
|--- |--- |
| Nuovo | [Creazione di un pubblico](../audience-library/audience-library.md). |
| Titolo e descrizione | Intestazione della colonna per identificare e descrivere il pubblico. |
| Autore | Persona che ha creato il segmento di pubblico. |
| Origine | Consente di identificare dove è stato creato il pubblico.<ul><li>**Analytics:** Un segmento creato in reporting e analisi o analisi ad hoc [, quindi pubblicato in Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud**: un nuovo pubblico [creato in Experience Cloud Audiences](../audience-library/audience-library.md).</li><li>**Audience Manager**: i tipi di pubblico creati da Audience Manager vengono visualizzati automaticamente in Experience Cloud Audiences.</li></ul> |
| Dimensioni attuali | Dimensione corrente del pubblico. |
| Attivo | Stato attivo del segmento. |
