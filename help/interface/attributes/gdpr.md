---
title: Supporto degli attributi del cliente per il regolamento generale sulla protezione dei dati
description: Supporto degli attributi del cliente per il regolamento generale sulla protezione dei dati
translation-type: tm+mt
source-git-commit: 3a86aed0794c3e35cc028e5bfde5dafcb2285fc8
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 5%

---


# Supporto degli attributi del cliente per il regolamento generale sulla protezione dei dati


>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consulenza in merito al Regolamento generale sulla protezione dei dati.

Il Regolamento [](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html) generale sulla protezione dei dati (GDPR), una legge in vigore dal 25 maggio 2018, conferisce a tutti gli individui (soggetti) entro i confini dell&#39;Unione Europea (UE) il controllo dei loro dati personali e semplifica il contesto normativo per le imprese internazionali. La presente legge si applica a tutte le imprese (responsabili del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da persone all&#39;interno dei confini dell&#39;UE al momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come un processore di dati per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento, puoi determinare i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In questo documento viene descritto in che modo gli attributi del cliente supportano i diritti di accesso e di eliminazione dei dati GDPR degli interessati tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente del servizio per la privacy.

Per maggiori informazioni sul significato del GDPR per la tua attività, consulta [GDPR e la sezione dedicata alle tue attività](https://www.adobe.com/it/privacy/general-data-protection-regulation.html).

## Configurazione richiesta per l&#39;invio di richieste per gli attributi del cliente

Per richiedere l&#39;accesso e l&#39;eliminazione dei dati per gli attributi cliente, dovrai:

1. Identificate quanto segue:

* ID organizzazione IMS
* ID alias dell&#39;origine dati CRS su cui si desidera agire
* ID CRM del profilo su cui vuoi agire

Un ID organizzazione IMS è una stringa alfanumerica composta da 24 caratteri, con l’aggiunta di @AdobeOrg. Se il team marketing o l&#39;amministratore di sistema Adobe interno non conosce l&#39;ID organizzazione IMS dell&#39;azienda, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare le richieste all&#39;API per la privacy è necessario l&#39;ID organizzazione IMS.

2. Utilizzare l&#39;interfaccia utente del servizio Privacy per inviare ed eliminare richieste di accesso agli attributi del cliente e per verificare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON degli attributi del cliente

&quot;contesto aziendale&quot;:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*valore* ID organizzazione IMS>

&quot;users&quot;:

* &quot;key&quot;: &lt;*in genere il nome del cliente*>

* &quot;action&quot;: **accesso** o **eliminazione**

* &quot;ID utente&quot;:

   * &quot;namespace&quot;: &lt;ID *alias dell&#39;origine* dati CRS>

   * &quot;type&quot;: **integrationCode**

   * &quot;value&quot;: &lt;ID ** CRM>

* &quot;include&quot;: **CRS** (prodotto Adobe che si applica alla richiesta)

* &quot;regolamento&quot;: **gdpr** (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta JSON

```
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## Campi dati restituiti per le richieste di accesso

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
