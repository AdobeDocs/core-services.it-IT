---
description: Scopri  Strumento di amministrazione Experience Cloud per visualizzare un elenco ordinabile e filtrabile di tutti gli utenti e i criteri  Experience Cloud.
keywords: core services
seo-description: Scopri  Strumento di amministrazione Experience Cloud per visualizzare un elenco ordinabile e filtrabile di tutti gli utenti e i criteri  Experience Cloud.
seo-title: Visualizzare gli utenti e i dettagli utente di Experience Cloud
solution: Experience Cloud
title: 'Visualizzare gli utenti e i dettagli utente di Experience Cloud '
index: true
translation-type: tm+mt
source-git-commit: 82b0b42d8b06388e396bf2959503fe484c8b3a66
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 51%

---


# Visualizzare  utenti e criteri di Experience Cloud in Admin Tool

Gli amministratori possono visualizzare un elenco ordinabile e filtrabile di tutti gli utenti e i criteri  Experience Cloud con i dettagli in Admin Tool. I dettagli utente includono l’accesso ai prodotti, i ruoli e le informazioni sull’ultimo accesso. I dettagli dei criteri includono l&#39;utente, il gruppo, lo sviluppatore, l&#39;integrazione e l&#39;elenco di amministratori di un criterio (profilo di prodotto), nonché le autorizzazioni e le informazioni dettagliate sulle risorse per il criterio.

>[!NOTE]
>
>User and product management is configured in the [Admin Console](admin-getting-started.md).

