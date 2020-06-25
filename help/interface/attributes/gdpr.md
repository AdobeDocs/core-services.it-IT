---
title: Supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati
description: Supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati
translation-type: ht
source-git-commit: 4223f9260865756842ad43b99d2509908f4d6572
workflow-type: ht
source-wordcount: '430'
ht-degree: 100%

---


# Supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati

Questa pagina descrive come gli attributi del cliente supportano il regolamento generale sulla protezione dei dati (RGPD).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta o non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al RGPD.

Il [regolamento generale sulla protezione dei dati](https://www.adobe.com/it/privacy/general-data-protection-regulation/what-is-gdpr.html), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all&#39;interno dei confini dell&#39;Unione europea (Ue) il controllo dei loro dati personali. Semplifica inoltre il contesto normativo per le aziende internazionali. La presente legge si applica a tutte le aziende (titolari del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da soggetti all&#39;interno dei confini dell&#39;Ue nel momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come responsabile del trattamento per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento dei dati, puoi determinare i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In questo documento viene descritto come gli [!UICONTROL attributi del cliente] supportano i diritti all&#39;accesso e all&#39;eliminazione dei dati degli interessati ai sensi del RGPD tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente di Privacy Service.

Per maggiori informazioni sul significato del RGPD per la tua attività, consulta [RGPD e aziende](https://www.adobe.com/it/privacy/general-data-protection-regulation.html).

## Configurazione necessaria per inviare richieste per gli [!UICONTROL attributi del cliente]

Per richiedere l&#39;accesso e l&#39;eliminazione dei dati per gli [!UICONTROL attributi del cliente], è necessario:

1. Identificare quanto segue:

   * ID organizzazione IMS
   * ID alias dell&#39;origine dati CRS su cui desideri agire
   * ID CRM del profilo su cui desideri agire

   Un ID organizzazione IMS è una stringa alfanumerica composta da 24 caratteri, con l&#39;aggiunta di @AdobeOrg. Se il team marketing o l&#39;amministratore di sistema Adobe interno non conosce l&#39;ID organizzazione IMS dell&#39;azienda, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare richieste all&#39;API per la privacy è necessario l&#39;ID organizzazione IMS.

1. In [!UICONTROL Privacy Service], puoi inviare le richieste di accesso ed eliminazione agli attributi del cliente e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON di [!UICONTROL attributi del cliente]

&quot;company context&quot; (contesto dell&#39;azienda):

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*valore ID organizzazione IMS*>

&quot;users&quot; (utenti):

* &quot;key&quot;: &lt;*in genere il nome del cliente*>

* &quot;action&quot;: **accesso** o **eliminazione**

* &quot;user IDs&quot; (ID utente):

   * &quot;namespace&quot;: &lt;*ID alias dell&#39;origine dati CRS*>

   * &quot;type&quot;: **integrationCode**

   * &quot;value&quot;: &lt;*ID CRM*>

* &quot;include&quot;: **CRS** (prodotto Adobe che si applica alla richiesta)

* &quot;regulation&quot;: **gdpr** (regolamento sulla privacy applicabile alla richiesta)

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
