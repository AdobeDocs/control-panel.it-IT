---
product: campaign
solution: Campaign
title: Autorizzazioni URL
description: Scopri come gestire le autorizzazioni URL nel Pannello di controllo Campaign
feature: Control Panel
role: Architect
level: Intermediate
exl-id: a7df90da-a2ce-409f-9bc3-c7d4fa3024c8
source-git-commit: c834ae7226ed9dd1f78d4f4511b52cb5f04abfae
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 86%

---

# Autorizzazioni URL {#url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_urlpermissions"
>title="Informazioni sulle autorizzazioni URL"
>abstract="Gestisci gli URL a cui le istanze di Adobe Campaign possono connettersi."
>additional-url="https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4" text="Guarda il video dimostrativo"

## Informazioni sulle autorizzazioni URL {#about-url-permissions}

>[!IMPORTANT]
>
>Questa funzione è disponibile solo per le istanze Campaign v7/v8, dalla build 8850. Se utilizzi una build precedente, dovrai eseguire l’aggiornamento per utilizzare questa funzione.

L’elenco predefinito di URL che possono essere richiamati tramite codici JavaScript (flussi di lavoro, ecc.) dalle istanze Campaign è limitato. Si tratta di URL che consentono il corretto funzionamento delle istanze.

Per impostazione predefinita, le istanze non possono connettersi a URL esterni. Il Pannello di controllo Campaign consente di aggiungere degli URL esterni all’elenco degli URL autorizzati, in modo che l’istanza possa connettersi a tali URL. Questo consente di connettere le istanze Campaign a sistemi esterni, ad esempio server SFTP o siti Web, per abilitare il trasferimento di file e/o dati.

Una volta aggiunto l’URL, viene inserito un suo riferimento nel file di configurazione dell’istanza (serverConf.xml).

![](assets/do-not-localize/how-to-video.png) [Scopri questa funzione nel video](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/adding-url-permissions.html#instance-settings)

**Argomenti correlati:**

* [Configurazione del server Campaign](https://docs.adobe.com/content/help/it-IT/campaign-classic/using/installing-campaign-classic/additional-configurations/configuring-campaign-server.html)
* [Protezione delle connessioni in uscita](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/security-privacy/server-configuration.html#outgoing-connection-protection)

## Best practice {#best-practices}

* Non collegare l’istanza Campaign a siti web/server ai quali non intendi connetterti.
* Elimina gli URL con i quali non lavori più. Tuttavia, tieni presente che, se un’altra sezione della tua azienda continua a collegarsi all’URL eliminato, nessuno potrà più utilizzarlo.
* Il Pannello di controllo Campaign supporta protocolli **http**, **https** e **sftp**. L’immissione di URL o protocolli non validi causa errori.

## Gestione delle autorizzazioni URL {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_url_add"
>title="Definizione URL"
>abstract="Aggiungi URL per consentire connessioni all’istanza Campaign."

Per aggiungere un URL a cui l’istanza può connettersi, effettua le seguenti operazioni:

1. Apri la scheda **[!UICONTROL Instances Settings]** (Impostazioni istanze) per accedere alla scheda **[!UICONTROL URL Permissions]** (Dettagli istanza).

   >[!NOTE]
   >
   >Se la scheda Instance Settings (Impostazioni istanze) non è visibile nella home page del Pannello di controllo Campaign, significa che [ID organizzazione](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=it) non è associato ad alcuna istanza di Adobe Campaign
   >
   >La scheda <b><span class="uicontrol">URL permissions (Autorizzazioni URL)</span></b> elenca tutti gli URL esterni a cui l’istanza può connettersi. Questo elenco non include gli URL necessari per il funzionamento di Campaign (ad esempio, le connessioni tra parti dell’infrastruttura).

1. Seleziona nel riquadro di sinistra l’istanza desiderata, quindi fai clic sul pulsante **[!UICONTROL Add new URL]**.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Tutte le istanze Campaign vengono visualizzate nell’elenco del riquadro a sinistra.
   >
   >Poiché la gestione delle autorizzazioni URL è dedicata solo alle istanze Campaign v7/v8, se selezioni un’istanza di Campaign Standard viene visualizzato il messaggio &quot;Non-Applicable Instance&quot; (&quot;Istanza non applicabile&quot;).

1. Digita l’URL da autorizzare, con il relativo protocollo associato (http, https o sftp).

   >[!NOTE]
   >
   >È possibile autorizzare più istanze a connettersi all’URL. Per farlo, aggiungile direttamente dal campo Instance(s) (Istanza) digitando la prima lettera.

   ![](assets/add_url2.png)

1. L’URL viene aggiunto all’elenco, ora è possibile connettersi ad esso.

   >[!NOTE]
   >
   >I caratteri &quot;/.*&quot; vengono aggiunti automaticamente alla fine dell’URL immesso dopo la convalida, in modo da includere tutte le sottopagine della pagina immessa.

   ![](assets/add_url_listnew.png)

Puoi eliminare un URL in qualsiasi momento selezionandolo e facendo clic sul pulsante **[!UICONTROL Delete URL]**.

Tieni presente che, se elimini un URL, l’istanza non sarà più in grado di richiamarlo.

## Domande comuni {#common-questions}

**Ho aggiunto un nuovo URL, ma la mia istanza non è ancora in grado di connettersi a esso. Perché?**

In alcuni casi, gli URL a cui tenti di connetterti richiedono l’inserimento nell’elenco Consentiti, l’accesso tramite password o un altro tipo di autenticazione. Il Pannello di controllo Campaign non gestisce l’autenticazione aggiuntiva.
