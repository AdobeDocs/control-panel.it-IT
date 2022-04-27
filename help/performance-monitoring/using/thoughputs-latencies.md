---
product: campaign
solution: Campaign
title: Trasmissione e monitoraggio della latenza
description: Scopri come monitorare le esperienze di Campaign e la latenza nel Pannello di controllo.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: ht
source-wordcount: '314'
ht-degree: 100%

---

# Trasmissione e monitoraggio della latenza {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Informazioni sulle uscite e sul monitoraggio della latenza "
>abstract="In questa scheda, puoi monitorare la tendenza delle consegne e della latenza in un periodo di tempo sulle istanze."

Il Pannello di controllo ti consente di monitorare gli output di consegna e la latenza di ciascuna istanza.

>[!IMPORTANT]
>
>Questa funzione è disponibile per tutti i clienti Campaign Standard e v8 e per i clienti Campaign v7 con numeri di build 9032, 9330, 9346 o 9349 che hanno distribuzioni [autonome](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=it) (senza alcuna istanza MID).

Per comprendere l’utilizzo delle istanze e garantirne le prestazioni, è essenziale monitorare la tendenza degli output di consegna e della latenza in un determinato periodo di tempo.

Queste informazioni sono disponibili nel Pannello di controllo Campaign per ciascuna istanza di Campaign nella sezione **[!UICONTROL Performance Monitoring]**, all’interno della scheda **[!UICONTROL Throughputs & Latency]**. Tieni presente che il Pannello di controllo Campaign può richiedere fino a 1 ora prima di visualizzare i dati.

* L’area **[!UICONTROL Throughput]** fornisce informazioni sul numero di messaggi inviati all’ora dall’istanza di Campaign selezionata per tutti i canali di comunicazione a cui hai diritto.

   >[!NOTE]
   >
   >Per Campaign v7/v8, il valore di velocità effettiva visualizzato è quello ottenuto dalle istanze MID (mid sourcing). Per le distribuzioni di marketing (MKT) autonome (senza alcuna istanza MID), viene mostrata invece la velocità effettiva dall’istanza MKT.

* L’area **[!UICONTROL Latency]** fornisce informazioni sulla latenza riscontrata nell’istanza selezionata durante l’invio di comunicazioni transazionali in tempo reale. Le latenze vengono acquisite e visualizzate al 95 e 99 percentile, il che significa che il 95% e il 99% delle richieste dovrebbero essere più veloci della latenza specificata.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Tutte le cifre presentate in questo settore sono approssimative e solo a scopo informativo.

Per impostazione predefinita, i dati vengono visualizzati per il giorno corrente. È possibile modificare il periodo di tempo visualizzato utilizzando i pulsanti **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** e **[!UICONTROL 7 days]**.

Puoi anche visualizzare queste informazioni in formato tabulare con colonne ordinabili, anziché con un grafico. Per farlo, fai clic sul pulsante **[!UICONTROL Visualization settings]**, quindi seleziona **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)
