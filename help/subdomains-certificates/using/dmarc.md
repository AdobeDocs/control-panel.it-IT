---
product: campaign
solution: Campaign
title: Aggiungere record DMARC
description: Scopri come aggiungere un record DMARC per un sottodominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 80b9f62feb9f00758cf175762b1cf4dc26912ed8
workflow-type: ht
source-wordcount: '885'
ht-degree: 100%

---

# Aggiungere record DMARC {#dmarc}

## Informazioni sui record DMARC {#about}

DMARC (Domain Based Message Authentication, Reporting and Conformance) è uno standard del protocollo di autenticazione e-mail che aiuta le organizzazioni a proteggere i domini e-mail dagli attacchi di phishing e spoofing. Consente di decidere in che modo un provider di cassette postali deve gestire le e-mail che non superano i controlli SPF e DKIM, fornendo un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi.

Informazioni dettagliate sull’implementazione di DMARC sono disponibili nella  [Guida alle best practice per la recapitabilità di Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=it)

## Limitazioni e prerequisiti {#limitations}

* I record SPF e DKIM sono prerequisiti per la creazione di un record DMARC.
* I record DMARC possono essere aggiunti solo per i sottodomini che utilizzano la delega completa dei sottodomini. [Ulteriori informazioni sui metodi di configurazione dei sottodomini](subdomains-branding.md#subdomain-delegation-methods)

  Per stabilire un record DMARC in un sottodominio basato su CNAME, puoi configurare il record DMARC nel relativo dominio principale. In questo modo tutti i sottodomini associati ereditano i parametri del record DMARC, anche se delegati tramite CNAME.

* Se esistono record DMARC e BIMI per un sottodominio:
   * Impossibile eliminare i record DMARC. Se si desidera eliminare un record DMARC, eliminare prima il record BIMI.
   * È possibile modificare i record DMARC, ma il downgrade dei criteri DMARC a “Nessuno” non è consentito e il valore percentuale deve essere impostato su “100”.

## Aggiungere un record DMARC per un sottodominio {#add}

Per aggiungere un record DMARC per un sottodominio, segui questi passaggi:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Dettagli sottodominio]**.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi record TXT]**, quindi scegli **[!UICONTROL DMARC]** dall’elenco a discesa **[!UICONTROL Tipo di record]**.

   ![](assets/dmarc-add.png)

1. Scegli il **[!UICONTROL Tipo di criterio]** che il server destinatario deve seguire nel caso in cui una delle e-mail non riesca. I tipi di criteri disponibili sono:

   * **[!UICONTROL Nessuno]**,
   * **[!UICONTROL Quarantena]** (inserimento nella cartella di posta indesiderata),
   * **[!UICONTROL Rifiuta]** (blocco dell’e-mail).

   Come best practice, si consiglia di distribuire lentamente l’implementazione di DMARC aumentando il livello dei criteri DMARC da c=nessuno a c=quarantena, fino a c=rifiuta man mano che acquisisci una comprensione di DMARC e del suo potenziale impatto.

   * **Passaggio 1:** analizza il feedback ricevuto e utilizza (c=nessuno), che indica al destinatario di non eseguire azioni sui messaggi che non superano l’autenticazione, ma che inviano comunque i rapporti e-mail al mittente. Inoltre, se l’autenticazione dei messaggi legittimi non riesce, esamina e risolvi i problemi relativi a SPF/DKIM.

   * **Passaggio 2:** determina se SPF e DKIM sono allineati e trasmettono l’autenticazione per tutte le e-mail legittime, quindi sposta il criterio su (c=quarantena), che indica al server e-mail ricevente di mettere in quarantena le e-mail che non riescono a eseguire l’autenticazione (in genere significa inserire tali messaggi nella cartella di posta indesiderata). Se il criterio è impostato per la quarantena, si consiglia di iniziare con una piccola percentuale di e-mail.

   * **Passaggio 3:** imposta il criterio su (c=rifiuta). NOTA: utilizza questo criterio con cautela e determina se è appropriato per la tua organizzazione. Il criterio c= rifiuta indica al destinatario di rifiutare completamente (non recapitare) qualsiasi e-mail per il dominio che non supera l’autenticazione. Con questo criterio abilitato, solo i messaggi e-mail verificati come autenticati al 100% dal dominio avranno anche la possibilità di inserire la casella in entrata.

   >[!NOTE]
   >
   > La creazione di record BIMI non è disponibile con un tipo di criterio di record DMARC impostato su “Nessuno”.

1. Inserisci gli indirizzi e-mail che devono ricevere i rapporti DMARC. Puoi aggiungere più indirizzi e-mail separati da virgole. Quando una delle e-mail non riesce, i rapporti DMARC vengono inviati automaticamente all’indirizzo e-mail scelto:

   * I rapporti Aggregate-DMARC forniscono informazioni di alto livello come, ad esempio, il numero di e-mail non riuscite per un determinato periodo.
   * I rapporti forensi sugli errori DMARC forniscono informazioni dettagliate, ad esempio l’indirizzo IP da cui proviene l’e-mail non riuscita.

   >[!CAUTION]
   >
   >Se gli indirizzi e-mail che stai aggiungendo per ricevere i rapporti si trovano all’esterno del dominio per il quale viene creato il record DMARC, dovrai autorizzare il dominio esterno a specificare al DNS che possiedi quel dominio. A questo scopo, segui i passaggi descritti nella [Documentazione di dmarc.org](https://dmarc.org/2015/08/receiving-dmarc-reports-outside-your-domain)

1. Se il criterio DMARC è impostato su “Nessuno”, immetti una percentuale valida per il 100% delle e-mail.

   Se il criterio è impostato su “Rifiuta” o “Quarantena”, si consiglia di iniziare con una piccola percentuale di e-mail. Man mano che più e-mail dal dominio passano l’autenticazione con i server riceventi, aggiorna il record lentamente con una percentuale più alta.

   >[!NOTE]
   >
   >Se il dominio utilizza BIMI, il criterio DMARC deve avere un valore percentuale del 100%. BIMI non supporta i criteri DMARC con questo valore impostato su una percentuale inferiore al 100%.

   ![](assets/dmarc-add2.png)

1. I rapporti DMARC vengono inviati ogni 24 ore. Puoi modificare la frequenza di invio dei rapporti nel campo **[!UICONTROL Intervallo di reportiistica]**. L’intervallo minimo autorizzato è di 1 ora, mentre il valore massimo autorizzato è di 2190 ore (ovvero 3 mesi).

1. Nei campi **SPF** e **[!UICONTROL Allineamento identificatore DKIM]**, specifica quanto dovranno essere restrittivi i server destinatari nella verifica delle autenticazioni SPF e DKIM di un messaggio e-mail.

   * **[!UICONTROL Rilassato]**: il server accetta l’autenticazione anche se l’e-mail viene inviata da un sottodominio,
   * In modalità **[!UICONTROL Rigoroso]**, l’autenticazione viene accettata solo se il dominio del mittente corrisponde esattamente a un dominio SPF e DKIM.

   Supponiamo di utilizzare il dominio `http://www.luma.com`. In modalità “Rilassata”, le e-mail provenienti dal sottodominio `marketing.luma.com` verranno autorizzate dal server, mentre verranno rifiutate in modalità “Rigorosa”.

1. Fai clic su **[!UICONTROL Aggiungi]** per confermare la creazione del record DMARC.

Una volta elaborata la creazione del record DMARC (circa 5 minuti), questo viene mostrato nella schermata dei dettagli dei sottodomini. [Scopri come monitorare i record TXT per i sottodomini](gs-txt-records.md#monitor)
