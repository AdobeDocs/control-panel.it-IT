---
product: campaign
solution: Campaign
title: Gestione chiavi GPG
description: Scoprite come gestire le chiavi GPG per cifrare e decifrare i dati in  Adobe Campaign.
translation-type: tm+mt
source-git-commit: e41f92fc80f77a8d4a4067360725ce3d6efe3f4c
workflow-type: tm+mt
source-wordcount: '1153'
ht-degree: 8%

---


# Gestione chiavi GPG {#gpg-keys-management}

## Informazioni sulla crittografia GPG {#about-gpg-encryption}

La crittografia GPG consente di proteggere i dati utilizzando un sistema di coppie di chiavi pubblica-privata che seguono la specifica [OpenPGP](https://www.openpgp.org/about/standard/).

Una volta implementati, è possibile che i dati in entrata siano decrittografati e quelli in uscita crittografati prima del trasferimento, per garantire che non siano accessibili a nessuno senza una coppia di chiavi corrispondente valida.

Per implementare la crittografia GPG con Campaign, un utente amministratore deve installare e/o generare le chiavi GPG in un’istanza di marketing direttamente dal Pannello di controllo Campaign.

Potrete quindi:

* **Cifra dati** inviati:  Adobe Campaign invia i dati dopo averli crittografati con la chiave pubblica installata.

* **Decrittografa dati** in arrivo:  Adobe Campaign riceve i dati crittografati da un sistema esterno utilizzando una chiave pubblica scaricata dal Pannello di controllo Campaign.  Adobe Campaign decrittografa i dati utilizzando una chiave privata generata dal Pannello di controllo Campaign.

## Cifratura dei dati {#encrypting-data}

Il Pannello di controllo Campaign consente di crittografare i dati provenienti dall’istanza Adobe Campaign.

A tal fine, è necessario generare una coppia di chiavi GPG da uno strumento di crittografia PGP, quindi installare la chiave pubblica nel Pannello di controllo Campaign. Sarà quindi possibile crittografare i dati prima di inviarli dall&#39;istanza. Per farlo, segui la procedura indicata di seguito.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](#video)

1. Generare una coppia di chiavi pubblica/privata utilizzando uno strumento di crittografia PGP che segue la [specifica OpenPGP](https://www.openpgp.org/about/standard/). A tal fine, installare un&#39;utility GPG o un software GNuGP.

   >[!NOTE]
   >
   >È disponibile un software libero open source per generare chiavi. Tuttavia, accertatevi di seguire le linee guida della vostra organizzazione e di utilizzare l&#39;utility GPG consigliata dall&#39;organizzazione IT/Security.

1. Una volta installata l&#39;utility, eseguite il comando seguente, in Mac Terminal o Windows.

   `gpg --full-generate-key`

1. Quando richiesto, specificate i parametri desiderati per la chiave. I parametri richiesti sono:

   * **tipo** chiave: RSA
   * **lunghezza** chiave: 1024 - 4096 bit
   * **nome reale** e indirizzo **** e-mail: Consente di tenere traccia di chi ha creato la coppia di chiavi. Immettete un nome e un indirizzo e-mail collegati all’organizzazione o al dipartimento.
   * **commento**: l&#39;aggiunta di un&#39;etichetta al campo del commento consente di identificare facilmente la chiave da utilizzare per cifrare i dati.
   * **scadenza**: Data o &quot;0&quot; per nessuna data di scadenza.
   * **passphrase**

   ![](assets/do-not-localize/gpg_command.png)

1. Una volta confermato, lo script genererà una chiave con l&#39;impronta digitale associata, da esportare in un file o incollare direttamente nel Pannello di controllo Campaign. Per esportare il file, eseguire questo comando seguito dall&#39;impronta digitale della chiave generata.

   `gpg -a --export <fingerprint>`

1. Per installare la chiave pubblica nel Pannello di controllo Campaign, aprite la scheda **[!UICONTROL Instance settings]**, quindi selezionate la scheda **[!UICONTROL GPG keys]** e l&#39;istanza desiderata.

1. Fai clic sul pulsante **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Incollate la chiave pubblica generata dal vostro strumento di crittografia PGP. Potete anche trascinare e rilasciare direttamente il file della chiave pubblica esportato.

   >[!NOTE]
   >
   >La chiave pubblica deve essere in formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Fai clic sul pulsante **[!UICONTROL Install Key]**.

Una volta installata la chiave pubblica, questa viene visualizzata nell&#39;elenco. È possibile utilizzare la **...Pulsante** per scaricarlo o copiarne l&#39;impronta digitale.

![](assets/gpg_install_download.png)

La chiave è quindi disponibile per l&#39;uso  flussi di lavoro Adobe Campaign. È possibile utilizzarlo per cifrare i dati quando si utilizzano le attività di estrazione dei dati.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](#video)

Per ulteriori informazioni su questo argomento, consulta  documentazione Adobe Campaign:

**Campaign Classic:**

* [Zipping o cifratura di un file](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [Caso di utilizzo: Cifratura ed esportazione di dati tramite una chiave installata sul Pannello di controllo Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso di utilizzo: Cifratura ed esportazione di dati tramite una chiave installata sul Pannello di controllo Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## Decrittografia dei dati {#decrypting-data}

Pannello di controllo Campaign consente di decrittografare dati esterni nelle istanze Adobe Campaign .

A tal fine, è necessario generare una coppia di chiavi GPG direttamente dal Pannello di controllo Campaign.

* La **chiave pubblica** verrà condivisa con il sistema esterno, che la utilizzerà per cifrare i dati da inviare a Campaign.
* La **chiave privata** verrà utilizzata da Campaign per decrittografare i dati crittografati in arrivo.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](#video)

Per generare una coppia di chiavi nel Pannello di controllo Campaign, effettuate le seguenti operazioni:

1. Aprite la scheda **[!UICONTROL Instance settings]**, quindi selezionate la scheda **[!UICONTROL GPG keys]** e l&#39;istanza  Adobe Campaign desiderata.

1. Fai clic sul pulsante **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Specificate il nome della chiave, quindi fate clic su **[!UICONTROL Generate Key]**. Questo nome ti aiuterà a identificare la chiave da usare per la decrittazione nei flussi di lavoro Campaign

   ![](assets/gpg_generate_name.png)

Una volta generata la coppia di chiavi, nell&#39;elenco viene visualizzata la chiave pubblica. Si noti che le coppie di chiavi di decrittazione vengono generate senza data di scadenza.

È possibile utilizzare la **...** per scaricare la chiave pubblica o copiarne l&#39;impronta digitale.

![](assets/gpg_generate_list.png)

La chiave pubblica è quindi disponibile per essere condivisa con qualsiasi sistema esterno.  Adobe Campaign sarà in grado di utilizzare la chiave privata nelle attività di caricamento dei dati per decifrare i dati crittografati con la chiave pubblica.

Per ulteriori informazioni, consulta  documentazione Adobe Campaign:

**Campaign Classic:**

* [Estrazione o decrittografia di un file prima dell&#39;elaborazione](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [Caso di utilizzo: Importazione di dati crittografati con una chiave generata dal Pannello di controllo Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso di utilizzo: Importazione di dati crittografati con una chiave generata dal Pannello di controllo Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Monitoraggio delle chiavi GPG

Per accedere ai tasti GPG installati e generati per le istanze, aprite la scheda **[!UICONTROL Instance settings]**, quindi selezionate la scheda **[!UICONTROL GPG keys]**.

![](assets/gpg_list.png)

Nell&#39;elenco sono visualizzate tutte le chiavi GPG di cifratura e decrittazione installate e generate per le istanze, con informazioni dettagliate su ciascuna chiave:

* **[!UICONTROL Name]**: Nome definito al momento dell’installazione o della generazione della chiave.
* **[!UICONTROL Use case]**: Questa colonna specifica il caso di utilizzo della chiave:

   ![](assets/gpg_icon_encrypt.png): La chiave è stata installata per la crittografia dei dati.

   ![](assets/gpg_icon_decrypt.png): La chiave è stata generata per consentire la decrittografia dei dati.

* **[!UICONTROL Fingerprint]**: l&#39;impronta digitale della chiave.
* **[!UICONTROL Expires]**: Data di scadenza della chiave. Si noti che il Pannello di controllo Campaign fornirà indicazioni visive man mano che la chiave si avvicina alla sua data di scadenza:

   * Urgente (rosso) è mostrato 30 giorni prima.
   * L&#39;avviso (giallo) è visualizzato 60 giorni prima.
   * Alla scadenza di una chiave viene visualizzato un banner rosso &quot;Scaduto&quot;.

   >[!NOTE]
   >
   >Notate che il Pannello di controllo Campaign non invierà alcuna notifica e-mail.

Come procedura ottimale, si consiglia di rimuovere qualsiasi chiave non più necessaria. A tale scopo, fare clic sul simbolo **...** quindi selezionare **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Prima di rimuovere una chiave, accertatevi che non sia utilizzata in alcun  flusso di lavoro Adobe Campaign per evitare che si verifichi un errore.

## Video di esercitazione {#video}

Il video seguente mostra come generare e installare le chiavi GPG per la crittografia dei dati.

Video dedicati alla gestione delle chiavi GPG sono disponibili nelle pagine delle esercitazioni [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings) e [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)

