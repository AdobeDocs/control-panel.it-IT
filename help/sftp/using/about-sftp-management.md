---
product: campaign
solution: Campaign
title: Informazioni sulla gestione SFTP
description: Ulteriori informazioni sulla gestione SFTP nel Pannello di controllo
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%

---

# Informazioni sulla gestione SFTP {#about-sftp-management}

Nel Pannello di controllo, puoi interagire con tutti i server SFTP collegati alle istanze di Campaign a cui hai accesso. La maggior parte delle istanze dispone di server SFTP connessi (in alcuni casi, le istanze di sviluppo e stage potrebbero non essere collegate ad alcun server SFTP).

L’accesso ai server SFTP viene effettuato utilizzando un software client SFTP, che puoi trovare e scaricare online. Per connettersi a un server tramite tale applicazione client o un’API, è necessario impostare una chiave SSH pubblica e aggiungere all’elenco Consentiti l’indirizzo IP che si connette al server SFTP.

Per gestire i server SFTP, il Pannello di controllo consente di eseguire le seguenti azioni:

* monitorare la **capacità di archiviazione**,
* gestire l’**Inserimento di indirizzi IP nell’elenco Consentiti**, aggiungere o eliminare intervalli di indirizzi IP per uno o più server,
* gestire le **chiavi SSH pubbliche** per accedere ai server.

Informazioni dettagliate su ciascuna di queste azioni sono disponibili nelle sezioni seguenti.
