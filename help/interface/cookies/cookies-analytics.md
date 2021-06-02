---
description: Scopri come funzionano i cookie di Adobe Analytics in Adobe Experience Cloud.
keywords: cookie;privacy
solution: Experience Cloud,Analytics,Target
title: 'Cookie di Analytics '
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookie
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 84%

---

# Cookie di Analytics {#analytics-cookies}

Adobe Analytics utilizza i cookie per differenziare le richieste di browser diversi e memorizzare informazioni utili che un’applicazione può utilizzare in un secondo momento. Possono anche essere utilizzati per associare le informazioni di navigazione ai record dei clienti.

Analytics utilizza i cookie per definire in modo anonimo nuovi visitatori, aiutare ad analizzare i dati clickstream e monitorare l’attività storica sul sito web, ad esempio la risposta a campagne particolari o la lunghezza del ciclo di vendita.

* [Nome cookie: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Nome cookie: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Nome cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nome cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nome cookie: s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Nome cookie: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Nome cookie: s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [Cookie impostati da plug-in](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Ulteriori informazioni sui [cookie di prime parti](/help/interface/cookies/cookies-first-party.md) sono disponibili nella guida di Analytics.

## Nome cookie: s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Contiene una copia dell’Experience Cloud ID (ECID) o del MID. Il MID viene memorizzato in una coppia chiave/valore con sintassi s_ecid=MCMID | `<ECID>` |
| Scadenza | 2 anni |
| Utilizzo | Questo cookie viene impostato dal dominio del cliente dopo che il cookie AMCV è stato impostato dal client. Questo cookie ha lo scopo di consentire il tracciamento degli ID permanenti nello stato Prima parte e viene utilizzato come ID di riferimento se il cookie AMCV è scaduto. Vedi Cookie AMCV qui per ulteriori dettagli |
| Posizione | Solo clienti CNAME. Non applicabile in caso di terze parti. Il cookie è memorizzato nel tuo dominio, lo stesso utilizzato dal CNAME e dalla richiesta di immagine Analytics. |
| Dimensione | 45 byte |

## Nome cookie: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Questo cookie viene impostato e letto dal codice JavaScript per determinare se i cookie sono abilitati (impostato su &quot;True&quot;) |
| Scadenza | Questo è un cookie di sessione e scade quando il browser viene chiuso |
| Utilizzo | Un solo cookie per tutti gli account |
| Posizione | Il cookie viene memorizzato nel dominio della pagina. |
| Dimensione | 4 byte |

## Nome cookie: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Questo cookie viene impostato e letto dal codice JavaScript quando sono abilitate le funzionalità ClickMap e Activity Map; contiene informazioni sul collegamento precedente su cui l’utente ha fatto clic |
| Scadenza | Questo è un cookie di sessione e scade quando il browser viene chiuso |
| Utilizzo | Un solo cookie per tutti gli account |
| Posizione | Il cookie viene memorizzato nel dominio della pagina. |
| Dimensione | Varia a seconda della dimensione dell’URL della pagina, ma in genere è compresa tra 100 e 200 byte |

## Nome cookie: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | ID visitatore univoco/timestamp. |
| Scadenza | 2 anni |
| Utilizzo | Questo cookie viene usato per identificare un visitatore univoco. |
| Posizione | Questo cookie viene memorizzato nel dominio della richiesta di immagine, in genere 2o7.net o omtrdc.net se utilizzi cookie di terze parti o il tuo dominio se utilizzi cookie di prime parti |
| Dimensione | 44 byte |

>[!NOTE]
>
>Ogni ID visitatore di Analytics è associato a un profilo visitatore sui server Adobe. I profili dei visitatori vengono eliminati dopo 1 anno di inattività, a prescindere dalla scadenza del cookie ID visitatore.

## Nome cookie: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | ID visitatore univoco/timestamp di fallback. |
| Scadenza | 2 anni |
| Utilizzo | Questo cookie viene usato per identificare un visitatore univoco. Se il cookie standard `s_vi` non è disponibile a causa di restrizioni relative ai cookie di terze parti. Non viene utilizzato per le implementazioni che utilizzano cookie di prime parti |
| Posizione | Questo cookie viene memorizzato nel dominio come cookie di prime parti |
| Dimensione | 33 byte |

## Flag dei cookie

Nella tabella seguente sono descritti i flag per i cookie di Analytics:

| Cookie (impostato da) | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi (risposta http) | No | Sì quando SameSite è &quot;None&quot; e la connessione utilizza HTTPS | &quot;Lax&quot; per impostazione predefinita quando si utilizza CNAME. &quot;None&quot; quando si utilizza 2o7.net o omtrdc.net |
| s_ecid (risposta http) | No | No | &quot;Lax&quot; |
| s_fid (Javascript) | No | No | Non impostato |
| s_cc (Javascript) | No | No | Non impostato |
| s_sq (Javascript) | No | No | Non impostato |

>[!NOTE]
>
>Se si utilizza un singolo CNAME per il monitoraggio tra più domini o proprietà, SameSite deve essere impostato su “None” per `s_vi`. Per assistenza sulla modifica delle impostazioni dei cookie di Analytics, contatta l’Assistenza clienti.

## Cookie impostati da plug-in {#section-a6b1cae8454945fab9eea5c7884c40fc}

Puoi impostare altri cookie in base all’utilizzo dei plug-in di Analytics. Questi cookie sono snippet di codice disponibili per il client in varie circostanze. Queste circostanze includono: recupero dei valori dall’URL; concatenazione di valori da passare ad Analytics; acquisizione dell’abbandono del modulo e così via. Per informazioni specifiche sui cookie impostati da ciascun plug-in, contatta l’Assistenza clienti. Un esempio può essere il cookie [!DNL s_vh] usato con i plug-in *Imposta una volta per* e *Imposta e ottieni ultimo valore*.

Le variabili di conversione (eVarX) trasmesse su una richiesta di immagine senza JavaScript, come il codice inserito all’interno di un’e-mail, vengono attribuite correttamente solo se il client e-mail e il browser Web condividono lo spazio dei cookie.
