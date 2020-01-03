---
title: Rinnovo del certificato SSL di un sottodominio
description: Scopri come rinnovare i certificati SSL dei sottodomini
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Rinnovo del certificato SSL di un sottodominio {#renewing-subdomains-ssl-certificates}

## Informazioni sul rinnovo dei certificati {#about-certificate-renewal-process}

Il processo di rinnovo del certificato SSL comprende 3 passaggi, tutti eseguiti direttamente dal Pannello di controllo:

1. **La generazione della richiesta di firma dei certificati (CSR)** Adobe Customer Care genera un CSR. Per generare il CSR è necessario fornire alcune informazioni (ad esempio Nome comune, Nome organizzazione e indirizzo, ecc.).
1. **Acquisto del certificato** SSL Una volta generato il CSR, è possibile scaricarlo e utilizzarlo per acquistare il certificato SSL dall’autorità di certificazione approvata dalla società.
1. **Installazione del certificato** SSL Una volta acquistato il certificato SSL, è possibile installarlo nel sottodominio desiderato.

## Generazione di una richiesta di firma dei certificati (CSR) {#generating-csr}

Per generare una richiesta di firma dei certificati (CSR), procedere come segue:

1. Nella **[!UICONTROL Subdomains & Certificates]**scheda, selezionate l&#39;istanza desiderata, quindi fate clic sul**[!UICONTROL Manage Certificate]** pulsante.

   ![](assets/renewal1.png)

1. Selezionate **[!UICONTROL Generate a CSR]**, quindi fate clic**[!UICONTROL Next]** per avviare la procedura guidata che vi guiderà attraverso il processo di generazione CSR.

   ![](assets/renewal2.png)

1. Viene visualizzato un modulo con tutti i dettagli necessari per generare il CSR.

   Assicuratevi di compilare le informazioni richieste in modo completo e accurato (se necessario, contattate il team interno, i team di sicurezza e IT), quindi fate clic **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**:
   * **[!UICONTROL Organization Unit]**:
   * **[!UICONTROL Instance]**: URL dell&#39;istanza Campaign associata al sottodominio.
   ![](assets/renewal3.png)

1. Seleziona i sottodomini da includere nella CSR, quindi fai clic su **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. I sottodomini selezionati vengono visualizzati nell&#39;elenco. Per ciascuno di essi, seleziona i sottodomini da includere, quindi fai clic su **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Viene visualizzato un riepilogo dei sottodomini da includere nel CSR. Fate clic **[!UICONTROL Submit]**per confermare la richiesta.

   ![](assets/renewal6.png)

1. Il file .csr corrispondente alla selezione viene generato e scaricato automaticamente. Ora potete usarlo per acquistare il certificato SSL dall’autorità di certificazione approvata dalla società.

## Acquisto di un certificato con il CSR {#purchasing-certificate}

Dopo aver ottenuto un CSR per la richiesta di firma dei certificati dal Pannello di controllo, acquistate un certificato SSL da un&#39;autorità di certificazione approvata dalla vostra organizzazione.

## Installazione del certificato SSL {#installing-ssl-certificate}

Una volta acquistato un certificato SSL, effettuate le seguenti operazioni per installarlo nell’istanza.

1. Nella **[!UICONTROL Subdomains & Certificates]**scheda, selezionate l&#39;istanza desiderata, quindi fate clic sul**[!UICONTROL Manage Certificate]** pulsante.

   ![](assets/renewal1.png)

1. Fate clic **[!UICONTROL Install SSL Certificate]**, quindi**[!UICONTROL Next]** per avviare la procedura guidata che vi guiderà attraverso il processo di installazione del certificato.

   ![](assets/install1.png)

1. Selezionate il file .zip che contiene il certificato da installare, quindi fate clic **[!UICONTROL Submit]**.

   ![](assets/install2.png)