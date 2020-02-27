---
description: Implementa il recupero preventivo del DNS per contribuire a ridurre i tempi di caricamento delle pagine con soluzioni e servizi diversi.
seo-description: Implementa il recupero preventivo del DNS per contribuire a ridurre i tempi di caricamento delle pagine con soluzioni e servizi diversi.
seo-title: Utilizzo del recupero preventivo del DNS con diverse soluzioni e servizi
solution: Experience Cloud
title: Utilizzo del recupero preventivo del DNS con diverse soluzioni e servizi
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: 73cb227d2b44024706ce24a9ae6aa06c57a8ce85

---


# Utilizzo del recupero preventivo del DNS con diverse soluzioni e servizi

Implementa il recupero preventivo del DNS per contribuire a ridurre i tempi di caricamento delle pagine con soluzioni e servizi diversi.

## Informazioni sul recupero preventivo del DNS {#section_772BF9CB7C4141DE9B0355146E2CD962}

I browser utilizzano il recupero preventivo del DNS per risolvere automaticamente i nomi di dominio collegati a una pagina Web negli indirizzi IP corrispondenti. Il processo di recupero preventivo inizia quando il browser carica una pagina Web. Ad esempio, supponiamo che la tua pagina contenga un collegamento selezionabile a `www.adobe.com`. Quando un browser carica la pagina, utilizza il [sistema DNS](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) per cercare il nome di dominio collegato e risolverlo nell&#39;indirizzo IP numerico corrispondente. Il recupero preventivo del DNS migliora le prestazioni delle pagine perché il nome di dominio viene risolto sempre in un indirizzo IP prima che il visitatore di un sito faccia clic sul collegamento o pulsante. Il processo di recupero preventivo del DNS è trasparente per gli altri utenti.

## Recupero preventivo del DNS e soluzioni Adobe Experience Cloud {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

Il recupero preventivo del DNS funziona automaticamente con i collegamenti statici integrati in una pagina. Ciò significa anche che il recupero preventivo del DNS non funziona con soluzioni e servizi [!UICONTROL Experience Cloud] diversi perché:

* Ogni soluzione o servizio Experience Cloud genera dinamicamente chiamate DNS durante il caricamento della pagina.
* Il browser non può risolvere i nomi di dominio in indirizzo IP prima dell&#39;esecuzione di tali chiamate.

Tuttavia, puoi implementare manualmente il recupero preventivo del DNS con le soluzioni Experience Cloud. Per farlo, aggiungi il tag HTML `<dns-prefetch>` alla sezione `<head>` del codice della pagina come mostrato di seguito. Se implementato correttamente, il recupero preventivo del DNS può contribuire a risparmiare alcuni millisecondi sul tempo di caricamento della pagina.

## Esempi di codici di recupero preventivo del DNS {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

Gli esempi seguenti mostrano come eseguire chiamate di recupero preventivo del DNS in diverse soluzioni e servizi [!DNL Experience Cloud]. Alcune chiamate di recupero preventivo richiedono il tuo ID organizzazione [!DNL Adobe] o i dati del server di registrazione. In questi esempi, il codice in *corsivo* rappresenta un segnaposto variabile. Il codice deve essere sostituito con il tuo ID partner [!DNL Adobe], il codice cliente o le informazioni sul server di registrazione, ecc.

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   Aggiungi un tag separato per ogni nome DNS se utilizzi server di registrazione non sicuri e sicuri.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **** Servizio Experience Cloud ID: `<link rel="dns-prefetch" href="//fast. *`inserire qui l&#39;ID del partner`*.demdex.net">`

* **Dynamic Tag Manager** (DTM): non obbligatorio. I collegamenti DTM sono disponibili non appena si carica la pagina.

* **Media Optimizer (Ad Cloud):**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **Target:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_LIKE_THIS]
>
>* [Recupero preventivo del DNS](https://www.chromium.org/developers/design-documents/dns-prefetching)

