---
product: campaign
solution: Campaign
title: Rinnovo del certificato SSL di un sottodominio
description: Scopri come rinnovare i certificati SSL dei sottodomini
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: ht
source-wordcount: '228'
ht-degree: 100%

---

# Rinnovo di un certificato SSL {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Rinnovo del certificato SSL"
>abstract="Per rinnovare un certificato SSL, devi generare una richiesta di firma del certificato (CSR, Certificate Signing Request), acquistare il certificato SSL per i tuoi sottodomini e installare il Bundle certificati."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=it#geberating-csr" text="Generazione di una richiesta di firma del certificato (CSR, Certificate Signing Request)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=it#installing-ssl-certificate" text="Installazione di un certificato SSL"

Il processo di rinnovo del certificato SSL comprende 3 passaggi:

1. **Generazione della richiesta di firma del certificato (CSR, Certificate Signing Request)**

   La richiesta di firma del certificato (CSR, Certificate Signing Request) deve essere generata per l’istanza e i sottodomini che intendi proteggere prima di acquistare un certificato.  Per generare la CSR dovrai fornire alcune informazioni (ad esempio nome comune, nome e indirizzo dell’organizzazione, ecc.). [Ulteriori informazioni](generate-csr.md)

1. **Acquisto del certificato SSL**

   Una volta generata la CSR, puoi utilizzarla per acquistare il certificato SSL dall’autorità di certificazione approvata dalla tua azienda.

1. **Installazione del certificato SSL**

   Installa il certificato SSL acquistato nel sottodominio desiderato per proteggerlo. [Ulteriori informazioni](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Scopri questa funzione nel video per [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=it#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=it#adding-ssl-certificates)

**Argomenti correlati:**

* [Guida alle best practice per il recapito messaggi - Processo di richiesta del certificato SSL per Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=it)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)
