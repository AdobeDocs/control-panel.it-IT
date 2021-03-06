---
title: Monitorare i flussi di lavoro
description: Scopri come monitorare specifici parametri dei flussi di lavoro che richiedono attenzione per evitare problemi nelle istanze.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 8016f800-430a-413d-a77b-b7f18f5ab733
source-git-commit: 485069285709a7cc5c074f8813b322328e2840c0
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 93%

---

# Monitorare i flussi di lavoro {#monitor-workflows}

<!-- Clean paused and completed workflows

When [!DNL Adobe Campaign] workflows are paused or completed, they leave temporary tables on your instances database that consume space and can lead to performance issues.

Control Panel allows you to identify those workflows and clean the temporary resources generated on your instances.

>[!NOTE]
>
>Technically, this operation executes the **[!UICONTROL Database cleanup technical workflow]** that runs on your Campaign instance everyday (see [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) and [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) documentation). 

To clean paused and completed workflows, follow these steps:

1. Navigate to the **[!UICONTROL Performance monitoring]** card.

1. In the **[!UICONTROL Databases]** tab, select the instance where you want to perform the operation.

1. Access the **[!UICONTROL Storage overview]** details, then filter the list on **[!UICONTROL Temporary tables]**. Learn more on **[!UICONTROL Storage overview]** in [this page](database-storage-overview.md).

    ![](assets/wkf-monitoring-filter.png)

1. All temporary tables generated on your instances by workflows and deliveries display. Click the **[!UICONTROL Clean now]** button to delete the resources generated by paused and completed workflows.

    ![](assets/wkf-monitoring-clean.png)

1. Once the operation is confirmed, you can track the estimated remaining time in the **[!UICONTROL Storage overview]** list.

    ![](assets/wkf-monitoring-in-progress.png)

Monitor workflow parameters -->

In Adobe Campaign, alcuni parametri dei flussi di lavoro possono richiedere particolare attenzione per evitare problemi alle istanze. I dettagli **[!UICONTROL Storage overview]** nel Pannello di controllo Campaign consentono di verificare se una di queste opzioni ?? abilitata per i flussi di lavoro.

![](assets/wkf-monitoring-parameters.png)

## **[!UICONTROL Keep interim results]** {#keep-results}

Quando ?? abilitata (valore ???1???), questa opzione salva i risultati delle transizioni tra le varie attivit?? di un flusso di lavoro. Per ulteriori informazioni, consulta la documentazione di [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=it) e [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=it#logs).

>[!IMPORTANT]
>
>Questa opzione non deve mai essere selezionata in un flusso di lavoro di produzione. Viene utilizzata a scopo di analisi e test e pertanto deve essere utilizzata solo in ambienti di sviluppo o di staging. ?? consigliabile disattivarla in Campaign.

![](assets/wkf-monitoring-keep.png)

## **[!UICONTROL Show SQL log]** {#sql}

Quando questa opzione ?? abilitata, le query SQL inviate al database durante l???esecuzione del flusso di lavoro vengono visualizzate in Adobe Campaign. Per ulteriori informazioni, consulta la documentazione di [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=en) e [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/workflow-properties.html?lang=it#execution).

Il valore ???1??? indica che il flusso di lavoro ha il campo **Severity** (Gravit??) ?? impostato su ???Produzione??? e che l???opzione del registro query SQL ?? abilitata.

>[!IMPORTANT]
>
>L???attivazione di questa opzione pu?? influire sulle prestazioni e compilare i file di registro sul server. Deve essere utilizzata esclusivamente a fini di analisi e di diagnosi.

![](assets/wkf-monitoring-sql.png)

## **[!UICONTROL Supervisors]** {#supervisors}

Questo campo consente di assegnare un operatore a un flusso di lavoro. Se il flusso di lavoro non riesce, l???operatore riceve un avviso. Per ulteriori informazioni, consulta la documentazione di [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/monitoring-workflow-execution.html?lang=en#error-management) e [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/workflow-properties.html?lang=it#error-management).

Il valore ???1??? indica che il flusso di lavoro ha il campo **Severity** (Gravit??) impostato su ???Produzione??? e che nessun gruppo di supervisori ?? stato assegnato al flusso di lavoro.

![](assets/wkf-monitoring-supervisors.png)
