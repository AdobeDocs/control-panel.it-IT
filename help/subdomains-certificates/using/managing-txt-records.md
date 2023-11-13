---
product: campaign
solution: Campaign
title: Aggiungere record di verifica del sito Google per un sottodominio
description: Scopri come aggiungere un record di verifica del sito Google per un sottodominio al fine di verificare la proprietà del dominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '300'
ht-degree: 100%

---

# Aggiungere record di verifica del sito Google {#adding-a-google-txt-record}

Al fine di garantire tassi di posta in arrivo elevati e tassi di posta indesiderata ridotti, alcuni servizi, come Google, richiedono l’aggiunta di un record TXT alle impostazioni del dominio per verificare che tu sia il proprietario del dominio.

Attualmente, Gmail è uno dei provider di indirizzi e-mail più popolari. Al fine di garantire un buon recapito dei messaggi e la corretta consegna delle e-mail agli indirizzi Gmail, Adobe Campaign ti consente di aggiungere ai sottodomini record TXT di Google specifici per la verifica del sito, in modo da verificarne la validità.

Per aggiungere un record TXT di Google al tuo sottodominio utilizzato per inviare e-mail a indirizzi Gmail, procedi come segue:

1. Dall’elenco dei sottodomini, fai clic sul pulsante con i puntini di sospensione accanto al sottodominio desiderato e seleziona **[!UICONTROL Dettagli sottodominio]**.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi record TXT]** , quindi scegli **[!UICONTROL Verifica sito Google]** dall’elenco a discesa **[!UICONTROL Tipo di record]**.

1. Inserisci il valore generato negli strumenti per l’amministrazione di G Suite. Per ulteriori informazioni, consulta la [guida per gli amministratori di G Suite](https://support.google.com/a/answer/183895?hl=it).

   ![](assets/txt_addtxt.png)

1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** per confermare.

   ![](assets/txt_txtadded.png)

Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A tal fine, accedi agli strumenti di amministrazione di G Suite e avvia il passaggio di verifica (consulta la [Guida di Amministratore di G Suite](https://support.google.com/a/answer/183895?hl=it)).

Per eliminare un record, selezionalo dall’elenco dei record, quindi fai clic sul pulsante di rimozione.

>[!NOTE]
>
>L’unico record che puoi eliminare dall’elenco dei record DNS è quello che hai aggiunto in precedenza (nel nostro caso il record TXT di Google).

![](assets/do-not-localize/how-to-video.png) Guarda il video su questa funzione per [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=it#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=it#subdomains-and-certificates)
