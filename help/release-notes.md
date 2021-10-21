---
product: campaign
solution: Campaign
title: Versioni del Pannello di controllo Campaign
description: Note sulla versione più recente del Pannello di controllo Campaign.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 8b0f652559e0296a22b3eac92057e6f4487215e1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Versioni del Pannello di controllo Campaign {#control-panel-releases}

Qui troverai informazioni sulle ultime versioni del Pannello di controllo Campaign.

>[!NOTE]
>
>Il Pannello di controllo Campaign è accessibile a tutti gli utenti amministratori. I passaggi per concedere a un utente i diritti da amministratore sono descritti in [questa sezione](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html#discover-control-panel).
>
>Per Campaign Classic v7, tieni presente che l’istanza deve essere ospitata su AWS e aggiornata con l’ultima [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=it) o [build GA più recente (21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=it#release-notes). Scopri come controllare la versione in [questa sezione](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=it#getting-your-campaign-version). Per verificare se l’istanza è ospitata su AWS, segui i passaggi descritti in [questa sezione](faq.md).

## Ottobre 2021 {#october-2021}

**Intervallo IP e periodo di validità della chiave pubblica**

È ora possibile impostare una durata per la disponibilità di intervalli IP e chiavi pubbliche. Ulteriori informazioni nella sezione [Inserimento di intervalli IP nell’elenco Consentiti](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) e [Gestione delle chiavi](sftp/using/key-management.md#installing-ssh-key) sezioni.

**Gamma IP e chiave pubblica**

È ora possibile modificare le [Intervalli IP](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) e [chiavi pubbliche](sftp/using/key-management.md#editing-public-keys) che crei. Questa funzione non è disponibile per gli elementi creati prima della versione del Pannello di controllo Campaign corrente.

**Avvisi sull’intervallo IP SFTP e sulla scadenza della chiave pubblica**

La funzionalità di avvisi e-mail ora include avvisi sulla scadenza dell’inserimento nell’elenco Consentiti SFTP e sulla scadenza della chiave pubblica SFTP. [Leggi tutto](performance-monitoring/using/email-alerting.md)

<!--**Full support with Campaign v8**

The **Subdomain** and **Certificate** management capabilities are now supported by Control Panel on Adobe Campaign v8.-->

## Agosto 2021 {#august-2021}

**Supporto con Campaign v8**

Il Pannello di controllo Campaign è ora disponibile per Adobe Campaign v8, tranne il **Sottodominio** e **Certificato** funzionalità di gestione non ancora supportate. Ulteriori informazioni sono disponibili nella [documentazione di Campaign  v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Ottobre 2020 {#october-2020}

**Configurazione di sottodomini tramite CNAME**

Il Pannello di controllo Campaign ora consente di configurare un sottodominio in modo che sia compatibile con Adobe tramite CNAME direttamente dall’interfaccia. [Leggi tutto](subdomains-certificates/using/setting-up-new-subdomain.md)

**Miglioramenti al monitoraggio del database**

Il monitoraggio del database è stato migliorato con metriche aggiuntive che consentono di ottenere informazioni dettagliate sulle risorse che occupano spazio nel database. [Leggi tutto](performance-monitoring/using/database-monitoring.md)

## Giugno 2020 {#june-2020}

**Audit del recapito di messaggi dei sottodomini**

Dopo aver delegato un nuovo sottodominio, il Pannello di controllo Campaign ora consente di monitorare l’audit eseguito dal team di Adobe Deliverability. [Leggi tutto](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gestione chiavi GPG**

Il Pannello di controllo Campaign ora ti consente di generare una coppia di chiavi GPG, in modo da poter decifrare facilmente i dati che arrivano in Campaign dall’esterno. Inoltre, è stata aggiunta una funzionalità che ti consente di installare una chiave GPG pubblica per cifrare i dati in uscita da Campaign. [Leggi tutto](instances-settings/using/gpg-keys-management.md)

**Monitoraggio profili attivi**

Il Pannello di controllo Campaign ora consente di monitorare il numero di profili attivi utilizzati dalle istanze e conteggiati a scopo di fatturazione. [Leggi tutto](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Il monitoraggio profili attivi dal Pannello di controllo Campaign è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso.

## Maggio 2020 {#may-2020}

**Gestione dei certificati per sottodomini CNAME**

Il Pannello di controllo Campaign ora consente di rinnovare i certificati SSL dei sottodomini configurati con il metodo CNAME. [Leggi tutto](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Aprile 2020 {#april-2020}

**Gestione dei record TXT di Google**

Aggiungi il record TXT di Google per la verifica del sito a tutti i tuoi sottodomini utilizzati per inviare e-mail agli indirizzi Gmail tramite il Pannello di controllo Campaign. [Leggi tutto](subdomains-certificates/using/managing-txt-records.md)

**Monitoraggio dello spazio del database**

Il Pannello di controllo Campaign è dotato di funzionalità di monitoraggio del database che ti consentono di visualizzare lo spazio del database utilizzato su richiesta e nel tempo. [Leggi tutto](performance-monitoring/using/database-monitoring.md)

**Avvisi e-mail**

Il Pannello di controllo Campaign è dotato di funzionalità di avvisi e-mail in tempo reale, che ti consentono di accedere al Pannello di controllo Campaign e attivare la ricezione di avvisi quando il sistema è a rischio di deterioramento delle prestazioni o è necessaria un’azione per garantire prestazioni elevate in futuro. [Leggi tutto](performance-monitoring/using/email-alerting.md)

## Gennaio 2020 {#january-2020}

*22 gennaio 2020*

Sono state aggiunte nuove funzionalità che consentono agli utenti amministratori di configurare i sottodomini e rinnovare i certificati SSL dal Pannello di controllo Campaign.

Per ulteriori informazioni, consulta le pagine seguenti:
* [Configurazione di un nuovo sottodominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Rinnovo del certificato SSL di un sottodominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Queste funzionalità saranno disponibili in versione beta e soggette a frequenti aggiornamenti e modifiche senza preavviso.

## Settembre 2019 {#september-2019}

*16 settembre 2019*

Sono state introdotte nuove funzionalità che consentono agli utenti amministratori di aggiungere indirizzi IP all’elenco Consentiti per connettersi alle istanze Campaign Classic.
Inoltre, gli utenti amministratori possono ora visualizzare l’elenco delle istanze di Campaign Classic e l’idoneità agli aggiornamenti della build.

Per ulteriori informazioni, consulta la [documentazione dedicata](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto 2019 {#august-2019}

Abbiamo aggiunto nuove funzionalità affinché gli utenti amministratori ricevano notifiche prima della scadenza dei certificati SSL dei loro domini. Per ulteriori informazioni, consulta la [documentazione dettagliata](subdomains-certificates/using/monitoring-ssl-certificates.md).

Inoltre, gli utenti amministratori possono ora eliminare le chiavi SSH aggiunte per accedere ai server SFTP.

## Luglio 2019 {#july-2019}

Sono state aggiunte nuove funzioni per consentire agli utenti amministratori di avere un maggiore controllo sulle impostazioni delle istanze di Campaign Classic. Le nuove funzionalità del Pannello di controllo Campaign includono la possibilità di aggiungere URL a cui Adobe Campaign si collega per il trasferimento di dati/file.

Per ulteriori informazioni, consulta la [documentazione dettagliata](instances-settings/using/url-permissions.md).
