---
description: Scopri come abilitare le impostazioni della privacy per i cookie del browser. Puoi rimuovere gli utenti che hanno bloccato tutti i cookie su browser desktop e mobili.
keywords: cookie;privacy
solution: Experience Cloud, Analytics, Target, Social
title: 'Impostazioni della privacy per i cookie del browser  '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookie
topic: Amministrazione
role: Admin
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 57%

---

# Abilitazione delle impostazioni della privacy per i cookie del browser{#enable-privacy-settings-for-browser-cookies}

Puoi rimuovere gli utenti che hanno bloccato tutti i cookie su browser desktop e mobili. Questa funzione è un’impostazione per la privacy che esclude gli utenti che rinunciano alla raccolta dei dati e consente di rispettare l’intenzione di un utente di interrompere l’elaborazione di Analytics.

**Per abilitare le impostazioni della privacy per i cookie del browser**

1. Passa a **[!UICONTROL Strumenti di amministrazione]** > **[!UICONTROL Suite di rapporti]**.
1. Vai a **[!UICONTROL Modifica impostazioni]** > **[!UICONTROL Generale]** > **[!UICONTROL Impostazioni privacy]**.
1. Abilita **[!UICONTROL Impostazioni privacy]** (per desktop o dispositivi mobili).

>[!IMPORTANT]
>
>Molte app mobili (come il browser in-app per Facebook o Twitter) possono essere visualizzate come browser mobile standard ma non consentono tutti i cookie. Se abiliti questa funzione, una parte importante del traffico mobile potrebbe essere esclusa dai report di Analytics.

**Informazioni sulle impostazioni della privacy del browser**

Secondo quanto stabilito dalle leggi e dalle indicazioni normative, l’azione di blocco dei cookie da parte di un utente è equiparabile alla scelta dell’utente di rinunciare alle attività di profiling. Attivando questa funzione, i dati raccolti dai browser desktop impostati dall’utente sul blocco di tutti i cookie, vengono esclusi dai report di Analytics. Se Adobe non è in grado di riconoscere il browser Web, i dati vengono inclusi nei rapporti [!DNL Analytics] .

I legislatori di tutto il mondo hanno stabilito (sia nelle norme che negli accordi) che le impostazioni dei browser sui cookie rappresentano un’indicazione della preferenza degli utenti di rinunciare al profiling. Nello specifico, questi legislatori hanno dichiarato che l’impostazione del browser per il blocco dei cookie di terze parti costituisce una richiesta di rinuncia al tracciamento da parte di terzi (intersito). Il blocco di tutti i cookie è una richiesta di rinuncia a ogni attività di tracciamento. Anche se gli identificatori lato server (come l’indirizzo IP o l’agente utente) possono essere un’opzione auspicabile che aggira le impostazioni del browser dei cookie, alcuni legislatori li considerano come un’elusione delle scelte degli utenti.
