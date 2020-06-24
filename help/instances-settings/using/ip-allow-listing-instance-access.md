---
title: Elenco di indirizzi IP consentiti
description: Scoprite come aggiungere indirizzi IP all'elenco di indirizzi consentiti nel Pannello di controllo, ad esempio l'accesso
translation-type: tm+mt
source-git-commit: d8fe1c2e847fa25919f81bf0a4195de5ad0b2781
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 49%

---


# Elenco di indirizzi IP consentiti {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Informazioni sull&#39;impostazione di autorizzazione IP"
>abstract="Aggiungete gli indirizzi IP all&#39;elenco Consenti per accedere alle vostre istanze."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Guarda il video dimostrativo"

>[!IMPORTANT]
>
>Questa funzione è disponibile solo per le istanze di Campaign Classic.

## Informazioni sull&#39;impostazione di autorizzazione IP {#about-ip-allow-listing}

Per impostazione predefinita, l’istanza di Adobe Campaign Classic non è accessibile da vari indirizzi IP.

Se il tuo indirizzo IP non è stato aggiunto all&#39;elenco di indirizzi consentiti, non potrai accedere all&#39;istanza da questo indirizzo. Allo stesso modo, potrebbe non essere possibile collegare un&#39;API al Centro messaggi o all&#39;istanza Marketing se l&#39;indirizzo IP non è stato aggiunto all&#39;elenco allow con l&#39;istanza esplicitamente.

Il Pannello di controllo consente di impostare nuove connessioni alle istanze aggiungendo intervalli di indirizzi IP all&#39;elenco di indirizzi consentiti. Per farlo, attieniti alla procedura descritta di seguito.

Una volta che gli indirizzi IP sono nell&#39;elenco di indirizzi consentiti, puoi creare e collegare gli operatori Campaign per consentire agli utenti di accedere all&#39;istanza.

## Best practice {#best-practices}

Quando aggiungete indirizzi IP all&#39;elenco di autorizzazioni del Pannello di controllo, accertatevi di rispettare le raccomandazioni e le limitazioni riportate di seguito.

* **Non abilitare l’accesso IP per tutti i tipi di accesso** se non vuoi che l’indirizzo IP si connetta ai tuoi server RT o all’area di sicurezza AEM.
* **Se avete temporaneamente attivato l&#39;accesso all&#39;istanza per un indirizzo** IP, accertatevi di rimuovere gli indirizzi IP dall&#39;elenco di autorizzazioni una volta che non è più necessario connettersi all&#39;istanza.
* **Non si consiglia di aggiungere indirizzi IP di luoghi pubblici alla lista** di autorizzazione (aeroporti, alberghi, ecc.). Utilizza l’indirizzo VPN dell’azienda per proteggere sempre la tua istanza.

## Aggiunta di indirizzi IP all&#39;elenco allow per l&#39;accesso a Instance {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Aggiungere un nuovo intervallo IP"
>abstract="Definire l&#39;intervallo IP che si desidera aggiungere all&#39;elenco di autorizzazioni per collegarsi all&#39;istanza."

Per aggiungere indirizzi IP all&#39;elenco di indirizzi consentiti, procedere come segue:

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Se la scheda Instance Settings (Impostazioni istanze) non è visibile nella home page del Pannello di controllo Campaign, significa che il tuo ID organizzazione IMS non è associato ad alcuna istanza di Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Compilate le informazioni per l&#39;intervallo IP che desiderate aggiungere all&#39;elenco di autorizzazioni come descritto di seguito.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: le istanze a cui gli indirizzi IP saranno in grado di connettersi. È possibile operare su più istanze contemporaneamente. Ad esempio, l&#39;opzione IP consente l&#39;elencazione sia nelle istanze Produzione che Stage attraverso lo stesso passaggio.
   * **[!UICONTROL IP Range]**: L&#39;intervallo IP che si desidera aggiungere all&#39;elenco di valori consentiti, in formato CIDR. Un intervallo IP non può sovrapporsi a un intervallo esistente nell&#39;elenco allow. In tal caso, elimina prima l’intervallo che contiene l’IP sovrapposto.
   >[!NOTE]
   >
   >CIDR (Classless Inter-Domain Routing) è il formato supportato per l’aggiunta di intervalli IP tramite l’interfaccia del Pannello di controllo Campaign. La sintassi è composta da un indirizzo IP seguito da un carattere “/” e da un numero decimale. Il formato e la sintassi sono descritti dettagliatamente in [questo articolo](https://whatismyipaddress.com/cidr).
   >
   >Puoi cercare su Internet strumenti online gratuiti che ti aiuteranno a convertire gli intervalli IP che hai a disposizione in formato CIDR.

   * **[!UICONTROL Label]**: Etichetta che verrà visualizzata nell&#39;elenco Consenti.
   * **[!UICONTROL Name]**: il nome deve essere univoco per Access Type (Tipo di accesso), Instance (Istanza) (in caso di connessione API esterna) e per l’indirizzo IP.


1. Specifica il tipo di accesso che desideri concedere agli indirizzi IP:

   * **[!UICONTROL Campaign Console Access]**: gli indirizzi IP saranno autorizzati a connettersi alla console Campaign Classic. L’accesso alla console è abilitato solo per le istanze Marketing. L’accesso all’istanza MID e RT non è consentito e pertanto non è abilitato.
   * **[!UICONTROL AEM connection]**: gli indirizzi IP AEM specificati saranno autorizzati a connettersi all’istanza Marketing.
   * **[!UICONTROL External API connection]**: le API esterne con gli indirizzi IP specificati saranno autorizzate a connettersi all’istanza Marketing e/o Message Center (Centro messaggi) (RT). La connessione delle istanze RT alla console non è abilitata.
   ![](assets/ip_whitelist_acesstype.png)

1. Fai clic sul pulsante **[!UICONTROL Save]**. L&#39;intervallo IP viene aggiunto all&#39;elenco allow.

   ![](assets/ip_whitelist_added.png)

Per eliminare gli intervalli IP dall&#39;elenco Consenti, selezionateli e fate clic sul **[!UICONTROL Delete IP range]** pulsante .

**Argomenti correlati:**
* [Elenco di indirizzi IP consentiti (video di esercitazione)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [Collegamento di un’area di sicurezza a un operatore](https://docs.adobe.com/content/help/it-IT/campaign-classic/using/installing-campaign-classic/additional-configurations/configuring-campaign-server.html#Linking_a_security_zone_to_an_operator)
