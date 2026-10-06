---
product: campaign
solution: Campaign
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scopri come monitorare i certificati SSL dei sottodomini
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
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
source-wordcount: '578'
ht-degree: 100%
---
# Monitoraggio dei certificati SSL dei sottodomini {#monitoring-ssl-certificates}

## Informazioni sui certificati SSL {#about-ssl-certificates}

Adobe Campaign consiglia di proteggere i sottodomini che ospitano le pagine di destinazione, in particolare quelli che raccolgono informazioni riservate dei clienti.

La **crittografia SSL (Secure Socket Layer)** garantisce che i sottodomini configurati per utilizzare Adobe siano protetti. Quando il cliente compila un modulo web o visita una pagina di destinazione ospitata da Adobe Campaign, per impostazione predefinita le informazioni vengono inviate tramite un protocollo non sicuro (HTTP). Per garantire ulteriore sicurezza, proteggi le informazioni inviate con un protocollo HTTPS. Ad esempio, l’indirizzo del sottodominio “http://info.mywebsite.com/” sarà “https://info.mywebsite.com/”.

**I certificati SSL non sono installati nei sottodomini configurati stessi**. Sono installati nei sottodomini associati, principalmente quelli che ospitano pagine di destinazione, pagine di risorse e altri.

**I certificati SSL vengono forniti per un periodo di tempo specifico** (1 anno, 60 giorni, ecc.). Una volta scaduto il certificato, potrebbero verificarsi dei problemi durante l’accesso alle pagine di destinazione o l’utilizzo delle risorse del sottodominio. Per evitare questo problema, il Pannello di controllo ti consente di monitorare i certificati SSL dei sottodomini e di avviare il processo di rinnovo.

![](assets/no_certificate.png)

## Gestione dei certificati SSL {#management}

Il monitoraggio dei certificati SSL è fondamentale per garantire la sicurezza dei sottodomini. Con il Pannello di controllo, puoi installare e rinnovare direttamente i certificati SSL dei sottodomini, oppure delegarli ad Adobe in modo che questo venga eseguito automaticamente senza alcun intervento da parte tua.

Si consiglia vivamente di delegare la gestione dei certificati SSL dei sottodomini ad Adobe, in quanto Adobe creerà automaticamente il certificato e lo rinnoverà ogni anno prima della scadenza. In questo modo si riduce il rischio che possono verificarsi errori durante la gestione manuale dei certificati. [Scopri come delegare i certificati SSL dei sottodomini ad Adobe](delegate-ssl.md)

Di seguito è riportato un elenco completo degli impatti associati alla gestione manuale dei certificati, rispetto alla delega ad Adobe:

|       | Certificato gestito dal cliente | Certificato gestito da Adobe |
|  ---  |  ---  |  ---  |
| Fornitore di certificati | Autorità di Certificazione di terze parti | Adobe tramite AWS Certificate Manager |
| Passaggi manuali | Generazione della CSR, acquisto e installazione del certificato | Nessuno |
| Processo di rinnovo | Responsabilità del cliente | Gestito in automatico da Adobe |
| Sicurezza dei sottodomini | Il dominio può avere dei sottodomini non protetti (tracciamento, mirror e res) a meno che non installi e rinnovi i certificati. | Ogni nuovo dominio (se si opta per la gestione da parte di Adobe) avrà per impostazione predefinita tutti i sottodomini protetti. |
| Costo del certificato | Il cliente sostiene il costo dei certificati | Gratuito |

## Monitoraggio dei certificati SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Dettagli del sottodominio"
>abstract="Recupera informazioni sui certificati SSL dei sottodomini."

Lo stato dei certificati SSL dei sottodomini è disponibile direttamente nell’elenco dei sottodomini selezionando la scheda **[!UICONTROL Sottodomini e certificati]**.

I sottodomini sono organizzati in base alla data di scadenza più vicina del certificato SSL, con informazioni visive sulla scadenza, espressa in giorni:

* **Verde**: il sottodominio non dispone di un certificato che scade nei successivi 60 giorni.
* **Arancione**: uno o più sottodomini dispongono di un certificato che scade nei successivi 60 giorni.
* **Rosso**: uno o più sottodomini dispongono di un certificato che scade nei successivi 30 giorni.
* **Grigio**: nessun certificato installato per il sottodominio.

![](assets/subdomains_list.png)

Per visualizzare ulteriori dettagli su un sottodominio, fai clic sul pulsante **[!UICONTROL Dettagli sottodominio]**.
Viene visualizzato l’elenco di tutti i relativi sottodomini. In genere include i sottodomini di pagine di destinazione, pagine di risorse, ecc..

La scheda **[!UICONTROL Informazioni mittente]** fornisce informazioni sulle caselle in entrata configurate (Mittente, Rispondi a, E-mail per errore).

![](assets/subdomain_details.png)

Se uno dei certificati SSL del sottodominio sta per scadere, puoi rinnovarlo direttamente dal Pannello di controllo. Per ulteriori informazioni, consulta questa sezione: [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

**Argomenti correlati:**

* [Rinnovo del certificato SSL di un sottodominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
