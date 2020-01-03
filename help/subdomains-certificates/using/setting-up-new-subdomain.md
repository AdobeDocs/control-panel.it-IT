---
title: Impostazione di un nuovo sottodominio
description: Scoprite come impostare un nuovo sottodominio per le istanze della campagna
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Impostazione di un nuovo sottodominio {#setting-up-subdomain}

>[!NOTE]
>
>La delega di sottodominio del Pannello di controllo è attualmente in versione beta e soggetta a frequenti aggiornamenti e modifiche senza notifica.

## Delega di sottodomini completa {#full-subdomain-delegation}

Il Pannello di controllo consente di delegare completamente un sottodominio ad Adobe Campaign. A questo scopo, effettuate le seguenti operazioni:

1. Nella **[!UICONTROL Subdomains & Certificates]**scheda, selezionate l&#39;istanza di produzione desiderata, quindi fate clic su**[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >La delega subdoman è disponibile solo per le istanze di **produzione** .

1. Fare clic **[!UICONTROL Next]**per confermare il metodo di delega completo.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[I metodi CNAME](#use-cnames) e personalizzati non sono attualmente supportati dal Pannello di controllo.

1. Create il sottodominio e i server di nomi desiderati nella soluzione di hosting utilizzata dalla vostra organizzazione. A questo scopo, copiate e incollate le informazioni di Adobe Nameserver visualizzate nella procedura guidata. Per ulteriori informazioni su come creare un sottodominio in una soluzione di hosting, consulta il video [di](https://video.tv.adobe.com/v/30175?captions=ita)esercitazione.

   >[!CAUTION]
   >
   >Durante la configurazione dei server dei nomi, accertati di **non delegare il sottodominio principale ad Adobe**. In caso contrario, il dominio potrà funzionare solo con Adobe. Qualsiasi altro utilizzo sarà impossibile, ad esempio l&#39;invio di e-mail interne ai dipendenti dell&#39;azienda.

   ![](assets/subdomain4.png)

   Se non è configurato alcun sottodominio, il sottodominio impostato verrà considerato come sottodominio **** principale. Le caselle in entrata (mittente, errore, indirizzi di risposta) rimarranno invariate per tutti i sottodomini configurati successivamente su questo sottodominio.

   Una volta creato il sottodominio con le informazioni corrispondenti del server dei nomi Adobe, fate clic su **[!UICONTROL Next]**.

1. Selezionare il caso di utilizzo desiderato per il sottodominio:

   * **Comunicazioni** di marketing: comunicazioni destinate a scopi commerciali. Esempio: campagna e-mail di vendita.
   * **Comunicazioni** operative e transazionali: le comunicazioni transazionali contengono informazioni volte a completare un processo avviato dal destinatario. Esempio: conferma dell&#39;acquisto, e-mail di reimpostazione della password. Le comunicazioni organizzative si riferiscono allo scambio di informazioni, idee e opinioni all&#39;interno e all&#39;esterno dell&#39;organizzazione, senza fini commerciali.
   >[!NOTE]
   >
   >Suddividere i sottodomini in base ai casi di utilizzo è una procedura consigliata per la recapito. In questo modo, la reputazione di ciascun sottodominio è isolata e protetta.
   >
   >Ad esempio, se il tuo sottodominio per le comunicazioni di marketing finirà per essere inserito in blacklist dai provider di servizi Internet, il sottodominio delle comunicazioni transazionali non subentrerà e continuerà a essere in grado di inviare comunicazioni.

   ![](assets/subdomain5.png)

1. Immettete il sottodominio creato nella soluzione di hosting, quindi fate clic su **[!UICONTROL Submit]**.

   >[!NOTE]
   >
   > Accertatevi di compilare il nome **** completo del sottodominio da delegare. Ad esempio, per delegare il sottodominio &quot;usoffer.email.weretail.com&quot;, digitare &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Dopo l&#39;invio del sottodominio, il Pannello di controllo verificherà che esso punti correttamente ai record Adobe NS e che il record Start of Authority (SOA) non esista per questo sottodominio.

1. Se i controlli vengono eseguiti correttamente, il Pannello di controllo avvia la configurazione del sottodominio con record DNS, URL aggiuntivi, inbox e così via. Per maggiori dettagli sull’avanzamento della configurazione, fai clic sul **[!UICONTROL Process details]**pulsante .

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >In alcuni casi, la delega viene eseguita ma il sottodominio potrebbe non essere stato verificato. Il sottodominio entrerà direttamente nell&#39; **[!UICONTROL Verified subdomains]**elenco con lo**[!UICONTROL Unverified]** stato e un registro di processo che fornisce informazioni sull&#39;errore. In caso di problemi con la risoluzione del problema, contatta l’Assistenza clienti.
   >
   >Durante l&#39;esecuzione della delega di sottodominio, altre richieste tramite il Pannello di controllo verranno inserite in una coda ed eseguite solo al termine della delega di sottodominio, per evitare problemi di prestazioni.

Al termine del processo, i sottodomini saranno configurati per lavorare con l&#39;istanza Adobe Campaign e verranno creati gli elementi seguenti:

* **Il sottodominio** con i seguenti record **** DNS: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Sottodomini** aggiuntivi per ospitare mirror, risorse, pagine di tracciamento e domainkey,
* **Inbox**: Mittente, Errore, Risposta.

Per ottenere ulteriori dettagli sul sottodominio, fare clic sul **[!UICONTROL Subdomain Details]**pulsante.

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>Oltre alla fase di elaborazione, Adobe avviserà il team di recapito del nuovo sottodominio per controllare il sottodominio creato. Il processo di controllo può richiedere fino a 3 giorni dopo la delega del sottodominio.
>
>I controlli eseguiti includono cicli di feedback e cicli di reclamo spam. Pertanto non si consiglia di utilizzare il sottodominio prima che l&#39;audit sia stato completato, in quanto potrebbe causare una cattiva reputazione del sottodominio.

## Utilizzo dei CNAME {#use-cnames}

L’utilizzo di CNAME per la delega di sottodominio non è consigliato da Adobe e non è supportato dal Pannello di controllo. Per utilizzare questo metodo, contatta l’Assistenza clienti Adobe.
