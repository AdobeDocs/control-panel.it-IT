---
product: campaign
solution: Campaign
title: Identificare eventi e contatti chiave
description: Scopri come identificare gli eventi che si verificano sulle istanze e i contatti chiave in Adobe.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 5e2a5975a4a2ced4b23a18900309fc537daf13c0
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 43%

---

# Identificare eventi e contatti chiave {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendario dei servizi"
>abstract="Nella sezione dei contatti chiave sono elencate le persone in Adobe da contattare per eventuali richieste o problemi relativi alle istanze. Nella sezione Service Event Calendar (Calendario eventi dei servizi) è possibile identificare le versioni precedenti e future e gli avvisi per l’istanza selezionata, nonché impostare i promemoria per un dato evento."

>[!IMPORTANT]
>
>La funzionalità Service Calendar (Calendario dei servizi) è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

Per monitorare in modo efficace le istanze di Campaign, è fondamentale tenere traccia di eventi importanti che possono potenzialmente influire sulle istanze. Il Pannello di controllo Campaign consente di identificare eventi come nuove versioni, aggiornamenti, patch, hotfix e così via. e fornisce un elenco di contatti di Adobe chiave per eventuali richieste o problemi.

Queste informazioni sono accessibili da **[!UICONTROL Service Calendar]** sulla home page del Pannello di controllo Campaign.

## Contatti chiave {#key-contacts}

Nella sezione **[!UICONTROL Key contacts]** sono elencate le persone in Adobe che puoi contattare per eventuali richieste o problemi relativi alle tue istanze.

>[!NOTE]
>
>In questa sezione vengono visualizzate solo le informazioni relative agli account Managed Services.

![](assets/service-events-contacts.png)

I contatti chiave includono i seguenti ruoli:

* **[!UICONTROL TAM]**: Technical Account Manager,
* **[!UICONTROL CSM]**: Customer Success Manager,
* **[!UICONTROL Deliverability]**: punto di contatto per le operazioni di consegna,
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (solo per account Managed Services),
* **[!UICONTROL On-boarding Specialist]**: specialista assegnato all’account per aiutarti a iniziare con Campaign Classic (solo per account Managed Services).

## Tieni traccia degli eventi importanti {#events}

Il **[!UICONTROL Service Event Calendar]** Questa sezione mostra tutte le versioni precedenti e future, nonché gli avvisi per gli utenti abbonati agli avvisi e-mail del Pannello di controllo Campaign. Inoltre, il Pannello di controllo Campaign consente agli utenti di impostare promemoria e contrassegnare eventi rilevanti per l’istanza selezionata in modo da organizzarli meglio ed essere efficienti.

Gli eventi vengono visualizzati in un calendario o in un elenco. È possibile passare da una visualizzazione all&#39;altra utilizzando **[!UICONTROL Calendar]** e **[!UICONTROL List]** nell&#39;angolo superiore destro della sezione.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>Nella vista calendario, nell’angolo superiore destro sono disponibili pulsanti di navigazione per facilitare la navigazione tra gli eventi. Utilizza il <b>doppia freccia</b> per passare al primo evento presente dopo/prima del mese selezionato e al <b>frecce singole</b> per spostarsi da un mese all'altro. Fai clic su <b>pulsante cerchio</b> per tornare alla visione odierna.</td>
</tr></table>

Vengono visualizzati tre tipi di eventi:

* **Promemoria** sono impostate dagli utenti per essere notificate prima che si verifichi un evento. Questi sono visualizzati in verde nella vista calendario. [Scopri come impostare il promemoria](#reminders)
* **Avvisi** vengono inviati tramite e-mail dal Pannello di controllo Campaign per avvisare gli utenti dei problemi relativi alle loro istanze, come il sovraccarico di archiviazione o la scadenza del certificato SSL. Vengono visualizzate in arancione nella vista calendario. La descrizione dell’evento specifica se l’avviso viene inviato all’utente connesso, a seconda dell’abbonamento agli avvisi e-mail. [Ulteriori informazioni sulle funzionalità degli avvisi e-mail di Pannello di controllo Campaign](../performance-monitoring/using/email-alerting.md)

* **Versioni** indica sia le distribuzioni passate che quelle future nell’istanza, visualizzate rispettivamente in grigio e blu nella vista calendario. I dettagli dell’evento specificano il tipo di versione associata a ciascuna distribuzione:

   * **[!UICONTROL General availability]**: build stabile più recente disponibile.
   * **[!UICONTROL Limited availability]**: solo per implementazione su richiesta.
   * **[!UICONTROL Release candidate]**: convalidata dal team Engineering. In attesa di prove di produzione.
   * **[!UICONTROL Pre release]**: disponibilità anticipata per esigenze specifiche dei clienti.
   * **[!UICONTROL No longer available]**: la build non contiene problemi importanti ma ne è disponibile una nuova con ulteriori correzioni di bug. È necessario un aggiornamento.
   * **[!UICONTROL Deprecated]**: build con regressioni note. La build non è più supportata. È obbligatorio eseguire l’aggiornamento.

Puoi assegnare un flag a uno o più eventi in programma per tenerne traccia. A questo scopo, fai clic sul pulsante con i puntini di sospensione accanto al nome dell’evento.

![](assets/service-events-flag.png)

## Impostare i promemoria {#reminders}

Con Service Calendar (Calendario dei servizi), è possibile impostare i promemoria per ricevere le notifiche via e-mail prima che si verifichi un evento.

>[!NOTE]
>
>Per ricevere notifiche sui prossimi eventi, assicurati di aver richiesto la ricezione degli avvisi e-mail in Pannello di controllo. [Ulteriori informazioni](../performance-monitoring/using/email-alerting.md)

Per impostare un avviso per un evento, effettua le seguenti operazioni:

1. Passa il puntatore del mouse sull&#39;evento di cui vuoi cevere il promemoria oppure fai clic sul pulsante con i tre punti (...) nella vista a elenco e seleziona **[!UICONTROL Set Reminder]**.

1. Assegna un titolo al promemoria e seleziona la data in cui desideri ricevere la notifica prima che si verifichi l’evento.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Se non ti sei iscritto agli avvisi del Pannello di controllo, verrà visualizzato un messaggio che ti consentirà di registrarti per ricevere le notifiche e-mail.

1. Il promemoria è ora impostato per l’evento selezionato. Puoi passare il cursore sopra di esso in qualsiasi momento per visualizzarne il titolo.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >È possibile impostare fino a 2 promemoria per lo stesso evento.

1. Alla data specificata nel promemoria, verrà inviata un’e-mail per avvisarti dell’evento in arrivo e il promemoria verrà rimosso automaticamente dal conteggio **[!UICONTROL Reminders]** nel menu Service Calendar (Calendario dei servizi).
