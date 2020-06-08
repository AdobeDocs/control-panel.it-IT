---
title: Domande frequenti sul Pannello di controllo Campaign
description: Domande comuni relative al Pannello di controllo Campaign
translation-type: ht
source-git-commit: 7bde86a86fbd128f4eb7bf029e58b0f95964390b
workflow-type: ht
source-wordcount: '625'
ht-degree: 100%

---


# Domande frequenti {#faq}

## ID organizzazione IMS {#ims-org-id}

**Che cos’è un ID organizzazione IMS?**

Si tratta di un ID univoco fornito all’istanza al primo accesso ad Adobe Experience Cloud. Deve essere nel formato: xxx@AdobeOrg.

Per ulteriori informazioni, consulta la [documentazione di Adobe Experience Cloud](https://marketing.adobe.com/resources/help/it_IT/mcloud/organizations.html).

**Dove posso trovare il mio ID organizzazione IMS?**

Un metodo consiste nell’accedere alla pagina [Home di Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Troverai il tuo ID organizzazione IMS nella parte inferiore della sezione **[!UICONTROL Quick Access]** di Administration (Amministrazione). Per maggiori informazioni, consulta la [documentazione di Adobe Experience Cloud](https://marketing.adobe.com/resources/help/it_IT/mcloud/organizations.html).

L’altro modo consiste nell’avviare **Admin Console**. L’ID organizzazione IMS sarà visibile nell’URL e avrà un aspetto simile a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Perché devo conoscere il mio ID organizzazione IMS?**

Per poter gestire le impostazioni per la tua istanza, vogliamo assicurarci che tu ottenga le informazioni corrette per l’istanza corretta nel caso in cui utilizzi più istanze per la tua azienda.

**Cosa succede se dispongo di più ID organizzazione IMS?**

Se hai accesso a più soluzioni Adobe, puoi disporre di più ID organizzazione IMS. In questo caso, l’ID organizzazione IMS corretto da utilizzare è quello visualizzato nella tua istanza di Adobe Campaign.

>[!NOTE]
>
>Se disponi dello stesso ID organizzazione IMS per Adobe Campaign e Adobe Analytics, è un’ottima soluzione. Disporre dello stesso ID organizzazione IMS per Analytics e Campaign è un requisito se intendi integrare le soluzioni per sfruttare i casi d’uso complessi, come l’abbandono del carrello (per AA + AC).
>
>Se disponi di ID organizzazione IMS diversi per Adobe Campaign e Adobe Analytics, contatta l’Assistenza clienti per allinearli.

**Come posso sapere se la mia istanza di Adobe Campaign è ospitata o meno su AWS?**

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

## Pannello di controllo Campaign {#control-panel}

**Che cos’è il Pannello di controllo Campaign?**

Il Pannello di controllo Campaign consente agli amministratori di prodotto di gestire direttamente le varie impostazioni e monitorare la capacità dei server SFTP connessi ad Adobe Campaign.

**Quali sono alcune delle attuali funzionalità del Pannello di controllo Campaign?**

Il Pannello di controllo Campaign consente di tenere traccia dell’archiviazione, inserire IP nella whitelist, gestire le chiavi SSH per i server SFTP in modo indipendente in base alle tue esigenze e altre azioni.

Per ulteriori informazioni, consulta la documentazione sulle azioni supportate dal Pannello di controllo Campaign.

**Il Pannello di controllo Campaign è solo per Adobe Campaign?**

Sì, puoi gestire solo le impostazioni per Adobe Campaign nel Pannello di controllo Campaign.

**Posso usare il Pannello di controllo Campaign?**

Il Pannello di controllo Campaign è accessibile solo agli amministratori di prodotto dei nostri clienti attuali che dispongono di Adobe Campaign ospitato su AWS. Gli ambienti ibridi non sono ancora supportati.

Se non sei un amministratore, ma desideri accedervi, contatta il tuo amministratore di prodotto per essere aggiunto come amministratore.

**Come posso accedere al Pannello di controllo Campaign?**

Segui le istruzioni dettagliate riportate nella documentazione Accesso al Pannello di controllo Campaign.

**È previsto un costo aggiuntivo per l’utilizzo del Pannello di controllo Campaign?**

No, non ci sono costi aggiuntivi se sei un cliente attuale di Adobe Campaign.
