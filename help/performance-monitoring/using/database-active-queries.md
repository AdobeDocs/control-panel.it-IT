---
product: campaign
solution: Campaign
title: Monitoraggio delle query attive
description: Scopri come monitorare le query attive sulle istanze Campaign nel Pannello di controllo.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 50%

---

# Monitoraggio delle query attive {#long-running-queries}

L’area **[!UICONTROL Active queries]** dalla scheda **[!UICONTROL Databases]** elenca le cinque query in esecuzione da più tempo nell’istanza selezionata.

![](assets/active-queries.png)

Le **[!UICONTROL Duration]** colonne specificano per quanto tempo una query è in esecuzione sull’istanza. La durata viene visualizzata in questo formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Se una delle query è attiva da più di 24 ore, riceverai una notifica via e-mail se ti sei abbonato a [avvisi e-mail](email-alerting.md).
>
>In tal caso, contatta l’Assistenza clienti in modo che identifichino e risolvano il problema. Dovrai fornire loro il **[!UICONTROL PID]** valore di colonna, che è un identificatore univoco per la query.
