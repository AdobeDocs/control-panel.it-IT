---
product: campaign
solution: Campaign
title: Avvisi e-mail
description: Scopri come ricevere notifiche e-mail in caso di problemi con le istanze Campaign
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 3%

---

# Avvisi e-mail {#email-alerting}

Per garantire una maggiore flessibilità al lavoro, Pannello di controllo Campaign è dotato di funzionalità di avviso e-mail in tempo reale.

## Elenco delle segnalazioni {#list}

L’elenco delle segnalazioni è il seguente:

* **Utilizzo dell’archiviazione SFTP**: uno dei server SFTP ha raggiunto l’80% o più della capacità. Consulta [Gestione dell’archiviazione SFTP](../../sftp/using/sftp-storage-management.md).

* **Utilizzo del database**: uno dei database delle istanze ha raggiunto l’80% o più della capacità. Consulta [Monitoraggio del database](../../performance-monitoring/using/database-monitoring.md).

* **Scadenza dell’inserimento di IP nell’elenco Consentiti SFTP**: uno degli intervalli IP definiti è scaduto o scade tra 10 giorni o meno. Consulta [Inserimento di intervalli IP nell’elenco Consentiti](../../sftp/using/ip-range-allow-listing.md).

* **Scadenza chiave pubblica SFTP**: una delle chiavi pubbliche definita è scaduta o scadrà tra 10 giorni o meno. Consulta [Gestione delle chiavi](../../sftp/using/key-management.md).

* **Scadenza certificato SSL**: uno dei certificati SSL dei sottodomini è scaduto o scade tra 30 giorni o meno. Consulta [Monitoraggio dei certificati SSL dei sottodomini](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Inoltre, il Pannello di controllo Campaign consente di: **impostare i promemoria** per ricevere notifiche tramite e-mail prima che un evento si verifichi sulle istanze (versioni e revisioni dei servizi).
>
>A questo scopo, è necessario essersi abbonati agli avvisi e-mail e aver impostato un promemoria per i prossimi eventi desiderati. [Scopri come impostare i promemoria per i prossimi eventi](../../service-events/service-events.md#reminders)

## Abbonati agli avvisi {#subscribe}

Per iscriverti a questi avvisi, segui questi passaggi:

1. Fai clic su **[!UICONTROL Alerting notifications]** disponibile da qualsiasi posizione nel Pannello di controllo Campaign, quindi fai clic su **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Viene inviata un’e-mail per confermare l’abbonamento.

   ![](assets/email_subscription.png)

1. Dopo l’abbonamento, il Pannello di controllo Campaign invierà una notifica sui problemi del sistema e raccomanderà le azioni da intraprendere. Gli avvisi e-mail vengono inviati a tutti coloro che si sono iscritti a **tutte le istanze** di essere amministratori di.

   ![](assets/alert_sample.png)
