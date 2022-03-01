---
description: Scopri la funzione Ricerca unificata per alcune applicazioni in Experience Cloud.
solution: Experience Cloud
title: 'Experience Cloud Unified Search '
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
source-git-commit: 7e7129fbf0c3407dac3a91b645bddc878b1a7d45
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 1%

---


# [!UICONTROL Ricerca unificata] per oggetti ed entità {#globally-search}

La [!UICONTROL Ricerca unificata] la ricerca consente di trovare oggetti o entità aziendali ricercabili in un’esperienza semplice, coerente e semplice. Questa ricerca superfici anche gli oggetti a cui è stato effettuato l’accesso di recente.

![Ricerca globale di oggetti ed entità](assets/platform-search.png)

## Accessing Unified Search

La funzione Ricerca unificata è disponibile in ogni pagina dell’intestazione dell’Experience Cloud nella parte superiore della pagina. You can also use the keyboard shortcut `command /` or `ctrl /` to access the search.

Questa funzione è disponibile solo per i prodotti supportati, che al momento sono:

* Experience Platform (AEP)
* Journey Optimizer (AJO)

Poiché è stato indicizzato più contenuto, questa funzione viene aggiunta alle applicazioni pertinenti.

## Oggetti e campi ricercati

Mentre si digita, i primi risultati corrispondenti degli Oggetti a cui si ha accesso per la visualizzazione.

I nostri algoritmi mostrano prima i record più rilevanti. L’ordine dei risultati dipende da diversi fattori, quali:

Le tue autorizzazioni di funzionalità e oggetto Corrispondenza percentuale Se esiste una corrispondenza esatta

![Ricerca unificata in Experience Cloud](assets/unified-search-results.png)

Gli oggetti business ricercabili includono:

* Segmenti (nome, descrizione, ID)
* Schema (Nome, Descrizione, ID)
* Set di dati (nome, descrizione, ID)
* Sources (Name, Description, ID)
* Destinazioni (Nome, Descrizione, ID)
* Query (Nome, Descrizione, ID)
* Messaggi (nome, descrizione, ID)
* Offerte (Nome, Descrizione, ID)
* Componenti (Nome, Descrizione, ID)
* Percorsi (Nome, Descrizione, ID)

Se una parola chiave corrisponde a una pagina di navigazione, puoi ottenere un collegamento di accesso rapido ai set di dati di esempio della pagina di navigazione. The top results section shows the Top 30 results.

You also find the help articles from Experience League and Communities. Sono supportate le query per lingue naturali.

For example, _How to create a schema_ produces results from Experience League under _[!UICONTROL Learning]_:

![Aiuto per la ricerca unificata nell’Experience Cloud](assets/unified-search-learning.png)

Gli algoritmi di ricerca visualizzano per primi i record più rilevanti. L’ordine dei risultati dipende da diversi fattori, quali:

* Autorizzazioni utente per accedere agli oggetti
* Percentuale corrispondente
* Corrispondenza esatta
* La _[!UICONTROL Risultati principali]_ La sezione mostra i primi 30 risultati.

Per perfezionare la ricerca, fai clic su una delle seguenti opzioni:

* **[!UICONTROL Tutto l&#39;apprendimento]**: Apre la ricerca in Experience League.
* **[!UICONTROL Mostra tutto...]**: Consente di perfezionare e filtrare ulteriormente i risultati.

## Funzioni di ricerca unificata

The following features are available in Unified Search.

| Funzione | Descrizione |
| ------- | ------- |
| Supporto linguistico globale | La ricerca globale comprende le query e produce risultati per tedesco, spagnolo, francese, italiano, giapponese, coreano, portoghese e cinese. |
| Tolleranza Typo | La ricerca unificata fornisce una forte tolleranza di errore utilizzando gli algoritmi avanzati. Questi algoritmi calcolano le modifiche e forniscono i risultati appropriati. |
| Evidenziazione | La risposta alla ricerca evidenzia la parola chiave corrispondente dalla query di ricerca in modo da poter trovare facilmente la sezione e le parole corrispondenti alla query. L’evidenziazione funziona anche per le parole errate. |
| Frammenti | Nella risposta alla ricerca, puoi vedere uno snippet del risultato. Gli snippet restituiscono le parole corrispondenti e alcuni contenuti intorno alle parole chiave corrispondenti. |
| Interrompi parole | Alcune parole comunemente utilizzate in inglese sono definite come _interrompi parole_. Se nella query di ricerca sono incluse le parole di arresto, viene loro assegnato meno peso. <br>Le parole di interruzione includono: _a, an, e, sono, come, at, be, ma, per, per, se, in, in, è, è, no, non, di, on, o, tale, il, loro, allora, là, questi, loro, questo, a, era, volontà, con_. <br>Le parole di arresto non sono supportate in altre lingue globali. |
| Query di lingua naturale | Quando cerchi un articolo della guida o una discussione da Experience League Communities, puoi digitare la domanda utilizzando il linguaggio naturale e ottenere la risposta. Example search: &quot;How do I create a schema?&quot; |
| Ricerca esatta tra virgolette | È possibile eseguire una ricerca esatta utilizzando le virgolette nella query. Non viene eseguita alcuna correzione dell’errore ortografico sulle query di correzione. Ad esempio: &quot;Percorso Luma 2022&quot;. |
| Filtri | Puoi applicare filtri come _Tipo di oggetto_ e altri filtri specifici per gli oggetti nella finestra a comparsa dei risultati della ricerca completa. Quando premi Invio dopo aver legato la query di ricerca, viene visualizzata una finestra a comparsa a pagina intera che include i filtri. |

{style=&quot;table-layout:auto&quot;}

## Non riesce a trovarla?

Prova questi suggerimenti:

* Immettere un termine di ricerca più specifico
* Controllare l’ortografia
* Prova a scrivere il termine di ricerca completo
* Assicurati di disporre delle autorizzazioni per gli oggetti ricercati











