---
product: campaign
solution: Campaign
title: Aggiungi record BIMI
description: Scopri come aggiungere un record BIMI per un sottodominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0ad4c1f12eb035c8d543777be2a8806d507be5be
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Aggiungi record BIMI {#dmarc}

## Informazioni sui record BIMI {#about}

Brand Indicators for Message Identification (BIMI) è uno standard di settore che consente la visualizzazione di un logo approvato accanto all’e-mail di un mittente nelle caselle in entrata dei provider di caselle postali per migliorare il riconoscimento e l’affidabilità del brand. Aiuta a prevenire lo spoofing e il phishing delle e-mail verificando l’identità del mittente tramite l’autenticazione DMARC, rendendo più difficile per gli attori malintenzionati impersonare marchi legittimi nelle e-mail. Informazioni dettagliate sull’attuazione di BIMI sono disponibili all’indirizzo [Guida alle procedure consigliate per la consegna dei messaggi di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## Limitazioni e prerequisiti {#limitations}

* I record SPF, DKIM e DMARC sono prerequisiti per la creazione di un record BIMI.
* I record BIMI possono essere aggiunti solo per i sottodomini che utilizzano la delega completa dei sottodomini. [Ulteriori informazioni sui metodi di configurazione dei sottodomini](subdomains-branding.md#subdomain-delegation-methods)
* Prerequisiti per i record DMARC:

   * Il tipo di criterio di record per il sottodominio deve essere impostato su &quot;Quarantena&quot; o &quot;Rifiuta&quot;. La creazione di record BIMI non è disponibile con un tipo di criterio DMARC impostato su &quot;None&quot;.
   * La percentuale di e-mail a cui viene applicato il criterio DMARC deve essere 100%. BIMI non supporta i criteri DMARC con questa percentuale impostata su un valore inferiore al 100%.

[Scopri come configurare i record DMARC](dmarc.md)

## Aggiungere un record BIMI per un sottodominio {#add}

Per aggiungere un record BIMI per un sottodominio, effettua le seguenti operazioni:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Subdomain details]**.

1. Fai clic su **[!UICONTROL Add TXT record]** , quindi scegliere **[!UICONTROL BIMI]** dal **[!UICONTROL Record type]** elenco a discesa.

   ![](assets/bimi-add.png)

1. In **[!UICONTROL Company Logo URL]**, specifica l’URL del file SVG contenente il logo.

1. Il **[!UICONTROL Certificate URL]** è facoltativo. Ti consente di aggiungere un URL VMC (Verified Mark Certificate) per attestare che la tua organizzazione è il proprietario legale del logo, al fine di evitare che spammer e altri utenti malintenzionati utilizzino logo del brand di cui non sono proprietari.

   +++Come si ottiene un VMC?

   I passaggi principali per ottenere un VMC sono i seguenti:

   1. Registra il logo del tuo marchio come marchio presso un ufficio per la proprietà intellettuale riconosciuto dagli emittenti VMC. Se hai un team legale, ti consigliamo di collaborare con loro per ottenere il marchio registrato del tuo logo o per verificare che sia già registrato.

   1. Dopo aver verificato che il logo sia registrato, contattare DigiCert o Entrust Certificate Authority (CA) per richiedere un VMC.

   1. Una volta approvato il proprio VMC, si riceverà un certificato di entità PEM (Privacy Enhanced Mail). Aggiungere al file PEM tutti gli altri certificati intermedi ricevuti dalla CA. Carica il file PEM (insieme ai file aggiunti) sul server web pubblico e annota l’URL del file PEM. Utilizzerai l’URL nel tuo record TXT di BIMI.

   Informazioni dettagliate sull’attuazione di BIMI sono disponibili nella [Documentazione standard BIMI](https://bimigroup.org/implementation-guide/)
+++

1. Clic **[!UICONTROL Add]** per confermare la creazione del record BIMI.

Una volta elaborata la creazione del record BIMI (circa 5 minuti), questo viene visualizzato nella schermata dei dettagli dei sottodomini. [Scopri come monitorare i record TXT per i sottodomini](gs-txt-records.md#monitor)
