---
description: Scopri come [!DNL Adobe Target] utilizza i cookie per consentire agli operatori dei siti Web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.
solution: Experience Cloud,Analytics,Target
title: Cookie di Adobe Target
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 95ca3a8e172166d7901873e0dc2e096e0bba7cd2
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 8%

---

# Cookie di [!DNL Adobe Target]

[!DNL Adobe Target] utilizza i cookie per consentire agli operatori dei siti Web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.

>[!NOTE]
>
>Le informazioni contenute in questo articolo si applicano solo alla [[!DNL Target] libreria JavaScript at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}.
>
>Per informazioni sui cookie utilizzati in un&#39;implementazione di [!DNL Target] utilizzando [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target=_blank}, vedere &quot;[!DNL Adobe Experience Platform Web SDK] utilizza i cookie? In caso affermativo, quali cookie utilizza?&quot; in [[!DNL Domande frequenti nella guida panoramica di Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>Se necessario, puoi modificare le impostazioni descritte in questo articolo, fatta eccezione per la durata del cookie. [Consulta il rappresentante del tuo account](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} quando modifichi le impostazioni dei cookie.
>
>[!DNL Target] utenti possono anche creare cookie di terze parti personalizzati.

## Cookie di prime parti

I seguenti cookie di prime parti sono memorizzati nel dominio del cliente:

| Cookie | Dettagli |
| --- | --- |
| mbox | Memorizza identificatori anonimi del visitatore.<P>**Dominio cookie**: il dominio da cui distribuisci la mbox. Poiché questo cookie viene fornito dal dominio della tua azienda, il cookie è un cookie di prime parti. Esempio: `mycompany.com`. Se uno dei tuoi nomi di dominio include il codice di un paese, ad esempio `mycompany.co.uk`, rivolgiti al team dei servizi client per configurare at.js in modo da supportare tale codice. Per informazioni sulla personalizzazione del dominio dei cookie, se necessario, vedere &quot;`cookieDomain`&quot; in [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} nella Guida per gli sviluppatori di *[!DNL Adobe Target]*.<P>**Dominio server**: `clientcode.tt.omtrdc.net`, utilizzando il codice client per l&#39;account [!DNL Target].<P>**Durata cookie**: il cookie rimane nel browser del visitatore per due anni dall&#39;ultimo accesso. Non puoi modificare la durata del cookie.<P>Nel cookie è conservata una serie di valori per la gestione dell&#39;esperienza dei visitatori in relazione alle attività di [!DNL Target]:<P>**session ID**: un identificatore univoco per una determinata sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se generi `sessionId` autonomamente (ad esempio, per [implementazioni lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}), verifica quanto segue:<ul><li>L’ID sessione può essere una stringa stampabile qualsiasi, ad eccezione di uno spazio, un punto interrogativo ( ? ), parentesi graffe ( { } ) o una barra ( / ).</li><li>L’ID sessione può contenere da 1 a 128 caratteri.</li><li>Per una particolare sessione, il valore del cookie deve rimanere lo stesso in più richieste.</li><li>Non si dovrebbero mai avere sessioni parallele (distinte `sessionIds`) per un determinato visitatore in un dato momento.</li></ul>L’indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l’ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non utilizzare un ID sessione diverso per un particolare `tntId/thirdPartyId` entro 30 minuti dall&#39;ultima richiesta effettuata con `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero risultare incoerenti e imprevedibili.</li><li>Dopo trenta minuti di inattività da parte di un visitatore, è necessario utilizzare un nuovo ID sessione.</li><li>L&#39;utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul>NOTA: vedi [limite del numero di richieste simultanee](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=it#content-delivery){target=_blank} per un determinato ID sessione.<P>**pc ID**: ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente.<P>**check**: un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina.<P>**disable**: impostato se il tempo di caricamento di un visitatore supera il timeout configurato nel file at.js. Per impostazione predefinita, questo timeout dura un’ora. |
| at_check | Cookie temporaneo per verificare se la funzionalità di lettura/scrittura del cookie è abilitata nel browser. |
| mboxEdgeCluster | Questi cookie sono presenti solo se l&#39;impostazione [overrideMboxEdgeServer](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} è impostata su `true`. |

Non è possibile utilizzare HTTPOnly solo su questi cookie di prime parti. La libreria JavaScript at.js deve leggere/scrivere su questi cookie. Questi cookie vengono creati da at.js e non sono impostati dal server.

L&#39;impostazione `secure` può essere abilitata su tutti questi cookie utilizzando la configurazione `secureOnly: true` nell&#39;implementazione at.js.

## Cookie di terze parti

I seguenti cookie di terze parti sono archiviati in `tt.omtrdc.net`:

| Cookie | Dettagli |
| --- | --- |
| customerclientcode!mboxPC | Questo cookie è presente se è abilitato l’attraversamento di più domini. |
| customerclientcode!mboxSession | Questo cookie è presente se è abilitato l’attraversamento di più domini. |

Questi cookie di terze parti sono solo HTTPOnly preconfigurati e sono impostati dai server perimetrali [!DNL Target].

L&#39;impostazione `secure` può essere abilitata su tutti i cookie utilizzando la configurazione `secureOnly: true` nell&#39;implementazione at.js.