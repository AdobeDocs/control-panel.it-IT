---
product: campaign
solution: Campaign
title: Monitoraggio dei sottodomini
description: Monitora i sottodomini per assicurarti che siano tutti configurati correttamente per funzionare con Adobe Campaign.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: 'https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w'
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
source-wordcount: '154'
ht-degree: 100%
---
# Monitorare i sottodomini {#monitoring-subdomains}

È essenziale monitorare i sottodomini per assicurarsi che siano tutti configurati correttamente per funzionare con Adobe Campaign.

L’elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando si seleziona la scheda **[!UICONTROL Sottodomini e certificati]**.

La colonna **[!UICONTROL Ultima verifica]** indica quando un sottodominio è stato verificato per l’ultima volta. Puoi avviare una verifica in qualsiasi momento facendo clic sul pulsante **...** / **[!UICONTROL Verifica sottodominio]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe non consiglia di utilizzare sottodomini senza data di certificato, in quanto questo potrebbe indicare la presenza di problemi di recapitabilità in questi sottodomini.

All’avvio di una verifica, vengono eseguite diverse operazioni per accertarsi che il sottodominio sia configurato correttamente (controllo del tenant dell’istanza, test di invio e-mail, ecc.). Se la verifica del sottodominio non riesce, contatta l’Assistenza clienti di Adobe per ulteriori indagini.

**Argomenti correlati:**

* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
