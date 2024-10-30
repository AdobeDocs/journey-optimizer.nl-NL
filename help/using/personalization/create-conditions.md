---
solution: Journey Optimizer
product: journey optimizer
title: Voorwaarden maken
description: Leer hoe u voorwaarden kunt maken
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressie, editor, voorwaardelijk, regels
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 6f9bdb179f2bfff30494495b68a15aaac77d6b9e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---

# Werken met voorwaardelijke regels {#conditions}

Voorwaardelijke regels zijn sets regels die bepalen welke inhoud in uw berichten moet worden weergegeven, afhankelijk van verschillende criteria zoals de kenmerken van profielen, het lidmaatschap van het publiek of contextuele gebeurtenissen.

Voorwaardelijke regels worden gecreeerd gebruikend de verpersoonlijkingsredacteur en kunnen worden opgeslagen als u hen over uw inhoud wilt opnieuw gebruiken. [ Leer hoe te om een voorwaardelijke regel aan de bibliotheek te bewaren ](#save)

>[!NOTE]
>
>De individuen zullen [ nodig hebben leiden de Punten van de Bibliotheek ](../administration/ootb-product-profiles.md) toestemming om voorwaardelijke regels te bewaren of te schrappen. Opgeslagen voorwaarden zijn beschikbaar voor gebruik door alle gebruikers binnen een organisatie.

## Toegang krijgen tot de constructor voor voorwaardelijke regels {#access}

Voorwaardelijke regels worden gemaakt in het menu **[!UICONTROL Conditions]** in de verpersoonlijkingseditor, die toegankelijk is:

* Vanuit de Designer-e-mail, wanneer dynamische inhoud wordt ingeschakeld voor een component in de hoofdtekst van de e-mail. [ Leer hoe te om dynamische inhoud in e-mails toe te voegen ](dynamic-content.md#emails)

  ![](assets/conditions-access-email.png)

* Op om het even welk gebied waar u verpersoonlijking kunt toevoegen gebruikend de [ verpersoonlijkingsredacteur ](personalization-build-expressions.md).

  ![](assets/conditions-access-editor.png)

## Een voorwaardelijke regel maken {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Voorwaarde maken"
>abstract="Combineer profielkenmerken, contextafhankelijke gebeurtenissen of soorten publiek om regels op te stellen die bepalen welke inhoud in uw berichten moet worden weergegeven."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Voorwaarde maken"
>abstract="Combineer profielkenmerken, contextafhankelijke gebeurtenissen of soorten publiek om regels op te stellen die bepalen welke inhoud in uw berichten moet worden weergegeven."

U kunt als volgt een voorwaardelijke regel maken:

1. Open het menu **[!UICONTROL Conditions]** vanuit de verpersoonlijkingseditor of de e-mailtoepassing Designer en klik vervolgens op **[!UICONTROL Create new]** .

1. Bouw de voorwaardelijke regel volgens uw behoeften. U doet dit door de gewenste kenmerken vanuit het linkermenu naar het canvas te slepen en neer te zetten.

   De stappen om kenmerken in het canvas te combineren zijn gelijkaardig aan de ervaring van het segmentbouwen. Voor meer informatie over hoe te met het canvas van de regelbouwer te werken, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#rule-builder-canvas).

   ![](assets/conditions-create.png)

   De kenmerken zijn ingedeeld in drie tabbladen:

   * **[!UICONTROL Profile]** :
      * **[!UICONTROL Audiences]** geeft alle publiekskenmerken weer (bijvoorbeeld status, versie enz.) voor [ de dienst van de Segmentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL XDM Individual profiles]** maakt een lijst van alle profielattributen verbonden aan het [ Model van de Gegevens van de Ervaring (XDM) schema ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) dat in Adobe Experience Platform wordt bepaald.
   * **[!UICONTROL Contextual]**: wanneer uw bericht tijdens een reis wordt gebruikt, zijn de contextuele reisgebieden beschikbaar door dit lusje.
   * **[!UICONTROL Audiences]**: maakt een lijst van alle publiek dat van segmentdefinities wordt geproduceerd die in [ de dienst van de Segmentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html) worden gecreeerd.

1. Zodra uw voorwaardelijke regel klaar is, kunt u deze aan uw bericht toevoegen om dynamische inhoud te maken. [ Leer hoe te om dynamische inhoud toe te voegen ](dynamic-content.md)

   U kunt de regel ook opslaan om verder hergebruik toe te staan. [ Leer hoe te om een voorwaarde ](#save) te bewaren

## Een voorwaardelijke regel opslaan {#save}

Als er voorwaardenregels zijn die u vaak opnieuw gebruikt, kunt u deze opslaan in de voorwaardenbibliotheek. Alle opgeslagen regels worden gedeeld en kunnen worden benaderd en gebruikt door personen binnen uw organisatie.

>[!NOTE]
>
>Voorwaardelijke regels die contextafhankelijke kenmerken voor reizen gebruiken, kunnen niet worden opgeslagen in de bibliotheek.

1. Klik op de knop **[!UICONTROL Save condition]** in het scherm van de voorwaardeneditie.

1. Geef de regel een naam en een beschrijving (optioneel) en klik op **[!UICONTROL Add]** .

   ![](assets/conditions-name-description.png)

1. De voorwaardelijke regel wordt opgeslagen in de bibliotheek. U kunt het nu gebruiken om dynamische inhoud in uw berichten tot stand te brengen. [ Leer hoe te om dynamische inhoud toe te voegen ](dynamic-content.md)

## Opgeslagen voorwaardelijke regels bewerken en verwijderen {#edit-delete}

U kunt op elk gewenst moment een voorwaardelijke regel verwijderen met de knop voor ovaal.

![](assets/conditions-open.png)

Voorwaardelijke regels die zijn opgeslagen in de bibliotheek kunnen niet worden gewijzigd. U kunt ze echter nog steeds gebruiken om nieuwe regels te maken. Hiervoor opent u de voorwaardelijke regel, brengt u de gewenste wijzigingen aan en slaat u deze op in de bibliotheek. [ Leer hoe te om een voorwaarde aan de bibliotheek ](#save) te bewaren
