---
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scoprite come monitorare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Monitoraggio dei certificati SSL dei sottodomini {#monitoring-ssl-certificates}

Adobe Campaign consiglia di proteggere i sottodomini che ospitano le pagine di destinazione, in particolare quelli che raccolgono informazioni riservate dei clienti.

**La cifratura** SSL (Secure Socket Layer) garantisce che i sottodomini delegati ad Adobe siano protetti. Quando il cliente compila un modulo Web o visita una pagina di destinazione ospitata da Adobe Campaign, per impostazione predefinita le informazioni vengono inviate tramite un protocollo non protetto (HTTP). Per garantire ulteriore sicurezza, è necessario proteggere le informazioni inviate con un protocollo HTTPS. Ad esempio, l&#39;indirizzo del sottodominio &quot;http://info.mywebsite.com/&quot; sarà &quot;https://info.mywebsite.com/&quot;.

**I certificati SSL non sono installati nei sottodomini delegati stessi**. Sono installati nei sottodomini associati, principalmente quelli che ospitano pagine di destinazione, pagine di risorse e altri.

**I certificati SSL vengono forniti per un periodo di tempo** specifico (1 anno, 60 giorni, ecc.). Una volta scaduto il certificato, potrebbero verificarsi dei problemi durante l&#39;accesso alle pagine di destinazione o l&#39;utilizzo delle risorse del sottodominio. Per evitare questo problema, il Pannello di controllo consente di monitorare i certificati SSL dei sottodomini e di avviare il processo di rinnovo.

![](assets/no_certificate.png)

Se uno dei certificati SSL del sottodominio sta per scadere, è possibile rinnovarlo direttamente dal Pannello di controllo. Per ulteriori informazioni, consulta questa sezione: Rinnovo [del certificato](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL di un sottodominio.
