---
title: Gestione delle chiavi
description: Scopri come gestire le chiavi per la connessione ai server SFTP
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: ht
source-wordcount: '597'
ht-degree: 100%

---


# Gestione delle chiavi {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Informazioni sulla gestione delle chiavi"
>abstract="In questa scheda puoi gestire le tue chiavi pubbliche."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Guarda il video dimostrativo"

Adobe consiglia a tutti i clienti di stabilire una connessione ai propri server SFTP con una **coppia di chiavi pubblica e privata**.

Di seguito sono descritti i passaggi per generare una chiave SSH pubblica e aggiungerla per accedere al server SFTP, nonché le raccomandazioni relative all’autenticazione.

Una volta configurato l’accesso al server, ricorda di **inserire nella whitelist gli indirizzi IP** che richiederanno l’accesso al server in modo da poterti connettere a esso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../../instances-settings/using/ip-whitelisting-instance-access.md).

>[!NOTE]
>
>Attualmente non è possibile eliminare una chiave pubblica SSH.

## Best practice {#best-practices}

**Informazioni sulla chiave SSH pubblica**

Assicurati di utilizzare sempre la stessa autenticazione per connetterti al server e di utilizzare un formato supportato per la chiave.

**Integrazione API con nome utente e password**

In casi molto rari l’autenticazione basata sulla password è abilitata su alcuni server SFTP. Adobe consiglia di utilizzare l’autenticazione basata sulle chiavi, in quanto questo metodo è più efficiente e sicuro. Puoi richiedere di passare all’autenticazione basata sulle chiavi contattando l’Assistenza clienti.

>[!IMPORTANT]
>
>Se la tua password scade, anche in presenza di chiavi installate nel sistema, non potrai accedere ai tuoi account SFTP.

![](assets/control_panel_passwordexpires.png)

## Installazione della chiave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Aggiungere una nuova chiave pubblica"
>abstract="Aggiungi una nuova chiave pubblica per un’istanza."

>[!IMPORTANT]
>
>I passaggi indicati di seguito sono solo un esempio di creazione di chiavi SSH. Segui le linee guida aziendali relative alle chiavi SSH. Il seguente è solo un esempio di come ciò possa essere fatto e funge da utile punto di riferimento per la comunicazione dei requisiti al tuo team o gruppo di rete interno.

1. Accedi alla scheda **[!UICONTROL Key Management]**, quindi fai clic sul pulsante **[!UICONTROL Add new public key]**.

   ![](assets/key0.png)

1. Nella finestra di dialogo visualizzata, seleziona il nome utente per il quale desideri creare la chiave pubblica e il server per il quale desideri attivare la chiave.

   >[!NOTE]
   >
   >L’interfaccia controllerà se un determinato nome utente è attivo in una determinata istanza e ti darà la possibilità di attivare la chiave in una o più istanze.
   >
   >Per ogni utente è possibile aggiungere una o più chiavi SSH pubbliche.

   ![](assets/key1.png)

1. Copia e incolla la chiave SSH pubblica. Per generare una chiave pubblica, attieniti alla procedura seguente corrispondente al tuo sistema operativo:

   >[!NOTE]
   >
   >La dimensione della chiave SSH pubblica deve essere **2048 bit**.

   **Linux e Mac:**

   Utilizza il terminale per generare una coppia di chiavi pubblica e privata:
   1. Inserisci questo comando: `ssh-keygen -t rsa -C <your_email@example.com>`.
   1. Quando richiesto, specifica un nome alla chiave. Se la directory .ssh non esiste, il sistema ne creerà una.
   1. Inserisci e reinserisci una passphrase quando richiesto. Può anche essere lasciata vuota.
   1. Il sistema crea una coppia di chiavi “name” e “name.pub”. Cerca il file “name.pub”, quindi aprilo. Deve avere una stringa alfanumerica che termina con l’indirizzo e-mail specificato.
   **Windows:**

   Potrebbe essere necessario installare uno strumento di terze parti che ti aiuterà a generare una coppia di chiavi pubblica/privata nello stesso formato “name.pub”.

1. Apri il file .pub, quindi copia e incolla l’intera stringa a partire da “ssh...” nel Pannello di controllo Campaign.

   ![](assets/publickey.png)

1. Fai clic sul pulsante **[!UICONTROL Save]** per creare la chiave. Il Pannello di controllo Campaign salva la chiave pubblica e l’impronta digitale associata, crittografate con il formato SHA256.

Puoi utilizzare le impronte digitali per far corrispondere le chiavi private salvate sul computer alle corrispondenti chiavi pubbliche salvate nel Pannello di controllo Campaign.

![](assets/fingerprint_compare.png)

Il pulsante “**...**” ti consente di eliminare una chiave esistente o di copiarne l’impronta digitale negli Appunti.

![](assets/key_options.png)
