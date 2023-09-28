---
product: campaign
solution: Campaign
title: Aggiungi record DMARC
description: Scopri come aggiungere un record DMARC per un sottodominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: fc026f157346253fc79bde4ce624e7efa3373af2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# Aggiungi record DMARC {#dmarc}

## Informazioni sui record DMARC {#about}

DMARC (Domain Based Message Authentication, Reporting and Conformance) è uno standard del protocollo di autenticazione e-mail che aiuta le organizzazioni a proteggere i domini e-mail dagli attacchi di phishing e spoofing. Consente di decidere in che modo un provider di caselle di posta deve gestire le e-mail che non superano i controlli SPF e DKIM, fornendo un modo per autenticare il dominio del mittente e impedire l’uso non autorizzato del dominio per scopi dannosi.

## Limitazioni e prerequisiti {#limitations}

* I record SPF e DKIM sono prerequisiti per la creazione di un record DMARC.
* I record DMARC possono essere aggiunti solo per i sottodomini che utilizzano la delega completa dei sottodomini. [Ulteriori informazioni sui metodi di configurazione dei sottodomini](subdomains-branding.md#subdomain-delegation-methods)

## Aggiungere un record DMARC per un sottodominio {#add}

Per aggiungere un record DMARC per un sottodominio, effettua le seguenti operazioni:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Subdomain details]**.

1. Fai clic su **[!UICONTROL Add TXT record]** , quindi scegliere **[!UICONTROL DMARC]** dal **[!UICONTROL Record Type]** elenco a discesa.

   ![](assets/dmarc-add.png)

1. Scegli la **[!UICONTROL Policy Type]** che il server del destinatario deve seguire quando una delle e-mail non riesce. I tipi di criteri disponibili sono:

   * Nessuna,
   * quarantena (posizionamento di cartelle di posta indesiderata),
   * Rifiuta (blocca l’e-mail).

   Se il sottodominio è appena stato configurato, si consiglia di impostare questo valore su &quot;None&quot; finché il sottodominio non è completamente configurato e le e-mail non vengono inviate correttamente. Una volta che tutto è configurato correttamente, puoi impostare il Tipo di criterio su &quot;Quarantena&quot; o &quot;Rifiuta&quot;.

   >[!NOTE]
   >
   > La creazione di record BIMI non è disponibile con un tipo di criterio di record DMARC impostato su &quot;None&quot;.

1. Inserisci gli indirizzi e-mail che devono ricevere i rapporti DMARC. Quando una delle e-mail non riesce, i rapporti DMARC vengono inviati automaticamente all’indirizzo e-mail scelto:

   * I rapporti Aggregate-DMARC forniscono informazioni di alto livello come, ad esempio, il numero di e-mail non riuscite per un determinato periodo.
   * I rapporti forensi sugli errori DMARC forniscono informazioni dettagliate, ad esempio l’indirizzo IP da cui proviene l’e-mail non riuscita.

1. Per impostazione predefinita, il criterio DMARC selezionato viene applicato a tutte le e-mail. Puoi modificare questo parametro per applicarlo solo a una percentuale specifica di e-mail.

   Quando distribuisci gradualmente DMARC, puoi iniziare con una piccola percentuale dei messaggi. Man mano che più messaggi provenienti dal dominio passano l’autenticazione con i server riceventi, aggiorna il record con una percentuale più alta, fino a raggiungere il 100%.

   >[!NOTE]
   >
   >Se il dominio utilizza BIMI, il criterio DMARC deve avere un valore percentuale del 100%. BIMI non supporta i criteri DMARC con questo valore impostato su un valore inferiore al 100%.

   ![](assets/dmarc-add2.png)

1. I rapporti DMARC vengono inviati ogni 24 ore. Puoi modificare la frequenza di invio dei rapporti in **[!UICONTROL Reporting Interval]** campo. L’intervallo minimo autorizzato è di 1 ora, mentre il valore massimo autorizzato è di 2190 ore (ovvero 3 mesi).

1. In **SPF** e **[!UICONTROL DKIM Identifier Alignment]** specificare il livello di rigidità dei server dei destinatari durante la verifica delle autenticazioni SPF e DKIM per un messaggio e-mail.

   * **[!UICONTROL Relaxed]** modalità: il server accetta l’autenticazione anche se l’e-mail viene inviata da un sottodominio,
   * **[!UICONTROL Strict]** La modalità accetta l&#39;autenticazione solo quando il dominio del mittente corrisponde esattamente a un dominio SPF e DKIM.

   Supponiamo di lavorare con `http://www.luma.com` dominio. In modalità &quot;Relax&quot;, le e-mail provenienti dal `marketing.luma.com` Il sottodominio verrà autorizzato dal server, mentre verrà rifiutato in modalità &quot;Strict&quot; (Rigoroso).

1. Clic **[!UICONTROL Add]** per confermare la creazione del record DMARC.

Una volta elaborata la creazione del record DMARC (circa 5 minuti), questa viene visualizzata nella schermata dei dettagli dei sottodomini. [Scopri come monitorare i record TXT per i sottodomini](gs-txt-records.md#monitor)