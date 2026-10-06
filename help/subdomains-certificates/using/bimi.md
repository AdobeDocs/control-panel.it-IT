---
product: campaign
solution: Campaign
title: Aggiungere record BIMI
description: Scopri come aggiungere un record BIMI per un sottodominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
TQID: 'https://experienceleague.adobe.com/gdmtHgMWI-8y3w6uzXdNxOatrjJMDdp6EWLuXz1mhhg'
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 100%
---
# Aggiungere record BIMI {#dmarc}

## Informazioni sui record BIMI {#about}

Brand Indicators for Message Identification (BIMI) è uno standard di settore che consente la visualizzazione di un logo approvato accanto all’e-mail di un mittente, nelle caselle di posta in arrivo dei provider di posta elettronica, in modo da migliorare il riconoscimento e l’affidabilità del brand.

Informazioni dettagliate sull’attuazione di BIMI sono disponibili nella [Guida alle best practice per la recapitabilità di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html?lang=it)

![](assets/bimi-example.png){width="70%" align="center"}

## Limitazioni e prerequisiti {#limitations}

* I record SPF, DKIM e DMARC sono prerequisiti per la creazione di un record BIMI.

* Il record BIMI deve essere pubblicato nel DNS, per un dominio completamente delegato, ciò è possibile tramite il Pannello di controllo. [Ulteriori informazioni sui metodi di configurazione dei sottodomini](subdomains-branding.md#subdomain-delegation-methods)

* Prerequisiti per i record DMARC:

  * Il tipo di criterio del record per il dominio organizzativo deve essere impostato su “Quarantena” o “Rifiuta”. La creazione di record BIMI non è disponibile con un tipo di criterio DMARC impostato su “Nessuno”.
  * La percentuale di e-mail a cui viene applicato il criterio DMARC deve essere 100%. BIMI non supporta i criteri DMARC con questa percentuale impostata su un valore inferiore al 100%.

    [Scopri come configurare i record DMARC](dmarc.md)

## Aggiungere un record BIMI per un sottodominio {#add}

Per aggiungere un record BIMI per un sottodominio, segui questi passaggi:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Dettagli sottodominio]**.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi record TXT]**, quindi scegli **[!UICONTROL BIMI]** dall’elenco a discesa **[!UICONTROL Tipo di record]**.

   ![](assets/bimi-add.png)

1. Il campo **[!UICONTROL Selettore]** consente di specificare un selettore BIMI per il record. Un selettore BIMI è un identificatore univoco che puoi assegnare a un record BIMI. Questo consente di definire più loghi per un determinato sottodominio. Al momento questo servizio non è supportato dai provider di posta elettronica.

1. Nel campo **[!UICONTROL URL logo aziendale]**, specifica l’URL del file SVG che contiene il logo.

1. Anche se l’**[!UICONTROL URL del certificato]** è facoltativo, è necessario per alcuni provider di posta elettronica come Gmail e Apple. Pertanto, è consigliabile ottenere un certificato VMC (Verified Mark Certificate) per sfruttare al meglio BIMI.

   +++In che modo si ottiene un VMC?

   I passaggi principali per ottenere un VMC sono i seguenti:

   1. Registra il logo del tuo brand come marchio registratio presso un ufficio per la proprietà intellettuale riconosciuto dagli emittenti VMC. Se disponi di un team legale, ti consigliamo di collaborare con loro per ottenere il marchio registrato del tuo logo o per verificare che sia già registrato.

   1. Dopo aver verificato che il logo è stato registrato, contatta DigiCert o un’autorità di certificazione (CA) incaricata per richiedere un VMC.

   1. Una volta approvato il VMC, riceverai un certificato di entità PEM (Privacy Enhanced Mail). Aggiungi al file PEM tutti gli altri certificati intermedi ricevuti dall’autorità di certificazione. Carica il file PEM (insieme ai file aggiunti) sul server web pubblico e annotane l’URL. Tale URL verrà utilizzato nel record TXT di BIMI.

   1. Una volta che il record BIMI è visibile nella pagina dei dettagli del sottodominio per un determinato sottodominio, puoi utilizzare lo strumento Bimi Inspector disponibile [qui](https://bimigroup.org/bimi-generator/) per verificare il corretto funzionamento del record BIMI.

   Informazioni dettagliate sull’implementazione di BIMI sono disponibili nella [Documentazione standard di BIMI](https://bimigroup.org/implementation-guide/)
   +++

1. Fai clic su **[!UICONTROL Aggiungi]** per confermare la creazione del record BIMI.

Una volta elaborata la creazione del record BIMI (circa 5 minuti), questo viene mostrato nella schermata dei dettagli dei sottodomini. [Scopri come monitorare i record TXT per i sottodomini](gs-txt-records.md#monitor)
