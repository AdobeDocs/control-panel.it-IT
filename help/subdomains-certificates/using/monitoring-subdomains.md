---
product: campaign
solution: Campaign
title: Monitoraggio dei sottodomini
description: Monitora i sottodomini per assicurarti che siano tutti configurati correttamente per funzionare con Adobe Campaign.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: ht
source-wordcount: 154
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