1. Accedi a `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. In Accesso [!UICONTROL rapido], fai clic su **[!UICONTROL Admin Tool.]**

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

## Informazioni sulla sezione

In questa sezione viene visualizzato un riepilogo dell’account utente, il quale include:

* Avatar dell’utente e badge dell’amministratore di sistema (laddove applicabile)
* Nome
* E-mail
* Nome utente (gli account Federated ID possono presentare nomi utente diversi dall’indirizzo e-mail)
* [ID Type (Tipo di ID)](https://helpx.adobe.com/it/enterprise/using/identity.html)
* Paese
* Last Login (Ultimo accesso)

## Riepilogo delle soluzioni

In questa sezione viene visualizzato un riepilogo delle soluzioni Experience Cloud a cui l’utente può accedere, comprensivo del ruolo amministrativo del prodotto, se applicabile.

## Elenco dettagliato di accesso ai prodotti

In questa sezione viene visualizzato un elenco completo di tutti i profili di prodotto dell’utente in questione.

| Elemento | Descrizione |
|---------|----------|
| [!UICONTROL Prodotto] | Il nome associato al profilo di prodotto. |
| [!UICONTROL Istanza] | Il nome dell’istanza (ad esempio società di accesso o tenant) associata al prodotto e al profilo di prodotto. |
| [!UICONTROL Profilo di prodotto] | Nome univoco del profilo di prodotto. |
| [!UICONTROL Assigned by Group (Assegnato dal gruppo)] | Nome del gruppo di utenti che associa l’utente a un profilo di prodotto. I risultati vuoti indicano che l’utente è stato assegnato in modo diretto al profilo di prodotto, non tramite un gruppo. |
| [!UICONTROL Product Roles (Ruoli prodotto)] | Assegnazione del ruolo dell’utente all’interno del profilo di prodotto. Attualmente, queste informazioni sono valide solo per i profili di prodotto di Adobe Target. |

## Pagina Criteri

In questa pagina viene visualizzato l&#39;elenco completo dei criteri di  Experience Cloud dell&#39;organizzazione. Fornisce informazioni su prodotti, istanze, utenti e sviluppatori. Potete cercare, ordinare e filtrare le visualizzazioni personalizzate dell&#39;elenco dei criteri.

![](assets/admin-tool-policies.png)

| Elemento | Descrizione |
|---|---|
| [!UICONTROL Profilo di prodotto] | Nome del profilo di prodotto. La colonna può essere ordinata A->Z, Z->A. Fate clic sul nome di un profilo di prodotto per visualizzare ulteriori dettagli sul criterio. |
| [!UICONTROL Prodotto] | Il prodotto associato al profilo di prodotto. La colonna può essere ordinata da A->Z e da Z->A. |
| [!UICONTROL Istanza] | L&#39;istanza (ad esempio tenant o società di accesso) associata al profilo di prodotto. I prodotti che non hanno istanze univoche o tenant visualizzeranno un &quot; - &quot; per il valore. La colonna può essere ordinata da A->Z e da Z->A. |
| [!UICONTROL Numero di utenti] | Numero univoco di utenti associati al profilo di prodotto, inclusa l&#39;assegnazione diretta e l&#39;assegnazione del gruppo. Le colonne possono essere ordinate in base al più piccolo, al più grande o al più piccolo. |
| [!UICONTROL Numero di sviluppatori] | Conteggio dei ruoli sviluppatore associati al profilo di prodotto. Le colonne possono essere ordinate in base al più piccolo, al più grande o al più piccolo. |

## Personalizzare la visualizzazione elenco criteri

È possibile cercare, ordinare o filtrare le colonne per personalizzare l&#39;elenco dei criteri.

* Cerca profili di prodotto per nome. Le ricerche corrispondono alla stringa di testo digitata.
* Ordina le colonne in base ai valori crescenti o decrescenti. Questo vale per profilo [!UICONTROL prodotto,] [!UICONTROL prodotto,] [!UICONTROL istanza,] [!UICONTROL numero di utenti,] e [!UICONTROL numero di sviluppatori,] colonne.
* Click the **[!UICONTROL Filter By]** icon to apply multiple filters to list product profiles with specific criteria. Quando vengono applicate più categorie di filtri, le ricerche contengono i gruppi associati alla `AND` soluzione di `AND` istanza.

| Elemento | Descrizione |
|---------|----------|
| [!UICONTROL Filtro istanza] | Cercare stringhe di caratteri nella colonna dell&#39;istanza per limitare i risultati a una o più istanze. Aggiungete più filtri premendo Invio dopo ogni termine di ricerca. |
| Filtro [!UICONTROL Soluzione] | Scegli tra le soluzioni disponibili. I filtri per più soluzioni cercano i risultati contenenti la soluzione 1 `OR` la soluzione 2. |

## Visualizza dettagli criteri

Nella pagina [!UICONTROL Criteri] , per visualizzare i dettagli di un criterio, fate clic sul nome del profilo di prodotto.

![](assets/admin-tool-policy-detail.png)

Una visualizzazione dettagliata di ciascun profilo di prodotto mostra dettagli importanti sui soggetti del profilo di prodotto (utenti, gruppi e così via). Vengono inoltre visualizzate le autorizzazioni e le risorse abilitate dal profilo di prodotto.

I dettagli del profilo di prodotto possono essere esportati in file CSV. L’opzione [!UICONTROL Esporta CSV] genera due file CSV:

* Dettagli Oggetto (Utenti, Gruppi Di Utenti, Sviluppatori, Integrazioni, Amministratori)
* Autorizzazioni e risorse

## Sezione Riepilogo

In questa sezione viene visualizzato un riepilogo del profilo di prodotto che include:

* Nome profilo di prodotto
* Numero di utenti
* Numero di sviluppatori
* Numero di integrazioni
* Prodotti associati
* Istanza

## Elenco dettagliato oggetto

In questa sezione viene visualizzato un elenco completo di tutti gli utenti, i gruppi di utenti, gli sviluppatori, le integrazioni e gli amministratori assegnati al profilo di prodotto.

| Tab | Descrizione |
|---------|----------|
| [!UICONTROL Utenti] | Elenco di utenti inclusi nel profilo di prodotto. L&#39;associazione del gruppo di utenti verrà visualizzata nella colonna [!UICONTROL Assegnato per gruppo] . |
| [!UICONTROL Gruppi di utenti] | Elenco di gruppi di utenti associati al profilo di prodotto. |
| [!UICONTROL Sviluppatori] | Elenco di sviluppatori associati al profilo di prodotto. |
| [!UICONTROL Integrazioni] | Elenco di integrazioni associate al profilo di prodotto. |
| [!UICONTROL Amministratori] | Elenco di amministratori associati al profilo di prodotto. |

## Elenchi dettagliati di autorizzazioni e risorse

In questa sezione viene visualizzato un elenco completo delle autorizzazioni e delle risorse disponibili per il profilo di prodotto. Le autorizzazioni e le risorse incluse nel profilo di prodotto sono state contrassegnate con un ✔ &quot;. Gli elenchi di autorizzazioni e risorse sono stati organizzati in schede e colonne per facilitarne la visualizzazione. Le schede e le colonne visualizzano l&#39;elenco delle sezioni applicabili al prodotto corrente.
