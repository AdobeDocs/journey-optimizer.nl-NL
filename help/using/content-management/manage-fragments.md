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
source-git-commit: 4f238177485ccc5ab53b48488dd1f2084d34d684
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 1%

---

# Fragmenten beheren {#manage-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nieuwe fragmentstatussen"
>abstract="Sinds **Concept** en **Live** De status &#39;Concept&#39; is ingevoerd met de release van Journey Optimizer June. Alle fragmenten die vóór deze release zijn gemaakt, hebben de status &#39;Concept&#39;, zelfs als ze op reis of tijdens een campagne worden gebruikt. Als u wijzigingen aanbrengt in deze fragmenten, moet u deze publiceren om ze &quot;live&quot; te maken en de wijzigingen aan de bijbehorende campagnes en reizen door te geven. U moet ook een nieuwe reis/campagneversie tot stand brengen en het publiceren."

Als u uw fragmenten wilt beheren, opent u de fragmentlijst via de **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** links.

![](assets/fragment-list.png)

Alle fragmenten die op de huidige sandbox zijn gemaakt - ofwel [van de **[!UICONTROL Fragments]** menu](#create-fragments), waarbij de [Opslaan als fragment](#save-as-fragment) -optie - worden weergegeven.

U kunt fragmenten filteren op hun:

* Type: **[!UICONTROL Visual]** of **[!UICONTROL Expression]**
* Tags
* Aanmaakdatum of wijzigingsdatum

U kunt ervoor kiezen om alle fragmenten weer te geven, of alleen de items die de huidige gebruiker heeft gemaakt of gewijzigd.

U kunt ook de **[!UICONTROL Archived]** fragmenten. [Meer informatie](#archive-fragments)

![](assets/fragment-list-filters.png)

Van de **[!UICONTROL More actions]** naast elk fragment kunt u:

* Dupliceer een fragment.

* Gebruik de **[!UICONTROL Explore references]** de reis, de campagnes of de sjablonen waar deze worden gebruikt. [Meer informatie](#explore-references)

* Archiveer een fragment. [Meer informatie](#archive-fragments)

* Een fragment bewerken [tags](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Fragmenten bewerken {#edit-fragments}

Voer de onderstaande stappen uit om een fragment te bewerken.

1. Klik op het gewenste item in het pop-upmenu **[!UICONTROL Fragments]** lijst.
1. Vanuit de fragmenteigenschappen kunt u [verwijzingen verkennen](#explore-references), [zijn toegang beheren](../administration/object-based-access.md)en werkt de fragmentdetails bij, inclusief [tags](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. Selecteer de bijbehorende knop om de inhoud te bewerken zoals u zou doen bij het maken van een geheel nieuw fragment. [Meer informatie](#create-from-scratch)

>[!NOTE]
>
>Wanneer u een fragment bewerkt, worden de wijzigingen automatisch doorgegeven aan alle inhoud die dat fragment gebruikt, met uitzondering van inhoud die wordt gebruikt in **[!UICONTROL Live]** reizen of campagnes. U kunt de overerving van het oorspronkelijke fragment ook verbreken. Meer informatie in het dialoogvenster [Visuele fragmenten toevoegen aan uw e-mails](../email/use-visual-fragments.md#break-inheritance) en [Expressiefragmenten benutten](../personalization/use-expression-fragments.md#break-inheritance) secties.

## Verwijzingen verkennen {#explore-references}

U kunt een lijst weergeven met de reizen, campagnes en inhoudssjablonen die momenteel een fragment gebruiken.

Selecteer **[!UICONTROL Explore references]** hetzij van de **[!UICONTROL More actions]** in de fragmentlijst of vanuit het scherm met fragmenteigenschappen.

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
