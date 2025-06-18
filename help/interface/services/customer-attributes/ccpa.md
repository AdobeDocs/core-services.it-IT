---
title: Supporto degli attributi del cliente per il California Consumer Privacy Act
description: Scopri il supporto degli attributi del cliente per il California Consumer Privacy Act
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 57%

---

# Supporto degli attributi del cliente per il California Consumer Privacy Act

Questa pagina descrive il supporto di [!UICONTROL attributi cliente] per il California Consumer Privacy Act (CCPA).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al CCPA.

Il CCPA è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Esso garantisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, puoi determinare quali sono i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Experience Cloud fornisce supporto alla tua azienda per l’adempimento dei suoi obblighi in virtù dei CCPA applicabili all’uso di prodotti e servizi Experience Cloud. Questo supporto include la gestione delle richieste di accesso e la cancellazione delle informazioni personali.

In questo documento viene descritto come [!UICONTROL attributi cliente] supporta i diritti all&#39;accesso e all&#39;eliminazione dei dati degli interessati ai sensi del CCPA tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente di Privacy Service.

Per ulteriori informazioni sui servizi di privacy Adobe per il CCPA, visita il [Centro per la privacy di Adobe](https://www.adobe.com/privacy/ccpa.html).

## Configurazione necessaria per inviare richieste per [!UICONTROL attributi del cliente]

Per richiedere l&#39;accesso e l&#39;eliminazione dei dati per [!UICONTROL attributi del cliente], è necessario:

1. Identificare quanto segue:

   * [ID organizzazione](../../administration/organizations.md)
   * ID alias dell&#39;origine dati CRS su cui desideri agire
   * ID CRM del profilo su cui desideri agire

   L’ID organizzazione è una stringa alfanumerica composta da 24 caratteri a cui segue @AdobeOrg. Per inviare richieste all’API per la privacy è necessario l’ID organizzazione. Se non ti è possibile individuare l’ID, contatta l’Assistenza clienti Adobe all’indirizzo `gdprsupport@adobe.com`.

1. In [!UICONTROL Privacy Service] è possibile inviare le richieste di accesso ed eliminazione agli attributi del cliente e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori in [!UICONTROL attributi cliente] richieste JSON

&quot;company context&quot; (contesto dell&#39;azienda):

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*valore ID organizzazione*>

&quot;users&quot; (utenti):

* &quot;key&quot;: &lt;*in genere il nome del cliente*>
* &quot;action&quot;: **accesso** (access) o **eliminazione** (delete)
* &quot;user IDs&quot; (ID utente):
   * &quot;namespace&quot;: &lt;*ID alias dell&#39;origine dati CRS*>
   * &quot;type&quot;: **integrationCode**
   * &quot;value&quot;: &lt;*ID CRM*>
* &quot;include&quot;: **CRS** (prodotto Adobe che si applica alla richiesta)
* &quot;regulation&quot;: **ccpa** (il regolamento sulla privacy applicabile alla richiesta)

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
