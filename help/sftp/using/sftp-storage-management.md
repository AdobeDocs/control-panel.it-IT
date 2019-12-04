---
title: Gestione dello storage SFTP
description: Scopri come monitorare e gestire lo storage del server SFTP
translation-type: tm+mt
source-git-commit: 111c8fd461f6f1c567288acd7a83aee5ef7fce97

---


# Gestione dello storage SFTP {#sftp-storage-management}

È possibile che sul server SFTP sia stata fornita una capacità di storage diversa, a seconda dei termini contrattuali.

È fondamentale monitorare regolarmente lo spazio disponibile per ciascuno dei server SFTP. In caso contrario, potrebbe non essere più possibile salvare file aggiuntivi sul server o eseguire con successo flussi di lavoro che si basano sugli aggiornamenti di questo server.

**Argomenti correlati:**

* [Video sull'esercitazione Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-sftp-servers.html)
* [Video sull'esercitazione Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Accesso alle informazioni sulla capacità di storage {#accessing-storage-capacity-information}

La **[!UICONTROL Top utilized SFTP disk capacity]** sezione dell’intestazione include i tre server più utilizzati collegati alle istanze a cui l’amministratore ha accesso. Queste informazioni sono disponibili in ogni scheda della scheda SFTP.

![](assets/control_panel_topspaceNEW.png)

Le informazioni sullo spazio utilizzato da tutte le istanze a cui avete accesso sono disponibili nella **[!UICONTROL Storage]** scheda della scheda SFTP. Viene aggiornato in ogni aggiornamento di pagina.

![](assets/control_panel_spaceNEW.png)

Ad esempio, un avviso visivo consente di sapere quando lo storage supera la capacità:

* **Arancia**: l'istanza ha superato l'80% della sua capacità,
* **Rosso**: l'istanza supera il 90% della sua capacità.

Sono inoltre disponibili ulteriori suggerimenti per aiutarvi a sapere come procedere con l'avvicinarsi della capacità del server.

## Best practice per l'esaurimento della capacità di storage {#best-practices-when-capacity-runs-out}

1. **Pulite il server SFTP da file** vecchi o superflui. Per ulteriori informazioni su come accedere alla cartella del server SFTP, consulta [questa sezione](../../sftp/using/logging-into-sftp-server.md).
1. Verificate che i **flussi** di lavoro che puliscono i server SFTP siano eseguiti correttamente. Per ulteriori informazioni sui flussi di lavoro tecnici in Adobe Campaign, consulta la documentazione dedicata a [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) e [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Rivolgetevi al team dell'account per **richiedere più spazio di archiviazione** (potrebbero essere applicati costi aggiuntivi).
1. Se ritieni che ci possa essere un problema, contatta l’**Assistenza clienti**.
