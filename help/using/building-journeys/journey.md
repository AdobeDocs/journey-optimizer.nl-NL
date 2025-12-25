---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met reizen
description: Aan de slag met reizen
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: reis, ontdek, begin
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 0%

---


# Aan de slag met reizen{#jo-general-principle}

De reizen in Adobe Journey Optimizer stellen u in staat om persoonlijke, uit meerdere stappen bestaande klantritten te maken die zich in real time aanpassen aan het gedrag en de behoeften van uw publiek. Met een intuïtief canvas voor slepen en neerzetten kunt u berichten en acties op meerdere kanalen ordenen, waarbij gebruik wordt gemaakt van contextafhankelijke gegevens en doelgroepen voor maximale impact. Of u in real time trekkers onderzoekt, het beheren van reiseigenschappen, of het gebruiken van geavanceerde hulpmiddelen zoals douaneacties en uitdrukkingen, deze sectie verstrekt een duidelijke roadmap om u te helpen reizen ontwerpen en verfijnen die betekenisvolle, geschikte klantenervaringen leveren.

Gebruik [!DNL Journey Optimizer] om in real time orchestratiefase samen te stellen met gebruik van contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen. U kunt meerdere stappen geavanceerde scenario&#39;s met de volgende mogelijkheden ontwerpen:

