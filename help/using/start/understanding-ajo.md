---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer begrijpen
description: Leer hoe Adobe Journey Optimizer met Adobe Experience Platform werkt om persoonlijke ervaringen van klanten te bieden
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 87f714e380957b40df196652ac37d1e6cd611925
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 2%

---

# Journey Optimizer begrijpen {#understanding-ajo}

Adobe Journey Optimizer en Adobe Experience Platform werken samen om datatiedriving op grote schaal mogelijk te maken. In deze pagina wordt uitgelegd hoe deze systemen werken en hoe hun belangrijkste functionele gebieden worden gecombineerd om uitzonderlijke klantervaringen te bieden. [ leer over zeer belangrijke mogelijkheden ](get-started.md) | [ Onderzoek zeer belangrijke terminologie ](terminology.md)

## Hoe Journey Optimizer werkt {#how-it-works}

Adobe Journey Optimizer werkt als een continue stroom waarbij gegevens worden verzameld, geanalyseerd en toegepast om persoonlijke klantritten te maken.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: De Stichting {#aep-foundation}

Adobe Experience Platform fungeert als ruggengraat en stelt merken in staat klantgegevens te centraliseren en te activeren voor persoonlijke ervaringen:

* **Platform van Gegevens** - Centrale hub voor het verzamelen, het leiden, en het structureren van klantengegevens om consistentie over systemen te verzekeren. [ leer over schema&#39;s en datasets ](../data/get-started-schemas.md)
* **Ingestie van Gegevens (Bronnen)** - de gegevens van de platforms van CRM, websites, mobiele apps, en wolkenopslag die pre-gebouwde schakelaars gebruiken. [ Onderzoek gegevensbronnen ](get-started-sources.md)
* **In real time het Profiel van de Klant** - creeert verenigde profielen door gegevens van veelvoudige bronnen (e-mailinteractie, in-store aankopen, Webgedrag) samen te voegen. [ leer over profielen ](../audience/get-started-profiles.md)
* **Laag van de Governance** - beheert gegevenstoegang, privacynaleving, en veiligheid terwijl het naleven van verordeningen. [ de privacydocumentatie van de Mening ](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: De Orchestration Engine {#ajo-orchestration}

Adobe Journey Optimizer past de gegevens en inzichten van Adobe Experience Platform toe om intelligente, gepersonaliseerde klantenervaringen te bieden:

* **Klantbegrip** - In real time de Profielen van de Klant laten segmentatie in publiek voor gericht overseinen toe. [ creeer publiek ](../audience/about-audiences.md)
* **Inhoud &amp; Aanbiedingen** - Hulpmiddelen voor het creëren van, het leiden van, en het personaliseren van inhoud; logica in real time om de beste aanbieding voor elk individu te selecteren. [ inhoud van het Ontwerp ](../../rp_landing_pages/content-management-landing-page.md) | [ beheert aanbiedingen ](../offers/get-started/starting-offer-decisioning.md)
* **Reis &amp; het Beheer van de Campagne** - Automatiseert opeenvolgingen van interactie (reizen) of programma&#39;s éénmalig gerichte berichten (campagnes). [ Bouw reizen ](../building-journeys/journey-gs.md) | [ creeer campagnes ](../campaigns/get-started-with-campaigns.md)
* **Levering (Verbindingen)** - levert berichten door kanalen zoals e-mail, SMS, dupberichten, en directe post; exporteert gegevens aan externe systemen. [ vorm kanalen ](../configuration/get-started-configuration.md)
* **Meting &amp; Analyse** - de klantenovereenkomst en campagneprestaties van het spoor met rapporten voor ononderbroken verbetering. [ rapporten van de Mening ](../reports/campaign-global-report-cja.md)

### De doorlopende optimalisatiecyclus {#optimization-cycle}

Dit ecosysteem werkt als een doorlopende optimalisatiecyclus. Gegevens zorgen ervoor dat de klant begrijpt wat persoonlijke inhoud en beslissingen zijn. Deze worden georkestreerd in ritten, via kanalen geleverd, gemeten voor effectiviteit, en in de loop van de tijd verfijnd.

![](../assets/do-not-localize/get-started-flow.png)

## Belangrijkste functionele gebieden {#functional-areas}

Journey Optimizer omvat zeven belangrijke functionele gebieden die naadloos samenwerken:

| Functioneel gebied | Doel | Belangrijkste activiteiten |
|-----------------|---------|----------------|
| **het Beheer van Gegevens** | Klantgegevens organiseren | Bepaal schema&#39;s, creeer datasets, de invoergegevens van diverse systemen. [Meer informatie](../data/get-started-schemas.md) |
| **Beheer van de Klant** | Begrijp wie uw klanten zijn | Samengestelde profielen maken, identiteiten oplossen, publiek maken. [Meer informatie](../audience/get-started-profiles.md) |
| **Contentmanagement** | Persoonlijke berichten maken | E-mails ontwerpen, elementen beheren, sjablonen en fragmenten maken, inhoud aanpassen. [Meer informatie](../../rp_landing_pages/content-management-landing-page.md) |
| **Beheer van het Besluit** | Selecteer de beste aanbieding in real-time | De aanbiedingsbibliotheek beheren, regels definiëren, beperkingen toepassen en waarderingslogica instellen. [Meer informatie](../offers/get-started/starting-offer-decisioning.md) |
| **Beheer van de Reis** | Ontwerp geautomatiseerde klantenervaringen | Reizen maken met visuele ontwerper, triggers instellen, voorwaarden toevoegen en stappen wachten. [Meer informatie](../building-journeys/journey-gs.md) |
| **Verbindingen** | Gegevensbronnen en kanalen verbinden | Vorm bronschakelaars, opstellingskanalen, verbind met externe platforms. [Meer informatie](../configuration/get-started-configuration.md) |
| **Beleid &amp; Privacy** | Instellen en compatibiliteit van besturingselementen | Gebruikers beheren, sandboxen configureren, kanalen instellen, privacyverzoeken afhandelen. [Meer informatie](../administration/permissions.md) |

### Hoe deze gebieden samenwerken {#working-together}

Deze functionele gebieden werken in een doorlopende cyclus:

1. **Ingestie van Gegevens** - de stromen van Gegevens in Adobe Experience Platform, die door het Beheer van Gegevens worden gestructureerd
2. **Klant Begrip** - Echte - de Profielen van de Klant verenigen gegevens; Het Beheer van de Klant leidt tot publiek
3. **de Strategie van de Inhoud &amp; van het Aanbod** - het Beheer van de Inhoud leidt tot berichten; Het Beheer van het Besluit bepaalt aanbiedingslogica
4. **Orchestration** - de kaarten van het Beheer van de Reis interacties over kanalen gebruikend klantengegevens, inhoud, en besluiten
5. **Levering** - de Verbindingen vergemakkelijken berichtlevering via kanalen of delen gegevens met externe systemen
6. **Meting** - de gegevens van Prestaties voeren terug inzichten terug naar raffineren publiek, inhoud, besluiten, en reizen
7. **Bestuur** - de controles van het Beleid en van de Privacy verzekeren naleving door

## Architectuurgegevens {#architecture-details}

Voor technische teams, hier is het gedetailleerde architectuurdiagram dat toont hoe Journey Optimizer met Adobe Experience Platform integreert. [ Navigeer de interface ](user-interface.md) om deze componenten in praktijk te onderzoeken.

![ Architectuur van Adobe Journey Optimizer ](assets/ajo-architecture.png)

Vier toepassingen zijn native gebaseerd op Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics en Adobe Mix Modeler. Journey Optimizer werkt naadloos met deze toepassingen, maar kan ook onafhankelijk werken. [ de gidsen en beperkingen van het Overzicht ](guardrails.md) voor implementatieoverwegingen.

### Integratiepunten {#integration-points}

Journey Optimizer kan op meerdere niveaus worden geïntegreerd met Adobe Experience Platform:

* **Laag van Gegevens** - deelt het zelfde Profiel van de Klant in real time, de Grafiek van de Identiteit, en datasets
* **Laag van de Dienst** - Hefboomwerkingen het bestuur van Adobe Experience Platform, privacy, en de vraagdiensten
* **Laag van de Toepassing** - verstrekt reisorchestratie, besluitvormingsbeheer, en inhoudsbeheer bovenop Adobe Experience Platform

Leer meer over [ blauwdrukken van Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Privacy en beveiliging {#privacy-security}

De privacy- en beveiligingspraktijken van Adobe Experience Cloud gelden voor Adobe Journey Optimizer. Deze maatregelen zorgen ervoor dat de privacyregels, zoals GDPR, worden nageleefd, zodat u persoonlijke ervaringen kunt bieden en het vertrouwen van de klant blijft behouden. [ Leer meer over privacy in Journey Optimizer ](../privacy/get-started-privacy.md)
