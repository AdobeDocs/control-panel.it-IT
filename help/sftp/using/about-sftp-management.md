---
product: campaign
solution: Campaign
title: Informazioni sulla gestione SFTP
description: Ulteriori informazioni sulla gestione SFTP nel Pannello di controllo Campaign
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# Informazioni sulla gestione SFTP {#about-sftp-management}

Nel Pannello di controllo Campaign, puoi interagire con tutti i server SFTP collegati alle istanze di Campaign a cui hai accesso. La maggior parte delle istanze dispone di server SFTP connessi (in alcuni casi, le istanze di sviluppo e stage potrebbero non essere connesse ad alcun server SFTP).

L&#39;accesso ai server SFTP viene effettuato utilizzando un software client SFTP, che puoi trovare e scaricare online. Per connettersi a un server tramite tale applicazione client o un’API, è necessario impostare una chiave SSH pubblica e aggiungere all’elenco consentiti l’indirizzo IP che si connette al server SFTP.

Il pannello di controllo consente di eseguire le azioni seguenti per gestire i server SFTP:

* Monitorare **capacità di archiviazione**,
* Gestisci **Inserimento di indirizzi IP nell’elenco Consentiti**: aggiungere o eliminare intervalli di indirizzi IP per uno o più server,
* Gestisci **chiavi SSH pubbliche** per accedere ai server.

Informazioni dettagliate su ciascuna di queste azioni sono disponibili nelle sezioni seguenti.
