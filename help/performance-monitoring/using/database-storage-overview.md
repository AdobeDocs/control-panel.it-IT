---
product: campaign
solution: Campaign
title: Panoramica sull’archiviazione
description: Scopri come monitorare nel Pannello di controllo le diverse risorse di Campaign che occupano spazio nel database delle istanze.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 100%

---

# Panoramica sull’archiviazione {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Panoramica sull’archiviazione"
>abstract="In questa scheda puoi ottenere informazioni dettagliate sulle diverse risorse di Campaign che occupano spazio nel database."

L’area **[!UICONTROL Panoramica dell’archiviazione]** fornisce una rappresentazione grafica dello spazio occupato da:

* **[!UICONTROL Risorse di sistema]**

  Tieni presente che, se le risorse di sistema occupano gran parte dello spazio del database, è consigliabile contattare l’Assistenza clienti.

* **[!UICONTROL Tabelle preconfigurate]** fornite per impostazione predefinita con le istanze di Campaign
* **[!UICONTROL Tabelle temporanee]** create da flussi di lavoro e consegne
* **[!UICONTROL Tabelle non preconfigurate]** generate dopo la creazione di risorse personalizzate

![](assets/database-storage-overview.png)

Fai clic sul pulsante **[!UICONTROL Visualizza dettagli]** per ottenere ulteriori dettagli sulle diverse risorse che occupano spazio nel database.

Puoi utilizzare l’elenco a discesa per perfezionare le tabelle di ricerca e visualizzarle solo per uno specifico tipo di risorsa (flussi di lavoro, consegne, destinatari).

![](assets/database-storage-details.png)

Questa schermata consente inoltre di monitorare i parametri dei flussi di lavoro che possono richiedere un’attenzione specifica per evitare problemi nelle istanze. Per ulteriori informazioni, consulta [questa pagina](workflow-monitoring.md).
