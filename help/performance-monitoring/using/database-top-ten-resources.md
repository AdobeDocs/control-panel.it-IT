---
product: campaign
solution: Campaign
title: Le 10 risorse temporanee principali
description: Scopri come monitorare nel Pannello di controllo Campaign le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne sul database Campaign.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 92%

---

# Le 10 risorse temporanee principali {#top-10}

Nell’area **[!UICONTROL Top 10 temporary resources]** sono elencate le 10 risorse temporanee più grandi generate dai flussi di lavoro e dalle consegne.

Il monitoraggio dei flussi di lavoro e delle consegne che creano grandi risorse temporanee è un passaggio chiave per monitorare il database. Se una risorsa temporanea occupa troppo spazio nel database, assicurati che il flusso di lavoro o la consegna sia effettivamente indispensabile e, nel caso non lo sia, accedi all’istanza per interromperla.

>[!IMPORTANT]
>
>Si consiglia di evitare di avere **più di 40 colonne** in risorse non fornite con il prodotto.

![](assets/database-top10.png)

>[!NOTE]
>
>Se un flusso di lavoro ha un numero elevato di voci di tabella o dimensioni eccessive nel database, è consigliabile rivedere il flusso di lavoro per scoprire perché genera così tanti dati.
>
>Alla fine di questa pagina trovi alcune risorse di Campaign Standard e Classic utili per evitare il sovraccarico del database.

Il pulsante **[!UICONTROL View all]** consente di accedere a informazioni dettagliate su queste risorse temporanee.

![](assets/database-top10-view.png)

Il valore nella colonna **[!UICONTROL Keep interim results]** indica se l’opzione è abilitata (&quot;1&quot;) o disabilitata (&quot;0&quot;) in Campaign. Questa opzione consente di salvare i risultati delle transizioni tra le varie attività di un flusso di lavoro (consulta la documentazione di [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=it) e [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=it#logs)).

>[!IMPORTANT]
>
>Questa opzione non deve mai essere selezionata in un flusso di lavoro di produzione. Viene utilizzata per analizzare i risultati ed è progettata solo a scopo di test e quindi deve essere utilizzata solo in ambienti di sviluppo o di staging.
>
>Se il valore in Pannello di controllo Campaign indica che l’opzione è abilitata per uno dei flussi di lavoro, si consiglia vivamente di disattivarla.
