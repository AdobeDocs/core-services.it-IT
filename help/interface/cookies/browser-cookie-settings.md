---
description: Rimuovi utenti che hanno bloccato tutti i cookie su browser desktop e mobili.
keywords: cookie; privacy
seo-description: Rimuovi utenti che hanno bloccato tutti i cookie su browser desktop e mobili.
seo-title: Abilitare le impostazioni della privacy per i cookie del browser
solution: Marketing Cloud, Analytics, Target, Social
title: Abilitare le impostazioni della privacy per i cookie del browser
uuid: f 6 a 56 e 8 b-b 021-49 db -8 eb 4-6 c 14 af 0 c 7243
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Enable privacy settings for browser cookies{#enable-privacy-settings-for-browser-cookies}

Rimuovi utenti che hanno bloccato tutti i cookie su browser desktop e mobili.

Questa impostazione consente di rispettare l'intenzione di un utente di interrompere l'elaborazione di Analytics se blocca tutti i cookie nelle impostazioni dei cookie del browser.

1. Navigate to **[!UICONTROL Admin Tools]** &gt; **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Privacy Settings]**.
1. Enable **[!UICONTROL Privacy Settings]** (for desktop or mobile).

   Attivando questa funzione, i dati raccolti dai browser desktop in cui l'utente ha impostato il proprio browser per bloccare tutti i cookie saranno esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser , i dati verranno inclusi nei report di Analytics.

>[!IMPORTANT]
>
>Tenete presente che molte app mobili (come il browser in app per Facebook o Twitter) possono essere visualizzate come browser mobile standard ma non consentono tutti i cookie. L'abilitazione di questa funzione potrebbe escludere un'alta proporzione del traffico mobile dai report di Analytics.

**Informazioni sulle impostazioni della privacy del browser**

Secondo quanto stabilito dalle leggi e dalle indicazioni normative, l'azione di blocco dei cookie da parte di un utente è equiparabile alla scelta dell'utente di non partecipare alle attività di profiling. Attivando questa funzione, i dati raccolti dai browser desktop in cui l'utente ha impostato il proprio browser per bloccare tutti i cookie saranno esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser Web, i dati verranno inclusi nei report di Analytics.

I legislatori in tutto il mondo hanno dichiarato (sia in guida che negli accordi) che le impostazioni del browser dei cookie rappresentano un'indicazione della preferenza utente per rifiutare il profiling. Specificamente, questi legislatori hanno dichiarato che l'impostazione del browser per bloccare i cookie di terze parti è una richiesta di rinuncia da tracciamento di terze parti (cross-site); e bloccare tutti i cookie è una richiesta di rinuncia per tutti i tracciamenti. Mentre identificatori lato server (come indirizzo IP o agente utente) possono essere un'opzione utile che ignora le impostazioni del browser dei cookie, alcuni legislatori li visualizzano come un'elusione di scelta utente.

<!--
<p>Awaiting content from Vinay May 20 2015 </p>
<p>https://wiki.corp.adobe.com/display/omtrcache/Inferred+Opt+Out </p>
<p>https://wiki.corp.adobe.com/display/omtrplatform/Auto-opt-out+For+Users+Who+Block+Cookies </p>
-->

