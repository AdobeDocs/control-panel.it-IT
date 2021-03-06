---
product: campaign
solution: Campaign
title: Monitoraggio dei sottodomini
description: Monitora i sottodomini per assicurarti che siano configurati correttamente per lavorare con Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: fa45ec38ff06a0b02ab724e7ced79b7b5de2c766
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# Monitoraggio dei sottodomini {#monitoring-subdomains}

È essenziale monitorare i sottodomini per garantire che siano configurati correttamente per lavorare con Adobe Campaign.

L’elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando selezioni la **[!UICONTROL Subdomains & Certificates]** il Card.

La **[!UICONTROL Last verification]** indica quando un sottodominio è stato verificato per l’ultima volta. Puoi avviare una verifica in qualsiasi momento facendo clic sul pulsante **...** / **[!UICONTROL Verify subdomain]** pulsante .

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>L’Adobe non consiglia di utilizzare sottodomini privi di data di certificato, in quanto ciò potrebbe significare che questi sottodomini potrebbero avere alcuni problemi di recapito messaggi.

Quando si avvia una verifica, vengono eseguite diverse operazioni per verificare che il sottodominio sia configurato correttamente (controllo del tenant dell’istanza, test di invio dell’e-mail, ecc.)

Se la verifica del sottodominio non riesce, contatta l’Assistenza clienti Adobe per ulteriori indagini.

**Argomenti correlati:**

* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
