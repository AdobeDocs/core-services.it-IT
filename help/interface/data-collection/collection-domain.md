---
title: Scegli un dominio di raccolta dati
description: Scopri i domini che puoi utilizzare per inviare dati ad Adobe e come trovare l’ID tenant della tua organizzazione.
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%
---
# Scegli un dominio di raccolta dati

Il dominio di raccolta dati è il nome host al quale l’implementazione invia i dati. Tutti i prodotti Adobe CX Enterprise che utilizzano la raccolta dati di Adobe (come Adobe Analytics, Customer Journey Analytics, Adobe Experience Platform, Adobe Target e Adobe Journey Optimizer) si basano su questo dominio.

## Opzioni del dominio di raccolta dati

| Opzione | Dominio di implementazione | [RDC](rdc.md) bloccato dall&#39;area geografica | Manutenzione certificati |
| --- | --- | --- | --- |
| [Dominio di terze parti](#third-party) | `example.data.adobedc.net` | Non supportato | Nessuna |
| Dominio di prima parte con un [certificato gestito da Adobe](adobe-managed-cert.md) | `data.example.com` | Supportato | Nessuno (Adobe rinnova il certificato automaticamente) |
| Dominio di prima parte con un [certificato gestito dal cliente](customer-managed-cert.md) | `data.example.com` | Supportato | La tua organizzazione rinnova il certificato e lo fornisce ad Adobe |
| [Rete di distribuzione di contenuti (CDN) con origine di terze parti](cdn.md#third-party-origin) | `data.example.com` | Non supportato | Nessuna |
| [CDN con origine di prime parti](cdn.md#first-party-origin) | `data.example.com` | Supportato | La tua organizzazione rinnova il certificato e lo fornisce ad Adobe |

## Dominio di raccolta dati di terze parti {#third-party}

Se non utilizzi un dominio di prime parti, invia dati a un sottodominio di `data.adobedc.net`. Adobe consiglia di utilizzare il [ID tenant](#tenant-id) della tua organizzazione come sottodominio. Ad esempio, `example.data.adobedc.net`. Questo dominio è anche l&#39;origine consigliata quando si [instrada la raccolta dati tramite una rete CDN](cdn.md).

* I domini di terze parti utilizzano sempre il tipo predefinito [RDC](rdc.md#third-party-data-collection).
* Non utilizzare sottodomini più profondi di `example.data.adobedc.net`. `custom.example.data.adobedc.net` ad esempio non è un dominio di raccolta dati valido.
* Le implementazioni meno recenti potrebbero utilizzare domini come `sc.omtrdc.net` o `2o7.net`. Anche se questi domini sono ancora validi, Adobe consiglia di utilizzare `data.adobedc.net` ove possibile.

### Trovare l’ID tenant {#tenant-id}

1. Accedi a [Adobe CX Enterprise](https://experience.adobe.com) utilizzando le credenziali Adobe ID.
1. In qualsiasi punto dell&#39;interfaccia di CX Enterprise, premere `[Cmd]` + `[I]` (macOS) o `[Ctrl]` + `[I]` (Windows).
1. Viene visualizzato un **[!UICONTROL Debugger dati utente]**. Selezionare la scheda **[!UICONTROL Organizzazioni assegnate]**.
1. Espandi l’organizzazione IMS desiderata.
1. Individua il campo **[!UICONTROL Tenant]**. Questo valore è l’ID tenant.

L&#39;ID tenant è diverso dall&#39;ID organizzazione IMS, che termina con `@AdobeOrg`. Ogni organizzazione IMS ha un ID tenant. Se la tua azienda utilizza più organizzazioni IMS, ogni organizzazione ha il proprio ID tenant.

## Aggiornare l’implementazione {#update-implementation}

Quando modifichi il dominio di raccolta dei dati, aggiorna ogni implementazione che invia dati ad Adobe:

* **Estensione tag per Web SDK**: aggiorna il campo [[!UICONTROL Dominio Edge]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general) durante la configurazione dell&#39;estensione.
* **Web SDK (lega)**: aggiornare la proprietà [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain) nel comando `configure`.
* **Estensione Adobe Analytics**: aggiorna il campo [[!UICONTROL SSL Tracking Server]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview) durante la configurazione dell&#39;estensione. Assicurati inoltre di aver installato l&#39;estensione tag [Visitor ID Service](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview). Per ulteriori informazioni, consulta [Identificazione del visitatore tramite l&#39;estensione tag Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension).
* **AppMeasurement**: aggiorna la variabile di configurazione [`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure). Assicurati inoltre di avere implementato il [Servizio ID visitatori](https://experienceleague.adobe.com/it/docs/id-service/using/home) tramite `VisitorAPI.js`. Per ulteriori informazioni, consulta [Identificazione del visitatore tramite AppMeasurement](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement).
* **Altre implementazioni**: aggiorna il dominio di raccolta dati in qualsiasi altra implementazione che invia dati ad Adobe, ad esempio applicazioni per dispositivi mobili o implementazioni lato server.

Se l’implementazione non utilizza il servizio ID visitatore o il Web SDK, la modifica del dominio di raccolta dati cambia il dominio dei cookie visitatore e i visitatori di ritorno possono essere conteggiati come nuovi visitatori.

Se il sito utilizza più metodi di implementazione e non è possibile aggiornarli tutti contemporaneamente, è consigliabile configurare un periodo di tolleranza. Consulta le [considerazioni sulla migrazione al servizio ID visitatori](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration) per ulteriori passaggi su come evitare che i visitatori vengano conteggiati come nuovi visitatori nel tuo sito.
