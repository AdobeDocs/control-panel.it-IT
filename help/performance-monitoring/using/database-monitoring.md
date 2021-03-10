---
product: campaign
solution: Campaign
title: Monitoraggio del database
description: Scopri come monitorare il database Campaign nel Pannello di controllo Campaign
feature: 'Pannello di controllo Campaign   '
role: Architetto
level: Esperienza
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---


# Monitoraggio del database {#database-monitoring}

## Informazioni sui database delle istanze {#about-instances-databases}

In base al contratto, a ciascuna istanza di Campaign viene fornito uno spazio di database specifico.

I database includono tutti i **risorse**, **flussi di lavoro** e **dati** memorizzati in Adobe Campaign.

Nel tempo, i database possono raggiungere la loro capacità massima, soprattutto se le risorse memorizzate non vengono mai eliminate dall&#39;istanza o se sono presenti molti flussi di lavoro in stato di pausa.

Lo overflow di un database di istanze può causare diversi problemi (impossibilità di accedere, inviare e-mail, ecc.). Il monitoraggio dei database delle istanze è quindi essenziale per garantire prestazioni ottimali.

>[!NOTE]
>
>Se la quantità di spazio del database fornito come mostrato nel Pannello di controllo Campaign non riflette la quantità specificata nel contratto, contatta l’Assistenza clienti.

## Monitoraggio dell&#39;utilizzo del database {#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) Scopri questa funzione nel video utilizzando  [Campaign ](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring) Classicor  [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring)

Il Pannello di controllo Campaign ti consente di monitorare l’utilizzo del database per ciascuna istanza di Campaign. A questo scopo, apri la scheda **[!UICONTROL Performance Monitoring]** , quindi seleziona la scheda **[!UICONTROL Databases]** .

Seleziona l’istanza desiderata da **[!UICONTROL Instance List]** per visualizzare informazioni sulla capacità del database dell’istanza e sullo spazio utilizzato.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>I dati di questo dashboard vengono aggiornati in base alla documentazione **[!UICONTROL Database cleanup technical workflow]** in esecuzione nell’istanza Campaign (consulta [Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) e [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) ).
>
>Puoi controllare l’ultima volta che il flusso di lavoro è stato eseguito sotto le metriche **[!UICONTROL Used Space]** e **[!UICONTROL Provided Space]** . Tieni presente che, se il flusso di lavoro non è in esecuzione da più di 3 giorni, ti consigliamo di contattare l’Assistenza clienti di Adobe in modo che possa indagare il motivo per cui il flusso di lavoro non è in esecuzione.

Altre metriche, descritte di seguito, sono disponibili in questo dashboard per consentire di analizzare l’utilizzo del database dell’istanza:

* [Utilizzo del database](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Panoramica sullo storage](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [Primi 10 risorse temporanee](../../performance-monitoring/using/database-monitoring.md#top-10)

### Utilizzo del database {#database-utilization}

L&#39;area **[!UICONTROL Database utilization]** fornisce una rappresentazione grafica dell&#39;utilizzo minimo, medio e massimo del database negli ultimi 7 giorni e della soglia di utilizzo del database del 90% rappresentata da una curva punteggiata rossa.

Per modificare il periodo di tempo, utilizza i filtri disponibili nell’angolo superiore destro del grafico.

Per una migliore leggibilità, potete anche evidenziare una o più curve nel grafico. A questo scopo, selezionali dalla legenda **[!UICONTROL Aggregation Type]**.

Per ulteriori dettagli su un periodo di tempo specifico, passa il cursore del mouse sul grafico per visualizzare le informazioni sull’utilizzo del database in questo momento.

![](assets/databases_dashboard_detail.png)

### Panoramica sullo storage {#storage-overview}

L&#39;area **[!UICONTROL Storage overview]** fornisce una rappresentazione grafica dello spazio occupato da:

* **[!UICONTROL System resources]**

   Tieni presente che, se le risorse di sistema occupano gran parte dello spazio del database, è consigliabile contattare l’Assistenza clienti.

* **[!UICONTROL Out-of-the-box tables]** fornito per impostazione predefinita con le istanze Campaign,
* **[!UICONTROL Temporary tables]** creati da flussi di lavoro e consegne,
* **[!UICONTROL Non-out of the box tables]** generato dopo la creazione di risorse personalizzate.

![](assets/database-storage-overview.png)

Fai clic sul pulsante **[!UICONTROL View details]** per ottenere ulteriori dettagli sulle diverse risorse che occupano spazio nel database.

![](assets/database-storage-details.png)

Usa il filtro per perfezionare le tabelle di ricerca e visualizzazione solo da un tipo di risorsa specifico.

![](assets/database-storage-overview-filter.png)

### Le 10 risorse temporanee principali {#top-10}

Nell’area **[!UICONTROL Top 10 temporary resources]** sono elencate le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne.

Il monitoraggio dei flussi di lavoro e delle consegne che creano grandi risorse temporanee è un passaggio chiave per monitorare il database. Se una risorsa temporanea richiede troppo spazio nel database, assicurati che sia necessario disporre di questo flusso di lavoro o di questa consegna e, infine, accedi all’istanza per interromperla.

>[!IMPORTANT]
>
>Si consiglia di evitare di avere **più di 40 colonne** in risorse non preconfigurate.

![](assets/database-top10.png)

>[!NOTE]
>
>Se un flusso di lavoro ha un numero elevato di conteggi di tabella o dimensioni del database, è consigliabile rivedere il flusso di lavoro per scoprire perché sta generando così tanti dati.
>
>Le risorse di Campaign Standard e Classic sono disponibili anche alla fine di questa pagina per evitare il sovraccarico del database.

Il pulsante **[!UICONTROL View all]** ti consente di accedere a informazioni dettagliate su queste risorse temporanee.

![](assets/database-top10-view.png)

>[!NOTE]
>
>Il valore nella colonna **[!UICONTROL Keep interim results]** indica se l’opzione è abilitata (&quot;1&quot;) o disabilitata (&quot;0&quot;) in Campaign. L’opzione **[!UICONTROL Keep interim results]** è accessibile nelle proprietà dei flussi di lavoro. Ti consente di salvare i risultati delle transizioni tra le varie attività di un flusso di lavoro (consulta la documentazione [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) e [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs) ).
>
>Se l’opzione è abilitata per uno dei flussi di lavoro, il flusso di lavoro di pulizia del database non sarà in grado di recuperare lo spazio utilizzato dai risultati provvisori. Pertanto, consigliamo di rivedere il flusso di lavoro per verificare se l’opzione può essere disattivata.

## Prevenzione del sovraccarico del database {#preventing-database-overload}

Campaign Standard e Classic offrono diversi modi per evitare un eccessivo consumo di spazio su disco del database.

La sezione seguente fornisce utili risorse dalla documentazione di Campaign per ottimizzare l’utilizzo dei database:

**Monitoraggio dei flussi di lavoro**

* [Best practice per i flussi di lavoro](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html)  (Campaign Standard)
* [Monitoraggio dell’esecuzione del flusso di lavoro](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html)  (Campaign Classic)

**Manutenzione del database**

* Flusso di lavoro tecnico di pulizia del database ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guida alla manutenzione del database](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html)  (Campaign Classic)
* [Risoluzione dei problemi di prestazioni del database](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html)  (Campaign Classic)
* [Opzioni relative al database](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database)  (Campaign Classic)
* Conservazione dei dati ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Inoltre, puoi ricevere notifiche quando uno dei tuoi database raggiunge la sua capacità. A questo scopo, abbonati a [avvisi e-mail](../../performance-monitoring/using/email-alerting.md).
