---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: Belangrijke stappen om uw eerste journey met Adobe Journey Optimizer te bouwen
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 3%

---

# Uw eerste journey maken {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Reizen maken"
>abstract="Het gebruik **Adobe Journey Optimizer** om in real time het gebruikscase van het orkestgebruik te bouwen gebruikend contextafhankelijke gegevens die in gebeurtenissen of gegevensbronnen worden opgeslagen."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Ontwerpen van klantritten om persoonlijke, contextuele ervaringen te bieden. Met Journey Optimizer kunt u gebruiksscenario&#39;s voor realtime orchestratie maken met contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen. Het **Overzicht** lusje toont een dashboard met zeer belangrijke metriek met betrekking tot uw reizen. Het **doorbladert** lusje toont de lijst van bestaande reizen."

Adobe Journey Optimizer bevat een omnichannel orchestration canvas dat marketers in staat stelt marketingactiviteiten te harmoniseren met een-op-een-klantenservice. Met de gebruikersinterface kunt u activiteiten van het palet naar het canvas slepen om uw reis te maken. Het interface van de reisgebruiker is gedetailleerd op [ deze pagina ](journey-ui.md).

![ steekproef van wegcanvas ](assets/journey38.png)


De belangrijkste stappen om een reis tot stand te brengen zijn gedetailleerd op deze pagina. Zij worden als volgt gestroomlijnd:

![ stappen van de reisverwezenlijking: creeer, ontwerp, test, en publiceer ](assets/journey-creation-process.png)


Bouw uit meerdere stappen klantenreizen om een opeenvolging van interactie, aanbiedingen, en berichten over kanalen in real time in werking te stellen. Deze benadering zorgt ervoor dat klanten op de optimale momenten worden betrokken die op hun acties en relevante bedrijfssignalen worden gebaseerd. Het doelpubliek wordt gedefinieerd op basis van gedrag, contextuele gegevens en bedrijfsgebeurtenissen. De vereisten hangen van uw gebruiksgeval en het [ type van reis ](entry-management.md#types-of-journeys) af u bouwt.

Voordat u begint met het bouwen van uw reis, dient u ervoor te zorgen dat de relevante configuratiestappen zijn voltooid:

* Als u uw reizen individueel wilt teweegbrengen wanneer een gebeurtenis wordt ontvangen, **vormt een gebeurtenis**. Definieer de verwachte informatie en hoe deze moet worden verwerkt. [Meer informatie](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Uw reis kan aan het publiek van Adobe Experience Platform ook luisteren om berichten in partijen naar een gespecificeerde reeks profielen te verzenden. Voor dit, **creeer publiek**. [Meer informatie](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* Definieer een verbinding met een systeem om aanvullende informatie op te halen die bijvoorbeeld in uw omstandigheden tijdens uw reizen wordt gebruikt. Deze verbinding baseert zich op a **gegevensbron**. [Meer informatie](../datasource/about-data-sources.md).

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer komt met [ ingebouwde berichtmogelijkheden ](../building-journeys/journeys-message.md). Als u een derdesysteem gebruikt om uw berichten te verzenden, kunt u **tot een douaneactie** leiden. Leer meer in deze [ sectie ](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Als gegevensingenieur, zijn de stappen om uw reizen, met inbegrip van Gegevensbronnen, Gebeurtenissen en Acties te vormen gedetailleerd in [ deze sectie ](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>De de gidsen en beperkingen van de reis zijn gedetailleerd op [ deze pagina ](../start/guardrails.md)

## Een journey maken {#jo-build}

Voer de volgende stappen uit om een reis in meerdere stappen te maken:

1. Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** .

1. Klik op de knop **[!UICONTROL Create Journey]** om een nieuwe rit te maken.

1. Bewerk het configuratievenster van de rit om de naam van de rit te definiëren en de eigenschappen ervan in te stellen. Leer hoe te om de eigenschappen van uw reis op [ te plaatsen deze pagina ](journey-properties.md).

   ![](assets/jo-properties.png)

U kunt dan beginnen uw reis te ontwerpen.

## De reis ontwerpen {#jo-design}

De omnichannel reisontwerper helpt u multi-step reizen met gericht publiek, updates bouwen die op klanten of bedrijfsinteractie in real time worden gebaseerd, en omnichannel berichten gebruikend een intuïtieve belemmering-en-dalingsinterface.

![](assets/journey38.png)

1. Begin door een gebeurtenis te slepen en te laten vallen of a **las de activiteit van het publiek** van het palet in het canvas. Meer over reisontwerp leren, verwijs naar [ deze sectie ](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Begin door een gebeurtenis of a **Gelezen activiteit van het publiek** van het palet in het canvas te slepen en te laten vallen. Meer over reisontwerp leren, verwijs naar [ deze sectie ](using-the-journey-designer.md).

## De reis testen {#jo-test}

Als u uw reis hebt gemaakt, test u deze voordat u publiceert. Journey Optimizer biedt de wijze van de a **Test** als manier aan om testprofielen te bekijken aangezien zij zich langs de reis bewegen, die potentiële fouten vóór activering ontdekken. Door snelle tests uit te voeren, zorgt u ervoor dat de reizen correct werken, zodat u ze met vertrouwen kunt publiceren. Leer hoe te om uw reis [ in deze sectie ](testing-the-journey.md) te testen

U kunt uw reis in **Droog looppas** ook uitvoeren. Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken. Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren. Leer hoe te om een reis op Dry looppas wijze [ in deze sectie ](journey-dry-run.md) te publiceren.

## De reis publiceren {#jo-pub}

U moet een reis publiceren om het te activeren en het ter beschikking te stellen voor nieuwe profielen om het in te gaan. Voordat u uw reis publiceert, controleert u of deze geldig is en of er geen fouten zijn. U kunt geen reis met fouten publiceren. Leer meer over reispublicatie in deze [ sectie ](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Na publicatie kunt u uw reis controleren met behulp van de speciale rapportagetools om de effectiviteit van uw reis te meten.

![](assets/jo-dynamic_report_journey_12.png)

Leer meer over reisrapporten in deze [ sectie ](../reports/live-report.md).

>[!NOTE]
>
>Als u a **levende** reis moet wijzigen, [ creeer een nieuwe versie ](journey-ui.md#journey-versions) van uw reis.
