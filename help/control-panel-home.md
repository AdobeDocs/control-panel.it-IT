---
title: Documentazione del prodotto
description: Documentazione del Pannello di controllo.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: ht
source-wordcount: '248'
ht-degree: 100%

---

# Centro risorse {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="Informazioni sul Pannello di controllo"
>abstract="La home page del Pannello di controllo ti consente di accedere a tutte le azioni che possono essere eseguite sulle istanze Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=it" text="Accesso al Pannello di controllo"

Il Pannello di controllo Campaign ti aiuta ad amministrare Campaign Standard e v7/v8 in modo più efficiente, consentendoti di gestire le impostazioni e tenere traccia dell’utilizzo di ciascuna istanza di Campaign.

## Novità

**Interfaccia utente**

* Il Pannello di controllo è ora disponibile in altre lingue. [Ulteriori informazioni](discover/using/discovering-the-interface.md#supported-languages-languages)

**Monitoraggio profili attivi**

* Se utilizzi più istanze, ora puoi monitorare il numero di profili attivi a cui hai diritto per la tua organizzazione e il numero totale di profili utilizzati nell’organizzazione all’interno di tutte le istanze. [Ulteriori informazioni](performance-monitoring/using/active-profiles-monitoring.md)

**Record DMARC**

* Più indirizzi e-mail possono ora ricevere e-mail di report aggregati e di report di errori. [Ulteriori informazioni](subdomains-certificates/using/dmarc.md)
* Sono state apportate modifiche se esistono record DMARC e BIMI per un sottodominio:

   * Impossibile eliminare i record DMARC. Se desideri eliminarne uno, devi prima eliminare il record BIMI.
   * È possibile modificare i record DMARC, ma il downgrade del criterio a “Nessuno” non è consentito e il relativo valore percentuale deve essere 100.

>[!CAUTION]
>
>* Il Pannello di controllo è riservato agli utenti amministratori. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=it#discover-control-panel)
>
>* Per Campaign v7, si applicano restrizioni di distribuzione. [Ulteriori informazioni](faq.md#v7-restrictions)

## Risorse aggiuntive {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=it">Video tutorial sul Pannello di controllo</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=it">Documentazione del prodotto di Campaign Standard</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=it">Video tutorial sul Pannello di controllo</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=it">Documentazione del prodotto di Campaign v7</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=it">Video tutorial sul Pannello di controllo</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=it">Documentazione del prodotto Campaign v8</a></li>
        </ul>
        </td>
    </tr>
</table>
