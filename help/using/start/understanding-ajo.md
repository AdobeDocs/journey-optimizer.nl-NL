---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer begrijpen
description: Leer hoe Adobe Journey Optimizer met Adobe Experience Platform werkt om persoonlijke ervaringen van klanten te bieden
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: a956684ab52f9045b5e1f84cc0b8d0071689873b
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Journey Optimizer begrijpen {#understanding-ajo}

Adobe Journey Optimizer (AJO) en Adobe Experience Platform (AEP) werken samen om gegevensgestuurde personalisatie op grote schaal mogelijk te maken. In deze pagina wordt uitgelegd hoe deze systemen werken en hoe hun belangrijkste functionele gebieden worden gecombineerd om uitzonderlijke klantervaringen te bieden.

## Hoe Journey Optimizer werkt {#how-it-works}

Adobe Journey Optimizer werkt als een continue stroom waarbij gegevens worden verzameld, geanalyseerd en toegepast om persoonlijke klantritten te maken.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: De Stichting {#aep-foundation}

Adobe Experience Platform fungeert als ruggengraat en stelt merken in staat klantgegevens te centraliseren en te activeren voor persoonlijke ervaringen:

* **Platform van Gegevens** - Centrale hub voor het verzamelen, het leiden, en het structureren van klantengegevens om consistentie over systemen te verzekeren
* **Ingestie van Gegevens (Bronnen)** - de gegevens van de platforms van CRM, websites, mobiele apps, en wolkenopslag die pre-gebouwde schakelaars gebruiken
* **Real-time het Profiel van de Klant** - creeert verenigde profielen door gegevens van veelvoudige bronnen (e-mailinteracties, in-store aankopen, Webgedrag samen te voegen)
* **Laag van de Governance** - de gegevenstoegang, privacynaleving, en veiligheid terwijl het naleven van verordeningen

### Adobe Journey Optimizer: De Orchestration Engine {#ajo-orchestration}

Adobe Journey Optimizer past de gegevens en inzichten van AEP toe om intelligente, gepersonaliseerde klantenervaringen te bieden:

* **Klantbegrip** - De Profielen van de Klant in real time laten segmentatie in publiek voor gericht overseinen toe
* **Inhoud &amp; Aanbiedingen** - Hulpmiddelen voor het creëren van, het leiden van, en het personaliseren van inhoud; logica in real time om de beste aanbieding voor elke individu te selecteren
* **Reis &amp; het Beheer van de Campagne** - automatiseert opeenvolgingen van interactie (reizen) of programma&#39;s één-tijd gerichte berichten (campagnes)
* **Levering (Verbindingen)** - levert berichten door kanalen zoals e-mail, SMS, dupberichten, en directe post; exporteert gegevens aan externe systemen
* **Meting &amp; Analyse** - Traceert klantenovereenkomst en campagneprestaties met rapporten voor ononderbroken verbetering

### De doorlopende optimalisatiecyclus {#optimization-cycle}

Dit ecosysteem werkt als een doorlopende optimalisatiecyclus. Gegevens zorgen ervoor dat de klant begrijpt wat persoonlijke inhoud en beslissingen zijn. Deze worden georkestreerd in ritten, via kanalen geleverd, gemeten voor effectiviteit, en in de loop van de tijd verfijnd.

![](../assets/do-not-localize/get-started-flow.png)

## Belangrijkste functionele gebieden {#functional-areas}

Journey Optimizer omvat zeven belangrijke functionele gebieden die naadloos samenwerken:

| Functioneel gebied | Doel | Belangrijkste activiteiten |
|-----------------|---------|----------------|
| **het Beheer van Gegevens** | Klantgegevens organiseren | Definieer schema&#39;s, maak gegevenssets, importeer gegevens van verschillende systemen |
| **Beheer van de Klant** | Begrijp wie uw klanten zijn | Samengestelde profielen maken, identiteiten oplossen, publiek maken |
| **Contentmanagement** | Persoonlijke berichten maken | E-mails ontwerpen, elementen beheren, sjablonen en fragmenten maken, inhoud aanpassen |
| **Beheer van het Besluit** | Selecteer de beste aanbieding in real-time | Aanbiedingsbibliotheek beheren, regels definiëren, beperkingen toepassen, waarderingslogica instellen |
| **Beheer van de Reis** | Ontwerp geautomatiseerde klantenervaringen | Reizen maken met visuele ontwerper, triggers instellen, voorwaarden toevoegen en stappen wachten |
| **Verbindingen** | Gegevensbronnen en kanalen verbinden | Bronconnectors configureren, kanalen instellen, verbinding maken met externe platforms |
| **Beleid &amp; Privacy** | Instellen en compatibiliteit van besturingselementen | Gebruikers beheren, sandboxen configureren, kanalen instellen, privacyverzoeken verwerken |

### Hoe deze gebieden samenwerken {#working-together}

Deze functionele gebieden werken in een doorlopende cyclus:

1. **Ingestie van Gegevens** - de stromen van Gegevens in AEP, die door het Beheer van Gegevens worden gestructureerd
2. **Klant Begrip** - Echte - de Profielen van de Klant verenigen gegevens; Het Beheer van de Klant leidt tot publiek
3. **de Strategie van de Inhoud &amp; van het Aanbod** - het Beheer van de Inhoud leidt tot berichten; Het Beheer van het Besluit bepaalt aanbiedingslogica
4. **Orchestration** - de kaarten van het Beheer van de Reis interacties over kanalen gebruikend klantengegevens, inhoud, en besluiten
5. **Levering** - de Verbindingen vergemakkelijken berichtlevering via kanalen of delen gegevens met externe systemen
6. **Meting** - de gegevens van Prestaties voeren terug inzichten terug naar raffineren publiek, inhoud, besluiten, en reizen
7. **Bestuur** - de controles van het Beleid en van de Privacy verzekeren naleving door

## Architectuurgegevens {#architecture-details}

Voor technische teams, hier is het gedetailleerde architectuurdiagram dat toont hoe Journey Optimizer met Adobe Experience Platform integreert:

![ Architectuur van Adobe Journey Optimizer ](assets/ajo-architecture.png)

Vier toepassingen zijn native gebaseerd op Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics en Adobe Mix Modeler. Journey Optimizer werkt naadloos met deze toepassingen, maar kan ook onafhankelijk werken.

### Integratiepunten {#integration-points}

Journey Optimizer kan op meerdere niveaus worden geïntegreerd met Adobe Experience Platform:

* **Laag van Gegevens** - deelt het zelfde Profiel van de Klant in real time, de Grafiek van de Identiteit, en datasets
* **Laag van de Dienst** - Hefboomwerkingen het bestuur van AEP, privacy, en de vraagdiensten
* **Laag van de Toepassing** - verstrekt reisorchestratie, besluitvormingsbeheer, en inhoudsbeheer bovenop AEP

Leer meer over [ blauwdrukken van Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Privacy en beveiliging {#privacy-security}

De privacy- en beveiligingspraktijken van Adobe Experience Cloud gelden voor Adobe Journey Optimizer. Deze maatregelen zorgen ervoor dat de privacyregels, zoals GDPR, worden nageleefd, zodat u persoonlijke ervaringen kunt bieden en het vertrouwen van de klant blijft behouden.

[Meer informatie over privacy in Journey Optimizer](../privacy/get-started-privacy.md)

>[!MORELIKETHIS]
>
>* [ worden begonnen met Journey Optimizer ](get-started.md)
>* [ Zeer belangrijke terminologie ](terminology.md)
>* [ gebruikersinterfacegids ](user-interface.md)
>* [ Grafieken en beperkingen ](guardrails.md)

