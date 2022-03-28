---
description: Scopri come implementare il recupero preventivo del DNS per ridurre i tempi di caricamento delle pagine con diversi servizi e applicazioni in Experience Cloud.
solution: Experience Cloud
title: 'Utilizzo del recupero preventivo del DNS con diverse applicazioni e servizi '
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 542d3b9a246ca9616a853f4b6711efea290398d7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 100%

---

# Utilizzo del recupero preventivo del DNS con diverse applicazioni e servizi

Implementa il recupero preventivo del DNS per contribuire a ridurre i tempi di caricamento delle pagine con applicazioni e servizi diversi.

## Informazioni sul recupero preventivo del DNS {#section_772BF9CB7C4141DE9B0355146E2CD962}

I browser utilizzano il recupero preventivo del DNS per risolvere automaticamente i nomi di dominio collegati in una pagina web ai relativi indirizzi IP. Il processo di recupero preventivo inizia quando il browser carica una pagina Web. Ad esempio, supponiamo che la pagina contenga un collegamento cliccabile per `www.adobe.com`. Quando un browser carica la pagina, utilizza il [sistema DNS](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) per cercare il nome di dominio collegato e risolverlo nell’indirizzo IP numerico corrispondente. Il recupero preventivo del DNS migliora le prestazioni delle pagine perché il nome di dominio viene risolto sempre in un indirizzo IP prima che il visitatore di un sito faccia clic sul collegamento o pulsante. Il processo di recupero preventivo del DNS è trasparente per gli utenti.

## Recupero preventivo del DNS e applicazioni Adobe Experience Cloud {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

Il recupero preventivo del DNS funziona automaticamente con i collegamenti statici integrati in una pagina. Ciò significa anche che il recupero preventivo del DNS non funziona con applicazioni e servizi diversi da [!UICONTROL Experience Cloud] per i seguenti motivi:

* Ogni applicazione o servizio Experience Cloud genera le chiamate DNS in modo dinamico durante il caricamento della pagina.
* Il browser non può risolvere i nomi di dominio con indirizzi IP prima che vengano effettuate tali chiamate.

Tuttavia, puoi implementare manualmente il recupero preventivo del DNS con le applicazioni Experience Cloud. Per farlo, aggiungi il tag HTML `<dns-prefetch>` alla sezione `<head>` del codice della pagina come mostrato di seguito. Se implementato correttamente, il recupero preventivo del DNS può contribuire a risparmiare alcuni millisecondi sul tempo di caricamento della pagina.

## Esempi di codici di recupero preventivo del DNS {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

Gli esempi seguenti mostrano come eseguire chiamate di recupero preventivo del DNS in diverse applicazioni e servizi [!DNL Experience Cloud]. Alcune chiamate di recupero preventivo richiedono il tuo ID organizzazione [!DNL Adobe] o i dati del server di registrazione. In questi esempi, il codice in *corsivo* rappresenta un segnaposto variabile. Il codice deve essere sostituito con il tuo ID partner [!DNL Adobe], il codice cliente o le informazioni sul server di registrazione, ecc.

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   Aggiungi un tag separato per ogni nome DNS se utilizzi server di registrazione non sicuri e sicuri.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Servizio Experience Cloud ID:** `<link rel="dns-prefetch" href="//fast. *`inserisci l’ID partner qui`*.demdex.net">`

* **Dynamic Tag Manager** (DTM): non obbligatorio. I collegamenti DTM sono disponibili quando viene caricata la pagina.

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [Recupero preventivo del DNS](https://www.chromium.org/developers/design-documents/dns-prefetching)

