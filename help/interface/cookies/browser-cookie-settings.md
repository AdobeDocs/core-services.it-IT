---
description: Rimozione degli utenti che hanno bloccato tutti i cookie su browser desktop e mobili. Questa impostazione di privacy esclude gli utenti che rinunciano alla raccolta dati di Analytics.
keywords: cookies;privacy
seo-description: Rimozione degli utenti che hanno bloccato tutti i cookie su browser desktop e mobili. Questa impostazione di privacy esclude gli utenti che rinunciano alla raccolta dati di Analytics.
seo-title: Abilitazione delle impostazioni della privacy per i cookie del browser
solution: Marketing Cloud,Adobe Analytics,Adobe Target,Adobe Social
title: Abilitazione delle impostazioni della privacy per i cookie del browser
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Abilitazione delle impostazioni della privacy per i cookie del browser{#enable-privacy-settings-for-browser-cookies}

Potete rimuovere gli utenti che hanno bloccato tutti i cookie sul desktop e sui browser mobili. Questa funzione è un&#39;impostazione della privacy che esclude gli utenti che rinunciano alla raccolta dei dati e consente di rispettare l&#39;intenzione di un utente di interrompere l&#39;elaborazione dell&#39;analisi.

**Per abilitare le impostazioni di privacy per i cookie del browser**

1. Navigate to **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. Abilita **[!UICONTROL Impostazioni privacy]** (per desktop o dispositivi mobili).

>[!IMPORTANT]
>
>Tenete presente che molte app mobili (come il browser in-app per Facebook o Twitter) possono essere visualizzate come browser mobile standard ma non consentono tutti i cookie. Se abiliti questa funzione, una parte importante del traffico mobile potrebbe essere esclusa dai report di Analytics.

**Informazioni sulle impostazioni della privacy del browser**

Le leggi e le linee guida normative hanno indicato che l&#39;azione di un utente per bloccare i cookie è la stessa dell&#39;azione di un utente di rifiutare il profiling. Attivando questa funzione, i dati raccolti dai browser desktop, dove l&#39;utente ha impostato il browser per bloccare tutti i cookie, verranno esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser Web, i dati verranno inclusi nei report di Analytics.

I legislatori di tutto il mondo hanno dichiarato (sia nelle linee guida che negli accordi) che le impostazioni dei cookie del browser sono un&#39;indicazione della preferenza dell&#39;utente per rifiutare il profiling. Nello specifico, questi legislatori hanno dichiarato che l&#39;impostazione del browser per bloccare i cookie di terze parti è una richiesta di rinuncia da parte di terzi (monitoraggio intersito). Il blocco di tutti i cookie è una richiesta di rifiuto per tutto il tracciamento. Anche se gli identificatori lato server (come l’indirizzo IP o l’agente utente) possono essere un’opzione utile per ignorare le impostazioni dei browser sui cookie, alcuni legislatori li considerano come un modo di eludere la volontà degli utenti.