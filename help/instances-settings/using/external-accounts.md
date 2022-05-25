---
product: campaign
solution: Campaign
title: Aggiungi istanze MID/RT (modello ibrido)
description: Scopri come aggiungere istanze MID/RT al Pannello di controllo Campaign con modello di hosting ibrido.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# Aggiungi istanze MID/RT (modello ibrido)

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Account esterni"
>abstract="In questa schermata, i clienti con modello di hosting ibrido possono fornire il loro URL di istanza MID/RT configurato nell’istanza di marketing del Pannello di controllo Campaign, al fine di sfruttare le funzionalità del Pannello di controllo Campaign."

Il Pannello di controllo Campaign consente ai clienti con un modello di hosting ibrido di sfruttare funzionalità specifiche del Pannello di controllo Campaign. A questo scopo, devono fornire l’URL dell’istanza MID/RT configurato nella loro istanza di marketing nel Pannello di controllo Campaign .

Per ulteriori informazioni sui modelli di hosting, consulta [Documentazione di Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Aggiungi un’istanza MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="URL dell’istanza, che si trova nella console client di Campaign nel menu Amministrazione > Piattaforma > Account esterni ."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operatore"
>abstract="ID dell’operatore fornito dopo il provisioning iniziale da parte dell’amministratore di Adobe."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Password"
>abstract="Password dell’operatore fornita dopo il provisioning iniziale da parte dell’amministratore di Adobe."

I clienti ibridi devono connettersi ad Pannelli di controllo Campaign tramite Experience Cloud. Quando si accede al Pannello di controllo Campaign per la prima volta, nella home page vengono visualizzate solo due schede.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Nel caso in cui si verifichino problemi nell’accesso al Pannello di controllo Campaign, è molto probabile che l’istanza di marketing non sia ancora stata mappata con il tuo ID organizzazione. Contatta l&#39;Assistenza clienti per completare la configurazione e procedere ulteriormente. Una volta stabilita la connessione, verrà visualizzata la homepage del Pannello di controllo Campaign.

Per poter accedere alle funzionalità del Pannello di controllo Campaign, devi fornire le informazioni sull’istanza MID/RT nel **[!UICONTROL Instances Settings]** il Card. Per farlo, segui la procedura indicata di seguito.

1. In **[!UICONTROL Instances Settings]** scheda , seleziona **[!UICONTROL External Accounts]** scheda .

1. Seleziona l’istanza di marketing desiderata dall’elenco a discesa, quindi fai clic su **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Fornisci informazioni sull’istanza MID/RT da aggiungere.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL dell’istanza, che si trova nella console client di Campaign nella **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** menu.

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credenziali dell’operatore fornite dopo il provisioning iniziale da parte dell’amministratore di Adobe.

      >[!NOTE]
      >
      >Se tali dettagli non sono disponibili, contatta l’Assistenza clienti.

1. Fai clic su **[!UICONTROL Save]** per confermare.

Quando si aggiunge un URL MID/RT, viene attivato un processo asincrono per convalidare la correttezza degli URL. Questo processo potrebbe richiedere alcuni minuti. Fino a quando l’URL dell’istanza MID/RT non viene convalidato, il processo sarà in sospeso. Solo una volta completata la convalida, puoi accedere alle funzionalità principali del Pannello di controllo Campaign.

![](assets/external-account-pending.png)

Puoi rimuovere o disattivare l’URL di un’istanza MID/RT in qualsiasi momento selezionandolo dall’elenco.

![](assets/external-account-edit.png)

Puoi monitorare qualsiasi azione eseguita nel **[!UICONTROL External Accounts]** scheda su un URL di un’istanza MID/RT dal **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Funzionalità disponibili per i clienti ibridi {#capabilities}

Una volta aggiunta un’istanza MID/RT al Pannello di controllo Campaign, puoi sfruttare le funzionalità elencate di seguito:

* [Monitorare eventi e contatti chiave](../../service-events/service-events.md)
* [Visualizza i dettagli dell’istanza](../../instances-settings/using/instance-details.md),
* [Aggiungi indirizzi IP all’elenco consentiti](../../instances-settings/using/ip-allow-listing-instance-access.md) (per le istanze RT),
* [Visualizzare informazioni sui sottodomini delegati](../../subdomains-certificates/using/monitoring-subdomains.md),
* [Visualizza informazioni sui certificati SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).