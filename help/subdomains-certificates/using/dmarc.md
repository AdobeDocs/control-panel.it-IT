---
product: campaign
solution: Campaign
title: Aggiungere record DMARC
description: Scopri come aggiungere un record DMARC per un sottodominio.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: ht
source-wordcount: '714'
ht-degree: 100%

---

# Aggiungere record DMARC {#dmarc}

## Informazioni sui record DMARC {#about}

DMARC (Domain Based Message Authentication, Reporting and Conformance) è uno standard del protocollo di autenticazione e-mail che aiuta le organizzazioni a proteggere i domini e-mail dagli attacchi di phishing e spoofing. Consente di decidere in che modo un provider di cassette postali deve gestire le e-mail che non superano i controlli SPF e DKIM, fornendo un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi.

Informazioni dettagliate sull’implementazione di DMARC sono disponibili nella  [Guida alle best practice per la recapitabilità di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=it)

## Limitazioni e prerequisiti {#limitations}

* I record SPF e DKIM sono prerequisiti per la creazione di un record DMARC.
* I record DMARC possono essere aggiunti solo per i sottodomini che utilizzano la delega completa dei sottodomini. [Ulteriori informazioni sui metodi di configurazione dei sottodomini](subdomains-branding.md#subdomain-delegation-methods)

## Aggiungere un record DMARC per un sottodominio {#add}

Per aggiungere un record DMARC per un sottodominio, segui questi passaggi:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Subdomain details]**.

1. Fai clic sul pulsante **[!UICONTROL Add TXT record]**, quindi scegli **[!UICONTROL DMARC]** dall’elenco a discesa **[!UICONTROL Record Type]**.

   ![](assets/dmarc-add.png)

1. Scegli il **[!UICONTROL Policy Type]** che il server del destinatario deve seguire quando una delle e-mail non riesce. I tipi di criteri disponibili sono:

   * **[!UICONTROL None]**,
   * **[!UICONTROL Quarantine]** (posizionamento cartelle di posta indesiderata),
   * **[!UICONTROL Reject]** (blocco dell’e-mail).

   Come best practice, si consiglia di distribuire lentamente l’implementazione di DMARC aumentando il livello dei criteri DMARC da c=nessuno a c=quarantena, fino a c=rifiuta man mano che acquisisci una comprensione di DMARC e del suo potenziale impatto.

   * **Passaggio 1:** analizza il feedback ricevuto e utilizza (c=nessuno), che indica al destinatario di non eseguire azioni sui messaggi che non superano l’autenticazione, ma che inviano comunque i rapporti e-mail al mittente. Inoltre, se l’autenticazione dei messaggi legittimi non riesce, esamina e risolvi i problemi relativi a SPF/DKIM.

   * **Passaggio 2:** determina se SPF e DKIM sono allineati e trasmettono l’autenticazione per tutte le e-mail legittime, quindi sposta il criterio su (c=quarantena), che indica al server e-mail ricevente di mettere in quarantena le e-mail che non riescono a eseguire l’autenticazione (in genere significa inserire tali messaggi nella cartella di posta indesiderata). Se il criterio è impostato per la quarantena, si consiglia di iniziare con una piccola percentuale di e-mail.

   * **Passaggio 3:** imposta il criterio su (c=rifiuta). NOTA: utilizza questo criterio con cautela e determina se è appropriato per la tua organizzazione. Il criterio c= rifiuta indica al destinatario di rifiutare completamente (non recapitare) qualsiasi e-mail per il dominio che non supera l’autenticazione. Con questo criterio abilitato, solo i messaggi e-mail verificati come autenticati al 100% dal dominio avranno anche la possibilità di inserire la casella in entrata.

   >[!NOTE]
   >
   > La creazione di record BIMI non è disponibile con un tipo di criterio di record DMARC impostato su “Nessuno”.

1. Inserisci gli indirizzi e-mail che devono ricevere i rapporti DMARC. Quando una delle e-mail non riesce, i rapporti DMARC vengono inviati automaticamente all’indirizzo e-mail scelto:

   * I rapporti Aggregate-DMARC forniscono informazioni di alto livello come, ad esempio, il numero di e-mail non riuscite per un determinato periodo.
   * I rapporti forensi sugli errori DMARC forniscono informazioni dettagliate, ad esempio l’indirizzo IP da cui proviene l’e-mail non riuscita.

1. Se il criterio DMARC è impostato su “Nessuno”, immetti una percentuale valida per il 100% delle e-mail.

   Se il criterio è impostato su “Rifiuta” o “Quarantena”, si consiglia di iniziare con una piccola percentuale di e-mail. Man mano che più e-mail dal dominio passano l’autenticazione con i server riceventi, aggiorna il record lentamente con una percentuale più alta.

   >[!NOTE]
   >
   >Se il dominio utilizza BIMI, il criterio DMARC deve avere un valore percentuale del 100%. BIMI non supporta i criteri DMARC con questo valore impostato su una percentuale inferiore al 100%.

   ![](assets/dmarc-add2.png)

1. I rapporti DMARC vengono inviati ogni 24 ore. Puoi modificare la frequenza di invio dei rapporti nel campo **[!UICONTROL Reporting Interval]**. L’intervallo minimo autorizzato è di 1 ora, mentre il valore massimo autorizzato è di 2190 ore (ovvero 3 mesi).

1. Nei campi **SPF** e **[!UICONTROL DKIM Identifier Alignment]**, specifica quanto dovrà essere restrittivo il server del destinatario durante la verifica delle autenticazioni SPF e DKIM per un messaggio e-mail.

   * Modalità **[!UICONTROL Relaxed]**: il server accetta l’autenticazione anche se l’e-mail viene inviata da un sottodominio.
   * La modalità **[!UICONTROL Strict]** accetta l’autenticazione solo quando il dominio del mittente corrisponde esattamente a un dominio SPF e DKIM.

   Supponiamo di utilizzare il dominio `http://www.luma.com`. In modalità “Rilassata”, le e-mail provenienti dal sottodominio `marketing.luma.com` verranno autorizzate dal server, mentre verranno rifiutate in modalità “Restrittiva”.

1. Fai clic su **[!UICONTROL Add]** per confermare la creazione del record DMARC.

Una volta elaborata la creazione del record DMARC (circa 5 minuti), questo viene mostrato nella schermata dei dettagli dei sottodomini. [Scopri come monitorare i record TXT per i sottodomini](gs-txt-records.md#monitor)