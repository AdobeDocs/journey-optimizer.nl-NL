---
title: Beslissingen nemen
description: Leer hoe u beslissingen maakt
feature: Aanbiedingen
topic: Integraties
role: User
level: Intermediate
source-git-commit: d09eedce833b41037452bb46bc748e7e9f477d0a
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 4%

---

# Beslissingen nemen {#create-offer-activities}

Besluiten (voorheen bekend als aanbiedingsactiviteiten) zijn containers voor uw aanbiedingen die gebruikmaken van de Offertenbeslissingsengine om de beste aanbieding te kiezen, afhankelijk van het doel van de levering.

➡️ [Ontdek deze functie in video](#video)

De lijst met beslissingen is toegankelijk op het tabblad **[!UICONTROL Offers]** / **[!UICONTROL Decisions]**. De filters zijn beschikbaar om u te helpen besluiten op hun status of begin en einddata terugwinnen.

![](../../assets/activities-list.png)

Voordat u een beslissing maakt, moet u controleren of de onderstaande componenten zijn gemaakt in de bibliotheek met aanbiedingen:

* [Plaatsingen](../offer-library/creating-placements.md)
* [Verzamelingen](../offer-library/creating-collections.md)
* [Persoonlijke aanbiedingen](../offer-library/creating-personalized-offers.md)
* [Alternatieve aanbiedingen](../offer-library/creating-fallback-offers.md)

## De beslissing maken {#create-activity}

1. Heb toegang tot de besluitenlijst, dan klik **[!UICONTROL Create activity]**.

1. Geef de naam van het besluit en de begin- en einddatum en -tijd op en klik vervolgens op **[!UICONTROL Next]**.

   ![](../../assets/activities-name.png)

## Beslissingsbereik toevoegen {#add-decision-scopes}

1. Sleep een positie uit de lijst om deze aan de beslissing toe te voegen en klik vervolgens op **[!UICONTROL Add collection]**.

   ![](../../assets/activities-placement.png)

   >[!NOTE]
   >
   >Dezelfde plaatsing kan meerdere keren in de beslissing worden geselecteerd.

1. Selecteer de inzameling die de aanbiedingen bevat om te overwegen, dan klik **[!UICONTROL Add]**.

   ![](../../assets/activities-collection.png)

1. De geselecteerde voorstellen worden toegevoegd aan de plaatsing. In dit voorbeeld, selecteerden wij twee aanbiedingen die in een JSON-type plaatsing zullen tonen gericht op het voorstellen van aanbiedingen in een oplossing van het vraagcentrum.

   ![](../../assets/offers-added.png)

1. Als meerdere aanbiedingen voor deze plaatsing in aanmerking komen, worden standaard de aanbiedingen met de hoogste prioriteitsscore aan de klant geleverd.

   Als u een specifieke formule wilt gebruiken om te kiezen welke in aanmerking komende aanbieding moet worden geleverd, selecteert u een rangschikkende formule in de vervolgkeuzelijst **[!UICONTROL Rank offers by]**. Raadpleeg [deze sectie](../offer-activities/configure-offer-selection.md) voor meer informatie.

1. In het veld **[!UICONTROL Constraint]** is de selectie van aanbiedingen voor deze plaatsing beperkt. Deze beperking kan worden toegepast door een beslissingsregel of een of meerdere Adobe Experience Platform-segmenten te gebruiken.

   Als u de selectie van de aanbiedingen wilt beperken tot de leden van een Adobe Experience Platform-segment, selecteert u **[!UICONTROL Segments]** en klikt u op **[!UICONTROL Add segments]**.

   ![](../../assets/activity_constraint_segment.png)

   Voeg een of meerdere segmenten uit het linkervenster toe, combineer deze met de logische operatoren **[!UICONTROL And]** / **[!UICONTROL Or]** en klik vervolgens op **[!UICONTROL Select]** om te bevestigen.

   Raadpleeg de [documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html) voor meer informatie over het werken met segmenten.

   ![](../../assets/activity_constraint_segment2.png)

   Als u een selectiegrens voor deze plaatsing gebruikend een besluitregel wilt toevoegen, selecteer **[!UICONTROL Decision rule]** optie, dan sleep de gewenste regel van de linkerruit in **[!UICONTROL Decision rule]** gebied. Voor meer op hoe te om een besluitregel tot stand te brengen, verwijs naar [deze sectie](../offer-library/creating-decision-rules.md).

   ![](../../assets/activity_constraint_rule.png)

## Een fallback-aanbieding toevoegen {#add-fallback}

Selecteer de fallback-aanbieding die als laatste redmiddel zal worden weergegeven aan klanten die niet voldoen aan de regels en beperkingen voor het in aanmerking nemen van aanbiedingen en klik vervolgens op **[!UICONTROL Next]**.

![](../../assets/add-fallback-offer.png)

## Beslissing bekijken en opslaan {#review}

Als alles correct wordt gevormd en uw besluit klaar is om te worden gebruikt om aanbiedingen aan klanten voor te stellen, klik **[!UICONTROL Finish]**, dan uitgezocht **[!UICONTROL Save and activate]**.

U kunt de beslissing ook opslaan als concept, zodat u deze later kunt bewerken en activeren.

![](../../assets/save-activities.png)

De beslissing wordt in de lijst weergegeven met de status **[!UICONTROL Live]** of **[!UICONTROL Draft]**, afhankelijk van of u de beslissing hebt geactiveerd in de vorige stap.

Het is nu klaar om te worden gebruikt om aanbiedingen aan klanten te leveren. U kunt het selecteren om zijn eigenschappen te tonen en het uit te geven of te onderdrukken.

Raadpleeg de volgende secties voor meer informatie over aanbiedingen:

* [Aangepaste aanbiedingen in berichten toevoegen](../../deliver-personalized-offers.md)
* [Aanbiedingen leveren met behulp van API&#39;s](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>Zodra een besluit is gecreeerd, kunt u zijn naam in de lijst klikken om tot gedetailleerde informatie toegang te hebben, en alle veranderingen visualiseren die aan het gebruikend **[!UICONTROL Change log]** tabel (zie [Veranderingen logboek van Aanbiedingen en van Besluiten ](../get-started/user-interface.md#changes-log)) zijn aangebracht.

## Video over zelfstudie {#video}

>[!NOTE]
>
>Deze video is van toepassing op de Offer decisioning toepassingsservice die op Adobe Experience Platform is gebouwd. Het biedt echter algemene richtlijnen voor het gebruik van Aanbieding in de context van Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
