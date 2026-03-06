---
description: Scopri come impostare certificati protetti da utilizzare con i cookie di prime parti di Adobe Experience Cloud.
solution: Experience Cloud,Analytics
title: Programma di certificazione gestito da Adobe
index: true
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
TQID: https://experienceleague.adobe.com/LWbjh-jXKmY6mcl047uzA1ZkhZlAmeNpt9JRg3Ynt9E
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: e992d880-33bc-4949-a648-aa7d410276cd
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 5354e3c8a48184315ca4eaa8c8de1d12493cc227
workflow-type: tm+mt
source-wordcount: 1106
ht-degree: 3%

---

# Programma di certificazione gestito da Adobe

Il programma di certificazione gestito da Adobe è il processo consigliato per la configurazione dei certificati di prime parti necessari per un’implementazione CNAME. Una volta configurato, il programma è completamente automatizzato. I certificati vengono rinnovati in modo tempestivo, in modo da non influire sulla raccolta dei dati a causa di certificati scaduti. Il programma è gratuito per i primi 100 CNAME.

Se attualmente gestisci i tuoi certificati, sei responsabile dell’acquisto, della manutenzione e della fornitura di un certificato ad Adobe per l’utilizzo dei cookie di prime parti. Contatta l’Assistenza clienti di Adobe per informazioni sulla migrazione al programma di certificazione gestito da Adobe.

## Implementazione

Per implementare un nuovo certificato per la raccolta dati di prime parti, effettua le seguenti operazioni:

