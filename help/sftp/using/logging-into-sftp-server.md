---
product: campaign
solution: Campaign
title: Accesso al server SFTP
description: Scopri come accedere al server SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
TQID: 'https://experienceleague.adobe.com/m02LjIAF8WJEB3TTSerLtktGejxwoDFu7HfGUpYsYok'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e8445399-14db-4931-a0bb-477780230387
    internal-label: SFTP Management
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 100%
---
# Accesso al server SFTP {#logging-into-sft-server}

I passaggi seguenti descrivono in dettaglio come connettere il server SFTP tramite l’applicazione client SFTP.

![](assets/do-not-localize/how-to-video.png) Guarda il [video su questa funzione](https://video.tv.adobe.com/v/27263?quality=12)

Prima di effettuare l’accesso al server, assicurati che i seguenti requisiti siano rispettati:

* Il server SFTP è **ospitato da Adobe**
* Il tuo **nome utente** è stato configurato per il server. Puoi controllare queste informazioni direttamente nel Pannello di controllo, nella scheda **Gestione delle chiavi** disponibile dalla scheda SFTP.
* Disponi di un **coppia di chiavi privata e pubblica** per accedere al server SFTP. Per informazioni su come aggiungere la chiave SSH, consulta [questa sezione](../../sftp/using/key-management.md).
* Il tuo **indirizzo IP pubblico è stato aggiunto all’elenco Consentiti** sul server SFTP. In caso contrario, consulta [questa sezione](../../sftp/using/ip-range-allow-listing.md) per informazioni su come aggiungere l’intervallo IP all’elenco Consentiti.
* Hai accesso a un **software client SFTP**. Rivolgiti al reparto IT della tua organizzazione per sapere quale applicazione client SFTP consigliano di utilizzare; oppure puoi cercarne una su Internet, se questo è consentito dalle politiche della tua azienda.

Per connetterti al server SFTP, segui questi passaggi:

1. Avvia il Pannello di controllo, quindi seleziona la scheda **[!UICONTROL Gestione delle chiavi]** disponibile dalla scheda **[!UICONTROL SFTP]**.

   ![](assets/sftp_card.png)

1. Avvia l’applicazione client SFTP, quindi copia e incolla l’indirizzo del server dal Pannello di controllo, seguito da “campaign.adobe.com”, quindi inserisci il nome utente.

   ![](assets/do-not-localize/connect1.png)

1. Nel campo **[!UICONTROL Chiave privata SSH]** seleziona il file della chiave privata memorizzato nel computer. Questo corrisponde a un file di testo con lo stesso nome della chiave pubblica, senza l’estensione “.pub” (ad esempio, “enable”).

   ![](assets/do-not-localize/connect2.png)

   Nel campo **[!UICONTROL Password]** viene automaticamente inserita la chiave privata fornita dal file.

   ![](assets/do-not-localize/connect3.png)

   Per verificare che la chiave che stai tentando di utilizzare sia salvata nel Pannello di controllo, confronta l’impronta digitale della chiave privata o pubblica con l’impronta digitale delle chiavi visualizzata nella scheda Gestione delle chiavi, nella scheda SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se utilizzi un computer Mac, puoi visualizzare l’impronta digitale della chiave privata memorizzata nel computer eseguendo il comando seguente:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una volta inserite tutte le informazioni, fai clic su **[!UICONTROL Connetti]** per accedere al server SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
