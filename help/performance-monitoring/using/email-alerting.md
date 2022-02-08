---
product: campaign
solution: Campaign
title: Avvisi e-mail
description: Scopri come ricevere notifiche e-mail in caso di problemi con le istanze di Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 65f4603e6ff6c232479bf567981871e92b1cfa1c
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Avvisi e-mail {#email-alerting}

Per offrire una maggiore flessibilità al tuo lavoro, il Pannello di controllo Campaign è dotato di funzionalità di avviso e-mail in tempo reale.

Per abbonarti a questi avvisi, segui questi passaggi:

1. Fai clic sul pulsante **[!UICONTROL Alerting notifications]** pulsante disponibile in qualsiasi posizione del Pannello di controllo Campaign, quindi fare clic su **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Viene inviata un’e-mail per confermare l’abbonamento.

   ![](assets/email_subscription.png)

1. Dopo l&#39;iscrizione, il Pannello di controllo Campaign invierà una notifica dei problemi di sistema e raccomanderà le azioni da intraprendere. Gli avvisi e-mail vengono inviati a tutti coloro che si sono registrati per **tutte le istanze** di cui sono amministratori.

   ![](assets/alert_sample.png)

L&#39;elenco degli avvisi è il seguente:

* **Utilizzo dell’archiviazione SFTP**: Uno dei server SFTP ha raggiunto l’80% o più della sua capacità. Vedi [Gestione dell’archiviazione SFTP](../../sftp/using/sftp-storage-management.md).

* **Utilizzo del database**: Uno dei database delle istanze ha raggiunto l&#39;80% o più della sua capacità. Vedi [Monitoraggio del database](../../performance-monitoring/using/database-monitoring.md).

* **Scadenza certificato SSL**: Uno dei certificati SSL di uno dei sottodomini è scaduto o scadrà tra 60 giorni o meno. Vedi [Monitoraggio dei certificati SSL dei sottodomini](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **Scadenza dell’inserimento di IP SFTP**: Uno degli intervalli IP definiti è scaduto o scadrà tra 10 giorni o meno. Vedi [Inserimento di intervalli IP nell’elenco Consentiti](../../sftp/using/ip-range-allow-listing.md).

* **Scadenza della chiave pubblica SFTP**: Una delle chiavi pubbliche definite è scaduta o scadrà tra 10 giorni o meno. Vedi [Gestione delle chiavi](../../sftp/using/key-management.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->