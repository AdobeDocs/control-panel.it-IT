---
title: Monitoraggio profili attivi
description: Scopri come ottenere informazioni in tempo reale sull’utilizzo e l’evoluzione più recenti e storici dei profili attivi per ciascuna delle istanze della campagna.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Monitoraggio profili attivi {#active-profiles-monitoring}

>[!IMPORTANT]
>
>Il monitoraggio dei profili attivi dal Pannello di controllo è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso.
>
>Questa funzione è disponibile per i clienti ospitati su AWS dalla build Campaign Standard 10368 e dalla build Campaign Classic 8931. Se si utilizza una build precedente, è necessario eseguire l&#39;aggiornamento per utilizzare questa funzione.

## Informazioni sui profili attivi {#about-active-profiles}

In base al contratto, a ciascuna istanza di Campaign viene fornito un numero specifico di profili attivi conteggiati a scopo di fatturazione. Per riferimento al numero di profili attivi acquistati, fare riferimento al contratto più recente.

Per &quot;profilo&quot; si intende un registro di informazioni (ad esempio: un record nella tabella nmsRecipient o una tabella esterna contenente un ID cookie, un ID cliente, un identificatore mobile o altre informazioni pertinenti a un canale specifico) che rappresenta un cliente finale, un potenziale o un lead.

I profili sono considerati attivi se sono stati presi di mira o comunicati con negli ultimi 12 mesi tramite qualsiasi canale.

>[!NOTE]
>
>I canali Facebook e Twitter non vengono presi in considerazione.

Per ulteriori informazioni sui profili attivi, consulta la documentazione [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) e [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) .

## Monitoraggio dei profili attivi {#monitoring-active-profiles}

Il Pannello di controllo consente di monitorare l&#39;utilizzo dei profili attivi per ciascuna istanza di Campaign.

A questo scopo, effettuate le seguenti operazioni:

1. Apri la scheda **[!UICONTROL Performance Monitoring]**, quindi seleziona la scheda **[!UICONTROL Active Profiles]**.

1. Selezionate l’istanza desiderata dall’ **[!UICONTROL Instance List]**.

1. Viene visualizzato il numero di profili attivi utilizzati dall&#39;istanza e l&#39;ultima volta che il flusso di lavoro di fatturazione è stato eseguito sull&#39;istanza.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>I profili attivi vengono conteggiati in base ai flussi di lavoro tecnici dedicati che vengono eseguiti quotidianamente sulle vostre istanze:
>
>* Il flusso di lavoro [&quot;Fatturazione&quot;](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) per Campaign Standard,
>* Flusso di lavoro [&quot;Numero di profili di fatturazione attivi&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) per Campaign Classic.


L’area inferiore fornisce una rappresentazione grafica dell’utilizzo dei profili attivi negli ultimi 30 giorni. Potete cambiare il periodo di tempo visualizzato a 1 anno utilizzando i filtri disponibili nell&#39;angolo superiore destro.

Passando il puntatore del mouse su una delle barre del grafico è possibile ottenere il numero esatto di profili attivi utilizzati per il periodo selezionato.
