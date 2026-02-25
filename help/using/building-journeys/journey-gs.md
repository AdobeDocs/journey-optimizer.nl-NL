---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste journey maken
description: De belangrijkste stappen om uw eerste reis met  [!DNL Adobe Journey Optimizer] te bouwen
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 2%

---

# Uw eerste journey maken {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Reizen maken"
>abstract="Gebruik **[!DNL Adobe Journey Optimizer]** om in real time orchestratiefase samen te stellen met gebruik van contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Ontwerpen van klantritten om persoonlijke, contextuele ervaringen te bieden. Met Journey Optimizer kunt u gebruiksscenario&#39;s voor realtime orchestratie maken met contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen. Het **Overzicht** lusje toont een dashboard met zeer belangrijke metriek met betrekking tot uw reizen. Het **doorbladert** lusje toont de lijst van bestaande reizen."

[!DNL Adobe Journey Optimizer] bevat een omnichannel orchestration canvas dat marketers in staat stelt marketingactiviteiten te harmoniseren met een-op-een-klantenservice. Met de gebruikersinterface kunt u activiteiten van het palet naar het canvas slepen om uw reis te maken. Het interface van de reisgebruiker is gedetailleerd op [&#x200B; deze pagina &#x200B;](journey-ui.md).

![&#x200B; steekproef van wegcanvas &#x200B;](assets/journey38.png)

De belangrijkste stappen om een reis tot stand te brengen zijn gedetailleerd op deze pagina. Zij worden als volgt gestroomlijnd:

![&#x200B; stappen van de reisverwezenlijking: creeer, ontwerp, test, en publiceer &#x200B;](assets/journey-creation-process.png)


Bouw uit meerdere stappen klantenreizen om een opeenvolging van interactie, aanbiedingen, en berichten over kanalen in real time in werking te stellen. Deze benadering zorgt ervoor dat klanten op de optimale momenten worden betrokken die op hun acties en relevante bedrijfssignalen worden gebaseerd. Het doelpubliek wordt gedefinieerd op basis van gedrag, contextuele gegevens en bedrijfsgebeurtenissen. De vereisten hangen van uw gebruiksgeval en het [&#x200B; type van reis &#x200B;](entry-management.md#types-of-journeys) af u bouwt.

Leer meer over hoe de profielen door reizen en de tarieven van de reisverwerking in [&#x200B; deze sectie &#x200B;](entry-management.md#journey-processing-rate) stromen.

Voordat u begint met het bouwen van uw reis, dient u ervoor te zorgen dat de relevante configuratiestappen zijn voltooid:

* Als u uw reizen individueel wilt teweegbrengen wanneer een gebeurtenis wordt ontvangen, **vormt een gebeurtenis**. Definieer de verwachte informatie en hoe deze moet worden verwerkt. [Meer informatie](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Uw reis kan aan het publiek van Adobe Experience Platform ook luisteren om berichten in partijen naar een gespecificeerde reeks profielen te verzenden. Voor dit, **creeer publiek**. [Meer informatie](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* Definieer een verbinding met een systeem om aanvullende informatie op te halen die bijvoorbeeld in uw omstandigheden tijdens uw reizen wordt gebruikt. Deze verbinding baseert zich op a **gegevensbron**. [Meer informatie](../datasource/about-data-sources.md).

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer komt met [&#x200B; ingebouwde berichtmogelijkheden &#x200B;](../building-journeys/journey-action.md). Als u een derdesysteem gebruikt om uw berichten te verzenden, kunt u **tot een douaneactie** leiden. Leer meer in deze [&#x200B; sectie &#x200B;](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Als gegevensingenieur, zijn de stappen om uw reizen, met inbegrip van Gegevensbronnen, Gebeurtenissen en Acties te vormen gedetailleerd in [&#x200B; deze sectie &#x200B;](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>De de gidsen en beperkingen van de reis zijn gedetailleerd op [&#x200B; deze pagina &#x200B;](../start/guardrails.md)

## Een journey maken {#jo-build}

Voer de volgende stappen uit om een reis in meerdere stappen te maken:

1. Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** .

1. Klik op de knop **[!UICONTROL Create Journey]** om een nieuwe rit te maken.

1. Bewerk het configuratievenster van de rit om de naam van de rit te definiëren en de eigenschappen ervan in te stellen. Leer hoe te om de eigenschappen van uw reis op [&#x200B; te plaatsen deze pagina &#x200B;](journey-properties.md).

   ![&#x200B; Reis eigenschappen paneel met montages en configuratieopties &#x200B;](assets/jo-properties.png)

U kunt dan beginnen uw reis te ontwerpen.

## De reis ontwerpen {#jo-design}

De omnichannel reisontwerper helpt u multi-step reizen met gericht publiek, updates bouwen die op klanten of bedrijfsinteractie in real time worden gebaseerd, en omnichannel berichten gebruikend een intuïtieve belemmering-en-dalingsinterface.

![&#x200B; de ontwerperinterface van de Reis met activiteitenpalet en canvas &#x200B;](assets/journey38.png)

1. Begin door een gebeurtenis te slepen en te laten vallen of a **las de activiteit van het publiek** van het palet in het canvas. Meer over reisontwerp leren, verwijs naar [&#x200B; deze sectie &#x200B;](using-the-journey-designer.md).

   ![&#x200B; las de activiteitenconfiguratie van het publiek voor het selecteren van doelpubliek &#x200B;](assets/read-segment.png)

1. De belemmering en laat vallen een gebeurtenis of a **las de activiteit van het publiek** van het palet in het canvas. Meer over reisontwerp leren, verwijs naar [&#x200B; deze sectie &#x200B;](using-the-journey-designer.md).

## De reis testen {#jo-test}

Als u uw reis hebt gemaakt, test u deze voordat u publiceert. Journey Optimizer biedt de wijze van de a **Test** als manier aan om testprofielen te bekijken aangezien zij zich langs de reis bewegen, die potentiële fouten vóór activering ontdekken. Door snelle tests uit te voeren, zorgt u ervoor dat de reizen correct werken, zodat u ze met vertrouwen kunt publiceren. Leer hoe te om uw reis [&#x200B; in deze sectie &#x200B;](testing-the-journey.md) te testen

U kunt uw reis in **Droog looppas** ook uitvoeren. Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken. Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren. Leer hoe te om een reis op Dry looppas wijze [&#x200B; in deze sectie &#x200B;](journey-dry-run.md) te publiceren.

## De reis publiceren {#jo-pub}

U moet een reis publiceren om het te activeren en het ter beschikking te stellen voor nieuwe profielen om het in te gaan. Voordat u uw reis publiceert, controleert u of deze geldig is en of er geen fouten zijn. U kunt geen reis met fouten publiceren. Leer meer over reispublicatie in deze [&#x200B; sectie &#x200B;](publish-journey.md).

![&#x200B; Volledige reisstroom met publiek, voorwaarden, en acties &#x200B;](assets/jo-journeyuc2_32bis.png)

Na publicatie kunt u uw reis controleren met behulp van de speciale rapportagetools om de effectiviteit van uw reis te meten.

![&#x200B; rapport van de Analyse van de Reis die prestatiesmetriek en statistieken tonen &#x200B;](assets/jo-dynamic_report_journey_12.png)

Leer meer over reisrapporten in deze [&#x200B; sectie &#x200B;](../reports/live-report.md).

## Aanvullende bronnen

* **[Overzicht van de ontwerper van de Reis](using-the-journey-designer.md)** - Meester de interface van het wegcanvas om klantenreizen te ontwerpen en te ordenen.
* **[de activiteiten van de Reis](about-journey-activities.md)** - ontdekt alle beschikbare activiteiten met inbegrip van gebeurtenissen, acties, en orchestration componenten.
* **[het Testen reizen](testing-the-journey.md)** - Leer hoe te om uw reizen te testen gebruikend testwijze alvorens aan productie te publiceren.
* **[het Publiceren reizen](publish-journey.md)** - begrijp het proces van de reispublicatie en hoe te om levende reizen te beheren.
* **[Reis die](report-journey.md)** meldt - spoor en analyseert reisprestaties met gedetailleerde metriek en inzichten.
* **[reizen van het Oplossen van problemen](troubleshooting.md)** - vind oplossingen aan gemeenschappelijke reiskwesties en beste praktijken voor het zuiveren.
* **[leerprogramma&#39;s van de Reis &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** - Onderzoek geleidelijke videoleerprogramma&#39;s op het wegbouw en beste praktijken.

>[!NOTE]
>
>Als u a **levende** reis moet wijzigen, [&#x200B; creeer een nieuwe versie &#x200B;](journey-ui.md#journey-filter) van uw reis.
