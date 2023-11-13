---
product: campaign
solution: Campaign
title: Gestione chiavi GPG
description: Scopri come gestire le chiavi GPG per crittografare e decrittografare i dati in Adobe Campaign.
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: ht
source-wordcount: '1232'
ht-degree: 100%

---

# Gestione chiavi GPG {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="Informazioni sulle chiavi GPG"
>abstract="In questa scheda puoi installare e/o generare chiavi GPG su un’istanza marketing per crittografare i dati inviati da Campaign e decrittografare i dati in arrivo."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=it" text="Informazioni sul monitoraggio delle prestazioni"

## Informazioni sulla crittografia GPG {#about-gpg-encryption}

La crittografia GPG consente di proteggere i dati utilizzando un sistema di coppie di chiavi pubblica-privata che seguono la specifica [OpenPGP](https://www.openpgp.org/about/standard/).

Una volta implementata, i dati in entrata possono essere decrittografati e quelli in uscita crittografati prima del trasferimento, affinché nessuno possa accedervi senza una coppia di chiavi valida.

Per implementare la crittografia GPG con Campaign, un utente amministratore deve installare e/o generare le chiavi GPG in un’istanza di marketing direttamente dal Pannello di controllo.

Potrai quindi:

* **Crittografare i dati inviati**: Adobe Campaign invia i dati dopo averli crittografati con la chiave pubblica installata.

* **Decrittografare i dati in entrata**: Adobe Campaign riceve i dati crittografati da un sistema esterno che utilizza una chiave pubblica scaricata dal Pannello di controllo. Adobe Campaign decrifra i dati utilizzando una chiave privata generata dal Pannello di controllo.

## Crittografia dei dati {#encrypting-data}

Il Pannello di controllo consente di crittografare i dati provenienti dall’istanza Adobe Campaign.

A questo scopo, devi generare una coppia di chiavi GPG con uno strumento di crittografia PGP, quindi installare la chiave pubblica nel Pannello di controllo. Potrai quindi crittografare i dati prima di inviarli dall’istanza. A tale scopo, segui la procedura indicata di seguito.

>[!NOTE]
>
>Nel Pannello di controllo puoi installare fino a 60 chiavi GPG.

![](assets/do-not-localize/how-to-video.png) Guarda il [video su questa funzione](#video)

1. Genera una coppia di chiavi pubblica/privata utilizzando uno strumento di crittografia PGP che segue la [specifica OpenPGP](https://www.openpgp.org/about/standard/). Per eseguire questa operazione, installa un’utility GPG o un software GNuGP.

   >[!NOTE]
   >
   >Sono disponibili software gratuiti open source per generare le chiavi. Tuttavia, assicurati di seguire le linee guida della tua organizzazione e utilizza l’utility GPG consigliata dal reparto IT/Sicurezza della tua organizzazione.

1. Una volta installata l’utility, esegui il comando seguente nel Terminale per Mac o nel prompt dei comandi in Windows.

   `gpg --full-generate-key`

1. Quando richiesto, specifica i parametri desiderati per la chiave. I parametri richiesti sono:

   * **key type**: (tipo di chiave) RSA
   * **key length**: (lunghezza chiave) 3072 - 4096 bit
   * **real name** e **email address**: (nome reale e indirizzo e-mail): consente di tenere traccia di chi ha creato la coppia di chiavi. Immetti un nome e un indirizzo e-mail collegati alla tua organizzazione o al tuo reparto.
   * **comment**: (commento) se aggiungi un’etichetta al campo del commento, sarà più facile riconoscere la chiave da utilizzare per crittografare i dati.
     >[!IMPORTANT]
     >
     >Assicurati che questo campo non sia lasciato vuoto e che sia inserito un commento.

   * **expiration**: (scadenza) data oppure “0” se non vi è una data di scadenza.
   * **passphrase**

   ![](assets/do-not-localize/gpg_command.png)

1. Una volta confermato, lo script genera una chiave con l’impronta digitale associata, che puoi esportare in un file o incollare direttamente nel Pannello di controllo. Per esportare il file, esegui questo comando seguito dall’impronta digitale della chiave generata.

   `gpg -a --export <fingerprint>`

1. Per installare la chiave pubblica nel Pannello di controllo, apri la scheda **[!UICONTROL Impostazioni istanze]**, quindi seleziona la scheda **[!UICONTROL Chiavi GPG]** e l’istanza desiderata.

1. Fai clic sul pulsante **[!UICONTROL Installa chiave]**.

   ![](assets/gpg_install_button.png)

1. Incolla la chiave pubblica generata dallo strumento di crittografia PGP. Puoi anche trascinare direttamente il file della chiave pubblica esportato.

   >[!NOTE]
   >
   >La chiave pubblica deve essere in formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Fai clic sul pulsante **[!UICONTROL Installa chiave]**.

Una volta installata, la chiave pubblica viene visualizzata nell’elenco. Puoi utilizzare il pulsante **...** per scaricarla o copiarne l’impronta digitale.

![](assets/gpg_install_download.png)

La chiave potrà quindi essere utilizzata nei flussi di lavoro di Adobe Campaign. Puoi utilizzarla per crittografare i dati quando utilizzi attività di estrazione dati.

![](assets/do-not-localize/how-to-video.png)Guarda il [video su questa funzione](#video)

Per ulteriori informazioni su questo argomento, consulta la documentazione di Adobe Campaign:

**Campaign v7/v8:**

* [Compressione o crittografia di un file](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=it)
* [Caso di utilizzo: crittografia ed esportazione di dati tramite una chiave installata sul Pannello di controllo](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=it#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=it)
* [Caso di utilizzo: crittografia ed esportazione di dati tramite una chiave installata sul Pannello di controllo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=it#use-case-gpg-encrypt)

## Decrittografia dei dati {#decrypting-data}

Il Pannello di controllo consente di decrittografare i dati esterni che entrano nelle istanze Adobe Campaign.

A questo scopo, devi generare una coppia di chiavi GPG direttamente dal Pannello di controllo.

* La **chiave pubblica** verrà condivisa con il sistema esterno, che lo utilizzerà per crittografare i dati da inviare a Campaign.
* La **chiave privata** verrà utilizzata da Campaign per decrittografare i dati crittografati in arrivo.

![](assets/do-not-localize/how-to-video.png)Guarda il [video su questa funzione](#video)

Per generare una coppia di chiavi nel Pannello di controllo, effettua le seguenti operazioni:

1. Apri la scheda **[!UICONTROL Impostazioni istanze]**, quindi seleziona la scheda **[!UICONTROL Chiavi GPG]** e l’istanza di Adobe Campaign desiderata.

1. Fai clic sul pulsante **[!UICONTROL Genera chiave]**.

   ![](assets/gpg_generate.png)

1. Specifica il nome della chiave, quindi fai clic su **[!UICONTROL Genera chiave]**. Questo nome ti aiuterà a identificare la chiave da utilizzare per la decrittografia nei flussi di lavoro di Campaign

   ![](assets/gpg_generate_name.png)

Una volta generata la coppia di chiavi, la chiave pubblica viene visualizzata nell’elenco. Tieni presente che le coppie di chiavi di decrittografia vengono generate senza data di scadenza.

Puoi utilizzare il pulsante **...** per scaricare la chiave pubblica o copiarne l’impronta digitale.

![](assets/gpg_generate_list.png)

La chiave pubblica è quindi disponibile per essere condivisa con qualsiasi sistema esterno. Adobe Campaign sarà in grado di utilizzare la chiave privata nelle attività di caricamento dei dati per decrittografare i dati crittografati con la chiave pubblica.

Per ulteriori informazioni, consulta la documentazione di Adobe Campaign:

**Campaign v7 e v8:**

* [Estrazione o decrittografia di un file prima dell’elaborazione](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=it)
* [Caso di utilizzo: importazione di dati crittografati utilizzando una chiave generata dal Pannello di controllo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=it#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gestione dei dati crittografati](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=it)
* [Caso di utilizzo: importazione di dati crittografati utilizzando una chiave generata dal Pannello di controllo](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=it#use-case-gpg-decrypt)

## Monitoraggio delle chiavi GPG

Per accedere alle chiavi GPG installate e generate per le istanze, apri la scheda **[!UICONTROL Impostazioni istanze]**, quindi seleziona la scheda **[!UICONTROL Chiavi GPG]**.

![](assets/gpg_list.png)

L’elenco mostra tutte le chiavi GPG di crittografia e decrittografia installate e generate per le istanze con informazioni dettagliate su ciascuna chiave:

* **[!UICONTROL Nome]**: nome definito durante l’installazione o la generazione della chiave.
* **[!UICONTROL Caso d’uso]**: questa colonna specifica il caso di utilizzo della chiave:

  ![](assets/gpg_icon_encrypt.png): la chiave per la crittografia dei dati è stata installata.

  ![](assets/gpg_icon_decrypt.png): la chiave è stata generata per consentire la decrittografia dei dati.

* **[!UICONTROL Impronta digitale]**: impronta digitale della chiave.
* **[!UICONTROL Scade]**: data di scadenza della chiave. Tieni presente che il Pannello di controllo fornirà indicazioni visive in prossimità della data di scadenza della chiave:

   * Urgente (rosso) viene visualizzato 30 giorni prima.
   * Avvertenza (giallo) viene visualizzata 60 giorni prima.
   * Una volta scaduta la chiave, verrà visualizzato un banner rosso con la dicitura “Scaduto”.

  >[!NOTE]
  >
  >Tieni presente che il Pannello di controllo non invierà alcuna notifica e-mail.

Come best practice, è consigliabile rimuovere le chiavi non più necessarie. A tale scopo, fai clic sul pulsante **...**, quindi seleziona **[!UICONTROL Elimina chiave].**

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Prima di rimuovere una chiave, assicurati che non sia utilizzata in alcun flusso di lavoro di Adobe Campaign, per evitare che si verifichino errori.

## Video tutorial {#video}

Il video seguente mostra come generare e installare le chiavi GPG per la crittografia dei dati.

Ulteriori video relativi alla gestione delle chiavi GPG sono disponibili nelle pagine dei tutorial per [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=it#instance-settings) e [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=it#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
