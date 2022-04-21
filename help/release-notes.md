---
product: campaign
solution: Campaign
title: Versioni del Pannello di controllo Campaign
description: In questa pagina sono elencate tutte le nuove funzioni e i miglioramenti apportati al Pannello di controllo Campaign
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: da68420340ea8605f6e1347e86797c9e6a790ea6
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 61%

---

# Versioni del Pannello di controllo Campaign {#control-panel-releases}

In questa pagina sono elencate tutte le nuove funzioni e i miglioramenti apportati al Pannello di controllo Campaign.

>[!NOTE]
>
>Il Pannello di controllo Campaign è accessibile solo agli utenti amministratori. Ulteriori informazioni sulle autorizzazioni in [questa sezione](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=it#discover-control-panel).
>
>Per Campaign v7, l’istanza deve essere ospitata su Amazon Web Services (AWS) e aggiornata alla versione più recente [Build stabile della campagna](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=it#rn-statuses) (o per costruire 9032 o superiore). Scopri come controllare la versione in [questa sezione](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=it#getting-your-campaign-version). Per verificare se l’istanza è ospitata su AWS, segui i passaggi descritti in [questa sezione](faq.md#hosted-aws).

## Aprile 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Monitorare contatti ed eventi chiave nelle istanze</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi monitorare le versioni precedenti e future e le revisioni dei servizi che si verificano sulle tue istanze, nonché accedere a un elenco di contatti chiave all’Adobe per qualsiasi richiesta o problema.</p><p>Per ulteriori informazioni, consulta la <a href="service-events/service-events.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>

## Marzo 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilità del monitoraggio della latenza e delle immagini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il monitoraggio dei flussi di lavoro e della latenza è ora disponibile per tutti i clienti Campaign Standard e v8 e per i clienti Campaign V7 con numeri di build 9032,9330, 9346 o 9349 che dispongono di distribuzioni indipendenti (senza istanza intermedia).</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/thoughputs-latencies.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>

## Febbraio 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Monitoraggio dei parametri dei flussi di lavoro</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi monitorare i parametri dei flussi di lavoro che richiedono particolare attenzione per evitare problemi alle istanze. </p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/workflow-monitoring.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

## Gennaio 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle query attive</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo ora consente di monitorare le query in esecuzione da molto tempo sulle istanze.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/database-active-queries.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trasmissione e monitoraggio della latenza</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile monitorare la tendenza degli output di consegna e della latenza in un periodo di tempo sulle istanze.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/thoughputs-latencies.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Operazioni sui certificati SSL nei nuovi sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le operazioni sui certificati SSL possono ora essere eseguite su un sottodominio appena configurato, anche se il controllo del recapito messaggi è ancora in corso.</p><p>Per ulteriori informazioni, consulta la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

## Ottobre 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>Intervallo IP e periodo di validità della chiave pubblica</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile impostare una durata per la disponibilità di intervalli IP e chiavi pubbliche. </p><p>Per ulteriori informazioni, consulta la <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Inserimento di intervalli IP nell’elenco Consentiti</a> e <a href="sftp/using/key-management.md#installing-ssh-key">Gestione delle chiavi</a> sezioni.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gamma IP e chiave pubblica</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile modificare le <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">Intervalli IP</a> e <a href="sftp/using/key-management.md#editing-public-keys">chiavi pubbliche</a> che crei. Questa funzione non è disponibile per gli elementi creati prima della versione del Pannello di controllo Campaign corrente.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi sull’intervallo IP SFTP e sulla scadenza della chiave pubblica</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzionalità di avvisi e-mail ora include avvisi sulla scadenza dell’inserimento nell’elenco Consentiti SFTP e sulla scadenza della chiave pubblica SFTP.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/email-alerting.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto completo con Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>Sottodominio</strong> e <strong>Certificato</strong> le funzionalità di gestione sono ora supportate da Pannelli di controllo Campaign in Adobe Campaign v8.</a>.</p>
</td>
</tr>
</tbody>
</table>

## Agosto 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Supporto con Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign è ora disponibile per Adobe Campaign v8, tranne il <strong>Sottodominio</strong> e <strong>Certificato</strong> funzionalità di gestione non ancora supportate.</p><p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Documentazione di Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Ottobre 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Configurazione dei sottodomini tramite CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign ora consente di configurare un sottodominio in modo che sia compatibile con Adobe tramite CNAME direttamente dall’interfaccia.</p><p>Per ulteriori informazioni, consulta la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Miglioramenti al monitoraggio del database</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il monitoraggio del database è stato migliorato con metriche aggiuntive che consentono di ottenere informazioni dettagliate sulle risorse che occupano spazio nel database.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/database-monitoring.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

## Giugno 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Audit del recapito di messaggi dei sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dopo aver delegato un nuovo sottodominio, il Pannello di controllo Campaign ora consente di monitorare l’audit eseguito dal team di Adobe Deliverability.</p><p>Per ulteriori informazioni, consulta la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestione chiavi GPG</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign ora ti consente di generare una coppia di chiavi GPG, in modo da poter decifrare facilmente i dati che arrivano in Campaign dall’esterno. Inoltre, è stata aggiunta una funzionalità che ti consente di installare una chiave GPG pubblica per cifrare i dati in uscita da Campaign.</p><p>Per ulteriori informazioni, consulta la <a href="instances-settings/using/gpg-keys-management.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio profili attivi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign ora consente di monitorare il numero di profili attivi utilizzati dalle istanze e conteggiati a scopo di fatturazione.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/active-profiles-monitoring.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>Il monitoraggio profili attivi dal Pannello di controllo Campaign è disponibile in versione beta e soggetto a frequenti aggiornamenti e modifiche senza preavviso.

## Maggio 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Gestione dei certificati per sottodomini CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign ora consente di rinnovare i certificati SSL dei sottodomini configurati con il metodo CNAME.</p><p>Per ulteriori informazioni, consulta la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

## Aprile 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Gestione dei record TXT di Google</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aggiungi il record TXT di Google per la verifica del sito a tutti i tuoi sottodomini utilizzati per inviare e-mail agli indirizzi Gmail tramite il Pannello di controllo Campaign.</p><p>Per ulteriori informazioni, consulta la <a href="subdomains-certificates/using/managing-txt-records.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio dello spazio del database</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign è dotato di funzionalità di monitoraggio del database che ti consentono di visualizzare lo spazio del database utilizzato su richiesta e nel tempo.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/database-monitoring.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo Campaign è dotato di funzionalità di avvisi e-mail in tempo reale, che ti consentono di accedere al Pannello di controllo Campaign e attivare la ricezione di avvisi quando il sistema è a rischio di deterioramento delle prestazioni o è necessaria un’azione per garantire prestazioni elevate in futuro.</p><p>Per ulteriori informazioni, consulta la <a href="performance-monitoring/using/email-alerting.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

## Gennaio 2020 {#january-2020}

Sono state aggiunte nuove funzionalità che consentono agli utenti amministratori di configurare i sottodomini e rinnovare i certificati SSL dal Pannello di controllo Campaign.

Per ulteriori informazioni, consulta le pagine seguenti:
* [Configurazione di un nuovo sottodominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Rinnovo del certificato SSL di un sottodominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Queste funzionalità saranno disponibili in versione beta e soggette a frequenti aggiornamenti e modifiche senza preavviso.

## Settembre 2019 {#september-2019}

Sono state aggiunte nuove funzionalità che consentono agli utenti amministratori di aggiungere indirizzi IP all’elenco consentiti per connettersi alle istanze Campaign v7/v8.
Inoltre, gli utenti amministratori possono ora visualizzare l’elenco delle istanze Campaign v7/v8 e l’idoneità per gli aggiornamenti della build.

Per ulteriori informazioni, consulta la [documentazione dedicata](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto 2019 {#august-2019}

Abbiamo aggiunto nuove funzionalità affinché gli utenti amministratori ricevano notifiche prima della scadenza dei certificati SSL dei loro domini. Per ulteriori informazioni, consulta la [documentazione dettagliata](subdomains-certificates/using/monitoring-ssl-certificates.md).

Inoltre, gli utenti amministratori possono ora eliminare le chiavi SSH aggiunte per accedere ai server SFTP.

## Luglio 2019 {#july-2019}

Sono state aggiunte nuove funzioni per consentire agli utenti amministratori di avere un maggiore controllo sulle impostazioni delle istanze di Campaign v7/v8. Le nuove funzionalità del Pannello di controllo Campaign includono la possibilità di aggiungere URL a cui Adobe Campaign si collega per il trasferimento di dati/file.

Per ulteriori informazioni, consulta la [documentazione dettagliata](instances-settings/using/url-permissions.md).
