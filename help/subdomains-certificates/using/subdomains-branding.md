---
title: Branding dei sottodomini
description: Ulteriori informazioni sul branding dei sottodomini
translation-type: ht
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451
workflow-type: ht
source-wordcount: '459'
ht-degree: 100%

---


# Branding dei sottodomini {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Informazioni sui sottodomini e i certificati SSL"
>abstract="Monitora i sottodomini e i certificati SSL associati."
>additional-url="https://docs.adobe.com/content/help/it-IT/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Come monitorare i certificati SSL dei sottodomini"

>[!IMPORTANT]
>
>La delega dei sottodomini dal Pannello di controllo Campaign è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

## Perché impostare i sottodomini? {#why-setting-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico (messaggi transazionali, informazioni di marketing, ecc.).

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” finissero per essere inseriti in blacklist dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento in blacklist dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

## Metodi di delega dei sottodomini {#subdomain-delegation-methods}

La delega dei sottodomini ti consente di delegare una sottosezione del dominio (tecnicamente una “zona DNS”) all’utilizzo con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega completa del sottodominio ad Adobe Campaign** (consigliato): il sottodominio viene delegato completamente ad Adobe. Adobe è in grado di fornire Campaign come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

* **Utilizzo di CNAME** (non consigliato e non supportato dal Pannello di controllo Campaign): crea un sottodominio e utilizza i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, sia Adobe che il cliente condividono la responsabilità della manutenzione del DNS.

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:

| Metodo di delega | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Campaign.<br/><br/>In questa configurazione, Adobe è completamente responsabile della gestione del sottodominio e di tutti i record DNS. | Basso |
| **CNAME, metodo personalizzato** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alto |

Ulteriori informazioni sulla delega del dominio sono disponibili in [questa documentazione](https://helpx.adobe.com/it/campaign/kb/domain-name-delegation.html).

Se hai domande sui metodi di delega dei sottodomini, rivolgiti al team di Adobe Deliverability o contatta l’Assistenza clienti per richiedere consulenza sul recapito dei messaggi.

**Argomenti correlati:**

* [Configurazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Delega di sottodomini (video tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)
