---
product: campaign
solution: Campaign
title: Rinnovo del certificato SSL di un sottodominio
description: Scopri come rinnovare i certificati SSL dei sottodomini
feature: Control Panel
role: Architect
level: Experienced
exl-id: af440b5d-1d21-44fb-831f-f2bdd6011b82
source-git-commit: 9be5a3ae48dccf74f509aa95fee29bbfdafddcdf
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 89%

---

# Installare il certificato SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Installazione del certificato SSL"
>abstract="Installa il certificato SSL acquistato dall’autorità di certificazione approvata dalla tua organizzazione."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=it" text="Informazioni sul branding dei sottodomini"

Una volta acquistato un certificato SSL, puoi installarlo nell’istanza. Prima di procedere, accertati di conoscere i prerequisiti seguenti:

* La richiesta di firma del certificato (CSR, Certificate Signing Request) deve essere stata generata dal Pannello di controllo. In caso contrario, non potrai installare il certificato dal Pannello di controllo.
* La richiesta di firma del certificato (CSR, Certificate Signing Request) deve corrispondere al sottodominio configurato per funzionare con Adobe. Ad esempio, non può contenere più sottodomini di quello configurato.
* Il certificato deve avere una data corrente. Non è possibile installare certificati con date future e non deve essere scaduto (vale a dire date di inizio e fine valide).
* Il certificato deve essere rilasciato da un’autorità di certificazione (CA, Certificate Authority) affidabile, come Comodo, DigiCert, GoDaddy, ecc..
* La dimensione del certificato deve essere di 2048 bit e l’algoritmo deve essere RSA.
* Il certificato deve essere in formato X.509 PEM.
* I certificati SAN sono supportati.
* I certificati con caratteri jolly non sono supportati.
* Il file ZIP o il certificato non devono essere protetti da password.
* Il file ZIP deve contenere solo quanto segue, preferibilmente in singoli file:
   * Certificato dell’entità finale.
   * Catena di certificati intermedi (ordinata in modo corretto).
   * Certificato radice (facoltativo).

Per installare il certificato, effettua le seguenti operazioni:

1. Nella scheda **[!UICONTROL Subdomains & Certificates]**, seleziona l’istanza desiderata, quindi fai clic sul pulsante **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Seleziona **[!UICONTROL 3 - Install Certificate Bundle]**, quindi fai clic su **[!UICONTROL Next]** per avviare la procedura guidata che ti guiderà attraverso il processo di installazione del certificato.

   ![](assets/install1.png)

1. Seleziona il file .zip che contiene il certificato da installare, quindi fai clic su **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>Il certificato verrà installato su tutti i domini/sottodomini inclusi nella CSR. Eventuali altri domini/sottodomini presenti nel certificato non saranno presi in considerazione.

Una volta installato il certificato SSL, la data di scadenza e l’icona di stato del certificato vengono aggiornate di conseguenza.
