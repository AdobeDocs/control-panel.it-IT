---
product: campaign
solution: Campaign
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scopri come monitorare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 16%

---


# Monitoraggio dei sottodomini {#monitoring-subdomains}

È essenziale monitorare i sottodomini per assicurarsi che siano configurati correttamente per lavorare con  Adobe Campaign.

L&#39;elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando si seleziona la scheda **[!UICONTROL Subdomains & Certificates]**.

La colonna **[!UICONTROL Last verification]** indica quando un sottodominio è stato verificato per l&#39;ultima volta. È possibile avviare una verifica in qualsiasi momento facendo clic su **...Pulsante** / **[!UICONTROL Verify subdomain]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
> Adobe non consiglia di utilizzare sottodomini senza data certificato, in quanto potrebbe significare che tali sottodomini potrebbero presentare alcuni problemi di recapito.

Quando si avvia una verifica, vengono eseguite diverse operazioni per verificare che il sottodominio sia configurato correttamente (controllo tenant istanza, test di invio e-mail, ecc.)

Se la verifica del sottodominio ha esito negativo, contatta  Assistenza clienti del Adobe per ulteriori indagini.

**Argomenti correlati:**

* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
