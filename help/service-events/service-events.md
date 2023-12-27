---
product: campaign
solution: Campaign
title: Identificare eventi e contatti chiave
description: Scopri come identificare gli eventi che si verificano sulle istanze e i contatti chiave in Adobe.
feature: Control Panel, Monitoring
role: Admin
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '781'
ht-degree: 100%

---

# Identificare eventi e contatti chiave {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendario dei servizi"
>abstract="Nella sezione dei contatti chiave sono elencate le persone in Adobe da contattare per eventuali richieste o problemi relativi alle istanze. Nella sezione Calendario eventi dei servizi trovi le versioni precedenti e prossime e gli avvisi per l’istanza selezionata e puoi impostare i promemoria per un dato evento."

>[!IMPORTANT]
>
>La funzionalità Calendario dei servizi è disponibile in versione beta e soggetta a frequenti aggiornamenti e modifiche senza preavviso.

Per monitorare in modo efficace le istanze di Campaign, è fondamentale tenere traccia di eventi importanti che possono potenzialmente influire sulle istanze. Il Pannello di controllo consente di identificare eventi come nuove versioni, aggiornamenti, patch, correzioni rapide e così via e fornisce un elenco di contatti Adobe chiave per eventuali richieste o problemi.

Queste informazioni sono accessibili dalla scheda **[!UICONTROL Calendario del servizio]** sulla pagina home del Pannello di controllo.

## Contatti chiave {#key-contacts}

Nella sezione **[!UICONTROL Contatti chiave]** sono elencate le persone in Adobe che puoi contattare per eventuali richieste o problemi relativi alle tue istanze.

>[!NOTE]
>
>In questa sezione vengono visualizzate informazioni solo per gli account Managed Services.

![](assets/service-events-contacts.png)

I contatti chiave includono i seguenti ruoli:

* **[!UICONTROL TAM]**: Technical Account Manager
* **[!UICONTROL CSM]**: Customer Success Manager
* **[!UICONTROL Deliverability]**: contatto per le operazioni di recapitabilità dei messaggi
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (solo per account Managed Services)
* **[!UICONTROL On-boarding Specialist]**: specialista assegnato all’account per aiutarti a iniziare con Campaign Classic (solo per account Managed Services)

## Tenere traccia degli eventi importanti {#events}

La sezione **[!UICONTROL Calendario eventi di servizio]** mostra tutte le versioni passate e future, nonché gli avvisi per gli utenti iscritti agli avvisi e-mail del Pannello di controllo. Inoltre, il Pannello di controllo consente agli utenti di impostare promemoria e contrassegnare eventi rilevanti per l’istanza selezionata per una migliore organizzazione e una maggiore efficienza.

Gli eventi vengono visualizzati in un calendario o in un elenco. È possibile passare da una visualizzazione all’altra utilizzando i pulsanti **[!UICONTROL Calendario]** e **[!UICONTROL Elenco]** in alto a destra in questa sezione.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>Nella vista calendario, nell’angolo superiore a destra sono disponibili pulsanti di navigazione per facilitare la navigazione tra gli eventi. Utilizza la <b>doppia freccia</b> per passare al primo evento presente dopo/prima del mese selezionato e le <b>frecce singole</b> per passare da un mese all’altro. Fai clic sul <b>pulsante a forma di cerchio</b> per tornare alla vista odierna.</td>
</tr></table>

Vengono visualizzati tre tipi di eventi:

* I **promemoria** vengono impostati dagli utenti per ricevere una notifica prima che si verifichi un evento. Questi sono visualizzati in verde nella vista calendario. [Scopri come impostare il promemoria](#reminders)
* Gli **avvisi** vengono inviati tramite e-mail dal Pannello di controllo per avvisare gli utenti dei problemi relativi alle loro istanze, come il sovraccarico di archiviazione o la scadenza del certificato SSL. Vengono visualizzati in arancione nella vista calendario. La descrizione dell’evento specifica se l’avviso viene inviato all’utente connesso, a seconda del tipo di iscrizione agli avvisi e-mail. [Ulteriori informazioni sulle funzionalità degli avvisi e-mail del Pannello di controllo](../performance-monitoring/using/email-alerting.md)

* Le **versioni** indicano sia le distribuzioni passate che quelle future nell’istanza, visualizzate rispettivamente in grigio e blu nella vista calendario. I dettagli dell’evento specificano il tipo di versione associata a ciascuna distribuzione:

   * **[!UICONTROL Disponibilità generale]**: ultima versione stabile disponibile.
   * **[!UICONTROL Disponibilità limitata]**: solo distribuzione su richiesta.
   * **[!UICONTROL Versione candidata]**: convalidata dal team Engineering. In attesa di prove di produzione.
   * **[!UICONTROL Pre-release]**: disponibilità anticipata per esigenze specifiche del cliente.
   * **[!UICONTROL Non più disponibile]**: la versione non contiene problemi importanti ma ne è disponibile una nuova con nuove correzioni di bug. È necessario un aggiornamento.
   * **[!UICONTROL Obsoleta]**: versione con regressioni note. La build non è più supportata. È obbligatorio eseguire l’aggiornamento.

Puoi assegnare un flag a uno o più eventi in programma per tenerne traccia. A questo scopo, fai clic sul pulsante con i puntini di sospensione accanto al nome dell’evento.

![](assets/service-events-flag.png)

## Impostare i promemoria {#reminders}

Con Service Calendar (Calendario dei servizi), è possibile impostare i promemoria per ricevere le notifiche via e-mail prima che si verifichi un evento.

>[!NOTE]
>
>Per ricevere notifiche sui prossimi eventi, assicurati di aver richiesto la ricezione degli avvisi e-mail in Pannello di controllo. [Ulteriori informazioni](../performance-monitoring/using/email-alerting.md)

Per impostare un avviso per un evento, effettua le seguenti operazioni:

1. Passa il puntatore del mouse sull’evento di cui vuoi ricevere il promemoria oppure fai clic sul pulsante con i puntini di sospensione nella visualizzazione a elenco e seleziona **[!UICONTROL Imposta promemoria]**.

1. Assegna un titolo al promemoria, quindi seleziona la data in cui desideri ricevere la notifica prima che si verifichi l’evento.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Se non ti sei iscritto agli avvisi del Pannello di controllo, verrà visualizzato un messaggio che ti consentirà di registrarti per ricevere le notifiche e-mail.

1. Il promemoria è ora impostato per l’evento selezionato. Puoi passare il cursore sopra di esso in qualsiasi momento per visualizzarne il titolo.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >È possibile impostare fino a 2 promemoria per lo stesso evento.

1. Alla data specificata nel promemoria, verrà inviata un’e-mail per avvisarti dell’evento imminente e il promemoria verrà rimosso automaticamente dall’elenco dei **[!UICONTROL Promemoria]** nel menu del Calendario del servizio.