* Verzend in real time **unitaire levering** teweeggebracht wanneer een [&#x200B; gebeurtenis &#x200B;](general-events.md) wordt ontvangen, of **in partij** gebruikend Adobe Experience Platform [&#x200B; publiek &#x200B;](read-audience.md).

* Hefboomwerking **contextafhankelijke gegevens** van [&#x200B; gebeurtenissen &#x200B;](../event/about-events.md), informatie van Adobe Experience Platform, of gegevens van de diensten van derdeAPI door [&#x200B; gegevensbronnen &#x200B;](../datasource/about-data-sources.md).

* Gebruik **[ingebouwde acties](journeys-message.md)** om berichten te verzenden die in [!DNL Journey Optimizer] worden ontworpen of **[douaneacties](using-custom-actions.md)** tot stand te brengen als u een derdesysteem gebruikt om uw berichten te verzenden.

* Met de **[reisontwerper](using-the-journey-designer.md)**, bouwt uw multi-step gebruiksgevallen: belemmering en laat vallen gemakkelijk een ingangsgebeurtenis of a [&#x200B; gelezen publieksactiviteit &#x200B;](read-audience.md), voeg [&#x200B; voorwaarden &#x200B;](condition-activity.md) toe en verzend gepersonaliseerde berichten.

➡️ [&#x200B; ontdekt Journey Optimizer in video &#x200B;](#video)

## Overzicht van reizen

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Aan de slag met het maken van reizen

Stapsgewijze begeleiding bij het ontwerpen, testen, publiceren en volgen van klantentreizen om gepersonaliseerde omnichannel campagnes te bouwen.

[Uw eerste journey maken](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Journey Orchestration - Volledige handleiding

Uitgebreide documentatie die alle aspecten van het creëren, beheren en optimaliseren van reizen in Adobe Journey Optimizer bestrijkt.

[De volledige handleiding verkennen](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Uw reizen beheren

Beheer klantritten efficiënt met hulpmiddelen voor het filtreren, profielbeheer, tijdzones, en optimalisatietechnieken.

[Meer informatie over reisbeheer](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

Reisactiviteiten

Ontdek hoe u activiteiten zoals triggers, beslissingsstappen, publieksbeheer en gepersonaliseerde berichten tijdens reizen kunt configureren en gebruiken.

[Activiteiten verkennen](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Expressies maken

Masterexpressies maken voor dynamische workflows, gegevensmanipulatie en geavanceerde reisorganisatie met krachtige gereedschappen en syntaxis.

[Meer informatie over expressies](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Gevallen voor gebruik tijdens reizen

Verken real-world toepassingen van Adobe Journey Optimizer, met inbegrip van multi-channel overseinen en integratie met externe systemen.

[Gebruiksgevallen ontdekken](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Wat kan je doen met reizen?

Van binnen de reisontwerper, kunnen de marketers in real time teweeggebrachte 1 :1 berichten door om het even welk kanaal verzenden wanneer een gebeurtenis voorkomt. Bijvoorbeeld, wanneer een klant aan de dienst intekent, kan het [&#x200B; welkome e-mail &#x200B;](message-to-subscribers-uc.md) teweegbrengen, die hen aanmoedigen om in app voor het eerst te registreren en hun voorkeur te plaatsen. Handelingen als het voltooien van de aankoop, het openen van de e-mail en het aanmelden bij de app kunnen worden gebruikt om nieuwe klanten door hun reizen te leiden.

## Soorten reizen

Adobe Journey Optimizer ondersteunt vier reistypes, elk ontworpen voor verschillende gebruiksgevallen en toegangsmechanismen. Kies het juiste type op basis van de manier waarop u wilt dat profielen worden ingevoerd en dat de ervaringen van uw klanten doorlopen.

>[!BEGINTABS]

>[!TAB  Eenheids reizen ]

**de uniale reizen** worden teweeggebracht individueel door een gebeurtenis wanneer een specifieke actie, zoals een aankoop, app aanmelding, of vormvoorlegging voorkomt. Profielen gaan één voor één de reis in real time in wanneer de gebeurtenis wordt ontvangen, die dit ideaal voor gepersonaliseerde, op gedrag-gedreven ervaringen maken.

**Zeer belangrijke kenmerken:**

* Real-time, gebeurtenisgestuurde toegang
* Afzonderlijke profielverwerking
* Ideaal voor transactieberichten en directe reacties
* Ondersteunt contextafhankelijke gegevens van de activerende gebeurtenis

**gevallen van het Gebruik:**

* Bevestiging van bestelling na aankoop
* Welkomstbericht wanneer iemand zich abonneert
* Opzegging van winkelwagentje geactiveerd door het bladergedrag
* Meldingen voor opnieuw instellen van wachtwoord

➡️ [&#x200B; Leer over gebeurtenisconfiguratie &#x200B;](../event/about-events.md) | [&#x200B; Algemene gebeurtenissen &#x200B;](general-events.md) | [&#x200B; Bericht aan abonnees gebruikt geval &#x200B;](message-to-subscribers-uc.md)

>[!TAB  lees de reizen van het Publiek ]

**lees de reizen van het Publiek** beginnen met een publiek van Adobe Experience Platform en verzendt berichten in partij naar alle profielen in dat publiek. Dit type van reis verwerkt het volledige publiek in één keer, die het voor geplande campagnes en terugkomende mededelingen ideaal maken.

**Zeer belangrijke kenmerken:**

* Batchverwerking van publiekssegmenten
* Geplande of eenmalige uitvoering
* Alle profielen worden tegelijk ingevoerd
* Ondersteunt grootschalige communicatie

**gevallen van het Gebruik:**

* Maandelijkse nieuwsbrieven
* Promotiecampagnes voor doelsegmenten
* Aankondigingen van producten aan alle klanten
* Seizoensgebonden marketingcampagnes

➡️ [&#x200B; Leer over Gelezen activiteit van het Publiek &#x200B;](read-audience.md) | [&#x200B; krijgen begonnen met publiek &#x200B;](../audience/about-audiences.md) | [&#x200B; Gebruiksgeval van het multi-kanaaloverseinen &#x200B;](journeys-uc.md)

>[!TAB  reizen van de Kwalificatie van het publiek ]

{de reizen van de Kwalificatie van het publiek 0} **worden teweeggebracht wanneer de profielen voor (of uitgang uit) een specifiek publiekssegment kwalificeren.** Profielen gaan de reis individueel in aangezien zij aan de publiekscriteria in real time voldoen, toelatend directe betrokkenheid wanneer het gedrag van de klant verandert.

**Zeer belangrijke kenmerken:**

* In real time op kwalificatie-gebaseerde ingang
* Voortdurende monitoring van het lidmaatschap van de doelgroep
* Individuele profielverwerking omdat deze in aanmerking komen
* Best met streaming publiek

**gevallen van het Gebruik:**

* VIP-upgrademeldingen
* Opnieuw in dienst nemen wanneer klanten inactief worden
* Eerste berichten voor aankoopfeest
* Geografisch doel wanneer klanten verhuizen

➡️ [&#x200B; Leer over de Kwalificatie van het Publiek &#x200B;](audience-qualification-events.md) | [&#x200B; de activiteit van de Voorwaarde &#x200B;](condition-activity.md) | [&#x200B; Creërend segmentdefinities &#x200B;](../audience/creating-a-segment-definition.md)

>[!TAB  Van bedrijfs gebeurtenisreizen ]

&lbrace;de ritten van de Bedrijfs gebeurtenis **worden teweeggebracht door bedrijfsgebeurtenissen (zoals voorraadupdates, weeralarm, of prijsveranderingen) die veelvoudige profielen gelijktijdig beïnvloeden.** In plaats van op individuele acties van klanten te reageren, reageren deze reizen op bredere bedrijfsvoorwaarden of externe factoren.

**Zeer belangrijke kenmerken:**

* Wordt geactiveerd door gebeurtenissen op bedrijfsniveau, niet door afzonderlijke acties
* Beïnvloedt meerdere profielen tegelijk
* Hiermee wordt een specifiek publiek aangewezen wanneer de gebeurtenis plaatsvindt
* Combineert gebeurtenisgestuurde timing met doelgerichtheid

**gevallen van het Gebruik:**

* Lage inventariswaarschuwingen aan geïnteresseerde klanten
* Aankondigingen Flash-verkoop
* Op weersomstandigheden gebaseerde promoties
* Prijsdalingsberichten
* Waarschuwing over back-in-stock van producten

➡️ [&#x200B; Leer over bedrijfsgebeurtenissen &#x200B;](general-events.md) | [&#x200B; vorm bedrijfsgebeurtenissen &#x200B;](../event/about-creating-business.md) | [&#x200B; Invoerbeheer &#x200B;](entry-management.md)

>[!ENDTABS]

## Journey Designer{#journey-designer}

De [&#x200B; reisontwerper &#x200B;](using-the-journey-designer.md) verstrekt alles Marketers en de reisartsen moeten multi-step 1 :1 reizen over kanalen organiseren. Dit omvat een intuïtief belemmering-en-dalingscanvas om elke stap van de reis te ordenen, het doelpubliek te bepalen, en de berichten, de aanbiedingen, en de inhoud te omvatten over kanalen die doelpublieksleden gebaseerd op gedrag, contextuele gegevens, en bedrijfsgebeurtenissen zullen zien.

De reisontwerper verstrekt alles u moet ontwerpen multi-step ervaringen:

* **[Ingebouwde kanaalacties](journeys-message.md)** - verzend berichten door e-mail, dupberichten, SMS/MMS, in-app, Web, code-gebaseerde ervaringen, en meer, allen die direct binnen Journey Optimizer worden ontworpen
* **[de acties van de Douane](using-custom-actions.md)** - integreer derdesystemen om berichten te verzenden of werkschema&#39;s in externe platforms teweeg te brengen
* **[de activiteiten van het Orchestration](about-journey-activities.md)** - voeg logica, voorwaarden, wachttijden, en publiek toe richtend om verfijnde klantenervaringen te creëren
* **[Voorwaarden](condition-activity.md)** - Tak uw reis die op profielattributen, publiekslidmaatschap, of gebeurtenissen in real time wordt gebaseerd
* **[Uitdrukkingen](expression/expressionadvanced.md)** - Bouw geavanceerde logica en verpersoonlijking gebruikend de uitdrukkingsredacteur

Leer hoe te om de reisontwerper [&#x200B; in deze gebruiksgevallen van begin tot eind te gebruiken &#x200B;](jo-use-cases.md).

>[!NOTE]
>
>De de gidsen en beperkingen van de reis zijn gedetailleerd op [&#x200B; deze pagina &#x200B;](../start/guardrails.md)

## Hoe kan ik-video {#video}

Ontdek de onderdelen van een reis en begrijp de grondbeginselen van het maken van een reis op het canvas.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## Aanvullende bronnen {#additional-resources}

* **[de Reizen van de Klant van het oplossen van problemen](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnose en los kwesties van de reisuitvoering met hulpmiddelen, foutencodes, en beste praktijken voor het zuiveren en optimaliseren op
* **[Veelgestelde vragen van de Reis](journey-faq.md)** - Veelgestelde vragen over reizen
* **[Waarschuwingen van de Reis](../reports/alerts.md)** - De alarm van de opstelling voor reis controle en tekent aan berichten voor updates in real time in
* **[Verwijzing van de codes van de Fout](error-codes-reference.md)** - de codes van de de foutenfout van de Reis en het oplossen van problemenstappen
* **[het Oplossen van problemen](troubleshooting.md)** - Gemeenschappelijke reiskwesties en oplossingen
* **[Zelfstudies van de Reis (video&#39;s) &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - leer reis die door hands-on videoleerprogramma&#39;s bouwt die eigenschappen, mogelijkheden, en beste praktijken behandelen
