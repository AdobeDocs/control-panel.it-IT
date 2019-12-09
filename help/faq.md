---
title: Domande frequenti sul Pannello di controllo
description: Domande comuni relative al Pannello di controllo
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Domande frequenti {#faq}

## ID organizzazione IMS {#ims-org-id}

**Cos’è un ID organizzazione IMS?**


Si tratta di un ID univoco fornito all’istanza al primo accesso ad Adobe Experience Cloud. Deve essere nel formato: xxx@AdobeOrg.

Per ulteriori informazioni, consulta la documentazione [di](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)Adobe Experience Cloud.

**Dove posso trovare il mio ID organizzazione IMS?**

One way is to navigate to [Adobe Experience Cloud Home](https://exc-login.experiencecloud.adobe.com/exc-content/login.html?prefixtenantid=amc) &gt; **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration **[!UICONTROL Quick Access]** section. Per maggiori informazioni, consulta la [documentazione di Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

L'altro modo consiste nell'avviare **Admin Console**. L’ID organizzazione IMS sarà visibile nell’URL e avrà un aspetto simile a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Perché devo conoscere il mio ID organizzazione IMS?**


Per poter gestire le impostazioni per l'istanza in uso, vogliamo assicurarci di ottenere le informazioni corrette per l'istanza corretta nel caso in cui si utilizzino più istanze per la società.

**Cosa succede se dispongo di più ID organizzazione IMS?**


Se avete accesso a più soluzioni Adobe, potete disporre di più ID organizzazione IMS. In questo caso, l'ID organizzazione IMS corretto da utilizzare è quello visualizzato nell'istanza di Adobe Campaign.

>[!NOTE]
>
>Se disponi dello stesso ID organizzazione IMS per Adobe Campaign e Adobe Analytics, è un'ottima soluzione. Disporre di un ID organizzazione IMS tra Analytics e Campaign è un requisito se intendete integrare le soluzioni per sfruttare i casi d’uso complessi, come l’abbandono del carrello (per AA + AC).
>
>Se disponi di ID organizzazione IMS diversi per Adobe Campaign e Adobe Analytics, contatta l'Assistenza clienti per allinearli.

**Come posso sapere che l'istanza di Adobe Campaign è ospitata o meno su AWS?**

Per verificare se l’istanza è in hosting su AWS, effettuate le seguenti operazioni:

1. Recuperate l’URL di accesso. Si tratta dell'URL utilizzato per accedere all'istanza Campaign, che termina principalmente con ".campaign.adobe.com".
1. Aprite il terminale, quindi eseguite un'operazione **di ricerca** sull'URL di accesso.

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

1. Eseguire un'operazione **nssearch** sull'indirizzo IP restituito.

   `doe-macOS% nslookup 12.34.567.89`

1. Selezionare il valore "name" nel risultato restituito. Se contiene "amazonaws.com", significa che l’istanza è ospitata in AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Se desiderate effettuare la migrazione ad AWS, avviate il processo contattando il Customer Success Manager.

## Pannello di controllo Campaign {#control-panel}

**Cos'è il Pannello di controllo?**


Il Pannello di controllo consente agli amministratori dei prodotti di gestire direttamente le varie impostazioni e monitorare la capacità dei server SFTP collegati ad Adobe Campaign.

**Quali sono alcune delle attuali funzionalità del Pannello di controllo?**


Il Pannello di controllo consente di tenere traccia dello storage, inserire nella whitelist IP e gestire le chiavi SSH per i server SFTP in modo indipendente in base alle esigenze e ad altre azioni.

Per ulteriori informazioni, consultare la documentazione sulle azioni supportate dal Pannello di controllo.

**Il Pannello di controllo è solo per Adobe Campaign?**


Sì, potrai gestire solo le impostazioni per Adobe Campaign nel Pannello di controllo.

**Posso usare il Pannello di controllo?**


Il Pannello di controllo è aperto solo agli amministratori dei prodotti dei clienti attuali che hanno Adobe Campaign ospitato su AWS.

Se non sei un amministratore, ma desideri accedere, contatta l’amministratore del prodotto per aiutarti ad aggiungerti come amministratore.

**Come posso accedere al Pannello di controllo?**

Seguire le istruzioni dettagliate riportate nella documentazione Accesso al Pannello di controllo.

**È previsto un costo aggiuntivo per l'utilizzo del Pannello di controllo?**


No, non ci sono costi aggiuntivi se sei un cliente corrente di Adobe Campaign.