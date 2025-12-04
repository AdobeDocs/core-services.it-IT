---
title: Creare un pubblico nella libreria Pubblico
description: Scopri come utilizzare le regole per attributi per creare un pubblico condivisibile in Libreria tipi di pubblico. Scopri come configurare una regola e definire un pubblico composito.
solution: Experience Cloud
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
source-git-commit: e63dd988abba199049da2b3620eed9ebf51043d1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 62%

---

# Creazione di un pubblico

In [!UICONTROL Audience Library] è possibile utilizzare le regole degli attributi per creare un pubblico e definire un pubblico composito per la condivisione nelle applicazioni Experience Cloud.

Questo articolo ti aiuta a capire come:

* Creazione di un pubblico
* Creare una regola
* Utilizzare le regole per definire un pubblico composito

L’immagine seguente rappresenta due regole in un pubblico composito.

![Due regole in un pubblico composito](assets/audience_sharing.png)

Ogni cerchio rappresenta una regola che definisce l’iscrizione al pubblico. I visitatori che si qualificano come membri in entrambe le regole di pubblico si sovrappongono diventando il pubblico composito e definito.

>[!NOTE]
>
>Il pubblico è completamente definito al termine della raccolta dei dati per il periodo specificato.

L’esempio seguente mostra come creare le regole per un pubblico composito. Questo pubblico è composto da:

* Sezione Home &amp; Garden (Casa e giardino) derivata dai dati di pagina o dai dati di analisi non elaborati.
* Utenti Chrome e Safari derivati da un segmento [!DNL Adobe Analytics] [pubblicato](overview.md) in [!DNL Experience Cloud].

  ![Creare le regole per un pubblico composito](assets/audience_create.png)

**Creare un pubblico**

1. Fai clic su [!DNL Experience Cloud] app (![icona app](assets/apps-icon.png)), quindi fai clic su **[!UICONTROL People]** > **[!UICONTROL Audience Library].**

1. Nella pagina [!UICONTROL Audiences], fare clic su **[!UICONTROL New]**. ![Nuovo pubblico](assets/add_icon_small.png)

   ![Creazione di un pubblico](assets/audience_create_new.png)

1. Nella pagina [!UICONTROL Create New Audience], completare i campi **[!UICONTROL Title]** e **[!UICONTROL Description]**.
1. In [!UICONTROL Rules], seleziona una suite di rapporti di riferimento, quindi un&#39;origine attributo:

   * **[!UICONTROL Real-Time Analytics Data:]** (o dati non elaborati) Si tratta di dati attributo derivati da richieste di immagini Real-Time Analytics. Include eVar ed eventi. Quando utilizzi questa origine di attributi, devi selezionare una suite di rapporti e definire la dimensione o l’evento da includere. Questa selezione di suite di rapporti fornisce la struttura delle variabili utilizzata dalla suite di rapporti.

   >[!NOTE]
   >
   >A causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** dati attributo derivati da [!DNL Experience Cloud] origini. Ad esempio, potrebbe trattarsi dei dati dei segmenti di pubblico che hai creato in [!DNL Analytics] o dei dati di [!DNL Audience Manager].

1. Definisci le regole del pubblico, quindi fai clic su **[!UICONTROL Save].**

**Esempio: definire le regole per il pubblico composito**

>[!NOTE]
>
>Quando definisci le regole per i tipi di pubblico, devi conoscere le variabili di implementazione.

In [!UICONTROL Rules], definire le selezioni dell&#39;attributo *`Home & Garden`*:

* **[!UICONTROL Attribute Source:]** dati grezzi di Analytics
* Suite di rapporti **[!UICONTROL Report Suite:]** 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home & Garden]**

![Selezioni di attributi nella libreria Pubblico](assets/home_garden.png)

*Chrome &amp; Safari Visitors (visitatori di Chrome e Safari)* è un segmento di pubblico condiviso da Analytics:

* Experience Cloud **[!UICONTROL Attribute Source:]**
* **[!UICONTROL Dimension:]** visitatori di Chrome e Safari

![Visitatori Chrome e Safari](assets/chrome_safari.png)

Per un confronto, potresti aggiungere una regola *OR* per visualizzare tutti i visitatori in una sezione del sito, ad esempio Patio e mobili.

![Regola OR per un pubblico](assets/audiences_rule_patio.png)

La regola risultante è un pubblico definito composto dagli utenti di Chrome e Safari che hanno visitato Home &amp; Garden (Casa e giardino). Il segmento Patio &amp; Furniture (Patio e mobili) fornisce informazioni approfondite su tutti i visitatori che visitano quella sezione del sito.

![Pubblico definito in Experience Cloud](assets/defined_audience.png)

* **Stima storica:** (cerchio punteggiato) rappresenta le regole create basandosi sui dati di [!DNL Analytics].
* **Pubblico effettivo:** (cerchio continuo) qualsiasi regola creata con 30 giorni di dati provenienti da Audience Manager. Quando i dati di Audience Manager raggiungono i 30 giorni, la linea diventa continua e rappresenta i numeri effettivi.

Al termine della raccolta dei dati per il periodo specificato, i cerchi si combinano per mostrare un pubblico definito.

Una volta salvato, il pubblico è disponibile per altre applicazioni Experience Cloud. Ad esempio, puoi includere un pubblico condiviso in una [attività](https://experienceleague.adobe.com/en/docs/target/using/activities/activities) di Adobe Target.
