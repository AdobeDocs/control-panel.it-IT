---
title: Ultima versione
description: Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in Pannello di controllo
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 26%

---

# Ultima versione {#control-panel-releases}

Questa pagina elenca le nuove funzionalità e i miglioramenti introdotti in Pannello di controllo.

## Ottobre 2023 {#october-2023}

**Interfaccia utente**

* Il Pannello di controllo Campaign è ora disponibile in altre lingue. [Ulteriori informazioni](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Monitoraggio profili attivi**

* Se utilizzi più istanze, ora puoi monitorare il numero di profili attivi a cui hai diritto per la tua organizzazione e il numero totale di profili utilizzati nell’organizzazione all’interno di tutte le istanze. [Ulteriori informazioni](../performance-monitoring/using/active-profiles-monitoring.md)

**Record DMARC**

* Più indirizzi e-mail possono ora ricevere e-mail di report aggregati e di report di errori. [Ulteriori informazioni](../subdomains-certificates/using/dmarc.md)
* Sono state apportate modifiche se esistono record DMARC e BIMI per un sottodominio:

   * Impossibile eliminare i record DMARC. Se desideri eliminarne uno, devi prima eliminare il record BIMI.
   * È possibile modificare i record DMARC, ma il downgrade del criterio a &quot;None&quot; non è consentito e il relativo valore percentuale deve essere 100.

