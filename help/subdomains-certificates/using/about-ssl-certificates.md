---
title: Informazioni sui certificati SSL
description: Ulteriori informazioni sui certificati SSL
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# Informazioni sui certificati SSL {#about-ssl-certificates}

Adobe Campaign consiglia di proteggere i sottodomini che ospitano le pagine di destinazione, in particolare quelli che raccolgono informazioni riservate dei clienti.

**La cifratura** SSL (Secure Socket Layer) garantisce che i sottodomini delegati ad Adobe siano protetti. Quando il cliente compila un modulo Web o visita una pagina di destinazione ospitata da Adobe Campaign, per impostazione predefinita le informazioni vengono inviate tramite un protocollo non protetto (HTTP). Per garantire ulteriore sicurezza, è necessario proteggere le informazioni inviate con un protocollo HTTPS. Ad esempio, l&#39;indirizzo del sottodominio &quot;http://info.mywebsite.com/&quot; sarà &quot;https://info.mywebsite.com/&quot;.

**I certificati SSL non sono installati nei sottodomini delegati stessi**. Sono installati nei sottodomini associati, principalmente quelli che ospitano pagine di destinazione, pagine di risorse e altri.

**I certificati SSL vengono forniti per un periodo di tempo** specifico (1 anno, 60 giorni, ecc.). Una volta scaduto il certificato, potrebbero verificarsi dei problemi durante l&#39;accesso alle pagine di destinazione o l&#39;utilizzo delle risorse del sottodominio. Per evitare questo problema, il Pannello di controllo consente di monitorare i certificati SSL dei sottodomini e di avviare il processo di rinnovo.

Maggiori dettagli sulla delega del sottodominio sono disponibili [qui](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
