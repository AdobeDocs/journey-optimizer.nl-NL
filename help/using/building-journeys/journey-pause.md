---
solution: Journey Optimizer
product: journey optimizer
title: Een reis pauzeren
description: Leer hoe u een reis pauzeert/hervat
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beperkte beschikbaarheid" type="Informative"
keywords: publiceren, reizen, live, geldigheid, controle
source-git-commit: 9ac387f073d8f0384e20cb2d8fe327efe4b8ecde
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Een reis pauzeren {#journey-pause}

U kunt uw live reizen pauzeren, alle benodigde wijzigingen uitvoeren en deze op elk gewenst moment hervatten. Een reis kan maximaal 14 dagen worden onderbroken. U kunt kiezen of de reis wordt hervat aan het einde van de pauze periode, of of het volledig stopt.


>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.


## Belangrijkste voordelen {#journey-dry-run-benefits}

Het pauzeren en hervatten van reizen geeft de marketers meer controle en flexibiliteit door het tijdelijk opschorten van de rechtstreekse reizen zonder de ervaring van de klant te verstoren. Wanneer gepauzeerd, worden geen mededelingen verzonden, en de profielen blijven in een geschorste staat tot de reis wordt hervat.

Dit vermogen vermindert het risico om onbedoelde berichten tijdens fouten of updates (bijvoorbeeld: verandering op berichtinhoud) te verzenden, steunt veiliger reisbeheer, en verhoogt praktiserend vertrouwen. De zichtbaarheid in gepauzeerde reizen en hun status rechtstreeks in de gebruikersinterface verbeteren de transparantie en de operationele flexibiliteit verder.

>[!CAUTION]
>
>Machtigingen om reizen te pauzeren en te hervatten zijn beperkt tot gebruikers met de machtiging op hoog niveau van **[!DNL Publish journeys]** . Leer meer over het beheren van [!DNL Journey Optimizer] de toegangsrechten van gebruikers in [ deze sectie ](../administration/permissions-overview.md).

## Guardrails en aanbevelingen

* Een reisversie kan maximaal 14 dagen worden onderbroken.
* Gepauzeerde reizen worden in alle bedrijfsregels beschouwd, net als wanneer ze in leven waren.
* Profielen worden tijdens een gepauzeerde reis &quot;verwijderd&quot; wanneer ze een actieactiviteit bereiken. Als ze op een wachttijd blijven tijdens het pauzeren van een reis en het verlaten van een reis die wacht op de hervatting, zullen ze de reis voortzetten en niet worden weggegooid.
* Zelfs na het pauzeren zouden deze gebeurtenissen, naarmate de gebeurtenissen verder worden verwerkt, worden geteld in het quotum van 5 ktps, waarna de vertraging voor de eenheid zichtbaar wordt.
* Profielen die tijdens de pauze op de reis zijn gekomen, worden nog steeds als aanspreekbare profielen geteld.
* Als profielen tijdens een gepauzeerde rit staan, worden de profielkenmerken tijdens het hervatten vernieuwd
* Voorwaarden worden nog steeds uitgevoerd tijdens gepauzeerde reizen, dus als een reis is gepauzeerd vanwege problemen met de gegevenskwaliteit, kan elke voorwaarde voorafgaand aan een actieknooppunt worden geëvalueerd met onjuiste gegevens.
* Voor de incrementele op het publiek gebaseerde leestreis wordt rekening gehouden met de gepauzeerde duur. Als de reis bijvoorbeeld op de tweede dag werd gepauzeerd en op de vijfde van de maand werd hervat, zal de 6de reis alle profielen nemen die van de eerste tot en met de zesde zijn gekwalificeerd. Dit is niet het geval voor publiekskwalificatie of op gebeurtenis-gebaseerde reizen (als een publiekskwalificatie of een gebeurtenis tijdens een pauze worden ontvangen, worden die gebeurtenissen verworpen).
* Gepauzeerde ritten worden meegeteld in de quota voor rechtstreekse reizen.
* De wereldwijde time-out van de reis geldt nog steeds voor gepauzeerde reizen. Als een profiel bijvoorbeeld 90 dagen op reis was en de reis wordt gepauzeerd, zal dit profiel de reis op de 91ste dag nog steeds verlaten.
* Een nieuwe **Hervatten** reisstatus is beschikbaar wanneer een reis wordt hervat. Het begint opnieuw aan reisgebeurtenissen te luisteren wanneer u **klikt hervat**.  Er is enige vertraging bij de hervatting van profielen in de reis. Wanneer de reis van **het Hervatten** aan **Levend** gaat, betekent het dat alle profielen zijn hervat. **het Hervatten** kan daarom wat tijd vergen.
* Als profielen op reis worden gehouden en deze reis automatisch na XX dagen wordt hervat, worden profielen doorgevoerd en niet weggelaten. Als u hen wilt laten vallen, moet u de reis manueel hervatten.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Hoe een reis pauzeren {#journey-pause-steps}

U kunt elke live reis pauzeren.

Voer de volgende stappen uit om uw reis te pauzeren:

1. Open de reis die u wilt pauzeren.
1. Klik op **...Meer** knoop op de hoger-juiste sectie van het wegcanvas, en selecteer **Pauzeren**.

   ![ Pauzeer de reisknoop ](assets/pause-journey-button.png)

1. Selecteer hoe u profielen wilt beheren die zich momenteel op de reis bevinden.

   ![ de reisopties van de Pauze ](assets/pause-confirm.png){width="50%" align="left"}

   U kunt:

   * Profielen vasthouden
   * Profielen negeren

1. Klik de **knoop van de Pauze** om te bevestigen.

Een reis kan maximaal 14 dagen worden onderbroken.

## Hoe te om een gepauzeerde reis te hervatten {#journey-resume-steps}

Gepauzeerde reizen kunnen op elk gewenst moment handmatig worden hervat.

Ga als volgt te werk om een rit te hervatten:

1. Open de reis die u wilt hervatten.
1. Klik op **...Meer** knoop op de hoger-juiste sectie van het wegcanvas, en selecteer **Hervatten**.




