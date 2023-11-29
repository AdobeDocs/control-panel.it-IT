---
product: campaign
solution: Campaign
title: Dettagli istanza
description: Scopri come monitorare i dettagli dell’istanza nel Pannello di controllo
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '536'
ht-degree: 100%

---

# Dettagli istanza {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Informazioni su Dettagli istanza"
>abstract="Visualizza i dettagli delle istanze di Adobe Campaign: tipi, nomi, informazioni sulla build e consigli su possibili aggiornamenti."

## Informazioni su Dettagli istanza {#about-instance-details}

>[!IMPORTANT]
>
>Questa funzione è disponibile solo per le istanze di Campaign v7/v8.

L’architettura dell’istanza di Adobe Campaign può contenere diversi server per consentire la flessibilità delle attività di marketing. Ad esempio, possono supportare l’istanza i server Marketing, Real Time (In tempo reale) (o Message Center [Centro messaggi]) e Mid Sourcing.

La funzionalità Instance Details (Dettagli istanza) consente di visualizzare l’architettura semplice dell’istanza. Oltre alle informazioni sul server, ti consente anche di sapere se la build dell’istanza è corrente o meno e consiglia gli aggiornamenti quando necessario.

>[!NOTE]
>
>È consigliabile aggiornare le istanze almeno una volta all’anno al fine di evitare il calo delle prestazioni e poter sfruttare le funzionalità più recenti e le correzioni offerte da Adobe Campaign v7/v8.

**Argomenti correlati:**

* [Esecuzione di un aggiornamento della build](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=it)
* [Aggiornamento di Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/introduction.html?lang=it)

## Recupero di informazioni sulle istanze {#retrieving-information-about-instances}

Per ottenere informazioni sui server connessi alle istanze, procedi come segue:

1. Apri la scheda **[!UICONTROL Impostazioni istanze]** per accedere alla scheda **[!UICONTROL Dettagli istanza]**.

   >[!NOTE]
   >
   >Se la scheda Impostazioni istanze non è visibile nella home page del Pannello di controllo, significa che il tuo ID organizzazione non è associato ad alcuna istanza di Adobe Campaign v7/v8

1. Seleziona nel riquadro a sinistra l’istanza di Campaign desiderata.

   >[!NOTE]
   >
   >Tutte le istanze di Campaign vengono visualizzate nell’elenco del riquadro a sinistra. Poiché la funzione Dettagli istanza è dedicata solo alle istanze di Campaign v7/v8, se selezioni un’istanza di Campaign Standard viene visualizzato il messaggio “Istanza non applicabile”.

1. Vengono visualizzati i server connessi all’istanza.

   ![](assets/instance_details.png)

Le informazioni disponibili sono:

* **[!UICONTROL Tipo]**: il tipo di server. I valori possibili sono MKT (Marketing), MID (Mid sourcing) e RT (Centro messaggi/Messaggistica in tempo reale).
* **[!UICONTROL Nome]**: il nome del server.
* **[!UICONTROL Build:]** la versione di build installata sul server.
* **[!UICONTROL Informazioni sull’aggiornamento]**: questa colonna indica se è necessario aggiornare il server.
   * Verde: il server è aggiornato, non è richiesto alcun aggiornamento.
   * Giallo: è consigliabile effettuare l’aggiornamento. Non disponi delle funzioni e delle correzioni più recenti.
   * Rosso: esegui l’aggiornamento il prima possibile. Non disponi di nuove funzioni e le prestazioni del server potrebbero non essere ottimali.

Se uno dei server richiede l’aggiornamento, consulta [questa documentazione](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=it) per ulteriori informazioni su come procedere.

## Domande comuni {#common-questions}

**Non visualizzo il server MID nell’architettura delle mie istanze, significa che le mie istanze non funzionano correttamente? È necessaria l’istanza RT per qualcosa che non posso fare attualmente?**

La tua istanza può avere un aspetto molto diverso e può non disporre di tutti i tipi di server, o può disporre di più server uguali. Se non disponi di un tipo di server o di un altro, non vuol dire che non puoi inviare un messaggio in tempo reale o eseguire altri tipi di attività. Puoi richiedere una capacità server aggiuntiva. Saranno applicati costi aggiuntivi.

Se ritieni che alcuni server non siano visualizzati nella pagina “Dettagli istanza”, contatta l’Assistenza clienti. Ricorda di indicare l’URL specifico dell’istanza nel messaggio.
