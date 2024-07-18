---
title: Note sulla versione 2023
description: In questa pagina sono elencate tutte le versioni del Pannello di controllo del 2023.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Note sulla versione 2023 {#rn-2023}

## Settembre 2023 {#september-2023}

<table>
<thead>
<tr>
<th><strong>Gestione dei record DMARC e BIMI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Ora puoi aggiungere record DMARC e BIMI direttamente dal Pannello di controllo:

<ul><li>I <strong>record DMARC</strong> forniscono un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi. <a href="../subdomains-certificates/using/dmarc.md">Scopri come aggiungere record DMARC</a></li>
<li>I <strong>record BIMI</strong> ti consentono di visualizzare un logo approvato accanto alle e-mail nelle caselle in entrata dei provider di casette postali per migliorare il riconoscimento e l’affidabilità del brand. <a href="../subdomains-certificates/using/bimi.md">Scopri come aggiungere record BIMI</a></li></ul>
</td>
</tr>
</tbody>
</table>

## Giugno 2023 {#june-2023}

* Ora puoi delegare i certificati SSL dei sottodomini già delegati ad Adobe direttamente dall’elenco dei sottodomini. [Ulteriori informazioni](../subdomains-certificates/using/delegate-ssl.md)

* Il mittente delle e-mail di avviso è stato modificato in `"alert@notifications.campaign.adobe.com"`.

## Miglioramenti di maggio 2023 {#may-2023}

**Delega dei certificati SSL dei sottodomini ad Adobe**

Ora i certificati SSL dei sottodomini possono essere gestiti da Adobe. Se utilizzi i CNAME per configurare il sottodominio, i record dei certificati verranno generati e forniti automaticamente per generare un certificato nella soluzione di hosting del dominio.

Questa funzionalità è disponibile solo durante la configurazione di un nuovo sottodominio. Non puoi delegare certificati per sottodomini delegati esistenti. [Ulteriori informazioni](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>L’SSL gestito da Adobe è una funzione gratuita disponibile per gli utenti.

## Marzo 2023 {#march-2023}

**Rimozione della delega del sottodominio per CNAME**

Ora puoi rimuovere la delega dei sottodomini configurati tramite CNAME. [Ulteriori informazioni](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Febbraio 2023 {#february-2023}

**Rimozione della delega per i sottodomini delegati ad Adobe**

Ora puoi rimuovere la delega di un sottodominio completamente delegato ad Adobe. [Ulteriori informazioni](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>La rimozione della delega non è attualmente disponibile per i sottodomini impostati tramite CNAME.

**Calendario del servizio**

Il calendario del servizio ora fornisce una vista calendario per tenere traccia di eventi importanti che si verificano sulle istanze. Sono state inoltre aggiunte informazioni sulle notifiche inviate agli utenti abbonati agli avvisi del Pannello di controllo. [Ulteriori informazioni](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Gennaio 2023 {#january-2023}

**Nuova funzionalità del modello di hosting ibrido**

I clienti con modello di hosting ibrido possono ora aggiungere indirizzi IP all’elenco consentiti per accedere alle istanze MID. [Ulteriori informazioni](../instances-settings/using/ip-allow-listing-instance-access.md)

**Miglioramento della richiesta di firma del certificato (CSR)**

Il campo Città/Località è ora facoltativo durante la generazione della richiesta di firma del certificato.
