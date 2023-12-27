---
product: campaign
solution: Campaign
title: Gestione delle chiavi
description: Scopri come gestire le chiavi per la connessione ai server SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '1058'
ht-degree: 100%

---

# Gestione delle chiavi {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Informazioni sulla gestione delle chiavi pubbliche"
>abstract="In questa scheda puoi creare, gestire e modificare le tue chiavi pubbliche."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Guarda il video dimostrativo"

Adobe consiglia a tutti i clienti di stabilire una connessione ai propri server SFTP con una **coppia di chiavi pubblica e privata**.

Di seguito sono descritti i passaggi per generare una chiave SSH pubblica e aggiungerla per accedere al server SFTP, nonché le raccomandazioni relative all’autenticazione.

Una volta configurato l’accesso al server, ricorda di **inserire nell’elenco Consentiti gli indirizzi IP che richiederanno l’accesso al server** in modo da poterti connettere a esso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../../instances-settings/using/ip-allow-listing-instance-access.md).

![](assets/do-not-localize/how-to-video.png) Guarda il video su questa funzione per [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html?lang=it#sftp-management) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=it#sftp-management)

## Best practice {#best-practices}

**Informazioni sulla chiave SSH pubblica**

Assicurati di utilizzare sempre la stessa autenticazione per connetterti al server e di utilizzare un formato supportato per la chiave.

**Integrazione API con nome utente e password**

In casi molto rari l’autenticazione basata sulla password è abilitata su alcuni server SFTP. Adobe consiglia di utilizzare l’autenticazione basata sulle chiavi, in quanto questo metodo è più efficiente e sicuro. Puoi richiedere di passare all’autenticazione basata sulle chiavi contattando l’Assistenza clienti.

>[!IMPORTANT]
>
>Se la tua password scade, anche in presenza di chiavi installate nel sistema, non potrai accedere ai tuoi account SFTP.

## Installazione della chiave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Aggiunta di una chiave pubblica"
>abstract="Genera una chiave SSH pubblica per un’istanza e aggiungila al Pannello di controllo per accedere al server SFTP."

>[!IMPORTANT]
>
>Segui sempre le linee guida della tua organizzazione per quanto riguarda le chiavi SSH. I passaggi riportati di seguito rappresentano solo un esempio di come può essere effettuata la creazione di chiavi SSH; puoi utilizzarli come punto di riferimento utile per la comunicare i requisiti al tuo team o al gruppo di rete interno.

1. Passa alla scheda **[!UICONTROL Gestione delle chiavi]**, quindi fai clic sul pulsante **[!UICONTROL Aggiungi nuova chiave pubblica]**.

   ![](assets/key0.png)

1. Nella finestra di dialogo visualizzata, seleziona il nome utente per il quale desideri creare la chiave pubblica e il server per il quale desideri attivare la chiave.

   ![](assets/key1.png)

   >[!NOTE]
   >
   >Il pannello di controllo verificherà se un determinato nome utente è attivo in una determinata istanza e ti darà la possibilità di attivare la chiave in una o più istanze.
   >
   >Per ogni utente è possibile aggiungere una o più chiavi SSH pubbliche.

1. Per gestire meglio le chiavi pubbliche, puoi impostare una durata per la disponibilità di ciascuna chiave. A tale scopo, seleziona un’unità nell’elenco a discesa **[!UICONTROL Tipo]** e definisci una durata nel campo corrispondente. Per ulteriori informazioni sulla scadenza della chiave pubblica, consulta [questa sezione](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >Per impostazione predefinita, il campo **[!UICONTROL Tipo]** è impostato su **[!UICONTROL Illimitato]**, il che significa che la chiave pubblica non scade mai.

1. Nel campo **[!UICONTROL Commento]**, puoi indicare un motivo per l’aggiunta di questa chiave pubblica (perché, per chi, ecc.).

1. Per poter compilare il campo **[!UICONTROL Chiave pubblica]**, è necessario generare una chiave pubblica SSH. Segui i passaggi riportati di seguito in base al sistema operativo in uso.

   **Linux e Mac:**

   Utilizza il terminale per generare una coppia di chiavi pubblica e privata:
   1. Inserisci questo comando: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Quando richiesto, specifica un nome alla chiave. Se la directory .ssh non esiste, il sistema ne creerà una.
   1. Inserisci e reinserisci una passphrase quando richiesto. Può anche essere lasciata vuota.
   1. Il sistema crea una coppia di chiavi “name” e “name.pub”. Cerca il file “name.pub”, quindi aprilo. Deve avere una stringa alfanumerica che termina con l’indirizzo e-mail specificato.

   **Windows:**

   Potrebbe essere necessario installare uno strumento di terze parti che ti aiuterà a generare una coppia di chiavi pubblica/privata nello stesso formato “name.pub”.

1. Apri il file .pub, quindi copia e incolla nel Pannello di controllo l’intera stringa a partire da “ssh...”.

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >Il campo **[!UICONTROL Chiave pubblica]** accetta solo il formato OpenSSH. La dimensione della chiave SSH pubblica deve essere **2048 bit**.

1. Fai clic sul pulsante **[!UICONTROL Salva]** per creare la chiave. Il Pannello di controllo salva la chiave pubblica e l’impronta digitale associata, crittografate con il formato SHA256.

>[!IMPORTANT]
>
>Se la chiave creata viene utilizzata per stabilire una connessione con un sistema che non è ancora mai stato collegato al server SFTP selezionato, sarà necessario aggiungere un IP pubblico di tale sistema all’elenco Consentiti prima di poter utilizzare questo sistema con il server SFTP. Consulta [questa sezione](ip-range-allow-listing.md).

Puoi utilizzare le impronte digitali per far corrispondere le chiavi private salvate sul computer alle chiavi pubbliche corrispondenti salvate nel Pannello di controllo.

![](assets/fingerprint_compare.png)

Il pulsante “**...**” consente di eliminare una chiave esistente o di copiarne l’impronta digitale negli Appunti.

![](assets/key_options.png)

## Gestione delle chiavi pubbliche {#managing-public-keys}

Le chiavi pubbliche create vengono visualizzate nella scheda **[!UICONTROL Gestione delle chiavi]**.

Puoi ordinare gli elementi in base alla data di creazione o di modifica, all’utente che li ha creati o modificati e alla scadenza degli intervalli IP.

È inoltre possibile cercare una chiave pubblica iniziando a digitare un nome o un commento.

![](assets/control_panel_key_management_sort.png)

Per modificare uno o più intervalli IP, consulta [questa sezione](#editing-public-keys).

Per eliminare una o più chiavi pubbliche dall’elenco, selezionale, quindi fai clic sul pulsante **[!UICONTROL Elimina chiave pubblica]**.

![](assets/control_panel_delete_key.png)

### Scadenza {#expiry}

La colonna **[!UICONTROL Scade]** mostra quanti giorni mancano alla scadenza della chiave pubblica.

Se ti sei iscritto agli [avvisi e-mail](../../performance-monitoring/using/email-alerting.md), riceverai delle notifiche tramite e-mail 10 giorni e 5 giorni prima della scadenza di una chiave pubblica e il giorno stesso della scadenza. Dopo aver ricevuto l’avviso, puoi [modificare la chiave pubblica](#editing-public-keys) per prolungarne, se necessario, il periodo di validità.

Una chiave pubblica scaduta verrà eliminata automaticamente dopo 7 giorni. Viene visualizzata come **[!UICONTROL Scaduta]** nella colonna **[!UICONTROL Scade]**. Entro questo periodo di 7 giorni:

* Una chiave pubblica scaduta non può più essere utilizzata per connettersi al server SFTP.

* È possibile [modificare](#editing-public-keys) una chiave pubblica scaduta e aggiornarne la durata per renderla nuovamente disponibile.

* Puoi eliminarla dall’elenco.

## Modifica delle chiavi pubbliche {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="Modificare le chiavi pubbliche"
>abstract="Aggiorna le chiavi pubbliche selezionate per accedere al server SFTP."

Per modificare le chiavi pubbliche, segui la procedura indicata di seguito.

>[!NOTE]
>
>Puoi modificare solo le chiavi pubbliche create a partire dal rilascio di ottobre 2021 del Pannello di controllo.

1. Seleziona uno o più elementi dall’elenco **[!UICONTROL Gestione delle chiavi]** .
1. Fai clic sul pulsante **[!UICONTROL Aggiorna chiave pubblica]**.

   ![](assets/control_panel_edit_key.png)

1. Puoi modificare solo la scadenza della chiave pubblica e/o aggiungere un nuovo commento.

   >[!NOTE]
   >
   >Per modificare il nome utente, l’istanza e la chiave pubblica nel formato OpenSSH, elimina la chiave pubblica e creane una nuova che corrisponda alle tue esigenze.

1. Salva le modifiche.
