---
description: Adobe Analytics utilizza i cookie per differenziare le richieste di vari browser e memorizzare utili informazioni che un'applicazione può utilizzare in un secondo momento. Possono inoltre essere utilizzati per associare le informazioni di navigazione ai record dei clienti.
keywords: cookie; privacy
seo-description: Adobe Analytics utilizza i cookie per differenziare le richieste di vari browser e memorizzare utili informazioni che un'applicazione può utilizzare in un secondo momento. Possono inoltre essere utilizzati per associare le informazioni di navigazione ai record dei clienti.
seo-title: Cookie di Analytics
solution: Marketing Cloud, Analytics, Target, Social
title: Cookie di Analytics
uuid: e 2 d 3 d 61 d -2708-48 b 2-a 7 e 6-2331 f 2 aed 8 e 0
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# Cookie di Analytics{#analytics-cookies}

Adobe Analytics utilizza i cookie per differenziare le richieste di vari browser e memorizzare utili informazioni che un'applicazione può utilizzare in un secondo momento. Possono inoltre essere utilizzati per associare le informazioni di navigazione ai record dei clienti.

In particolare, Analytics utilizza i cookie per definire in modo anonimo nuovi visitatori, aiutare ad analizzare i dati clickstream e monitorare l'attività storica sul sito Web, ad esempio la risposta a campagne particolari o alla lunghezza del ciclo di vendita.

* [Nome cookie: s_ ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Nome cookie: AMCV_ # # # @ adobeorg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Nome cookie: s_ cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nome cookie: s_ cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nome cookie: s_ sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Nome cookie: s_ vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Nome cookie: s_ fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [Cookie impostati per plug-in](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Ulteriori informazioni sono disponibili in Analytics sui cookie [di prime parti](/help/interface/cookies/cookies-first-party.md).

## Nome cookie: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Contiene una copia dell'Experience Cloud ID (ECID) o MID. Il MID viene memorizzato in una coppia chiave-valore che segue questa sintassi, s_ ecid = MCMID | <ECID> |
| Scadenza | 2 anni |
| Utilizzo | Questo cookie viene impostato dal dominio del cliente dopo che il cookie AMCV è stato impostato dal client. Lo scopo di questo cookie è quello di consentire il tracciamento ID permanente nello stato 1 ^ st ^ party e viene utilizzato come ID di riferimento se il cookie AMCV è scaduto. Controlla il cookie AMCV qui per ulteriori dettagli. |
| Posizione | Solo clienti CNAME. Non applicabile per scenari 3 rd-party. Cookie è memorizzato nel dominio, lo stesso dominio utilizzato dal CNAME e dalla richiesta di immagine Analytics. |
| Dimensioni | 45 byte |

## Nome cookie: s_ cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Questo cookie viene impostato e letto dal codice javascript per determinare se i cookie sono abilitati (impostati semplicemente su "True") |
| Scadenza | Questo cookie è un cookie di sessione e scade quando il browser viene chiuso |
| Utilizzo | Un solo cookie per tutti gli account |
| Posizione | Il cookie viene memorizzato nel dominio della pagina |
| Dimensioni | 4 byte |

## Nome cookie: s_ sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Questo cookie viene impostato e letto dal codice javascript quando sono abilitate le funzionalità clickmap e la funzionalità Activity Map; contiene informazioni sul collegamento precedente su cui è stato fatto clic dall'utente |
| Scadenza | Questo cookie è un cookie di sessione e scade quando il browser viene chiuso |
| Utilizzo | Un solo cookie per tutti gli account |
| Posizione | Il cookie viene memorizzato nel dominio della pagina |
| Dimensioni | Varia a seconda della dimensione dell'URL della pagina, ma in genere di 100-200 byte |

## Nome cookie: s_ vi {#section-5d50a078de444d12b7d927d68ff3b679}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Marca temporale/timbro data ID univoco |
| Scadenza | 2 anni |
| Utilizzo | Questo cookie viene usato per identificare un visitatore univoco |
| Posizione | Questo cookie viene memorizzato nel dominio della richiesta di immagine, in genere 2 O 7. net se utilizzi cookie di terze parti o il tuo dominio se utilizzi cookie di prime parti. |
| Dimensioni | 44 byte |

>[!NOTE]
>
>Ogni ID visitatore di Analytics è associato a un profilo visitatore sui server Adobe. I profili dei visitatori vengono eliminati dopo 1 anno di inattività, a prescindere dalla scadenza del cookie ID visitatore.

## Nome cookie: s_ fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| Attributo | Descrizione |
|--- |--- |
| Informazioni memorizzate | Indicatore del tempo/data ID visitatore univoco |
| Scadenza | 5 anni |
| Utilizzo | Questo cookie viene utilizzato per identificare un visitatore univoco se il cookie s_ vi standard non è disponibile a causa di limitazioni dei cookie di terze parti. Non utilizzata per le implementazioni che utilizzano cookie di prime parti. |
| Posizione | Questo cookie viene memorizzato nel dominio come cookie di prime parti. |
| Dimensioni | 33 byte |

## Cookie impostati per plug-in {#section-a6b1cae8454945fab9eea5c7884c40fc}

Potete impostare altri cookie in base all'utilizzo dei plug-in di Analytics. Questi cookie sono snippet di codice disponibili per il client in diverse circostanze. Queste circostanze includono: recupero dei valori dall'URL; concatenazione di valori da passare ad Analytics; acquisire l'abbandono del modulo e così via. Per informazioni sui cookie impostati da ciascun plug-in, contatta clientcare. Un esempio rappresenta [!DNL s_vh] il cookie usato con i plug-in *Imposta una volta per* volta e *Imposta e ottieni ultimo valore* .

Le variabili di conversione (evarx) trasmesse in una richiesta di immagine senza javascript, come il codice inserito all'interno di un'e-mail, vengono attribuite correttamente solo se il client e-mail e il browser Web condividono lo stesso spazio di cookie.
