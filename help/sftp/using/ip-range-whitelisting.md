---
title: Intervallo IP per l'inserimento
description: Scopri come aggiungere intervalli IP all'elenco di autorizzazioni per l'accesso ai server SFTP
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 40%

---


# Intervallo IP per l&#39;inserimento {#ip-range-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Informazioni sull&#39;impostazione di autorizzazione IP"
>abstract="In questa scheda, puoi aggiungere intervalli IP all&#39;elenco di autorizzazioni, per stabilire una connessione ai server SFTP. Solo i server SFTP a cui hai accesso sono visualizzati qui. Contatta l’amministratore per richiedere l’accesso ad altri server SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Guarda il video dimostrativo"

I server SFTP sono protetti. Per potervi accedere al fine di visualizzare i file o di scriverne di nuovi, è necessario aggiungere l&#39;indirizzo IP pubblico del sistema o del client che accede ai server all&#39;elenco di autorizzazioni.

## Informazioni sul formato CIDR {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) è il formato supportato per l’aggiunta di intervalli IP tramite l’interfaccia del Pannello di controllo Campaign.

La sintassi è composta da un indirizzo IP seguito da un carattere “/” e da un numero decimale. Il formato e la sintassi sono descritti dettagliatamente in [questo articolo](https://whatismyipaddress.com/cidr).

Puoi cercare su Internet strumenti online gratuiti che ti aiuteranno a convertire gli intervalli IP che hai a disposizione in formato CIDR.

## Best practice {#best-practices}

Quando aggiungete indirizzi IP all&#39;elenco di autorizzazioni del Pannello di controllo, accertatevi di rispettare le raccomandazioni e le limitazioni riportate di seguito.

* **Aggiungete intervalli IP all&#39;elenco** di indirizzi IP consentiti anziché a indirizzi IP singoli. Per aggiungere un singolo indirizzo IP all&#39;elenco di indirizzi consentiti, aggiungetegli un &#39;/32&#39; per indicare che l&#39;intervallo include solo un singolo IP.
* **Non aggiungete intervalli molto ampi all&#39;elenco** di autorizzazioni, ad esempio includendo > 265 indirizzi IP. Il Pannello di controllo Campaign rifiuterà qualsiasi intervallo in formato CIDR compreso tra /0 e /23.
* Solo gli indirizzi **IP** pubblici possono essere aggiunti all&#39;elenco allow.
* Accertatevi di eliminare **regolarmente indirizzi** IP non più necessari dall&#39;elenco di indirizzi consentiti.

## Aggiunta di indirizzi IP all&#39;elenco di indirizzi consentiti {#whitelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Aggiungere un nuovo intervallo IP"
>abstract="Definire gli intervalli IP che si desidera aggiungere all&#39;elenco di autorizzazioni per connettersi ai server SFTP."

Per aggiungere un intervallo IP all&#39;elenco di autorizzazioni, procedere come segue:

1. Apri la scheda **[!UICONTROL SFTP]**, quindi seleziona la scheda **[!UICONTROL IP Whistelisting]**.
1. Per ogni istanza viene visualizzato l&#39;elenco degli indirizzi IP nell&#39;elenco allow. Seleziona l’istanza desiderata dall’elenco a sinistra, quindi fai clic sul pulsante **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Definire l&#39;intervallo IP che si desidera aggiungere all&#39;elenco di valori consentiti, in formato CIDR, quindi definire l&#39;etichetta che verrà visualizzata nell&#39;elenco.

   >[!NOTE]
   >
   >I seguenti caratteri speciali sono consentiti nel campo Etichetta:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Un intervallo IP non può sovrapporsi a un intervallo esistente nell&#39;elenco allow. In tal caso, elimina prima l’intervallo che contiene l’IP sovrapposto.
   >
   >È possibile aggiungere un intervallo nell&#39;elenco allow per più istanze. A questo scopo, premi il tasto freccia giù o digita le prime lettere dell’istanza desiderata, quindi selezionala dall’elenco dei suggerimenti.

   ![](assets/control_panel_add_range3.png)

1. Fai clic sul pulsante **[!UICONTROL Save]**. L&#39;aggiunta IP all&#39;elenco di autorizzazioni verrà visualizzata come IN SOSPESO fino a quando la richiesta non sarà stata completamente elaborata. Questo dovrebbe richiedere solo qualche secondo.

Per eliminare gli intervalli IP dall&#39;elenco Consenti, selezionateli e fate clic sul **[!UICONTROL Delete IP range]** pulsante .

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Al momento non è possibile modificare un intervallo nell&#39;elenco allow. Per modificare un intervallo IP, eliminalo, quindi creane uno corrispondente alle tue esigenze.

## Monitoraggio delle modifiche {#monitoring-changes}

The **[!UICONTROL Job Logs]** in the Control Panel home page let you monitor all changes that have been made to IP addresses on the allow list.

Per ulteriori informazioni sull’interfaccia del Pannello di controllo Campaign, consulta [questa sezione](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
