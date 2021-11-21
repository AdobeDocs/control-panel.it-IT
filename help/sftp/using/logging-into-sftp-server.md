---
product: campaign
solution: Campaign
title: Accesso al server SFTP
description: Scopri come accedere al server SFTP
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Accesso al server SFTP {#logging-into-sft-server}

I passaggi seguenti descrivono come collegare il server SFTP tramite l’applicazione client SFTP.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](https://video.tv.adobe.com/v/27263?quality=12)

Prima di accedere al server, assicurati che:

* Il server SFTP è **ospitato da Adobe**.
* Il tuo **nome utente** è stato configurato per il server. Puoi controllare queste informazioni direttamente nel Pannello di controllo Campaign, nel **Gestione delle chiavi** scheda dalla scheda SFTP.
* Hai un **coppia di chiavi privata e pubblica** per accedere al server SFTP. Fai riferimento a [questa sezione](../../sftp/using/key-management.md) per ulteriori informazioni su come aggiungere la chiave SSH.
* Le **l’indirizzo IP pubblico è stato aggiunto all’elenco consentiti** sul server SFTP. In caso contrario, fare riferimento a [questa sezione](../../sftp/using/ip-range-allow-listing.md) per ulteriori informazioni su come aggiungere l’intervallo IP all’elenco consentiti.
* Hai accesso a un **Software client SFTP**. Puoi consultare il tuo reparto IT per l’applicazione client SFTP che ti consigliano di utilizzare, oppure cercare una su Internet se consentito dalle politiche aziendali.

Per connettersi al server SFTP, procedi come segue:

1. Avvia il Pannello di controllo Campaign, quindi seleziona la **[!UICONTROL Key Management]** dalla scheda **[!UICONTROL SFTP]** il Card.

   ![](assets/sftp_card.png)

1. Avvia la tua applicazione client SFTP, quindi copia-incolla l&#39;indirizzo del server dal Pannello di controllo Campaign, seguito da &quot;campaign.adobe.com&quot;, quindi compila il tuo nome utente.

   ![](assets/do-not-localize/connect1.png)

1. In **[!UICONTROL SSH Private Key]** selezionare il file di chiave privata memorizzato nel computer. Corrisponde a un file di testo che ha lo stesso nome della chiave pubblica, senza l&#39;estensione &quot;.pub&quot; (ad esempio, &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   La **[!UICONTROL Password]** viene compilato automaticamente con la chiave privata del file .

   ![](assets/do-not-localize/connect3.png)

   Puoi verificare che la chiave che stai cercando di utilizzare sia salvata nel Pannello di controllo Campaign confrontando l&#39;impronta digitale della chiave privata o pubblica con l&#39;impronta digitale delle chiavi visualizzate nella scheda Key Management della scheda SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se si utilizza un computer Mac, è possibile visualizzare l&#39;impronta digitale della chiave privata memorizzata nel computer eseguendo questo comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una volta inserite tutte le informazioni, fai clic su **[!UICONTROL Connect]** per accedere al server SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
