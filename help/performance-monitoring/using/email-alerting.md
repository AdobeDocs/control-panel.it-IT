---
product: campaign
solution: Campaign
title: Avvisi e-mail
description: Scopri come ricevere notifiche e-mail in caso di problemi relativi alle istanze di Campaign
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# Avvisi e-mail {#email-alerting}

Per garantire una maggiore flessibilità, il Pannello di controllo è dotato di funzionalità di avviso e-mail in tempo reale.

## Elenco degli avvisi {#list}

L’elenco degli avvisi contiene le seguenti categorie di avvisi:

* **Utilizzo dell’archiviazione SFTP**: uno dei server SFTP ha raggiunto o superato l’80% della capacità. Consulta [Gestione dell’archiviazione SFTP](../../sftp/using/sftp-storage-management.md).

* **Utilizzo del database**: uno dei database delle istanze ha raggiunto o superato l’80% della capacità. Consulta [Monitoraggio del database](../../performance-monitoring/using/database-monitoring.md).

* **Scadenza dell’inserimento dell’IP SFTP nell’elenco Consentiti**: uno degli intervalli IP definiti è scaduto o scade entro 10 giorni. Consulta [Inserimento di intervalli IP nell’elenco Consentiti](../../sftp/using/ip-range-allow-listing.md).

* **Scadenza della chiave pubblica SFTP**: una delle chiavi pubbliche definita è scaduta o scadrà entro 10 giorni. Consulta [Gestione delle chiavi](../../sftp/using/key-management.md).

* **Scadenza del certificato SSL**: uno dei certificati SSL dei sottodomini è scaduto o scade entro 30 giorni. Consulta [Monitoraggio dei certificati SSL dei sottodomini](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Inoltre, il Pannello di controllo consente di **impostare i promemoria** per ricevere notifiche tramite e-mail prima che un evento si verifichi sulle istanze (versioni e revisioni dei servizi).
>
>A questo scopo, devi iscriverti agli avvisi e-mail e impostare un promemoria per i prossimi eventi che ti interessano. [Scopri come impostare i promemoria per i prossimi eventi](../../service-events/service-events.md#reminders)

## Iscriversi agli avvisi {#subscribe}

Per iscriverti a questi avvisi, segui questi passaggi:

1. Fai clic sul pulsante **[!UICONTROL Avvisi di notifica]** disponibile in ogni area del Pannello di controllo, quindi fai clic su **[!UICONTROL Iscriviti]**.

   ![](assets/subscribing.png)

1. Viene inviata un’e-mail per confermare l’iscrizione.

   ![](assets/email_subscription.png)

1. Dopo l’iscrizione, il Pannello di controllo invierà una notifica in caso di problemi del sistema, consigliando le azioni da intraprendere. Gli avvisi e-mail vengono inviati a tutti gli utenti che si sono iscritti per **tutte le istanze** di cui sono amministratori.

   ![](assets/alert_sample.png)
