---
description: Scopri come impostare certificati protetti da utilizzare con i cookie di prime parti di Adobe Experience Cloud.
solution: Experience Cloud,Analytics
title: Programma di certificazione gestito da Adobe
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 4%

---

# Programma di certificazione gestito da Adobe

Il programma di certificazione gestito da Adobe è il processo consigliato per la configurazione dei certificati di prime parti necessari per un’implementazione CNAME. Una volta configurato, il programma è completamente automatizzato. I certificati vengono rinnovati in modo tempestivo, in modo da non influire sulla raccolta dei dati a causa di certificati scaduti. Il programma è gratuito per i primi 100 CNAME.

Se attualmente gestisci i tuoi certificati, sei responsabile dell’acquisto, della manutenzione e della fornitura di un certificato di Adobe per l’utilizzo dei cookie di prime parti. Contatta l’Assistenza clienti Adobe per informazioni sulla migrazione al programma di certificazione gestito da Adobe.

## Implementazione

Per implementare un nuovo certificato per la raccolta dati di prime parti, effettua le seguenti operazioni:

1. Scarica e compila il [modulo di richiesta per dominio di prime parti](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. Apri un ticket con l’Assistenza clienti Adobe per richiedere la configurazione della raccolta dati di prime parti nel programma di certificazione gestito da Adobe.

1. Quando ricevi il ticket, il rappresentante dell’Adobe ti fornisce un record CNAME. Questi record devono essere configurati sul server DNS della tua azienda per consentire ad Adobe di acquistare il certificato per conto tuo. Ad esempio, il nome host `data.example.com` punta a `hiodsibxvip01.data.adobedc.net`.

1. Quando il record CNAME è presente sui server dell’organizzazione, Adobe collabora con DigiCert per acquistare e installare un certificato sui server di raccolta dati di Adobe.

## Convalida dell’inoltro nome host {#validate}

Adobe Dopo aver installato il certificato, puoi utilizzare uno dei seguenti metodi per verificare che funzioni.

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

## Aggiorna il codice di implementazione {#update}

Dopo aver verificato il corretto funzionamento del certificato, puoi aggiornare l’implementazione di Adobe in modo da utilizzare questi valori.

* Per le implementazioni Adobe Analytics AppMeasurement, aggiornare la variabile di configurazione [`trackingServer`](https://experienceleague.adobe.com/it/docs/analytics/implementation/vars/config-vars/trackingserver). Se hai un&#39;implementazione esistente, consulta [Migrazione visitatori](https://experienceleague.adobe.com/it/docs/analytics/technotes/visitor-migration) per ulteriori passaggi su come evitare che i visitatori esistenti vengano conteggiati come nuovi visitatori.
* Per le implementazioni Web SDK, aggiornare la proprietà [`edgeDomain`](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/edgedomain) all&#39;interno del comando [`configure`](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/commands/configure/overview).

## Manutenzione e rinnovi

Trenta giorni prima della scadenza del certificato di prima parte, Adobe verifica se il CNAME è ancora valido e in uso. In tal caso, Adobe presuppone che tu voglia continuare a utilizzare il servizio e rinnova automaticamente il certificato per tuo conto.

>[!IMPORTANT]
>
>Se il record CNAME della tua organizzazione viene rimosso o non è più mappato al nome host protetto dell’Adobe fornito, Adobe non può rinnovare il certificato. La voce nell&#39;Adobe è contrassegnata per la rimozione senza ulteriore comunicazione.

## Domande frequenti

+++Il processo è sicuro?

Sì.  Il programma di certificazione gestito da Adobe è più sicuro dell’organizzazione che fornisce all’Adobe un certificato. Nessun certificato o chiave privata passa di mano al di fuori di Adobe e dell’autorità di certificazione emittente.

+++

+++In che modo Adobe può acquistare un certificato per il nostro dominio?

Il certificato può essere acquistato solo dopo aver puntato il nome host specificato su un nome host di proprietà di un Adobe. In sostanza, puoi delegare questo nome host ad Adobe e consentire ad Adobe di acquistare il certificato per tuo conto.

+++

+++Posso richiedere la revoca del certificato?

Sì.  In qualità di proprietario del dominio, hai il diritto di richiedere la revoca del certificato. Per avviare questa procedura, contatta l’Assistenza clienti Adobe.

+++

+++Quale tipo di crittografia viene utilizzato?

Adobe funziona con DigiCert per rilasciare un certificato SHA-2.

+++

+++Il programma comporta costi aggiuntivi?

No. Adobe offre questo servizio a tutti i clienti Adobe Experience Cloud senza costi aggiuntivi.

+++

+++Quali livelli di protezione crittografata offre Adobe?

Adobe offre due livelli di sicurezza crittografati per soddisfare le diverse esigenze dei clienti in materia di sicurezza nella raccolta dati di prime parti. Questi livelli determinano gli algoritmi di crittografia supportati per le connessioni HTTPS con i server Adobe. Adobe rivede e aggiorna regolarmente il set di algoritmi supportati in base alle procedure di sicurezza correnti. Se desideri modificare le impostazioni di protezione crittografata, contatta l’Assistenza clienti.

* **Standard** richiede la crittografia TLS 1.2 o successiva e almeno a 128 bit. È progettato per garantire la massima compatibilità con i dispositivi, mantenendo al contempo la crittografia sicura.
* Il livello di protezione crittografata **Elevato** richiede TLS 1.2 o versione successiva e rimuove il supporto per le crittografie più deboli. È progettato per i clienti che desiderano la crittografia più potente e non si preoccupano del supporto di dispositivi meno recenti.

I seguenti client non sono in grado di connettersi con la protezione crittografata impostata su **Elevata**:

* Windows 8.1 e versioni precedenti (ultimo aggiornamento: 2018)
* Windows Phone 8.1 e versioni precedenti (ultimo aggiornamento: 2016)
* OS X 10.10 e versioni precedenti (ultimo aggiornamento: 2017)
* iOS 8.4 e versioni precedenti (ultimo aggiornamento: 2015)

+++

+++Quali tipi di certificati HTTPS sono supportati?

Adobe supporta sia i tipi di certificato RSA che ECC per soddisfare le diverse esigenze dei clienti. I certificati RSA sono più ampiamente supportati per i client, ma i certificati ECC utilizzano una minore elaborazione sia sul lato server che su quello client. Ad Adobe, vengono forniti i certificati gestiti RSA e ECC. Per i certificati gestiti dal cliente, è necessario RSA e si consiglia ECC. I client moderni supportano sia RSA che ECC. I client seguenti in genere supportano solo i certificati RSA:

* Windows Vista e versioni precedenti (ultimo aggiornamento: 2012)
* Windows Phone 8.0 e versioni precedenti (ultimo aggiornamento: 2014)
* OS X 10.8 e versioni precedenti (ultimo aggiornamento: 2013)
* iOS 5.1 e versioni precedenti (ultimo aggiornamento: 2012)
* Android 4.3 e versioni precedenti (ultimo aggiornamento: 2013)

+++
