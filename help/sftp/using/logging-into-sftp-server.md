---
product: campaign
solution: Campaign
title: Accesso al server SFTP
description: Scopri come accedere al server SFTP
translation-type: tm+mt
source-git-commit: 54d3239a566491c854e5d46c297e72afeff83792
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---


# Accesso al server SFTP {#logging-into-sft-server}

Nei passaggi seguenti viene descritto come collegare il server SFTP tramite l&#39;applicazione client SFTP.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](https://video.tv.adobe.com/v/27263?quality=12&captions=ita)

Prima di accedere al server, accertatevi che:

* Il server SFTP è **ospitato da  Adobe**.
* Il tuo **nome utente** è stato configurato per il server. Puoi controllare queste informazioni direttamente nel Pannello di controllo Campaign, nella scheda **Gestione chiavi** dalla scheda SFTP.
* Hai una **coppia di chiavi pubblica e privata** per accedere al server SFTP. Per ulteriori informazioni sull&#39;aggiunta della chiave SSH, fare riferimento a [questa sezione](../../sftp/using/key-management.md).
* Il tuo **indirizzo IP pubblico è stato aggiunto al elenco consentiti** sul server SFTP. In caso contrario, consultare [questa sezione](../../sftp/using/ip-range-allow-listing.md) per ulteriori informazioni su come aggiungere l&#39;intervallo IP al elenco consentiti .
* Hai accesso a un **software client SFTP**. È possibile consultare il reparto IT per l&#39;applicazione client SFTP che si consiglia di utilizzare, o cercare uno su Internet, se ciò è consentito dalle politiche aziendali.

Per connettersi al server SFTP, attenetevi alla procedura seguente:

1. Avviate l&#39;Pannello di controllo Campaign, quindi selezionate la scheda **[!UICONTROL Key Management]** dalla scheda **[!UICONTROL SFTP]**.

   ![](assets/sftp_card.png)

1. Avviate l&#39;applicazione client SFTP, quindi copiate e incollate l&#39;indirizzo del server dal Pannello di controllo Campaign, seguito da &quot;campaign.adobe.com&quot;, quindi inserite il vostro nome utente.

   ![](assets/do-not-localize/connect1.png)

1. Nel campo **[!UICONTROL SSH Private Key]**, selezionare il file di chiave privata memorizzato nel computer. Corrisponde a un file di testo che ha lo stesso nome della chiave pubblica, senza l&#39;estensione &quot;.pub&quot; (ad esempio, &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   Il campo **[!UICONTROL Password]** viene compilato automaticamente con la chiave privata del file.

   ![](assets/do-not-localize/connect3.png)

   È possibile verificare che la chiave che si sta tentando di utilizzare sia salvata nel Pannello di controllo Campaign confrontando l&#39;impronta digitale della chiave privata o pubblica con l&#39;impronta digitale delle chiavi visualizzate nella scheda Gestione chiavi della scheda SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se si utilizza un computer Mac, è possibile visualizzare l&#39;impronta digitale della chiave privata memorizzata nel computer eseguendo questo comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una volta compilate tutte le informazioni, fate clic su **[!UICONTROL Connect]** per accedere al server SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
