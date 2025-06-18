---
solution: Journey Optimizer
product: journey optimizer
title: Werken met regelsets
description: Leer hoe u regelsets maakt en toepast
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: bericht, frequentie, regels, druk
exl-id: 80bd5a61-1368-435c-9a9a-dd84b9e4c208
source-git-commit: 37eed59b64a8bfad0b216c279b15612b6ac57897
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Frequentiecapaciteit per kanaal en communicatietype {#rule-sets}

**de regelreeksen van het Kanaal** passen het afschilderen regels op communicatiekanalen toe. Verzend bijvoorbeeld niet meer dan 1 e-mail- of sms-communicatie per dag.

De reeksen van de kanaalregel van hefboomwerking staat u toe om frequentie het begrenzen door communicatie type te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. Bijvoorbeeld, kunt u een regel tot stand brengen die wordt geplaatst om het aantal **promotionele mededelingen** te beperken naar uw klanten en een andere die regel wordt verzonden om het aantal **nieuwsbrieven** te beperken naar hen wordt verzonden. Afhankelijk van het type campagne dat u creeert, kunt u dan verkiezen om of de promotionele mededeling of de nieuwsbrieven regelreeks toe te passen.

## Een regel voor kanaaluitlijning maken

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Bepaal de kanalen waarop de regel van toepassing is"
>abstract="Selecteer ten minste één kanaal. De bedekking wordt toegepast over kanalen als totale telling."

Ga als volgt te werk om een kanaalregelset te maken:

>[!NOTE]
>
>U kunt tot 10 actieve lokale regelreeksen voor kanaaldomein en voor het reisdomein tot stand brengen.

1. Open de lijst **[!UICONTROL Rules sets]** en klik vervolgens op **[!UICONTROL Create rule set]** .

   ![](assets/rule-sets-create-button.png)

1. Selecteer de regelset waaraan u de afkapregel wilt toevoegen of maak een nieuwe regelset:

   * Om een bestaande regelreeks te gebruiken, selecteer het van de lijst. Regels voor kanaalbegrenzing kunnen alleen worden toegevoegd aan regelsets met het &#39;kanaal&#39;-domein. U kunt deze informatie controleren in de lijsten met regelsets in de kolom **[!UICONTROL Domain]** .

     ![](assets/journey-capping-list.png)

   * Als u een nieuwe regelset wilt maken met de uitlijningsregel, klikt u op **[!UICONTROL Create rule set]** , geeft u een unieke naam voor de regelset op en selecteert u &#39;Kanaal&#39; in de vervolgkeuzelijst **[!UICONTROL Rule Set Domain]** en klikt u vervolgens op **[!UICONTROL Save]** .

     ![](assets/rule-sets-create.png)

1. In het scherm van de regelreeks, klik de **[!UICONTROL Add Rule]** knoop en bepaal een unieke naam voor de regel.

1. Het **gebied van de Categorie** specificeert de categorie van bericht de regel op van toepassing is. Momenteel is dit veld alleen-lezen, aangezien alleen de categorie **[!UICONTROL Marketing]** beschikbaar is.

   ![](assets/rule-set-channels.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Duration]** of u de uitlijning maandelijks, wekelijks of dagelijks wilt toepassen. De frequentiegrens is gebaseerd op de geselecteerde kalenderperiode. Deze wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader.

   De teller loopt voor elke periode als volgt af:

   * **[!UICONTROL Monthly]**: Het frequentiekapitaal is geldig tot de laatste dag van de maand bij 23 :59: 59 UTC. Bijvoorbeeld, is de maandelijkse vervaldatum voor Januari 01-31 23 :59: 59 UTC.

   * **[!UICONTROL Weekly]**: Het frequentiekapitaal is geldig tot Zaterdag 23 :59: 59 UTC van die week aangezien de kalenderweek op zondag begint. De vervaldatum is van toepassing ongeacht wanneer de regel is gemaakt. Bijvoorbeeld, als de regel op Donderdag wordt gecreeerd, is deze regel geldig tot Zaterdag bij 23 :59: 59.

   * **[!UICONTROL Daily]**: Het dagelijkse frequentiekapitaal is geldig voor de dag tot 23 :59: 59 UTC en stelt aan 0 bij het begin van de volgende dag terug.

     >[!CAUTION]
     > 
     >Om ervoor te zorgen dat de regels voor dagelijkse frequentiecapping correct zijn, moet u de naamruimte met de hoogste prioriteit kiezen tijdens het ontwerpen van een campagne of een reis. Leer meer over namespace prioriteit in de [ gids van de Dienst van de Identiteit van het Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

   Houd er rekening mee dat de waarde van de profielteller wordt bijgewerkt wanneer de communicatie wordt geleverd. Begrijpt u dit wanneer u grote hoeveelheden communicatie verzendt aangezien de productie in de ontvanger zou kunnen resulteren die de e-mailnotulen of zelfs uren na de inleiding van de mededeling (in het geval dat u miljoenen mededelingen gelijktijdig verzendt) krijgen.

   Dit is van belang wanneer een ontvanger twee mededelingen dicht bij elkaar ontvangt. We stellen voor om communicatie met elkaar te scheiden met minstens twee uur, waar mogelijk, zodat de ontvanger voldoende tijd heeft om de communicatie te ontvangen en de tegenwaarde dienovereenkomstig bij te werken.

1. Stel de plafonnering voor uw regel in. Dit betekent het maximumaantal berichten dat naar een individueel gebruikersprofiel kan worden verzonden per maand, week of dag - volgens de bovenstaande selectie.

1. Selecteer het kanaal dat u voor deze regel wilt gebruiken: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Push notification]** of **[!UICONTROL Direct mail]** .

1. Selecteer meerdere kanalen als u de afdekking op alle geselecteerde kanalen als een totaal aantal wilt toepassen.

   Stel de aftopping bijvoorbeeld in op 5 en selecteer zowel het e-mailadres als het sms-kanaal. Als een profiel al 3 marketingberichten en 2 marketingberichten voor de geselecteerde periode heeft ontvangen, wordt dit profiel uitgesloten van de eerstvolgende levering van een marketingbericht of -bericht.

1. Klik op **[!UICONTROL Save]** om het maken van de regel te bevestigen. Uw bericht wordt toegevoegd aan de regelset, met de status **[!UICONTROL Draft]** .

   ![](assets/rule-set-rule-created.png)

1. Herhaal bovenstaande stappen om zoveel regels toe te voegen als nodig zijn voor de regelset.

1. Wanneer de begrenzingsregel klaar is om op berichten te worden toegepast, activeer de regelreeks en de regel waar het is toegevoegd. [ Leer hoe te om regelreeksen te activeren ](../conflict-prioritization/rule-sets.md#create)

## Regelsets toepassen op een bericht {#apply-frequency-rule}

Voer de volgende stappen uit om een regel toe te passen die op een bericht is ingesteld:

1. Wanneer het creëren van een reis of campagnebericht, selecteer één van de kanalen u voor uw regelreeks bepaalde en geef de inhoud van uw bericht uit

1. Klik op de knop **[!UICONTROL Add Business Rule]** in het scherm voor de inhoudseditie.

1. Selecteer de regelset die u hebt gemaakt.

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Slechts [ geactiveerde ](#activate-rule) regelreeksen tonen in de lijst.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Voordat u uw reis of campagne activeert, moet u ervoor zorgen dat de uitvoering ervan ten minste 20 minuten in de toekomst wordt gepland.

   Dit staat voor voldoende tijd toe om de tellerwaarden op het profiel voor de bedrijfsregel te bevolken u selecteerde. Als u de campagne onmiddellijk activeert, zullen de de tellerwaarden van de regelreeks niet op de profielen van de ontvangers bevolken, en het bericht zal niet naar hun frequentie het begrenzen regels voor de reeksen van de douaneregel worden geteld.

   ![](assets/rule-set-schedule-campaign.png)

1. U kunt het aantal profielen bekijken die van levering in het [ rapport van Customer Journey Analytics ](../reports/report-gs-cja.md) worden uitgesloten, en in het [ Levende rapport ](../reports/live-report.md), waar de frequentieregels als mogelijke reden voor gebruikers zullen worden vermeld die van levering worden uitgesloten.

>[!NOTE]
>
>Verschillende regels kunnen op hetzelfde kanaal van toepassing zijn, maar wanneer het onderste hoofdlettergebruik is bereikt, wordt het profiel uitgesloten van de volgende leveringen.

Wanneer het testen van frequentieregels, wordt het geadviseerd om een pas gecreeerd [ testprofiel ](../audience/creating-test-profiles.md) te gebruiken, omdat zodra de de frequentiedrempel van een profiel wordt bereikt, er geen manier is om de teller tot de volgende periode terug te stellen. Als u een regel deactiveert, kunnen beperkte profielen berichten ontvangen, maar worden er geen tellerverhogingen verwijderd of verwijderd.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435531?quality=12)
