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

I passaggi seguenti descrivono in dettaglio come connettere il server SFTP tramite l’applicazione client SFTP.

![](assets/do-not-localize/how-to-video.png)[ Scopri questa funzione nel video](https://video.tv.adobe.com/v/27263?quality=12)

Prima di effettuare l&#39;accesso al server, verificare che:

* Il server SFTP è **in hosting da Adobe**.
* Il tuo **nome utente** è stato configurato per il server. Puoi controllare queste informazioni direttamente nel Pannello di controllo Campaign, nel **Gestione delle chiavi** dalla scheda SFTP.
* Hai un **coppia di chiavi privata e pubblica** per accedere al server SFTP. Fai riferimento a [questa sezione](../../sftp/using/key-management.md) per ulteriori informazioni su come aggiungere la chiave SSH.
* Il tuo **l&#39;indirizzo IP pubblico è stato aggiunto all&#39;elenco consentiti** sul server SFTP. In caso contrario, fare riferimento a [questa sezione](../../sftp/using/ip-range-allow-listing.md) per ulteriori informazioni su come aggiungere l’intervallo IP all’elenco consentiti.
* Accesso a **Software client SFTP**. Puoi consultare il reparto IT per l’applicazione client SFTP che ti consiglia di utilizzare, oppure puoi cercarne una su Internet se consentito dalle politiche aziendali.

Per connettersi al server SFTP, segui questi passaggi:

1. Avvia il Pannello di controllo Campaign, quindi seleziona la **[!UICONTROL Key Management]** scheda da **[!UICONTROL SFTP]** Card.

   ![](assets/sftp_card.png)

1. Avvia l’applicazione client SFTP, quindi copia e incolla l’indirizzo del server dal Pannello di controllo Campaign, seguito da &quot;campaign.adobe.com&quot;, quindi inserisci il nome utente.

   ![](assets/do-not-localize/connect1.png)

1. In **[!UICONTROL SSH Private Key]** selezionare il file della chiave privata memorizzato nel computer. Corrisponde a un file di testo con lo stesso nome della chiave pubblica, senza estensione &quot;.pub&quot; (ad esempio, &quot;abilita&quot;).

   ![](assets/do-not-localize/connect2.png)

   Il **[!UICONTROL Password]** viene compilato automaticamente con la chiave privata del file.

   ![](assets/do-not-localize/connect3.png)

   Puoi verificare che la chiave che stai tentando di utilizzare sia salvata nel Pannello di controllo Campaign confrontando l’impronta digitale della chiave privata o pubblica con l’impronta digitale delle chiavi visualizzata nella scheda Key Management (Gestione chiavi) della scheda SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se si utilizza un computer Mac, è possibile visualizzare l&#39;impronta digitale della chiave privata memorizzata nel computer eseguendo il comando seguente:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una volta inserite tutte le informazioni, fai clic su **[!UICONTROL Connect]** per accedere al server SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
