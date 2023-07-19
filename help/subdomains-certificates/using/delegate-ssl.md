---
product: campaign
solution: Campaign
title: Delegare i certificati SSL dei sottodomini ad Adobe
description: Scopri come delegare i certificati SSL dei sottodomini ad Adobe
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 01da21a883804b9c79c7ee4056d984f3df6cb96c
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 83%

---

# Delegare i certificati SSL dei sottodomini ad Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegare i certificati SSL dei sottodomini ad Adobe"
>abstract="Il Pannello di controllo ti consente di gestire i certificati SSL dei sottodomini gestiti da Adobe. Se utilizzi i CNAME per configurare il sottodominio, i record dei certificati verranno generati e forniti automaticamente per generare un certificato nella soluzione di hosting del dominio."

Si consiglia vivamente di delegare la gestione dei certificati SSL dei sottodomini ad Adobe, in quanto Adobe creerà automaticamente il certificato e lo rinnoverà ogni anno prima della scadenza.

Se utilizzi i CNAME per impostare una delega di sottodominio, Adobe fornirà i record del certificato da utilizzare nella soluzione di hosting del dominio per generare il certificato.

La delega dei certificati SSL ad Adobe può essere eseguita durante la configurazione di un nuovo sottodominio o per i sottodomini già delegati.

>[!NOTE]
>
>L’SSL gestito da Adobe è una funzione gratuita disponibile per gli utenti. La delega del certificato di un sottodominio ad Adobe è trasparente e non ha alcun impatto sulle campagne e sul recapito messaggi. [Ulteriori informazioni sulla gestione dei certificati SSL](monitoring-ssl-certificates.md#management)


## Delegare i certificati SSL dei nuovi sottodomini {#new}

Per delegare i certificati SSL durante la configurazione di un nuovo sottodominio, abilita l’opzione **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** della procedura guidata di configurazione del sottodominio. I record dei certificati da copiare nella soluzione di hosting verranno forniti più avanti nella procedura guidata di configurazione. I passaggi dettagliati sono documentati in [questa sezione](setting-up-new-subdomain.md).

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegare i certificati SSL per i sottodomini già delegati {#delegated}

Per delegare i certificati SSL per un sottodominio già delegato, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e fai clic su **[!UICONTROL Switch to Managed SSL]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Viene visualizzata una finestra di dialogo con i record del certificato generati automaticamente da Adobe. Copia questi record, uno per uno, oppure scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i certificati corrispondenti.

Assicurati che tutti i record del certificato siano stati generati nella soluzione di hosting del tuo dominio. Se tutto è configurato correttamente, conferma la creazione dei record, quindi fai clic su **[!UICONTROL Submit]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
