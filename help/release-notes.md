---
title: Versioni del Pannello di controllo Campaign
translation-type: tm+mt
source-git-commit: 0bea4b1508305254d53eb23d45bd62944a32495a
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 70%

---


# Versioni del Pannello di controllo Campaign {#control-panel-releases}

Qui trovi informazioni sulle ultime versioni del Pannello di controllo Campaign.

>[!NOTE]
>
>Il Pannello di controllo Campaign è disponibile solo per i clienti ospitati su AWS, ad eccezione degli ambienti ibridi non ancora supportati. Per accedere al Pannello di controllo Campaign non sono necessari aggiornamenti. Assicurati di essere un utente amministratore per accedervi.

## Giugno 2020 {#june-2020}

**Rimozione di &#39;Whitelist&#39; / &#39;Blacklist&#39;**

Sia i termini &quot;whitelist&quot; che &quot;blacklist&quot; sono stati rimossi dalla documentazione  Adobe Campaign. Alcune occorrenze di questi termini potrebbero ancora esistere nell&#39;interfaccia utente del prodotto, nei nomi delle opzioni e nel codice interno, ma verranno sostituiti nelle prossime release di Campaign con ‘blocklist’ e ‘Allowlist’.

**Monitoraggio profili attivi**

Il Pannello di controllo ora consente di monitorare il numero di profili attivi utilizzati dalle istanze e conteggiati a scopo di fatturazione. [Leggi tutto](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Il monitoraggio dei profili attivi dal Pannello di controllo è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso.
>
>Questa funzione è disponibile per i clienti ospitati su AWS dalla build Campaign Standard 10368 e dalla build Campaign Classic 8931. Se si utilizza una build precedente, è necessario eseguire l&#39;aggiornamento per utilizzare questa funzione.

## Maggio 2020 {#may-2020}

**Gestione dei certificati per sottodomini CNAME**

Il Pannello di controllo Campaign ora ti consente di rinnovare i certificati SSL dei sottodomini delegati con il metodo CNAME. [Leggi tutto](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Aprile 2020 {#april-2020}

**Gestione dei record TXT di Google**

Aggiungi il record TXT di Google per la verifica del sito a tutti i tuoi sottodomini utilizzati per inviare e-mail agli indirizzi Gmail tramite il Pannello di controllo Campaign. [Leggi tutto](subdomains-certificates/using/managing-txt-records.md)

**Monitoraggio dello spazio del database**

Il Pannello di controllo Campaign è dotato di funzionalità di monitoraggio del database che ti consentono di visualizzare lo spazio del database utilizzato su richiesta e nel tempo. [Leggi tutto](performance-monitoring/using/database-monitoring.md)

**Avvisi e-mail**

Il Pannello di controllo Campaign è dotato di funzionalità di avvisi e-mail in tempo reale, che ti consentono di accedere al Pannello di controllo Campaign e attivare la ricezione di avvisi quando il sistema è a rischio di deterioramento delle prestazioni o è necessaria un’azione per garantire prestazioni elevate in futuro. [Leggi tutto](performance-monitoring/using/email-alerting.md)

## Gennaio 2020 {#january-2020}

*22 gennaio 2020*

Sono state aggiunte nuove funzionalità che consentono agli utenti amministratori di delegare i sottodomini e rinnovare i certificati SSL dal Pannello di controllo Campaign.

Per ulteriori informazioni, consulta le pagine seguenti:
* [Configurazione di un nuovo sottodominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Rinnovo del certificato SSL di un sottodominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Queste funzionalità saranno disponibili in versione beta e soggette a frequenti aggiornamenti e modifiche senza preavviso.

## Settembre 2019 {#september-2019}

*16 settembre 2019*

Sono state aggiunte nuove funzionalità per consentire agli utenti Admin di aggiungere indirizzi IP all&#39;elenco di indirizzi consentiti per connettersi alle istanze Campaign Classic.
Inoltre, gli utenti amministratori possono ora visualizzare l’elenco delle istanze di Campaign Classic e l’idoneità agli aggiornamenti della build.

Per ulteriori informazioni, consulta la [documentazione dedicata](instances-settings/using/ip-whitelisting-instance-access.md).

## Agosto 2019 {#august-2019}

Abbiamo aggiunto nuove funzionalità affinché gli utenti amministratori ricevano notifiche prima della scadenza dei certificati SSL dei loro domini. Per ulteriori informazioni, consulta la [documentazione dettagliata](subdomains-certificates/using/monitoring-ssl-certificates.md).

Inoltre, gli utenti amministratori possono ora eliminare le chiavi SSH aggiunte per accedere ai server SFTP.

## Luglio 2019 {#july-2019}

Sono state aggiunte nuove funzioni per consentire agli utenti amministratori di avere un maggiore controllo sulle impostazioni delle istanze di Campaign Classic. Le nuove funzionalità del Pannello di controllo Campaign includono la possibilità di aggiungere URL a cui Adobe Campaign si collega per il trasferimento di dati/file.

Per ulteriori informazioni, consulta la [documentazione dettagliata](instances-settings/using/url-permissions.md).
