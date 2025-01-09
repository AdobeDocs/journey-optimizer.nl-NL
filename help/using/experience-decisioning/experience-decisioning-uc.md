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
source-git-commit: ff17e7609eb6504632d35671a4bd2aa11a613372
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 3%

---

# Gebruiksscenario voor beslissing {#experience-decisioning-uc}

In dit geval worden alle stappen beschreven die nodig zijn om Decisioning te gebruiken met het op code gebaseerde kanaal van [!DNL Journey Optimizer] .

In dit voorbeeld bent u niet zeker of een specifieke rangschikkingsformule beter zal presteren dan de vooraf toegewezen aanbiedingsprioriteiten.

Om te meten welke het beste voor uw doelpubliek presteert, creeer een campagne gebruikend [ Experimenteer van de Inhoud ](../content-management/content-experiment.md) waar u twee leveringsbehandelingen bepaalt:

* De eerste behandeling gebruikt prioriteit als rangorde methode.
* De tweede behandeling gebruikt een formule: de rangorde.

## Selectiestrategieën maken

Ten eerste moet u twee selectiestrategieën ontwikkelen: een met prioriteit als rangschikkingsmethode en een andere met een formule als rangschikkingsmethode.

### De eerste selectiestrategie maken

Volg de onderstaande stappen om de eerste selectiestrategie met prioriteit als rangordemethode te maken.

1. Maak een beslissingsitem. [ leer hoe ](items.md)

1. Stel de **[!UICONTROL Priority]** van het beslissingsitem in vergelijking met andere. Als een profiel voor meerdere items in aanmerking komt, krijgt het item met een hogere prioriteit voorrang boven andere items.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >De prioriteit is een gegevenstype van gehele getallen. Alle attributen die geheelgegevenstypes zijn zouden geheelwaarden (geen decimalen) moeten bevatten.

1. Bepaal de geschiktheid van het besluitvormingspunt:

   * Bepaal publiek of regels om het punt tot specifieke profielen slechts te beperken. [Meer informatie](items.md#eligibility)

   * Stel de begrenzingsregels in om het maximumaantal keren te bepalen dat een aanbieding kan worden gepresenteerd. [Meer informatie](items.md#capping)

1. Herhaal indien nodig de bovenstaande stappen om aanvullende beslissingsitems te maken.

1. Creeer a **inzameling** waar uw besluitvormingspunt(en) zal worden omvat. [Meer informatie](collections.md)

1. Creeer a [ selectiestrategie ](selection-strategies.md#create-selection-strategy) en selecteer de [ inzameling ](collections.md) die de te overwegen aanbieding(en) bevat.

1. [ kies de het rangschikken methode ](#select-ranking-method) om de beste aanbieding voor elk profiel te selecteren. Selecteer in dit geval **[!UICONTROL Offer priority]** : als meerdere aanbiedingen in aanmerking komen voor deze strategie, gebruikt de engine voor besluitvorming de waarde die is ingesteld als **[!UICONTROL Priority]** in de aanbieding(en). [Meer informatie](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

### De tweede selectiestrategie maken

Volg onderstaande stappen om de tweede selectiestrategie samen te stellen met een formule als waarderingsmethode te selecteren.

1. Maak een beslissingsitem. [ leer hoe ](items.md)

   <!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Bepaal de geschiktheid van het besluitvormingspunt:

   * Bepaal publiek of regels om het punt tot specifieke profielen slechts te beperken. [Meer informatie](items.md#eligibility)

   * Stel de begrenzingsregels in om het maximumaantal keren te bepalen dat een aanbieding kan worden gepresenteerd. [Meer informatie](items.md#capping)

1. Herhaal indien nodig de bovenstaande stappen om aanvullende beslissingsitems te maken.

1. Creeer a **inzameling** waar uw besluitvormingspunt(en) zal worden omvat. [Meer informatie](collections.md)

1. Creeer a [ selectiestrategie ](selection-strategies.md#create-selection-strategy) en selecteer de [ inzameling ](collections.md) die de te overwegen aanbieding(en) bevat.

1. [ kies de het rangschikken methode ](#select-ranking-method) u wilt gebruiken om de beste aanbieding voor elk profiel te selecteren. Selecteer in dit geval **[!UICONTROL Formula]** om een specifieke berekende score te gebruiken om te bepalen welke geschikte aanbieding moet worden gedaan. [Meer informatie](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

## Een op code gebaseerde ervaringscampagne maken

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

Zodra u de twee selectiestrategieën vormde, creeer een code-gebaseerde ervaringscampagne waar u een verschillende behandeling voor elke strategie bepaalt om te vergelijken welke het beste presteert.

1. Maak een campagne en selecteer de handeling **[!UICONTROL Code-base experience]** . [Meer informatie](../code-based/create-code-based.md)

1. Klik in de overzichtspagina van de campagne op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren. [Meer informatie](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png)

1. Selecteer of maak een op code gebaseerde configuratie in de overzichtspagina van de campagne en klik op **[!UICONTROL Edit content]** .

   ![](assets/exd-uc-edit-cbe-content.png)

<!--1. Sart personalizing **Treatment A** by clicking **[!UICONTROL Create]**.

    ![](assets/exd-uc-create-treatment-a.png)-->

1. Van het venster van de inhoudsuitgave, begin **Behandeling A** te personaliseren door **[!UICONTROL Edit code]** te klikken.

   ![](assets/exd-uc-experiment-treatment-a.png)

1. Selecteer **[!UICONTROL Decision policy]** , klik op **[!UICONTROL Add decision policy]** en vul de beslissingsdetails in. [Meer informatie](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Selecteer de eerste strategie die u hebt gemaakt. Klik op **[!UICONTROL Add strategy]**.

1. Klik op **[!UICONTROL Create]**. De nieuwe beslissing wordt toegevoegd onder **[!UICONTROL Decisions]** .

   ![](assets/decision-code-based-decision-added.png)

1. Klik op het pictogram Meer handelingen (drie punten) en selecteer **[!UICONTROL Add]** . Nu kunt u alle beslissingskenmerken toevoegen die u in deze map wilt opnemen.

   ![](assets/decision-code-based-add-decision.png)

1. U kunt ook alle andere kenmerken toevoegen die beschikbaar zijn in de verpersoonlijkingseditor, zoals profielkenmerken.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Van het venster van de inhoudsuitgave, uitgezochte **Behandeling B**, en herhaal de stappen hierboven om een ander besluitvormingsbeleid tot stand te brengen en de tweede selectiestrategie te selecteren die u creeerde.

   ![](assets/exd-uc-experiment-treatment-b.png)

1. Sla uw inhoud op.
