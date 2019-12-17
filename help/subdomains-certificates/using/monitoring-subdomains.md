---
title: Monitoraggio dei certificati SSL dei sottodomini
description: Scoprite come monitorare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Monitoraggio dei sottodomini {#monitoring-subdomains}

È essenziale monitorare i domini secondari per assicurarsi che siano configurati correttamente per l&#39;utilizzo con Adobe Campaign.

L&#39;elenco dei sottodomini per ciascuna istanza di produzione è accessibile direttamente quando si seleziona la **[!UICONTROL Subdomains & Certificates]**scheda.

![](assets/subdomains_list.png)

Per visualizzare ulteriori dettagli su un sottodominio, fare clic sul **[!UICONTROL Subdomain Details]**pulsante .
Viene visualizzato l&#39;elenco di tutti i sottodomini correlati. In genere include sottodomini di pagine di destinazione, pagine di risorse e così via.

La **[!UICONTROL Sender info]**scheda fornisce informazioni sulle inbox configurate (Mittente, Rispondi a, E-mail di errore).

![](assets/subdomain_details.png)


Nell’elenco dei sottodomini, la **[!UICONTROL Last verification]**colonna indica quando un sottodominio è stato verificato per l’ultima volta.** Puoi avviare una verifica in qualsiasi momento facendo clic su **... /**[!UICONTROL Verify subdomain]** pulsante.

>[!CAUTION]
>
>Adobe non consiglia di utilizzare sottodomini senza verificate data, in quanto potrebbe indicare che tali sottodomini potrebbero presentare problemi di recapito.

![](assets/subdomain_verification.png)

Quando si avvia una verifica, vengono eseguite diverse operazioni per verificare che il sottodominio sia configurato correttamente:

1. Il Pannello di controllo controlla che il sottodominio appartenga al tenant dell’istanza.
1. Un&#39;e-mail viene inviata dall&#39;istanza che utilizza tale sottodominio a un set di destinatari di test pari a &quot;250ok&quot; (una piattaforma di analisi e-mail e recapito di terze parti).
1. Dopo aver ricevuto l’e-mail, 250ok legge le intestazioni dell’e-mail e verifica se SPF e DKIM sono configurati e validi.
1. Il Pannello di controllo controlla continuamente lo stato di consegna da 250ok per circa 20 minuti. Se SPF e DKIM vengono superati, significa che il sottodominio richiesto viene verificato ed è completamente configurato e pronto per l&#39;invio di e-mail.
