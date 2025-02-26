---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: Belangrijke stappen om uw eerste journey met Adobe Journey Optimizer te maken
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 93dab17fc74396887e3b68051be777645e02709f
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 4%

---

# Uw eerste journey maken {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Reizen maken"
>abstract="Het gebruik **Adobe Journey Optimizer** om in real time het gebruikscase van het orkestgebruik te bouwen gebruikend contextafhankelijke gegevens die in gebeurtenissen of gegevensbronnen worden opgeslagen."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Ontwerpen van klantritten om persoonlijke, contextuele ervaringen te bieden. Met Journey Optimizer kunt u in real-time gebruikmaken van het orkestgebruik en contextuele gegevens opslaan in gebeurtenissen of gegevensbronnen. Het **Overzicht** lusje toont een dashboard met zeer belangrijke metriek met betrekking tot uw reizen. Het **doorbladert** lusje toont de lijst van bestaande reizen."

Adobe Journey Optimizer bevat een omnichannel orchestration canvas dat marketers in staat stelt marketingactiviteiten te harmoniseren met een-op-een-klantenservice. Met de gebruikersinterface kunt u activiteiten van het palet naar het canvas slepen om uw reis te maken. Het interface van de reisgebruiker wordt gedetailleerd in [ deze pagina ](journey-ui.md).

![ steekproef van wegcanvas ](assets/journey38.png)


De belangrijkste stappen om een reis tot stand te brengen zijn gedetailleerd in deze pagina. Zij worden als volgt gestroomlijnd:

![ stappen van de reisverwezenlijking: creeer, ontwerp, test, en publiceer ](assets/journey-creation-process.png)


Bouw multi-step klantenreizen een opeenvolging van interactie, aanbiedingen, en berichten over kanalen in echt in werking stellen - tijd. Deze benadering zorgt ervoor dat klanten op de optimale momenten worden betrokken die op hun acties en relevante bedrijfssignalen worden gebaseerd. Het doelpubliek kan worden gedefinieerd op basis van gedrag, contextuele gegevens en bedrijfsgebeurtenissen. De vereisten hangen van uw gebruiksgeval af, en het [ type van reis ](entry-management.md#types-of-journeys) u bouwt. Voordat u begint met het ontwerpen van uw reis, controleert u of de relevante configuratiestappen zijn uitgevoerd:

* Als u uw reizen wilt teweegbrengen tijdelijk wanneer een gebeurtenis wordt ontvangen, moet u **een gebeurtenis** vormen. U bepaalt de verwachte informatie en hoe te om het te verwerken. [Meer informatie](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Uw reis kan ook naar het publiek van Adobe Experience Platform luisteren om berichten in partij naar een gespecificeerde reeks profielen te verzenden. Voor dit, moet u **publiek** creëren. [Meer informatie](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* U kunt een verbinding met een systeem bepalen om extra informatie terug te winnen die in uw reizen, bijvoorbeeld in uw voorwaarden zal worden gebruikt. Deze verbinding baseert zich op a **gegevensbron**. [Meer informatie](../datasource/about-data-sources.md)

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer komt met [ ingebouwde berichtmogelijkheden ](../building-journeys/journeys-message.md). Als u een derdesysteem gebruikt om uw berichten te verzenden, kunt u **tot een douaneactie** leiden. Leer meer in deze [ sectie ](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Als gegevensingenieur, zijn de stappen om uw reizen, met inbegrip van Gegevensbronnen, Gebeurtenissen en Acties te vormen gedetailleerd in [ deze sectie ](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>De gidsen en de beperkingen van de reis zijn gedetailleerd in [ deze pagina ](../start/guardrails.md)

## Een journey maken {#jo-build}

Voer de volgende stappen uit om een reis in meerdere stappen te maken:

1. Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** .

1. Klik op de knop **[!UICONTROL Create Journey]** om een nieuwe rit te maken.

1. Bewerk het configuratievenster van de rit om de naam van de rit te definiëren en de eigenschappen ervan in te stellen. Leer hoe te om de eigenschappen van uw reis in [ te plaatsen deze pagina ](journey-properties.md).

   ![](assets/jo-properties.png)

U kunt dan beginnen uw reis te ontwerpen.

## De reis ontwerpen {#jo-design}

De omnichannel reisontwerper helpt u multi-step reizen met gericht publiek, updates bouwen die op klanten of bedrijfsinteractie in real time worden gebaseerd, en omnichannel berichten gebruikend een intuïtieve belemmering-en-dalingsinterface.

![](assets/journey38.png)

1. Begin door een gebeurtenis te slepen en te laten vallen of a **las de activiteit van het publiek** van het palet in het canvas. Meer over reisontwerp leren, verwijs naar [ deze sectie ](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Sleep de volgende stappen die het individu zal volgen en zet ze neer. U kunt bijvoorbeeld een voorwaarde toevoegen, gevolgd door een kanaalactie. Meer over activiteiten leren, verwijs naar [ deze sectie ](about-journey-activities.md).

## De reis testen {#jo-test}

Nadat u uw reis hebt gemaakt, kunt u deze testen voordat u de site publiceert. Journey Optimizer biedt &quot;testmodus&quot; als een manier om testprofielen te bekijken terwijl ze op reis gaan en mogelijke fouten vóór activering op te sporen. Door snelle tests uit te voeren kunt u controleren of de reizen correct werken, zodat u ze met vertrouwen kunt publiceren.

Leer meer in deze [ sectie ](testing-the-journey.md)

## De reis publiceren {#jo-pub}

U moet een reis publiceren om het te activeren en het ter beschikking te stellen voor nieuwe profielen om het in te gaan. Voordat u uw reis publiceert, controleert u of deze geldig is en of er geen fout optreedt. U kunt geen reis met fouten publiceren. Leer meer over de reispublicatie in deze [ sectie ](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Na publicatie kunt u uw reis controleren met behulp van de speciale rapportagetools om de effectiviteit van uw reis te meten.

![](assets/jo-dynamic_report_journey_12.png)

Leer meer over reisrapporten in deze [ sectie ](../reports/live-report.md).

>[!NOTE]
>
>Als u aan a **levende** reis moet wijzigen, [ creeer een nieuwe versie ](journey-ui.md#journey-versions) van uw reis.
