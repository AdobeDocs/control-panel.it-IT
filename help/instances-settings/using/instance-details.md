---
title: Dettagli istanza
description: Scoprite come monitorare i dettagli dell’istanza nel Pannello di controllo
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Dettagli istanza {#instance-details}

>[!CAUTION]
>
>Questa funzione è disponibile solo per le istanze di Campaign Classic.

## Informazioni sui dettagli dell’istanza {#about-instance-details}

L'architettura dell'istanza di Adobe Campaign Classic può contenere diversi server per abilitare la flessibilità delle attività di marketing. Ad esempio, i server Marketing, Real Time (o Message Center) e Mid Sourcing possono supportare l’istanza.

La funzionalità Instance Details (Dettagli istanza) consente di visualizzare l'architettura semplice dell'istanza. Oltre alle informazioni sul server, consente anche di sapere se la build dell'istanza è corrente o meno e consiglia gli aggiornamenti quando necessario.

>[!NOTE]
>
>È consigliabile aggiornare le istanze almeno una volta all'anno al fine di evitare il degrado delle prestazioni e poter sfruttare le funzionalità più recenti e le correzioni offerte da Adobe Campaign Classic.

**Argomenti correlati:**

* [Esecuzione di un aggiornamento build](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Aggiornamento di Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Recupero di informazioni sulle istanze {#retrieving-information-about-instances}

Per ottenere informazioni sui server connessi alle istanze, procedere come segue:

1. Open the **[!UICONTROL Instances Settings]** card to access the **[!UICONTROL Instance Details]** tab.

   >[!NOTE]
   >
   >Se la scheda Instance Settings (Impostazioni istanza) non è visibile nella home page del Pannello di controllo, significa che il tuo ID ORG IMS non è associato ad alcuna istanza di Adobe Campaign Classic

1. Selezionate nel riquadro a sinistra l'istanza Campaign Classic desiderata.

   >[!NOTE]
   >
   >Tutte le istanze Campaign vengono visualizzate nell'elenco del riquadro a sinistra. Poiché la funzione Instance Details (Dettagli istanza) è dedicata solo alle istanze Campaign Classic, se selezionate un'istanza Campaign Standard viene visualizzato il messaggio "Non applicabile".

1. Vengono visualizzati i server connessi all'istanza.

   ![](assets/instance_details.png)

Le informazioni disponibili sono:

* **[!UICONTROL Type]**: il tipo di server. I valori possibili sono MKT (Marketing), MID (Mid sourcing) e RT (Message Center / Messaggistica in tempo reale).
* **[!UICONTROL Name]**: il nome del server.
* **[!UICONTROL Build:]** la versione di build installata sul server.
* **[!UICONTROL Upgrade info]**: questa colonna indica se è necessario aggiornare il server.
   * Verde: il server è corrente, non è richiesto alcun aggiornamento.
   * Giallo: è consigliabile effettuare l'aggiornamento. Mancano le funzioni e le correzioni più recenti.
   * Rosso: eseguire l'aggiornamento il prima possibile. Mancano nuove funzioni e le prestazioni del server potrebbero non essere ottimali.

Se uno dei server richiede l'aggiornamento, consulta [questa documentazione](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) per ulteriori informazioni su come procedere.

## Domande frequenti {#common-questions}

**Non vedo il server MID nell'architettura della mia istanza, significa che le mie istanze non funzionano correttamente? Ho bisogno dell'istanza RT per una cosa che non posso fare oggi?**

La tua istanza può avere un aspetto molto diverso e potrebbe non avere tutti i tipi di server, o può avere diversi dello stesso server. Se non si dispone di un tipo di server o di un altro, non è possibile inviare un messaggio in tempo reale né eseguire altri tipi di attività. È possibile richiedere una capacità server aggiuntiva. Saranno applicati costi aggiuntivi.

Se ritenete che alcuni server non siano visualizzati nella pagina "Dettagli istanza", contattate l'Assistenza clienti. Ricorda l’URL specifico dell’istanza nel messaggio.
