---
product: campaign
solution: Campaign
title: Gestione dei record TXT
description: Scopri come gestire i record TXT per la verifica della proprietà del dominio.
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 100%

---


# Gestione dei record TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gestione dei record TXT"
>abstract="Alcuni servizi, come Google, richiedono l’aggiunta di un record TXT alle impostazioni del dominio per verificare che tu sia il proprietario del dominio."

## Informazioni sui record TXT {#about-txt-records}

I record TXT sono un tipo di record DNS utilizzati per fornire informazioni testuali su un dominio, leggibili da sorgenti esterne.

Al fine di garantire elevate percentuali di posta in arrivo e basse percentuali di posta indesiderata, alcuni servizi, come Google, richiedono l’aggiunta di un record TXT alle impostazioni del dominio per verificare che tu sia il proprietario del dominio.

Attualmente, Gmail è uno dei provider di indirizzi e-mail più popolari. Al fine di garantire un buon recapito dei messaggi e la corretta consegna delle e-mail agli indirizzi Gmail, Adobe Campaign ti consente di aggiungere ai sottodomini record TXT di Google specifici per la verifica del sito, in modo da verificarne la validità.

Risorse aggiuntive:

* [Video tutorial per Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)
* [Video tutorial per Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/google-txt-record-management.html)

## Aggiunta di un record TXT di Google a un sottodominio {#adding-a-google-txt-record}

Per aggiungere un record TXT di Google al tuo sottodominio utilizzato per inviare e-mail a indirizzi Gmail, procedi come segue:

1. Accedi alla scheda **[!UICONTROL Subdomain and Certificates]**.

1. Seleziona l’istanza, quindi apri i dettagli del sottodominio a cui desideri aggiungere un record DNS.

   ![](assets/txt_subdomaindetails.png)

1. Fai clic sul pulsante **[!UICONTROL Add TXT record]**, quindi inserisci il valore generato negli strumenti di Amministratore di G Suite. Per ulteriori informazioni, consulta la [Guida di Amministratore di G Suite](https://support.google.com/a/answer/183895?hl=it).

   ![](assets/txt_addtxt.png)

1. Fai clic sul pulsante **[!UICONTROL Add]** per confermare.

   ![](assets/txt_txtadded.png)

Una volta aggiunto il record TXT, è necessario che sia verificato da Google. A tal fine, accedi agli strumenti di amministrazione di G Suite e avvia il passaggio di verifica (consulta la [Guida di Amministratore di G Suite](https://support.google.com/a/answer/183895?hl=it)).

Per eliminare un record, selezionalo dall’elenco dei record, quindi fai clic sul pulsante di rimozione.

>[!NOTE]
>
>L’unico record che puoi eliminare dall’elenco dei record DNS è quello che hai aggiunto in precedenza (nel nostro caso il record TXT di Google).
