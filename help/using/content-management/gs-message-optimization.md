---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met optimalisatie van inhoud
description: Leer hoe u inhoud optimaliseert voor persoonlijke en geoptimaliseerde inhoud tijdens campagnes en reizen.
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: optimalisatie, doelgericht, experimenteren, A/B-tests, campagnes, reizen, personalisatie
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 8dba26f29fda47d0b953d80656aa0f0b6fe294a9
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 2%

---

# Aan de slag met optimalisatie van inhoud {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="Inhoud optimaliseren"
>abstract="Met de functie voor het optimaliseren van inhoud in Journey Optimizer kunt u verschillende versies van uw inhoud testen en bepalen welke versie het beste werkt. U kunt richten gebruiken om gepersonaliseerde inhoud aan specifieke segmenten te leveren, experimenteren om veelvoudige variaties te testen, of beide benaderingen voor verfijnde optimaliseringsstrategieën te combineren."

Met de gereedschappen kunt u de juiste boodschap op het juiste moment aan het juiste publiek afgeven. Door gegevensgestuurde inzichten te combineren met krachtige personalisatiemogelijkheden kunt u uw betrokkenheid en conversies maximaliseren voor al uw campagnes en reizen.

De optimalisering van de inhoud is beschikbaar in zowel [&#x200B; campagnes &#x200B;](../campaigns/create-campaign.md) als [&#x200B; reizen &#x200B;](../building-journeys/journey-gs.md), toelatend u om de zelfde optimaliseringsstrategieën over al uw klanten toe te passen touchpoints.

➡️ [&#x200B; Leer hoe te optimalisering van de hefboominhoud binnen een campagne in deze video &#x200B;](#video)

## Optimalisatiefuncties {#capabilities}

Met de optimalisatie van inhoud in Journey Optimizer kunt u:

* [&#x200B; Gebruik richtend &#x200B;](optimization-targeting.md) om gepersonaliseerde inhoud aan specifieke publiekssegmenten te leveren die op profielattributen, contextafhankelijke gegevens, of publiekslidmaatschap worden gebaseerd.

* [&#x200B; de experimenten van de Looppas &#x200B;](optimization-experimentation.md) om veelvoudige inhoudvariaties te testen en te identificeren die best op uw succesmetriek wordt gebaseerd.

* [&#x200B; combineer beide benaderingen &#x200B;](optimization-combination.md) om verfijnde optimaliseringsstrategieën tot stand te brengen waar u verschillende variaties voor elk gericht segment test.

## Doelstelling versus experimenteren {#targeting-vs-experimentation}

Als u het verschil begrijpt tussen gericht en experimenteren, kunt u de juiste optimalisatiebenadering kiezen voor uw doelen.

**het richten** gebruikt deterministische regels om gepersonaliseerde inhoud aan specifieke segmenten te leveren die op bekende profielattributen, context, of publiekslidmaatschap worden gebaseerd. Het zorgt ervoor dat het juiste bericht het juiste publiek bereikt.

**de Experimentatie** gebruikt willekeurige taak om veelvoudige inhoudsvariaties te testen en te ontdekken die het best presteert. Het helpt u te leren wat het meest met uw publiek door gegeven-gedreven het testen resoneert.

De onderstaande tabel geeft een overzicht van de belangrijkste verschillen:

| Capaciteit | Targeting | Experimentatie |
|--------|-----------|-----------------|
| **methode van de Toewijzing** | Deterministisch - gebaseerd op regels | Willekeurig - gebaseerd op verkeerstoewijzing |
| **Gebaseerd op** | Profielkenmerken, context, publiek | Willekeurige distributie |
| **Gebruiksscenario** | Verstrek relevante inhoud aan bekende segmenten | Controleren welke inhoud het beste presteert |
| **Voorbeeld** | Verschillende aanbiedingen per locatie tonen | Test 2 onderwerpregel om te zien welke knop meer opent |
| **Best voor** | Personalization op schaal | Optimalisatie en leren |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Vaak voorkomende gebruiksscenario&#39;s {#use-cases}

Hier volgen enkele typische scenario&#39;s waarbij optimalisatie van inhoud u kan helpen betere resultaten te bereiken:

Doelstelling:

* **Geo-gericht** - verzend plaats-specifieke aanbiedingen die op waar uw klanten worden gebaseerd worden gevestigd. Bijvoorbeeld winterjassen in koudere regio&#39;s en zwemkleding in warmer klimaat bevorderen.

* **optimalisering van het Apparaat** - lever apparaat-specifieke inhoud, zoals Desktop-geoptimaliseerde lay-outs voor Desktopgebruikers en mobiele-geoptimaliseerde lay-outs voor smartphonegebruikers.

Experimentatie:

* **het testen A/B** - test verschillende e-mailonderwerplijnen, de knopen van call-to-action, of promotionele aanbiedingen om te ontdekken welke drijven de meeste omzettingen.

* **de marketing van de Levenscyclus** - test verschillende onboarding berichten voor nieuwe klanten tegenover bewaaraanbiedingen voor bestaande klanten.

Combinatie:

* **Geavanceerde segmentatie** - de klanten van het doel door loyaliteitrij en test verschillende beloningsoverseinen binnen elke rij om overeenkomst over alle segmenten te maximaliseren.

## Aan de slag {#get-started}

Uw inhoud optimaliseren:

1. **creeer een campagne of een reis**: Opstelling uw [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) of [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md) en voeg minstens één actie toe.

1. **kies uw optimalisatiebenadering**:
   * [&#x200B; Gebruik richtend &#x200B;](optimization-targeting.md) om inhoud voor specifieke segmenten te personaliseren.
   * [&#x200B; experimenteren van het Gebruik &#x200B;](optimization-experimentation.md) om veelvoudige variaties te testen.
   * [&#x200B; combineer allebei &#x200B;](optimization-combination.md) voor geavanceerde optimalisering.

1. **bepaal uw inhoud**: Creeer de verschillende inhoudsvariaties voor uw optimaliseringsstrategie.

1. **activeer en controleer**: Lanceer uw geoptimaliseerde campagne of reis en spoorprestaties in de [&#x200B; rapporten &#x200B;](../reports/campaign-global-report-cja.md).

## Werking {#how-it-works}

Zodra uw reis of campagne levend is, worden de profielen beoordeeld aan de criteria u hebt bepaald. Op basis van deze evaluaties ontvangt elk profiel de meest geschikte inhoudsversie:

1. **de evaluatie van het Profiel** - wanneer een profiel uw campagne of reis ingaat, evalueert Journey Optimizer hun attributen en context.

1. **toewijzing van de Inhoud** - Gebaseerd op uw optimalisatieconfiguratie:
   * Voor **het richten**, ontvangen de profielen die specifieke criteria aanpassen de overeenkomstige gepersonaliseerde inhoud.
   * Voor **experimenteren**, worden de profielen willekeurig toegewezen aan verschillende inhoudsvariaties die op uw montages van de verkeerstoewijzing worden gebaseerd.
   * Voor **combinaties**, passen de profielen eerst een het richten regel aan, dan worden willekeurig toegewezen aan één van de experimentele variaties voor dat segment.

1. **Prestaties die** volgen - Journey Optimizer volgt automatisch betrokkenheidsmetriek en omzettingsgegevens om u te helpen identificeren welke inhoud het best presteert.

## Hoe kan ik-video {#video}

Leer hoe u de optimalisatie van inhoud kunt optimaliseren in actie- of API-campagnes. U zult zien hoe te om sub-publiek te richten, berichtvariaties door plaats tot stand te brengen, fallback inhoud toe te laten, en veelvoudige experimenten in één enkele campagne in werking te stellen. In deze zelfstudie wordt ook uitgelegd hoe u campagnes met meerdere kanalen kunt beheren en tegelijkertijd de consistentie van berichten kunt behouden.

>[!VIDEO](https://video.tv.adobe.com/v/3470374?captions=dut&quality=12)

**Verwante onderwerpen**

* [Een campagne maken](../campaigns/create-campaign.md)
* [Een journey maken](../building-journeys/journey-gs.md)
* [Inhoudsexperiment](../content-management/get-started-experiment.md)
