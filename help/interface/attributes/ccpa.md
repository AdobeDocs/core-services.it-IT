---
title: Supporto degli attributi del cliente per il California Consumer Privacy Act
description: Supporto degli attributi del cliente per il California Consumer Privacy Act
translation-type: tm+mt
source-git-commit: 8709449909ce4fbd441d77fb4bbfb0b7758e805d
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 4%

---


# Supporto degli attributi del cliente per il California Consumer Privacy Act

Questa pagina descrive il supporto degli attributi del [!UICONTROL cliente per il California Consumer Privacy Act (CCPA)] .

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta il tuo consulente legale per ricevere consigli in merito alla (CCPA).

L’APP è la nuova legge sulla privacy californiana, in vigore dal 1° gennaio 2020. L&#39;CCPA fornisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone loro responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. L&#39;APP garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli, nonché il diritto di non partecipare a determinate attività che possono essere considerate come &quot;vendita&quot; a terzi di informazioni personali.

In qualità di azienda, determinerai i dati personali che Adobe Experience Cloud elabora e archivia per tuo conto.

In qualità di fornitore di servizi, Adobe Experience Cloud fornisce supporto alla tua azienda per adempiere ai suoi obblighi in virtù dell&#39;accordo di associazione per i servizi e i prodotti Experience Cloud applicabili all&#39;uso di prodotti e servizi Experience Cloud, compresa la gestione delle richieste di accesso ed eliminazione di informazioni personali.

Questo documento descrive come gli attributi [!UICONTROL del] cliente supportano l&#39;accesso e i diritti di eliminazione dei dati CCPA degli interessati tramite l&#39;API Adobe Experience Platform Privacy Service e l&#39;interfaccia utente del servizio per la privacy.

Per ulteriori informazioni sui servizi Adobe Privacy per CCPA, visitare il Centro [per la privacy di](https://www.adobe.com/privacy/ccpa.html)Adobe.

## Configurazione necessaria per inviare richieste per gli attributi [!UICONTROL cliente]

Per richiedere l&#39;accesso e l&#39;eliminazione di dati per gli attributi cliente, dovrete:

1. Identificate quanto segue:

   * ID organizzazione IMS
   * ID alias dell&#39;origine dati CRS su cui si desidera agire
   * ID CRM del profilo su cui vuoi agire
   Un ID organizzazione IMS è una stringa alfanumerica composta da 24 caratteri, con l’aggiunta di @AdobeOrg. Se il team marketing o l&#39;amministratore di sistema Adobe interno non conosce l&#39;ID organizzazione IMS dell&#39;azienda, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare le richieste all&#39;API per la privacy è necessario l&#39;ID organizzazione IMS.

1. In [!UICONTROL Privacy Service], puoi inviare le richieste di accesso ed eliminazione agli attributi del cliente e controllare lo stato delle richieste esistenti.

## Valori campo obbligatori nelle richieste JSON degli attributi  cliente

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

* &quot;regolamento&quot;: **ccpa** (che è il regolamento sulla privacy applicabile alla richiesta)

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
