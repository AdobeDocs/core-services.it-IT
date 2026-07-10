---
description: Scopri come implementare il recupero preventivo del DNS per ridurre i tempi di caricamento delle pagine con diversi servizi e applicazioni in CX Enterprise.
solution: Experience Cloud
title: Usa prelettura DNS
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
TQID: https://experienceleague.adobe.com/oAe81mw-qFetDM0zky2eS6DNf-XZ67H68Qw-Sa8mk0Y
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7bfc22e90d727d1743c2b6b7bc645033d5d38f1b
workflow-type: tm+mt
source-wordcount: 359
ht-degree: 77%

---

# Utilizzare il recupero preventivo del DNS

Implementa il recupero preventivo del DNS per contribuire a ridurre i tempi di caricamento delle pagine con applicazioni e servizi diversi.

## Informazioni sul recupero preventivo del DNS

I browser utilizzano il recupero preventivo del DNS per risolvere automaticamente i nomi di dominio collegati in una pagina web ai relativi indirizzi IP. Il processo di recupero preventivo inizia quando il browser carica una pagina Web. Ad esempio, supponiamo che la pagina contenga un collegamento cliccabile per `www.adobe.com`. Quando un browser carica la pagina, utilizza il _sistema DNS_ per cercare il nome di dominio collegato e risolverlo nell’indirizzo IP numerico corrispondente. Il recupero preventivo del DNS migliora le prestazioni delle pagine perché il nome di dominio viene risolto sempre in un indirizzo IP prima che il visitatore di un sito faccia clic sul collegamento o pulsante. Il processo di recupero preventivo del DNS è trasparente per gli utenti.

## Recupero preventivo del DNS e applicazioni Adobe CX Enterprise

Il recupero preventivo del DNS funziona automaticamente con i collegamenti statici integrati in una pagina. Ciò significa anche che il recupero preventivo del DNS non funziona con applicazioni e servizi [!UICONTROL CX Enterprise] diversi per i seguenti motivi:

* Ogni applicazione o servizio CX Enterprise genera le chiamate DNS in modo dinamico durante il caricamento della pagina.
* Il browser non può risolvere i nomi di dominio con indirizzi IP prima che vengano effettuate tali chiamate.

Tuttavia, è possibile implementare manualmente il recupero preventivo del DNS con le applicazioni CX Enterprise. Per farlo, aggiungi il tag HTML `<dns-prefetch>` alla sezione `<head>` del codice della pagina come mostrato di seguito. Se implementato correttamente, il recupero preventivo del DNS può contribuire a risparmiare alcuni millisecondi sul tempo di caricamento della pagina.

## Esempi di codici di recupero preventivo del DNS

Gli esempi seguenti mostrano come eseguire chiamate di recupero preventivo del DNS in diverse applicazioni e servizi [!DNL CX Enterprise]. Alcune chiamate di recupero preventivo richiedono il tuo ID organizzazione [!DNL Adobe] o i dati del server di registrazione. In questi esempi, il codice in *corsivo* rappresenta un segnaposto variabile. Il codice deve essere sostituito con il tuo ID partner [!DNL Adobe], il codice cliente o le informazioni sul server di registrazione, ecc.

* **Analytics:** `<link rel="dns-prefetch" href="//data.example.com">`.

  Aggiungi un tag separato per ogni nome DNS se utilizzi server di registrazione non sicuri e sicuri.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Servizio ID visitatore:** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [Recupero preventivo del DNS](https://www.chromium.org/developers/design-documents/dns-prefetching) in Chromium

