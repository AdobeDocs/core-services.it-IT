---
title: 'Supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati '
description: Scopri come sono supportati gli attributi cliente per il Regolamento generale sulla protezione dei dati
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: 55c81003b94b7e033cddb6854b5c1f1c1ffa199c
workflow-type: ht
source-wordcount: '416'
ht-degree: 100%

---

# Supporto per gli attributi del cliente per il regolamento generale sulla protezione dei dati

Questa pagina descrive come la funzione [!UICONTROL Attributi del cliente] supporta il regolamento generale sulla protezione dei dati (RGPD).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta o non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al RGPD.

Il [regolamento generale sulla protezione dei dati](https://business.adobe.com/it/privacy/general-data-protection-regulation.html), una legge in vigore dal 25 maggio 2018, conferisce a tutte le persone (soggetti dei dati) all&#39;interno dei confini dell&#39;Unione europea (Ue) il controllo dei loro dati personali. Semplifica inoltre il contesto normativo per le aziende internazionali. La presente legge si applica a tutte le aziende (titolari del trattamento dei dati) che offrono beni o servizi, che controllano il comportamento o raccolgono dati personali da soggetti all&#39;interno dei confini dell&#39;Ue nel momento in cui i loro dati personali vengono trattati, indipendentemente dalla sede del titolare del trattamento.

Adobe Experience Cloud agisce come responsabile del trattamento per tutti i dati personali che riceve e archivia per conto dei propri clienti. In qualità di titolare del trattamento dei dati, puoi determinare i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In questo documento viene descritto come gli [!UICONTROL attributi del cliente] supportano i diritti all&#39;accesso e all&#39;eliminazione dei dati degli interessati ai sensi del RGPD tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente di Privacy Service.

Per maggiori informazioni sul significato del RGPD per la tua attività, consulta [RGPD e aziende](https://business.adobe.com/it/privacy/general-data-protection-regulation.html).

## Configurazione necessaria per inviare richieste per gli [!UICONTROL attributi del cliente]

Per richiedere l’accesso e l’eliminazione dei dati per [!UICONTROL Attributi del cliente], è necessario:

1. Identificare quanto segue:

   * [ID organizzazione](#organizations.md)
   * ID alias dell&#39;origine dati CRS su cui desideri agire
   * ID CRM del profilo su cui desideri agire

   Il tuo [ID organizzazione](#organizations.md) è una stringa alfanumerica composta da 24 caratteri a cui segue @AdobeOrg. Per inviare richieste all’API per la privacy è necessario l’ID organizzazione. Se non ti è possibile individuare l’ID, contatta l’Assistenza clienti Adobe all’indirizzo `gdprsupport@adobe.com`.

1. In [!UICONTROL Privacy Service], puoi inviare le richieste di accesso ed eliminazione agli attributi del cliente e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON di [!UICONTROL attributi del cliente]

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
