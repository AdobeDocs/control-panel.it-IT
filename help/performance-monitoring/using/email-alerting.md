---
product: campaign
solution: Campaign
title: Avvisi e-mail
description: Scopri come ricevere le notifiche e-mail in caso di problemi con le istanze di Campaign
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Avvisi e-mail {#email-alerting}

Per offrire maggiore flessibilità al lavoro, il Pannello di controllo Campaign è dotato di funzionalità di avvisi e-mail in tempo reale.

Per effettuare la sottoscrizione a questi avvisi, procedere come segue:

1. Fate clic sul **[!UICONTROL Alerting notifications]** pulsante disponibile in qualsiasi posizione del Pannello di controllo Campaign, quindi fate clic su **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Viene inviato un messaggio e-mail di conferma dell’iscrizione.

   ![](assets/email_subscription.png)

1. Dopo l&#39;iscrizione, il Pannello di controllo Campaign notifica i problemi del sistema e consiglia le azioni da intraprendere. Gli avvisi e-mail vengono inviati a tutti gli utenti che si sono registrati per **tutte le istanze** di cui sono amministratori.

   ![](assets/alert_sample.png)


L&#39;elenco degli avvisi è il seguente:

* **Utilizzo** dell&#39;archivio SFTP: Uno dei server SFTP ha raggiunto l&#39;80% o più della capacità. See [SFTP storage management](../../sftp/using/sftp-storage-management.md).

* **Uso** del database: Uno dei database delle istanze ha raggiunto l&#39;80% o più della capacità. Vedere Monitoraggio [del](../../performance-monitoring/using/database-monitoring.md)database.

* **Scadenza** certificato SSL: Uno dei certificati SSL di uno dei sottodomini è scaduto o scadrà tra 60 giorni o meno. See [Monitoring subdomains&#39; SSL certificates](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

