---
solution: Journey Optimizer
product: journey optimizer
title: Toegang tot en abonnement op systeemwaarschuwingen
description: Meer informatie over toegang tot systeemwaarschuwingen en uw abonnement op systeemwaarschuwingen
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 03e9d4205f59a32347cd1702b24bfbad2bf540b9
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 0%

---

# Toegang tot en abonnement op systeemwaarschuwingen {#alerts}

## Overzicht

Adobe Journey Optimizer biedt twee typen waarschuwingen om u te helpen uw bewerkingen te controleren en problemen op te lossen:

* **In-canvas bevestigingsalarm**: Wanneer het bouwen van reizen en campagnes, gebruik de **Alarm** knoop in het canvas om configuratiefouten te identificeren en op te lossen alvorens te publiceren. Leer hoe te [&#x200B; uw reizen &#x200B;](../building-journeys/troubleshooting.md) problemen op te lossen en uw campagnes te herzien: [&#x200B; campagnes van de Actie &#x200B;](../campaigns/review-activate-campaign.md) | [&#x200B; API-teweeggebrachte campagnes &#x200B;](../campaigns/review-activate-api-triggered-campaign.md) | [&#x200B; Geordende campagnes &#x200B;](../orchestrated/start-monitor-campaigns.md).

* **het monitoringsalarm van het Systeem** (die op deze pagina wordt gedetailleerd): Ontvang pro-actieve berichten wanneer de operationele drempels worden overschreden of de kwesties in levende reizen en kanaalconfiguraties worden ontdekt. Deze waarschuwingen helpen u snel op potentiële problemen te antwoorden alvorens zij uw klantenervaringen beïnvloeden.

Systeemwaarschuwingen zijn beschikbaar in het menu **[!UICONTROL Alerts]** onder **[!UICONTROL Administration]** . Adobe Experience Platform biedt verschillende vooraf gedefinieerde waarschuwingsregels die u kunt inschakelen, waaronder [!DNL Adobe Journey Optimizer] -specifieke waarschuwingen voor reizen en kanaalconfiguraties.

## Vereisten

Voordat u gaat werken met waarschuwingen:

* **Toestemmingen**: U hebt specifieke toestemmingen nodig om alarm te bekijken en te leiden. Zie [&#x200B; vereiste toestemmingen in Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html#permissions){target="_blank"}.

* **het bewustzijn van Sandbox**: De alarm abonnementen zijn zandbak-specifiek. Wanneer u zich abonneert op waarschuwingen, zijn deze alleen van toepassing op de huidige sandbox. Wanneer een sandbox opnieuw wordt ingesteld, worden ook alle waarschuwingsabonnementen opnieuw ingesteld.

* **voorkeur van het Bericht**: Vorm hoe u alarm (e-mail en/of in-app) in uw [&#x200B; Voorkeur van Adobe Experience Cloud &#x200B;](../start/user-interface.md#in-product-uc) ontvangt.

>[!NOTE]
>
>Journey Optimizer-specifieke alarm is slechts op **levende** reizen van toepassing. Er worden geen waarschuwingen gegeven voor reizen in testmodus. Voor meer informatie over het waakzame kader, zie de [&#x200B; het alarm van Adobe Experience Platform documentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html){target="_blank"}.

## Beschikbare waarschuwingen

Als u waarschuwingen wilt openen, navigeert u naar **[!UICONTROL Administration]** > **[!UICONTROL Alerts]** in het linkermenu. Het **doorbladert** lusje toont alle pre-gevormde alarm beschikbaar voor Journey Optimizer.

![](assets/updated-alerts-list.png){width=50%}

Journey Optimizer biedt twee categorieën systeemwaarschuwingen:

**het alarm van de Reis** - de uitvoering en de prestaties van de reis van de monitor:

* [&#x200B; las de Trekker van het Publiek Onsuccesvol &#x200B;](#alert-read-audiences) - waarschuwt wanneer een Gelezen activiteit van het Publiek geen profielen verwerkt
* [&#x200B; het Tarief van de Fout van de Actie van de Douane overschreden &#x200B;](#alert-custom-action-error-rate) - ontdekt hoge foutenpercentages in de vraag van douaneAPI van de Actie (vervangt het vorige Falen van de Actie van de Douane van de Reis)
* [&#x200B; Profiel verwerpt Tarief dat &#x200B;](#alert-discard-rate) wordt overschreden - identificeert wanneer de profielen aan een abnormaal tarief worden verworpen
* [&#x200B; het Tarief van de Fout van het Profiel overtrok &#x200B;](#alert-profile-error-rate) - Vlaggen wanneer de profielen fouten tijdens reisuitvoering ontmoeten
* [&#x200B; Gepubliceerde Reis &#x200B;](#alert-journey-published) - Informatief bericht wanneer een reis wordt gepubliceerd
* [&#x200B; Reis die &#x200B;](#alert-journey-finished) wordt geëindigd - Informatief bericht wanneer een reis voltooit
* [&#x200B; Gegrafeerde het In kaart brengen van de Actie van de Douane &#x200B;](#alert-custom-action-capping) - Meldt wanneer de grenzen van de API vraag worden bereikt

**de configuratiealarm van het Kanaal** - ontdek kwesties met de opstelling van de e-maillevering:

* [&#x200B; DNS van het Domein van AJO ontbreekt &#x200B;](#alert-dns-record-missing) - identificeert ontbrekende of onjuist gevormde DNS verslagen
* [&#x200B; de mislukking van de kanaalconfiguratie van AJO &#x200B;](#alert-channel-config-failure) - ontdekt de kwesties van de e-mailconfiguratie (SPF, DKIM, MX verslagen)
  <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

>[!NOTE]
>
>Voor alarm van andere diensten van Adobe Experience Platform (gegevensopname, identiteitsresolutie, segmentatie, en meer), zie de [&#x200B; standaarddocumentatie van de waakzame regels &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html){target="_blank"}.

## Abonneren op waarschuwingen {#subscribe-alerts}

Waarschuwingsmeldingen worden verzonden naar gebruikers die zich op hen hebben geabonneerd wanneer aan specifieke voorwaarden is voldaan (zoals drempelwaarden die worden overschreden of configuratieproblemen die worden gedetecteerd).

U kunt zich op twee manieren abonneren op waarschuwingen:

* **[Globaal abonnement](#global-subscription)**: Is op alle reizen en campagnes in de huidige zandbak van toepassing
* **[Reis-specifiek abonnement](#unitary-subscription)**: Is slechts op individuele reizen van toepassing

**hoe de waakzame berichten werken:**

* **de kanalen van de Levering**: De alarm wordt verzonden via e-mail en/of in-app berichten in het het berichtcentrum van Journey Optimizer (belpictogram in de hoger-juiste hoek). Vorm uw aangewezen leveringskanalen in uw [&#x200B; Voorkeur van Adobe Experience Cloud &#x200B;](../start/user-interface.md#in-product-uc).

* **de types van Alarm**: Journey Optimizer verstrekt zowel éénmalige alarm (informatiegebeurtenissen zoals gepubliceerde reis) als herhalend alarm (controledrempels). Herhalende waarschuwingen blijven bestaan totdat de voorwaarde is opgelost.

* **Resolutie**: Wanneer een waakzame voorwaarde wordt opgelost, ontvangen de abonnees een &quot;Opgelost&quot;bericht. Om berichtvermoeidheid te voorkomen die waarden fluctueert, worden waarschuwingen automatisch na 1 uur opgelost, zelfs als de voorwaarde aanhoudt.

Voor informatie over het intekenen via Gebeurtenissen I/O, zie de [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}.


### Globaal abonnement {#global-subscription}

Met wereldwijde abonnementen kunt u waarschuwingen ontvangen voor alle reizen en campagnes in de huidige sandbox.

**om aan een alarm in te tekenen:**

1. Navigeer naar **[!UICONTROL Administration]** > **[!UICONTROL Alerts]** in het linkermenu.

1. Zoek op het tabblad **[!UICONTROL Browse]** de waarschuwing die u wilt controleren.

1. Klik op **[!UICONTROL Subscribe]** voor de gewenste waarschuwing.

   ![&#x200B; het Abonneren aan een alarm &#x200B;](assets/alert-subscribe.png){width=80%}

**om af te melden:**

Klik op **[!UICONTROL Unsubscribe]** naast de waarschuwing.

>[!IMPORTANT]
>
>Waarschuwingsabonnementen zijn specifiek voor een sandbox. U moet zich afzonderlijk abonneren op waarschuwingen in elke sandbox waarin u meldingen wilt ontvangen.

**Alternatieve abonnementsmethode:**

U kunt ook via [&#x200B; I/O de berichten van de Gebeurtenis &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"} intekenen, die integratie met externe systemen toestaat. De namen van het abonnement van de gebeurtenis voor het alarm van Journey Optimizer worden vermeld in elk [&#x200B; waakzame beschrijving hieronder &#x200B;](#journey-alerts).

### Reisspecifiek abonnement {#unitary-subscription}

Met reisspecifieke abonnementen kunt u afzonderlijke reizen met hoge prioriteit volgen zonder dat u waarschuwingen ontvangt voor alle reizen in uw organisatie.

**om op alarm voor een specifieke reis in te tekenen:**

1. Ga naar de reisvoorraad.

1. Klik op het menu **⋯** (Meer handelingen) voor de reis die u wilt controleren.

1. Selecteer **[!UICONTROL Subscribe to alerts]**.

   ![&#x200B; het Abonneren aan een alarm voor een specifieke reis &#x200B;](assets/subscribe-journey-alert.png){width=75%}

1. Selecteer de waarschuwing(en) die u wilt inschakelen uit de beschikbare opties:
   * [Profielverwijderingsfrequentie overschreden](#alert-discard-rate)
   * [Foutsnelheid aangepaste handeling overschreden](#alert-custom-action-error-rate)
   * [Foutsnelheid profiel overschreden](#alert-profile-error-rate)
   * [Reis gepubliceerd](#alert-journey-published)
   * [Reis voltooid](#alert-journey-finished)
   * [Aangepaste actiekoppeling geactiveerd](#alert-custom-action-capping)

1. Klik op **[!UICONTROL Save]** om uw abonnementen te bevestigen.

**om af te melden:**

Open hetzelfde dialoogvenster, deselecteer de waarschuwing(en) en klik op **[!UICONTROL Save]** .

>[!NOTE]
>
>Het [&#x200B; Gelezen Gevonden &#x200B;](#alert-read-audiences) alarm van de Trekker van het Publiek is slechts beschikbaar door globaal abonnement, niet per-reis abonnement.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## Reiswaarschuwingen {#journey-alerts}


Alle reisberichten die beschikbaar zijn in de gebruikersinterface worden hieronder vermeld.

>[!CAUTION]
>
>Het specifieke alarm van Adobe Journey Optimizer is slechts op **levende** reizen van toepassing. Er worden geen waarschuwingen gegeven voor reizen in testmodus.

### Trigger voor publiek lezen is mislukt {#alert-read-audiences}

Dit alarm waarschuwt u als de a **Gelezen activiteit van het publiek** geen profiel 10 min na geplande tijd van uitvoering heeft verwerkt. Deze fout kan worden veroorzaakt door technische problemen, of omdat het publiek leeg is. Als deze fout door technische problemen wordt veroorzaakt, moet u er rekening mee houden dat er nog steeds pogingen kunnen worden gedaan, afhankelijk van het type probleem (bijvoorbeeld: als het aanmaken van exportarbeidsplaatsen is mislukt, proberen we elke 10 miljoen opnieuw gedurende maximaal 1 uur).

Het alarm op **Gelezen de activiteiten van het publiek** zijn slechts op terugkomende reizen van toepassing. **las de activiteiten van het publiek** in levende reizen die een programma hebben om **in werking te stellen** of **zodra mogelijk** wordt genegeerd.

Het alarm op **Gelezen Publiek** wordt opgelost wanneer een profiel de **Gelezen knoop van het Publiek**, of na 1 uur ingaat.

De I/O naam van het gebeurtenisabonnement die aan **beantwoordt las de Trekker van het Publiek Onsuccesvol** alarm is **Reis leest publieksvertragingen, Mislukkingen en Fouten**.

Om **te problemen op te lossen leest het 1&rbrace; alarm van het publiek &lbrace;, controleer uw publiekstelling in de interface van Experience Platform.**

### Profielverwijderingsfrequentie overschreden {#alert-discard-rate}

In deze waarschuwing wordt u gewaarschuwd als de verhouding tussen het profiel en de ingevoerde profielen in de afgelopen 5 minuten de drempel overschrijdt. De standaarddrempel wordt geplaatst aan 20% maar u kunt [&#x200B; een douanedrempel &#x200B;](#custom-threshold) bepalen.

Klik de naam van het alarm om de waakzame details en configuratie te controleren.

![](assets/profile-discard-alert.png)

Er zijn verscheidene redenen een profiel kon worden verworpen, dat de methode van het oplossen van problemen zal informeren. Hieronder volgen enkele algemene redenen:

* Profiel dat bij binnenkomst is weggegooid omdat het al in die eenheidsreis woont. Om dit op te lossen, zorg ervoor dat het profiel genoeg tijd heeft om de reis weg te gaan alvorens de volgende gebeurtenis voor dat profiel aankomt.
* Identiteit is niet ingesteld voor het profiel of de naamruimte die wordt gebruikt door de reis van het leespubliek wordt niet gebruikt in dat profiel. Om dit op te lossen, zorg ervoor dat namespace in de reis de identiteitsnamespace aanpast die door de profielen wordt gebruikt.
* Doorvoersnelheid van gebeurtenis wordt overschreden. Om dit op te lossen, moet ervoor worden gezorgd dat gebeurtenissen die in het systeem komen deze grenzen niet overschrijden.


### Foutsnelheid aangepaste handeling overschreden {#alert-custom-action-error-rate}

Deze waarschuwing waarschuwt u als de verhouding van de fouten van de douaneactie aan succesvolle vraag van HTTP de laatste 5 minuten overschrijdt drempel. De standaarddrempel wordt geplaatst aan 20% maar u kunt [&#x200B; een douanedrempel &#x200B;](#custom-threshold) bepalen.

>[!NOTE]
>
>Dit alarm vervangt het vorige **alarm van de Actie van de Douane van de 1&rbrace; Reis.**

Klik de naam van het alarm om de waakzame details en configuratie te controleren.

Fouten in aangepaste handelingen kunnen om verschillende redenen optreden. Als u deze fouten wilt oplossen, kunt u:

* Controleer uw douaneactie gebruikend [&#x200B; testwijze &#x200B;](../building-journeys/testing-the-journey.md) op een andere reis.
* Controleer uw [&#x200B; reisrapport &#x200B;](../reports/journey-live-report.md) om foutenredenen op actie te zien.
* Controleer uw reis stepEvents om naar meer informatie rond &quot;failureReason&quot; te zoeken.
* Controleer of de aangepaste handeling correct is geconfigureerd en bevestig dat de verificatie nog steeds geldig is. Voer bijvoorbeeld een handmatige controle uit met Postman.
* Controleer dat het eindpunt bereikbaar is en de douaneactie het via de controle van de douaneactieconnectiviteit kan bereiken.
* Verifieer de verificatiereferenties, controleer de internetverbinding, enz.

### Foutsnelheid profiel overschreden {#alert-profile-error-rate}

In deze waarschuwing wordt u gewaarschuwd als de verhouding tussen profielen in fout en ingevoerde profielen in de afgelopen 5 minuten de drempel overschrijdt. De standaarddrempel wordt geplaatst aan 20% maar u kunt [&#x200B; een douanedrempel &#x200B;](#custom-threshold) bepalen.

Klik de naam van het alarm om de waakzame details en configuratie te controleren.

Om profielfout problemen op te lossen, kunt u de gegevens in stapgebeurtenissen vragen om te begrijpen waar en waarom het profiel in de reis ontbrak.

### Reis gepubliceerd {#alert-journey-published}

Deze waarschuwing brengt u op de hoogte wanneer een reis door een arts op het reiscanvas is gepubliceerd.

Dit is een informatieve waarschuwing die u helpt de gebeurtenissen van de reis levenscyclus in uw organisatie te volgen. Er zijn geen resolutiecriteria, aangezien dit een eenmalige kennisgeving is.

### Reis voltooid {#alert-journey-finished}

Deze waarschuwing brengt u op de hoogte wanneer een reis is gebeëindigd. De definitie van &quot;voltooid&quot; varieert afhankelijk van het type transport. [&#x200B; leer meer over wanneer de reizen als gebeëindigd &#x200B;](../building-journeys/end-journey.md#journey-finished-definition) worden beschouwd.

Dit is een informatieve waarschuwing die u helpt bij het volgen van de voltooiing van de reis. Er zijn geen resolutiecriteria, aangezien dit een eenmalige kennisgeving is.

### Aangepaste actiekoppeling geactiveerd {#alert-custom-action-capping}

Deze waarschuwing geeft een waarschuwing wanneer een aangepaste handeling tot het vastzetten van de afbeelding heeft geleid. Het in kaart brengen wordt gebruikt om het aantal vraag te beperken die naar een extern eindpunt wordt verzonden om overweldigend het eindpunt te verhinderen.

Klik de naam van het alarm om de waakzame details en configuratie te controleren.

Wanneer het begrenzen wordt teweeggebracht, betekent het dat het maximumaantal API vraag binnen de bepaalde tijdspanne is bereikt, en verdere vraag wordt vertraagd of een rij gevormd. Leer meer over het aftappen op douaneacties op [&#x200B; deze pagina &#x200B;](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices).

Deze waarschuwing wordt opgelost wanneer het maximum niet meer actief is, of wanneer geen profielen de douaneactie tijdens de evaluatieperiode bereiken.

U kunt als volgt problemen met de begrenzing oplossen:

* Controleer de configuratie van het maximum op uw douaneactie om de grenzen voor uw gebruiksgeval te verzekeren.
* Controleer of het volume van API-aanroepen hoger is dan verwacht en denk na of u het reisontwerp of de instellingen voor aftopping wilt aanpassen.
* Controleer het externe eindpunt om ervoor te zorgen het de verwachte lading kan behandelen.

## Configuratiewaarschuwingen {#configuration-alerts}

De waarschuwingen voor de bewaking van kanaalconfiguraties die beschikbaar zijn in de gebruikersinterface worden hieronder weergegeven.

### AJO Domain DNS-record ontbreekt {#alert-dns-record-missing}

Dit alarm brengt u op de hoogte wanneer de kritieke DNS verslagen (NS of CNAME) die voor juiste leveringsconfiguratie worden vereist ontbreken of misconfigured zijn. Zonder deze records kan de e-mailleverbaarheid in het gedrang komen.

>[!NOTE]
>
>* NS-records zijn essentieel voor volledige subdomeindelegatie naar Adobe. [Meer informatie](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME-records ondersteunen CNAME-subdomeininstelling. [Meer informatie](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

Het **DNS van het Domein van AJO DNS verslag missen** alarm wordt teweeggebracht wanneer het systeem ontdekt dat de vereiste NS of CNAME verslagen afwezig zijn of niet de configuratienormen aanpassen.

1. Klik het alarm dat aan beïnvloede [&#x200B; subdomain &#x200B;](../configuration/delegate-subdomain.md) in de [!DNL Journey Optimizer] interface moet worden geleid.

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Verbeter de DNS configuratie door de verslagen correct te plaatsen en [&#x200B; voorlegt opnieuw subdomain &#x200B;](../configuration/delegate-subdomain.md#submit-subdomain) delegatie.

   >[!NOTE]
   >
   >Zorg ervoor dat alle verslagen behoorlijk op uw domein het ontvangen oplossing alvorens te werk te gaan worden gecreeerd.

1. Als u niet zeker bent van de juiste waarden, kunt u een nieuw subdomein maken in [!DNL Journey Optimizer] met dezelfde naam als het subdomein waarop het effect is toegepast. [&#x200B; leer hoe te opstelling een nieuw subdomain &#x200B;](../configuration/delegate-subdomain.md#set-up-subdomain)

Als de wijzigingen het probleem niet verhelpen, wordt dezelfde waarschuwing de volgende dag opnieuw geactiveerd.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### AJO-kanaalconfiguratiefout {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Dit alarm is slechts op **e-mail** kanaalconfiguraties van toepassing gebruikend het [&#x200B; type van de douanesubdomain &#x200B;](../configuration/delegate-custom-subdomain.md) delegatie. <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Deze waarschuwing wordt geactiveerd als de systeemcontrole problemen met de configuratie van het e-mailkanaal detecteert. Deze kwesties kunnen misconfigured kanaalmontages, ongeldige DNS configuratie, de kwestie van de suppressielijst, IP inconsistentie, of een andere fouten omvatten die e-maillevering kunnen beïnvloeden.

Als u een dergelijke waarschuwing ontvangt, worden de resolutiestappen hieronder weergegeven:

1. Klik het alarm dat aan de beïnvloede [&#x200B; configuratie van het e-mailkanaal &#x200B;](../email/get-started-email-config.md) in de [!DNL Journey Optimizer] interface moet worden geleid.

   Voor begeleiding bij het uitgeven van kanaalconfiguraties, zie [&#x200B; deze sectie &#x200B;](../configuration/channel-surfaces.md#edit-channel-surface).

1. Bekijk de configuratiegegevens en de foutberichten die u hebt ontvangen. Vaak voorkomende oorzaken van falen zijn:

   * Validatie van SPF is mislukt
   * Validatie van DKIM is mislukt
   * Validatie van MX-record mislukt
   * Ongeldige DNS-records

   >[!NOTE]
   >
   >De mogelijke redenen van de configuratiefout zijn vermeld in [&#x200B; deze sectie &#x200B;](../configuration/channel-surfaces.md).

1. Los het probleem op:

   * Werk indien nodig de kanaalconfiguratie bij.
   * Mogelijk moet u specifieke DNS-problemen oplossen die in de waarschuwing worden vermeld.

   >[!NOTE]
   >
   >Aangezien één enkel domein met veelvoudige kanaalconfiguraties kan worden geassocieerd, kan het oplossen van DNS kwesties voor één kanaalconfiguratie verwante kwesties over verscheidene configuraties automatisch bevestigen.

Als de wijziging het probleem niet verhelpt, wordt dezelfde waarschuwing de volgende dag opnieuw geactiveerd.

Houd bij het oplossen van problemen met de e-mailconfiguratie rekening met de onderstaande aanbevolen procedures:

* Reageer onmiddellijk - De configuratiefouten van de Adres zodra zij worden ontdekt om verstoringen in e-maillevering te vermijden.
* Controleer alle configuraties - Als in de waarschuwing meerdere van invloed zijnde e-mailconfiguraties worden aangegeven, controleert en corrigeert u deze.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## Waarschuwingen beheren {#manage-alerts}

### Een waarschuwing bewerken

U kunt de details van een alarm controleren door op zijn lijn te klikken. De naam, status en meldingskanalen worden weergegeven in het linkerdeelvenster.
Voor Reis-waarschuwingen gebruikt u de knop **[!UICONTROL More actions]** om deze te bewerken. U kunt a [&#x200B; douanedrempel &#x200B;](#custom-threshold) voor deze alarm dan bepalen.

![](assets/alert-more-actions.png){width=60%}

### Een aangepaste drempel definiëren {#custom-threshold}

U kunt drempels voor het [&#x200B; alarm van de Reis &#x200B;](#journey-alerts) plaatsen. De drempelwaarschuwingen boven de standaardwaarde is 20%.

De drempel wijzigen:

1. Doorblader aan het **Alarm** scherm
1. Klik op de knop **[!UICONTROL More actions]** van de waarschuwing die u wilt bijwerken
1. Voer de nieuwe drempelwaarde in en bevestig deze. De nieuwe drempel is op **van toepassing alle** reizen


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>De drempelwaarden zijn voor alle reizen wereldwijd en kunnen per reis niet afzonderlijk worden gewijzigd.

### Een waarschuwing uitschakelen

Standaard zijn alle waarschuwingen ingeschakeld. Als u een waarschuwing wilt uitschakelen, selecteert u de optie **[!UICONTROL Disable alert]** : alle abonnees van deze waarschuwing ontvangen de gerelateerde meldingen niet meer.


### Waarschuwingsstatussen

De mogelijke statussen voor waarschuwingen worden hieronder weergegeven:

* **[!UICONTROL Enabled]** - De waarschuwing is ingeschakeld en controleert momenteel de triggervoorwaarde.
* **[!UICONTROL Disabled]** - De waarschuwing is uitgeschakeld en controleert momenteel niet de triggervoorwaarde. U ontvangt geen meldingen voor deze waarschuwing.
* **[!UICONTROL Triggered]** - Er wordt momenteel voldaan aan de triggervoorwaarde van de waarschuwing.


### Abonnees weergeven en bijwerken {#manage-subscribers}

Selecteer **[!UICONTROL Manage alert subscribers]** om de lijst weer te geven met gebruikers die zich op de waarschuwing hebben geabonneerd.

![](assets/alert-subscribers.png){width=80%}

Als u meer abonnees wilt toevoegen, voert u hun e-mail gescheiden door een komma in en selecteert u **[!UICONTROL Update]** .

Als u abonnees wilt verwijderen, verwijdert u hun e-mailadres uit de huidige abonnees en selecteert u **[!UICONTROL Update]** .

## Aanvullende bronnen {#additional-resources-alerts}

* Leer hoe te om uw reizen op [&#x200B; problemen op te lossen deze pagina &#x200B;](../building-journeys/troubleshooting.md).
* Leer hoe te om uw campagnes op [&#x200B; te herzien deze pagina &#x200B;](../campaigns/review-activate-campaign.md).
