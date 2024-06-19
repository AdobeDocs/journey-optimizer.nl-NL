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
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# Fragmenten beheren {#manage-fragments}

Als u uw fragmenten wilt beheren, opent u de fragmentlijst via de **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** links.

Alle fragmenten die op de huidige sandbox zijn gemaakt - ofwel [van de **[!UICONTROL Fragments]** menu](#create-fragments), waarbij de [Opslaan als fragment](#save-as-fragment) -optie - worden weergegeven.

![](assets/fragment-list-filters.png)

U kunt fragmenten filteren op hun:

* Status (concept of live)
* Type (visueel of expression)
* Aanmaakdatum of wijzigingsdatum
* Staat (al dan niet gearchiveerd)
* Tags

U kunt er ook voor kiezen om alle fragmenten weer te geven, of alleen de items die de huidige gebruiker heeft gemaakt of gewijzigd.

Van de **[!UICONTROL More actions]** naast elk fragment kunt u:

* Dupliceer een fragment.
* Gebruik de **[!UICONTROL Explore references]** de reis, de campagnes of de sjablonen waar deze worden gebruikt. [Meer informatie](#explore-references)
* Archiveer een fragment. [Meer informatie](#archive-fragments)
* De tags van een fragment bewerken [Leer hoe te met Verenigde markeringen werken](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Fragmentstatussen

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nieuwe fragmentstatussen"
>abstract="Sinds **Concept** en **Live** De status &#39;Concept&#39; is ingevoerd met de release van Journey Optimizer June. Alle fragmenten die vóór deze release zijn gemaakt, hebben de status &#39;Concept&#39;, zelfs als ze op reis of tijdens een campagne worden gebruikt. Als u wijzigingen aanbrengt in deze fragmenten, moet u deze publiceren om ze &quot;live&quot; te maken en de wijzigingen aan de bijbehorende campagnes en reizen door te geven. U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren. Voor publiceren is een gebruikersmachtiging vereist."

>[!AVAILABILITY]
>
> Let op: de fragmentatiestatus wordt geleidelijk ingevoerd gedurende enkele dagen na de release van Journey Optimizer in juni. Terwijl sommige gebruikers directe toegang zullen hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu&#39;s beschikbaar wordt. Als deze verbetering nog niet beschikbaar is in uw omgeving, hoeft het fragment niet **Live** voor uw reizen en campagnes.

Fragmenten kunnen meerdere statussen hebben:

* **[!UICONTROL Draft]**: Het fragment wordt bewerkt en is niet goedgekeurd.

* **[!UICONTROL Live]**: Het fragment is goedgekeurd en is actief. [Leer hoe u een fragment publiceert](../content-management/create-fragments.md#publish)

  Wanneer een actief fragment wordt bewerkt, wordt een specifiek pictogram naast de status weergegeven. Klik op dit pictogram om de conceptversie van het fragment te openen.

* **[!UICONTROL Publishing]**: Het fragment is goedgekeurd en wordt gepubliceerd.
* **[!UICONTROL Archived]**: Het fragment is gearchiveerd. [Leer hoe u fragmenten kunt archiveren](#archive-fragments)

>[!CAUTION]
>
>Sinds **Concept** en **Live** De status &#39;Concept&#39; is ingevoerd met de release van Journey Optimizer June. Alle fragmenten die vóór deze release zijn gemaakt, hebben de status &#39;Concept&#39;, zelfs als ze op reis of tijdens een campagne worden gebruikt. Als u wijzigingen aanbrengt in deze fragmenten, moet u deze publiceren om ze &quot;live&quot; te maken en de wijzigingen aan de bijbehorende campagnes en reizen door te geven. U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren. Voor publiceren is een gebruikersmachtiging vereist.

## Fragmenten bewerken {#edit-fragments}

Voer de onderstaande stappen uit om een fragment te bewerken.

1. Klik op het gewenste fragment in het menu **[!UICONTROL Fragments]** lijst.

1. De fragmenteigenschappen worden geopend met een voorvertoning van de inhoud ervan.

1. Als het fragment dat wordt bewerkt het **Live** status, klik op de knop **Wijzigen** om een conceptversie van het fragment te maken. De huidige versie van het fragment blijft actief totdat u de conceptversie publiceert.

1. Breng de gewenste wijzigingen aan in het fragment. Als u de inhoud wilt bewerken, klikt u op de knop **Bewerken** bewerk vervolgens de inhoud zoals u zou doen bij het maken van een geheel nieuw fragment. [Leer hoe u een fragment maakt](#create-from-scratch)

   >[!NOTE]
   >
   >Wanneer u een expressiefragment bewerkt, kunt u elk willekeurig aanpassingsveld verwijderen, maar u kunt geen nieuwe velden toevoegen aan de fragmentinhoud. Als u aanpassingsvelden wilt toevoegen, dupliceert u het fragment om een nieuw fragment te maken.

   U kunt ook de lijst controleren van de reizen, campagnes en inhoudssjablonen waar het fragment momenteel wordt gebruikt door de optie **Verwijzingen naar Verkenner** -optie. [Meer informatie](#explore-references)

   ![](assets/fragment-edit.png)

1. Als uw wijzigingen gereed zijn, klikt u op de knop **Publiceren** om uw wijzigingen live te zetten.

Wanneer u een fragment bewerkt, worden de wijzigingen automatisch doorgegeven aan alle inhoud met dat fragment, inclusief live reizen en campagnes, behalve voor inhoud waarin u de overerving van het oorspronkelijke fragment hebt verbroken. Leer hoe u overerving kunt onderbreken in de [Visuele fragmenten toevoegen aan uw e-mails](../email/use-visual-fragments.md#break-inheritance) en [Expressiefragmenten benutten](../personalization/use-expression-fragments.md#break-inheritance) secties.

>[!AVAILABILITY]
>
>De verspreiding van fragmenten verandert geleidelijk in de loop van enkele dagen na de vrijlating van Journey Optimizer in juni. Terwijl sommige gebruikers directe toegang zullen hebben, kunnen anderen een vertraging ervaren alvorens het in hun milieu&#39;s beschikbaar wordt. Als deze verbetering nog niet in uw milieu beschikbaar is, zullen uw veranderingen niet aan inhoud worden verspreid die in levende reizen of campagnes wordt gebruikt.

## Verwijzingen verkennen {#explore-references}

U kunt een lijst weergeven met de reizen, campagnes en inhoudssjablonen die momenteel een fragment gebruiken. Selecteer **[!UICONTROL Explore references]** hetzij van de **[!UICONTROL More actions]** in de fragmentlijst of vanuit het scherm met fragmenteigenschappen.

![](assets/fragment-explore-references.png)

Selecteer een tabblad om te schakelen tussen reizen, campagnes, sjablonen en fragmenten. U kunt hun status zien en op een naam klikken die moet worden omgeleid naar het corresponderende item waar naar het fragment wordt verwezen.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Als het fragment wordt gebruikt in een reis, campagne of sjabloon met een label dat u ervan weerhoudt het te openen, wordt boven op het geselecteerde tabblad een waarschuwingsbericht weergegeven. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md)

## Fragmenten archiveren {#archive-fragments}

U kunt de fragmentlijst opruimen van de items die niet meer van belang zijn voor uw merk.

Klik hiertoe op de knop **[!UICONTROL More actions]** naast het gewenste fragment en selecteer **[!UICONTROL Archive]**. Deze verdwijnt uit de fragmentlijst, zodat gebruikers deze niet meer kunnen gebruiken in toekomstige e-mails of sjablonen.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Als u een fragment archiveert dat in een inhoud wordt gebruikt, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->de inhoud wordt niet beïnvloed.

Als u een fragment ongedaan wilt maken, filtert u op het tabblad **[!UICONTROL Archived]** items en selecteer **[!UICONTROL Unarchive]** van de **[!UICONTROL More actions]** -menu. Het is nu weer toegankelijk vanuit de fragmentlijst en kan in elke e-mail of sjabloon worden gebruikt.

![](assets/fragment-list-unarchive.png)
