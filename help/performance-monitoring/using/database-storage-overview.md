---
product: campaign
solution: Campaign
title: Panoramica sull’archiviazione
description: Scopri come monitorare nel Pannello di controllo Campaign le diverse risorse di Campaign che occupano spazio nel database delle istanze.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# Panoramica sull’archiviazione {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Panoramica sull’archiviazione"
>abstract="In questa scheda puoi ottenere informazioni dettagliate sulle diverse risorse di Campaign che occupano spazio nel database."

L’area **[!UICONTROL Storage overview]** fornisce una rappresentazione grafica dello spazio occupato da:

* **[!UICONTROL System resources]**

  Tieni presente che, se le risorse di sistema occupano gran parte dello spazio del database, è consigliabile contattare l’Assistenza clienti.

* **[!UICONTROL Out-of-the-box tables]** fornite per impostazione predefinita con le istanze Campaign,
* **[!UICONTROL Temporary tables]** create da flussi di lavoro e consegne,
* **[!UICONTROL Non-out of the box tables]** generate dopo la creazione di risorse personalizzate.

![](assets/database-storage-overview.png)

Fai clic sul pulsante **[!UICONTROL View details]** per ottenere ulteriori dettagli sulle diverse risorse che occupano spazio nel database.

Puoi utilizzare l’elenco a discesa per perfezionare le tabelle di ricerca e visualizzazione solo da un tipo di risorsa specifico (flussi di lavoro, consegne, destinatari).

![](assets/database-storage-details.png)

Questa schermata consente inoltre di monitorare i parametri dei flussi di lavoro che possono richiedere un’attenzione specifica per evitare problemi alle istanze. Per ulteriori informazioni, consulta [questa pagina](workflow-monitoring.md).
