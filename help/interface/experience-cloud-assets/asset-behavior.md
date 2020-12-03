---
description: Regole per il comportamento delle cartelle condivise in caso di spostamento, eliminazione e ripristino delle stesse.
keywords: asset sharing;Creative Cloud;core services
seo-description: Regole per il comportamento delle cartelle condivise in caso di spostamento, eliminazione e ripristino delle stesse.
seo-title: Comportamento delle cartelle condivise
solution: Experience Cloud
title: Comportamento delle cartelle condivise
uuid: 86348401-f4b1-4efe-acd1-7e73a7030edf
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 25%

---


# Comportamento delle cartelle condivise

Regole per il comportamento delle cartelle condivise in caso di spostamento, eliminazione e ripristino delle stesse.

>[!NOTE]
>
>Le cartelle e le risorse condivise di Experience Cloud si riflettono sul desktop di Creative Cloud in una relazione 1:1. Se un utente di Experience Cloud modifica una cartella (elimina, aggiunge o rimuove condivisioni) l&#39;azione si riflette sul desktop e sul Web di Creative Cloud. Di conseguenza, se una cartella non è condivisa, la cartella e le risorse vengono eliminate dal computer locale. Una volta rimossa la condivisione, la cartella e il relativo contenuto vengono spostati nel cestino del computer locale, dove è possibile ripristinarli manualmente nel computer locale.

## Cartella non condivisa in una cartella condivisa {#section_A9BAC1A244A246A984AC62660E61E0C0}

Spostate una cartella non condivisa in una cartella condivisa:

![](assets/01_assets_move.png)

**Risultato**: Entrambe le cartelle vengono condivise.

## Cartella condivisa in una cartella non condivisa {#section_8BA83001DCEC4CF084B980C4A660F59A}

Sposta una cartella condivisa in una cartella non condivisa.

![](assets/02_assets_move.png)

**Risultato**: la cartella non condivisa rimane non condivisa. La cartella condivisa rimane condivisa.

## Contenuto di una cartella non condivisa in una cartella condivisa {#section_2941ED0DC52E4573AC1AB4C22313DD8E}

Sposta il contenuto di una cartella non condivisa in una cartella condivisa.

![](assets/03_assets_move.png)

**Risultato:** Il contenuto ora è condiviso e tutti i collaboratori possono visualizzarlo. L&#39;archiviazione aumenta in base alla dimensione del contenuto.

## Contenuto condiviso archiviato ed eliminato {#section_5210D5F4943A44D0BA675D8EB4EAE20F}

Archiviate o eliminate il contenuto presente in una cartella condivisa.

![](assets/04_assets_move.png)

**Risultato:** Il contenuto viene archiviato per il proprietario della cartella. I collaboratori che non possiedono il contenuto non possono più accedervi.

## Contenuto di proprietà condiviso in una cartella non condivisa {#section_3810A364B67E4B8C9CA244BC52BF91BB}

Spostate il contenuto da una cartella condivisa di proprietà in una cartella non condivisa.

![](assets/05_assets_move.png)

**Risultato:** Il contenuto ora non è condiviso. I collaboratori della cartella condivisa non hanno più accesso al contenuto.

## Contenuto non di proprietà in una cartella non condivisa {#section_310766EBF0DC4C0BB4AB3E8A4DAEBE07}

Sposta il contenuto da una cartella condivisa di proprietà di qualcun altro in una cartella non condivisa.

![](assets/06_assets_move.png)

**Risultato:** Il contenuto viene visualizzato nella cartella non condivisa e rimosso dalla cartella condivisa. I collaboratori della cartella condivisa non hanno più accesso al contenuto. Il contenuto viene archiviato per il proprietario della cartella condivisa.

I proprietari e gli editor possono spostare contenuti che non possiedono, ma i visualizzatori no. Se i proprietari e gli editor spostano il contenuto, non è disponibile in una cartella condivisa per alcun utente.

## Cartella di proprietà archiviata o eliminata {#section_B314B13512A5409C87C49DFDB7602E14}

Archiviate (via Web) o eliminate (via desktop) una cartella condivisa di proprietà.

![](assets/07_assets_move.png)

**Risultato:** La cartella viene rimossa dalla condivisione e quindi archiviata. I collaboratori non hanno più accesso alla cartella.

## Cartella condivisa in un’altra cartella condivisa {#section_0A3F203D048D4D1586E9850DC92C51E9}

Sposta una cartella condivisa di proprietà in un&#39;altra cartella condivisa di proprietà o di proprietà.

![](assets/09_assets_move.png)

**Risultato:** Spostando la cartella nella cartella 2, questa viene condivisa con i nuovi collaboratori.

## Contenuto condiviso in un’altra cartella condivisa {#section_69F6C312792A4CD2831BD14A340F850E}

Sposta il contenuto di una cartella condivisa in un&#39;altra cartella condivisa.

![](assets/11_assets_move.png)

**Risultato:** Il contenuto viene visualizzato nella cartella 2 e ora viene condiviso con i nuovi collaboratori. Il contenuto viene rimosso dalla cartella 1 e il proprietario lo visualizza come archiviato, mentre gli altri collaboratori non possono più accedervi.

## Contenuto ripristinato dall’archivio {#section_DEA990B3581741F89FBB81D18C2AB449}

Ripristinate il contenuto da un archivio che apparteneva a una cartella condivisa. Il contenuto era di proprietà al momento dell&#39;archiviazione.

![](assets/12_assets_move.png)

**Risultato:** Il contenuto viene ripristinato nella cartella condivisa e tutti i collaboratori possono accedervi nuovamente. Se la cartella condivisa non esiste più, il contenuto viene inserito in una copia non condivisa delle cartelle principali originali.
