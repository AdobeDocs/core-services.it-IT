---
description: Rimozione degli utenti che hanno bloccato tutti i cookie su browser desktop e mobili.
keywords: cookie;privacy
seo-description: Rimozione degli utenti che hanno bloccato tutti i cookie su browser desktop e mobili.
seo-title: Abilitazione delle impostazioni della privacy per i cookie del browser
solution: Experience Cloud,Analytics,Target,Social
title: Abilitazione delle impostazioni della privacy per i cookie del browser
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: 012283d79bda42f9dabb20b25903927b075f6d54

---


# Abilitazione delle impostazioni della privacy per i cookie del browser{#enable-privacy-settings-for-browser-cookies}

Rimozione degli utenti che hanno bloccato tutti i cookie su browser desktop e mobili.

Questa impostazione consente di rispettare l’intenzione di un utente di interrompere l’elaborazione di Analytics se blocca tutti i cookie nelle impostazioni dei cookie del browser.

1. Seleziona **[!UICONTROL Strumenti di amministrazione]** &gt; **[!UICONTROL Suite di report]**.
1. Fai clic su **[!UICONTROL Modifica impostazioni]** &gt; **[!UICONTROL Generali]** &gt; **[!UICONTROL Impostazioni privacy]**.
1. Abilita **[!UICONTROL Impostazioni privacy]** (per desktop o dispositivi mobili).

   Attivando questa funzione, i dati raccolti dai browser desktop impostati dall’utente sul blocco di tutti i cookie verranno esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser, i dati verranno inclusi nei report di Analytics.

>[!IMPORTANT]
>
>Tieni presente che molte app mobili (come il browser in app per Facebook o Twitter) possono essere visualizzate come browser mobile standard ma non consentono tutti i cookie. Se abiliti questa funzione, una parte importante del traffico mobile potrebbe essere esclusa dai report di Analytics.

**Informazioni sulle impostazioni della privacy del browser**

Secondo quanto stabilito dalle leggi e dalle indicazioni normative, l’azione di blocco dei cookie da parte di un utente è equiparabile alla scelta dell’utente di non partecipare alle attività di profiling. Attivando questa funzione, i dati raccolti dai browser desktop impostati dall’utente sul blocco di tutti i cookie, verranno esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser Web, i dati verranno inclusi nei report di Analytics.

I legislatori di tutto il mondo hanno stabilito (sia nelle norme che negli accordi) che le impostazioni dei browser sui cookie rappresentano un’indicazione della preferenza degli utenti di rifiutare il profiling. In particolare, i legislatori hanno dichiarato che impostare il browser in modo che blocchi i cookie di terze parti costituisce una richiesta di rinuncia al tracciamento di terze parti (cross-site) e che il blocco di tutti i cookie è una richiesta di rinuncia a ogni tipo di tracciamento. Anche se gli identificatori lato server (come l’indirizzo IP o l’agente utente) possono essere un’opzione utile per ignorare le impostazioni dei browser sui cookie, alcuni legislatori li considerano come un modo di eludere la volontà degli utenti.