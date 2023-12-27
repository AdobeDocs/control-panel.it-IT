---
product: campaign
solution: Campaign
title: Aggiungere istanze MID/RT (modello ibrido)
description: Scopri come aggiungere istanze MID/RT al Pannello di controllo con un modello di hosting ibrido.
feature: Control Panel, Access Management
role: Admin
level: Intermediate
exl-id: ff64acbe-d8cb-499b-b20f-b0934fb0f695
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '567'
ht-degree: 100%

---

# Aggiungere istanze MID/RT (modello ibrido){#add-mid-rt-instances-hybrid-model}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Account esterni"
>abstract="In questa schermata, i clienti con modello di hosting ibrido possono fornire l’URL dell’istanza MID/RT configurato nell’istanza marketing del Pannello di controllo, al fine di sfruttarne le funzionalità."

Il Pannello di controllo consente ai clienti con un modello di hosting ibrido di sfruttarne le funzionalità specifiche. A questo scopo, è necessario:

* [Fornire l’URL dell’istanza MID/RT](#add) configurato nella tua istanza di marketing nel Pannello di controllo.
* [Aggiungere l’indirizzo IP dell’istanza MID/RT all’elenco Consentiti](#ip) per consentire all’istanza di marketing di connettersi ad essa.

Per ulteriori informazioni sui modelli di hosting, consulta la [documentazione di Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html?lang=it).

## Aggiungere un’istanza MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="URL dell’istanza, accessibile nella console client di Campaign dal menu Administration > Platform > External Accounts (Amministrazione > Platform > Account esterni)."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operatore"
>abstract="ID dell’operatore fornito dopo il provisioning iniziale da Adobe Admin."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Password"
>abstract="Password dell’operatore fornita dopo il provisioning iniziale da Adobe Admin."

I clienti ibridi devono connettersi al Pannello di controllo tramite Experience Cloud. Quando si accede al Pannello di controllo per la prima volta, nella pagina home vengono visualizzate solo due schede.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Nel caso riscontrassi problemi durante l’accesso al Pannello di controllo, è probabile che l’istanza marketing non sia ancora stata mappata con il tuo [ID organizzazione](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=it). Contatta l’Assistenza clienti per completare la configurazione e procedere. Una volta stabilita la connessione, verrà visualizzata la pagina home del Pannello di controllo.

Per poter accedere alle funzionalità del Pannello di controllo, devi fornire le informazioni sull’istanza MID/RT nella scheda **[!UICONTROL Impostazioni istanze]**. A tale scopo, segui la procedura indicata di seguito.

1. Nella scheda **[!UICONTROL Impostazioni istanze]**, seleziona la scheda **[!UICONTROL Account esterni]**.

1. Seleziona l’istanza marketing desiderata dall’elenco a discesa, quindi fai clic su **[!UICONTROL Aggiungi nuovo URL]**.

   ![](assets/external-account-addbutton.png)

1. Fornisci le informazioni relative all’istanza MID/RT da aggiungere.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL dell’istanza, accessibile nella console client di Campaign dal menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Piattaforma]** > **[!UICONTROL Account esterni]**.

     ![](assets/external-account-url.png)

   * **[!UICONTROL Operatore]** / **[!UICONTROL Password]**: credenziali dell’operatore fornite dopo il provisioning iniziale da Adobe Admin.

     >[!NOTE]
     >
     >Se tali dettagli non sono disponibili, contatta l’Assistenza clienti.

1. Fai clic su **[!UICONTROL Salva]** per confermare.

Quando si aggiunge un URL MID/RT, viene attivato un processo asincrono per convalidare la correttezza degli URL. Questo processo potrebbe richiedere alcuni minuti. Fino a quando l’URL dell’istanza MID/RT non viene convalidato, il lavoro risulterà in sospeso. Al completamento della convalida, potrai accedere alle funzionalità principali del Pannello di controllo.

![](assets/external-account-pending.png)

Puoi rimuovere o disattivare l’URL di un’istanza MID/RT in qualsiasi momento selezionandolo dall’elenco.

![](assets/external-account-edit.png)

Inoltre, puoi monitorare qualsiasi azione eseguita nella scheda **[!UICONTROL Account esterni]** sull’URL di un’istanza MID/RT da **[!UICONTROL Registri dei processi]**:

![](assets/external-account-logs.png)

## Aggiungere l’indirizzo IP all’elenco Consentiti {#ip}

Una volta che l’istanza MID/RT è stata aggiunta, è necessario aggiungere il relativo IP all’elenco Consentiti in modo che l’istanza di marketing possa connettersi ad essa.

Questa operazione può essere eseguita dalla scheda **[!UICONTROL Elenco indirizzi IP consentiti]** nella scheda **[!UICONTROL Impostazioni istanze]**. [Scopri come aggiungere indirizzi IP all’elenco Consentiti](ip-allow-listing-instance-access.md)

Al termine della procedura, potrai utilizzare le funzionalità del Pannello di controllo con la tua istanza MID/RT.

## Funzionalità disponibili per i clienti ibridi {#capabilities}

Una volta aggiunta un’istanza MID/RT al Pannello di controllo, puoi sfruttare le funzionalità elencate di seguito:

* [Monitorare eventi e contatti chiave](../../service-events/service-events.md)
* [Visualizzare i dettagli dell’istanza](../../instances-settings/using/instance-details.md)
* [Aggiungere indirizzi IP all’elenco Consentiti](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Configurare nuovi sottodomini](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Rinnovare i certificati SSL dei sottodomini](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
