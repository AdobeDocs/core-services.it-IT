---
description: Scopri come Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.
solution: Target
title: 'Cookie di Adobe Target '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 2fbf283e5ef06314a679b364fd3f0dfc262a884d
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 16%

---

# Cookie di Adobe Target

Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.

>[!NOTE]
>
>Le informazioni contenute in questo articolo si applicano solo alla [libreria JavaScript di Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} (`at.js`). Consulta [Cookie di Adobe Experience Platform Web SDK](web-sdk.md) per informazioni sulle implementazioni di Target tramite Web SDK.
>
>Se necessario, puoi modificare le impostazioni descritte in questo articolo, fatta eccezione per la durata del cookie. [Consulta il rappresentante del tuo account](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html?lang=it){target=_blank} quando modifichi le impostazioni dei cookie.

## Cookie di prime parti

I seguenti cookie di prime parti sono memorizzati nel dominio del cliente:

| Cookie | Dettagli |
| --- | --- |
| `mbox` | Memorizza identificatori anonimi del visitatore.<P>**Dominio cookie**: il dominio da cui distribuisci la mbox. Poiché questo cookie viene fornito dal dominio della tua azienda, il cookie è un cookie di prime parti. Se uno dei tuoi nomi di dominio include il codice di un paese, ad esempio `example.co.uk`, rivolgiti a Servizi client per configurare `at.js` in modo da supportare tale codice. Per informazioni sulla personalizzazione del dominio dei cookie, se necessario, vedere `cookieDomain` in [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} nella guida per gli sviluppatori di Adobe Target.<P>**Dominio server**: `clientcode.tt.omtrdc.net`, utilizzando il codice client per il tuo account Adobe Target.<P>**Durata cookie**: il cookie rimane nel browser del visitatore per due anni dall&#39;ultimo accesso. Non puoi modificare la durata del cookie.<P>Nel cookie è conservata una serie di valori per la gestione dell&#39;esperienza dei visitatori in relazione alle attività di [!DNL Target]:<P>**session ID**: un identificatore univoco per una determinata sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se generi `sessionId` autonomamente (ad esempio, per [implementazioni lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=it){target=_blank}), verifica quanto segue:<ul><li>L’ID sessione può essere una stringa stampabile qualsiasi, ad eccezione di uno spazio, un punto interrogativo ( ? ), parentesi graffe ( { } ) o una barra ( / ).</li><li>L’ID sessione può contenere da 1 a 128 caratteri.</li><li>Per una particolare sessione, il valore del cookie deve rimanere lo stesso in più richieste.</li><li>Non si dovrebbero mai avere sessioni parallele (distinte `sessionIds`) per un determinato visitatore in un dato momento.</li></ul>L’indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l’ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non utilizzare un ID sessione diverso per un particolare `tntId/thirdPartyId` entro 30 minuti dall&#39;ultima richiesta effettuata con `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero risultare incoerenti e imprevedibili.</li><li>Dopo trenta minuti di inattività da parte di un visitatore, è necessario utilizzare un nuovo ID sessione.</li><li>L&#39;utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul>NOTA: vedi [limite del numero di richieste simultanee](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=it#content-delivery){target=_blank} per un determinato ID sessione.<P>**pc ID**: ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente.<P>**check**: un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina.<P>**disable**: impostato se il tempo di caricamento di un visitatore supera il timeout configurato nel file at.js. Per impostazione predefinita, questo timeout dura un’ora. |
| `at_check` | Cookie temporaneo per verificare se la funzionalità di lettura/scrittura del cookie è abilitata nel browser. |
| `mboxEdgeCluster` | Questi cookie sono presenti solo se l&#39;impostazione [overrideMboxEdgeServer](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} è impostata su `true`. |

Impossibile utilizzare `HTTPOnly` su questi cookie di prime parti. La libreria JavaScript `at.js` deve leggere/scrivere su questi cookie. Questi cookie vengono creati da `at.js` e non sono impostati dal server.

L&#39;impostazione `secure` può essere attivata su tutti questi cookie utilizzando la configurazione `secureOnly: true` in `at.js`.

## Cookie di terze parti

Gli utenti di Adobe Target possono creare cookie di terze parti personalizzati. I seguenti cookie di terze parti sono archiviati in `tt.omtrdc.net`:

| Cookie | Dettagli |
| --- | --- |
| `customerclientcode!mboxPC` | Presente se è abilitato l’attraversamento di più domini. |
| `customerclientcode!mboxSession` | Presente se è abilitato l’attraversamento di più domini. |

Questi cookie di terze parti sono solo HTTPO predefiniti e sono impostati dai server di raccolta dati di Adobe Target.

L&#39;impostazione `secure` può essere attivata su tutti i cookie utilizzando la configurazione `secureOnly: true` in `at.js`.
