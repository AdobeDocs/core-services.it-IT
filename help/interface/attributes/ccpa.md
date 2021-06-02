---
title: 'Supporto per gli attributi del cliente per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California) '
description: Scopri il supporto relativo agli attributi del cliente per il California Consumer Privacy Act (legge sulla privacy dei consumatori della California)
feature: Attributi del cliente
topic: Amministrazione
role: Administrator
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: b968ca3a2751ab9af27e86595447f84f3cb20d68
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 66%

---

# Supporto per gli attributi del cliente per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California)

Questa pagina descrive il supporto per gli [!UICONTROL Attributi del cliente] per il California Consumer Privacy Act (accordo sulla privacy dei consumatori della California).

>[!IMPORTANT]
>
>Il contenuto di questo documento non rappresenta e non intende sostituirsi a una consulenza legale. Consulta l&#39;assistenza legale per ricevere consigli in merito al CCPA.

Il CCPA è la nuova legge sulla privacy della California, in vigore dal 1° gennaio 2020. Esso garantisce ai residenti della California nuovi diritti in merito alle loro informazioni personali e impone responsabilità in materia di protezione dei dati a determinate entità che conducono attività commerciali in California. Il CCPA garantisce ai consumatori il diritto di accedere ai propri dati personali e di cancellarli e il diritto di rinunciare a determinate attività che possono essere considerate come &quot;vendita&quot; di informazioni personali a terzi.

In qualità di azienda, puoi determinare i dati personali elaborati e archiviati da Adobe Experience Cloud per tuo conto.

In qualità di fornitore di servizi, Adobe Experience Cloud fornisce supporto alla tua azienda per adempiere ai suoi obblighi in virtù del CCPA applicabili all&#39;utilizzo di prodotti e servizi Experience Cloud. Questo supporto include la gestione delle richieste di accesso e cancellazione delle informazioni personali.

Questo documento descrive come [!UICONTROL Attributi del cliente] supporta i diritti di accesso e cancellazione dei dati degli interessati ai sensi del CCPA tramite l’API di Adobe Experience Platform Privacy Service e l’interfaccia utente di Privacy Service.

Per ulteriori informazioni sui servizi di privacy Adobe per il CCPA, visita il [Centro per la privacy di Adobe](https://www.adobe.com/privacy/ccpa.html).

## Configurazione necessaria per inviare richieste per gli [!UICONTROL attributi del cliente]

Per richiedere l&#39;accesso e l&#39;eliminazione dei dati per [!UICONTROL Attributi del cliente], devi:

1. Identificare quanto segue:

   * ID organizzazione IMS
   * ID alias dell&#39;origine dati CRS su cui desideri agire
   * ID CRM del profilo su cui desideri agire

   Un ID organizzazione IMS è una stringa alfanumerica composta da 24 caratteri, con l&#39;aggiunta di @AdobeOrg. Se il team marketing o l&#39;amministratore di sistema Adobe interno non conosce l&#39;ID organizzazione IMS dell&#39;azienda, contatta l&#39;Assistenza clienti Adobe all&#39;indirizzo gdprsupport@adobe.com. Per inviare richieste all’API Privacy è necessario l’ID organizzazione IMS.

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
