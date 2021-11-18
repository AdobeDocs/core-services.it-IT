---
description: Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.
keywords: servizi di base
seo-description: An overview of new features and updates in the Experience Cloud.
seo-title: What's new in the Experience Cloud
solution: Experience Cloud
title: 'Novità in Experience Cloud '
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 87%

---


# Novità in Experience Cloud

Una panoramica delle nuove funzionalità e degli aggiornamenti in Experience Cloud.

## Agosto 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Correzioni e miglioramenti per agosto 2018.

* Miglioramenti apportati alla sincronizzazione dei commenti e delle risorse in Creative Cloud ed Experience Cloud. (CORE-15971)
* È stato aggiunto un flag di funzione per controllare la sincronizzazione di risorse tra Experience Cloud e Creative Cloud. (CORE-15938)
* Sono stati apportati miglioramenti alla creazione di segmenti di pubblico, inclusa una migliore esperienza di ricerca ed inserzione. (CORE-5833, CORE-14278)
* È stato corretto un problema di priorità elevata che bloccava la condivisione di cartelle da Experience Cloud a Creative Cloud. (CORE-16677)

## 19 luglio 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Correzioni e miglioramenti per luglio 2018.

* È stata implementata una funzionalità back-end per controllare la condivisione delle risorse tra Experience Cloud-to-AEM e Experience Cloud-to-Creative Cloud. (CORE-14386)
* È stato risolto un problema che impediva il provisioning di nuovi tenant in alcuni ambienti. (CORE-15509)
* È stato corretto un problema a causa del quale gli utenti venivano reindirizzati a [!DNL experiencecloud.adobe.com] nel tentativo di accedere a [!DNL experiencecloud.adobe.com] tramite [!DNL http] invece di [!DNL https] (protetto). (CORE-15587)
* È stato risolto un problema che bloccava le notifiche per alcuni nuovi tenant. (CORE-15240)

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
| Nuova pagina di destinazione dell’amministrazione | Quando accedi all’Experience Cloud e apri la pagina Amministrazione, è disponibile una nuova interfaccia intuitiva per aiutarti ad accedere rapidamente alle tue applicazioni Experience Cloud e ai Servizi di base. |

{style=&quot;table-layout:auto&quot;}

**Correzioni**

* Corretto un errore di caricamento dell&#39;immagine dovuto un aggiornamento di Scene7. (CORE-12746)
* Aggiornamenti effettuati per ridurre il supporto per il protocollo TLS 1.0, come indicato dal PCI al fine eliminare le vulnerabilità relative alla sicurezza. (CORE-7695)

## 26 ottobre 2017 {#section_11195859B4094177A939C0561428B525}

**Problema noto**

Molte delle notifiche di manutenzione su interventi pianificati di manutenzione/aggiornamento di prodotti sono assenti nel riepilogo e-mail delle notifiche. Stiamo lavorando affinché tutte le notifiche di manutenzione vengano incluse nel riepilogo e-mail.

## 8 agosto 2017 {#section_2313A875454044F490B418506DD24593}

| Funzione | Descrizione |
|--- |--- |
| Notifiche - Impostazioni granulari | Puoi abilitare le notifiche per eventi e attività relative a prodotti e applicazioni, comprese le notifiche su [Attributi del cliente](attributes.md) carica attività. |
| Notifiche - Notifiche di manutenzione | Nelle impostazioni di notifica, puoi abilitare le notifiche di manutenzione per prodotti e applicazioni. |
| Admin Console per soluzioni Experience Cloud | I nuovi clienti Experience Cloud possono iniziare a utilizzare Admin Console, che offre una posizione centrale per la gestione delle autorizzazioni Adobe nell’intera l’organizzazione.<br>La migrazione ad Admin Console per la gestione degli utenti procederà a ondate. Quando sarà il momento di effettuare la migrazione, Adobe contatterà gli amministratori di sistema.<br>Per gli amministratori di Analytics: consulta la sezione [Migrazione di Analytics](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=it). |

{style=&quot;table-layout:auto&quot;}

## 22 maggio 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Funzione | Descrizione |
|--- |--- |
| Mappatura in batch di suite di rapporti | In Amministrazione > Mappatura suite di rapporti ora puoi selezionare più suite di rapporti, quindi mapparle su un&#39;organizzazione. (in precedenza era necessario mapparle singolarmente).  <br>[Mappatura di suite di rapporti](core-services.md) in un’unica organizzazione consente di abilitare funzioni e servizi tra più applicazioni nell’Experience Cloud. |
| Aggiornamenti relativi al pubblico di Experience Cloud | **Applicazione di suite di rapporti**<br> Ora puoi applicare una suite di rapporti a tutte le tue [regole per il pubblico](t-audience-create.md). In precedenza, era necessario indicare una suite di rapporti per ciascuna definizione di regola. <br>**Prop e variabili**<br> Ora è possibile includere le proprietà di Analytics e le variabili predefinite (oltre a eVar ed eventi) per il pubblico in tempo reale. |

{style=&quot;table-layout:auto&quot;}

## 8 novembre 2016, 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Funzione | Descrizione |
|--- |--- |
| Aggiornamento di Profilo e password | Gli utenti non possono più modificare le informazioni del profilo utente IMS in Dati personali nella sezione Modifica profilo > Profilo e password, bensì vengono reindirizzati a `accounts.adobe.com`. Questo aggiornamento vale per tutti i tipi di identità (Adobe ID, Enterprise e Federated). |

{style=&quot;table-layout:auto&quot;}

**Correzioni**

* Risolto un problema relativo alle password tecniche che causava un errore nella condivisione delle cartelle tra Creative Cloud e Experience Cloud. (MAC-31067, MAC-32014)
* È stato risolto un problema relativo al caricamento di alcuni tipi di file, inclusi i PDF, che si verificava dopo la versione di ottobre nel servizio core di Assets. (MAC-32517)
