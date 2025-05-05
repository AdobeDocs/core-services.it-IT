---
title: '[!DNL Customer Attributes]'
description: Scopri  [!DNL Customer Attributes]  in Experience Cloud. Scopri come caricare i dati degli attributi del cliente da utilizzare in Adobe Analytics e Adobe Target.
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 96%

---

# [!DNL Customer Attributes] in Experience Cloud

[!DNL Customer Attributes] in Experience Cloud consente di caricare i dati aziendali acquisiti da un database di gestione delle relazioni con i clienti (CRM). Puoi caricare i dati in un’origine dati di attributi del cliente in Experience Cloud, quindi utilizzarli in [!DNL Adobe Analytics] e [!DNL Adobe Target].

## Individua la funzione [!DNL Customer Attributes].

1. Accedere a Experience Cloud.

1. Passa a **[!DNL Experience Platform]** > **[!UICONTROL Persone]** > **[!UICONTROL Attributi del cliente]**

![Panoramica degli Attributi del cliente](assets/custom_reports.png)

## Prerequisiti per il caricamento di [!DNL Customer Attributes] {#section_BD38693AFBF34926BA28E964963B4EA0}

* **Iscrizione al gruppo:** Per caricare i dati di attributi cliente, gli utenti devono essere membri del gruppo Attributi cliente. Devi anche appartenere a un gruppo Adobe Analytics o Adobe Target.

  Per sapere se l&#39;azienda ha accesso a Attributi del cliente, l&#39;amministratore [!DNL Experience Cloud] deve effettuare l&#39;accesso a [Experience Cloud](https://experience.adobe.com). Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Prodotti]**. Se *[!DNL Customer Attributes]* viene visualizzato come uno dei [!UICONTROL Profili di prodotto], puoi iniziare.

  Gli utenti che vengono aggiunti a [!DNL Customer Attributes] troveranno la voce di menu [!UICONTROL Attributi del cliente] sul lato sinistro dell’interfaccia di Experience Cloud.

* Per Attributi del cliente è necessaria qualsiasi versione **Adobe Target** di `at.js` o la versione 5.8 di `mbox.js` o successive.

  Consulta [Come distribuire at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=it).

## Cosa sono i dati cliente Enterprise? {#section_6F34C29F11414842AA57D2B1248FA3C6}

I dati Enterprise risiedono in altri sistemi. Possono risultare complessi e diversi a seconda delle persone. Questi dati includono informazioni come appartenenze, livello di fedeltà, età, genere, prodotti posseduti, interessi e lifetime value.

L&#39;immagine seguente è un esempio di un file di dati che mostra i dati dell&#39;utente con sottoscrizione per prodotti, inclusi gli ID membro, i prodotti autorizzati, i prodotti più lanciati e così via.

![Cosa sono i dati cliente Enterprise?](assets/01_crs_usecase.png)

Dopo aver generato il file dati, puoi caricarlo nell’origine di Attributi del cliente creata in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Attributi del cliente]**.

Consulta [Caricamento dei dati degli attributi del cliente](t-crs-usecase.md) per conoscere questo flusso di lavoro.

## Esempi di Attributi del cliente in Analytics e Target {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Quando i dati si trovano in Experience Cloud, puoi personalizzarli e condividerli con soluzioni per reporting, segmentazioni, attività e campagne.

Esempio:

| Soluzione | Vantaggi e casi d&#39;uso |
|--- |--- |
| Adobe Analytics | Gli esperti di marketing e gli analisti sono pienamente consapevoli dei seguenti fatti:<ul><li>Le campagne online sono più efficaci con i tuoi clienti di livello Gold.</li><li>Quali sono i prodotti ricercati dai clienti di livello gold rispetto a clienti di livello platinum.</li><li>Se la nuova progettazione del tuo sito web sta avendo un impatto positivo sui tassi di conversione per i clienti meno recenti.</li><li>Quali sono i prodotti più ricercati nel sito dai clienti con un valore lifetime basso.</li></ul> |
| Adobe Target | I dati attributo consentono agli utenti di Adobe Target di:<ul><li>Mostrare sconti e offerte speciali ai membri del club fedeltà.</li><li>Consigliare prodotti più costosi ai clienti di lusso.</li><li>Per i clienti che già ricevono le e-mail, inserisci un&#39;offerta di upselling nello spazio normalmente riservato alle iscrizioni e-mail.</li></ul> |

{style="table-layout:auto"}
