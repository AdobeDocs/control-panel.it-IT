---
product: campaign
solution: Campaign
title: Informazioni sul monitoraggio del database
description: Scopri come monitorare il database Campaign nel Pannello di controllo Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 81%

---

# Informazioni sul monitoraggio del database {#database-monitoring}

## Informazioni sui database delle istanze {#about-instances-databases}

In base al contratto, a ciascuna istanza di Campaign viene fornito uno spazio di database specifico.

I database includono tutte le **risorse**, i **flussi di lavoro** e i **dati** memorizzati in Adobe Campaign.

Nel tempo, i database possono raggiungere la loro capacità massima, soprattutto se le risorse memorizzate non vengono mai eliminate dall’istanza o se sono presenti molti flussi di lavoro in stato di pausa.

L’overflow del database di un’istanza può causare diversi problemi (impossibilità di accedere, inviare e-mail, ecc.). Il monitoraggio dei database delle istanze è quindi essenziale per garantire prestazioni ottimali.

## Monitoraggio dell’utilizzo del database{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Informazioni sul monitoraggio del database"
>abstract="In questa scheda, puoi ottenere informazioni in tempo reale dati attuali e storici sull’utilizzo e l’evoluzione del database per ciascuna istanza di Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=it" text="Informazioni sul monitoraggio delle prestazioni"

Il Pannello di controllo Campaign consente di monitorare l’utilizzo del database per ciascuna istanza di Campaign. Per fare questo, apri la scheda **[!UICONTROL Performance Monitoring]**, quindi seleziona la scheda **[!UICONTROL Databases]**.

Seleziona l’istanza desiderata da **[!UICONTROL Instance List]** per visualizzare informazioni sulla capacità del database dell’istanza e sullo spazio utilizzato.

Inoltre, puoi ricevere notifiche quando uno dei database raggiunge la sua capacità massima. A questo scopo, abbonati agli [avvisi e-mail](../../performance-monitoring/using/email-alerting.md).

>[!NOTE]
>
>Se lo spazio del database disponibile riportata nel Pannello di controllo Campaign non corrisponde alla quantità specificata nel contratto, contatta l’Assistenza clienti.

![](assets/databases_dashboard.png)

I dati provenienti da questo dashboard vengono aggiornati in base al **[!UICONTROL Database cleanup technical workflow]** che viene eseguito sull’istanza Campaign (vedi [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=it#list-of-technical-workflows) e [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=it) documentazione). Puoi controllare l’ultima volta che il flusso di lavoro è stato eseguito sotto il **[!UICONTROL Used Space]** e **[!UICONTROL Provided Space]** metriche. Tieni presente che, se il flusso di lavoro non è stato eseguito da almeno 3 giorni, ti consigliamo di contattare l’Assistenza clienti di Adobe in modo che possa indagare il motivo per cui il flusso di lavoro si è interrotto.

In questa dashboard sono disponibili ulteriori metriche per analizzare l’utilizzo del database dell’istanza. Sono descritti in dettaglio in queste sezioni:

* [Utilizzo del database](../../performance-monitoring/using/database-utilization.md)
* [Panoramica sull’archiviazione](../../performance-monitoring/using/database-storage-overview.md)
* [Le 10 risorse temporanee principali](../../performance-monitoring/using/database-top-ten-resources.md)
* [Query attive](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) Scopri questa funzione nel video utilizzando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=it#performance-monitoring) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=it#performance-monitoring)
