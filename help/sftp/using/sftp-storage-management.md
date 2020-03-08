---
title: Gestione dello storage SFTP
description: Scopri come monitorare e gestire lo storage del server SFTP
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Gestione dello storage SFTP {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id=&quot;cp_storage&quot;
>title=&quot;Informazioni sulla capacità di storage&quot;
>abstract=&quot;In questa scheda, è possibile visualizzare le informazioni sulla capacità di storage e sull&#39;utilizzo dei server SFTP. Solo i server SFTP a cui avete accesso sono visualizzati qui. Contattate l&#39;amministratore per richiedere l&#39;accesso ad altri server SFTP.&quot;
>Additional-url=&quot;https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4&quot; text=&quot;Guarda il video dimostrativo&quot;

È possibile che sul server SFTP sia stata fornita una capacità di storage diversa, a seconda dei termini contrattuali.

È fondamentale monitorare regolarmente lo spazio disponibile per ciascuno dei server SFTP. In caso contrario, potrebbe non essere più possibile salvare file aggiuntivi sul server o eseguire con successo flussi di lavoro che si basano sugli aggiornamenti di questo server.

**Argomenti correlati:**

* [Video sull&#39;esercitazione Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Video sull&#39;esercitazione Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Accesso alle informazioni sulla capacità di storage {#accessing-storage-capacity-information}

La **[!UICONTROL Top utilized SFTP disk capacity]** sezione dell’intestazione include i tre server più utilizzati collegati alle istanze a cui l’amministratore ha accesso. Queste informazioni sono disponibili in ogni scheda della scheda SFTP.

![](assets/control_panel_topspace.png)

Le informazioni sullo spazio utilizzato da tutte le istanze a cui avete accesso sono disponibili nella **[!UICONTROL Storage]** scheda della scheda SFTP. Viene aggiornato in ogni aggiornamento di pagina.

![](assets/control_panel_space.png)

Ad esempio, un avviso visivo consente di sapere quando lo storage supera la capacità:

* **Arancione**: l&#39;istanza ha superato l&#39;80% della sua capacità,
* **Rosso**: l&#39;istanza supera il 90% della sua capacità.

Sono inoltre disponibili ulteriori suggerimenti per aiutarvi a sapere come procedere con l&#39;avvicinarsi della capacità del server.

## Best practice per l&#39;esaurimento della capacità di storage {#best-practices-when-capacity-runs-out}

1. **Pulite il server SFTP da file** vecchi o superflui. Per ulteriori informazioni su come accedere alla cartella del server SFTP, consulta [questa sezione](../../sftp/using/logging-into-sftp-server.md).
1. Verificate che i **flussi** di lavoro che puliscono i server SFTP siano eseguiti correttamente. Per ulteriori informazioni sui flussi di lavoro tecnici in Adobe Campaign, consulta la documentazione dedicata a [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) e [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Rivolgetevi al team dell&#39;account per **richiedere più spazio di archiviazione** (potrebbero essere applicati costi aggiuntivi).
1. Se ritieni che ci possa essere un problema, contatta l’**Assistenza clienti**.
