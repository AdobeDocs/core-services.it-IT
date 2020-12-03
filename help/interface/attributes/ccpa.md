---
title: Supporto per gli attributi del cliente per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California)
description: Supporto per gli attributi del cliente per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California)
translation-type: tm+mt
source-git-commit: 4223f9260865756842ad43b99d2509908f4d6572
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 100%

---


# Supporto per gli attributi del cliente per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California)

Questa pagina descrive il supporto per gli [!UICONTROL Attributi del cliente] per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al CCPA.

Il CCPA è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Esso garantisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate di “vendita” di informazioni personali a terzi.

In qualità di azienda, puoi determinare i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Experience Cloud fornisce supporto alla tua azienda per l&#39;adempimento dei suoi obblighi in virtù del CCPA applicabili all&#39;uso di prodotti e servizi Experience Cloud, compresa la gestione delle richieste di accesso ed eliminazione di informazioni personali.

In questo documento viene descritto come gli [!UICONTROL attributi del cliente] supportano i diritti all&#39;accesso e all&#39;eliminazione dei dati degli interessati ai sensi del CCPA tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente di Privacy Service.

Per ulteriori informazioni sui servizi di privacy Adobe per il CCPA, visita il [Centro per la privacy di Adobe](https://www.adobe.com/privacy/ccpa.html).

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

* &quot;regulation&quot;: **ccpa** (il regolamento sulla privacy applicabile alla richiesta)

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
