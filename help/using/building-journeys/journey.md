---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met reizen
description: Aan de slag met reizen - Meer informatie over soorten reizen, workflows, mogelijkheden en beste praktijken voor het creëren van persoonlijke klantervaringen in Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: reis, ontdek, get-start, unitary, read publiek, publiekskwalificatie, bedrijfsgebeurtenis, real time, gepland, partij, gebeurtenis-teweeggebracht, werkschema, orchestratie, personalisatie, multi-channel
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---


# Aan de slag met reizen{#jo-general-principle}

Met Adobe Journey Optimizer kunt u persoonlijke, uit meerdere stappen bestaande klantritten maken die zich in real-time aanpassen aan het gedrag en de behoeften van uw publiek. Met een intuïtief canvas voor slepen en neerzetten kunt u berichten en acties op meerdere kanalen ordenen, waarbij gebruik wordt gemaakt van contextafhankelijke gegevens en doelgroepen voor maximale impact.

Deze gids verstrekt een duidelijke routekaart om u te helpen de grondbeginselen van de reis begrijpen, het juiste reistype voor uw gebruiksgeval kiezen, en betrouwbaar ontwerpt reizen die betekenisvolle, geschikte klantenervaringen leveren.

## Wat zijn reizen?

**de Reizen** zijn geautomatiseerde, multi-step klantenervaringen die gepersonaliseerde interactie over kanalen in antwoord op klantengedrag, bedrijfsgebeurtenissen, of geplande campagnes organiseren.

Gebruik [!DNL Journey Optimizer] om:

* Bouw **gebruiksgevallen in real time van het orkestgebruik** gebruikend contextafhankelijke gegevens die in gebeurtenissen of gegevensbronnen worden opgeslagen
* Ontwerp **multistep geavanceerde scenario&#39;s** die dynamisch aan klantengedrag en bedrijfsgebeurtenissen antwoorden
* Lever **1 :1 gepersonaliseerde ervaringen** bij schaal over e-mail, duw, SMS, in-app, Web, en meer

