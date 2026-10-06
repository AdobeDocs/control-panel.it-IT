---
product: campaign
solution: Campaign
title: Gestione dei record TXT
description: Scopri come gestire i record TXT per la verifica della proprietà del dominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# Introduzione ai record TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gestione dei record TXT"
>abstract="I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne. Il Pannello di controllo consente di aggiungere tre tipi di record ai sottodomini: Google Site Verification, DMARC e BIMI."

## Informazioni sui record TXT {#about}

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne. Il Pannello di controllo consente di aggiungere tre tipi di record ai sottodomini:

* I **record TXT di Google** ti consentono di attestare di essere il proprietario del dominio, garantendo elevate percentuali di posta in arrivo e basse percentuali di posta indesiderata per le e-mail. [Scopri come aggiungere record TXT di Google](managing-txt-records.md)
* I **record DMARC** forniscono un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi. [Scopri come aggiungere record DMARC](dmarc.md)
* I **record BIMI** ti consentono di visualizzare un logo approvato accanto alle e-mail nelle caselle in entrata dei provider di casette postali per migliorare il riconoscimento e l’affidabilità del brand. [Scopri come aggiungere record BIMI](bimi.md)

## Monitorare i record dei sottodomini {#monitor}

Puoi monitorare tutti i record TXT aggiunti per ciascun sottodominio accedendo ai dettagli dei sottodomini.

In questa schermata vengono visualizzati tutti i record di tipo TXT per il sottodominio selezionato, con le informazioni sulla relativa configurazione nella colonna “Valore”. Per eliminare un record TXT, DMARC o BIMI di Google, fai clic sul pulsante con i puntini di sospensione e seleziona Elimina. Se necessario, puoi anche modificare i record DMARC e BIMI.

![](assets/txt-records.png)
