---
product: campaign
solution: Campaign
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scopri come monitorare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 24%

---


# Monitoraggio dei sottodomini {#monitoring-subdomains}

È essenziale monitorare i sottodomini per assicurarsi che siano configurati correttamente per lavorare con  Adobe Campaign.

L&#39;elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando si seleziona la **[!UICONTROL Subdomains & Certificates]** scheda.

La **[!UICONTROL Last verification]** colonna indica quando un sottodominio è stato verificato per l’ultima volta. Puoi avviare una verifica in qualsiasi momento facendo clic su **...** / **[!UICONTROL Verify subdomain]** pulsante.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
> Adobe non consiglia di utilizzare sottodomini senza data certificato, in quanto potrebbe significare che tali sottodomini potrebbero presentare alcuni problemi di recapito.

Quando si avvia una verifica, vengono eseguite diverse operazioni per verificare che il sottodominio sia configurato correttamente (controllo tenant istanza, test di invio e-mail, ecc.)

Se la verifica del sottodominio ha esito negativo, contatta  Assistenza clienti del Adobe per ulteriori indagini.

**Argomenti correlati:**

* [Aggiunta di certificati SSL (video tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
