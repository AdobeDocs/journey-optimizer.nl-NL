---
solution: Journey Optimizer
product: journey optimizer
title: Fragmenten beheren
description: Leer hoe u uw inhoudsfragmenten beheert
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Fragmenten beheren {#manage-fragments}

Als u uw fragmenten wilt beheren, opent u de fragmentlijst via **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** links menu.

Alle fragmenten die op de huidige zandbak - of [ van het **[!UICONTROL Fragments]** menu ](#create-fragments) werden gecreeerd, of gebruikend [ sparen als fragmentoptie ](#save-as-fragment) - worden getoond.

![](assets/fragment-list-filters.png)

U kunt fragmenten filteren op hun:

* Status (concept of live)
* Type (visueel of expression)
* Aanmaakdatum of wijzigingsdatum
* Staat (al dan niet gearchiveerd)
* Tags

U kunt er ook voor kiezen om alle fragmenten weer te geven, of alleen de items die de huidige gebruiker heeft gemaakt of gewijzigd.

Via de knop **[!UICONTROL More actions]** naast elk fragment kunt u:

* Dupliceer een fragment.
* Gebruik de optie **[!UICONTROL Explore references]** om de reizen, campagnes of sjablonen te zien waar deze worden gebruikt. [Meer informatie](#explore-references)
* Archiveer een fragment. [Meer informatie](#archive-fragments)
* Bewerk de markeringen van een fragment [ leren hoe te met Verenigde markeringen ](../start/search-filter-categorize.md#tags) te werken.

![](assets/fragment-list-more-actions.png)

## Fragmentstatussen

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nieuwe fragmentstatussen"
>abstract="Aangezien **Ontwerp** en **Levende** statussen met de versie van Journey Optimizer Juni zijn geïntroduceerd, hebben alle fragmenten die vóór deze versie worden gecreeerd de status &quot;van het Ontwerp&quot;, zelfs als zij in een reis of een campagne worden gebruikt. Als u wijzigingen aanbrengt in deze fragmenten, moet u deze publiceren om ze &quot;live&quot; te maken en de wijzigingen aan de bijbehorende campagnes en reizen door te geven. U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren. <br/> het Publiceren vereist de <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage"> 2} gebruikerstoestemming van het Fragment van Publish {.</a>"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Meer informatie over machtigingen voor inhoudsfragmenten"

Fragmenten kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: het fragment wordt bewerkt en is niet goedgekeurd.

* **[!UICONTROL Live]**: het fragment is goedgekeurd en is actief. [ leer hoe te om een fragment ](../content-management/create-fragments.md#publish) te publiceren

  Wanneer een actief fragment wordt bewerkt, wordt een specifiek pictogram naast de status weergegeven. Klik op dit pictogram om de conceptversie van het fragment te openen.

* **[!UICONTROL Publishing]**: Het fragment is goedgekeurd en wordt gepubliceerd.
* **[!UICONTROL Archived]**: het fragment is gearchiveerd. [ Leer hoe te om fragmenten ](#archive-fragments) te archiveren

>[!CAUTION]
>
>Aangezien **Ontwerp** en **Levende** statussen met de versie van Journey Optimizer Juni zijn geïntroduceerd, hebben alle fragmenten die vóór deze versie worden gecreeerd de status &quot;van het Ontwerp&quot;, zelfs als zij in een reis of een campagne worden gebruikt. Als u wijzigingen aanbrengt in deze fragmenten, moet u deze publiceren om ze &quot;live&quot; te maken en de wijzigingen aan de bijbehorende campagnes en reizen door te geven. U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren. Het publiceren vereist de ](../administration/ootb-product-profiles.md#content-library-manager) gebruikerstoestemming van het Fragment van 0} Publish.[

## Fragmenten bewerken {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Fragmenten bijwerken in campagnes"
>abstract="Deze campagne wordt niet bijgewerkt als u wijzigingen in het fragment publiceert. Er moet een nieuwe versie worden gepubliceerd zodat de functionaliteit voor fragmentupdate kan worden ondersteund."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Fragmenten worden bijgewerkt tijdens reizen"
>abstract="Deze reis zal niet worden bijgewerkt als u veranderingen in het fragment publiceert. Er moet een nieuwe versie worden gepubliceerd zodat de functionaliteit voor fragmentupdate kan worden ondersteund."

Voer de onderstaande stappen uit om een fragment te bewerken.

1. Klik op het gewenste fragment in de lijst **[!UICONTROL Fragments]** .

1. De fragmenteigenschappen worden geopend met een voorvertoning van de inhoud ervan.

1. Als het fragment dat wordt uitgegeven de **Levende** status heeft, klik **wijzigt** knoop om een ontwerp versie van het fragment tot stand te brengen. De huidige versie van het fragment blijft actief totdat u de conceptversie publiceert.

1. Breng de gewenste wijzigingen aan in het fragment. Om zijn inhoud uit te geven, klik **uitgeven** knoop dan uw inhoud zoals u wanneer het creëren van een fragment van kras zou doen. [ Leer hoe te om een fragment ](#create-from-scratch) tot stand te brengen

   >[!NOTE]
   >
   >Wanneer u een expressiefragment bewerkt, kunt u elk willekeurig aanpassingsveld verwijderen, maar u kunt geen nieuwe velden toevoegen aan de fragmentinhoud. Als u aanpassingsvelden wilt toevoegen, dupliceert u het fragment om een nieuw fragment te maken.

   U kunt de lijst van de reizen, campagnes en inhoudsmalplaatjes ook controleren waar het fragment momenteel door de **verwijzingen van de Ontdekkingsreiziger** optie te selecteren wordt gebruikt. [Meer informatie](#explore-references)

   ![](assets/fragment-edit.png)

1. Zodra uw veranderingen klaar zijn, klik de **knoop van Publish** om uw veranderingen levend te maken.

Wanneer u een fragment bewerkt, worden de wijzigingen automatisch doorgegeven aan alle inhoud met dat fragment, inclusief live reizen en campagnes, behalve voor inhoud waarin u de overerving van het oorspronkelijke fragment hebt verbroken. Leer hoe te om overerving in [ te breken voeg visuele fragmenten aan uw e-mails ](../email/use-visual-fragments.md#break-inheritance) en [ de uitdrukkingsfragmenten van de Leverage ](../personalization/use-expression-fragments.md#break-inheritance) secties toe.

## Verwijzingen verkennen {#explore-references}

U kunt een lijst weergeven met de reizen, campagnes en inhoudssjablonen die momenteel een fragment gebruiken. Selecteer hiervoor **[!UICONTROL Explore references]** in het menu **[!UICONTROL More actions]** in de fragmentlijst of in het scherm met fragmenteigenschappen.

![](assets/fragment-explore-references.png)

Selecteer een tabblad om te schakelen tussen reizen, campagnes, sjablonen en fragmenten. U kunt hun status zien en op een naam klikken die moet worden omgeleid naar het corresponderende item waar naar het fragment wordt verwezen.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Als het fragment wordt gebruikt in een reis, campagne of sjabloon met een label dat u ervan weerhoudt het te openen, wordt boven op het geselecteerde tabblad een waarschuwingsbericht weergegeven. [ leer meer op het Toegangsbeheer van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md)

## Fragmenten archiveren {#archive-fragments}

U kunt de fragmentlijst opruimen van de items die niet meer van belang zijn voor uw merk.

Klik hiertoe op de knop **[!UICONTROL More actions]** naast het gewenste fragment en selecteer **[!UICONTROL Archive]** . Deze verdwijnt uit de fragmentlijst, zodat gebruikers deze niet meer kunnen gebruiken in toekomstige e-mails of sjablonen.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Als u een fragment archiveert dat in een inhoud wordt gebruikt, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it--> dat de inhoud niet zal worden beïnvloed.

Als u het archiveren van een fragment ongedaan wilt maken, filtert u op de **[!UICONTROL Archived]** -items en selecteert u **[!UICONTROL Unarchive]** in het menu **[!UICONTROL More actions]** . Het is nu weer toegankelijk vanuit de fragmentlijst en kan in elke e-mail of sjabloon worden gebruikt.

![](assets/fragment-list-unarchive.png)

## Fragmenten exporteren naar een andere sandbox {#export}

Met Journey Optimizer kunt u een fragment van de ene naar de andere sandbox kopiëren. U kunt bijvoorbeeld een fragment uit de sandboxomgeving van het werkgebied kopiëren naar uw productiefandbox.

Het exemplaarproces wordt gedragen via de uitvoer en de invoer van het a **pakket** tussen de bron en doelzandbakken. De gedetailleerde informatie over hoe te om voorwerpen uit te voeren en hen in een doelzandbak in deze sectie in te voeren is beschikbaar: [ de voorwerpen van het Exemplaar aan een andere zandbak ](../configuration/copy-objects-to-sandbox.md)
