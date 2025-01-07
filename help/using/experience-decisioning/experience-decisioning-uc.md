---
title: Gebruiksscenario voor beslissing
description: Leer hoe te om besluiten tot stand te brengen gebruikend experimenten met het op code-gebaseerde kanaal
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 3%

---

# Gebruiksscenario voor beslissing {#experience-decisioning-uc}

In dit geval worden alle stappen beschreven die nodig zijn om Decisioning te gebruiken met het op code gebaseerde kanaal van [!DNL Journey Optimizer] .

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

In dit geval, bent u onzeker of zal een specifieke rangschikkende formule beter presteren dan de vooraf toegewezen aanbiedingsprioriteiten.

Om te meten welke het beste voor uw doelpubliek presteert, creeer een campagne waar u twee leveringsbehandelingen bepaalt:

<!--Set up the experiment such that:-->

* De eerste behandeling bevat één selectiestrategie met prioriteit als rangordemethode.
* De tweede behandeling bevat een andere selectiestrategie waarvoor een formule de rangorde-methode is.

## Selectiestrategieën maken

Ten eerste moet u twee selectiestrategieën ontwikkelen: een met prioriteit als rangschikkingsmethode en een andere met een formule als rangschikkingsmethode.

### De eerste selectiestrategie maken

Selecteer in de eerste selectiestrategie prioriteit als rangschikkingsmethode. Voer de onderstaande stappen uit.

1. Maak een beslissingsitem. [ leer hoe ](items.md)

1. Stel de **[!UICONTROL Priority]** van het beslissingsitem in vergelijking met andere. Als een profiel voor meerdere items in aanmerking komt, krijgt het item met een hogere prioriteit voorrang boven andere items.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >De prioriteit is een gegevenstype van gehele getallen. Alle attributen die geheelgegevenstypes zijn zouden geheelwaarden (geen decimalen) moeten bevatten.

1. Bepaal publiek of regels om het punt tot specifieke profielen slechts te beperken. [ Leer hoe te om de geschiktheid van het besluitvormingspunt te plaatsen ](items.md#eligibility)

1. Stel de begrenzingsregels in om het maximumaantal keren te bepalen dat een aanbieding kan worden gepresenteerd. [ leer hoe ](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Creeer a **inzameling** waar uw besluitvormingspunt(en) zal worden omvat. [Meer informatie](collections.md)

1. Creeer a **selectiestrategie**. [ leer hoe ](selection-strategies.md#create-selection-strategy)

1. Selecteer de [ inzameling ](collections.md) die de te overwegen aanbieding(en) bevat.

1. [ kies de het rangschikken methode ](#select-ranking-method) om de beste aanbieding voor elk profiel te selecteren. Selecteer in dit geval **[!UICONTROL Offer priority]** . [Meer informatie](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### De tweede selectiestrategie maken

Selecteer in de tweede selectiestrategie een formule als waarderingsmethode. Voer de onderstaande stappen uit.

1. Maak een beslissingsitem. [ leer hoe ](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Bepaal publiek of regels om het punt tot specifieke profielen slechts te beperken. [ Leer hoe te om de geschiktheid van het besluitvormingspunt te plaatsen ](items.md#eligibility)

1. Stel de begrenzingsregels in om het maximumaantal keren te bepalen dat een aanbieding kan worden gepresenteerd. [ leer hoe ](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Creeer a **inzameling** waar uw besluitvormingspunt(en) zal worden omvat. [Meer informatie](collections.md)

1. Creeer a **selectiestrategie**. [ leer hoe ](selection-strategies.md#create-selection-strategy)

1. Selecteer de [ inzameling ](collections.md) die de te overwegen aanbieding(en) bevat.

1. [ selecteer de het rangschikken methode ](#select-ranking-method) u wilt gebruiken om de beste aanbieding voor elk profiel te selecteren. Selecteer in dit geval **[!UICONTROL Formula]** om een specifieke berekende score te gebruiken en te kiezen welke geschikte aanbieding moet worden gedaan. [Meer informatie](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Beslissingsbeleid maken

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Maak een campagne en selecteer de handeling **[!UICONTROL Code-base experience]** . [Meer informatie](../code-based/create-code-based.md)

1. Start vanuit het venster **[!UICONTROL Edit content]** de aanpassing A.

1. Selecteer het pictogram **[!UICONTROL Decisions]** , klik op **[!UICONTROL Create a decision]** en vul de beslissingsdetails in. [Meer informatie](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Selecteer de eerste strategie die u hebt gemaakt. Klik op **[!UICONTROL Add strategy]**.

1. Klik op **[!UICONTROL Create]**. De nieuwe beslissing wordt toegevoegd onder **[!UICONTROL Decisions]** .

   ![](assets/decision-code-based-decision-added.png)

1. Klik op het pictogram Meer handelingen (drie punten) en selecteer **[!UICONTROL Add]** . Nu kunt u alle beslissingskenmerken toevoegen die u in deze map wilt opnemen.

   ![](assets/decision-code-based-add-decision.png)

1. U kunt ook alle andere kenmerken toevoegen die beschikbaar zijn in de verpersoonlijkingseditor, zoals profielkenmerken.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Klik in de overzichtspagina van de campagne op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren. [Meer informatie](../content-management/content-experiment.md)

1. Selecteer in het venster **[!UICONTROL Edit content]** de optie Behandeling B en herhaal de bovenstaande stappen om een andere beslissing te maken.

1. Selecteer de tweede strategie die u hebt gemaakt. Klik op **[!UICONTROL Add strategy]**.

1. Sla uw inhoud op.
