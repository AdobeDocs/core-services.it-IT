---
title: Indirizzi IP utilizzati da Experience Cloud
description: Se il firewall dell’organizzazione blocca gli indirizzi IP provenienti da Adobe, utilizza questo elenco per aggiornare le impostazioni del firewall.
exl-id: 1fca8d3b-ae8b-4095-96ef-d165f912b4c6
source-git-commit: faa9b8067a85f86cc0b559bdeeaed80df2339c7d
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 11%

---

# Indirizzi IP utilizzati da Experience Cloud

Alcune configurazioni del firewall bloccano gli indirizzi IP provenienti dai server di raccolta dati o dai server responsabili dell’accesso ai dati di Adobe. Puoi utilizzare questo elenco di intervalli per modificare le impostazioni del firewall dell’organizzazione per consentire l’accesso e l’invio di dati dall’interno dell’organizzazione. Questa pagina include sia i sistemi in entrata (come la raccolta dati) che i sistemi in uscita (come i feed di dati in Adobe Analytics) utilizzati da Adobe.

>[!IMPORTANT]
>
>Adobe fa del suo meglio per mantenere aggiornato questo documento, ma non può garantire che l’elenco degli intervalli IP rimanga lo stesso. Tra i possibili cambiamenti vi sono la crescita e l&#39;espansione dell&#39;attività, un registro Internet richiede modifiche allo spazio di indirizzi IP di Adobe o un provider di servizi Internet cessa di funzionare.

Oltre ai blocchi di indirizzi IP elencati di seguito, i singoli prodotti Adobe Experience Cloud dispongono di indirizzi IP propri che utilizzano:

* [Adobe Analytics](https://experienceleague.adobe.com/it/docs/analytics/technotes/ip-addresses)
* [Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/technotes/ip-addresses)
* [Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo#step-allowlist-marketo-ips)

## Tutti i blocchi di indirizzi IP di Adobe

La tabella seguente descrive tutti gli indirizzi IP di proprietà di Adobe. Questa tabella include tutti gli uffici dipendenti Adobe e i data center gestiti da Adobe a livello globale. Non sono inclusi i servizi ospitati su cloud pubblici.

| Blocco IP (notazione CIDR) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.240.0/22` |

{style="table-layout:auto"}

## Raccolta dati di Adobe Experience Cloud e blocchi di indirizzi IP FTP

Se la tua organizzazione preferisce consentire intervalli di indirizzi IP specifici, puoi fare riferimento alla tabella seguente. Include:

* Server di raccolta dati per tutti i prodotti Experience Cloud
* Server FTP per tutti i prodotti Experience Cloud

Tutti gli intervalli IP in questa sezione sono inclusi nella tabella precedente.

| Posizione | Intervallo IP (notazione CIDR) |
| --- | --- |
| Australia | `63.140.55.0/24` |
| Australia | `63.140.56.0/23` |
| California | `63.140.32.0/23` |
| California | `63.140.34.0/24` |
| Francia | `63.140.62.0/23` |
| India | `66.117.20.0/24` |
| India | `66.117.22.0/23` |
| Giappone | `130.248.169.0/23` |
| Giappone | `63.140.50.0/23` |
| Giappone | `66.117.31.0/24` |
| Londra | `66.235.156.0/24` |
| Londra | `185.34.188.0/22` |
| Londra | `130.248.152.0/22` |
| Londra | `130.248.244.0/23` |
| Oregon | `66.235.132.0/22` |
| Oregon | `130.248.130.0/23` |
| Oregon | `130.248.150.0/24` |
| Oregon | `130.248.160.0/21` |
| Oregon | `192.243.242.0/24` |
| Singapore | `130.248.170.0/23` |
| Singapore | `130.248.240.0/24` |
| Singapore | `63.140.44.0/22` |
| Singapore | `63.140.48.0/23` |
| Singapore | `66.117.30.0/24` |
| Singapore | `172.82.240.8/29` |
| Singapore | `172.82.240.88/29` |
| Virginia | `63.140.38.0/23` |
| Virginia | `63.140.54.0/24` |
| Virginia | `67.202.5.244` |

{style="table-layout:auto"}

Adobe Experience Cloud supporta anche IPv6 in capacità limitata. Questi blocchi IP servono a scopi di raccolta dati simili a quelli delle controparti IPv4 di cui sopra, ma non includono l’FTP.

| Posizione | Host |
| --- | --- |
| Australia | `2406:da1c:406:1a00::/56` |
| Australia | `2406:da1c:ce5:b400::/56` |
| California | `2600:1f1c:366:d900::/56` |
| Francia | `2a05:d012:706:d000::/56` |
| India | `2406:da1a:f34:6a00::/56` |
| Irlanda | `2a05:d018:309:600::/56` |
| Giappone | `2406:da14:b07:ab00::/56` |
| Oregon | `2600:1f14:1eb:7d00::/56` |
| Oregon | `2600:1f14:9d3:2b00::/56` |
| Singapore | `2406:da18:6e8:1e00::/56` |
| Virginia | `2600:1f18:1a20:e800::/56` |
| Virginia | `2600:1f18:4fd:6000::/56` |
| Virginia | `2600:1f18:b00:e100::/56` |
| Virginia | `2600:1f18:d1f:bd00::/56` |

>[!TIP]
>
>Le connessioni FTP per le funzioni di esportazione di Adobe Analytics (tra cui Data Warehouse e feed di dati) provengono solo da indirizzi IPv4 nelle sedi di Londra, Oregon e Singapore.
