---
description: Scopri come Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.
keywords: cookie;privacy
solution: Experience Cloud,Analytics,Target,Social
title: 'Cookie di Adobe Target  '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookie
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: c7ed1324015beb7ebcf7a4ee21b05601e36e608f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 83%

---

# Cookie di Adobe Target {#target-cookies}

Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.

Se necessario, puoi modificare queste impostazioni, fatta eccezione per la durata del cookie. In caso di modifica delle impostazioni dei cookie, consulta il rappresentante commerciale di riferimento.

>[!NOTE]
>
>Gli utenti di Adobe Target possono inoltre creare cookie di terze parti personalizzati.

| Impostazione | Informazioni |
| --- | --- |
| Nome cookie | mbox. |
| Dominio cookie | Il primo e il secondo livello dei domini da cui distribuisci il mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. |
| Dominio server | `clientcode.tt.omtrdc.net`, utilizzando il codice cliente per il tuo [!DNL Adobe Target] account. |
| Durata cookie | Il cookie rimane sul browser del visitatore per due anni dall’ultimo accesso. Non puoi modificare la durata del cookie. |

>[!NOTE]
>
>Se uno dei tuoi nomi di dominio include un codice del paese, ad esempio `mycompany.co.uk`, rivolgiti al team dei servizi client per configurare il `at.js` in modo che supporti questo codice.

Il cookie mantiene alcuni valori per gestire l’esperienza dei visitatori nelle campagne Adobe Target:

| Valore | Definizione |
| --- | --- |
| session ID | ID univoco per una sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se generi personalmente l’identificatore sessionId (ad esempio, per implementazioni lato server), considera i seguenti aspetti:<ul><li>L’ID sessione può essere una stringa stampabile qualsiasi, eccetto uno spazio, un punto interrogativo ( ?  ) o una barra ( / ).</li><li>* L&#39;ID sessione deve essere composto da 1 a 128 caratteri.</li><li>Per una particolare sessione, il suo valore deve rimanere lo stesso per tutte le varie richieste.</li><li>Non sono ammesse sessioni parallele (sessionID distinti) per un determinato visitatore in un dato momento.</li></ul>L’indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l’ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non utilizzare un ID sessione diverso per un particolare identificatore `tntId/thirdPartyId` entro 30 minuti dall’ultima richiesta effettuata con l’identificatore `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero risultare incoerenti e imprevedibili.</li><li>L’utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul> |
| pc ID | Un ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente. |
| check | Un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina. |
| disable | Impostato se il tempo di caricamento del visitatore supera il timeout configurato nel file at.js. Per impostazione predefinita, questo timeout dura 1 ora. |
