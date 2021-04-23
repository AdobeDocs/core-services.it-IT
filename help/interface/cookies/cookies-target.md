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
translation-type: tm+mt
source-git-commit: dcb6fa5d8458995cba66bc2f89c954aa6bcd5923
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Cookie di Adobe Target {#target-cookies}

Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.

Puoi modificare queste impostazioni, se necessario, fatta eccezione per la durata del cookie. In caso di modifica delle impostazioni dei cookie, consulta il rappresentante commerciale di riferimento.

>[!NOTE]
>
>Gli utenti di Adobe Target possono inoltre creare cookie di terze parti personalizzati.

| Impostazione | Informazioni |
| --- | --- |
| Nome cookie | mbox. |
| Dominio cookie | Il primo e il secondo livello dei domini da cui distribuisci il mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. |
| Dominio server | `clientcode.tt.omtrdc.net`[!DNL Adobe Target], utilizzando il codice cliente per il tuo account. |
| Durata cookie | Il cookie rimane sul browser del visitatore per due anni dal suo ultimo accesso. Non puoi modificare la durata del cookie. |



>[!NOTE]
>
>Se uno dei tuoi nomi di dominio include un codice del paese, ad esempio `mycompany.co.uk`, rivolgiti al team dei servizi client per configurare il [!DNL at.js] da supportare.

Nel cookie è conservata una serie di valori per la gestione dell’esperienza dei visitatori in relazione alle campagne di Adobe Target:

| Valore | Definizione |
| --- | --- |
| session ID | Identificatore univoco per una determinata sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se generi tu stesso sessionId (ad esempio, per le implementazioni lato server), assicurati quanto segue:<ul><li>L’ID sessione può essere una stringa stampabile tranne uno spazio, un punto interrogativo ( ? ) o una barra ( / ).</li><li>* L&#39;ID sessione deve essere compreso tra 1 e 128 caratteri.</li><li>Per una particolare sessione, il suo valore deve rimanere lo stesso in più richieste</li><li>Non dovresti mai avere sessioni parallele (sessionID distinti) per un determinato visitatore in un dato momento.</li></ul>L&#39;indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l&#39;ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non devi utilizzare un ID sessione diverso per un particolare `tntId/thirdPartyId` entro 30 minuti dall&#39;ultima richiesta effettuata con il `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero essere incoerenti e imprevedibili.</li><li>L’utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul> |
| pc ID | Un ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente. |
| check | Un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina. |
| disable | Impostato se il tempo di caricamento del visitatore supera il timeout configurato nel file at.js . Per impostazione predefinita, la sua durata è di 1 ora. |

