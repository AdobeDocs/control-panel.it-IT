---
product: campaign
solution: Campaign
title: Monitoraggio del database
description: Scopri come monitorare il database Campaign nel Pannello di controllo Campaign
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---


# Monitoraggio del database {#database-monitoring}

## Informazioni sui database delle istanze {#about-instances-databases}

In base al contratto, a ciascuna istanza di Campaign viene fornito uno spazio di database specifico.

I database includono tutte **le risorse**, i **flussi di lavoro** e **i dati** memorizzati in  Adobe Campaign.

Nel tempo, i database possono raggiungere la capacità massima, soprattutto se le risorse memorizzate non vengono mai eliminate dall&#39;istanza, o se sono presenti molti flussi di lavoro in stato di pausa.

Un overflow di un database di istanza può causare diversi problemi (impossibilità di effettuare il login, di inviare e-mail ecc.). Il monitoraggio dei database delle istanze è pertanto essenziale per garantire prestazioni ottimali.

>[!NOTE]
>
>Se la quantità di spazio del database fornito come indicato nel Pannello di controllo Campaign non riflette la quantità specificata nel contratto, rivolgiti all&#39;Assistenza clienti.

## Monitoraggio dell&#39;utilizzo del database {#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) Scoprite questa funzione nel video con [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring)

Il Pannello di controllo Campaign consente di monitorare l&#39;utilizzo del database per ciascuna istanza di Campaign. A questo scopo, aprite la **[!UICONTROL Performance Monitoring]** scheda, quindi selezionate la **[!UICONTROL Databases]** scheda.

Selezionate l&#39;istanza desiderata dall&#39;istanza **[!UICONTROL Instance List]** per visualizzare informazioni sulla capacità del database dell&#39;istanza e sullo spazio utilizzato.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>I dati di questo dashboard vengono aggiornati in base alla **[!UICONTROL Database cleanup technical workflow]** sequenza eseguita nell&#39;istanza Campaign (consultate la documentazione relativa ai Campaign Standard [e ai](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) Campaign Classic [](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) ).
>
>Puoi controllare l’ultima volta che il flusso di lavoro è stato eseguito sotto le **[!UICONTROL Used Space]** metriche e **[!UICONTROL Provided Space]** . Si noti che, se il flusso di lavoro non è in esecuzione da più di 3 giorni, si consiglia di contattare  Assistenza clienti di Adobe in modo che questi analizzino il motivo per cui il flusso di lavoro non è in esecuzione.

Ulteriori metriche, descritte di seguito, sono disponibili in questo dashboard per consentire di analizzare l&#39;utilizzo del database dell&#39;istanza:

* [Utilizzo del database](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Panoramica sull&#39;archiviazione](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [Primi 10 risorse temporanee](../../performance-monitoring/using/database-monitoring.md#top-10)

### Utilizzo del database {#database-utilization}

L&#39; **[!UICONTROL Database utilization]** area fornisce una rappresentazione grafica dell&#39;utilizzo minimo, medio e massimo del database negli ultimi 7 giorni, oltre alla soglia di utilizzo del database del 90% rappresentata da una curva punteggiata rossa.

Per modificare il periodo di tempo, usate i filtri disponibili nell’angolo superiore destro del grafico.

Per una migliore leggibilità, potete anche evidenziare una o più curve nel grafico. A questo scopo, selezionateli dalla **[!UICONTROL Aggregation Type]** legenda.

Per ulteriori dettagli su un periodo di tempo specifico, passate il puntatore del mouse sul grafico per visualizzare le informazioni sull&#39;utilizzo del database che è stato creato in quel momento.

![](assets/databases_dashboard_detail.png)

### Panoramica sull&#39;archiviazione {#storage-overview}

La **[!UICONTROL Storage overview]** zona offre una rappresentazione grafica dello spazio occupato da:

* **[!UICONTROL System resources]**

   Se le risorse di sistema occupano gran parte dello spazio del database, si consiglia di contattare l&#39;Assistenza clienti.

* **[!UICONTROL Out-of-the-box tables]** fornito per impostazione predefinita con le istanze Campaign,
* **[!UICONTROL Temporary tables]** creati da flussi di lavoro e consegne,
* **[!UICONTROL Non-out of the box tables]** generati dopo la creazione di risorse personalizzate.

![](assets/database-storage-overview.png)

Fate clic sul **[!UICONTROL View details]** pulsante per visualizzare ulteriori dettagli sulle diverse risorse che occupano spazio nel database.

![](assets/database-storage-details.png)

Usate il filtro per definire meglio le tabelle di ricerca e visualizzare solo le tabelle di un tipo di risorsa specifico.

![](assets/database-storage-overview-filter.png)

### Primi 10 risorse temporanee {#top-10}

Nell&#39; **[!UICONTROL Top 10 temporary resources]** area sono elencate le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne.

Il monitoraggio dei flussi di lavoro e delle consegne che creano risorse temporanee di grandi dimensioni è un passo fondamentale per monitorare il database. Se una risorsa temporanea utilizza troppo spazio nel database, accertatevi che sia necessario disporre di tale flusso di lavoro o consegna, quindi andate all&#39;istanza per interromperla.

>[!IMPORTANT]
>
>In generale, si consiglia di evitare di avere **più di 40 colonne** nelle risorse non incluse.

![](assets/database-top10.png)

>[!NOTE]
>
>Se un flusso di lavoro presenta un numero elevato di conteggi di tabelle o dimensioni del database, è consigliabile rivedere il flusso di lavoro per scoprire perché genera così tanti dati.
>
>Le risorse Campaign Standard e Classic sono disponibili anche alla fine di questa pagina per impedire il sovraccarico del database.

Il **[!UICONTROL View all]** pulsante consente di accedere a informazioni dettagliate su tali risorse temporanee.

![](assets/database-top10-view.png)

>[!NOTE]
>
>Il valore nella **[!UICONTROL Keep interim results]** colonna indica se l&#39;opzione è abilitata (&quot;1&quot;) o disattivata (&quot;0&quot;) in Campaign. L&#39; **[!UICONTROL Keep interim results]** opzione è accessibile nelle proprietà dei flussi di lavoro. Consente di salvare i risultati delle transizioni tra le varie attività di un flusso di lavoro (consultate la documentazione [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) e [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs) ).
>
>Se l&#39;opzione è abilitata per uno dei flussi di lavoro, il flusso di lavoro di pulizia del database non sarà in grado di recuperare lo spazio utilizzato dai risultati intermedi. È quindi consigliabile rivedere il flusso di lavoro per verificare se l&#39;opzione può essere disattivata.

## Prevenzione del sovraccarico del database {#preventing-database-overload}

Campaign Standard e Classic offrono diversi modi per impedire l&#39;eccessivo consumo di spazio su disco del database.

La sezione seguente fornisce utili risorse dalla documentazione relativa a Campaign per ottimizzare l’utilizzo dei database:

**Monitoraggio dei flussi di lavoro**

* [Best practice](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) sui flussi di lavoro (Campaign Standard)
* [Esecuzione](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) del flusso di lavoro di monitoraggio (Campaign Classic)

**Manutenzione del database**

* Flusso di lavoro tecnico per la pulizia del database ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guida](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) alla manutenzione del database (Campaign Classic)
* [Risoluzione dei problemi](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) delle prestazioni del database (Campaign Classic)
* [Opzioni](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) relative al database (Campaign Classic)
* Conservazione dei dati ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Inoltre, puoi ricevere notifiche quando uno dei tuoi database raggiunge la capacità. A questo scopo, iscriviti agli avvisi [per le](../../performance-monitoring/using/email-alerting.md)e-mail.
