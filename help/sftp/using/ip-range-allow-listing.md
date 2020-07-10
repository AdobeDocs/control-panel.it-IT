---
title: Intervallo IP per l'inserimento
description: Scopri come aggiungere intervalli IP al elenco consentiti  per l'accesso ai server SFTP
translation-type: tm+mt
source-git-commit: d96c044e83d37f020b5fd6ea55199c1223b9fa39
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 40%

---


# Intervallo IP per l&#39;inserimento {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Informazioni sull&#39;impostazione di autorizzazione IP"
>abstract="In questa scheda, puoi aggiungere intervalli IP al elenco consentiti , per stabilire una connessione ai server SFTP. Solo i server SFTP a cui hai accesso sono visualizzati qui. Contatta l’amministratore per richiedere l’accesso ad altri server SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Guarda il video dimostrativo"

I server SFTP sono protetti. Per potervi accedere per visualizzare i file o scriverne di nuovi, è necessario aggiungere l&#39;indirizzo IP pubblico del sistema o del client che accede ai server al elenco consentiti .

## Informazioni sul formato CIDR {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) è il formato supportato per l’aggiunta di intervalli IP tramite l’interfaccia del Pannello di controllo Campaign.

La sintassi è composta da un indirizzo IP seguito da un carattere “/” e da un numero decimale. Il formato e la sintassi sono descritti dettagliatamente in [questo articolo](https://whatismyipaddress.com/cidr).

Puoi cercare su Internet strumenti online gratuiti che ti aiuteranno a convertire gli intervalli IP che hai a disposizione in formato CIDR.

## Best practice {#best-practices}

Quando aggiungete indirizzi IP al elenco consentiti  nel Pannello di controllo, accertatevi di rispettare le raccomandazioni e i limiti indicati di seguito.

* **Aggiungete intervalli IP al elenco consentiti**  anziché a indirizzi IP singoli. Per aggiungere un singolo indirizzo IP al elenco consentiti , aggiungete un &#39;/32&#39; per indicare che l&#39;intervallo include solo un IP.
* **Non aggiungete intervalli molto ampi al elenco consentiti**, ad esempio includendo > 265 indirizzi IP. Il Pannello di controllo Campaign rifiuterà qualsiasi intervallo in formato CIDR compreso tra /0 e /23.
* Solo gli indirizzi **IP** pubblici possono essere aggiunti al elenco consentiti .
* Assicuratevi di eliminare **regolarmente gli indirizzi** IP di cui non avete più bisogno dal elenco consentiti .

## Aggiunta di indirizzi IP al elenco consentiti  {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Aggiungere un nuovo intervallo IP"
>abstract="Definite gli intervalli IP che desiderate aggiungere al elenco consentiti  per la connessione ai server SFTP."

Per aggiungere un intervallo IP al elenco consentiti , procedere come segue:

1. Apri la scheda **[!UICONTROL SFTP]**, quindi seleziona la scheda **[!UICONTROL IP Allow Listing]**.
1. L&#39;elenco degli indirizzi IP nel elenco consentiti  viene visualizzato per ogni istanza. Seleziona l’istanza desiderata dall’elenco a sinistra, quindi fai clic sul pulsante **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Definite l&#39;intervallo IP che desiderate aggiungere al elenco consentiti , in formato CIDR, quindi definite l&#39;etichetta che verrà visualizzata nell&#39;elenco.

   >[!NOTE]
   >
   >I seguenti caratteri speciali sono consentiti nel campo Etichetta:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Un intervallo IP non può sovrapporsi a un intervallo esistente sul elenco consentiti . In tal caso, elimina prima l’intervallo che contiene l’IP sovrapposto.
   >
   >È possibile aggiungere un intervallo nel elenco consentiti  per più istanze. A questo scopo, premi il tasto freccia giù o digita le prime lettere dell’istanza desiderata, quindi selezionala dall’elenco dei suggerimenti.

   ![](assets/control_panel_add_range3.png)

1. Fai clic sul pulsante **[!UICONTROL Save]**. L&#39;aggiunta IP al elenco consentiti  viene visualizzata come IN SOSPESO fino a quando la richiesta non viene completamente elaborata. Questo dovrebbe richiedere solo qualche secondo.

Per eliminare gli intervalli IP dal elenco consentiti , selezionateli e fate clic sul **[!UICONTROL Delete IP range]** pulsante .

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Al momento non è possibile modificare un intervallo nel elenco consentiti . Per modificare un intervallo IP, eliminalo, quindi creane uno corrispondente alle tue esigenze.

## Monitoraggio delle modifiche {#monitoring-changes}

The **[!UICONTROL Job Logs]** in the Control Panel home page let you monitor all changes that have been made to IP addresses on the allow list.

Per ulteriori informazioni sull’interfaccia del Pannello di controllo Campaign, consulta [questa sezione](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
