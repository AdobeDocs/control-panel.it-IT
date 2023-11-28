---
product: campaign
solution: Campaign
title: Monitoraggio profili attivi
description: Scopri come ottenere informazioni in tempo reale su utilizzi ed evoluzioni più recenti e storici dei profili attivi per ciascuna delle istanze di Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: a9b150a4f24447d22d5c1ecff5d456ca39cb65e2
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 89%

---

# Monitorare i profili attivi {#active-profiles-monitoring}

## Informazioni sui profili attivi {#about-active-profiles}

>[!IMPORTANT]
>
>Il monitoraggio profili attivi dal Pannello di controllo è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso. È disponibile dalla build Campaign Standard 10368.

In base al contratto, a ciascuna istanza di Campaign viene fornito un numero specifico di profili attivi conteggiati a scopo di fatturazione. Per informazioni sul numero di profili attivi acquistati, fai riferimento al contratto più recente.

Per “profilo” si intende un registro di informazioni (ad esempio un record nella tabella nmsRecipient o una tabella esterna contenente un ID cookie, un ID cliente, un identificatore mobile o altre informazioni pertinenti a un canale specifico) che rappresenta un cliente finale, potenziale o un lead.

I profili sono considerati attivi se sono stati targetizzati o se è avvenuta una comunicazione con essi negli ultimi 12 mesi tramite qualsiasi canale.

>[!NOTE]
>
>I canali facebook e X (precedentemente noti come Twitter) non vengono presi in considerazione.

Per ulteriori informazioni sui profili attivi, consulta la documentazione [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=it) e [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=it#active-profiles).

## Monitorare l’utilizzo dei profili attivi {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Informazioni sul monitoraggio dei profili attivi"
>abstract="In questa scheda, puoi ottenere informazioni in tempo reale con dati attuali e storici sull’utilizzo e l’evoluzione dei profili attivi per ciascuna istanza di Campaign."

Per monitorare l’utilizzo del profilo attivo nel Pannello di controllo, passa alla scheda **[!UICONTROL Monitoraggio delle prestazioni]** > **[!UICONTROL Profili attivi]** e seleziona l’istanza desiderata dall’**[!UICONTROL Elenco istanze]**.

Vengono visualizzate informazioni sull’utilizzo dei profili attivi.

![](assets/active-profiles-graph.png)

Nella sezione superiore vengono visualizzate le seguenti informazioni:

* Il numero di profili attivi attualmente utilizzati nell’istanza selezionata, insieme alla marca temporale dell’esecuzione più recente del flusso di lavoro di fatturazione per l’istanza.

* Numero totale di profili attivi utilizzati nell’organizzazione in tutte le istanze.

  >[!NOTE]
  >
  >Questa sezione è visibile solo se alla tua organizzazione sono associate più istanze.

* Numero totale di profili attivi allocati all’organizzazione.

La sezione inferiore fornisce una rappresentazione visiva dell’utilizzo del profilo attivo negli ultimi 30 giorni. Puoi impostare questo intervallo di tempo su 1 anno utilizzando il filtro posizionato nell’angolo in alto a destra. Passando il puntatore del mouse su una delle barre del grafico è possibile ottenere il numero esatto di profili attivi utilizzati durante il periodo selezionato.

Le informazioni relative all’utilizzo dei profili attivi vengono aggiornate in Pannello di controllo Campaign in base ai [!DNL Campaign] Flussi di lavoro tecnici di &quot;fatturazione&quot; eseguiti a intervalli regolari sulle istanze.

| Versione di Campaign | Flusso di lavoro tecnico | Esecuzioni |
|  ---  |  ---  |  ---  |
| Campaign Standard | [Billing](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=it) | Giornaliera |
| Campaign v7/v8 | [Billing](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflowsadvanced-management/about-technical-workflows.html) | Mensile |
