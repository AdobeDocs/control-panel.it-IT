---
title: Gestione dei record TXT
description: Scopri come gestire i record TXT per la verifica della proprietà del dominio.
translation-type: tm+mt
source-git-commit: 3ce9f62be9df0f6e6a61c16ddaf3ab8ae58712ce

---


# Gestione dei record TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id=&quot;cp_siteverification_add&quot;
>title=&quot;Gestione dei record TXT&quot;
>abstract=&quot;Alcuni servizi come Google richiedono l&#39;aggiunta di un record TXT alle impostazioni del dominio per verificare di essere proprietario del dominio.&quot;

## Informazioni sui record TXT {#about-txt-records}

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, che possono essere lette da origini esterne.

Al fine di garantire elevate percentuali di posta in arrivo e basse frequenze di posta indesiderata, alcuni servizi come Google richiedono l&#39;aggiunta di un record TXT alle impostazioni del dominio per verificare di essere proprietario del dominio.

Attualmente, Gmail è uno dei provider di indirizzi e-mail più popolari. Al fine di garantire la buona recapito e la corretta consegna delle e-mail agli indirizzi Gmail, Adobe Campaign consente di aggiungere ai sottodomini specifici record TXT per la verifica del sito Google, in modo da verificarne la validità.

## Aggiunta di un record Google TXT per un sottodominio {#adding-a-google-txt-record}

Per aggiungere un record Google TXT al tuo sottodominio utilizzato per inviare indirizzi Gmail, procedi come segue:

1. Passate alla **[!UICONTROL Subdomain and Certificates]** scheda.

1. Selezionare l&#39;istanza, quindi aprire i dettagli del sottodominio a cui si desidera aggiungere un record DNS.

   ![](assets/txt_subdomaindetails.png)

1. Fate clic sul **[!UICONTROL Add TXT record]** pulsante, quindi immettete il valore generato negli strumenti di amministrazione di G Suite. Per ulteriori informazioni, consulta la Guida [di amministrazione di](https://support.google.com/a/answer/183895)G Suite.

   ![](assets/txt_addtxt.png)

1. Fate clic sul **[!UICONTROL Add]** pulsante per confermare.

   ![](assets/txt_txtadded.png)

Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A tal fine, andate agli strumenti di amministrazione di G Suite e avviate il passaggio di verifica (consultate la Guida [di amministrazione di](https://support.google.com/a/answer/183895)G Suite).


Per eliminare un record, selezionatelo dall&#39;elenco dei record, quindi fate clic sul pulsante Rimuovi.

>[!NOTE]
>
>L&#39;unico record che puoi eliminare dall&#39;elenco dei record DNS è quello che hai aggiunto in precedenza (nel nostro caso il record Google TXT).
