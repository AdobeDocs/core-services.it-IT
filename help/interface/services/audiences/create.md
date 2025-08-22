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
source-git-commit: c98084e3960e40ae28e55050ce0727abce94ba0c
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 65%

---

# Creazione di un pubblico

In [!UICONTROL Libreria tipi di pubblico] è possibile utilizzare le regole degli attributi per creare un pubblico e definire un pubblico composito per la condivisione nelle applicazioni Experience Cloud.

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

**Creare un’audience**

1. Fai clic su [!DNL Experience Cloud] app (![Icona app](assets/apps-icon.png)), quindi fai clic su **[!UICONTROL Persone]** > **[!UICONTROL Libreria pubblico].**

1. Nella pagina [!UICONTROL Tipi di pubblico], fai clic su **[!UICONTROL Nuovo]**. ![Nuovo pubblico](assets/add_icon_small.png)

   ![Creazione di un pubblico](assets/audience_create_new.png)

1. Nella pagina [!UICONTROL Crea nuovo pubblico], completa i campi **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.
1. In [!UICONTROL Regole], seleziona una suite di rapporti di riferimento, quindi un&#39;origine attributo:

   * **[!UICONTROL Dati Real-Time Analytics:]** (o dati non elaborati) Si tratta di dati attributo derivati da richieste di immagini Real-Time Analytics. Include eVar ed eventi. Quando utilizzi questa origine di attributi, devi selezionare una suite di rapporti e definire la dimensione o l’evento da includere. Questa selezione di suite di rapporti fornisce la struttura delle variabili utilizzata dalla suite di rapporti.

   >[!NOTE]
   >
   >A causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud.

   * **[!UICONTROL Dati attributo Experience Cloud:]** derivati da [!DNL Experience Cloud] origini. Ad esempio, potrebbe trattarsi dei dati dei segmenti di pubblico che hai creato in [!DNL Analytics] o dei dati di [!DNL Audience Manager].

1. Definisci le regole del pubblico, quindi fai clic su **[!UICONTROL Salva].**

**Esempio: definire le regole per il pubblico composito**

>[!NOTE]
>
>Quando definisci le regole per i tipi di pubblico, devi conoscere le variabili di implementazione.

In [!UICONTROL Regole], definisci le selezioni dell’attributo *`Home & Garden`*:

* **[!UICONTROL Origine attributo:]** dati grezzi di Analytics
* **[!UICONTROL Suite di rapporti:]** Suite di rapporti 31
* Dimensione = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL È uguale a]** > **[!UICONTROL Home &amp; Garden (Casa e giardino)]**

![Selezioni di attributi nella libreria Pubblico](assets/home_garden.png)

*Chrome &amp; Safari Visitors (visitatori di Chrome e Safari)* è un segmento di pubblico condiviso da Analytics:

* **[!UICONTROL Origine attributo:]** Experience Cloud
* **[!UICONTROL Dimensione:]** Chrome &amp; Safari Visitors (visitatori di Chrome e Safari)

![Visitatori Chrome e Safari](assets/chrome_safari.png)

Per un confronto, potresti aggiungere una regola *OR* per visualizzare tutti i visitatori in una sezione del sito, ad esempio Patio e mobili.

![Regola OR per un pubblico](assets/audiences_rule_patio.png)

La regola risultante è un pubblico definito composto dagli utenti di Chrome e Safari che hanno visitato Home &amp; Garden (Casa e giardino). Il segmento Patio &amp; Furniture (Patio e mobili) fornisce informazioni approfondite su tutti i visitatori che visitano quella sezione del sito.

![Pubblico definito in Experience Cloud](assets/defined_audience.png)

* **Stima storica:** (cerchio punteggiato) rappresenta le regole create basandosi sui dati di [!DNL Analytics].
* **Pubblico effettivo:** (cerchio continuo) qualsiasi regola creata con 30 giorni di dati provenienti da Audience Manager. Quando i dati di Audience Manager raggiungono i 30 giorni, la linea diventa continua e rappresenta i numeri effettivi.

Al termine della raccolta dei dati per il periodo specificato, i cerchi si combinano per mostrare un pubblico definito.

Una volta salvato, il pubblico è disponibile per altre applicazioni Experience Cloud. Ad esempio, puoi includere un pubblico condiviso in una [attività](https://experienceleague.adobe.com/en/docs/target/using/activities/activities) di Adobe Target.
