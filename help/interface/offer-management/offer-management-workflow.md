---
description: Scopri il flusso di lavoro di alto livello di Gestione offerte, che include la creazione di posizioni e offerte, l'inserimento di attività di offerta e la visualizzazione di rapporti.
seo-description: Scopri il flusso di lavoro di alto livello di Gestione offerte, che include la creazione di posizioni e offerte, l'inserimento di attività di offerta e la visualizzazione di rapporti.
seo-title: Flusso di lavoro di gestione delle offerte
title: Flusso di lavoro di gestione delle offerte
uuid: c95ec474-88de-4e6e-92bf-f49f3a7b32c5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2f0c2eb70313c42da9e7ac1d75429ec768dea10d

---


# Flusso di lavoro di gestione delle offerte{#offer-management-workflow}

Scopri il flusso di lavoro di alto livello di Gestione offerta, che include la creazione di posizioni e offerte, l&#39;inserimento di attività di offerta e la visualizzazione di rapporti.

## Passaggio 1 - Determinate dove nei modelli delle e-mail sono necessarie offerte personalizzate {#section_F184E589428B403EA8EB921BF230CF87}

Identificare in quali campagne e-mail si desidera inserire offerte personalizzate. Da qui, stabilite le posizioni all&#39;interno del modello e-mail per inserire queste offerte. Ad esempio, potrebbe essere utile modificare l&#39;offerta di prodotto in base al settore o alla persona del cliente, modificare il messaggio in base agli stessi criteri e variare l&#39;immagine in base alla posizione geografica del cliente.

![](assets/workflow1.png)

## Passaggio 2 - Determinare gli attributi della campagna a cui destinare e condividerli con Gestione offerte {#section_1461F1FAC0B943E5BBDED6B3B00E9D5C}

Quando create un&#39;offerta in Gestione offerta, potete impostare regole di idoneità che limitano i profili che possono ricevere determinate offerte. Queste regole di idoneità possono essere impostate in base agli attributi (o ai campi) esistenti in Adobe Campaign. Questi campi devono essere condivisi da Campaign da un utente a livello di amministratore prima di essere visualizzati nel generatore di regole di idoneità di [!UICONTROL Gestione] offerte.

Per informazioni sulla condivisione di questi attributi, consultate [Condividere gli attributi da Campaign a Offer Management](campaign.md#task_4DFA9A20D7B04E1F9AFF4774D67B6EBC).

## Passaggio 3 - Inserire i posizionamenti richiesti in Gestione  offerta {#section_71619756A86F4DB58B8200D8A1CE1B87}

Una posizione garantisce che il contenuto dell&#39;offerta corretta venga visualizzato nella posizione corretta all&#39;interno del modello e-mail. Quando aggiungete contenuto a un&#39;offerta, vi verrà chiesto di selezionare una posizione in cui visualizzare il contenuto.

Potete avere più posizioni con lo stesso posizionamento. Nell’esempio seguente, esistono due posizioni per due immagini di dimensioni diverse e una posizione singola per il testo che viene visualizzato nella parte superiore e inferiore del modello.

Dopo aver determinato i posizionamenti necessari, è possibile aggiungerli alla scheda [!UICONTROL Posizionamento] .

![](assets/workflow2.png)

## Passaggio 4 - Creare le offerte {#section_C4F9732B0596425EB0BD5AE76E4BA6EF}

Create le offerte da utilizzare nella campagna e-mail. È possibile aggiungere dati e contenuti all&#39;offerta per determinare l&#39;offerta migliore da distribuire e determinare il contenuto da visualizzare. Quando create una rappresentazione di contenuto, associatela a una delle posizioni definite in [Posizionamenti](placements.md). Dopo aver creato e inviato un&#39;offerta, questa sarà disponibile per l&#39;utilizzo in un&#39;attività di offerta.

![](assets/workflow3.png)

## Passaggio 5: create la campagna e-mail e inserite un&#39;attività di offerta {#section_6FD36404759B4C6E9FD3A65ACABB26C8}

Dopo aver creato le offerte, potete utilizzarle in una campagna e-mail. Nell&#39;editor dei contenuti, potete selezionare un blocco e inserire un&#39;attività di offerta. Un&#39;attività di offerta consente di selezionare un gruppo di offerte dall&#39;inventario delle offerte, dal quale il modulo decisionale determinerà l&#39;offerta migliore da distribuire a ogni utente.

![](assets/workflow4.png)

## Passaggio 6: preparazione e invio della campagna e-mail {#section_EDD8EA4696664130A678D7C4483DA806}

Ora, quando prepari la tua campagna e-mail, [!UICONTROL Gestione] offerte determinerà l&#39;offerta migliore da distribuire a ogni visitatore in base alla data, agli attributi del profilo e alla priorità correnti. Determina inoltre se è disponibile una rappresentazione di contenuto per il posizionamento della posizione.

Nell&#39;esempio seguente, supponete di aver configurato una campagna e-mail con un&#39;attività di offerta contenente 3 offerte (A, B, C). Potete determinare quale offerta distribuire in una delle località dell&#39;e-mail. Al momento della preparazione, [!UICONTROL Offer Management] :

1. Analizzare la data corrente, i dati del profilo di ciascun utente e la priorità.
1. Confrontate quelle informazioni con i dati sulle offerte.
1. Determinate l&#39;offerta migliore da distribuire.

![](assets/workflow5.png)

## Passaggio 7 - Visualizzare i rapporti {#section_2104BAACAE154DE29B6EEB967C46F226}

Potete visualizzare un rapporto sulle offerte ricevute e sulle relative prestazioni in un&#39;attività di offerta. Per visualizzare questo rapporto, seleziona la scheda dei rapporti nella home page di Adobe Campaign Standard.
