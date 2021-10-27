---
product: campaign
solution: Campaign
title: Branding dei sottodomini
description: Ulteriori informazioni sul branding dei sottodomini
feature: Control Panel
role: Architect
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: 46a4e13e8017c5406dcd65f21c9839374dd44aa7
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 79%

---

# Branding dei sottodomini {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Informazioni sui sottodomini e i certificati SSL"
>abstract="Monitora i sottodomini e i certificati SSL associati."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=it" text="Monitoraggio dei certificati SSL"

## Perché impostare i sottodomini? {#why-setting-up-subdomains}

>[!IMPORTANT]
>
>La configurazione dei sottodomini dal Pannello di controllo Campaign è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico (messaggi transazionali, informazioni di marketing, ecc.).

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

## Metodi di configurazione dei sottodomini {#subdomain-delegation-methods}

La configurazione dei sottodomini ti consente di configurare una sottosezione del dominio (tecnicamente una &quot;zona DNS&quot;) da utilizzare con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega completa del sottodominio ad Adobe Campaign** (consigliato): il sottodominio viene delegato completamente ad Adobe. Adobe è in grado di fornire Campaign come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

* **Utilizzo dei CNAME**: Crea un sottodominio e utilizza i CNAME per puntare a record specifici per l’Adobe. Utilizzando questa configurazione, sia Adobe che il cliente condividono la responsabilità della manutenzione del DNS.

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:

| Metodo di configurazione | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Campaign.<br/><br/>In questa configurazione, Adobe si assume la piena responsabilità della gestione del sottodominio e di tutti i record DNS. | Basso |
| **CNAME, metodo personalizzato** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alto |

Ulteriori informazioni sulla configurazione del dominio sono disponibili in [questa documentazione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Se hai domande sui metodi di configurazione dei sottodomini, rivolgiti al team di Adobe Deliverability o contatta l’Assistenza clienti per richiedere consulenza sul recapito messaggi.

## Casi d’uso dei sottodomini (Campaign Classic){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Seleziona il caso d’uso per il sottodominio"
>abstract="Suddividere i sottodomini per casi d’uso è una best practice per il recapito di messaggi. In questo modo, la reputazione di ciascun sottodominio è isolata e protetta."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=it" text="Configurazione di un nuovo sottodominio"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=it" text="Branding dei sottodomini"

Quando imposti i sottodomini per le istanze di Campaign Classic, devi selezionare il caso d’uso per il quale verrà utilizzato il sottodominio (vedi [Configurazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

I casi d’uso possibili sono:

* **Comunicazioni di marketing**: comunicazioni destinate a scopi commerciali. Esempio: campagna e-mail di vendita.

* **Comunicazioni operative e transazionali**: le comunicazioni transazionali contengono informazioni volte a completare un processo avviato dal destinatario. Esempio: conferma dell’acquisto, e-mail di reimpostazione della password. Le comunicazioni organizzative riguardano lo scambio di informazioni, idee e opinioni all’interno e all’esterno dell’organizzazione, senza scopo commerciale.

**Suddividere i sottodomini in base ai casi di utilizzo è una best practice per il recapito di messaggi**. In questo modo, la reputazione di ciascun sottodominio è isolata e protetta. Ad esempio, se il tuo sottodominio per le comunicazioni di marketing viene inserito nell’elenco Bloccati dai provider di servizi Internet, il sottodominio delle comunicazioni transazionali non sarà coinvolto e continuerà a inviare comunicazioni.

**Puoi configurare un sottodominio sia per i casi di utilizzo di marketing che per quelli transazionali**:

* Per i casi di utilizzo di marketing, i sottodomini saranno configurati sulle istanze **MID** (Mid sourcing).
* Per i casi di utilizzo transazionali, i sottodomini saranno configurati su TUTTE le istanze **RT** (Message Center / Real-time messaging [Centro messaggi/Messaggistica in tempo reale]) per garantire la connettività. I sottodomini funzioneranno quindi con tutte le tue istanze RT.

>[!NOTE]
>
>Se utilizzi Campaign Classic, il Pannello di controllo Campaign ti consente di visualizzare quali istanze RT/MID sono collegate all’istanza di marketing con cui stai lavorando. Per ulteriori informazioni, consulta la sezione [Instance details](../../instances-settings/using/instance-details.md) (Dettagli istanza).

**Argomenti correlati:**

* [Configurazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)
