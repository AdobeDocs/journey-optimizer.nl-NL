---
solution: Journey Optimizer
product: journey optimizer
title: Berichtoptimalisatie
description: Gebruik berichtoptimalisatie om gepersonaliseerde en geoptimaliseerde marketingreizen en -campagnes te maken.
role: User
level: Intermediate
keywords: campagne optimaliseren, experimenteren, doelgericht testen, A/B testen
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Optimalisatie van campagnes en reizen {#message-optimization}

De optimalisering machtigt u met de hulpmiddelen om gepersonaliseerde en geoptimaliseerde inhoud aan uw publiek te leveren, <!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)--> die maximumbetrokkenheid en succes verzekeren om hoogst <!--customized and --> efficiënte reizen en campagnes tot stand te brengen.

Met Optimalisatie kunt u:

* Hefboomwerking [&#x200B; richtend &#x200B;](#targeting) regels
* Looppas [&#x200B; inhoudexperimenten &#x200B;](#experimentation)
* Gebruik [&#x200B; geavanceerde combinaties &#x200B;](#combination) van zowel experimenteren als het richten binnen één enkele campagne

Zodra de reis of de campagne live is, worden profielen beoordeeld aan de hand van de vastgestelde criteria en op basis van passende criteria, worden zij geleverd met de juiste ervaring of inhoud van de reis/campagne.

Het verschil tussen experimenten en doelgerichtheid kan als volgt worden aangegeven:

* Experimentatie bestaat uit een willekeurige splitsing in het leveren van inhoud op basis van &#x200B; voor verkeerstoewijzing.
* Het richten gebruikt deterministische technieken om inhoud te leveren die op gebruikersprofiel, publiekslidmaatschap, of op context-gebaseerde regels wordt gebaseerd.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

➡️ [&#x200B; Leer meer over optimalisering in een campagne in deze video &#x200B;](#video)

## Hefboomdoel {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_content_targeting_fallback"
>title="Wat is fallback-inhoud?"
>abstract="Met de inhoud voor alternatieven kan uw doelgroep een standaardinhoud ontvangen wanneer geen doelregel is gekwalificeerd.</br> als u deze optie niet selecteert, om het even welk publiek dat niet voor een het richten hierboven bepaalde regel kwalificeert zal geen inhoud ontvangen."

Het richten levert gepersonaliseerde inhoud aan specifieke publiekssegmenten die op gebruikersprofielattributen of contextafhankelijke attributen worden gebaseerd.

In tegenstelling tot experimenteren, een willekeurige toewijzing van de inhoud van een bericht, is het richten deterministisch wat betreft het leveren van de inhoud aan het juiste publiek.

Met betrekking tot doelgerichtheid kunnen specifieke regels worden vastgesteld op basis van:

* **de profielattributen van de Gebruiker** zoals plaats (b.v. geo-targeting), leeftijd of voorkeuren. Gebruikers in de VS zien bijvoorbeeld een &#39;Golden Gate&#39;-promotie, terwijl gebruikers in Frankrijk een &#39;Eiffeltoren&#39;-promotie zien.

* **Contextuele gegevens** zoals apparatentype (b.v. apparaat-richt), tijd van dag, of zittingsdetails. Desktopgebruikers ontvangen bijvoorbeeld inhoud die geoptimaliseerd is voor het bureaublad, terwijl mobiele gebruikers inhoud ontvangen die geoptimaliseerd is voor mobiele apparaten.

* **Soorten publiek** die kunnen worden gebruikt om profielen te omvatten of uit te sluiten die een bepaald publiekslidmaatschap hebben.

Volg de onderstaande stappen om doelframes in te stellen.

1. Creeer a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md#jo-build) of a [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Als u onderweg bent, voegt u een **[!UICONTROL Action]** -activiteit toe, kiest u een kanaalactiviteit en selecteert u **[!UICONTROL Configure action]** . [Meer informatie](../building-journeys/journey-action.md#add-action)

1. Selecteer op het tabblad **[!UICONTROL Actions]** ten minste één actie.

1. Selecteer **[!UICONTROL Optimization]** in de sectie **[!UICONTROL Create targeting rule]** .

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. Gebruik de regelbouwer om uw criteria te bepalen. Definieer bijvoorbeeld een regel voor inwoners van de VS, een regel voor inwoners van Frankrijk en een regel voor inwoners van India.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Selecteer de optie **[!UICONTROL Enable fallback content]** naar wens. Met de inhoud voor alternatieven kan uw doelgroep een standaardinhoud ontvangen wanneer geen doelregel is gekwalificeerd.

   >[!NOTE]
   >
   >Als u deze optie niet selecteert, ontvangen alle doelgroepen die niet in aanmerking komen voor een hierboven gedefinieerde doelregel geen inhoud.

1. Sla de instellingen voor de doelregel op.

1. Selecteer **[!UICONTROL Actions]** weer op het tabblad **[!UICONTROL Edit content]** .

1. Ontwerp aangewezen inhoud voor elke groep die door uw het richten regelmontages wordt bepaald.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   In dit voorbeeld, ontwerp een specifieke inhoud voor inwoners van de V.S., een verschillende inhoud voor Franse ingezetenen en een andere inhoud voor inwoners van India.

1. [&#x200B; activeer &#x200B;](review-activate-campaign.md) uw reis of campagne.

Zodra de reis/campagne live is, wordt inhoud die voor elk doel is ontworpen, verzonden zodat inwoners van de VS een specifieke boodschap krijgen, inwoners van Frankrijk een andere boodschap, enzovoort.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## Gebruik experimenteren {#experimentation}

Met behulp van experimenten kunt u meerdere versies van de inhoud testen om te bepalen wat het beste werkt op basis van vooraf gedefinieerde succeswaarden.

Volg onderstaande stappen om experimenten in te stellen.

Stel dat u de volgende promotieberichten in een campagne wilt testen:

* **Behandeling A**: &quot;20% van uw volgende aankoop&quot;
* **Behandeling B**: &quot;Vrije verschepen op orden boven $50&quot;
* **Behandeling C**: &quot;Krijg uw $10 geschenkkaart&quot;

Volg de onderstaande stappen om experimenten in te stellen en te bepalen welk bericht de meeste aankopen aanstuurt.

1. Creeer a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md#jo-build) of a [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Als u onderweg bent, voegt u een **[!UICONTROL Action]** -activiteit toe, kiest u een kanaalactiviteit en selecteert u **[!UICONTROL Configure action]** . [Meer informatie](../building-journeys/journey-action.md#add-action)

1. Van het **[!UICONTROL Actions]** lusje, selecteer twee binnenkomende acties, bijvoorbeeld [&#x200B; code-gebaseerde ervaring &#x200B;](../code-based/get-started-code-based.md) en [&#x200B; in-app &#x200B;](../../rp_landing_pages/in-app-landing-page.md).

1. Selecteer **[!UICONTROL Optimization]** in de sectie **[!UICONTROL Create experiment]** .

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Ontwerp en configureer uw content-experiment naar wens. [&#x200B; leer hoe &#x200B;](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Zodra het experiment is gedefinieerd, is het van toepassing op alle acties die in die campagne of door de reis **[!UICONTROL Action]** activiteit worden opgenomen, wat betekent dat dezelfde klanten dezelfde aanbiedingen op alle oppervlakken zien.

   >[!NOTE]
   >
   >U kunt andere acties selecteren: de experimenten zijn van toepassing op alle acties die aan de campagne of aan de reisactie worden toegevoegd.

1. [&#x200B; activeer &#x200B;](review-activate-campaign.md) uw reis of campagne.

Zodra de reis/de campagne levend is, worden de gebruikers willekeurig toegewezen de verschillende inhoudvariaties. [!DNL Journey Optimizer] houdt bij welke variatie meer aankopen drijft en actioneerbare inzichten verstrekt.

Volg het succes van uw campagne met de [&#x200B; reis &#x200B;](../reports/journey-global-report-cja.md) en [&#x200B; campagne &#x200B;](../reports/campaign-global-report-cja-experimentation.md) rapporten. <!--Link to Experimentation journey reportis missing-->

## Doelstellingen en experimenten combineren {#combination}

Met Journey Optimizer kunt u ook gerichte toepassingen en experimenten combineren binnen één reis of campagne om geavanceerdere strategieën te ontwikkelen.

U kunt doelgericht gebruiken om verschillende varianten te maken. Voor elke variant kunt u experimenteren om elke inhoud verder te optimaliseren. Dit zorgt ervoor dat de experimenten voor elke het richten regel specifiek zijn en zich niet over varianten uitstrekken.

U kunt bijvoorbeeld een &#39;50% korting op promotie&#39; testen in plaats van een &#39;50% cadeaukaart&#39; voor klanten in de VS en een andere test uitvoeren voor klanten in Europa, zoals &#39;gratis verzending voor bestellingen van meer dan 50 euro&#39; in plaats van &#39;20% korting op hun volgende aankoop&#39;.

Volg de onderstaande stappen om zowel gerichte als experimenten op een reis of campagne te combineren.

1. Creeer een reis of een campagne waar u verscheidene richtingsregels bepaalt. [&#x200B; leer hoe &#x200B;](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Maak een experiment voor de eerste doelregel.

1. Ontwerp en configureer uw content-experiment naar wens. [&#x200B; leer hoe &#x200B;](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Zodra de experimentatie wordt bepaald, is het slechts op de eerste gerichte regel van toepassing.

1. Selecteer **[!UICONTROL Actions]** weer op het tabblad **[!UICONTROL Edit content]** .

1. Voor de groep die door uw eerste het richten regel wordt bepaald, kunt u een specifieke inhoud voor elke variant van uw experiment bepalen.

   Als u meer dan één binnenkomende actie aan uw reis of campagne toevoegde, is de zelfde combinatie gericht en experiment op elke actie van toepassing. Nochtans, moet u een specifieke inhoud voor elke variant van elke actie bepalen.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Ga zo gelijkaardig voor andere het richten regels te werk, en ontwerp de overeenkomstige inhoud voor elke variant.

1. Sparen uw veranderingen en [&#x200B; activeer &#x200B;](review-activate-campaign.md) uw reis of campagne.

Zodra de reis/de campagne levend is, worden de gebruikers van elke doelgroep willekeurig toegewezen de verschillende inhoudvariaties die voor de groep worden bepaald zij tot behoren.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

## Hoe kan ik-video{#video}

Leer hoe u berichtoptimalisatie kunt benutten in actie- of API-campagnes. U zult zien hoe te om sub-publiek te richten, berichtvariaties door plaats tot stand te brengen, fallback inhoud toe te laten, en veelvoudige experimenten in één enkele campagne in werking te stellen. In deze zelfstudie wordt ook uitgelegd hoe u campagnes met meerdere kanalen kunt beheren en tegelijkertijd de consistentie van berichten kunt behouden.

>[!VIDEO](https://video.tv.adobe.com/v/3470374?captions=dut&quality=12)