---
solution: Journey Optimizer
product: journey optimizer
title: Toegang tot en abonnement op systeemwaarschuwingen
description: Meer informatie over toegang tot systeemwaarschuwingen en uw abonnement op systeemwaarschuwingen
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Toegang tot en abonnement op systeemwaarschuwingen {#alerts}

Wanneer het bouwen van uw reizen en campagnes, gebruik de **knoop van het Alarm** om fouten te controleren en op te lossen alvorens hen uit te voeren of te publiceren:

* Leer hoe te om uw reizen op [ problemen op te lossen deze pagina ](../building-journeys/troubleshooting.md).
* Leer hoe te om uw campagnes op [ te herzien deze pagina ](../campaigns/review-activate-campaign.md).

Vanuit het speciale menu **[!UICONTROL Alerts]** kunt u zich ook abonneren op [!DNL Adobe Journey Optimizer] -systeemwaarschuwingen zoals deze op deze pagina worden beschreven.

## Toegangswaarschuwingen {#access-alerts}

Wanneer een fout optreedt, kunt u systeemwaarschuwingen ontvangen in het Journey Optimizer-meldingscentrum (waarschuwingen in de app) en/of een e-mail ontvangen. Voer de onderstaande stappen uit om toegang te krijgen tot deze waarschuwingen.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>Leer meer over alarm in Adobe Experience Platform in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=nl-NL){target="_blank"}.

Klik in het linkermenu onder **[!UICONTROL Administration]** op **[!UICONTROL Alerts]** . Er zijn verschillende vooraf geconfigureerde waarschuwingen voor Journey Optimizer beschikbaar.

Deze worden als volgt vermeld en elke waarschuwing wordt hieronder beschreven.

