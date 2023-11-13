---
product: campaign
solution: Campaign
title: Branding dei sottodomini
description: Ulteriori informazioni sul branding dei sottodomini
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '729'
ht-degree: 100%

---

# Branding dei sottodomini {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Informazioni sui sottodomini e i certificati SSL"
>abstract="Monitora i sottodomini e i certificati SSL associati."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=it" text="Monitoraggio dei certificati SSL"

## Perché impostare i sottodomini? {#why-setting-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico (messaggi transazionali, informazioni di marketing, ecc.).

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

## Metodi di configurazione dei sottodomini {#subdomain-delegation-methods}

La configurazione dei sottodomini consente di configurare una sottosezione del dominio (tecnicamente una “zona DNS”) per l’utilizzo con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega completa del sottodominio ad Adobe Campaign** (consigliato): il sottodominio viene delegato completamente ad Adobe. Adobe è in grado di fornire Campaign come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

* **Utilizzo di CNAME**: crea un sottodominio e utilizza i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, sia Adobe che il cliente condividono la responsabilità della manutenzione del DNS.

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:

| Metodo di configurazione | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Campaign.<br/><br/>In questa configurazione, Adobe si assume la piena responsabilità della gestione del sottodominio e di tutti i record DNS. | Basso |
| **CNAME, metodo personalizzato** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alto |

Per ulteriori informazioni sulla configurazione del dominio, consulta [questa documentazione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=it).

Se hai domande sui metodi di configurazione dei sottodomini, rivolgiti al team Adobe Deliverability oppure contatta l’Assistenza clienti per richiedere consulenza sulla recapitabilità.

## Casi d’uso dei sottodomini (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Seleziona il caso d’uso per il sottodominio"
>abstract="Il raggruppamento dei sottodomini per casi d’uso è una best practice a supporto della recapitabilità. In questo modo, la reputazione di ciascun sottodominio è isolata e protetta."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=it" text="Configurazione di un nuovo sottodominio"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=it" text="Branding dei sottodomini"

Durante la configurazione dei sottodomini per le istanze di Campaign v7/v8, è necessario selezionare il caso d’uso per il quale verrà utilizzato il sottodominio (consulta [Configurazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

I casi d’uso possibili sono:

* **Comunicazioni di marketing**: comunicazioni destinate a scopi commerciali. Esempio: campagna e-mail di vendita.

* **Comunicazioni operative e transazionali**: le comunicazioni transazionali contengono informazioni volte a completare un processo avviato dal destinatario. Esempio: conferma dell’acquisto, e-mail di reimpostazione della password. Le comunicazioni organizzative riguardano lo scambio di informazioni, idee e opinioni all’interno e all’esterno dell’organizzazione, senza scopo commerciale.

**Suddividere i sottodomini in base ai casi di utilizzo è una best practice per il recapito di messaggi**. In questo modo, la reputazione di ciascun sottodominio è isolata e protetta. Ad esempio, se il tuo sottodominio per le comunicazioni di marketing viene inserito nell’elenco Bloccati dai provider di servizi Internet, il sottodominio delle comunicazioni transazionali non sarà coinvolto e continuerà a inviare comunicazioni.

**Puoi configurare un sottodominio sia per i casi d’uso di marketing che per quelli transazionali**:

* Per i casi di utilizzo di marketing, i sottodomini saranno configurati sulle istanze **MID** (Mid sourcing).
* Per i casi di utilizzo transazionali, i sottodomini saranno configurati su TUTTE le istanze **RT** (Message Center / Real-time messaging [Centro messaggi/Messaggistica in tempo reale]) per garantire la connettività. I sottodomini funzioneranno quindi con tutte le tue istanze RT.

>[!NOTE]
>
>Se utilizzi Campaign v7/v8, il Pannello di controllo consente di visualizzare quali istanze RT/MID sono collegate all’istanza di marketing con cui stai lavorando. Per ulteriori informazioni, consulta la sezione [Dettagli istanza](../../instances-settings/using/instance-details.md).

**Argomenti correlati:**

* [Configurazione di un nuovo sottodominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)
