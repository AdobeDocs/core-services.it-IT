---
description: Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.
keywords: core services
seo-description: Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.
seo-title: Novità in Experience Cloud
solution: Experience Cloud
title: Novità in Experience Cloud
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Novità in Experience Cloud

Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.

## Agosto 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Correzioni e miglioramenti per agosto 2018.

* Miglioramenti apportati alla sincronizzazione dei commenti delle risorse in Creative Cloud e Experience Cloud. (CORE-15971)
* È stato aggiunto un flag di funzione per controllare la sincronizzazione di risorse tra Experience Cloud e Creative Cloud. (CORE-15938)
* Sono stati apportati miglioramenti alla creazione di segmenti di pubblico, inclusa una migliore esperienza di ricerca ed elencazione. (CORE-5833, CORE-14278)
* È stato corretto un problema di priorità elevata che bloccava la condivisione di cartelle da MAC a Creative Cloud. (CORE-16677)

## 19 luglio 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Correzioni e miglioramenti per luglio 2018.

* È stata implementata una funzionalità back-end per controllare la condivisione delle risorse tra Marketing Cloud e AEM e Marketing Cloud-to-Creative Cloud. (CORE-14386)
* È stato risolto un problema che impediva il provisioning di nuovi tenant in alcuni ambienti. (CORE-15509)
* È stato corretto un problema a causa del quale gli utenti venivano reindirizzati a [!DNL experiencecloud.adobe.com] nel tentativo di accedere a [!DNL experiencecloud.adobe.com] tramite [!DNL http] invece di [!DNL https] (protetto). (CORE-15587)
* È stato risolto un problema che bloccava le notifiche per alcuni nuovi tenant. (CORE-15240)

## 14 giugno 2018 {#section_7ABC327992CB46B0B8E4A631B8B68899}

Problemi risolti e miglioramenti per giugno 2018.

* È stato abilitato un collegamento per consentire agli amministratori di accedere alle funzioni RGPD. (CORE-11731)
* Funzione Feedback beta aggiornata per limitare i tipi di file che possono essere allegati ai commenti. (CORE-10474)
* Risolto un problema con l&#39;eliminazione del pubblico da Audience Library. (CORE-12792)
* Risolto un problema che creava una schermata vuota durante l&#39;accesso ai collegamenti di Workspace utilizzando Federated ID. (CORE-11620)

## 10 maggio 2018 {#section_498AF78DA17C4720AA0F32B51493E550}

Nuove funzioni e correzioni nell’interfaccia di [!DNL Adobe Experience Cloud].

| Funzione | Descrizione |
|--- |--- |
| Nuova pagina di destinazione amministrazione | Quando accedi a Experience Cloud e vai alla pagina Amministrazione, è disponibile una nuova interfaccia intuitiva per aiutarti ad accedere rapidamente alle soluzioni e ai servizi di base di Experience Cloud. |

**Correzioni**

* Corretto un errore di caricamento dell&#39;immagine dovuto un aggiornamento di Scene7. (CORE-12746)
* Aggiornamenti effettuati per ridurre il supporto per il protocollo TLS 1.0, come indicato dal PCI al fine eliminare le vulnerabilità relative alla sicurezza. (CORE-7695)

## 26 ottobre 2017 {#section_11195859B4094177A939C0561428B525}

**Problema noto**

Molte delle notifiche di manutenzione su interventi pianificati di manutenzione/aggiornamento di prodotti sono assenti nel riepilogo e-mail delle notifiche. Stiamo lavorando per garantire che tutte le notifiche di manutenzione siano incluse nel riepilogo e-mail.

## August 8, 2017 {#section_2313A875454044F490B418506DD24593}

| Funzione | Descrizione |
|--- |--- |
| Notifiche - Impostazioni granulari | Puoi abilitare le notifiche per eventi e attività relative a prodotti e soluzioni, comprese le notifiche sull’attività di caricamento di [Attributi clienti](../attributes/attributes.md). |
| Notifiche - Notifiche di manutenzione | Nelle impostazioni di notifica potete abilitare le notifiche di manutenzione per prodotti e soluzioni. |
| Admin Console per soluzioni Experience Cloud | I nuovi clienti Experience Cloud possono iniziare a utilizzare Admin Console, una posizione centrale per la gestione delle adesioni Adobe in tutta l&#39;organizzazione.<br>La migrazione ad Admin Console per la gestione degli utenti procederà a ondate. Adobe ti contatterà (amministratori di sistema) quando è il momento di effettuare la migrazione.<br>Amministratori di Analytics, consultate Migrazione [di](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)Analytics. |

## 22 maggio 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Funzione | Descrizione |
|--- |--- |
| Mappatura di massa suite di rapporti | In Amministrazione > Mappatura suite di rapporti ora puoi selezionare più suite di rapporti, quindi mapparle su un&#39;organizzazione. (in precedenza era necessario mapparle singolarmente).  <br>[La mappatura delle suite di rapporti](../core-services/core-services.md) su un&#39;unica organizzazione consente di abilitare funzioni e servizi tra più soluzioni in Experience Cloud. |
| Aggiornamenti relativi al pubblico di Experience Cloud | **Applicazione di suite di rapporti **<br>Ora puoi applicare una suite di rapporti a tutte le tue[regole per il pubblico](../audience-library/t-audience-create.md). (in precedenza era necessario indicare una suite di rapporti per ciascuna definizione di regola).<br>**Prop e variabili**<br>Ora è possibile includere le proprietà di Analytics e le variabili predefinite (oltre a eVar ed eventi) per il pubblico in tempo reale. |

## 8 novembre 2016 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Funzione | Descrizione |
|--- |--- |
| Aggiorna a profilo e password | Gli utenti non possono più modificare le informazioni del profilo utente IMS in Dati personali nella sezione Modifica profilo > Profilo e password, bensì vengono reindirizzati a `accounts.adobe.com`. Questo vale per tutti i tipi di identità (Adobe ID, Enterprise e Federated). |

**Correzioni**

* Risolto un problema relativo alle password tecniche che causava un errore nella condivisione delle cartelle tra Creative Cloud e Experience Cloud. (MAC-31067, MAC-32014)
* È stato risolto un problema relativo al caricamento di alcuni tipi di file, inclusi i PDF, che si verificava dopo il rilascio di ottobre nel servizio core Assets. (MAC-32517)
