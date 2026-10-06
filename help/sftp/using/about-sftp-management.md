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
TQID: 'https://experienceleague.adobe.com/UZHhTNCld6p1RFGh3DY-2r3VRiLNxCtP0anuPxPnWVE'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e8445399-14db-4931-a0bb-477780230387
    internal-label: SFTP Management
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
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
