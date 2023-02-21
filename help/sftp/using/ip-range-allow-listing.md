---
product: campaign
solution: Campaign
title: Inserimento di intervalli IP nell’elenco Consentiti
description: Scopri come aggiungere intervalli IP all’elenco Consentiti per accedere ai server SFTP
feature: Control Panel
role: Architect
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 38%

---

# Inserimento di intervalli IP nell’elenco Consentiti {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Informazioni sull’inserimento di IP nell’elenco Consentiti"
>abstract="In questa scheda puoi aggiungere intervalli IP all’elenco Consentiti per stabilire una connessione ai server SFTP. Solo i server SFTP a cui hai accesso sono visualizzati qui. Contatta l’amministratore per richiedere l’accesso ad altri server SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Guarda il video dimostrativo"

I server SFTP sono protetti. Per potervi accedere per visualizzare i file o scriverne di nuovi, devi aggiungere all’elenco consentiti l’indirizzo IP pubblico del sistema o del client che accede ai server.

![](assets/do-not-localize/how-to-video.png) Scopri questa funzione nel video per [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management)

## Informazioni sul formato CIDR {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) è il formato supportato per l’aggiunta di intervalli IP tramite l’interfaccia del Pannello di controllo Campaign.

La sintassi è composta da un indirizzo IP seguito da un carattere “/” e da un numero decimale. Il formato e la sintassi sono descritti dettagliatamente in [questo articolo](https://whatismyipaddress.com/cidr){target="_blank"}.

È possibile cercare su Internet strumenti online gratuiti che ti aiuteranno a convertire l&#39;intervallo IP in formato CIDR.

## Best practice {#best-practices}

Accertati di seguire le raccomandazioni e le limitazioni riportate di seguito quando inserisci gli indirizzi IP nell’elenco Consentiti dal Pannello di controllo Campaign.

* **Aggiungere intervalli IP all’elenco Consentiti** anziché indirizzi IP singoli. Per inserire un indirizzo IP singolo nell’elenco Consentiti, aggiungi “/32” per indicare che l’intervallo include un solo IP.
* **Non aggiungere intervalli eccessivamente ampi all’elenco Consentiti**, ad esempio intervalli che includono > 265 indirizzi IP. Il Pannello di controllo Campaign rifiuterà qualsiasi intervallo in formato CIDR compreso tra /0 e /23.
* Solo gli **indirizzi IP pubblici** possono essere aggiunti all’elenco Consentiti.
* Assicurati di **eliminare regolarmente gli indirizzi IP** che non ti serve più dall&#39;elenco consentiti.

## Aggiungere indirizzi IP all’elenco Consentiti {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Configurazione dell&#39;intervallo IP"
>abstract="Definisci gli intervalli IP che desideri aggiungere all’elenco Consentiti per la connessione ai server SFTP."

Per aggiungere un intervallo IP all’elenco Consentiti, esegui questi passaggi:

1. Apri la scheda **[!UICONTROL SFTP]**, quindi seleziona la scheda **[!UICONTROL IP Allow Listing]**.
1. L’elenco degli indirizzi IP inseriti nell’elenco Consentiti viene visualizzato per ogni istanza. Seleziona l’istanza desiderata dall’elenco a sinistra, quindi fai clic sul pulsante **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Definisci l’intervallo IP da aggiungere all’elenco consentiti. Questo campo accetta solo intervalli IP in formato CIDR, ad esempio *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >Un intervallo IP non può sovrapporsi a un intervallo esistente nell’elenco Consentiti. In tal caso, elimina prima l’intervallo che contiene l’IP sovrapposto.

1. È possibile aggiungere un intervallo all’elenco consentiti per più istanze. A questo scopo, premi il tasto freccia giù o digita le prime lettere dell’istanza desiderata, quindi selezionala dall’elenco dei suggerimenti.

   ![](assets/control_panel_add_range3.png)

1. Definisci l’etichetta da visualizzare per questo intervallo IP nell’elenco.

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >I seguenti caratteri speciali sono consentiti nella variabile **[!UICONTROL Label]** campo:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. Per gestire meglio il tuo elenco consentiti IP, puoi impostare una durata per la disponibilità di ogni intervallo IP. A questo scopo, seleziona un’unità nella **[!UICONTROL Type]** elenco a discesa e definire una durata nel campo corrispondente. Per ulteriori informazioni sulla scadenza dell’intervallo IP, consulta [questa sezione](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >Per impostazione predefinita, la **[!UICONTROL Type]** campo impostato su **[!UICONTROL Unlimited]**, il che significa che l’intervallo IP non scade mai.

1. In **[!UICONTROL Comment]** campo , puoi indicare un motivo per consentire questo intervallo IP (perché, per chi, ecc.).

1. Fai clic sul pulsante **[!UICONTROL Save]**. L’intervallo IP aggiunto all’elenco consentiti verrà visualizzato come **[!UICONTROL Pending]** fino a quando la richiesta non viene completamente elaborata, il che dovrebbe richiedere solo pochi secondi.

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>Se tenti di collegare i server SFTP a un nuovo sistema e quindi aggiungi nuovi intervalli IP all’elenco consentiti, potrebbe essere necessario immettere nuove chiavi pubbliche per completare la connessione. Per ulteriori informazioni, consulta [questa sezione](key-management.md).

## Gestione degli intervalli IP {#managing-ip-ranges}

Gli intervalli IP creati vengono visualizzati nel **[!UICONTROL IP Allow Listing]** scheda .

Puoi ordinare gli elementi in base alla data di creazione o di modifica, all’utente che lo ha creato o modificato e alla scadenza dell’intervallo IP.

Puoi anche eseguire la ricerca in un intervallo IP iniziando a digitare un’etichetta, un intervallo, un nome o un commento.

![](assets/control_panel_allow_list_sort.png)

Per modificare uno o più intervalli IP, vedi [questa sezione](#editing-ip-ranges).

Per eliminare uno o più intervalli IP dall’elenco consentiti, selezionali, quindi fai clic sul pulsante **[!UICONTROL Delete IP range]** pulsante .

![](assets/control_panel_delete_range.png)

### Scadenza {#expiry}

La **[!UICONTROL Expires]** mostra quanti giorni rimangono fino alla scadenza dell’intervallo IP.

Se hai effettuato la sottoscrizione a [avvisi e-mail](../../performance-monitoring/using/email-alerting.md), riceverai notifiche via e-mail 10 giorni e 5 giorni prima della scadenza di un intervallo IP e il giorno in cui scade. Dopo aver ricevuto l&#39;avviso, puoi [modifica dell’intervallo IP](#editing-ip-ranges) di prorogare, se necessario, il periodo di validità.

Un intervallo IP scaduto verrà eliminato automaticamente dopo 7 giorni. Viene visualizzato come **[!UICONTROL Expired]** in **[!UICONTROL Expires]** colonna. Entro questo periodo di 7 giorni:

* Non è più possibile utilizzare un intervallo IP scaduto per accedere ai server SFTP.

* Non puoi creare un altro intervallo IP che si sovrappone a un intervallo scaduto. Prima di creare il nuovo intervallo, devi prima eliminare l’intervallo IP scaduto.

* È possibile [modifica](#editing-ip-ranges) un intervallo IP scaduto e aggiornarne la durata per renderlo nuovamente disponibile.

* È possibile eliminarlo dall’elenco consentiti.

## Modifica di intervalli IP {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="Aggiorna intervalli IP"
>abstract="Aggiorna gli intervalli IP selezionati consentiti per la connessione al server SFTP."

Per modificare gli intervalli IP, effettua le seguenti operazioni.

>[!NOTE]
>
>Puoi modificare solo gli intervalli IP creati a partire dalla versione di ottobre 2021 del Pannello di controllo Campaign.

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. Seleziona uno o più intervalli IP dal **[!UICONTROL IP Allow Listing]** elenco.

1. Fai clic sul pulsante **[!UICONTROL Update IP range]**.

   ![](assets/control_panel_edit_range.png)

1. Puoi solo modificare la scadenza dell’intervallo IP e/o aggiungere un nuovo commento.

   >[!NOTE]
   >
   >Per modificare il formato CIDR, la relativa etichetta o le istanze correlate, devi prima eliminare l’intervallo IP e crearne uno nuovo corrispondente alle tue esigenze.

   ![](assets/control_panel_edit_range2.png)

1. Salva le modifiche.

## Monitoraggio delle modifiche {#monitoring-changes}

La **[!UICONTROL Job Logs]** nella home page del Pannello di controllo Campaign puoi monitorare e monitorare tutte le modifiche apportate agli indirizzi IP nell’elenco consentiti.

Per ulteriori informazioni sull’interfaccia del Pannello di controllo Campaign, consulta [questa sezione](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
