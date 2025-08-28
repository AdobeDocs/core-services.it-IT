---
description: Scopri come configurare le sottoscrizioni di attributi cliente per Analytics e Target e attivare un’origine dati.
solution: Experience Cloud
title: Configurare gli abbonamenti
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: fc60b49af0839769fdd8d18fd61863c8b28bbd57
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 65%

---

# Configurare le sottoscrizioni e attivare l’origine dati

Le sottoscrizioni consentono il flusso di dati degli attributi del cliente tra Experience Cloud e le applicazioni ([!DNL Analytics] e [!DNL Target]).

Ad esempio, una sottoscrizione Adobe Analytics abilita i dati degli attributi nei rapporti. Se utilizzi Adobe Target, puoi caricare gli attributi del cliente per il targeting e la segmentazione.

**Per configurare le sottoscrizioni e attivare l&#39;origine dati**

1. Individuare l&#39;origine attributo del cliente per la modifica:

   In [!DNL Experience Cloud], fare clic su **[!UICONTROL App]** ![menu](assets/menu-icon.png) > **[!DNL Customer Attributes]**.

1. In [!UICONTROL Modifica attributo cliente Source], fare clic su **[!UICONTROL Caricamento file]**.

1. Fare clic su **[!UICONTROL Configura sottoscrizioni]**.

   ![Configurazione delle sottoscrizioni in Experience Cloud](assets/configure-subscriptions.png)

1. Per attivare l&#39;origine attributo del cliente, fare clic su **[!UICONTROL Attivo]**, quindi su **[!UICONTROL Salva]**.

1. Per configurare una sottoscrizione a [!DNL Analytics] o [!DNL Target], fare clic su **[!UICONTROL Configura]**.

   L&#39;esempio seguente mostra una sottoscrizione [!DNL Target]:

   ![Risultato del passaggio](assets/subscription-target.png)

   | Elemento | Descrizione |
   |--- |--- |
   | Soluzione | **Adobe Analytics**<br> Seleziona [!DNL Analytics], specifica le suite di rapporti in cui vuoi ricevere i dati degli attributi e gli attributi da includere.<br>**Adobe Target**<br> Puoi caricare gli attributi del cliente per il targeting e la segmentazione. Questa funzionalità è utile se vuoi destinare un test sulla base di dati di attributi o se vuoi rendere disponibili i dati per la segmentazione in Analytics.<br>I dati degli attributi dei clienti caricati per un visitatore sono disponibili all&#39;accesso in **[!DNL Target]** > **Audiences**.<br>Sono supportate più sorgenti di dati. Quando imposti gli ID cliente sul tuo sito Web, verifica che almeno uno degli alias sia iscritto a [!DNL Target]. |
   | Suite di rapporti (Adobe Analytics) | Le suite di rapporti da Analytics.<br>Non puoi aggiungere più di 10 suite di rapporti alle sottoscrizioni di Analytics in un&#39;unica origine attributo. Quando scegli quali suite di rapporti includere, prendi in considerazione i seguenti suggerimenti:<ul><li>Scegli suite di rapporti con un set comune di clienti autenticati. Se i clienti autenticati in una suite di rapporti non si sovrappongono ai clienti autenticati in un&#39;altra suite di rapporti, separa queste suite di rapporti in sorgenti di attributi diverse.</li><li>Se possibile, le suite di rapporti incluse in un&#39;origine di attributi devono avere un volume di traffico simile.</li></ul><br>Se hai più di 10 suite di rapporti con un set di clienti autenticati simile, puoi configurare altre origini attributi cliente, ciascuna con al massimo 10 suite di rapporti. |
   | Attributi da includere (Analytics e [!DNL Target]) | Attributi che desideri inviare all’applicazione. <br>Quando configuri le sottoscrizioni e selezioni gli attributi, si applicano i seguenti limiti _per suite di rapporti,_ a seconda delle soluzioni che possiedi:<ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totali</li><li>Premium: 200 per suite di report</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Nota:** quando esegui l&#39;aggiornamento ad Analytics Premium, si verifica un ritardo di 24 ore prima che gli attributi aggiuntivi siano disponibili. Durante questo lasso di tempo potresti ricevere un errore di tipo Limite di attributi massimo per abbonamento. |

1. Fai clic su **[!UICONTROL Salva]**.
