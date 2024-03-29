---
description: Scopri come Adobe Target utilizza i cookie per consentire agli operatori dei siti web di verificare quali contenuti e offerte online sono più rilevanti per i visitatori.
solution: Experience Cloud,Analytics,Target
title: Cookie di Adobe Target
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: ea50808d2514ff3c94ffa1bee2d9aa3ddf51f120
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 95%

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
| Durata cookie | Il cookie rimane sul browser del visitatore per due anni dal suo ultimo accesso. Non puoi modificare la durata del cookie. |



>[!NOTE]
>
>Se uno dei tuoi nomi di dominio include un codice del paese, ad esempio `mycompany.co.uk`, rivolgiti al team dei servizi client per configurare il [!DNL at.js] da supportare.

Nel cookie è conservata una serie di valori per la gestione dell’esperienza dei visitatori in relazione alle campagne di Adobe Target:

| Valore | Definizione |
| --- | --- |
| session ID | ID univoco per una sessione utente. Per impostazione predefinita, la sessione scade dopo 30 minuti di inattività. Se generi personalmente l’identificatore sessionId (ad esempio, per implementazioni lato server), considera i seguenti aspetti:<ul><li>L’ID sessione può essere una stringa stampabile qualsiasi, eccetto uno spazio, un punto interrogativo ( ?  ) o una barra ( / ).</li><li>* L’ID sessione può contenere da 1 a 128 caratteri.</li><li>Per una particolare sessione, il suo valore deve rimanere lo stesso per tutte le varie richieste.</li><li>Non sono ammesse sessioni parallele (sessionID distinti) per un determinato visitatore in un dato momento.</li></ul>L’indirizzamento a un particolare nodo nel cluster Edge viene eseguito utilizzando l’ID sessione.<ul><li>La sessione è attiva per 30 minuti sul lato server. Pertanto, non utilizzare un ID sessione diverso per un particolare `tntId/thirdPartyId` entro 30 minuti dall&#39;ultima richiesta effettuata con il `tntId/thirdPartyId`. In caso contrario, le modifiche al profilo potrebbero risultare incoerenti e imprevedibili.</li><li>L’utilizzo dello stesso ID sessione con più `tntIds/thirdPartyIds` può causare modifiche imprevedibili ai profili identificati da `tntId/thirdPartyIDs`.</li></ul>**Nota**: verifica il [limite del numero di richieste simultanee](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=it#content-delivery) per un determinato ID sessione. |
| pc ID | Un ID semi-permanente per il browser di un visitatore. Rimane attivo finché i cookie non vengono eliminati manualmente. |
| check | Un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina. |
| disable | Impostato se il tempo di caricamento del visitatore supera il timeout configurato nel file at.js. Per impostazione predefinita, la sua durata è di 1 ora. |

