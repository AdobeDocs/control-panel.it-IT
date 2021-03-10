---
product: campaign
solution: Campaign
title: Informazioni sulla gestione SFTP
description: Ulteriori informazioni sulla gestione SFTP nel Pannello di controllo Campaign
testing: SSECD-836 2
feature: 'Pannello di controllo Campaign   '
role: Architetto
level: Intermedio
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# Informazioni sulla gestione SFTP {#about-sftp-management}

Nel Pannello di controllo Campaign, puoi interagire con tutti i server SFTP collegati alle istanze Campaign a cui hai accesso. La maggior parte delle istanze dispone di server SFTP connessi (in alcuni casi, le istanze di sviluppo e stage potrebbero non essere connesse ad alcun server SFTP).

L&#39;accesso ai server SFTP viene effettuato utilizzando un software client SFTP, che puoi trovare e scaricare online. Per connettersi a un server tramite tale applicazione client o un’API, è necessario impostare una chiave SSH pubblica e aggiungere all’elenco consentiti l’indirizzo IP che si connette al server SFTP.

Il pannello di controllo consente di eseguire le azioni seguenti per gestire i server SFTP:

* Monitora la loro **capacità di archiviazione**,
* Gestisci **gli indirizzi IP consentiti**: aggiungere o eliminare intervalli di indirizzi IP per uno o più server,
* Gestisci **chiavi SSH pubbliche** per accedere ai tuoi server.

Informazioni dettagliate su ciascuna di queste azioni sono disponibili nelle sezioni seguenti.
