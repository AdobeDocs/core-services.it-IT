---
description: Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.
keywords: servizi di base
seo-description: Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.
seo-title: Pubblicazione di un segmento di pubblico di Analytics
solution: Experience Cloud
title: Pubblicazione di un segmento di pubblico di Analytics
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: ht
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# Pubblicazione di un segmento di pubblico di Analytics

Pubblica un segmento di pubblico, o audience, di Analytics in Experience Cloud e Adobe Target, per attività di marketing relative all’audience.

1. In Analytics, [genera un segmento](https://marketing.adobe.com/resources/help/en_US/analytics/segment/?f=seg_build).
1. In Segment Builder, abilita l’opzione **[!UICONTROL Make this an Experience Cloud audience]** (Crea pubblico di Experience Cloud).

   ![](assets/ec_audience_example.png)

   | Elemento | Descrizione |
   |--- |---|
   | Make this an Experience Cloud audience (Crea pubblico di Experience Cloud), per &lt;nome suite di rapporti&gt; | Pubblica questo segmento in Experience Cloud. Puoi utilizzare il pubblico per attività di marketing in Adobe Target e la segmentazione in Audience Manager.<br>I campi Titolo e Descrizione sono obbligatori per pubblicare il segmento.<br>Quando questa opzione viene attivata, vengono condivisi il titolo e la definizione del segmento di pubblico, ma non i dati effettivi. Quando quel pubblico viene associato a un&#39;attività in Target, Analytics inizia a inviare ID per i visitatori idonei per quel pubblico Experience Cloud e Target. A questo punto, il nome del pubblico e i dati corrispondenti iniziano a essere visualizzati sulla pagina di Experience Cloud Audiences.<br>Il pubblico condiviso con Experience Cloud da Analytics non può superare i 20 milioni di membri.<br>A causa della memorizzazione nella cache, sono necessarie 12 ore prima che l’eliminazione delle suite di rapporti di Analytics possa essere visibile in Experience Cloud.<br>In Analytics puoi modificare o eliminare un segmento pubblicato. Se il segmento è in uso, quando modifichi un segmento compare un messaggio di avviso. Non puoi eliminare un segmento modificato in uso in Adobe Target.<br>Quando un visitatore diventa idoneo per la condivisione del pubblico da Analytics, trascorrono 24-48 ore prima che tale informazione sia fruibile in Target, Advertising Cloud e Campaign.<br>**Privacy dei dati**<br>I tipi di pubblico non vengono filtrati sulla base dello stato di autenticazione di un visitatore. Se un visitatore può navigare nel sito come utente autenticato o non autenticato, le azioni che si verificano per un visitatore non autenticato possono comunque determinare l&#39;inclusione del visitatore nel pubblico. Controlla la [Panoramica sulla privacy in Analytics](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview) per comprendere tutte le implicazioni in materia di privacy derivanti dalla condivisione dei tipi di pubblico. |
   | Select the window for audience creation (Seleziona la finestra per la creazione del pubblico) | Nota che si tratta di una finestra temporale **mobile**, non fissa. |

1. Fai clic su **[!UICONTROL Salva]**.
1. Accedi a [!DNL Adobe Target], quindi fai clic su [!UICONTROL Audiences].
1. Nella pagina [!UICONTROL Audiences], individua il pubblico ottenuto da Experience Cloud.

   Questi tipi di pubblico sono disponibili per l’utilizzo nelle attività.
