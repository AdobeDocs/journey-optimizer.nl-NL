---
solution: Journey Optimizer
product: journey optimizer
title: Belangrijkste beginselen van het opzetten van georkestreerde campagnes
description: Belangrijke principes van georkestreerde campagnes met Adobe Journey Optimizer leren
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 03af80bbaa347237059abe74f26274df5ab39caa
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Belangrijkste beginselen {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Geordende campagne"
>abstract="In dit scherm, kunt u tot de volledige lijst van georkestreerde campagnes toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe georkestreerde campagne creëren."

U kunt georkestreerde campagnes in een visueel canvas bouwen om kanaalprocessen zoals segmentatie, campagneuitvoering, dossierverwerking te ontwerpen.

## Toegang tot georkestreerde campagnes

Blader in het menu **[!UICONTROL Campaigns]** naar het tabblad In meerdere stappen om de volledige lijst met georkestreerde campagnes te openen.

Elk georkestreerde campagne in de lijst toont informatie over zijn huidige [ status ](#status), de laatste tijd het werd uitgevoerd of, en de volgende geplande uitvoeringsdatum en tijd gewijzigd.

U kunt de weergegeven kolommen aanpassen door op het pictogram **[!UICONTROL Configure column for a custom layout]** in de rechterbovenhoek van de lijst te klikken. Hierdoor kunt u aanvullende informatie aan de lijst toevoegen, zoals de laatste foutactie voor elke georkestreerde campagne of de toegepaste doeldimensie.

Bovendien zijn er een zoekbalk en filters beschikbaar waarmee u gemakkelijk in de lijst kunt zoeken. U kunt bijvoorbeeld de georkestreerde campagnes filteren om alleen de campagnes weer te geven die tot een campagne behoren, of de campagnes die tijdens een bepaald datumbereik zijn verwerkt.

Als u een georkestreerde campagne wilt dupliceren of verwijderen, klikt u op de knop Ovaal en selecteert u **[!UICONTROL Duplicate]** of **[!UICONTROL Delete]** .

>[!NOTE]
>
>Wanneer een georkestreerde campagne in uitvoering is, kunt u deze dupliceren, maar u kunt deze niet verwijderen.


## Wat zit er in een georkestreerde campagne? {#gs-ms-campaign-inside}

De georkestreerde campagnedoek is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Elke georkestreerde campagne bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een geordend campagnediagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkerende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke georkestreerde campagne worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen gedurende de gehele levenscyclus van de georkestreerde campagne worden gebruikt.


## Statussen en levenscyclus {#status}

Campagnes kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: De georkestreerde campagne is gemaakt en opgeslagen.
* **[!UICONTROL In progress]**: De georkestreerde campagne wordt momenteel uitgevoerd.
* **[!UICONTROL Finished]**: De uitvoering van de georkestreerde campagne is voltooid.
* **[!UICONTROL Paused]**: De georkestreerde campagne is gepauzeerd.
* **[!UICONTROL Erroneous]**: Er is een fout opgetreden tijdens de georkestreerde campagne. Open de georkestreerde campagne en open de logboeken en de taken om de fout te identificeren en het op te lossen.
