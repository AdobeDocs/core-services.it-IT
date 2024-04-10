---
description: Scopri come Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.
solution: Experience Cloud,Analytics,Target
title: Cookie di Adobe Target
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 15%

---

# Cookie di Adobe Target

[!DNL Adobe Target] utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.

>[!NOTE]
>
>Le informazioni contenute nel presente articolo si applicano al [[!DNL Target] Libreria JavaScript at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} solo.
>
>Per informazioni sui cookie utilizzati in un [!DNL Target] implementazione tramite [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target=_blank}, see "Does the [!DNL Adobe Experience Platform Web SDK] use cookies? If so, what cookies does it use?" in [Frequently Asked questions in the DNL Platform Web SDK overview guide](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>Se necessario, puoi modificare le impostazioni descritte in questo articolo, fatta eccezione per la durata del cookie. [Consulta il rappresentante del tuo account](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} quando si modificano le impostazioni dei cookie.
>
>[!DNL Target] Gli utenti possono anche creare cookie di terze parti personalizzati.

## Cookie di prime parti

I seguenti cookie di prime parti sono memorizzati nel dominio del cliente:

| Cookie | Dettagli |
| --- | --- |
| mbox | Memorizza identificatori anonimi del visitatore.<P>**Dominio cookie**: dominio da cui distribuisci la mbox. Poiché questo cookie viene fornito dal dominio della tua azienda, il cookie è un cookie di prime parti. Esempio: `mycompany.com`. Se uno dei tuoi nomi di dominio include il codice di un paese, ad esempio `mycompany.co.uk`, collabora con i servizi client per configurare at.js per supportare questo codice. Per informazioni sulla personalizzazione del dominio dei cookie, se necessario, vedi &quot;`cookieDomain`&quot; sotto [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} nel *[!DNL Adobe Target]Guida per gli sviluppatori*.<P>**Dominio server**: `clientcode.tt.omtrdc.net`, utilizzando il codice cliente per il tuo [!DNL Target] account.<P>**Durata cookie**: il cookie rimane sul browser del visitatore per due anni dall’ultimo accesso. Non puoi modificare la durata del cookie.<P>Nel cookie è conservata una serie di valori per la gestione dell’esperienza dei visitatori [!DNL Target] attività:<P>**session ID**: identificatore univoco per una determinata sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se stai generando `sessionId` te stesso (ad esempio, per [implementazioni lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=it){target=_blank}), verifica quanto segue:<ul><li>L’ID sessione può essere una stringa stampabile qualsiasi, ad eccezione di uno spazio, un punto interrogativo ( ? ) o una barra ( / ).</li><li>L’ID sessione può contenere da 1 a 128 caratteri.</li><li>Per una particolare sessione, il valore del cookie deve rimanere lo stesso in più richieste.</li><li>Non si dovrebbero mai avere sessioni parallele (distinte) `sessionIds`) per un determinato visitatore in qualsiasi momento.</li></ul>L’indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l’ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non utilizzare un ID sessione diverso per un particolare `tntId/thirdPartyId` entro 30 minuti dall&#39;ultima richiesta effettuata con il `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero risultare incoerenti e imprevedibili.</li><li>Dopo trenta minuti di inattività da parte di un visitatore, è necessario utilizzare un nuovo ID sessione.</li><li>Utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul>NOTA: vedere [limite al numero di richieste simultanee](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=it#content-delivery){target=_blank} per un determinato ID sessione.<P>**pc ID**: ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente.<P>**spunta**: valore di test semplice utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina.<P>**disable**: impostato se il tempo di caricamento di un visitatore supera il timeout configurato nel file at.js. Per impostazione predefinita, questo timeout dura un’ora. |
| at_check | Cookie temporaneo per verificare se la funzionalità di lettura/scrittura del cookie è abilitata nel browser. |
| mboxEdgeCluster | Questi cookie sono presenti solo quando/se [impostazione overrideMboxEdgeServer](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=it){target=_blank} è impostato su `true`. |

Non è possibile utilizzare HTTPOnly solo su questi cookie di prime parti. La libreria JavaScript at.js deve leggere/scrivere questi cookie. Questi cookie vengono creati da at.js e non sono impostati dal server.

Il `secure` L&#39;impostazione può essere attivata su tutti questi cookie utilizzando `secureOnly: true` configurazione nell’implementazione at.js.

## Cookie di terze parti

I seguenti cookie di terze parti sono memorizzati su `tt.omtrdc.net`:

| Cookie | Dettagli |
| --- | --- |
| customerclientcode!mboxPC | Questo cookie è presente se è abilitato l’attraversamento di più domini. |
| customerclientcode!mboxSession | Questo cookie è presente se è abilitato l’attraversamento di più domini. |

Questi cookie di terze parti sono solo HTTPO predefiniti e sono impostati da [!DNL Target] server edge.

Il `secure` può essere attivata su tutti i cookie utilizzando `secureOnly: true` configurazione nell’implementazione at.js.