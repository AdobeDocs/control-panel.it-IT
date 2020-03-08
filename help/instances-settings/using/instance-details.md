---
title: Dettagli istanza
description: Scoprite come monitorare i dettagli dell’istanza nel Pannello di controllo
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Dettagli istanza {#instance-details}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;Informazioni sui dettagli dell’istanza&quot;
>abstract=&quot;Visualizza i dettagli delle istanze di Adobe Campaign: tipi, nomi, informazioni sulla build e possibili raccomandazioni di aggiornamento.&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Note sulla versione di Campaign Classic&quot;
>Additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Note sulla versione di Campaign Standard&quot;

>[!CAUTION]
>
>Questa funzione è disponibile solo per le istanze di Campaign Classic.

## Informazioni sui dettagli dell’istanza {#about-instance-details}

L&#39;architettura dell&#39;istanza di Adobe Campaign Classic può contenere diversi server per abilitare la flessibilità delle attività di marketing. Ad esempio, i server Marketing, Real Time (o Message Center) e Mid Sourcing possono supportare l’istanza.

La funzionalità Instance Details (Dettagli istanza) consente di visualizzare l&#39;architettura semplice dell&#39;istanza. Oltre alle informazioni sul server, consente anche di sapere se la build dell&#39;istanza è corrente o meno e consiglia gli aggiornamenti quando necessario.

>[!NOTE]
>
>È consigliabile aggiornare le istanze almeno una volta all&#39;anno al fine di evitare il degrado delle prestazioni e poter sfruttare le funzionalità più recenti e le correzioni offerte da Adobe Campaign Classic.

**Argomenti correlati:**

* [Esecuzione di un aggiornamento build](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Aggiornamento di Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Recupero di informazioni sulle istanze {#retrieving-information-about-instances}

Per ottenere informazioni sui server connessi alle istanze, procedere come segue:

1. Open the **[!UICONTROL Instances Settings]** card to access the **[!UICONTROL Instance Details]** tab.

   >[!NOTE]
   >
   >Se la scheda Instance Settings (Impostazioni istanza) non è visibile nella home page del Pannello di controllo, significa che il tuo ID ORG IMS non è associato ad alcuna istanza di Adobe Campaign Classic

1. Selezionate nel riquadro a sinistra l&#39;istanza Campaign Classic desiderata.

   >[!NOTE]
   >
   >Tutte le istanze Campaign vengono visualizzate nell&#39;elenco del riquadro a sinistra. Poiché la funzione Instance Details (Dettagli istanza) è dedicata solo alle istanze Campaign Classic, se selezionate un&#39;istanza Campaign Standard viene visualizzato il messaggio &quot;Non applicabile&quot;.

1. Vengono visualizzati i server connessi all&#39;istanza.

   ![](assets/instance_details.png)

Le informazioni disponibili sono:

* **[!UICONTROL Type]**: il tipo di server. I valori possibili sono MKT (Marketing), MID (Mid sourcing) e RT (Message Center / Messaggistica in tempo reale).
* **[!UICONTROL Name]**: il nome del server.
* **[!UICONTROL Build:]** la versione di build installata sul server.
* **[!UICONTROL Upgrade info]**: questa colonna indica se è necessario aggiornare il server.
   * Verde: il server è corrente, non è richiesto alcun aggiornamento.
   * Giallo: è consigliabile effettuare l&#39;aggiornamento. Mancano le funzioni e le correzioni più recenti.
   * Rosso: eseguire l&#39;aggiornamento il prima possibile. Mancano nuove funzioni e le prestazioni del server potrebbero non essere ottimali.

Se uno dei server richiede l&#39;aggiornamento, consulta [questa documentazione](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) per ulteriori informazioni su come procedere.

## Domande frequenti {#common-questions}

**Non vedo il server MID nell&#39;architettura della mia istanza, significa che le mie istanze non funzionano correttamente? Ho bisogno dell&#39;istanza RT per una cosa che non posso fare oggi?**

La tua istanza può avere un aspetto molto diverso e potrebbe non avere tutti i tipi di server, o può avere diversi dello stesso server. Se non si dispone di un tipo di server o di un altro, non è possibile inviare un messaggio in tempo reale né eseguire altri tipi di attività. È possibile richiedere una capacità server aggiuntiva. Saranno applicati costi aggiuntivi.

Se ritenete che alcuni server non siano visualizzati nella pagina &quot;Dettagli istanza&quot;, contattate l&#39;Assistenza clienti. Ricorda l’URL specifico dell’istanza nel messaggio.
