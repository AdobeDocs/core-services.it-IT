---
description: Scopri le origini di dati della soluzione e la configurazione delle sottoscrizioni. Le sottoscrizioni consentono il flusso di dati dell'attributo cliente tra Experience Cloud e le soluzioni (Analytics e Target).
keywords: attributi del cliente; servizi di base
seo-description: Scopri le origini di dati della soluzione e la configurazione delle sottoscrizioni. Le sottoscrizioni consentono il flusso di dati dell'attributo cliente tra Experience Cloud e le soluzioni (Analytics e Target).
seo-title: Configurazione delle sottoscrizioni
solution: Experience Cloud
title: Configurazione delle sottoscrizioni
uuid: f 74 a 8155-0 a 21-46 b 3-9 b 1 e -4 c 838 f 72 f 24 f
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Configurazione delle sottoscrizioni

Scopri le origini di dati della soluzione e la configurazione delle sottoscrizioni. Le sottoscrizioni consentono il flusso di dati dell&#39;attributo cliente tra Experience Cloud e le soluzioni (Analytics e Target).

Ad esempio, una sottoscrizione Adobe Analytics abilita i dati degli attributi nei report. Se usi Adobe Target, puoi caricare gli attributi del cliente per l&#39;impostazione della destinazione e la segmentazione.

**[!UICONTROL Origine attributo del cliente]** &gt; **[!UICONTROL Crea nuova origine attributo del cliente]** &gt; **[!UICONTROL Nuovo]**

![](assets/configure_subscription_page.png)

| Elemento | Descrizione |
|--- |--- |
| Soluzione | **Adobe analyticsselect**<br>Analytics, specifica le suite di rapporti a cui vuoi ricevere i dati attributo e gli attributi da includere.<br>**Adobe targetè**<br>possibile caricare gli attributi del cliente per il targeting e la segmentazione. Questa funzionalità è utile se vuoi destinare un test sulla base di dati di attributi o se vuoi rendere disponibili i dati per la segmentazione in Analytics.<br>I dati dell&#39;attributo del cliente caricato per un visitatore è disponibile all&#39;accesso, in Target &gt; Audience.<br>Sono supportate più origini di dati. Quando [imposti gli ID cliente](../core-services/core-services.md) sul tuo sito Web, verifica che almeno uno degli alias sia iscritto a Target. |
| Suite di rapporti (Analytics) | Le suite di rapporti di Analytics.<br>Non puoi aggiungere più di 10 suite di rapporti alle sottoscrizioni di Analytics in un&#39;unica origine attributo. Quando scegli quale suite di rapporti includere, prendi in considerazione i seguenti suggerimenti:<ul><li>Scegli suite di rapporti che hanno un set comune di clienti autenticati. Se i clienti autenticati in una suite di rapporti non superano i clienti autenticati in un&#39;altra suite di rapporti, separa queste suite di rapporti in diverse origini attributi.</li><li>Se possibile, le suite di rapporti incluse in un&#39;origine attributo devono avere lo stesso volume di traffico.</li></ul><br>Se hai più di 10 suite di rapporti con un set di clienti autenticati simile, puoi configurare altre origini attributi cliente, ciascuna con al massimo 10 suite di rapporti. |
| Attributi da includere (Analytics e Target) | Gli attributi che vuoi inviare alla soluzione.<br>Durante la configurazione delle sottoscrizioni e la selezione degli attributi, vengono applicate le seguenti limitazioni, in base alle soluzioni che possedete:<ul><li>Foundation: 0</li><li>Seleziona: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totali</li><li>Premium: 200 per suite di report</li><li>Target Standard: 5</li><li>Target Premium: 200</li></ul><br>**Nota:** quando esegui l&#39;aggiornamento ad Analytics Premium, si verifica un ritardo di 24 ore prima che gli attributi aggiuntivi siano disponibili. Potresti visualizzare un errore Sottoscrizione attributi max durante questo ritardo. |
