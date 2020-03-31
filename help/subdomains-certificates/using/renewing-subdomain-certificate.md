---
title: Rinnovo del certificato SSL di un sottodominio
description: Scopri come rinnovare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: f08b0e68cf0a208b1385052510c06ca1eb679e63

---


# Rinnovo del certificato SSL di un sottodominio {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;Aggiungi certificato SSL&quot;
>abstract=&quot;Per aggiungere un certificato SSL, è necessario generare un CSR, acquistare il certificato SSL per i sottodomini e installare il Bundle certificati.&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generazione di una richiesta di firma dei certificati (CSR)&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;Come installare un certificato SSL&quot;

>[!IMPORTANT]
>
>La delega di sottodominio del Pannello di controllo è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

## Informazioni sul rinnovo dei certificati {#about-certificate-renewal-process}

Il processo di rinnovo del certificato SSL comprende 3 passaggi:

1. **La generazione della richiesta di firma dei certificati (CSR)** Adobe Customer Care genera un CSR. Per generare il CSR sarà necessario fornire alcune informazioni (ad esempio Nome comune, Nome organizzazione e indirizzo, ecc.).
1. **Acquisto del certificato** SSL Una volta generato il CSR, è possibile scaricarlo e utilizzarlo per acquistare il certificato SSL dall’autorità di certificazione approvata dalla società.
1. **Installazione del certificato** SSL Una volta acquistato il certificato SSL, è possibile installarlo nel sottodominio desiderato.

>[!NOTE]
>
>Il rinnovo dei certificati SSL tramite il Pannello di controllo è disponibile solo per i sottodomini **delegati** completi.

## Generazione di una richiesta di firma dei certificati (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Generate CSR&quot;
>abstract=&quot;La richiesta di firma del certificato deve essere generata per l&#39;istanza e i sottodomini che si intende proteggere prima di acquistare un certificato.&quot;

>[!CONTEXTUALHELP]
>id=&quot;cp_select_subdomini&quot;
>title=&quot;Seleziona i sottodomini per la tua CSR&quot;
>abstract=&quot;Potete scegliere di includere nella richiesta di firma dei certificati tutti i sottodomini o solo alcuni di essi. Solo i sottodomini selezionati saranno certificati tramite il certificato SSL acquistato.&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generazione di una richiesta di firma dei certificati (CSR)&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;About subdomini branding&quot;

Per generare una richiesta di firma dei certificati (CSR), procedere come segue:

1. Nella **[!UICONTROL Subdomains & Certificates]** scheda, selezionate l&#39;istanza desiderata, quindi fate clic sul **[!UICONTROL Manage Certificate]** pulsante.

   ![](assets/renewal1.png)

1. Selezionate **[!UICONTROL Generate a CSR]**, quindi fate clic **[!UICONTROL Next]** per avviare la procedura guidata che vi guiderà attraverso il processo di generazione CSR.

   ![](assets/renewal2.png)

1. Viene visualizzato un modulo con tutti i dettagli necessari per generare il CSR.

   Assicuratevi di compilare le informazioni richieste in modo completo e accurato, altrimenti il certificato potrebbe non essere rinnovato (se necessario contattate il team interno, i team di sicurezza e IT), quindi fate clic **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: nome dell’organizzazione ufficiale.
   * **[!UICONTROL Organization Unit]**: unità collegata al sottodominio (esempio: Marketing, IT).
   * **[!UICONTROL Instance]** (precompilato): URL dell&#39;istanza Campaign associata al sottodominio.
   ![](assets/renewal3.png)

1. Seleziona i sottodomini da includere nella CSR, quindi fai clic su **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. I sottodomini selezionati vengono visualizzati nell&#39;elenco. Per ciascuno di essi, seleziona i sottodomini da includere, quindi fai clic su **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Viene visualizzato un riepilogo dei sottodomini da includere nel CSR. Fate clic **[!UICONTROL Submit]** per confermare la richiesta.

   ![](assets/renewal6.png)

1. Il file .csr corrispondente alla selezione viene generato e scaricato automaticamente. Ora potete usarlo per acquistare il certificato SSL dall’autorità di certificazione approvata dalla società.

   >[!NOTE]
   >
   >Se la CSR non viene salvata o scaricata, andrà persa e sarà necessario generarla di nuovo.

## Acquisto di un certificato con il CSR {#purchasing-certificate}

Dopo aver ottenuto un CSR per la richiesta di firma dei certificati dal Pannello di controllo, acquistate un certificato SSL da un&#39;autorità di certificazione approvata dalla vostra organizzazione.

## Installazione del certificato SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;Installa certificato SSL&quot;
>abstract=&quot;Installa il certificato SSL acquistato dall’autorità di certificazione approvata dall’organizzazione.&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;About subdomini branding&quot;

Una volta acquistato un certificato SSL, potete installarlo nell’istanza. Prima di procedere, accertatevi di conoscere i prerequisiti seguenti:

* La richiesta di firma del certificato (CSR) deve essere stata generata dal Pannello di controllo. In caso contrario, non sarà possibile installare il certificato dal Pannello di controllo.
* La richiesta di firma del certificato (CSR) deve corrispondere al sottodominio delegato ad Adobe. Ad esempio, non può contenere più sottodomini di quello delegato.
* Il certificato deve avere una data corrente. Non è possibile installare certificati con date future e non deve essere scaduto (vale a dire date di inizio e fine valide).
* Il certificato deve essere rilasciato da un&#39;autorità di certificazione (CA) affidabile, come Comodo, DigiCert, GoPapà, ecc.
* La dimensione del certificato deve essere di 2048 bit e l&#39;algoritmo deve essere RSA.
* Il certificato deve essere in formato X.509 PEM.
* I certificati SAN sono supportati.
* I certificati jolly non sono supportati.
* Il file ZIP o il certificato non devono essere protetti da password.
* Il file ZIP deve contenere solo quanto segue in preferibilmente singoli file:
   * Certificato di entità finale.
   * Catena certificati intermedia (ordinata in modo corretto).
   * Certificato di origine (facoltativo).

Per installare il certificato, effettuate le seguenti operazioni:

1. Nella **[!UICONTROL Subdomains & Certificates]** scheda, selezionate l&#39;istanza desiderata, quindi fate clic sul **[!UICONTROL Manage Certificate]** pulsante.

   ![](assets/renewal1.png)

1. Fate clic **[!UICONTROL Install SSL Certificate]**, quindi **[!UICONTROL Next]** per avviare la procedura guidata che vi guiderà attraverso il processo di installazione del certificato.

   ![](assets/install1.png)

1. Selezionate il file .zip che contiene il certificato da installare, quindi fate clic **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>Il certificato verrà installato su tutti i domini/sottodomini inclusi nel CSR. Eventuali altri domini/sottodomini presenti nel certificato non saranno presi in considerazione.

Una volta installato il certificato SSL, la data di scadenza e l&#39;icona di stato del certificato vengono aggiornate di conseguenza.

**Argomenti correlati:**

* [Aggiunta di certificati SSL (video di esercitazione)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Marchio dei sottodomini](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoraggio dei sottodomini](../../subdomains-certificates/using/monitoring-subdomains.md)