---
title: Supporto degli attributi del cliente per il regolamento generale sulla protezione dei dati
description: Supporto degli attributi del cliente per il regolamento generale sulla protezione dei dati
translation-type: tm+mt
source-git-commit: 4223f9260865756842ad43b99d2509908f4d6572
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Supporto degli attributi del cliente per il Regolamento generale sulla protezione dei dati

Questa pagina descrive come Attributi del cliente supporta il Regolamento generale sulla protezione dei dati (General Data Protection Regulation, GDPR).

>[!IMPORTANT]
>
>Il contenuto del presente documento non è un parere giuridico o un&#39;assistenza sostitutiva. Consulta il tuo consulente legale per ricevere consigli su GDPR.

Il Regolamento [](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html)generale sulla protezione dei dati, una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti) all’interno dei confini dell’Unione Europea (UE) il controllo dei loro dati personali. Semplifica inoltre il contesto normativo per le imprese internazionali. La presente legge si applica a tutte le imprese (responsabili del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da persone all&#39;interno dei confini dell&#39;UE al momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come un processore di dati per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento, puoi determinare i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In questo documento viene descritto come gli attributi [!UICONTROL del] cliente supportano i diritti di accesso e di eliminazione dei dati GDPR degli interessati tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente del servizio per la privacy.

Per maggiori informazioni sul significato del GDPR per la tua attività, consulta [GDPR e la sezione dedicata alle tue attività](https://www.adobe.com/it/privacy/general-data-protection-regulation.html).

## Configurazione necessaria per inviare richieste per gli attributi [!UICONTROL cliente]

Per richiedere l&#39;accesso e l&#39;eliminazione dei dati per gli attributi cliente, è necessario:

1. Identificate quanto segue:

   * ID organizzazione IMS
   * ID alias dell&#39;origine dati CRS su cui si desidera agire
   * ID CRM del profilo su cui vuoi agire
   Un ID organizzazione IMS è una stringa alfanumerica composta da 24 caratteri, con l’aggiunta di @AdobeOrg. Se il team marketing o l&#39;amministratore di sistema Adobe interno non conosce l&#39;ID organizzazione IMS dell&#39;azienda, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare le richieste all&#39;API per la privacy è necessario l&#39;ID organizzazione IMS.

1. In [!UICONTROL Privacy Service], puoi inviare le richieste di accesso ed eliminazione agli attributi del cliente e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON di attributi  cliente

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
