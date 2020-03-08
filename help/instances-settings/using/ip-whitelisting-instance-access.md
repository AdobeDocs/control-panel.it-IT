---
title: whitelist IP
description: Ulteriori informazioni sulla whitelist IP nel Pannello di controllo per l'accesso ad esempio
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# whitelist IP {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange&quot;
>title=&quot;Informazioni sulla whitelist IP&quot;
>abstract=&quot;Gestisci whitelist IP per accedere alle tue istanze.&quot;
>Additional-url=&quot;https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4&quot; text=&quot;Guarda il video dimostrativo&quot;

>[!CAUTION]
>
>Questa funzione è disponibile solo per le istanze di Campaign Classic.

## Informazioni sulla whitelist IP {#about-ip-whitelisting}

Per impostazione predefinita, l&#39;istanza di Adobe Campaign Classic non è accessibile da vari indirizzi IP.

Se l&#39;indirizzo IP non è stato inserito nella white list, non potrete accedere all&#39;istanza da questo indirizzo. Allo stesso modo, potrebbe non essere possibile collegare un&#39;API al Centro messaggi o all&#39;istanza Marketing se l&#39;indirizzo IP non è stato inserito in una whitelist con l&#39;istanza in modo esplicito.

Il Pannello di controllo consente di impostare nuove connessioni alle istanze tramite la whitelist degli intervalli di indirizzi IP. A questo scopo, attenetevi alla procedura descritta di seguito.

Una volta inseriti gli indirizzi IP nella white list, potete creare e collegare gli operatori Campaign per consentire agli utenti di accedere all&#39;istanza.

## Best practice {#best-practices}

Accertatevi di seguire le raccomandazioni e le limitazioni riportate di seguito quando inserite gli indirizzi IP nella white list del Pannello di controllo.

* **Non abilitate l&#39;accesso IP a tutti i tipi** di accesso se non intendete che l&#39;indirizzo IP si connetta ai server RT o all&#39;area di protezione AEM.
* **Se avete temporaneamente attivato l&#39;accesso all&#39;istanza per un indirizzo** IP, accertatevi di rimuovere gli indirizzi IP dagli indirizzi IP nella white list una volta che non è più necessario connettersi all&#39;istanza.
* **Non consigliamo di inserire in una whitelist gli indirizzi IP dei luoghi** pubblici (aeroporti, alberghi, ecc.). Utilizzate l&#39;indirizzo VPN della società per mantenere l&#39;istanza al sicuro in ogni momento.

## Whitelist di indirizzi IP per l&#39;accesso a Instance {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange_add&quot;
>title=&quot;Aggiungi nuovo intervallo Ip&quot;
>abstract=&quot;Definite l’intervallo IP da inserire nella whitelist per la connessione all’istanza.&quot;

Per inserire in una whitelist gli indirizzi IP, effettuate le seguenti operazioni:

1. Aprite la scheda **[!UICONTROL Instances Settings card]** per accedere alla whitelist IP, quindi fate clic su **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Se la scheda Instance Settings (Impostazioni istanza) non è visibile nella home page del Pannello di controllo, significa che il tuo ID ORG IMS non è associato ad alcuna istanza di Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Compila le informazioni per l’intervallo IP da inserire nella whitelist come descritto di seguito.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: Le istanze a cui gli indirizzi IP saranno in grado di connettersi. È possibile modificare più istanze contemporaneamente. Ad esempio, la whitelist IP può essere eseguita sia sulle istanze Produzione che Stage nello stesso passaggio.
   * **[!UICONTROL IP Range]**: La gamma IP che si desidera inserire nella whitelist, in formato CIDR. Tenete presente che un intervallo IP non può sovrapporsi a un intervallo esistente nella white list. In tal caso, eliminate prima l’intervallo che contiene l’IP sovrapposto.
   >[!NOTE]
   >
   >CIDR (Classless Inter-Domain Routing) è il formato supportato per l&#39;aggiunta di intervalli IP con l&#39;interfaccia del Pannello di controllo. La sintassi è composta da un indirizzo IP seguito da un carattere &quot;/&quot; e da un numero decimale. Il formato e la sintassi sono descritti dettagliatamente in [questo articolo](https://whatismyipaddress.com/cidr).
   >
   >È possibile ricercare su Internet strumenti online gratuiti che aiuteranno a convertire la gamma IP che si ha a portata di mano in formato CIDR.

   * **[!UICONTROL Label]**: Etichetta che verrà visualizzata nell&#39;elenco degli indirizzi IP consentiti.
   * **[!UICONTROL Name]**: Il nome deve essere univoco per Tipo di accesso, Istanza (in caso di connessione API esterna) e per l&#39;indirizzo IP.


1. Specificate il tipo di accesso che desiderate concedere agli indirizzi IP:

   * **[!UICONTROL Campaign Console Access]**: Gli indirizzi IP saranno autorizzati a connettersi alla console Campaign Classic. L&#39;accesso alla console è abilitato solo per le istanze di Marketing. L&#39;accesso all&#39;istanza MID e RT non è consentito e pertanto non è abilitato.
   * **[!UICONTROL AEM connection]**: Gli indirizzi IP AEM specificati saranno autorizzati a connettersi all&#39;istanza Marketing.
   * **[!UICONTROL External API connection]**: Le API esterne con gli indirizzi IP specificati saranno autorizzate a connettersi all&#39;istanza Marketing and/o Message Center (RT). Tenere presente che la connessione alla console delle istanze RT non è abilitata.
   ![](assets/ip_whitelist_acesstype.png)

1. Fate clic sul **[!UICONTROL Save]** pulsante. L&#39;intervallo IP viene aggiunto all&#39;elenco degli indirizzi IP consentiti.

   ![](assets/ip_whitelist_added.png)

Per eliminare gli intervalli IP consentiti, selezionateli e fate clic sul **[!UICONTROL Delete IP range]** pulsante .

**Argomenti correlati:**
* [whitelist IP (video di esercitazione)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [Collegamento di una zona di protezione a un operatore](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
