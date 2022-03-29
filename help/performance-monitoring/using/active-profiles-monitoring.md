---
product: campaign
solution: Campaign
title: Monitoraggio profili attivi
description: Scopri come ottenere informazioni in tempo reale su utilizzi ed evoluzioni più recenti e storici dei profili attivi per ciascuna delle istanze di Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 78%

---

# Monitoraggio profili attivi {#active-profiles-monitoring}

## Informazioni sui profili attivi {#about-active-profiles}

>[!IMPORTANT]
>
>Il monitoraggio profili attivi dal Pannello di controllo Campaign è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso. È disponibile dalla build Campaign Standard 10368.

In base al contratto, a ciascuna istanza di Campaign viene fornito un numero specifico di profili attivi conteggiati a scopo di fatturazione. Per informazioni sul numero di profili attivi acquistati, fai riferimento al contratto più recente.

Per “profilo” si intende un registro di informazioni (ad esempio un record nella tabella nmsRecipient o una tabella esterna contenente un ID cookie, un ID cliente, un identificatore mobile o altre informazioni pertinenti a un canale specifico) che rappresenta un cliente finale, potenziale o un lead.

I profili sono considerati attivi se sono stati targetizzati o se è avvenuta una comunicazione con essi negli ultimi 12 mesi tramite qualsiasi canale.

>[!NOTE]
>
>I canali Facebook e Twitter non vengono presi in considerazione.

Per ulteriori informazioni sui profili attivi, consulta [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) e [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) documentazione.

## Monitorare i profili attivi {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Informazioni sul monitoraggio dei profili attivi"
>abstract="In questa scheda, puoi ottenere informazioni in tempo reale sull’utilizzo e l’evoluzione dei profili attivi più recenti e storici per ciascuna delle istanze Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=it" text="Informazioni sul monitoraggio delle prestazioni"

Il Pannello di controllo Campaign consente di monitorare l’utilizzo dei profili attivi per ciascuna istanza di Campaign.

Per farlo, esegui questi passaggi:

1. Apri la scheda **[!UICONTROL Performance Monitoring]**, quindi seleziona la scheda **[!UICONTROL Active Profiles]**.

1. Seleziona l’istanza desiderata da **[!UICONTROL Instance List]**.

1. Viene visualizzato il numero di profili attivi utilizzati dall’istanza e l’ultima volta che il flusso di lavoro di fatturazione è stato eseguito sull’istanza.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>I profili attivi vengono conteggiati in base ai flussi di lavoro tecnici dedicati che vengono eseguiti quotidianamente sulle istanze:
>
>* Il flusso di lavoro [“Billing”](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=it) (Fatturazione) per Campaign Standard,
>* La [&quot;Numero di profili di fatturazione attivi&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) flusso di lavoro per Campaign v7/v8.


L’area inferiore fornisce una rappresentazione grafica dell’utilizzo dei profili attivi negli ultimi 30 giorni. Puoi impostare il periodo di tempo visualizzato a 1 anno utilizzando i filtri disponibili nell’angolo in alto a destra.

Passando il puntatore del mouse su una delle barre del grafico è possibile ottenere il numero esatto di profili attivi utilizzati durante il periodo selezionato.
