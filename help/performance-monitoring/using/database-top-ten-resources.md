---
product: campaign
solution: Campaign
title: Le 10 risorse temporanee principali
description: Scopri come monitorare nel Pannello di controllo Campaign le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne sul database Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# Le 10 risorse temporanee principali {#top-10}

Nell’area **[!UICONTROL Top 10 temporary resources]** sono elencate le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne.

Il monitoraggio dei flussi di lavoro e delle consegne che creano grandi risorse temporanee è un passaggio chiave per monitorare il database. Se una risorsa temporanea occupa troppo spazio nel database, assicurati che il flusso di lavoro o la consegna sia effettivamente indispensabile e, nel caso non lo sia, accedi all’istanza per interromperla.

>[!IMPORTANT]
>
>Si consiglia di evitare di avere **più di 40 colonne** in risorse non fornite con il prodotto. Se un flusso di lavoro ha un numero elevato di voci di tabella o dimensioni eccessive nel database, è consigliabile rivedere il flusso di lavoro per scoprire perché genera così tanti dati.
>
>Le linee guida di Campaign Standard e Classic sono disponibili anche in [questa pagina](database-preventing-overload.md) per evitare il sovraccarico del database.

![](assets/database-top10.png)

La **[!UICONTROL View all]** consente di accedere al **[!UICONTROL Storage overview]** informazioni dettagliate su queste risorse temporanee. Per ulteriori informazioni, consulta [questa pagina](database-storage-overview.md).
