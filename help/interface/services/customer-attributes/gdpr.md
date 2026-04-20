---
title: Supporto di [!DNL Customer Attributes] per il regolamento generale sulla protezione dei dati
description: Scopri il supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
TQID: https://experienceleague.adobe.com/wU6Y5XK5Fs9-w7Jl7THXjturzTVrsB7eh7GdExsS2TQ
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a42153ba5a885509e7735e7407e38586fcabb0ad
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 82%

---

# Supporto di [!DNL Customer Attributes] per il regolamento generale sulla protezione dei dati

Questa pagina descrive come [!DNL Customer Attributes] supportino il regolamento generale sulla protezione dei dati (GDPR).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta o non intende sostituirsi a una consulenza legale. Consulta l’assistenza legale per ricevere consigli in merito al GDPR.

Il [regolamento generale sulla protezione dei dati](https://business.adobe.com/it/privacy/general-data-protection-regulation.html), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all&#39;interno dei confini dell&#39;Unione europea (Ue) il controllo dei loro dati personali. Semplifica inoltre il contesto normativo per le aziende internazionali. La presente legge si applica a tutte le aziende (titolari del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da soggetti all’interno dei confini dell’Ue nel momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe CX Enterprise agisce come responsabile del trattamento per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento dei dati, l’utente determina i dati personali che Adobe CX Enterprise tratta e archivia per suo conto.

In questo documento viene descritto come [!DNL Customer Attributes] supporti i diritti all’accesso e all’eliminazione dei dati degli interessati ai sensi del GDPR tramite l’API di Privacy Service di Adobe Experience Platform e l’interfaccia utente di Privacy Service.

Per maggiori informazioni sul significato del GDPR per la tua attività, consulta [Il GDPR e la tua attività](https://business.adobe.com/it/privacy/general-data-protection-regulation.html).

## Configurazione necessaria per inviare richieste per [!DNL Customer Attributes]

Per richiedere l’accesso e l’eliminazione dei dati per [!DNL Customer Attributes], è necessario:

1. Identificare quanto segue:

   * [ID organizzazione](../../administration/organizations.md)
   * ID alias dell&#39;origine dati CRS su cui desideri agire
   * ID CRM del profilo su cui desideri agire

   Il tuo [ID organizzazione](../../administration/organizations.md) è una stringa alfanumerica composta da 24 caratteri a cui segue @AdobeOrg. Per inviare richieste all’API per la privacy è necessario l’ID organizzazione. Se non ti è possibile individuare l’ID, contatta l’Assistenza clienti Adobe all’indirizzo `gdprsupport@adobe.com`.

1. In [!UICONTROL Privacy Service] è possibile inviare le richieste di accesso ed eliminazione a [!DNL Customer Attributes] e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON di [!DNL Customer Attributes]

&quot;company context&quot; (contesto dell&#39;azienda):

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*valore ID organizzazione IMS*>

&quot;users&quot; (utenti):

* &quot;key&quot;: &lt;*in genere il nome del cliente*>
* &quot;action&quot;: **accesso** (access) o **eliminazione** (delete)
* &quot;user IDs&quot; (ID utente):
   * &quot;namespace&quot;: &lt;*ID alias dell&#39;origine dati CRS*>
   * &quot;type&quot;: **integrationCode**
   * &quot;value&quot;: &lt;*ID CRM*>
* &quot;include&quot;: **CRS** (prodotto Adobe che si applica alla richiesta)
* &quot;regulation&quot;: **gdpr** (regolamento sulla privacy applicabile alla richiesta)

## Esempio di richiesta JSON

```json
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

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
