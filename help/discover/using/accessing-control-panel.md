---
product: campaign
solution: Campaign
title: Accesso al Pannello di controllo
description: Scopri come accedere al Pannello di controllo
feature: Control Panel, Access Management
role: Admin
level: Experienced
exl-id: eb67af6e-a64e-49a7-9656-782f91bc1d67
TQID: https://experienceleague.adobe.com/Ug0vHjgyTK-BRO4IMdCwSQuiwO--XagzjW-MFTPcZrY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 57345245341bf2d04b9b01611d502532ba8f175b
workflow-type: ht
source-wordcount: 353
ht-degree: 100%

---

# Accesso al Pannello di controllo {#accessing-control-panel}

Il Pannello di controllo è disponibile direttamente da Experience Cloud o dal prodotto stesso.

## Prerequisiti {#prerequisites}

Per Campaign v7/v8, tieni presente che l’istanza deve essere ospitata su Amazon Web Services (AWS) e aggiornata all’ultima [versione stabile di Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=it#rn-statuses) o alla versione 9032 o superiore. Scopri come controllare la versione in [questa sezione](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=it#getting-your-campaign-version). Per verificare se l’istanza è ospitata su AWS, segui i passaggi descritti in [questa sezione](../../faq.md#hosted-aws).

Anche le istanze di Campaign v8 ospitate su Microsoft Azure hanno accesso a un sottoinsieme di funzionalità del Pannello di controllo: [inserimento di IP nell&#39;elenco Consentiti per l’accesso alle istanze](../../instances-settings/using/ip-allow-listing-instance-access.md), [inserimento di IP nell’elenco Consentiti per i server SFTP](../../sftp/using/ip-range-allow-listing.md) e [gestione dei certificati SSL gestiti dal cliente](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>Per impostazione predefinita, il Pannello di controllo è accessibile agli utenti amministratori che appartengono al profilo di prodotto “Amministratori”. In base alla configurazione della tua organizzazione, il profilo di prodotto può essere denominato in modo diverso (“admin”, “amministratori”, “admin di approvazione”, ecc.). **I profili di prodotto il cui nome contiene la parola “admin” nel nome concedono automaticamente l’accesso al Pannello di controllo**. Esamina attentamente la denominazione del profilo di prodotto affinché solo gli utenti autorizzati abbiano accesso al Pannello di controllo. [Scopri come gestire le autorizzazioni nel Pannello di controllo](../../discover/using/managing-permissions.md).

## Accedere da Experience Cloud Platform {#access-experience-cloud-platform}

Per accedere al Pannello di controllo da Adobe Experience Cloud Platform, segui la procedura indicata di seguito.

1. Accedi alla [pagina Home di Experience Cloud](https://experiencecloud.adobe.com/){target="_blank"}.

1. Fai clic sul collegamento dedicato nella sezione **Accesso rapido**.

   ![](assets/do-not-localize/quickaccess.png)

Il Pannello di controllo è accessibile anche dal **selettore soluzioni** di Experience Cloud Platform:

1. Dalla [pagina Home di Adobe Experience Cloud](https://experiencecloud.adobe.com/){target="_blank"}, seleziona **Campaign** dalla sezione **Accesso rapido** o nel menu in alto a destra.

   ![](assets/do-not-localize/control_panel_access1.png)

1. Viene visualizzato l’elenco delle istanze di Campaign. Fai clic sulla scheda **Pannello di controllo** per avviarlo.

   ![](assets/do-not-localize/control_panel_access2.png)

## Accedere dal prodotto {#access-product}

>[!NOTE]
>
>L’accesso dall’interno del prodotto è disponibile solo per [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=it){target="_blank"}.

1. Apri il prodotto Campaign Standard.

1. Seleziona il menu **[!UICONTROL Amministrazione]** dal riquadro **Navigazione**.

   ![](assets/control_panel_access3.png)

1. Fai clic sull’icona **[!UICONTROL Pannello di controllo]**.

   ![](assets/control_panel_access4.png)
