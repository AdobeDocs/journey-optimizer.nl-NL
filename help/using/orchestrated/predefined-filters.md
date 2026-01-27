---
solution: Journey Optimizer
product: journey optimizer
title: Werken met vooraf gedefinieerde filters
description: Leer hoe u vooraf gedefinieerde filters opslaat, toepast en beheert in geordende campagnes
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 2%

---


# Werken met vooraf gedefinieerde filters {#predefined-filters}

Vooraf gedefinieerde filters zijn opgeslagen regels die u opnieuw kunt gebruiken in de regelbuilder. Gebruik hen om het herbouwen van gemeenschappelijke vragen te vermijden en het richten logica over georkestreerde campagnes te standaardiseren.

U kunt vooraf gedefinieerde filters markeren als favorieten, deze delen met andere gebruikers en parameters toevoegen zodat geselecteerde velden kunnen worden bewerkt wanneer het filter wordt toegepast.

## Een vooraf gedefinieerd filter maken {#create}

Sparen een douanefilter van de regelbouwer om het voor toekomstig gebruik beschikbaar te maken. Voer de volgende stappen uit:

1. Open de regelbouwer en bepaal uw het filtreren voorwaarden. [ Leer hoe te om een regel ](../orchestrated/build-query.md) te bouwen

1. Optioneel: als u bepaalde velden bewerkbaar wilt maken wanneer u het filter gebruikt, selecteert u het veld en schakelt u **[!UICONTROL Set as parameter]** in. Wanneer u het filter toepast, kunnen alleen deze velden worden bewerkt.

   ![](assets/predefined-filter-parameter-enable.png)

1. Klik op **[!UICONTROL Select or save filter]** en selecteer **[!UICONTROL Save as filter]** om het filter op te slaan.

   ![](assets/predefined-filter-save.png)

1. Voer een label en beschrijving voor het filter in en klik op **[!UICONTROL Save]** .

   * Als u het filter wilt opslaan als een favoriet, schakelt u de optie **[!UICONTROL Favorite filter]** in of uit. Lees meer in [deze sectie](#fav-filter).
   * Als u het filter toegankelijk wilt maken voor andere gebruikers, schakelt u de optie **[!UICONTROL Shared filter]** in. Lees meer in [deze sectie](#share-filter).

   ![](assets/predefined-filter-save-name.png)

Uw douanefilter is nu beschikbaar in de **Vooraf bepaalde lijst van Filters**.

## Een vooraf gedefinieerd filter in een regel gebruiken {#apply}

De vooraf bepaalde filters zijn beschikbaar wanneer het bepalen van vragen in de regelbouwer.

1. Klik in het deelvenster **[!UICONTROL Rule properties]** op **[!UICONTROL Select or save filter]** .

1. Kies **[!UICONTROL Select predefined filter]** en selecteer een filter. U kunt ook rechtstreeks een vooraf gedefinieerd filter in de lijst selecteren als het aan favorieten is toegevoegd.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >Als u een vooraf gedefinieerd filter selecteert, wordt de regel die in het canvas is ingebouwd, vervangen door het geselecteerde filter.

1. Het filter wordt op het canvas geopend. Bewerk de voorwaarde indien nodig verder.

   ![](assets/predefined-filter-added.png)

   Als het geselecteerde filter parameters bevat, kunnen alleen de velden die als parameters zijn gemarkeerd, worden bewerkt. Ze worden weergegeven in het venster naast het deelvenster **[!UICONTROL Rule properties]** .

   ![](assets/predefined-filter-parameter-apply.png)

   Om de vooraf bepaalde filter zelf uit te geven, klik de ![ weglatingsknoop ](assets/do-not-localize/rule-builder-icon-more.svg) en selecteer **[!UICONTROL Switch to rule edition]**. Alle wijzigingen zijn alleen van toepassing op de huidige regel die u bouwt. Het vooraf gedefinieerde filter wordt niet gewijzigd.

   ![](assets/predefined-filter-parameter-edit.png)

## Een filter opslaan als een favoriet {#fav-filter}

Wanneer u een vooraf gedefinieerd filter maakt, schakelt u de optie **[!UICONTROL Favorite filter]** in om dit vooraf gedefinieerde filter in uw favorieten weer te geven.

Wanneer een filter wordt opgeslagen als een favoriet, verschijnt het in de **[!UICONTROL Favorite filters]** sectie van de filterlijst, zoals hieronder getoond:

![ Favoriete filterssectie ](assets/predefined-filter-favorites.png)

## Een vooraf gedefinieerd filter delen {#share-filter}

Vooraf gedefinieerde filters die u maakt, zijn standaard persoonlijk en zijn alleen voor u zichtbaar. Schakel de optie **[!UICONTROL Shared filter]** in als u een filter toegankelijk wilt maken voor andere operatoren in uw organisatie.

![ Gedeelde filteroptie ](assets/predefined-filter-shared.png)

De gedeelde filters verschijnen in de vooraf bepaalde filterlijst voor alle gebruikers, die hen toestaan om deze filters in hun eigen regels te gebruiken.

## Vooraf gedefinieerde filters beheren {#manage-predefined-filter}

Ga als volgt te werk om vooraf gedefinieerde filters te bewerken of te verwijderen:

1. Open de vooraf gedefinieerde filterlijst met de knop **[!UICONTROL Select or save filter]** in de regel.

1. Selecteer de ![ weglatingsknoop ](assets/do-not-localize/rule-builder-icon-more.svg) naast een filter en kies de gewenste actie.

![](assets/predefined-filters-edit.png)
