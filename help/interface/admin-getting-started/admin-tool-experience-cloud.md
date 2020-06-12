---
description: Per visualizzare un elenco ordinabile e filtrabile di tutti gli utenti di Experience Cloud, scopri Admin Tool di Experience Cloud.
keywords: core services
seo-description: Per visualizzare un elenco ordinabile e filtrabile di tutti gli utenti di Experience Cloud, scopri Admin Tool di Experience Cloud.
seo-title: Visualizzare gli utenti e i dettagli utente di Experience Cloud
solution: Experience Cloud
title: 'Visualizzare gli utenti e i dettagli utente di Experience Cloud '
index: true
translation-type: ht
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e
workflow-type: ht
source-wordcount: '693'
ht-degree: 100%

---


# Visualizzare gli utenti di Experience Cloud all’interno di Admin Tool

Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti Experience Cloud e dei relativi dettagli nel nuovo Admin Tool. I dettagli utente includono l’accesso ai prodotti, i ruoli e le informazioni sull’ultimo accesso. **Nota:** la gestione di utenti e prodotti è configurata all’interno di [Admin Console](admin-getting-started.md).

1. Accedi a `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. Dalla home di Experience Cloud, fai clic su **[!UICONTROL Admin Tool.]**

   In alternativa, nell’URL della pagina principale puoi sostituire _home_ con _admin_.

   Viene visualizzata la pagina [!UICONTROL Users (Utenti)].

## Pagina Users (Utenti)

In questa pagina viene visualizzato l’elenco completo degli utenti con accesso a Experience Cloud all’interno della tua organizzazione. La pagina offre informazioni in merito al diritto alla soluzione all’ultimo accesso. Puoi inoltre eseguire ricerche, oltre a ordinare e filtrare le viste personalizzate dell’elenco di utenti.

![](assets/admin-tool-users.png)

| Elemento | Descrizione |
|---|---|
| [!UICONTROL Nome] | Il nome e il cognome dell’utente. Puoi ordinare questa colonna da A a Z e da Z a A. Per visualizzare ulteriori dettagli sull’utente, fai clic sul nome relativo. |
| [!UICONTROL E-mail] | L’indirizzo e-mail associato all’utente. La colonna può essere ordinata da A->Z e da Z->A. |
| [!UICONTROL ID Type (Tipo di ID)] | Il tipo di identità per l’account dell’utente. È possibile applicare un filtro per visualizzare tipi di ID specifici. Per ulteriori informazioni, consulta [Manage identity types (Gestisci tipi di identità)](https://helpx.adobe.com/it/enterprise/using/identity.html). |
| [!UICONTROL Soluzioni] | In questa sezione sono riepilogate le soluzioni Experience Cloud a cui l’utente può accedere. Per limitare l’elenco di utenti con accesso specifico alla soluzione puoi applicare i filtri. |
| [!UICONTROL Last Login (Ultimo accesso)] | Ora e data dell’accesso utente più recente a Experience Cloud. Questa colonna può essere ordinata in base a date ascendenti o discendenti. <br> **Importante:** a partire dal 13 gennaio 2020, gli ultimi dati di accesso dell’utente saranno conservati per 365 giorni. Queste informazioni si propongono di mostrare l’attuale attività all’interno di Experience Cloud e non costituiscono un consiglio a intervenire sugli account inattivi prima del 13 gennaio 2020. |

## Personalizzare la vista elenco degli utenti

Puoi eseguire ricerche, oltre a ordinare o filtrare le viste personalizzate dell’elenco di utenti.

* Puoi cercare gli utenti per nome o e-mail. Le ricerche corrispondono alla stringa di testo digitata.
* Ordina le colonne in base ai valori crescenti o decrescenti. L’operazione può essere eseguite nelle colonne [!UICONTROL Nome,] [!UICONTROL E-mail,] [!UICONTROL Last login (Ultimo accesso)].
* Per applicare più filtri agli utenti dell’elenco con criteri specifici, fai clic sull’icona **[!UICONTROL Filter By (Filtra per)]**. Quando vengono applicate più categorie di filtro, le ricerche contengono la soluzione `AND`ID TYPE `AND` del dominio e-mail.

| Elemento | Descrizione |
|---------|----------|
| Filtro [!UICONTROL Email Domain (Dominio e-mail)] | Per limitare i risultati a uno o più domini, cerca le stringhe di caratteri nella colonna E-mail. Per aggiungere più filtri, premi Invio dopo ciascun termine di ricerca. |
| Filtro [!UICONTROL ID Type (Tipo di ID)] | Scegli tra i tipi di ID disponibili. È possibile utilizzare più tipi di ID come filtro. |
| Filtro [!UICONTROL Soluzione] | Scegli tra le soluzioni disponibili. I filtri per più soluzioni cercano i risultati contenenti la soluzione 1 `OR` la soluzione 2. |

## View user details (Visualizza dettagli utente)

Per visualizzare i dettagli di un utente, nella pagina [!UICONTROL Utenti], seleziona l’e-mail dell’utente in questione.

![](assets/admin-tool-user-details.png)

La visualizzazione dettagliata di ciascun utente mostra dettagli importanti sull’accesso alla soluzione da parte dell’utente, sui ruoli di amministratore e di prodotto, oltre alle informazioni sull’ultimo accesso.

## Sezione About (Informazioni)

In questa sezione viene visualizzato un riepilogo dell’account utente, il quale include:

* Avatar dell’utente e badge dell’amministratore di sistema (laddove applicabile)
* Nome
* E-mail
* Nome utente (gli account Federated ID possono presentare nomi utente diversi dall’indirizzo e-mail)
* [ID Type (Tipo di ID)](https://helpx.adobe.com/it/enterprise/using/identity.html)
* Paese
* Last Login (Ultimo accesso)

## Solutions Summary (Riepilogo delle soluzioni)

In questa sezione viene visualizzato un riepilogo delle soluzioni Experience Cloud a cui l’utente può accedere, comprensivo del ruolo amministrativo del prodotto, se applicabile.

## Detailed Product Access List (Elenco dettagliato di accesso al prodotto)

In questa sezione viene visualizzato un elenco completo di tutti i profili di prodotto dell’utente in questione.

| Elemento | Descrizione |
|---------|----------|
| [!UICONTROL Prodotto] | Il nome associato al profilo di prodotto. |
| [!UICONTROL Istanza] | Il nome dell’istanza (ad esempio società di accesso o tenant) associata al prodotto e al profilo di prodotto. |
| [!UICONTROL Profilo di prodotto] | Nome univoco del profilo di prodotto. |
| [!UICONTROL Assigned by Group (Assegnato dal gruppo)] | Nome del gruppo di utenti che associa l’utente a un profilo di prodotto. I risultati vuoti indicano che l’utente è stato assegnato in modo diretto al profilo di prodotto, non tramite un gruppo. |
| [!UICONTROL Product Roles (Ruoli prodotto)] | Assegnazione del ruolo dell’utente all’interno del profilo di prodotto. Attualmente, queste informazioni sono valide solo per i profili di prodotto di Adobe Target. |
