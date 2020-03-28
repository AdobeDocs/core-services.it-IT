---
description: Panoramica della gestione delle offerte, su come accedervi e su come concedere le autorizzazioni agli utenti.
seo-description: Panoramica della gestione delle offerte, su come accedervi e su come concedere le autorizzazioni agli utenti.
seo-title: Introduzione
title: Introduzione
uuid: 28d83606-ee36-4bbf-b52d-bbe8b097f6d5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Gestione delle offerte Adobe {#section_07CBD4C01F4049A5A19781737D2DCD35}

[!UICONTROL Gestione] offerta offre la creazione, la gestione e il processo decisionale delle offerte su tutti i canali in Experience Cloud. Funge da catalogo centrale delle offerte in cui è possibile associare le regole di idoneità e più parti di contenuto a ciascun _oggetto dell&#39;offerta._ Potete pubblicare tali offerte su canali e posizioni diversi e fornire l&#39;offerta migliore per ciascun cliente a ogni interazione. Queste funzioni consentono di offrire costantemente la migliore offerta ai clienti in modo coerente e coordinato attraverso la loro esperienza.

I vantaggi includono:

* Miglioramento delle prestazioni delle campagne e-mail grazie alla distribuzione di offerte più personalizzate nelle e-mail.
* Flusso di lavoro migliorato: Invece di creare più consegne o campagne, i team di marketing possono migliorare il flusso di lavoro creando un&#39;unica consegna e variare le offerte in diverse parti del modello.
* Consente di creare, gestire e approvare offerte al di fuori del flusso di lavoro della campagna e-mail Adobe Campaign Standard.
* Controllo del numero di volte in cui un&#39;offerta viene visualizzata tra campagne e clienti di e-mail.

## Accesso alle offerte {#task_DEB6F6A4B6E04E15AD3E1817D700688E}

Scoprite come accedere a Gestione offerte.

1. Contattate Adobe per il provisioning.

   Un&#39;organizzazione Experience Cloud deve avere un&#39;istanza di Campaign Standard. Adobe può inoltre abilitare una funzione in Campaign che consente di creare attività di offerta all&#39;interno dei messaggi e-mail.

1. Dal menu di navigazione di Experience Cloud, fai clic sul selettore della soluzione, quindi su **[!UICONTROL Offerte]**.

   ![](assets/access-offers.png)

   Per accedere alle offerte in Campaign Standard, fate clic sull&#39;icona **[!UICONTROL Offerte]** all&#39;interno di un modello e-mail.

   ![](assets/campaign-add-offer.png)

   Dopo aver visualizzato entrambi questi elementi in Marketing Cloud e nell&#39;account Adobe Campaign, è stata configurata l&#39;installazione con le funzionalità necessarie per iniziare.

## Users and Permissions {#concept_81F0ABB07ACC49E099EDCD87AA0436E1}

Gli amministratori possono aggiungere utenti alla gestione delle  offerte in Admin Console. Un invito e-mail viene inviato al nuovo utente con le istruzioni per accedere al prodotto. Dopo l&#39;aggiunta di un utente, potete regolare le relative autorizzazioni, consentendo loro di accedere a diverse funzionalità in [!UICONTROL Gestione]offerta.

Per ulteriori informazioni sull&#39;uso di Admin Console, consulta la documentazione [di](https://helpx.adobe.com/enterprise/help/aedash.html)HelpX Admin Console.

In Campaign, gli utenti standard hanno automaticamente il diritto di incorporare le attività delle offerte in un modello e-mail.

>[!NOTE]
>
>Per la versione beta, non sono disponibili autorizzazioni. Ogni utente aggiunto a Offerte avrà accesso completo a tutte le funzionalità di [!UICONTROL Gestione]offerte.

## Creare un profilo di prodotto per Gestione offerte

Un profilo di prodotto è un insieme di autorizzazioni che possono essere combinate per creare un ruolo utente all&#39;interno di un prodotto. I profili di prodotto devono essere creati e gli utenti o i gruppi devono quindi essere loro assegnati.

1. Passa ad Adobe [Admin Console](https://adminconsole.adobe.com/).

1. Fate clic sul processo (**[!UICONTROL ad esempio Offerte]**).

1. Nella pagina [!UICONTROL Profili] di prodotto, fate clic su **[!UICONTROL Nuovo profilo]**.

1. Digita un nome e una descrizione per il profilo di prodotto, quindi fai clic su **[!UICONTROL Fine]**.

1. Fai clic su **[!UICONTROL Salva]**.

### Autorizzazioni - Definizioni

Una descrizione delle autorizzazioni di gestione [!UICONTROL delle] offerte disponibili per i profili di prodotto in [!UICONTROL Admin Console].

| Elemento | Descrizione |
|--- |--- |
| Creare e modificare le offerte | Consente agli utenti di creare e modificare le offerte in [!UICONTROL Gestione]offerte. Se un utente dispone di questa autorizzazione ma non dell’autorizzazione _Approva offerte_ , può solo creare un’offerta e inviarla per l’approvazione. Non può essere utilizzato in un&#39;attività di offerta finché non viene approvata. |
| Eliminare le offerte | Consente agli utenti di eliminare le offerte. |
| Approva offerte | Consente agli utenti di approvare un&#39;offerta. Gli utenti con questa autorizzazione visualizzeranno una notifica quando accedono a Gestione offerte, se le offerte richiedono l&#39;approvazione. Se un utente dispone sia di questa autorizzazione che dell’autorizzazione per _creare e modificare le offerte_ , può creare e approvare le offerte in un unico flusso di lavoro. |
| Offerte archivio | Consente agli utenti di archiviare un&#39;offerta. |
| Creare etichette | Consente agli utenti di creare etichette, sia nella scheda Etichetta che in linea nella schermata di creazione delle offerte. Senza questa autorizzazione, un utente potrà selezionare le offerte già create solo al momento della creazione di un&#39;offerta. |
| Modificare le etichette | Consente agli utenti di modificare le etichette nella scheda Etichette. |
| Elimina etichette | Consente agli utenti di eliminare le etichette nella scheda Etichette. |
| Creazione di posizionamenti | Consente agli utenti di creare posizionamenti nella scheda Posizionamenti. |
| Modificare i posizionamenti | Consente agli utenti di modificare i posizionamenti nella scheda Posizionamenti. |
| Eliminare i posizionamenti | Consente agli utenti di eliminare i posizionamenti nella scheda Posizionamenti. **Nota:** È possibile eliminare solo i posizionamenti non utilizzati in un&#39;attività dell&#39;offerta. |