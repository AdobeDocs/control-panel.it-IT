---
product: campaign
solution: Campaign
title: Domande frequenti sul Pannello di controllo
description: Domande comuni relative al Pannello di controllo
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: c834ae7226ed9dd1f78d4f4511b52cb5f04abfae
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 100%

---

# Domande frequenti {#faq}

## Pannello di controllo {#control-panel}

### Che cos’è il Pannello di controllo?

Il Pannello di controllo consente agli amministratori di prodotto di gestire direttamente le varie impostazioni e monitorare la capacità dei server SFTP connessi ad Adobe Campaign.

### Quali sono alcune delle attuali funzionalità del Pannello di controllo?

Il Pannello di controllo consente di tenere traccia dell’archiviazione, inserire IP nell’elenco Consentiti, gestire le chiavi SSH per i server SFTP in modo indipendente in base alle tue esigenze e svolgere altre azioni.

Per ulteriori informazioni, consulta la documentazione sulle azioni supportate dal Pannello di controllo.

### Esistono alcune funzionalità non ancora supportate in Campaign v8 ma disponibili in Campaign Classic v7?{#v8-restrictions}

No. Tutte le funzionalità disponibili in Campaign v7 sono ora supportate anche tramite il Pannello di controllo di Campaign v8, incluse le funzioni relative alla gestione dei sottodomini e dei certificati.

### Il Pannello di controllo è solo per Adobe Campaign?

Sì, puoi gestire solo le impostazioni per Adobe Campaign nel Pannello di controllo.

### Posso usare il Pannello di controllo?

Il Pannello di controllo è accessibile solo agli amministratori di prodotto dei nostri clienti attuali che dispongono di Adobe Campaign ospitato su AWS.

Il Pannello di controllo consente ai clienti con un modello di hosting ibrido di sfruttarne le funzionalità specifiche. A questo scopo, è necessario fornire l’URL dell’istanza MID/RT configurato nell’istanza marketing nel Pannello di controllo. [Ulteriori informazioni](instances-settings/using/external-accounts.md)

Se non sei un amministratore, ma desideri accedervi, contatta il tuo amministratore di prodotto per essere aggiunto come amministratore.

### In qualità di utente di Campaign Classic v7, quali sono le condizioni per poter accedere al Pannello di controllo? {#v7-restrictions}

Il Pannello di controllo è riservato agli utenti amministratori. [Ulteriori informazioni](discover/using/managing-permissions.md).

Per Campaign v7, tieni presente che l’istanza deve essere ospitata su Amazon Web Services (AWS) e aggiornata all’ultima [versione stabile di Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=it#rn-statuses) o alla versione 9032 o superiore. Per controllare la versione di Campaign Classic v7 in uso, consulta [questa sezione](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=it#getting-your-campaign-version). Per verificare se l’istanza di Campaign Classic è ospitata su AWS, segui i passaggi descritti in [questa sezione](#hosted-aws).

### Come posso accedere al Pannello di controllo?

Segui le istruzioni dettagliate riportate nella documentazione Accesso al Pannello di controllo.

### È previsto un costo aggiuntivo per l’utilizzo del Pannello di controllo?

No, non ci sono costi aggiuntivi se sei un cliente attuale di Adobe Campaign.

## ID organizzazione  {#ims-org-id}

### Cos’è un ID organizzazione?

Si tratta di un ID univoco fornito all’istanza al primo accesso ad Adobe Experience Cloud. Deve essere nel formato: xxx@AdobeOrg.

Per ulteriori informazioni, consulta la [documentazione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=it).

### Dove posso trovare il mio ID organizzazione? 

Un metodo consiste nell’accedere alla pagina [Home di Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Troverai il tuo ID organizzazione nella parte inferiore della sezione **[!UICONTROL Quick Access]** di Administration (Amministrazione). Per maggiori informazioni, consulta la [documentazione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=it).

L’altro modo consiste nell’avviare **Admin Console**. L’ID organizzazione sarà visibile nell’URL e avrà un aspetto simile a: https://adminconsole.adobe.com/it_IT/xxx@AdobeOrg/overview.

### Perché devo conoscere il mio ID organizzazione? 

Affinché tu possa gestire le impostazioni per la tua istanza, se utilizzi più istanze per la tua azienda è importante essere certi che tu ottenga le informazioni giuste per una specifica istanza.

### Cosa succede se dispongo di più ID organizzazione? 

Se hai accesso a più soluzioni Adobe, potresti disporre di più ID organizzazione. In questo caso, l’ID organizzazione corretto da utilizzare è quello visualizzato nella tua istanza di Adobe Campaign.

>[!NOTE]
>
>Se disponi dello stesso ID organizzazione per Adobe Campaign e Adobe Analytics, il problema non si pone. Disporre di un ID organizzazione per Analytics e Campaign è un requisito se intendi integrare le soluzioni per sfruttare i casi d’uso complessi, come l’abbandono del carrello (per AA + AC).
>
>Se disponi di ID organizzazione diversi per Adobe Campaign e Adobe Analytics, contatta l’Assistenza clienti per allinearli.

### Come posso sapere se la mia istanza di Adobe Campaign è ospitata o meno su AWS?{#hosted-aws}

Per verificare se l’istanza è ospitata su AWS, effettua le seguenti operazioni:

1. Recupera l’URL di accesso. Si tratta dell’URL che utilizzi per accedere all’istanza Campaign e termina di solito con “.campaign.adobe.com” o “.neolane.net”.
1. Apri il terminale, quindi esegui un’operazione **[!DNL nslookup]** sull’URL di accesso.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. La risposta restituisce informazioni sull’istanza.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Esegui un’operazione **nslookup** sull’indirizzo IP restituito.

   `doe-macOS% nslookup 12.34.567.89`

1. Controlla il valore “name” nel risultato restituito. Se contiene “amazonaws.com”, significa che l’istanza è ospitata in AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Se desideri effettuare la migrazione ad AWS, avvia il processo contattando il tuo Customer Success Manager.
