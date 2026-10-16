---
title: Certificati gestiti dal cliente
description: Scopri quando utilizzare un certificato gestito dal cliente per la raccolta dati di prime parti e le responsabilità della tua organizzazione per il rinnovo.
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---
# Certificati gestiti dal cliente

Con un certificato gestito dal cliente, l’organizzazione ottiene il certificato per il nome host della raccolta dati di prime parti e lo fornisce ad Adobe. Adobe ospita il certificato sui propri server di raccolta dati. La tua organizzazione è responsabile del rinnovo del certificato e della fornitura di ogni certificato rinnovato ad Adobe prima della scadenza del certificato corrente.

>[!TIP]
>
>Adobe consiglia il [programma di certificazione gestito da Adobe](adobe-managed-cert.md) per la maggior parte delle implementazioni di prime parti. È più sicuro e rinnova automaticamente i certificati. Utilizza un certificato gestito dal cliente solo se richiesto dall’organizzazione.

## Quando utilizzare un certificato gestito dal cliente

* **Indirizzi la raccolta dati tramite una rete CDN con origine di prime parti**: il [programma di certificazione gestito da Adobe](adobe-managed-cert.md) non supporta le implementazioni della rete CDN. Consulta [Configurare una rete CDN con origine di prime parti](cdn.md#first-party-origin).
* **I criteri di sicurezza richiedono il controllo diretto del certificato**: ad esempio, l&#39;organizzazione deve essere in grado di revocare il certificato tramite la propria autorità di certificazione, anziché richiedere la revoca tramite l&#39;Assistenza clienti Adobe.
* **L&#39;organizzazione richiede un&#39;autorità di certificazione o un tipo di certificato specifico**: il programma di certificazione gestito da Adobe utilizza i certificati rilasciati da DigiCert.

## Confrontare i metodi dei certificati

| | Certificato gestito da Adobe | Certificato gestito dal cliente |
| --- | --- | --- |
| **Chi ottiene il certificato** | Adobe, tramite DigiCert | La tua organizzazione, attraverso un’autorità di certificazione commerciale di tua scelta |
| **Rinnovi** | Adobe rinnova automaticamente il certificato | La tua organizzazione rinnova il certificato e lo fornisce ad Adobe prima di ogni scadenza |
| **Tipi di certificato** | Adobe fornisce certificati RSA e ECC | RSA è obbligatorio; ECC è consigliato |
| **Supportato con CDN** | No | Sì, come origine di prima parte |

## Configurare un certificato gestito dal cliente

1. Contatta l’Assistenza clienti di Adobe per richiedere la raccolta dati di prime parti con un certificato gestito dal cliente. Includi il nome host di prime parti, ad esempio `data.example.com`. Se la tua organizzazione ha requisiti di residenza dei dati o conformità, specifica il tipo di [RDC](rdc.md) desiderato nella richiesta.
1. L’Assistenza clienti di Adobe fornisce una richiesta di firma del certificato (CSR, Certificate Signing Request) per il tuo nome host. Adobe genera e mantiene la chiave privata, in modo che la tua organizzazione non la gestisca mai. Adobe richiede un certificato RSA e consiglia un certificato ECC. Ogni tipo di certificato richiede una propria CSR, quindi se desideri un certificato ECC, chiedi all’Assistenza clienti di Adobe di fornirti una CSR ECC.
1. Invia ogni CSR all’autorità di certificazione commerciale desiderata per ottenere un certificato firmato. I servizi certificati gratuiti non sono supportati. Fornisci i certificati rilasciati ad Adobe come indicato dall’Assistenza clienti.
1. Una volta installato il certificato, Adobe indirizza il traffico per il nome host ad Adobe:
   * **Senza CDN**: aggiorna i record DNS della tua organizzazione come indicato dall&#39;Assistenza clienti di Adobe.
   * **Con una rete CDN**: imposta l&#39;origine della rete CDN sul nome host di prime parti. Consulta [Configurare una rete CDN con origine di prime parti](cdn.md#first-party-origin).
1. Se l&#39;implementazione non invia già i dati a questo nome host, [aggiorna l&#39;implementazione](collection-domain.md#update-implementation).

## Rinnovare il certificato {#renewals}

La tua organizzazione è responsabile del rinnovo del certificato e della fornitura del certificato rinnovato all’Assistenza clienti di Adobe prima della scadenza del certificato corrente.

Se il certificato sui server Adobe scade, i browser e le reti CDN rifiutano le connessioni al nome host e i dati di tali richieste andranno persi. Una rete CDN può eliminare questi dati senza inviare alcuna notifica.

La durata massima dei certificati è in calo, il che rende i rinnovi più frequenti. Per ulteriori informazioni, vedere [6.3.2 Periodi operativi del certificato e periodi di utilizzo della coppia di chiavi](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods) nella sezione Requisiti della linea di base del certificato del server del forum CA/browser. Per evitare vuoti nella raccolta dei dati:

* Monitora la data di scadenza di ogni certificato fornito ad Adobe.
* Assegna un proprietario per i rinnovi e documenta il processo di rinnovo in modo che continui attraverso le modifiche al personale.

Adobe sta attualmente esplorando un processo di rinnovo del certificato self-service.

## Interrompi l’utilizzo di un certificato gestito dal cliente

* **Per passare al programma di certificazione gestito da Adobe**: contatta l&#39;Assistenza clienti di Adobe. Il programma di certificazione gestito da Adobe richiede che il nome host punti direttamente ad Adobe, non a una rete CDN.
* **Per interrompere l&#39;utilizzo del nome host di prime parti**: aggiorna tutte le implementazioni che utilizzano il nome host, quindi contatta l&#39;Assistenza clienti di Adobe per rimuovere il certificato dai server Adobe.
* **Per passare a una rete CDN con origine di terze parti**: vedere [Spostare un&#39;implementazione di prime parti esistente in una rete CDN](cdn.md#migrate).