1. Scarica e compila il [modulo di richiesta per dominio di prime parti](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Apri un ticket con l’Assistenza clienti di Adobe per richiedere la configurazione della raccolta dati di prime parti nel programma di certificazione gestito da Adobe.
1. Quando ricevi il ticket, il rappresentante di Adobe ti fornisce un record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. Ad esempio, il nome host `data.example.com` punta a `hiodsibxvip01.data.adobedc.net`.
1. Quando il record CNAME è presente sui server dell’organizzazione, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di raccolta dati di Adobe.

## Convalida dell’inoltro nome host

Una volta installato il certificato, Adobe può utilizzare uno dei seguenti metodi per verificare che funzioni.

+++**Convalida browser**

Puoi utilizzare qualsiasi browser per verificare che un certificato sia installato correttamente. Digita il tuo CNAME con `_check` come percorso nella barra degli indirizzi. Ad esempio:

`data.example.com/_check`

Se tutto funziona, nel browser viene visualizzato `SUCCESS`. Se il certificato non è installato correttamente, viene visualizzato un avviso di protezione.

+++

+++**Riga di comando (`curl`)**

Nella maggior parte dei sistemi operativi moderni è già installato [`curl`](https://curl.se).

Digitare quanto segue nella riga di comando:

```sh
curl data.example.com/_check
```

Se tutto funziona correttamente, la console restituisce `SUCCESS`.

>[!TIP]
>
>È possibile utilizzare il flag `-k` per disabilitare l&#39;avviso di protezione per facilitare la risoluzione dei problemi.

+++

+++**Riga di comando (`nslookup`)**

Digitare quanto segue nella riga di comando:

```sh
nslookup data.example.com
```

Se tutto funziona correttamente, vengono restituiti i server di raccolta dati di Adobe:

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: smetrics.example.com
```

+++

## Aggiorna il codice di implementazione

Dopo aver verificato il corretto funzionamento del certificato, puoi aggiornare l’implementazione di Adobe in modo da utilizzare questi valori.

* **Estensione tag Web SDK**: aggiorna il campo [[!UICONTROL Edge domain]](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) durante la configurazione dell&#39;estensione.
* **Web SDK (lega)**: aggiornare la proprietà [`edgeDomain`](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/edgedomain) nel comando [`configure`](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/overview).
* **Estensione Adobe Analytics**: aggiorna il campo [[!UICONTROL SSL Tracking Server]](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/analytics/overview) durante la configurazione dell&#39;estensione. Assicurati inoltre di aver installato l&#39;estensione tag [Visitor ID Service](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/id-service/overview). Per ulteriori informazioni, consulta [Identificazione del visitatore tramite l&#39;estensione tag Analytics](https://experienceleague.adobe.com/it/docs/analytics/implementation/id/analytics-extension).
* **AppMeasurement**: aggiorna la variabile di configurazione [`trackingServerSecure`](https://experienceleague.adobe.com/it/docs/analytics/implementation/vars/config-vars/trackingserversecure). Assicurati inoltre di avere implementato il [Servizio ID visitatori](https://experienceleague.adobe.com/it/docs/id-service/using/home) tramite `VisitorAPI.js`. Per ulteriori informazioni, consulta [Identificazione del visitatore tramite AppMeasurement](https://experienceleague.adobe.com/it/docs/analytics/implementation/id/analytics-extension).

Se il sito utilizza più metodi di implementazione e non è possibile aggiornarli tutti contemporaneamente, è consigliabile configurare un periodo di tolleranza. Consulta le [considerazioni sulla migrazione al servizio ID visitatori](https://experienceleague.adobe.com/it/docs/analytics/implementation/id/migration) per ulteriori passaggi su come evitare che i visitatori vengano conteggiati come nuovi visitatori nel tuo sito.

## Manutenzione e rinnovi

Trenta giorni prima della scadenza del certificato di prima parte, Adobe verifica se il CNAME è ancora valido e in uso. In tal caso, Adobe presuppone che tu voglia continuare a utilizzare il servizio e rinnova automaticamente il certificato per tuo conto.

>[!IMPORTANT]
>
>Se il record CNAME della tua organizzazione viene rimosso o non è più mappato al nome host protetto di Adobe fornito, Adobe non può rinnovare il certificato. La voce nel sistema di Adobe è contrassegnata per la rimozione senza ulteriori comunicazioni.

## Domande frequenti

+++Il processo è sicuro?

Sì.  Il programma di certificazione gestito da Adobe è più sicuro dell’organizzazione che fornisce un certificato ad Adobe. Nessun certificato o chiave privata passa di mano al di fuori di Adobe e dell’autorità di certificazione emittente.

+++

+++In che modo Adobe può acquistare un certificato per il nostro dominio?

Il certificato può essere acquistato solo dopo aver puntato il nome host specificato su un nome host di proprietà di Adobe. In sostanza, deleghi questo nome host ad Adobe e consenti ad Adobe di acquistare il certificato per tuo conto.

+++

+++Posso richiedere la revoca del certificato?

Sì.  In qualità di proprietario del dominio, hai il diritto di richiedere la revoca del certificato. Per avviare questo processo, contatta l’Assistenza clienti di Adobe.

+++

+++Quale tipo di crittografia viene utilizzato?

Adobe collabora con DigiCert per rilasciare un certificato SHA-2.

+++

+++Il programma comporta costi aggiuntivi?

No. Adobe offre questo servizio a tutti i clienti Adobe Experience Cloud senza costi aggiuntivi.

+++

+++Quali livelli di sicurezza con crittografia offre Adobe?

Adobe offre due livelli di sicurezza crittografati per soddisfare le diverse esigenze dei clienti in materia di sicurezza nella raccolta dati di prime parti. Questi livelli determinano gli algoritmi di crittografia supportati per le connessioni HTTPS con i server Adobe. Adobe rivede e aggiorna regolarmente il set di algoritmi supportati in base alle procedure di sicurezza correnti. Se desideri modificare le impostazioni di protezione crittografata, contatta l’Assistenza clienti.

* **Standard** richiede la crittografia TLS 1.2 o successiva e almeno a 128 bit. È progettato per garantire la massima compatibilità con i dispositivi, mantenendo al contempo la crittografia sicura.
* Il livello di protezione crittografata **Elevato** richiede TLS 1.2 o versione successiva e rimuove il supporto per le crittografie più deboli. È progettato per i clienti che desiderano la crittografia più potente e non si preoccupano del supporto di dispositivi meno recenti.

I seguenti client non sono in grado di connettersi con la protezione crittografata impostata su **Elevata**:

* Windows 8.1 e versioni precedenti (ultimo aggiornamento: 2018)
* Windows Phone 8.1 e versioni precedenti (ultimo aggiornamento: 2016)
* OS X 10.10 e versioni precedenti (ultimo aggiornamento: 2017)
* iOS 8.4 e versioni precedenti (ultimo aggiornamento: 2015)

+++

+++Quali tipi di certificato HTTPS sono supportati?

Adobe supporta sia i tipi di certificato RSA che ECC per soddisfare le diverse esigenze dei clienti. I certificati RSA sono più ampiamente supportati per i client, ma i certificati ECC utilizzano una minore elaborazione sia sul lato server che su quello client. Per i certificati gestiti da Adobe, vengono forniti sia RSA che ECC. Per i certificati gestiti dal cliente, è necessario RSA e si consiglia ECC. I client moderni supportano sia RSA che ECC. I client seguenti in genere supportano solo i certificati RSA:

* Windows Vista e versioni precedenti (ultimo aggiornamento: 2012)
* Windows Phone 8.0 e versioni precedenti (ultimo aggiornamento: 2014)
* OS X 10.8 e versioni precedenti (ultimo aggiornamento: 2013)
* iOS 5.1 e versioni precedenti (ultimo aggiornamento: 2012)
* Android 4.3 e versioni precedenti (ultimo aggiornamento: 2013)

+++

+++Posso gestire i miei certificati?

Sì.  Tuttavia, se gestisci i certificati, sei responsabile del rinnovo dei certificati e della loro fornitura ad Adobe ogni volta che li rinnovi. Questo processo è meno sicuro e può causare la perdita di dati se l’organizzazione dimentica di rinnovare un certificato in tempo. Adobe consiglia di utilizzare il programma di certificazione gestito anziché gestire autonomamente i certificati, in particolare a causa della riduzione della durata massima dei certificati TLS. Per ulteriori informazioni, vedere [6.3.1 Public Key Archive](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods) in CA/Browser Forum Server Certificate Baseline Requirements.
+++

