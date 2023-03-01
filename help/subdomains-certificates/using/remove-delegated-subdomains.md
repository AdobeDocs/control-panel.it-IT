---
product: campaign
solution: Campaign
title: Rimuovere la delega dei sottodomini
description: Scopri come rimuovere la delega dei sottodomini ad Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: deb99ceb789f40c905de1a76cca8deca6b979765
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 16%

---

# Rimuovi la delega dei sottodomini ad Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Rimuovi la delega del sottodominio"
>abstract="Questa schermata ti consente di rimuovere la delega di un sottodominio all’Adobe. Tieni presente che questo processo non può essere annullato ed è irreversibile fino al completamento della sua esecuzione.<br><br>Se stai tentando di rimuovere la delega di un dominio primario per l’istanza selezionata, ti verrà chiesto di scegliere il dominio che la sostituirà."

Pannelli di controllo Campaign consente di rimuovere la delega di un sottodominio delegato ad Adobe, inclusa la configurazione di CNAME.

## Note importanti {#important}

Prima di procedere, considera attentamente gli impatti che si verificano una volta attivato il processo di rimozione:

* Una volta attivato il processo, la rimozione della delega del sottodominio non può essere annullata ed è irreversibile fino al completamento dell’esecuzione del processo.
* Nessun’altra delega di sottodominio può essere rimossa quando è in corso un processo simile su un altro sottodominio.
* Una delega rimossa in un sottodominio non può essere ridelegata fino a 3 giorni dalla sua rimozione.

## Rimuovere una delega di sottodominio {#steps}

Per rimuovere la delega di un sottodominio ad Adobe, effettua le seguenti operazioni:

1. Fai clic sul pulsante con i puntini di sospensione accanto alla delega di dominio da rimuovere e seleziona **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Rivedi la liberatoria e conferma la rimozione della delega del dominio all’Adobe.

1. Rivedi le informazioni relative all’istanza a cui è associato il sottodominio, incluse le affinità IP e le configurazioni del brand correlate.

   Se rimuovi la delega del dominio primario per l’istanza selezionata, devi scegliere il dominio che la sostituirà utilizzando **[!UICONTROL Replacement Domain]** elenco.

   Clic **[!UICONTROL Next]** per procedere con la rimozione.

   ![](assets/undelegate-subdomain-details.png)

1. Esamina il riepilogo visualizzato. Per confermare la rimozione, digita l’URL del dominio per il quale vuoi rimuovere la delega e fai clic su **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Dopo l’avvio della rimozione della delega, il processo in sospeso viene visualizzato nei registri del processo fino al suo completamento.

![](assets/undelegate-job.png)

## Codici di errore {#FAQ}

In questa sezione sono elencati i messaggi di errore che possono verificarsi quando si tenta di rimuovere la delega di un sottodominio:

| Codice errore | Messaggio | Descrizione |
|  ---  |  ---  |  ---  |
| 8002 | La rimozione del dominio delegato richiesta non può essere effettuata perché è in corso una richiesta simile in sovrapposizione. Riprova dopo 3 giorni | È già in corso un processo di rimozione della delega di sottodominio per l’istanza selezionata. Attendere 3 giorni per avviare un nuovo processo di rimozione. |
| 8003 | La rimozione del dominio delegato richiesta non è supportata per questa istanza. | La rimozione della delega non è supportata per il sottodominio selezionato a causa di un problema tecnico. Rivolgiti all’Assistenza clienti. |
| 8004 | La rimozione del dominio delegato richiesta non è consentita in quanto in questa istanza è presente un solo dominio. | È stato delegato un solo sottodominio per l’istanza selezionata. La rimozione della delega non è consentita. |
| 8005 | La rimozione del dominio delegato richiesta non è supportata per questa configurazione. | La rimozione della delega non è supportata per il sottodominio selezionato a causa di un problema tecnico. Rivolgiti all’Assistenza clienti. |
| 8006 | La rimozione del dominio delegato richiesta non è consentita per motivi sconosciuti. Contatta l’assistenza clienti. | La rimozione della delega non è supportata per l’istanza selezionata a causa di problemi sconosciuti. Rivolgiti all’Assistenza clienti. |
