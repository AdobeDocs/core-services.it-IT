---
description: Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.
keywords: attributi del cliente;servizi principali
seo-description: Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.
seo-title: Considerazioni sulla privacy - Attributi del cliente
solution: Experience Cloud
title: Considerazioni sulla privacy - Attributi del cliente
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Considerazioni sulla privacy - Attributi del cliente

Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* Nome e cognome
* Indirizzo abitazione o indirizzo fisico
* Indirizzo e-mail
* Numero di telefono
* Codice fiscale
* Altri dati identificativi che consentono di contattare fisicamente oppure online un individuo (varia a seconda del luogo. Verifica e rispetta le leggi e i regolamenti locali relativi alla privacy e i dati PII per tutti i luoghi in cui si svolge la propria attività).


Adobe fornisce degli strumenti che consentono agli inserzionisti di ottenere informazioni comportamentali sui consumatori che visitano i loro siti o utilizzano le loro applicazioni. Adobe fornisce inoltre degli strumenti che consentono agli inserzionisti di migliorare tali informazioni con record offline o di clienti esterni di cui gli inserzionisti possono disporre all'interno dei sistemi di gestione di altre informazioni.

Una delle principali motivazioni per cui un inserzionista utilizza questi strumenti è il miglioramento delle informazioni disponibili quando deve fare delle scelte appropriate per il cliente in ambito pubblicitario e marketing. Adobe Analytics e Target consentono agli inserzionisti di caricare personalmente dati personali (personally identifiable information, PII) come indirizzi e-mail solo dopo aver aggiunto l'hash per non renderne più possibile l'utilizzo per contattare la persona. Le informazioni con hash possono essere utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe, come ad esempio record medici, informazioni finanziarie e sui minori.

Adobe sa che questi tipi di decisioni in ambito marketing e pubblicitario possono avere delle implicazioni in merito alla privacy del consumatore, ed è il motivo per cui Adobe ha instaurato dei controlli sulla privacy per aiutare gli inserzionisti a soddisfare le aspettative dei consumatori. Adobe consiglia agli inserzionisti di considerare attentamente le informazioni da ritenersi appropriate per l'utilizzo a fini di marketing e le situazioni in cui l'inserzionista dispone dell'autorizzazione per utilizzare tali informazioni.

**Procedure consigliate**

Quando carichi i dati PII in Adobe Analytics o Target, Adobe consiglia di immettere gli hash prima di effettuare il caricamento in Adobe. Le informazioni con hash possono essere utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe Analytics e Target, come ad esempio record medici, informazioni finanziarie e sui minori.

Adobe consiglia agli inserzionisti di considerare attentamente le informazioni da ritenersi appropriate per l'utilizzo a fini di marketing e le situazioni in cui l'inserzionista dispone dell'autorizzazione per utilizzare tali informazioni.

Poiché la legge sulla privacy del consumatore è in continuo mutamento, Adobe consiglia agli inserzionisti di rispettare tre principi comuni:

1. Metti in pratica ciò che affermi (in relazione all'Informativa sulla privacy).
1. Spiega chiaramente ciò che fai (in relazione all'Informativa sulla privacy).
1. Non cogliere di sorpresa i consumatori.

Tenendo questi principi a mente, Adobe consiglia agli inserzionisti, al momento dell'associazione delle attività di esplorazione ai dati PII, di fornire avvisi o personalizzazioni indicando che il consumatore è autenticato. Un esempio può essere includere un saluto nell'intestazione del sito Web. Adobe consiglia inoltre agli inserzionisti di descrivere nell'informativa sulla privacy il tipo di informazioni di esplorazione associate ai dati PII e in quali circostanze le informazioni di esplorazioni vengono associate ai PII. Infine, Adobe consiglia vivamente agli inserzionisti di rivedere le scelte delle rinunce che forniscono ai consumatori per capire se e come possono rinunciare a utilizzare informazioni del Attributi del cliente non autenticate.

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to https://marketing.adobe.com/resources/help/en_US/mcloud/t-publish-audience-segment.html, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/ </p> -->
