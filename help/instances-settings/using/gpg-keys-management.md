---
title: Gestione chiavi GPG
description: Scoprite come gestire le chiavi GPG per cifrare e decifrare i dati all'interno  Adobe Campaign.
translation-type: tm+mt
source-git-commit: a83309bfb6e42db231fe970f47475fb85d6d441b
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 2%

---


# Gestione chiavi GPG {#gpg-keys-management}

## Informazioni sulla crittografia GPG {#about-gpg-encryption}

La crittografia GPG consente di proteggere i dati utilizzando un sistema di coppie di chiavi pubblica-privata che seguono le specifiche [OpenPGP](https://www.openpgp.org/about/standard/) .

Una volta implementati, è possibile che i dati in entrata siano decrittografati e quelli in uscita crittografati prima del trasferimento, per garantire che non siano accessibili a nessuno senza una coppia di chiavi corrispondente valida.

Per implementare la crittografia GPG con Campaign, le chiavi GPG devono essere installate e/o generate in un&#39;istanza di marketing da un utente amministratore direttamente dal Pannello di controllo.

Potrete quindi:

* **Cifra dati** inviati:  Adobe Campaign invia i dati dopo la cifratura con la chiave pubblica installata.

* **Decrittografa dati** in arrivo:  Adobe Campaign riceve i dati crittografati da un sistema esterno utilizzando una chiave pubblica scaricata dal Pannello di controllo.  Adobe Campaign decrittografa i dati utilizzando una chiave privata generata dal Pannello di controllo.

**Argomenti correlati:**

* [Video tutorial per Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/generating-and-installing-gpg-keys.html)
* [Video tutorial per Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/generating-and-installing-gpg-keys.html)


## Cifratura dei dati {#encrypting-data}

Il Pannello di controllo consente di crittografare i dati provenienti dall&#39;istanza del Adobe Campaign .

A tal fine, è necessario generare una coppia di chiavi GPG da uno strumento di crittografia PGP, quindi installare la chiave pubblica nel Pannello di controllo. Sarà quindi possibile crittografare i dati prima di inviarli dall&#39;istanza. A questo scopo, effettuate le seguenti operazioni:

1. Generare una coppia di chiavi pubblica/privata utilizzando uno strumento di crittografia PGP che segue la specifica [](https://www.openpgp.org/about/standard/)OpenPGP. A tal fine, installare un&#39;utility GPG o un software GNuGP.

   >[!NOTE]
   >
   >È disponibile un software libero open source per generare chiavi. Tuttavia, accertatevi di seguire le linee guida della vostra organizzazione e di utilizzare l&#39;utility GPG consigliata dall&#39;organizzazione IT/Security.

1. Una volta installata l&#39;utility, eseguite il comando seguente, in Mac Terminal o Windows.

   `gpg --full-generate-key`

1. Quando richiesto, specificate i parametri desiderati per la chiave. I parametri richiesti sono:

   * **tipo** chiave: RSA
   * **lunghezza** chiave: 1024 - 4096 bit
   * **nome** reale e indirizzo **** e-mail: Consente di tenere traccia di chi ha creato la coppia di chiavi. Immettete un nome e un indirizzo e-mail collegati all’organizzazione o al dipartimento.
   * **commento**: l&#39;aggiunta di un&#39;etichetta al campo del commento consente di identificare facilmente la chiave da utilizzare per cifrare i dati.
   * **scadenza**: Data o &quot;0&quot; per nessuna data di scadenza.
   * **passphrase**
   ![](assets/do-not-localize/gpg_command.png)

1. Una volta confermato, lo script genererà una chiave con l&#39;impronta digitale associata, da esportare in un file o incollare direttamente nel Pannello di controllo. Per esportare il file, eseguire questo comando seguito dall&#39;impronta digitale della chiave generata.

   `gpg -a --export <fingerprint>`

1. Per installare la chiave pubblica nel Pannello di controllo, aprite la **[!UICONTROL Instance settings]** scheda, quindi selezionate la **[!UICONTROL GPG keys]** scheda e l&#39;istanza desiderata.

1. Fai clic sul pulsante **[!UICONTROL Install Key]**. 

   ![](assets/gpg_install_button.png)

1. Incollate la chiave pubblica generata dal vostro strumento di crittografia PGP. Potete anche trascinare e rilasciare direttamente il file della chiave pubblica esportato.

   >[!NOTE]
   >
   >La chiave pubblica deve essere in formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Fai clic sul pulsante **[!UICONTROL Install Key]**. 

Una volta installata la chiave pubblica, questa viene visualizzata nell&#39;elenco. Puoi usare il **...** per scaricarlo o copiarne l&#39;impronta digitale.

![](assets/gpg_install_download.png)

La chiave è quindi disponibile per l&#39;uso nei flussi di lavoro  Adobe Campaign. È possibile utilizzarlo per cifrare i dati quando si utilizzano le attività di estrazione dei dati.

Per ulteriori informazioni, consulta la documentazione  Adobe Campaign:

**Campaign Classic:**

* [Zipping o cifratura di un file](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [Caso di utilizzo: Cifratura ed esportazione dei dati tramite una chiave installata nel Pannello di controllo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso di utilizzo: Cifratura ed esportazione dei dati tramite una chiave installata nel Pannello di controllo](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## Decrittografare i dati {#decrypting-data}

Il Pannello di controllo consente di decrittografare dati esterni nelle istanze del Adobe Campaign .

A tal fine, è necessario generare una coppia di chiavi GPG direttamente dal Pannello di controllo.

* La chiave **** pubblica verrà condivisa con il sistema esterno, che la utilizzerà per crittografare i dati da inviare a Campaign.
* La chiave **** privata verrà utilizzata da Campaign per decifrare i dati crittografati in arrivo.

Per generare una coppia di chiavi nel Pannello di controllo, procedere come segue:

1. Aprite la **[!UICONTROL Instance settings]** scheda, quindi selezionate la **[!UICONTROL GPG keys]** scheda e l&#39;istanza di Adobe Campaign  desiderata.

1. Fai clic sul pulsante **[!UICONTROL Generate Key]**. 

   ![](assets/gpg_generate.png)

1. Specificate il nome della chiave, quindi fate clic su **!UICONTROL Generate Key]**. Questo nome ti aiuterà a identificare la chiave da usare per la decrittazione nei flussi di lavoro Campaign

   ![](assets/gpg_generate_name.png)

Una volta generata la coppia di chiavi, nell&#39;elenco viene visualizzata la chiave pubblica. Si noti che le coppie di chiavi di decrittazione vengono generate senza data di scadenza.

Puoi usare il **...** per scaricare la chiave pubblica o copiarne l’impronta digitale.

![](assets/gpg_generate_list.png)

La chiave pubblica è quindi disponibile per essere condivisa con qualsiasi sistema esterno.  Adobe Campaign sarà in grado di utilizzare la chiave privata nelle attività di caricamento dei dati per decrittografare i dati crittografati con la chiave pubblica.

Per ulteriori informazioni, consulta la documentazione  Adobe Campaign:

**Campaign Classic:**

* [Estrazione o decrittografia di un file prima dell&#39;elaborazione](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [Caso di utilizzo: Importazione di dati crittografati con una chiave generata dal Pannello di controllo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso di utilizzo: Importazione di dati crittografati con una chiave generata dal Pannello di controllo](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Monitoraggio delle chiavi GPG

Per accedere ai tasti GPG installati e generati per le istanze, aprite la **[!UICONTROL Instance settings]** scheda, quindi selezionate la **[!UICONTROL GPG keys]** scheda.

![](assets/gpg_list.png)

Nell&#39;elenco sono visualizzate tutte le chiavi GPG di cifratura e decrittazione installate e generate per le istanze, con informazioni dettagliate su ciascuna chiave:

* **[!UICONTROL Name]**: Nome definito al momento dell’installazione o della generazione della chiave.
* **[!UICONTROL Use case]**: Questa colonna specifica il caso di utilizzo della chiave:

   ![](assets/gpg_icon_encrypt.png): La chiave è stata installata per la crittografia dei dati.

   ![](assets/gpg_icon_decrypt.png): La chiave è stata generata per consentire la decrittografia dei dati.

* **[!UICONTROL Fingerprint]**: l&#39;impronta digitale della chiave.
* **[!UICONTROL Expires]**: Data di scadenza della chiave. Il Pannello di controllo fornirà indicazioni visive man mano che la chiave si avvicina alla data di scadenza:

   * Urgente (rosso) è mostrato 30 giorni prima.
   * L&#39;avviso (giallo) è visualizzato 60 giorni prima.
   * Alla scadenza di una chiave viene visualizzato un banner rosso &quot;Scaduto&quot;.
   >[!NOTE]
   >
   >Il Pannello di controllo non invierà alcuna notifica e-mail.

Come procedura ottimale, si consiglia di rimuovere qualsiasi chiave non più necessaria. Per eseguire questa operazione, fare clic sul **..** quindi selezionate **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Prima di rimuovere una chiave, accertatevi che non sia utilizzata in alcun flusso di lavoro  Adobe Campaign per evitare che si verifichi un errore.
