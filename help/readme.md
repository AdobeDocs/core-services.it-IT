---
source-git-commit: 58ccef353b492b1c2adfbb8c2471e1f92263e6e4
translation-type: ht

---
# Istruzioni

**Nota: questa pagina (o qualsiasi pagina readme.md) non sarà pubblicata nella documentazione del cliente**

## TOC

+ La pagina `TOC.md` nella directory principale della guida utente fornisce la struttura degli argomenti contenuti nella guida per questa soluzione.
+ Ogni guida utente avrà la sua pagina `TOC.md` univoca, in cui puoi ordinare le pagine o gli argomenti secondo le necessità.
+ La prima pagina di tutte le guide utente è `overview.md`.

## Guida utente

+ L’introduzione alla guida utente è denominata `overview.md`
+ Ogni argomento nella guida utente dispone di una directory distinta.
   + Se nella guida è presente un argomento denominato *Implementazione*, la directory corrispondente è `/implementation`
+ Tutte le risorse di immagini sono memorizzate in `/assets` nella directory principale della guida utente.
   + Tutte le immagini nella directory `/assets` saranno localizzate.
   + Tutte le immagini della directory `/no-localize` non vengono localizzate (c’è una sorpresa!). Questa può essere utilizzata per garantire nelle versioni locali che determinate risorse non siano riprodotte inutilmente.

## Metadati a livello guida utente

+ I metadati che descrivono la guida utente sono memorizzati in `TOC.md`. Ciò include:
   + product: nome del prodotto/funzionalità.
   + cloud: cloud a cui appartiene il prodotto.
   + audience: pubblico o archetipo al quale è destinata la guida.
   + user-guide: nome della guida utente.

## Metadati a livello di pagina

+ I metadati necessari per descrivere un documento sono memorizzati come parte di ogni singola pagina. Ciò include:
   + title: titolo della pagina.
   + description: descrizione della pagina.
   + seo-title: titolo SEO alternativo.
   + seo-description: titolo alternativo ai fini della SEO.
   + short-title: campo facoltativo.
   + index - yes/no: indica se la pagina verrà indicizzata dalla piattaforma di ricerca di Adobe.
   + translate - yes/no: indica se la pagina sarà localizzata.
   + version: utilizzato principalmente per AEM e Campaign, per indicare la versione del prodotto.
   + private-feature-pack: utilizzato principalmente per AEM.
   + beta: indica se il prodotto è nella versione beta.
   + redirect: può essere utilizzato per creare un riferimento a una nuova pagina.
   + doc-type: reference (predefinito)/troubleshooting/developer/tutorial/kb/whitepaper.

## Ulteriori informazioni

Per ulteriori istruzioni su pubblicazione, guide di stile, esempi e altre risorse, visita il [repository con la documentazione collaborativa](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
