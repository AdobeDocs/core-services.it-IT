---
description: Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.
keywords: customer attributes;core services
seo-description: Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.
seo-title: Considerazioni sulla privacy - Attributi del cliente
solution: Experience Cloud
title: Considerazioni sulla privacy - Attributi del cliente
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Considerazioni sulla privacy - Attributi del cliente

Considerazioni e pratiche ottimali sui dati personali caricati e utilizzati in Adobe Experience Cloud.


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* Nome e cognome
* Indirizzo abitazione o altro indirizzo fisico
* Indirizzo e-mail
* Numero di telefono
* Numero previdenza sociale
* Altro identificatore che consente di contattare fisicamente o online un individuo. (varia in base alla posizione. Verifica e rispetta le leggi e i regolamenti locali relativi alla privacy e i dati PII per tutti i luoghi in cui si svolge la propria attività).


Adobe fornisce strumenti che consentono agli inserzionisti di raccogliere informazioni comportamentali sui consumatori che visitano i loro siti o utilizzano le loro applicazioni. Adobe fornisce inoltre strumenti che consentono agli inserzionisti di migliorare tali informazioni con record cliente offline o esterni che l&#39;inserzionista potrebbe avere all&#39;interno di altri sistemi di gestione delle informazioni.

Uno dei motivi comuni per cui gli inserzionisti fanno ciò è migliorare le informazioni disponibili quando prendono decisioni di marketing e pubblicità appropriate per il consumatore. Adobe Analytics e Target consentono agli inserzionisti di caricare personalmente dati personali (personally identifiable information, PII) come indirizzi e-mail solo dopo aver aggiunto l&#39;hash per non renderne più possibile l&#39;utilizzo per contattare la persona. Le informazioni con hash possono essere ancora utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe, come ad esempio record medici, informazioni finanziarie e sui minori.

Adobe è consapevole del fatto che questi tipi di decisioni relative a marketing e pubblicità possono avere implicazioni sulla privacy dei consumatori, ed è per questo che Adobe ha introdotto controlli sulla privacy per aiutare gli inserzionisti a soddisfare le aspettative dei consumatori. Adobe consiglia agli inserzionisti di considerare attentamente le informazioni da utilizzare a fini di marketing e in quali circostanze l&#39;inserzionista dispone dell&#39;autorizzazione per utilizzare tali informazioni.

**Procedure consigliate**

Quando carichi i dati PII in Adobe Analytics o Adobe Target, Adobe consiglia di immettere gli hash prima di caricarli in Adobe. Le informazioni con hash possono essere ancora utilizzate per analisi e per scopi di marketing. Adobe vieta agli inserzionisti di inviare dati personali ad Adobe Analytics e Adobe Target, come ad esempio record medici, informazioni finanziarie e sui minori.

Adobe consiglia agli inserzionisti di considerare attentamente le informazioni da utilizzare a fini di marketing e in quali circostanze l&#39;inserzionista dispone dell&#39;autorizzazione per utilizzare tali informazioni.

Poiché la normativa sulla privacy del consumatore è in continuo mutamento, Adobe consiglia agli inserzionisti di rispettare tre principi comuni:

1. Fai ciò che dici (nell&#39;informativa sulla privacy).
1. Dite quello che fate (nell&#39;informativa sulla privacy).
1. Non sorprendete i consumatori.

Tenendo presenti queste aspettative, Adobe consiglia che quando un inserzionista associa le attività di ricerca ai dati PII, l&#39;inserzionista presenti avvisi o personalizzazioni indicando che il consumatore è autenticato. Un esempio è includere un saluto all’interno dell’intestazione del sito Web. Adobe consiglia inoltre agli inserzionisti di descrivere nell&#39;informativa sulla privacy il tipo di informazioni di esplorazione associate ai dati PII e in quali circostanze le informazioni di navigazione sono associate ai dati PII. Infine, Adobe consiglia vivamente agli inserzionisti di rivedere le opzioni di rifiuto che forniscono ai consumatori per capire se e come possono utilizzare le informazioni di profilo non autenticate dopo l&#39;opzione di rifiuto.

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