* Signaleringen die specifiek zijn voor reizen:

   * het [ alarm van de Actie van de Douane van de 1&rbrace; Reis](#alert-custom-actions)
   * [ Gelezen de Trekker van de Publiek Onsuccesvol ](#alert-read-audiences) alarm

* Waarschuwingen specifiek voor kanaalconfiguratie:

   * het [ DNS van het Domein van AJO- verslag missen ](#alert-dns-record-missing) alarm
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Abonneren op waarschuwingen {#subscribe-alerts}

1. U kunt zich vanuit de gebruikersinterface op elke waarschuwing afzonderlijk abonneren door de optie **[!UICONTROL Subscribe]** te selecteren.

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >Abonnement is alleen van toepassing op een specifieke sandbox. U moet zich voor elke sandbox afzonderlijk abonneren op waarschuwingen.

1. Gebruik dezelfde methode voor **[!UICONTROL Unsubscribe]** .

1. U kunt aan alarm door [ I/O de berichten van de Gebeurtenis ook intekenen ](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=nl-NL){target="_blank"}. Waarschuwingsregels zijn ingedeeld in verschillende abonnementspakketten. De abonnementen van de gebeurtenis die aan het specifieke alarm van Journey Optimizer beantwoorden zijn gedetailleerd [ hieronder ](#journey-alerts).

1. Als een onverwacht gedrag optreedt en/of een bepaalde set voorwaarden in uw bewerkingen is bereikt (zoals een mogelijk probleem wanneer het systeem een drempelwaarde overschrijdt), worden waarschuwingsmeldingen verzonden naar gebruikers in uw organisatie die zich op deze gebruikers hebben geabonneerd.

Op basis van de voorkeuren van de abonnee worden waarschuwingen verzonden via e-mail en/of rechtstreeks in het Journey Optimizer-meldingscentrum in de rechterbovenhoek van de gebruikersinterface (in-app-meldingen). Selecteer in de sectie [!DNL Adobe Experience Cloud] **[!UICONTROL Preferences]** hoe u deze waarschuwingen wilt ontvangen. [Meer informatie](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>Standaard is alleen waarschuwingen in de app ingeschakeld.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=nl-NL#enable-email-alerts){target="_blank"}.-->

Wanneer een alarm wordt opgelost, ontvangen de abonnees een &quot;Opgelost&quot;bericht.

## Waarschuwingen beheren {#manage-alerts}

Selecteer een item en gebruik de knop **[!UICONTROL More actions]** om waarschuwingen te beheren.

![](assets/alert-more-actions.png){width=80%}

Standaard zijn alle waarschuwingen ingeschakeld. Als u een waarschuwing wilt uitschakelen, selecteert u de optie **[!UICONTROL Disable alert]** in het menu **[!UICONTROL More actions]** . Alle abonnees op deze waarschuwing ontvangen de gerelateerde meldingen niet meer.

Selecteer **[!UICONTROL Manage alert subscribers]** om de lijst weer te geven met gebruikers die zich op de waarschuwing hebben geabonneerd. Gebruik het lege veld om meer abonnees toe te voegen.

![](assets/alert-subscribers.png){width=80%}

De mogelijke statussen voor waarschuwingen worden hieronder weergegeven:

* **[!UICONTROL Enabled]** - De waarschuwing is ingeschakeld en controleert momenteel de triggervoorwaarde.
* **[!UICONTROL Disabled]** - De waarschuwing is uitgeschakeld en controleert momenteel niet de triggervoorwaarde. U ontvangt geen meldingen voor deze waarschuwing.
* **[!UICONTROL Triggered]** - Er wordt momenteel voldaan aan de triggervoorwaarde van de waarschuwing.

## Reiswaarschuwingen {#journey-alerts}

>[!CAUTION]
>
>Het specifieke alarm van Adobe Journey Optimizer is slechts op **levende** reizen van toepassing. Er worden geen waarschuwingen gegeven voor reizen in testmodus.

### Aangepaste actie voor reis mislukt {#alert-custom-actions}

Deze waarschuwing geeft een waarschuwing als een aangepaste handeling mislukt. Wij zijn van mening dat er sprake is van een mislukking waarbij de afgelopen vijf minuten meer dan 1 procent van de fouten is gemaakt bij een specifieke aangepaste actie. Dit wordt elke 30 seconden geëvalueerd.

![](assets/alerts-custom-action.png)

Waarschuwingen over aangepaste handelingen worden opgelost wanneer, gedurende de laatste 5 minuten:

* er is geen fout opgetreden bij die aangepaste handeling (of bij fouten onder de drempel van 1%);

* of, er is geen profiel dat aangepaste handeling heeft bereikt.

De naam van het I/O gebeurtenisabonnement die aan het alarm van de douaneactie beantwoordt is **de Mislukking van de Actie van de Douane van de Reis**.

Om **het alarm van de Actie van de Douane problemen op te lossen**:

* Controleer uw aangepaste actie in de testmodus op een andere reis:

  ![](assets/alert-troubleshooting-2.png)

* Controleer uw reisrapport om foutredenen voor actie te zien.

  ![](assets/alert-troubleshooting-3.png)

* Controleer uw reis stepEvents om naar meer informatie rond &quot;failureReason&quot; te zoeken.

* Controleer uw configuratie van de douaneactie en bevestig dat de authentificatie nog OK is. Voer bijvoorbeeld een handmatige controle uit met Postman.

### Trigger voor publiek lezen is mislukt {#alert-read-audiences}

Dit alarm waarschuwt u als de a **Gelezen activiteit van het publiek** geen profiel 10 min na geplande tijd van uitvoering heeft verwerkt. Deze fout kan worden veroorzaakt door technische problemen, of omdat het publiek leeg is. Als deze fout door technische problemen wordt veroorzaakt, moet u er rekening mee houden dat er nog steeds pogingen kunnen worden gedaan, afhankelijk van het type probleem (bijvoorbeeld: als het aanmaken van exportarbeidsplaatsen is mislukt, proberen we elke 10 miljoen opnieuw gedurende maximaal 1 uur).

![](assets/alerts1.png)

Het alarm op **Gelezen de activiteiten van het publiek** zijn slechts op terugkomende reizen van toepassing. **las de activiteiten van het publiek** in levende reizen die een programma hebben om **in werking te stellen** of **zodra mogelijk** wordt genegeerd.

Het alarm op **Gelezen Publiek** wordt opgelost wanneer een profiel de **Gelezen knoop van het Publiek** ingaat.

De I/O naam van het gebeurtenisabonnement die aan **beantwoordt las de Trekker van het Publiek Onsuccesvol** alarm is **Reis leest publieksvertragingen, Mislukkingen en Fouten**.

Om **te problemen op te lossen leest het 1&rbrace; alarm van het publiek &lbrace;, controleer uw publiekstelling in de interface van Experience Platform.**

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

## Configuratiewaarschuwingen {#configuration-alerts}

### AJO Domain DNS-record ontbreekt {#alert-dns-record-missing}

Dit alarm brengt u op de hoogte wanneer de kritieke DNS verslagen (NS of CNAME) die voor juiste leveringsconfiguratie worden vereist ontbreken of misconfigured zijn. Zonder deze records kan de e-mailleverbaarheid in het gedrang komen.

>[!NOTE]
>
>* NS-records zijn essentieel voor volledige subdomeindelegatie naar Adobe. [Meer informatie](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME-records ondersteunen CNAME-subdomeininstelling. [Meer informatie](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

Het **DNS van het Domein van AJO DNS verslag missen** alarm wordt teweeggebracht wanneer het systeem ontdekt dat de vereiste NS of CNAME verslagen afwezig zijn of niet de configuratienormen aanpassen.

1. Klik het alarm dat aan beïnvloede [ subdomain ](../configuration/delegate-subdomain.md) in de [!DNL Journey Optimizer] interface moet worden geleid.

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Verbeter de DNS configuratie door de verslagen correct te plaatsen en [ voorlegt opnieuw subdomain ](../configuration/delegate-subdomain.md#submit-subdomain) delegatie.

   >[!NOTE]
   >
   >Zorg ervoor dat alle verslagen behoorlijk op uw domein het ontvangen oplossing alvorens te werk te gaan worden gecreeerd.

1. Als u niet zeker bent van de juiste waarden, kunt u een nieuw subdomein maken in [!DNL Journey Optimizer] met dezelfde naam als het subdomein waarop het effect is toegepast. [ leer hoe te opstelling een nieuw subdomain ](../configuration/delegate-subdomain.md#set-up-subdomain)

Als de wijzigingen het probleem niet verhelpen, wordt dezelfde waarschuwing de volgende dag opnieuw geactiveerd.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?

### AJO channel configuration failure {#alert-channel-config-failure}

>[!IMPORTANT]
>
>This alert applies only to **email** channel configurations using the [custom subdomain](../configuration/delegate-custom-subdomain.md) delegation type. ///Other channel types (such as SMS, push, or in-app) are not covered by this alert.///

This alert is triggered in case the system audit detects email channel configuration issues. These issues may include misconfigured channel settings, invalid DNS configuration, suppression list issue, IP inconsistency, or any other errors that can impact email delivery.

If you receive such an alert, the resolution steps are listed below:

1. Click the alert to be directed to the impacted [email channel configuration](../email/get-started-email-config.md) in the [!DNL Journey Optimizer] interface.

   For guidance on editing channel configurations, see [this section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Review the configuration details and error messages provided. Common failure reasons include:

   * SPF validation failed
   * DKIM validation failed
   * MX record validation failed
   * Invalid DNS records

   >[!NOTE]
   >
   >The possible configuration failure reasons are listed in [this section](../configuration/channel-surfaces.md).

1. Resolve the issue:

   * Update the channel configuration as needed.
   * You may need to fix specific DNS issues mentioned in the alert.

   >[!NOTE]
   >
   >As a single domain can be associated with multiple channel configurations, resolving DNS issues for one channel configuration may automatically fix related issues across several configurations.

If the change does not resolve the issue, the same alert will be triggered again the next day.

When resolving email configuration issues, keep in mind the best practices listed below:

* Act promptly - Address configuration failures as soon as they are detected to avoid disruptions in email delivery.
* Check all configurations - If the alert indicates multiple impacted email configurations, review and fix each of them.

### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





