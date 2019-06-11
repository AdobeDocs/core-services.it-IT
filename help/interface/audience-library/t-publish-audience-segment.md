---
description: Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.
keywords: servizi di base
seo-description: Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.
seo-title: Pubblicazione di un segmento di pubblico di Analytics
solution: Experience Cloud
title: Pubblicazione di un segmento di pubblico di Analytics
uuid: 4201 dc 22-4 b 79-457 c-a 614-949 bba 087617
translation-type: tm+mt
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# Pubblicazione di un segmento di pubblico di Analytics

Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.

1. In Analytics, [genera un segmento](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html).
1. On the Segment Builder, enable the **[!UICONTROL Make this an Experience Cloud audience]** option.

   ![](assets/ec_audience_example.png)

   | Elemento | Descrizione |
   |--- |---|
   | Make this an Experience Cloud audience (Crea pubblico di Experience Cloud), per &lt;nome suite di rapporti&gt; | Pubblica questo segmento in Experience Cloud. Puoi utilizzare il pubblico per attività di marketing in Adobe Target e la segmentazione in Audience Manager.<br>I campi Titolo e Descrizione sono obbligatori per pubblicare il segmento.<br>Quando questa opzione viene attivata, vengono condivisi il titolo e la definizione del segmento di pubblico, ma non i dati effettivi. Quando quel pubblico viene associato a un&#39;attività in Target, Analytics inizia a inviare ID per i visitatori idonei per quel pubblico Experience Cloud e Target. A questo punto, il nome del pubblico e i dati corrispondenti iniziano a essere visualizzati sulla pagina di Experience Cloud Audiences.<br>Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri.<br>A causa della cache, sono necessarie 12 ore prima che l&#39;eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud.<br>In Analytics puoi modificare o eliminare un segmento pubblicato. Se il segmento è in uso, quando modifichi un segmento compare un messaggio di avviso. Non puoi eliminare un segmento modificato in uso in Adobe Target.<br>Una volta che un visitatore è idoneo per il pubblico condiviso da Analytics, si verifica un ritardo di 24 ore prima che le informazioni possano essere sfruttate in Target, Advertising Cloud e Campaign.<br>**I dati privacyaudiences**<br>non vengono filtrati in base allo stato di autenticazione di un visitatore. Se un visitatore può navigare nel sito come utente autenticato o non autenticato, le azioni che si verificano per un visitatore non autenticato possono comunque determinare l&#39;inclusione del visitatore nel pubblico. Consulta [Panoramica sulla privacy di Analytics](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview) per comprendere le tutte le implicazioni per la privacy relative alla condivisione del pubblico. |
   | Select the window for audience creation (Seleziona la finestra per la creazione del pubblico) | Nota che si tratta di una finestra temporale **mobile**, non fissa. |

1. Fai clic su **[!UICONTROL Salva]**.
1. Accesso [!DNL Adobe Target], fate clic [!UICONTROL su Audience].
1. Nella pagina [!UICONTROL Audiences] (Audience) individua il pubblico ottenuto da Experience Cloud.

   Queste audience sono disponibili per l&#39;uso nelle attività.
