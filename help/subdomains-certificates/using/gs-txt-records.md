---
product: campaign
solution: Campaign
title: Gestione dei record TXT
description: Scopri come gestire i record TXT per la verifica della proprietà del dominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# Introduzione ai record TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gestione dei record TXT"
>abstract="I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne. Il Pannello di controllo Campaign consente di aggiungere tre tipi di record ai sottodomini: Google Site Verification, DMARC e BIMI."

## Informazioni sui record TXT {#about}

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da origini esterne. Pannello di controllo Campaign consente di aggiungere tre tipi di record ai sottodomini:

* **Record TXT di Google** ti consente di attestare di essere il proprietario del dominio, garantendo elevate percentuali di posta in arrivo e basse percentuali di posta indesiderata per le e-mail. [Scopri come aggiungere record TXT di Google](managing-txt-records.md)
* **Record DMARC** fornire un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi. [Scopri come aggiungere record DMARC](dmarc.md)
* **Record BIMI** consente di visualizzare un logo approvato accanto alle e-mail nelle caselle in entrata dei provider di caselle postali per migliorare il riconoscimento e l’affidabilità del marchio. [Scopri come aggiungere record BIMI](bimi.md)

## Monitorare i record dei sottodomini {#monitor}

Puoi monitorare tutti i record TXT aggiunti per ciascun sottodominio accedendo ai dettagli dei sottodomini.

In questa schermata vengono visualizzati tutti i record di tipo TXT per il sottodominio selezionato, con le informazioni nella colonna &quot;Valore&quot; sulla relativa configurazione. Per eliminare un record TXT, DMARC o BIMI di Google, fai clic sul pulsante con i puntini di sospensione e seleziona Elimina. Se necessario, puoi anche modificare i record DMARC e BIMI.

![](assets/txt-records.png)
