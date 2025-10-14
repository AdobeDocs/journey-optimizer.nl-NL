---
solution: Journey Optimizer
product: journey optimizer
title: AJO-architectuur
description: Architectuur en relatie met AEP
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: f94067ffb421bfd095ed3fcb3001af0e5dc44ab3
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Architectuur

## Het grote beeld: hoe Adobe Journey Optimizer bij elkaar past

Adobe Journey Optimizer (AJO) en Adobe Experience Platform (AEP) werken samen om gegevensgestuurde personalisatie op grote schaal mogelijk te maken. Dit ecosysteem werkt als een continue stroom waarbij gegevens worden verzameld, geanalyseerd en toegepast om persoonlijke klantritten te maken.

![](../assets/do-not-localize/get-started-big-picture.png)


### Stichting: Adobe Experience Platform (AEP)

Adobe Experience Platform fungeert als ruggengraat en stelt merken in staat klantgegevens te centraliseren en te activeren voor persoonlijke ervaringen.

- **Platform van Gegevens**: AEP werkt als centrale hub voor het verzamelen, het leiden, en het structureren van klantengegevens om consistentie over systemen te verzekeren.
- **Ingestie van Gegevens (Bronnen)**: Merken de invoergegevens van diverse systemen, zoals de platforms van CRM, websites, mobiele apps, en wolkenopslag, gebruikend pre-gebouwde schakelaars. Bijvoorbeeld, neemt een Schakelaar van Source aankoopgegevens van een e-commerceplatform op.
- **In real time het Profiel van de Klant**: Deze eigenschap leidt verenigde profielen door gegevens van veelvoudige bronnen samen te voegen. Een profiel combineert bijvoorbeeld e-mailinteracties en in-store aankopen om een volledige weergave van een klant te bieden.
- **Laag van de Governance**: Deze laag beheerst gegevenstoegang, privacynaleving, en veiligheid. Het zorgt ervoor dat de merken veilig klantengegevens gebruiken terwijl het naleven van verordeningen.

### Orchestration Engine: Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer past de gegevens en inzichten van AEP toe om intelligente, gepersonaliseerde klantenervaringen op verschillende kanalen te bieden.

- **Klant Begrip**: De Profielen van de Klant in real time laten segmentatie in Soorten publiek voor gericht overseinen toe. Een publiek bevat bijvoorbeeld vaak winkelen die worden geïdentificeerd door de aankoopgeschiedenis.
- **Inhoud &amp; Aanbiedingen**:
   - **het Beheer van de Inhoud**: Deze eigenschap verstrekt hulpmiddelen om, inhoud over kanalen tot stand te brengen te leiden en te personaliseren. U kunt bijvoorbeeld een herbruikbaar inhoudsfragment maken voor een promotionele e-mailkoptekst.
   - **Beheer van het Besluit**: Dit systeem gebruikt logica in real time om de beste aanbieding of het bericht voor elk individu te selecteren. Een in aanmerking komende klant kan bijvoorbeeld een kortingsvoorstel ontvangen op basis van zijn browsergeschiedenis.
- **Reis &amp; het Beheer van de Campagne**: Deze eigenschap automatiseert opeenvolgingen van interactie (Reizen) of programma&#39;s eenmalige gerichte berichten (Campagnes). Een Journey activeert bijvoorbeeld vervolgberichten na een productweergave.
- **Levering (Verbindingen)**:
   - **Kanalen**: Deze eigenschap levert berichten en aanbiedingen door communicatie platforms zoals e-mail, SMS, dupberichten, en directe post.
   - **Doelen**: Deze eigenschap voert profiel en publieksgegevens naar externe systemen voor activering of analyse uit. De publieksgegevens worden bijvoorbeeld naar een sociaal mediaplatform verzonden voor advertenties.
- **Meting &amp; Analyse**: Deze eigenschap volgt klantenovereenkomst en campagneprestaties met rapporten. Deze inzichten maken voortdurende verbetering mogelijk.

## Doorlopende optimalisatiecyclus

Dit ecosysteem werkt als een doorlopende optimalisatiecyclus. Gegevens zorgen ervoor dat de klant begrijpt wat persoonlijke inhoud en beslissingen zijn. Deze worden georkestreerd in ritten, via kanalen geleverd, gemeten voor effectiviteit, en in de loop van de tijd verfijnd.

![](../assets/do-not-localize/get-started-flow.png)

## Gedetailleerde architectuur

![&#x200B; Architectuur van Adobe Journey Optimizer &#x200B;](assets/ajo-architecture.png)


## Privacy en beveiliging

De privacy- en beveiligingspraktijken van Adobe Experience Cloud gelden voor Adobe Journey Optimizer. Deze maatregelen zorgen ervoor dat de privacyregels worden nageleefd, zodat merken persoonlijke ervaringen kunnen bieden en het vertrouwen van de klant behouden blijft.
