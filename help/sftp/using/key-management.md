---
title: Gestione delle chiavi
description: Scopri come gestire le chiavi per la connessione ai server SFTP
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Gestione delle chiavi {#key-management}

Adobe consiglia a tutti i clienti di stabilire una connessione ai propri server SFTP con una **coppia di chiavi pubblica e privata**.

Di seguito sono descritti i passaggi per generare una chiave SSH pubblica e aggiungerla per accedere al server SFTP, nonché le raccomandazioni relative all&#39;autenticazione.

Una volta configurato l&#39;accesso al server, ricordate di **inserire in una whitelist gli indirizzi** IP che richiederanno l&#39;accesso al server in modo da potervi collegare. For more on this, refer to [this section](../../instances-settings/using/ip-whitelisting-instance-access.md).

>[!NOTE]
>
>Attualmente non è possibile eliminare una chiave pubblica SSH.

## Best practice {#best-practices}

**Informazioni sulla chiave SSH pubblica**

Assicuratevi di utilizzare sempre la stessa autenticazione per collegarvi al server e di utilizzare un formato supportato per la chiave.

**Integrazione API con nome utente e password**

In casi molto rari l&#39;autenticazione basata sulla password è abilitata su alcuni server SFTP. Adobe consiglia di utilizzare l&#39;autenticazione basata sulle chiavi, in quanto questo metodo è più efficiente e sicuro. Puoi richiedere di passare all&#39;autenticazione basata sulle chiavi contattando l&#39;Assistenza clienti.

>[!CAUTION]
>
>Se la password scade, anche in presenza di chiavi installate nel sistema, non potrai accedere ai tuoi account SFTP.

![](assets/control_panel_passwordexpires.png)

## Installazione della chiave SSH {#installing-ssh-key}

>[!CAUTION]
>
>I passaggi indicati di seguito sono solo un esempio di creazione di chiavi SSH. Seguite le linee guida aziendali relative alle chiavi SSH. L&#39;esempio seguente è solo un esempio di come ciò possa essere fatto e funge da utile punto di riferimento per comunicare i requisiti al team o al gruppo di rete interno.

1. Navigate to the **[!UICONTROL Key Management]**tab, then click the**[!UICONTROL Add public key]** button.

   ![](assets/key0.png)

1. Nella finestra di dialogo visualizzata, selezionate il nome utente per il quale desiderate creare la chiave pubblica e il server per il quale desiderate attivare la chiave.

   >[!NOTE]
   >
   >L&#39;interfaccia controllerà se un determinato nome utente è attivo in una determinata istanza e vi darà la possibilità di attivare la chiave in una o più istanze.
   >
   >Per ogni utente è possibile aggiungere una o più chiavi SSH pubbliche.

   ![](assets/key1.png)

1. Copiare e incollare la chiave SSH pubblica. Per generare una chiave pubblica, attenetevi alla procedura seguente che corrisponde al sistema operativo in uso:

   >[!NOTE]
   >
   >La dimensione della chiave SSH pubblica deve essere **2048 bit**.

   **Linux e Mac:**

   Utilizzate il terminale per generare una coppia di chiavi pubblica e privata:
   1. Immettete questo comando: `ssh-keygen -t rsa -C <your_email@example.com>`.
   1. Quando richiesto, specificate un nome alla chiave. Se la directory .ssh non esiste, il sistema ne creerà una per voi.
   1. Quando richiesto, inserite di nuovo una passphrase. Può anche essere lasciata vuota.
   1. Il sistema crea una coppia di chiavi &quot;name&quot; e &quot;name.pub&quot;. Cercate il file &quot;name.pub&quot;, quindi apritelo. Deve avere una stringa alfanumerica che termina con l&#39;indirizzo e-mail specificato.
   **Windows:**

   Potrebbe essere necessario installare uno strumento di terze parti che vi aiuterà a generare una coppia di chiavi pubblica/privata nello stesso formato &quot;name.pub&quot;.

1. Aprite il file .pub, quindi copiate e incollate l’intera stringa a partire da &quot;ssh...&quot; nel Pannello di controllo.

   ![](assets/publickey.png)

1. Fate clic sul **[!UICONTROL Save]**pulsante per creare la chiave. Il Pannello di controllo salva la chiave pubblica e l&#39;impronta digitale associata, crittografata con il formato SHA256.

È possibile utilizzare le impronte digitali per far corrispondere le chiavi private salvate sul computer con le corrispondenti chiavi pubbliche salvate nel Pannello di controllo.

![](assets/fingerprint_compare.png)

Il messaggio &quot;**...**&quot; consente di eliminare una chiave esistente o di copiarne l’impronta digitale negli Appunti.

![](assets/key_options.png)
