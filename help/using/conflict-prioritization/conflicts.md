---
title: Mogelijke conflicten tijdens reizen en campagnes identificeren
description: Leer hoe u mogelijke conflicten tijdens reizen en campagnes kunt identificeren.
role: User
level: Beginner
exl-id: efbb5ac4-4c07-4c62-9460-39eb4fed129a
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

---

# Mogelijke conflicten tijdens reizen en campagnes detecteren {#conflict}

Naarmate de markt het aantal campagnes en reizen in Journey Optimizer verhoogt, wordt het steeds moeilijker voor een marketeer om te weten of zij hun klanten met te veel marketinginteracties bombarderen. Daarom is het van essentieel belang dat er gemakkelijk kan worden vastgesteld wanneer er overlappende campagnes en reizen zijn, om ervoor te zorgen dat deze de juiste balans vinden tussen marketingcommunicatie en het risico van vermoeidheid van de klant.

De belangrijkste gebieden om voor potentiële overlapping te controleren zijn:

* **Chronologie** (begin en einddata): Zijn teveel reizen die gelijktijdig lopen?
* **Publiek**: Welk percentage van mijn reispubliek is ook deel van andere reizen?
* **Kanaal**: Zijn er andere mededelingen die voor zelfde timeframe worden gepland, en als zo, hoeveel?
* **het Bedekken van Reeks van de Regel**: Welke types van reizen ben ik bedekken en is er overlapping binnen die?
* **Configuratie van het Kanaal**: Zijn er andere reizen of campagnes gebruikend om het even welke kanaalconfiguratie die in de zelfde reis of de campagne wordt gebruikt die de reis of de campagne zou kunnen verhinderen aan het eind - gebruiker worden getoond?

➡️ [Ontdek deze functie in video](#video)

## Hoe Journey Optimizer conflicten detecteert {#detection}

Hieronder volgt een overzicht van de manier waarop Journey Optimizer mogelijke conflicten voor reizen en campagnes identificeert:

* **werkingsgebied van de Identificatie van het Conflict**: De conflicten worden getoond slechts voor levende of geplande campagnes en reizen.
* **Eenheidstreizen**: Als de geselecteerde reis unitair is, worden andere reizen die met de zelfde gebeurtenis beginnen getoond, aangezien deze gebeurtenis al dergelijke reizen teweegbrengt.
* **de kwalificatie van het publiek en gelezen Publiek/BedrijfsGebeurtenis** reizen: Als de geselecteerde reis of een kwalificatie van het Publiek of een Gelezen reis van de Gebeurtenis van het Publiek/van de Onderneming is, worden alle andere reizen van het zelfde type met een geldig publiek getoond, aangezien er overlappingen tussen het publiek kunnen zijn.
* **Campagnes**: Aangezien alle campagnes doelpubliek richten en er geen concept gebeurtenissen is, veroorzaken alle campagnes potentieel conflict met segment-teweeggebrachte reizen (die met een Gelezen publieksactiviteit beginnen).
* **Levende/Geplande campagnes**: Levende en geplande campagnes kunnen met elkaar in conflict brengen toe te schrijven aan potentiële publieksoverlap. Voor elke campagne worden alle live- of geplande campagnes vermeld in de conflictviewer.

## Geselecteerde conflicten voor een bepaalde reis of campagne weergeven {#view}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Mogelijke conflicten weergeven"
>abstract="Controleer of er een mogelijkheid is voor overlapping met andere campagnes. Conflicten worden alleen weergegeven voor live- en geplande campagnes. De knop wordt beschikbaar zodra u een van de volgende instellingen hebt toegewezen: **[!UICONTROL Start / end date]**, **[!UICONTROL Audience]**, **[!UICONTROL Channel]**, **[!UICONTROL Channel configuration]** en **[!UICONTROL Rule set]** ."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Mogelijke conflicten weergeven"
>abstract="Controleer wanneer er een mogelijkheid is van overlapping met andere reizen. Conflicten worden alleen getoond voor rechtstreekse en geplande reizen. De knop wordt beschikbaar zodra u een van de volgende instellingen hebt toegewezen: **[!UICONTROL Start / end date]**, **[!UICONTROL Audience]**, **[!UICONTROL Channel]**, **[!UICONTROL Channel configuration]** en **[!UICONTROL Rule set]** ."

Wanneer u een reis of campagne maakt, kunt u met Journey Optimizer controleren of er een mogelijkheid is om overlappingen te maken met andere reizen of campagnes. Ga als volgt te werk om dit te doen:

1. Klik op de knop **[!UICONTROL View Potential Conflicts]** op het moment dat u een reis of campagne maakt.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >De knop **[!UICONTROL View potential conflicts]** wordt beschikbaar om te selecteren zodra u een van de volgende instellingen hebt toegewezen: **[!UICONTROL Start / end date]**, **[!UICONTROL Audience]**, **[!UICONTROL Channel]**, **[!UICONTROL Channel configuration]** en **[!UICONTROL Rule set]** . Zorg ervoor dat u **[!UICONTROL Save]** selecteert nadat u deze instellingen hebt toegewezen, aangezien de knop pas kan worden geselecteerd nadat de wijzigingen zijn opgeslagen.

1. Het venster **[!UICONTROL Potential conflicts]** wordt geopend, zodat u alle elementen kunt visualiseren die de huidige reis/campagne overlappen.

   U kunt een overlappende reis of campagne rechtstreeks vanuit dit scherm openen door de naam ervan te selecteren.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Nieuwe gepubliceerde reizen en campagnes kunnen tot 3-7 minuten duren om in de conflictviewer te verschijnen, als gevolg van het in cache plaatsen.

Als u uw zoekopdracht naar mogelijke overlappingen verder wilt verfijnen, kunt u uw lijst met campagnes en reizen filteren op basis van de velden die u relevant vindt. Selecteer hiertoe het filterpictogram in de overzichtsweergave. [ leer hoe te met filters ](../start/search-filter-categorize.md#filter-lists) werken

## Conflicten oplossen {#resolve}

Hier volgen enkele tips voor het verminderen van mogelijke conflicten nadat deze zijn geïdentificeerd:

* Pas de **begin/einddata** aan om overlappende campagnes of reizen te vermijden.
* Verfijn **publiek richtend** om overlapping tussen reizen te minimaliseren.
* Voer **frequentiecappen** uit om klanten te verhinderen te veel mededelingen te ontvangen.
* Verminder het aantal **actieve reizen** om klantenervaring effectiever te beheren.
* Plaats **prioriteiten** op binnenkomende acties om de belangrijkste actie te verzekeren wordt getoond aan klanten.

Door deze mogelijkheden leveraging, kunt u ervoor zorgen dat uw marketing inspanningen worden gericht en dat u het juiste evenwicht in uw communicatie strategie handhaaft.

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435528?quality=12)
