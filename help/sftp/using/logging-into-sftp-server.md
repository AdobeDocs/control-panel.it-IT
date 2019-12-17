---
title: Accesso al server SFTP
description: Scopri come accedere al server SFTP
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Accesso al server SFTP {#logging-into-sft-server}

Nei passaggi seguenti viene descritto come collegare il server SFTP tramite l&#39;applicazione client SFTP.

Prima di accedere al server, accertatevi che:

* Il server SFTP è **ospitato da Adobe**.
* Il tuo **nome utente** è stato configurato per il server. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Hai una coppia **di chiavi pubblica e** privata per accedere al server SFTP. Per ulteriori informazioni su come aggiungere la chiave SSH, fare riferimento a [questa sezione](../../sftp/using/key-management.md) .
* Il tuo indirizzo IP **pubblico è stato inserito nella white** list del server SFTP. In caso contrario, consulta [questa sezione](../../sftp/using/ip-range-whitelisting.md) per ulteriori informazioni su come inserire in una whitelist l’intervallo IP.
* Hai accesso a un software **client** SFTP. È possibile consultare il reparto IT per l&#39;applicazione client SFTP che si consiglia di utilizzare, o cercare uno su Internet, se ciò è consentito dalle politiche aziendali.

Per connettersi al server SFTP, attenetevi alla procedura seguente:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]**tab from the**[!UICONTROL SFTP]** card.

   ![](assets/sftp_card.png)

1. Avviate l&#39;applicazione client SFTP, quindi copiate e incollate l&#39;indirizzo del server dal Pannello di controllo, seguito da &quot;campaign.adobe.com&quot;, quindi inserite il vostro nome utente.

   ![](assets/do-not-localize/connect1.png)

1. Nel **[!UICONTROL SSH Private Key]**campo selezionare il file di chiave privata memorizzato nel computer. Corrisponde a un file di testo che ha lo stesso nome della chiave pubblica, senza l&#39;estensione &quot;.pub&quot; (ad esempio, &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   Il **[!UICONTROL Password]**campo viene compilato automaticamente con la chiave privata del file.

   ![](assets/do-not-localize/connect3.png)

   È possibile verificare che la chiave che si sta tentando di utilizzare sia salvata nel Pannello di controllo confrontando l&#39;impronta digitale della chiave privata o pubblica con l&#39;impronta digitale delle chiavi visualizzate nella scheda Gestione chiavi della scheda SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se si utilizza un computer Mac, è possibile visualizzare l&#39;impronta digitale della chiave privata memorizzata nel computer eseguendo questo comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Dopo aver compilato tutte le informazioni, fai clic **[!UICONTROL Connect]**per accedere al server SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
