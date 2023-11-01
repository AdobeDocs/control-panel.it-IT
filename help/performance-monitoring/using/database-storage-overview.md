---
product: campaign
solution: Campaign
title: Panoramica sull’archiviazione
description: Scopri come monitorare nel Pannello di controllo Campaign le diverse risorse di Campaign che occupano spazio nel database delle istanze.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 30%

---

# Panoramica sull’archiviazione {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Panoramica sull’archiviazione"
>abstract="In questa scheda puoi ottenere informazioni dettagliate sulle diverse risorse di Campaign che occupano spazio nel database."

Il **[!UICONTROL Panoramica sull’archiviazione]** L&#39;area fornisce una rappresentazione grafica dello spazio occupato da:

* **[!UICONTROL Risorse di sistema]**

  Tieni presente che, se le risorse di sistema occupano gran parte dello spazio del database, è consigliabile contattare l’Assistenza clienti.

* **[!UICONTROL Tabelle pronte all’uso]** fornite per impostazione predefinita con le istanze Campaign,
* **[!UICONTROL Tabelle temporanee]** create da flussi di lavoro e consegne,
* **[!UICONTROL Tabelle non pronte all’uso]** generate dopo la creazione di risorse personalizzate.

![](assets/database-storage-overview.png)

Fai clic su **[!UICONTROL Visualizza dettagli]** per ottenere ulteriori dettagli sulle diverse risorse che occupano spazio nel database.

Puoi utilizzare l’elenco a discesa per perfezionare le tabelle di ricerca e visualizzazione solo da un tipo di risorsa specifico (flussi di lavoro, consegne, destinatari).

![](assets/database-storage-details.png)

Questa schermata consente inoltre di monitorare i parametri dei flussi di lavoro che possono richiedere un’attenzione specifica per evitare problemi alle istanze. Per ulteriori informazioni, consulta [questa pagina](workflow-monitoring.md).
