---
description: Scopri le regole sul comportamento delle cartelle condivise quando vengono spostate, eliminate e ripristinate in CX Enterprise.
keywords: condivisione di risorse;Creative Cloud;servizi principali
solution: Experience Cloud
title: Comportamento delle cartelle condivise
uuid: 86348401-f4b1-4efe-acd1-7e73a7030edf
feature: Assets
topic: Administration
role: Admin
level: Experienced
exl-id: 5ddcb2f0-b491-466d-b357-aeacbfcf0b8e
TQID: https://experienceleague.adobe.com/sRgVt31HAxmjTMmMB0Kfs5fYEXKDjDu73hhAgfixu4o
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 627
ht-degree: 90%

---

# Comportamento delle cartelle condivise

Regole per il comportamento delle cartelle condivise in caso di spostamento, eliminazione e ripristino delle stesse.

>[!NOTE]
>
>Le cartelle e le risorse condivise di CX Enterprise si riflettono sul desktop di Creative Cloud in una relazione 1:1. Se un utente di CX Enterprise modifica una cartella (elimina, aggiunge o rimuove condivisioni), l’azione si riflette sul desktop e sul Web di Creative Cloud. Di conseguenza, se una cartella non è più condivisa, la cartella e le relative risorse vengono eliminate dal computer locale. Una volta rimossa la condivisione, la cartella e il suo contenuto vengono spostati nel cestino del computer locale, dal quale è possibile ripristinarli manualmente in locale.

## Cartella non condivisa in una cartella condivisa

Sposti una cartella non condivisa in una cartella condivisa:

![Cartella non condivisa in una cartella condivisa](../../assets/01_assets_move.png)

**Risultato**: entrambe le cartelle vengono condivise.

## Cartella condivisa in una cartella non condivisa

Sposti una cartella condivisa in una cartella non condivisa.

![Cartella condivisa in una cartella non condivisa](../../assets/02_assets_move.png)

**Risultato**: la cartella non condivisa rimane non condivisa. La cartella condivisa rimane condivisa.

## Contenuto di una cartella non condivisa in una cartella condivisa

Sposti il contenuto di una cartella non condivisa in una cartella condivisa.

![Contenuto di una cartella non condivisa in una cartella condivisa](../../assets/03_assets_move.png)

**Risultato:** il contenuto ora è condiviso e tutti i collaboratori possono visualizzarlo. Lo spazio di archiviazione usato aumenta in base alla dimensione del contenuto.

## Contenuto condiviso archiviato ed eliminato

Archivi o elimini il contenuto di una cartella condivisa.

![Contenuto condiviso archiviato ed eliminato](../../assets/04_assets_move.png)

**Risultato:** il contenuto viene archiviato per il proprietario della cartella. I collaboratori che non possiedono il contenuto non potranno più accedervi.

## Contenuto di proprietà condiviso in una cartella non condivisa

Sposti il contenuto da una cartella condivisa di tua proprietà a una cartella non condivisa.

![Contenuto di proprietà condiviso in una cartella non condivisa](../../assets/05_assets_move.png)

**Risultato:** il contenuto non è più condiviso. I collaboratori della cartella condivisa non hanno più accesso al contenuto.

## Contenuto non di proprietà in una cartella non condivisa

Sposti il contenuto da una cartella condivisa di proprietà di un altro utente a una cartella non condivisa.

![Contenuto non di proprietà in una cartella non condivisa](../../assets/06_assets_move.png)

**Risultato:** il contenuto viene visualizzato nella cartella non condivisa e rimosso dalla cartella condivisa. I collaboratori della cartella condivisa non hanno più accesso al contenuto. Il contenuto viene archiviato per il proprietario della cartella condivisa.

I proprietari e gli editor possono spostare contenuti di cui non sono proprietari; gli utenti con sole autorizzazioni di visualizzazione non possono effettuare tali spostamenti. Se i proprietari e gli editor spostano i contenuti, questi non saranno disponibili in una cartella condivisa per alcun utente.

## Cartella di proprietà archiviata o eliminata

Archivi (via web) o elimini (via desktop) una cartella condivisa di tua proprietà.

![Cartella di proprietà archiviata o eliminata](../../assets/07_assets_move.png)

**Risultato:** la cartella non è più condivisa e viene quindi archiviata. I collaboratori non hanno più accesso alla cartella.

## Cartella condivisa in un’altra cartella condivisa

Sposti una cartella condivisa di tua proprietà in un’altra cartella condivisa, che sia di tua proprietà o meno.

![Cartella condivisa in un’altra cartella condivisa](../../assets/09_assets_move.png)

**Risultato:** quando la cartella viene spostata nella seconda cartella, viene condivisa con i nuovi collaboratori.

## Contenuto condiviso in un’altra cartella condivisa

Sposti il contenuto da una cartella condivisa a un’altra cartella condivisa.

![Contenuto condiviso in un’altra cartella condivisa](../../assets/11_assets_move.png)

**Risultato:** il contenuto viene visualizzato nella seconda cartella e ora è condiviso con i nuovi collaboratori. Il contenuto viene rimosso dalla prima cartella e il proprietario lo visualizza come archiviato; gli altri collaboratori non possono più accedervi.

## Contenuto ripristinato dall’archivio

Ripristini il contenuto da un archivio che apparteneva a una cartella condivisa. Il contenuto era di tua proprietà al momento dell’archiviazione.

![Contenuto ripristinato dall’archivio](../../assets/12_assets_move.png)

**Risultato:** il contenuto viene ripristinato nella cartella condivisa e tutti i collaboratori possono di nuovo accedervi. Se la cartella condivisa non esiste più, il contenuto viene inserito in una copia non condivisa delle cartelle principali originali.
