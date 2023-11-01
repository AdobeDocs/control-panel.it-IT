---
title: Note sulle versioni 2022
description: In questa pagina sono elencate tutte le versioni del Pannello di controllo del 2022.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '580'
ht-degree: 100%

---

# Note sulle versioni 2022 {#rn-2022}

## Ottobre 2022 {#october-2022}

Gli avvisi via e-mail ora ti avvisano quando uno dei certificati SSL è in scadenza entro 30 giorni o meno. [Ulteriori informazioni](../performance-monitoring/using/email-alerting.md)

## Settembre 2022 {#september-2022}

I clienti con modello di hosting ibrido possono ora configurare nuovi sottodomini. [Ulteriori informazioni](../subdomains-certificates/using/setting-up-new-subdomain.md)

## Agosto 2022 {#august-2022}

* I clienti con modello di hosting ibrido ora possono verificare i loro sottodomini. [Ulteriori informazioni](../subdomains-certificates/using/monitoring-subdomains.md)
* Il campo Unità organizzativa (OU) è ora facoltativo nella richiesta di generazione del certificato (CSR, Certificate Generation Request). [Ulteriori informazioni](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## Luglio 2022 {#july-2022}

<table>
<thead>
<tr>
<th><strong>Installazione dei certificati dei sottodomini per il modello di hosting ibrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>I clienti con modello di hosting ibrido possono ora rinnovare i certificati SSL dei loro sottodomini dal Pannello di controllo.</p><p>Per ulteriori informazioni, consulta la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>

## Giugno 2022 {#june-2022}

### Novità

<table>
<thead>
<tr>
<th><strong>Primi 10 file che occupano spazio su server SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi identificare i primi 10 file che occupano più spazio su un server SFTP. <a href="../sftp/using/sftp-storage-management.md">Ulteriori informazioni</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Promemoria del calendario dei servizi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Service Calendar (Calendario servizi) ora consente di impostare i promemoria per ricevere una notifica via e-mail prima che un evento si verifichi sulle istanze. <a href="../service-events/service-events.md">Ulteriori informazioni</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Miglioramenti alla generazione CSR dei sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono stati apportati diversi miglioramenti al processo di generazione della CSR. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Ulteriori informazioni</a></p><ul><li>Quando generi una CSR, ora puoi selezionare uno dei sottodomini inclusi come Nome comune.</li><li>Ora puoi copiare il riepilogo CSR prima di generare la CSR.</li><li>Una volta generata una CSR, puoi scaricarla nuovamente dai registri dei lavori. Questa funzionalità non si applica ai certificati generati prima di questa versione.</li></ul><p>

</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Impostazioni delle istanze**

* Il numero massimo di chiavi GPG nel Pannello di controllo è stato aumentato a 60 chiavi. [Ulteriori informazioni](../instances-settings/using/gpg-keys-management.md)

## Maggio 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilità del Pannello di controllo per il modello di hosting ibrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il Pannello di controllo è ora disponibile per i clienti con modello di hosting ibrido. Questi clienti possono ora sfruttarne le funzionalità fornendo l’URL dell’istanza MID/RT configurato nella propria istanza marketing nel Pannello di controllo.</p><p>Per ulteriori informazioni, consulta la <a href="../instances-settings/using/external-accounts.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aggiornamenti al monitoraggio delle prestazioni di consegna e delle latenze</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono state migliorate le funzionalità di monitoraggio delle prestazioni di consegna e delle latenze:<ul><li>Ora puoi identificare gli ID delle prime 5 consegne che contribuiscono alle prestazioni della tua istanza.</li><li>I clienti di Campaign Classic v7/v8 possono ora visualizzare la latenza per un canale specifico.</p></li><p>Per ulteriori informazioni, consulta la <a href="../performance-monitoring/using/throughputs-latencies.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>


## Aprile 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Monitorare eventi e contatti chiave nelle istanze</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi monitorare le versioni precedenti e future e le revisioni dei servizi che si verificano sulle tue istanze, nonché accedere a un elenco di contatti chiave in Adobe per eventuali richieste o problemi.</p><p>Per ulteriori informazioni, consulta la <a href="../service-events/service-events.md">documentazione dettagliata.</a></p>
</td>
</tr>
</tbody>
</table>

## Marzo 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle velocità effettive e della latenza</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa funzione è disponibile per tutti i clienti Campaign Standard e v8 e per i clienti Campaign v7 con numeri di build 9032, 9330, 9346 o 9349 che hanno distribuzioni autonome (senza alcuna istanza MID).</p><p>Per ulteriori informazioni, consulta la <a href="../performance-monitoring/using/throughputs-latencies.md">documentazione dettagliata.</a></p>
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
<p>Ora puoi monitorare i parametri dei flussi di lavoro che richiedono particolare attenzione per evitare problemi alle istanze. </p><p>Per ulteriori informazioni, consulta la <a href="../performance-monitoring/using/workflow-monitoring.md">documentazione dettagliata</a>.</p>
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
<p>Il Pannello di controllo ora consente di monitorare le query in esecuzione da molto tempo sulle istanze.</p><p>Per ulteriori informazioni, consulta la <a href="../performance-monitoring/using/database-active-queries.md">documentazione dettagliata</a>.</p>
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
<p>È ora possibile monitorare la tendenza degli output di consegna e della latenza in un periodo di tempo sulle istanze.</p><p>Per ulteriori informazioni, consulta la <a href="../performance-monitoring/using/throughputs-latencies.md">documentazione dettagliata</a>.</p>
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
<p>Le operazioni sui certificati SSL possono ora essere eseguite su un sottodominio appena configurato, anche se l'audit del recapito messaggi è ancora in corso.</p><p>Per ulteriori informazioni, consulta la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>
