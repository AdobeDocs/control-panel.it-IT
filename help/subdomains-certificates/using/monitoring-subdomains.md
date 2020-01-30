---
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scoprite come monitorare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: ce15da4aabb0350cb9a60cc16556ffcf691fc3df

---


# Monitoraggio dei sottodomini {#monitoring-subdomains}

È essenziale monitorare i domini secondari per assicurarsi che siano configurati correttamente per l&#39;utilizzo con Adobe Campaign.

L&#39;elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando si seleziona la **[!UICONTROL Subdomains & Certificates]**scheda.

La **[!UICONTROL Last verification]**colonna indica quando un sottodominio è stato verificato per l’ultima volta.** Puoi avviare una verifica in qualsiasi momento facendo clic su **... /**[!UICONTROL Verify subdomain]** pulsante.

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>Adobe non consiglia di utilizzare sottodomini privi di data del certificato, in quanto potrebbe indicare che tali sottodomini potrebbero presentare problemi di recapito.

Quando si avvia una verifica, vengono eseguite diverse operazioni per verificare che il sottodominio sia configurato correttamente (controllo tenant istanza, test di invio e-mail, ecc.)

Se la verifica del sottodominio ha esito negativo, contatta l&#39;Assistenza clienti Adobe per ulteriori indagini.

**Argomenti correlati:**

* [Aggiunta di certificati SSL (video di esercitazione)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marchio dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
