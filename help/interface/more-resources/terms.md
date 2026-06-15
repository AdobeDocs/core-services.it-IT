---
description: Scopri le differenze tra i termini di interfaccia e prodotto di Adobe tra CX Enterprise, le soluzioni Experience Cloud, Creative Cloud, Experience League e altre esperienze di supporto.
solution: Experience Cloud
title: Terminologia
feature-set: Experience Cloud Services
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 5%

---

# Terminologia

<!--
TQID: https://experienceleague.adobe.com/6wm7HcuAbaV1iV3AgN55dY5WR---BnMM7lJgN0HZDsk
-->

Usa questa tabella quando la stessa parola viene visualizzata in diverse esperienze Adobe (CX Enterprise, app di marketing, app di progettazione o siti di supporto). Non è un glossario completo. Per informazioni approfondite, vedere la guida specifica del prodotto in [Experience League](https://experienceleague.adobe.com).

| Termine | In CX Enterprise e questa guida | Altro utilizzo comune di Adobe |
| --- | --- | --- |
| **Adobe CX Enterprise** | Esperienza Web unificata in `experience.adobe.com`, in cui si aprono applicazioni di marketing, si impostano preferenze e notifiche e si raggiungono i servizi di interfaccia condivisa, ad esempio Attributi del cliente e [Libreria tipi di pubblico](../services/audiences/overview.md). Precedentemente *Adobe Experience Cloud*. | Non lo stesso prodotto di **Adobe Experience Platform** (infrastruttura dati del cliente, sandbox, set di dati). Non **Adobe Creative Cloud** (applicazioni di progettazione e multimediali). |
| **Adobe Experience Platform** | Viene visualizzato quando si collegano gli agenti di raccolta dati, identità o piattaforma alle soluzioni; alcune funzioni di ricerca navigazione e AI sono supportate da Platform. | Una piattaforma di dati e orchestrazione. Non utilizzare &quot;Experience Platform&quot; quando si intende la shell o la home page di CX Enterprise. |
| **Experience League** | Dove la Guida e i collegamenti interni al prodotto ti inviano per **documentazione**, **tutorial**, playlist di apprendimento, note sulla versione e contesto della community per le soluzioni Adobe. Inizia dalla [Experience League home](https://experienceleague.adobe.com). | Completa il **[Centro assistenza Adobe](https://helpx.adobe.com/support.html)**, che mette in evidenza **account**, **piano**, **fatturazione**, download e risoluzione dei problemi tra prodotti diversi per singoli utenti e team. Utilizza l&#39;Help Center per reimpostare le password, pianificare le modifiche e attività simili; utilizza Experience League per i contenuti dimostrativi dei prodotti. |
| **Assistente AI/IA agente** | Assistenti interni al prodotto e agenti orchestrati descritti negli argomenti AI di questa guida; l’accesso e i crediti dipendono dalle adesioni del prodotto. | Altre superfici di Adobe (ad esempio, **Firefly** o **Express**) utilizzano funzioni &quot;AI&quot; con ambiti e criteri diversi. |
| **Organizzazione** | La tua **organizzazione IMS**: il limite per le licenze Enterprise, le directory utente, l&#39;SSO e l&#39;amministrazione di Admin Console in CX Enterprise. Consulta [Organizzazioni e collegamento account](../administration/organizations.md). | Non è una *suite di rapporti* di Analytics, una *proprietà* di Target o una *sandbox* di Experience Platform (si tratta di contenitori specifici del prodotto). |
| **Admin Console** | Piano di controllo Enterprise in `adminconsole.adobe.com` per utenti, profili di prodotto e identità; collegato dagli argomenti di amministrazione **di CX Enterprise.** Consulta [Gestione di utenti e prodotti](../administration/admin-console.md). | Diverso da **amministratore interno al prodotto** all&#39;interno di ogni app (ad esempio, strumenti di amministrazione di Analytics o schermate delle autorizzazioni di Journey Optimizer). |
| **Profilo di prodotto** | Pacchetto di licenze in Admin Console che consente l’accesso a un prodotto o a una funzionalità. Per avere diritto, gli utenti devono appartenere a un profilo. Consulta [Gestione di prodotti e profili](https://helpx.adobe.com/it/enterprise/using/manage-products.html). | Non intercambiabile con ogni nome di &quot;area di lavoro&quot;, &quot;contenitore&quot; o &quot;proprietà&quot; interno al prodotto; questi variano a seconda della soluzione. |
| **Collegamento account** | Collegare l’accesso a un’applicazione (ad esempio, le credenziali di Analytics o Target) all’Adobe ID per l’organizzazione in modo che i servizi riconoscano un utente. Consulta [Organizzazioni e collegamento account](../administration/organizations.md). | Diverso dall&#39;installazione di **sincronizzazione directory**, **SSO** o **federazione** (decisioni di identità a livello di organizzazione in Admin Console). |
| **Servizio Experience Cloud ID / ECID** | L’identificatore visitatore persistente utilizzato nelle soluzioni; spesso distribuito con tag o Web SDK. Ancora comunemente indicato come **ID Experience Cloud** o **MID** nelle discussioni precedenti di Analytics. Consulta la [panoramica del servizio ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it). | Distinto dal nome di cookie legacy di una singola app o dai concetti del grafo delle identità di **Experience Platform**, anche se può essere correlato in un&#39;implementazione. |
| **Attributi del cliente** | Attributi CRM o Enterprise caricati e mappati per l’utilizzo in Analytics, Target e flussi di lavoro correlati tramite il servizio People. Consulta gli argomenti [Attributi del cliente](../services/customer-attributes/attributes.md). | Non eseguire l&#39;equazione con **caratteristiche Audience Manager** da sole o con ogni campo di profilo **Real-Time CDP** senza controllare il limite del prodotto. |
| **Libreria pubblico** | Interfaccia utente di CX Enterprise per comporre e condividere tipi di pubblico tra applicazioni integrate. | Anche **Audience Manager** e **Target** utilizzano &quot;tipi di pubblico&quot;, ma le regole di segmentazione e le destinazioni differiscono in base al prodotto. |
| **Segmento** (Analytics) | Una definizione di pubblico basata su regole che puoi creare in Adobe Analytics e, se supportata, pubblicare per tipi di pubblico condivisi. | In **Audience Manager**, i segmenti combinano **caratteristiche**; la denominazione si sovrappone, ma l&#39;implementazione non è identica. In **Target**, &quot;audiences&quot; ha sostituito le vecchie etichette &quot;segmento&quot; in molte posizioni. |
| **Assets (Experience Cloud Assets)** | Cartelle e file condivisi per la collaborazione tra i flussi di lavoro di marketing CX Enterprise e gli utenti approvati di **Creative Cloud**. Vedi [Panoramica di Assets](../services/assets/experience-cloud-assets.md). | In **Creative Cloud**, &quot;risorse&quot; in genere significa file di progettazione (PSD, AI, INDD). Stessa parola, modello di condivisione e governance diverso. |

{style="table-layout:auto"}

