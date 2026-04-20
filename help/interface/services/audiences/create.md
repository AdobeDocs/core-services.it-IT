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
TQID: https://experienceleague.adobe.com/xXhiBeGGEVpvdjZdpL2Q9-3eDn-gN58dynb56daQcig
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a42153ba5a885509e7735e7407e38586fcabb0ad
workflow-type: tm+mt
source-wordcount: 515
ht-degree: 60%

---

# Creazione di un pubblico

In [!UICONTROL Audience Library] è possibile utilizzare le regole degli attributi per creare un pubblico e definire un pubblico composito per la condivisione nelle applicazioni CX Enterprise.

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
* Utenti Chrome e Safari derivati da un segmento [!DNL Adobe Analytics] [pubblicato](overview.md) in [!DNL CX Enterprise].

  ![Creare le regole per un pubblico composito](assets/audience_create.png)

**Creare un pubblico**

1. Fai clic su [!DNL CX Enterprise] app (![icona app](assets/apps-icon.png)), quindi fai clic su **[!UICONTROL People]** > **[!UICONTROL Audience Library].**

1. Nella pagina [!UICONTROL Audiences], fare clic su **[!UICONTROL New]**. ![Nuovo pubblico](assets/add_icon_small.png)

   ![Creazione di un pubblico](assets/audience_create_new.png)

1. Nella pagina [!UICONTROL Create New Audience], completare i campi **[!UICONTROL Title]** e **[!UICONTROL Description]**.
1. In [!UICONTROL Rules], seleziona una suite di rapporti di riferimento, quindi un&#39;origine attributo:

   * **[!UICONTROL Real-Time Analytics Data:]** (o dati non elaborati) Si tratta di dati attributo derivati da richieste di immagini Real-Time Analytics. Include eVar ed eventi. Quando utilizzi questa origine di attributi, devi selezionare una suite di rapporti e definire la dimensione o l’evento da includere. Questa selezione di suite di rapporti fornisce la struttura delle variabili utilizzata dalla suite di rapporti.

     >[!NOTE]
     >
     >A causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in CX Enterprise.

   * **[!UICONTROL CX Enterprise:]** dati attributo derivati da [!DNL CX Enterprise] origini. Ad esempio, potrebbe trattarsi dei dati dei segmenti di pubblico che hai creato in [!DNL Analytics] o dei dati di [!DNL Audience Manager].

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

* **[!UICONTROL Attribute Source:]** CX Enterprise
* **[!UICONTROL Dimension:]** visitatori di Chrome e Safari

![Visitatori Chrome e Safari](assets/chrome_safari.png)

Per un confronto, potresti aggiungere una regola *OR* per visualizzare tutti i visitatori in una sezione del sito, ad esempio Patio e mobili.

![Regola OR per un pubblico](assets/audiences_rule_patio.png)

La regola risultante è un pubblico definito composto dagli utenti di Chrome e Safari che hanno visitato Home &amp; Garden (Casa e giardino). Il segmento Patio &amp; Furniture (Patio e mobili) fornisce informazioni approfondite su tutti i visitatori che visitano quella sezione del sito.

![Pubblico definito in CX Enterprise](assets/defined_audience.png)

* **Stima storica:** (cerchio punteggiato) rappresenta le regole create basandosi sui dati di [!DNL Analytics].
* **Pubblico effettivo:** (cerchio continuo) qualsiasi regola creata con 30 giorni di dati provenienti da Audience Manager. Quando i dati di Audience Manager raggiungono i 30 giorni, la linea diventa continua e rappresenta i numeri effettivi.

Al termine della raccolta dei dati per il periodo specificato, i cerchi si combinano per mostrare un pubblico definito.

Una volta salvato, il pubblico è disponibile per altre applicazioni CX Enterprise. Ad esempio, puoi includere un pubblico condiviso in una [attività](https://experienceleague.adobe.com/it/docs/target/using/activities/activities) di Adobe Target.