![&#x200B; de ontwerperinterface van de Reis met palet, canvas, en eigenschappenruit &#x200B;](assets/journey38.png)

➡️ **Klaar om te beginnen met bouwen?** [&#x200B; creeer uw eerste reis &#x200B;](journey-gs.md) in 5 minuten.

### Reizen vs. campagnes: Wanneer gebruiken {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer biedt drie benaderingen aan om klanten te bereiken: **(1** Reis in real time orchestratie), :1 Campagnes **(eenvoudige partij of API-teweeggebrachte levering), en** Geordende Campagnes **(de werkschema&#39;s van het partijcanvas met multi-entiteitgegevens).**

**Snelle beslissing:**

* Gebruik **Reizen** voor multi-stap, gedrag-gedreven ervaringen waar elke klant bij hun eigen tempo vordert
* De Campagnes van de Actie/API van het gebruik **voor eenvoudige, geplande of teweeggebrachte berichtlevering aan publiek**
* Gebruik **Geordende Campagnes** voor complexe partijwerkschema&#39;s die multi-entiteitsegmentatie en nauwkeurige pre-send tellingen vereisen

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Kies uw type reis {#journey-types}

Adobe Journey Optimizer ondersteunt vier soorten reizen, elk ontworpen voor verschillende toegangsmechanismen en bedrijfsscenario&#39;s:

* **Unitaire reizen**: In real time, gebeurtenis-teweeggebrachte ervaringen (ordesbevestigingen, welkome e-mails)
* **las de reizen van het Publiek**: Geplande partijmededelingen aan publiekssegmenten (nieuwsbrieven, promotiecampagnes)
* **reizen van de Kwalificatie van het publiek**: Reacties in real time op de veranderingen van het publiekslidmaatschap (verbeteringen van VIP, re-engagement)
* **Van Bedrijfs gebeurtenis reizen**: Bedrijfs voorwaarden die veelvoudige klanten beïnvloeden (inventarisalarm, flitsverkoop)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Bouw met de reisontwerper {#journey-designer}

De **[reisontwerper](using-the-journey-designer.md)** is uw visueel canvas voor het creëren van klantenervaringen. Met een intuïtieve drag-and-drop interface, kunt u elke stap van uw reis organiseren zonder code te schrijven.

![&#x200B; de ontwerperinterface van de Reis met palet, canvas, en eigenschappenruit &#x200B;](assets/journey38.png)

### Wat u in de ontwerper kunt doen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=nl-NL)

**bepaalt ingangspunten**

Kies hoe klanten ingaan: door een gebeurtenis, een publiekssegment, of een publiekskwalificatie.

[Meer informatie over entry-beheer](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=nl-NL)

**Berichten verzenden**

Gebruik ingebouwde kanaalacties voor e-mail, push, SMS/MMS, in-app, web en meer, allemaal ontworpen in Journey Optimizer.

[Berichten verzenden tijdens reizen](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=nl-NL)

**voeg logica &amp; voorwaarden** toe

Vertakken uw reis die op profielattributen, publiekslidmaatschap, of gebeurtenissen in real time wordt gebaseerd.

[Gebruiksvoorwaarden](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=nl-NL)

**gegevens van de Leverage**

Gebruik contextuele gegevens van gebeurtenissen, Adobe Experience Platform of externe API-services.

[Werken met gegevensbronnen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=nl-NL)

**verbindt externe systemen**

Aangepaste acties maken om systemen van derden te integreren voor het verzenden van berichten of het activeren van workflows.

[Aangepaste handelingen configureren](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=nl-NL)

**voeg orchestration activiteiten** toe

Gebruik wachttijden, sprongen, profielupdates en publieksbeheer om geavanceerde stromen te maken.

[Alle activiteiten verkennen](about-journey-activities.md)
:::

::::

➡️ **Hands-on het leren:** [&#x200B; bekijk de video van de reisontwerper &#x200B;](#video) of [&#x200B; onderzoek van begin tot eind gebruiksgevallen &#x200B;](jo-use-cases.md)

## Uw workflow voor het maken van reizen {#workflow}

De bouw van succesvolle reizen volgt een duidelijk, herhaalbaar proces. Dit is uw stapsgewijze workflow:

**1. Plan** → **2. Ontwerp** → **3. Test** → **4. Publiceer** → **5. Monitor** → **6. Optimaliseren**

### &#x200B;1. Plan uw reis {#plan}

Voordat u de ontwerper opent, moet u uw doelstellingen verduidelijken:

* **wat is het doel?** (bijvoorbeeld aan boord van nieuwe klanten, opnieuw inactieve gebruikers inschakelen)
* **Wie is het publiek?** (specifiek segment, gebeurtenisgestuurde personen)
* **Welk vervoerstype past?** (Zie [&#x200B; reistypes &#x200B;](#journey-types) hierboven)
* **Welke kanalen zult u gebruiken?** (e-mail, push, SMS, enz.)

### &#x200B;2. Ontwerp op het canvas {#design}

Gebruik de reisontwerper om uw stroom te bouwen:

* **vastgestelde ingangsvoorwaarden** - bepalen hoe de profielen ingaan (gebeurtenis, publiek, kwalificatie)
* **voeg orchestratielogica** toe - omvat wachttijden, voorwaarden, en besluitvormingspunten
* **vorm berichten** - Ontwerp uw mededelingen of hefboomwerking bestaande malplaatjes
* **de acties van de opstelling** - vorm ingebouwde of douaneacties om uit te voeren
* **bepaalt uitgangscriteria** - specificeer wanneer en hoe de profielen de reis voltooien

[Leer hoe u de reisontwerper → gebruikt](using-the-journey-designer.md)

### &#x200B;3. Testen vóór live gaan {#test}

Test altijd uw reis om kwesties te vangen alvorens de klanten hen ervaren:

* Gebruik **testwijze** om de reis met testprofielen te simuleren
* Gebruik **droge looppas** aan voorproefreis uitvoering zonder echte gegevens te beïnvloeden of berichten te verzenden
* Controleren of alle voorwaarden, berichten en handelingen naar behoren werken
* De timing, gegevensstromen, en verpersoonlijking van de controle

[&#x200B; test uw reis → &#x200B;](testing-the-journey.md) | [&#x200B; Leer over droge looppas → &#x200B;](journey-dry-run.md)

### &#x200B;4. Publiceer uw reis {#publish}

Als het testen is voltooid, publiceert u om uw reis live te maken:

* Definitieve instellingen en eigenschappen controleren
* Publiceren om te activeren voor echte klanten
* Opmerking: actieve reizen kunnen worden gestopt, maar niet worden bewerkt (u moet een nieuwe versie maken)

[Uw reis publiceren →](publish-journey.md)

### &#x200B;5. Monitorprestaties {#monitor}

Volg hoe je reis in de echte wereld presteert:

* Reisrapporten en analyses weergeven
* Het ingang, de voltooiing van de monitor, en foutenpercentages
* Waarschuwingen instellen voor kritieke problemen

[&#x200B; Monitor en rapport → &#x200B;](report-journey.md) | [&#x200B; opstelling alarm → &#x200B;](../reports/alerts.md)

### &#x200B;6. Optimaliseren en herhalen {#optimize}

Gebruik inzichten om te verbeteren:

* De betrokkenheidswaarden en conversiesnelheden analyseren
* Optimalisatie van verzendtijd testen
* Nieuwe reisversies maken met verbeteringen
* Aanbevelingen van AI gebruiken

[&#x200B; optimaliseer uw reizen →](optimize.md) | [&#x200B; Send-time optimalisering → &#x200B;](send-time-optimization.md)

➡️ **Klaar om te beginnen?** [&#x200B; creeer nu uw eerste reis → &#x200B;](journey-gs.md)

## Kwesties voor gebruik in de praktijk {#use-cases}

Leer uit praktische voorbeelden die aantonen hoe u reisconcepten toepast om gemeenschappelijke marketinguitdagingen op te lossen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=nl-NL)

**Onthaal nieuwe abonnees**

Wanneer een klant zich op uw dienst abonneert, teweeg een welkome reis die hen aanmoedigt om onboarding stappen te voltooien.

[Gebruiksscenario weergeven →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=nl-NL)

**Send-time optimalisering**

Gebruik AI om e-mails te verzenden wanneer elke klant waarschijnlijk verbinding zal maken, waarbij de geopende snelheden en kliksnelheden worden gemaximaliseerd.

[Gebruiksscenario weergeven →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=nl-NL)

**Ramp omhoog leveranties**

Verhoog geleidelijk het berichtvolume om uw verzendende reputatie op te warmen en leveringsproblemen te vermijden.

[Gebruiksscenario weergeven →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=nl-NL)

**Doel tegen weekdag**

Verstuur verschillende inhoud op de dag van de week die klanten uw reis voor betere relevantie ingaan.

[Gebruiksscenario weergeven →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=nl-NL)

**Multikanaalcampagnes**

Orchestreer naadloze ervaringen via e-mail, push, SMS en webkanalen in één reis.

[Gebruiksscenario weergeven →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=nl-NL)

**Alle gebruiksgevallen**

Ontdek de volledige bibliotheek met trajectgebruiksgevallen met stapsgewijze implementaties.

[&#x200B; doorblader allen → &#x200B;](jo-use-cases.md) | [&#x200B; de gevallenbibliotheek van het Gebruik → &#x200B;](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Verken de mogelijkheden van de reis {#capabilities}

Terwijl u comfortabeler bent met het maken van reizen, verkent u deze krachtige mogelijkheden om geavanceerde klantervaringen te creëren:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=nl-NL)

**Geavanceerde Uitdrukkingen**

Bouw dynamische voorwaarden en verpersoonlijking gebruikend de uitdrukkingsredacteur voor gegevensmanipulatie en complexe logica.

[Meer informatie over expressies](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=nl-NL)

**Tijdzonebeheer**

Verwerk het algemene publiek met automatische aanpassingen van de tijdzone en optimale verzendtijden.

[Tijdzones beheren](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=nl-NL)

**wijze van de Test &amp; droge looppas**

U kunt reizen valideren met testprofielen voordat u live gaat en een voorvertoning van de uitvoering weergeven zonder dat dit invloed heeft op de werkelijke gegevens.

[droge run gebruiken](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=nl-NL)

**Exemplaar aan zandbak**

Dubbele reizen tussen sandboxen om test- en implementatieworkflows te stroomlijnen.

[Reizen kopiëren](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=nl-NL)

**Markeringen &amp; organisatie**

Gebruik labels om ritten te categoriseren en filteren voor beter beheer op schaal.

[Organiseren met tags](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=nl-NL)

**controle van de Output**

Beperk berichtproductie om het verzenden van reputatie te beheren en overweldigende systemen te vermijden.

[Doorvoercontrole](limit-throughput.md)
:::

::::

[Alle reismogelijkheden weergeven →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Leren door te kijken {#video}

Bekijk een visuele introductie van reisonderdelen en leer de basisbeginselen van het maken van reizen op het canvas:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Wilt u meer video&#39;s?** [&#x200B; Onderzoek reis videoleerprogramma&#39;s &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Algemene vragen {#common-questions}

+++ Wat is het verschil tussen een reis en een campagne?

Adobe Journey Optimizer biedt drie mogelijkheden:

* **reizen**: 1 :1 organisatie in real time waar elk profiel door stappen bij hun eigen tempo reist. Het beste voor gedragsgedreven, multi-step ervaringen met voorwaardelijke logica (bv. onboarding, kartstopzetting).

* **Campagnes (actie &amp; API-teweeggebracht)**: Eenvoudige berichtlevering aan publiek, die gelijktijdig aan alle profielen of op programma of via API trekker uitvoeren. Meest geschikt voor promotiecampagnes, nieuwsbrieven en transactieberichten.

* **Geordende Campagnes**: De multi-step partijwerkschema&#39;s met complexe segmentatie die relationele gegevens (profielen + producten/opslag/het boeken) gebruiken. Alle profielen die samen met nauwkeurige aantallen pre-send worden verwerkt. Het beste voor seizoensgebonden promoties, productlanceringen, campagnes die gegevens van meerdere entiteiten vereisen.

**Zeer belangrijk verschil**: De reizen handhaven individuele klantenstaat voor acties in real time; De Campagnes Action/API leveren eenvoudige berichten in partij; Geordende Campagnes verstrekken het canvas van het partijwerkschema van multi-entiteitsegmenteringsmogelijkheden.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Meer informatie over geordende campagnes](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Kan ik een live reis bewerken?

U kunt beperkte elementen (naam, berichtinhoud) bewerken, maar voor structurele wijzigingen moet u een nieuwe versie maken. [&#x200B; Leer over reisversies &#x200B;](publish-journey.md#journey-versions)

+++

➡️ **Meer vragen?** [&#x200B; de Volledige Veelgestelde vragen van de Reis van de Mening &#x200B;](journey-faq.md) met 40+ gedetailleerde antwoorden

## Hebt u hulp nodig? {#help}

### Snelle koppelingen voor algemene taken

* **[creeer uw eerste reis](journey-gs.md)** - geleidelijke gids voor beginners
* **[Veelgestelde Veelgestelde vragen van de Reis](journey-faq.md)** - de Gemeenschappelijke beantwoorde vragen
* **[het Oplossen van problemen](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - onderzoekt en bevestigt kwesties
* **[Verwijzing van de codes van de Fout](error-codes-reference.md)** - begrijp foutenmeldingen
* **[Grafieken &amp; beperkingen](../start/guardrails.md)** - Technische grenzen en beste praktijken

### Ontvang meldingen over problemen

Opstelling **[reisalarm](../reports/alerts.md)** om bericht in real time te ontvangen wanneer de reizen fouten of ongebruikelijke patronen ontmoeten.

### Aanvullende bronnen

* **[hub van het het beheersbeleid van de Reis](/help/rp_landing_pages/manage-journey-landing-page.md)** - Hulpmiddelen voor het filtreren, optimalisering, en profielbeheer
* **[de activiteitenverwijzing van de Reis](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Volledige gids aan alle activiteitentypes
* **[de uitvoeringskwesties van het Oplossen van problemen](troubleshooting-execution.md)** - zuivert de problemen van de reisuitvoering
* **[het Oplossen van problemen binnenkomende activiteiten](troubleshooting-inbound.md)** - de ingang en kwalificatiekwesties van de moeilijke situatie

**Klaar om uw eerste reis te bouwen?** [&#x200B; wordt begonnen nu → &#x200B;](journey-gs.md)
