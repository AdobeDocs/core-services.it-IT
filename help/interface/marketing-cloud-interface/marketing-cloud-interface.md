---
description: Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.
keywords: servizi di base
seo-description: Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.
seo-title: Novità in Experience Cloud
solution: Experience Cloud
title: Novità in Experience Cloud
uuid: bc 1 b 1542-1 a 37-4 da 1-bcfd-fc 86 af 881642
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# Novità in Experience Cloud

Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.

## Agosto 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Correzioni e miglioramenti per agosto 2018.

* È stata migliorata la sincronizzazione dei commenti sulle risorse tra Creative Cloud ed Experience Cloud. (CORE-15971)
* Aggiunto flag di funzione per controllare la sincronizzazione delle risorse di Experience Cloud-Creative Cloud. (CORE-15938)
* È stata migliorata la creazione di segmenti di pubblico, compresa l’esperienza di ricerca e inserimento nell’elenco. (CORE-5833, CORE-14278)
* È stato corretto un problema di priorità elevata che bloccava la condivisione di cartelle da MAC a Creative Cloud. (CORE-16677)

## 19 luglio 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Correzioni e miglioramenti per luglio 2018.

* È stata implementata una capacità back-end per controllare la condivisione di risorse tra Marketing Cloud-AEM e Marketing Cloud-Creative Cloud. (CORE-14386)
* È stato corretto un problema che bloccava il provisioning di nuovi tenant in alcuni ambienti. (CORE-15509)
* È stato corretto un problema a causa del quale gli utenti venivano reindirizzati a [!DNL marketing.adobe.com] nel tentativo di accedere a [!DNL experiencecloud.adobe.com] tramite [!DNL http] invece di [!DNL https] (protetto). (CORE-15587)
* È stato corretto un problema che bloccava le notifiche per alcuni nuovi tenant. (CORE-15240)

## 14 giugno 2018 {#section_7ABC327992CB46B0B8E4A631B8B68899}

Correzioni e miglioramenti per giugno 2018.

* È stato abilitato un collegamento per consentire agli amministratori di accedere alle funzioni RGPD. (CORE-11731)
* Funzione Feedback beta aggiornata per limitare i tipi di file che possono essere allegati ai commenti. (CORE-10474)
* Risolto un problema con l&#39;eliminazione del pubblico da Audience Library. (CORE-12792)
* Risolto un problema che creava una schermata vuota durante l&#39;accesso ai collegamenti di Workspace utilizzando Federated ID. (CORE-11620)

## 10 maggio 2018 {#section_498AF78DA17C4720AA0F32B51493E550}

Nuove funzioni e correzioni nell’interfaccia di [!DNL Adobe Experience Cloud].

| Funzione | Descrizione |
|--- |--- |
| Nuova pagina di destinazione di amministrazione | Quando accedi in Experience Cloud ed esplori la pagina di amministrazione, è disponibile una nuova interfaccia intuitiva per consentirti di accedere rapidamente alle soluzioni Experience Cloud e ai servizi di base. |
**Correzioni**

* Corretto un errore di caricamento dell&#39;immagine dovuto un aggiornamento di Scene7. (CORE-12746)
* Aggiornamenti effettuati per ridurre il supporto per il protocollo TLS 1.0, come indicato dal PCI al fine eliminare le vulnerabilità relative alla sicurezza. (CORE-7695)

## 26 ottobre 2017 {#section_11195859B4094177A939C0561428B525}

**Problema noto**

Molte delle notifiche di manutenzione su interventi pianificati di manutenzione/aggiornamento di prodotti sono assenti nel riepilogo e-mail delle notifiche. Stiamo lavorando per l&#39;inclusione di tutte le notifiche di manutenzione nel riepilogo e-mail.

## 8 agosto 2017 {#section_2313A875454044F490B418506DD24593}

| Funzione | Descrizione |
|--- |--- |
| Notifiche - Impostazioni granulari | Puoi abilitare le notifiche per eventi e attività relative a prodotti e soluzioni, comprese le notifiche sull’attività di caricamento di [Attributi clienti](../attributes/attributes.md). |
| Notifiche - Notifiche di manutenzione | Nelle impostazioni di notifica, puoi attivare le notifiche di manutenzione relative a prodotti e soluzioni. |
| Admin Console per soluzioni Experience Cloud | I nuovi clienti Experience Cloud possono iniziare a utilizzare Admin Console, una posizione centrale per la gestione delle adesioni Adobe nell&#39;intera organizzazione.<br>La migrazione ad Admin Console per la gestione degli utenti procederà a ondate. Adobe ti contatterà (amministratori di sistema) quando è il momento di effettuare la migrazione.<br>Amministratori Analytics, consultare [Migrazione Analytics](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/). |

## 22 maggio 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Funzione | Descrizione |
|--- |--- |
| Mappatura di massa suite di rapporti | In Amministrazione &gt; Mappatura suite di rapporti ora puoi selezionare più suite di rapporti, quindi mapparle su un&#39;organizzazione. (in precedenza era necessario mapparle singolarmente).  <br>[La mappatura delle suite di rapporti su un&#39;unica organizzazione consente di abilitare funzioni e servizi tra più soluzioni in Experience Cloud.](../core-services/core-services.md) |
| Aggiornamenti relativi al pubblico di Experience Cloud | **Applicazione di Report: è ora**<br>possibile applicare una suite di rapporti a tutte le tue regole [per l&#39;audience](../audience-library/t-audience-create.md). (in precedenza era necessario indicare una suite di rapporti per ciascuna definizione di regola). <br>**Prop e variablesè**<br>ora possibile includere proprietà Analytics e variabili predefinite (oltre a evar ed eventi) in audience in tempo reale. |

## 8 novembre 2016 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Funzione | Descrizione |
|--- |--- |
| Aggiornamento del profilo e delle password | Gli utenti non possono più modificare le informazioni del profilo utente IMS in Dati personali nella sezione Modifica profilo &gt; Profilo e password, Al contrario, gli utenti vengono reindirizzati a `accounts.adobe.com`. Questo vale per tutti i tipi di identità (Adobe ID, Enterprise e Federated). |

**Correzioni**

* Risolto un problema relativo alle password tecniche che causava un errore nella condivisione delle cartelle tra Creative Cloud e Experience Cloud. (MAC-31067, MAC-32014)
* Risolto un problema relativo al caricamento di certi tipi di file, inclusi i PDF, che era stato riscontrato dopo il rilascio di ottobre nel servizio core Assets. (MAC-32517)

