---
title: Cookie di Adobe Experience Platform Web SDK
description: Scopri in che modo il Web SDK utilizza i cookie applicabili alla tua implementazione.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: 'https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 7b12d5debfccd62ab7b416e9a6fe278d251a4ca5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 0%
---
# Cookie di Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utilizza i cookie per memorizzare valori specifici dell’implementazione.

| Nome | Età massima | Dimensione | Descrizione |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 33696000 (390 giorni) quando scritto dal Web SDK | 44 byte quando scritti dal Web SDK (`MCMID\|<ECID>`); maggiore quando scritti da `VisitorAPI.js` | Presente quando [`idMigrationEnabled`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) è abilitato, impostazione predefinita. Questa funzione risulta utile durante la transizione al Web SDK, mentre alcune parti del sito utilizzano ancora `VisitorAPI.js`. Il Web SDK legge questo cookie per riutilizzare un ECID esistente. Dopo che Edge Network ha restituito un ECID, il Web SDK lo scrive in questo cookie se il cookie è mancante o contiene un ECID diverso. |
| **`com.adobe.alloy.getTld`** | Nessuno (cookie di sessione, eliminato immediatamente) | 22 byte | Cookie helper temporaneo utilizzato internamente dal Web SDK per determinare il dominio di primo livello del sito corrente. Il Web SDK scrive ed elimina questo cookie al caricamento della libreria, prima dell&#39;esecuzione del comando `configure` e prima della valutazione del consenso, in modo che gli scanner dei cookie possano segnalarlo come impostato prima del consenso. Il cookie contiene solo il proprio nome e non memorizza dati comportamentali o di profilo. |
| **`demdex`** | 15552000 (180 giorni) | varia | Cookie di terze parti nel dominio `demdex.net`. Presente quando [`thirdPartyCookiesEnabled`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/thirdpartycookiesenabled) è abilitato (impostazione predefinita) e il browser consente i cookie di terze parti per impostazione predefinita, ad esempio Chrome o Edge. In tal caso, il Web SDK invia richieste di identità a `adobedc.demdex.net`, che imposta il cookie. Audience Manager utilizza questo cookie per assegnare un ID univoco e supportare la sincronizzazione, la segmentazione, la modellazione e il reporting degli ID. Vedi `demdex` in [Cookie di Audience Manager](audience-manager.md). |
| **`kndctr_<orgId>_identity`** | 34128000 (395 giorni) | 100-120 byte (variabile) | Memorizza l’ECID e altre informazioni correlate per quel dispositivo. |
| **`kndctr_<orgId>_cluster`** | 1800 (30 minuti) | 3-5 byte | Memorizza l’area Edge Network (hint di posizione) che risponde alle richieste dell’utente corrente. L’area viene utilizzata nel percorso URL in modo che Edge Network possa indirizzare la richiesta all’area corretta. Se un utente si connette con un indirizzo IP diverso entro la durata del cookie, la richiesta viene nuovamente indirizzata all’area più vicina. |
| **`kndctr_<orgId>_consent`** | 15552000 (180 giorni) | 10-11 byte | Memorizza le preferenze di consenso del visitatore. Imposta sempre indipendentemente dal consenso, in quanto memorizza le preferenze di consenso stesse. |
| **`kndctr_<orgId>_consent_check`** | 7200 (2 ore) | | Helper con ambito di sessione che indica ad Edge Network di ricontrollare il lato server del consenso dopo la scadenza del TTL. Impone un TTL sul consenso memorizzato nella cache. |
| **`kndctr_<orgId>_personalization`** | 34128000 (395 giorni) | | Memorizza le informazioni sulla sessione utilizzate da Adobe Target per personalizzare il contenuto. |
| **`kndctr_<orgId>_advertising`** | 31622400 (366 giorni), rinnovato ogni volta che il cookie viene aggiornato | Da 80 byte a 1 KB (variabile) | Presente quando il componente Adobe Advertising (beta) viene incluso nella build del Web SDK e il consenso del visitatore è `in`. Il Web SDK scrive questo cookie quando l&#39;URL della pagina contiene i parametri di clic di Adobe Advertising (`s_kwcid` o `ef_id`) o quando sono configurati [Adobe Advertising DSP](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) inserzionisti. Memorizza JSON con codifica URL che può includere i dati dei clic di ricerca (`_les_lsc`), un indirizzo IP con hash, una busta RampID LiveRamp (quando è configurato un percorso JavaScript RampID) e marche temporali di conversione utilizzate per limitare le conversioni duplicate. Nei browser che consentono i cookie di terze parti per impostazione predefinita, vengono memorizzati anche l&#39;ID surfista di Adobe Advertising e i dati dei clic di visualizzazione (`ev_lcc`). Questo cookie è impostato solo sul nome host corrente. Il componente carica anche le risorse da `pixel.everesttech.net`, `www.everestjs.net` (quando è configurato un ID partner ID5) e il percorso RampID `ats.js`. Queste risorse possono impostare i propri cookie, che non sono elencati in questa pagina. |
| **`kndctr_<orgId>_bc_session_id`** | Nessuno (cookie di sessione) | | Presente quando si utilizza il componente Brand Concierge (beta). Memorizza l&#39;ID sessione chat di Brand Concierge. Il Web SDK legge questo cookie solo quando [`stickyConversationSession`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/conversation) è abilitato, in modo che le sessioni di chat persistano nei vari caricamenti di pagina. |
| **`mbox`** | 63072000 (2 anni) | | Presente quando [`targetMigrationEnabled`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) è abilitato. Consente di impostare il cookie [mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) di destinazione dal Web SDK. |
| **`mboxEdgeCluster`** | 1800 (30 minuti) | | Presente quando [`targetMigrationEnabled`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) è abilitato. Consente al Web SDK di comunicare il cluster Edge corretto a `at.js` in modo che i profili di Target possano rimanere sincronizzati mentre gli utenti navigano in un sito. Quando il cookie `kndctr_<orgId>_cluster` non è presente, Web SDK legge anche questo cookie per indirizzare le richieste all&#39;area Edge Network corrispondente. |
| **`s_ecid`** | 63115200 (2 anni) | ~ 45 byte | Contiene una copia del CX Enterprise ID (ECID/MID) nel formato `s_ecid=MCMID\|<ECID>`. Funge da backup di prima parte dell’ECID, principalmente per scenari CNAME (prime parti). Quando [`idMigrationEnabled`](https://experienceleague.adobe.com/it/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) è abilitato, Web SDK legge questo cookie per riutilizzare un ECID esistente. |
| **Destinazioni cookie di Audience Manager** (il nome varia) | 864000 (10 giorni), a meno che la destinazione non specifichi una durata diversa | varia | Presente quando Edge Network restituisce una [destinazione cookie](https://experienceleague.adobe.com/it/docs/audience-manager/user-guide/features/destinations/custom-destinations/create-cookie-destination) di Audience Manager per il visitatore. Il Web SDK scrive un cookie di prime parti utilizzando il nome del cookie, il valore e il dominio definiti nella destinazione. I valori sono codificati in URL, in modo coerente con Audience Manager Data Integration Library (DIL). |

Edge Network imposta tutti i cookie con gli attributi `secure` e `sameSite="none"`. Se al momento sul sito web sono presenti sezioni protette e non protette, l’identificazione dell’utente potrebbe non essere accurata. Quando un utente passa da una sezione protetta del sito a una non protetta, Edge Network genera un nuovo `ECID` con la richiesta.

I cookie creati dal Web SDK da soli, anziché in base alla direzione dell&#39;Edge Network, utilizzano attributi diversi. Le destinazioni dei cookie `AMCV_###@AdobeOrg` e Audience Manager includono gli attributi `secure` e `sameSite="none"` solo nelle pagine HTTPS. I cookie `com.adobe.alloy.getTld` e `kndctr_<orgId>_advertising` utilizzano gli attributi predefiniti del browser.
