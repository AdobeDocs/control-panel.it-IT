---
title: Marchio dei sottodomini
description: Ulteriori informazioni sul branding dei sottodomini
translation-type: tm+mt
source-git-commit: 762c445713e6e728fc1a45d5fcf8c9c1cb0dcdf6

---


# Marchio dei sottodomini {#subdomains-branding}

>[!IMPORTANT]
>
>La delega di sottodominio del Pannello di controllo sarà disponibile in versione beta entro la fine di gennaio e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

## Perché impostare i sottodomini? {#why-setting-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i marchi o vari tipi di traffico (messaggi transazionali, informazioni di marketing, ecc.).

Prendiamo ad esempio il dominio &quot;mybrand.com&quot;, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio &quot;info.mybrand.com&quot; per le comunicazioni transazionali (conferma dell&#39;acquisto, reimpostazione della password, ecc.),
* Sottodominio &quot;marketing.mybrand.com&quot; per le e-mail di ricerca.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini &quot;marketing.mybrand.com&quot; finissero per essere inseriti in blacklist dai provider di servizi Internet a causa di una scarsa possibilità di recapito, ciò impedirebbe l’inserimento in blacklist dell’intero dominio &quot;mybrand.com&quot; e del sottodominio &quot;info.mybrand.com&quot;.

## Metodi di delega per sottodominio {#subdomain-delegation-methods}

La delega di sottodominio consente di delegare una sottosezione del dominio (tecnicamente una &quot;zona DNS&quot;) da utilizzare con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega del sottodominio completo ad Adobe Campaign** (consigliato): Il sottodominio è delegato completamente ad Adobe. Adobe è in grado di fornire la Campaign come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

* **Utilizzo di CNAME** (non consigliato e non supportato dal Pannello di controllo): Create un sottodominio e utilizzate i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, sia Adobe che il cliente condividono la responsabilità per la manutenzione del DNS.

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di sforzo implicito:

| Metodo di delega | Come funziona | Livello di sforzo |
|---|---|---|
| **Delega completa** | Creare il record del sottodominio e dello spazio nomi. Adobe configurerà quindi tutti i record DNS richiesti per Adobe Campaign.<br/><br/>In questa configurazione, Adobe è completamente responsabile della gestione del sottodominio e di tutti i record DNS. | Bassa |
| **CNAME, metodo personalizzato** | Creare il record del sottodominio e dello spazio nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, sia voi che Adobe condividete la responsabilità di mantenere il DNS. | Alta |

Ulteriori informazioni sulla delega del dominio sono disponibili in [questa documentazione](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

In caso di domande sui metodi di delega dei sottodomini, rivolgiti al team di Adobe Deliverability o contatta l&#39;Assistenza clienti per richiedere la consulenza sulla conformità.

**Argomenti correlati:**

* [Impostazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Delega di sottodomini (video di esercitazione)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)
