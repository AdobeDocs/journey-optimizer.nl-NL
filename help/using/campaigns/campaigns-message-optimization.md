---
solution: Journey Optimizer
product: journey optimizer
title: Berichtoptimalisatie
description: Gebruik berichtoptimalisatie om gepersonaliseerde en geoptimaliseerde marketingcampagnes te maken.
role: User
level: Intermediate
keywords: campagne optimaliseren, experimenteren, doelgericht testen, A/B testen
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 4d7ad2c3ed71801298f1afe31d0e29d7bb1d5c7f
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Optimalisatie in campagnes {#message-optimization}

De optimalisering machtigt u met de hulpmiddelen om gepersonaliseerde en geoptimaliseerde inhoud aan het publiek van uw campagnes te leveren, <!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)--> die maximumbetrokkenheid en succes verzekeren om hoogst <!--customized and --> efficiënte campagnes tot stand te brengen.

Met Optimalisatie kunt u:

* Hefboomwerking [ richtend ](#targeting) regels
* Looppas [ inhoudexperimenten ](#experimentation)
* Gebruik [ geavanceerde combinaties ](#combination) van zowel experimenteren als het richten binnen één enkele campagne

Wanneer de campagne live is, worden profielen beoordeeld aan de hand van de gedefinieerde criteria en op basis van overeenkomstige criteria, worden ze geleverd met de juiste ervaring of inhoud van de campagne.

Het verschil tussen experimenten en doelgerichtheid kan als volgt worden aangegeven:

* Experimentatie bestaat uit een willekeurige splitsing in het leveren van inhoud op basis van &#x200B; voor verkeerstoewijzing.
* Het richten gebruikt deterministische technieken om inhoud te leveren die op gebruikersprofiel, publiekslidmaatschap, of op context-gebaseerde regels wordt gebaseerd.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Hefboomdoel {#targeting}

Het richten levert gepersonaliseerde inhoud aan specifieke publiekssegmenten die op gebruikersprofielattributen of contextafhankelijke attributen worden gebaseerd.

In tegenstelling tot experimenteren, een willekeurige toewijzing van de inhoud van een bericht, is het richten deterministisch wat betreft het leveren van de inhoud aan het juiste publiek.

Met betrekking tot doelgerichtheid kunnen specifieke regels worden vastgesteld op basis van:

* **de profielattributen van de Gebruiker** zoals plaats (b.v. geo-targeting), leeftijd of voorkeuren. Gebruikers in de VS zien bijvoorbeeld een &#39;Golden Gate&#39;-promotie, terwijl gebruikers in Frankrijk een &#39;Eiffeltoren&#39;-promotie zien.

* **Contextuele gegevens** zoals apparatentype (b.v. apparaat-richt), tijd van dag, of zittingsdetails. Desktopgebruikers ontvangen bijvoorbeeld inhoud die geoptimaliseerd is voor het bureaublad, terwijl mobiele gebruikers inhoud ontvangen die geoptimaliseerd is voor mobiele apparaten.

* **Soorten publiek** die kunnen worden gebruikt om profielen te omvatten of uit te sluiten die een bepaald publiekslidmaatschap hebben.

Volg de onderstaande stappen om uw abonnement op een campagne in te stellen.

1. Maak een campagne. [ Leer meer ](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Selecteer op het tabblad **[!UICONTROL Actions]** ten minste één actie.

1. Selecteer **[!UICONTROL Message Optimization]** in de sectie **[!UICONTROL Targeting]** .

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. Gebruik de regelbouwer om uw criteria te bepalen. Definieer bijvoorbeeld een regel voor inwoners van de VS, een regel voor inwoners van Frankrijk en een regel voor inwoners van India.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Selecteer **[!UICONTROL Enable fallback content]** naar wens. Met de inhoud voor alternatieven kan uw doelgroep een standaardinhoud ontvangen wanneer geen specifieke doelregels zijn gekwalificeerd. Als u deze optie niet selecteert, ontvangen alle doelgroepen die niet in aanmerking komen voor een hierboven gedefinieerde doelregel geen inhoud.

1. Sla de instellingen voor de doelregel op.

1. Selecteer **[!UICONTROL Actions]** weer op het tabblad Campagne **[!UICONTROL Edit content]** .

1. Ontwerp aangewezen inhoud voor elke groep die door uw het richten regelmontages wordt bepaald.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   In dit voorbeeld, ontwerp een specifieke inhoud voor inwoners van de V.S., een verschillende inhoud voor Franse ingezetenen en een andere inhoud voor inwoners van India.

1. [ activeer ](review-activate-campaign.md) uw campagne.

Als de campagne eenmaal live is, wordt inhoud die op maat is gemaakt voor elke doelgroep verzonden, zodat inwoners van de VS een specifieke boodschap krijgen, inwoners van Frankrijk een andere boodschap krijgen enzovoort.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## Gebruik experimenteren {#experimentation}

Met behulp van experimenten kunt u meerdere versies van de inhoud testen om te bepalen wat het beste werkt op basis van vooraf gedefinieerde succeswaarden.

Volg de onderstaande stappen om experimenten in een campagne op te zetten.

Stel dat u de volgende promotieberichten in een campagne wilt testen:

* **Behandeling A**: &quot;20% van uw volgende aankoop&quot;
* **Behandeling B**: &quot;Vrije verschepen op orden boven $50&quot;
* **Behandeling C**: &quot;Krijg uw $10 geschenkkaart&quot;

Volg de onderstaande stappen om experimenten in te stellen en te bepalen welk bericht de meeste aankopen aanstuurt.

1. Maak een campagne. [ Leer meer ](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Van het **[!UICONTROL Actions]** lusje, selecteer minstens twee binnenkomende acties, bijvoorbeeld [ code-gebaseerde ervaring ](../code-based/get-started-code-based.md) en [ in-app ](../../rp_landing_pages/in-app-landing-page.md).

1. Selecteer **[!UICONTROL Message Optimization]** in de sectie **[!UICONTROL Experimentation]** .

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Ontwerp en configureer uw content-experiment naar wens. [ leer hoe ](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Zodra het experiment wordt bepaald, is het op alle acties van toepassing die in die campagne worden opgenomen, betekenend dat de zelfde klanten de zelfde aanbiedingen over alle oppervlakten zien.

   >[!NOTE]
   >
   >U kunt andere acties selecteren: de experimentatie is van toepassing op alle acties die aan de campagne zijn toegevoegd.

1. [ activeer ](review-activate-campaign.md) uw campagne.

Wanneer de campagne live is, worden de verschillende inhoudvariaties willekeurig toegewezen aan gebruikers. [!DNL Journey Optimizer] houdt bij welke variatie meer aankopen drijft en actioneerbare inzichten verstrekt.

Volg het succes van uw campagne met het [ campagnerapport van de Experimentatie ](../reports/campaign-global-report-cja-experimentation.md).

## Doelstellingen en experimenten combineren {#combination}

Met Journey Optimizer kunt u ook gerichte toepassingen en experimenten combineren in één campagne om geavanceerdere strategieën te ontwikkelen.

U kunt doelgericht gebruiken om verschillende varianten te maken. Voor elke variant kunt u experimenteren om elke inhoud verder te optimaliseren. Dit zorgt ervoor dat experimenten specifiek zijn voor elke doelregel en zich niet uitstrekken over verschillende varianten binnen de campagne.

U kunt bijvoorbeeld een &#39;50% korting op promotie&#39; testen in plaats van een &#39;50% cadeaukaart&#39; voor klanten in de VS en een andere test uitvoeren voor klanten in Europa, zoals &#39;gratis verzending voor bestellingen van meer dan 50 euro&#39; in plaats van &#39;20% korting op hun volgende aankoop&#39;.

Volg onderstaande stappen om zowel gerichte als experimentele acties in een campagne te combineren.

1. Maak een campagne waarin u verschillende doelregels definieert. [ leer hoe ](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Maak een experiment voor de eerste doelregel.

1. Ontwerp en configureer uw content-experiment naar wens. [ leer hoe ](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Zodra de experimentatie wordt bepaald, is het slechts op de eerste gerichte regel van toepassing.

1. Selecteer **[!UICONTROL Actions]** weer op het tabblad Campagne **[!UICONTROL Edit content]** .

1. Voor de groep die door uw eerste het richten regel wordt bepaald, kunt u een specifieke inhoud voor elke variant van uw experiment bepalen.

   Als u meer dan één binnenkomende actie aan uw campagne toevoegde, is de zelfde combinatie gericht en experiment op elke actie van toepassing. Nochtans, moet u een specifieke inhoud voor elke variant van elke actie bepalen.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Ga zo gelijkaardig voor andere het richten regels te werk, en ontwerp de overeenkomstige inhoud voor elke variant.

1. Sparen uw veranderingen en [ activeer ](review-activate-campaign.md) uw campagne.

Zodra de campagne live is, worden gebruikers van elke doelgroep willekeurig toegewezen aan de verschillende inhoudvariaties die zijn gedefinieerd voor de groep waartoe ze behoren.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->
