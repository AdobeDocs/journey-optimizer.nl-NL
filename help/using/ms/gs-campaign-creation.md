---
solution: Journey Optimizer
product: journey optimizer
title: Belangrijkste beginselen van het opzetten van meerfasencampagnes
description: Belangrijke principes van multi-step campagnes met Adobe Journey Optimizer leren
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3ecb1691cc8a1c429d9bd9919b06ddc5a316eff7
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Belangrijkste beginselen {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Meerdere stappen"
>abstract="In dit scherm, kunt u tot de volledige lijst van multi-step campagnes toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe multi-step campagne creëren."

Met Adobe Journey Optimizer kunt u in meerdere stappen campagnes maken tot een visueel canvas om kanaalprocessen zoals segmentatie, uitvoering van campagnes en bestandsverwerking te ontwerpen.

## Wat zit er in een campagne met meerdere stappen? {#gs-ms-campaign-inside}

Het campagnecanvas met meerdere stappen is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Elke campagne met meerdere stappen bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een multi-step campagnediagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkerende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke campagne met meerdere stappen worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen gedurende de levenscyclus van de campagne in meerdere stappen worden gebruikt.

## Belangrijke stappen om een campagne met meerdere stappen te maken {#gs-ms-campaign-steps}

De belangrijkste stappen voor het maken van een campagne die uit meerdere stappen bestaat, zijn:

![](assets/workflow-creation-process.png){zoomable="yes"}

## Meerdere stappen benaderen

Blader in het menu **[!UICONTROL Campaigns]** naar het tabblad Meerdere stappen voor toegang tot de volledige lijst met campagnes die uit meerdere stappen bestaan.

Elke multi-step campagne in de lijst toont informatie over zijn huidige [ status ](#status), de laatste tijd het werd uitgevoerd of, en de volgende geplande uitvoeringsdatum en tijd gewijzigd.

U kunt de weergegeven kolommen aanpassen door op het pictogram **[!UICONTROL Configure column for a custom layout]** in de rechterbovenhoek van de lijst te klikken. Hierdoor kunt u aanvullende informatie aan de lijst toevoegen, zoals de laatste foutactie voor elke campagne met meerdere stappen of de toegepaste doeldimensie.

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld de campagnes met meerdere stappen filteren om alleen de campagnes weer te geven die tot een campagne behoren, of de campagnes die tijdens een bepaald datumbereik zijn verwerkt.

Als u een campagne met meerdere stappen wilt dupliceren of verwijderen, klikt u op de knop voor een ovaal en selecteert u **[!UICONTROL Duplicate]** of **[!UICONTROL Delete]** .

>[!NOTE]
>
>Wanneer een campagne in meerdere stappen wordt uitgevoerd, kunt u deze dupliceren, maar u kunt deze niet verwijderen.

## Statussen en levenscyclus {#status}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De campagne met meerdere stappen is gemaakt en opgeslagen.
* **[!UICONTROL In progress]**: De campagne met meerdere stappen wordt momenteel uitgevoerd.
* **[!UICONTROL Finished]**: De uitvoering van de campagne in meerdere stappen is voltooid.
* **[!UICONTROL Paused]**: De campagne met meerdere stappen is gepauzeerd.
* **[!UICONTROL Erroneous]**: Er is een fout opgetreden tijdens de campagne met meerdere stappen. Open de campagne met meerdere stappen en open de logboeken en taken om de fout te identificeren en op te lossen.


## Een query samenstellen

## Personalization-richtlijnen
