---
product: campaign
solution: Campaign
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scopri come monitorare i certificati SSL dei sottodomini
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 8dce5b9d1eb59b7ebc8ef1f73f7552dcf61077a1
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 91%

---

# Monitoraggio dei certificati SSL dei sottodomini {#monitoring-ssl-certificates}

>[!AVAILABILITY]
>
>Questa funzionalità non è disponibile per Campaign v8.

## Informazioni sui certificati SSL {#about-ssl-certificates}

Adobe Campaign consiglia di proteggere i sottodomini che ospitano le pagine di destinazione, in particolare quelli che raccolgono informazioni riservate dei clienti.

**Crittografia SSL (Secure Socket Layer)** assicura che i sottodomini configurati per lavorare con Adobe siano protetti. Quando il cliente compila un modulo web o visita una pagina di destinazione ospitata da Adobe Campaign, per impostazione predefinita le informazioni vengono inviate tramite un protocollo non sicuro (HTTP). Per garantire ulteriore sicurezza, proteggi le informazioni inviate con un protocollo HTTPS. Ad esempio, l’indirizzo del sottodominio “http://info.mywebsite.com/” sarà “https://info.mywebsite.com/”.

**I certificati SSL non sono installati nei sottodomini configurati**. Sono installati nei sottodomini associati, principalmente quelli che ospitano pagine di destinazione, pagine di risorse e altri.

**I certificati SSL vengono forniti per un periodo di tempo specifico** (1 anno, 60 giorni, ecc.). Una volta scaduto il certificato, potrebbero verificarsi dei problemi durante l’accesso alle pagine di destinazione o l’utilizzo delle risorse del sottodominio. Per evitare questo problema, il Pannello di controllo Campaign ti consente di monitorare i certificati SSL dei sottodomini e di avviare il processo di rinnovo.

![](assets/no_certificate.png)

## Monitoraggio dei certificati SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Dettagli del sottodominio"
>abstract="Recupera informazioni sui certificati SSL dei sottodomini."

Lo stato dei certificati SSL dei sottodomini è disponibile direttamente nell’elenco dei sottodomini selezionando la scheda **[!UICONTROL Subdomains & Certificates]**.

I sottodomini sono organizzati in base alla data di scadenza più vicina del certificato SSL, con informazioni visive sulla scadenza, espressa in giorni:

* **Verde**: il sottodominio non dispone di un certificato che scade nei successivi 60 giorni.
* **Arancione**: uno o più sottodomini dispongono di un certificato che scade nei successivi 60 giorni.
* **Rosso**: uno o più sottodomini dispongono di un certificato che scade nei successivi 30 giorni.
* **Grigio**: nessun certificato installato per il sottodominio.

![](assets/subdomains_list.png)

Per visualizzare ulteriori dettagli su un sottodominio, fai clic sul pulsante **[!UICONTROL Subdomain Details]**.
Viene visualizzato l’elenco di tutti i relativi sottodomini. In genere include i sottodomini di pagine di destinazione, pagine di risorse, ecc..

La scheda **[!UICONTROL Sender info]** fornisce informazioni sulle caselle in entrata configurate (Sender, Reply to, Error email [Mittente, Risposta, E-mail di errore]).

![](assets/subdomain_details.png)

Se uno dei certificati SSL del sottodominio sta per scadere, puoi rinnovarlo direttamente dal Pannello di controllo Campaign. Per ulteriori informazioni, consulta questa sezione: [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>Il rinnovo del certificato dal Pannello di controllo Campaign è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso.

**Argomenti correlati:**

* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
