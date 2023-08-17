---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud helemaal opnieuw ontwerpen in Journey Optimizer
description: Leer hoe u uw inhoud helemaal zelf ontwerpt
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: inhoud, editor, e-mail, starten
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Inhoud helemaal opnieuw ontwerpen {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurelementen definiëren de indeling van de e-mail. Sleep een **Structuur** op het canvas om uw e-mailinhoud te ontwerpen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurcomponenten definiëren de indeling van de bestemmingspagina. Sleep een **Structuur** op het canvas om de inhoud van de bestemmingspagina te ontwerpen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurcomponenten definiëren de indeling van het fragment. Sleep een **Structuur** op het canvas om de inhoud van het fragment te ontwerpen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurelementen definiëren de lay-out van de sjabloon. Sleep een **Structuur** op het canvas om de inhoud van de sjabloon te ontwerpen."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="E-mailkolommen definiëren"
>abstract="Met de E-mailontwerper kunt u de indeling van uw e-mail eenvoudig definiëren door de kolomstructuur te selecteren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Startpaginakolommen definiëren"
>abstract="Met Designer kunt u de lay-out van de bestemmingspagina eenvoudig definiëren door de kolomstructuur te selecteren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Fragmentkolommen definiëren"
>abstract="In Designer kunt u de indeling van een fragment eenvoudig definiëren door de kolomstructuur te selecteren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Sjabloonkolommen definiëren"
>abstract="Met Designer kunt u de indeling van uw sjabloon eenvoudig definiëren door de kolomstructuur te selecteren."


Met Adobe Journey Optimizer Designer kunt u eenvoudig de structuur van uw inhoud definiëren. Door structuurelementen toe te voegen en te bewegen met eenvoudige belemmering-en-dalingsacties, kunt u de vorm van uw inhoud binnen seconden ontwerpen.

Voer de onderstaande stappen uit om uw inhoud te gaan samenstellen:

1. Selecteer op de introductiepagina van Designer de **[!UICONTROL Design from scratch]** -optie.

   ![](assets/email_designer.png)

1. Beginnen met het ontwerpen van uw inhoud door slepen en neerzetten **[!UICONTROL Structures]** in het canvas om de lay-out van uw e-mail te definiëren.

   >[!NOTE]
   >
   >Kolommen stapelen is niet compatibel met alle e-mailprogramma&#39;s. Kolommen worden niet gestapeld als deze functie niet wordt ondersteund.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Zoveel toevoegen **[!UICONTROL Structures]** en bewerk de instellingen in het daarvoor bestemde venster aan de rechterkant.

   ![](assets/email_designer_structure_components.png)

   Selecteer de **[!UICONTROL n:n column]** om het aantal kolommen van uw keus (tussen 3 en 10) te bepalen. U kunt de breedte van elke kolom ook bepalen door de pijlen bij de bodem van elke kolom te bewegen.

   >[!NOTE]
   >
   >Elke kolomgrootte mag niet kleiner zijn dan 10% van de totale breedte van de structuurcomponent. U kunt geen kolom verwijderen die niet leeg is.

1. Breid uit **[!UICONTROL Contents]** en voegt zo veel elementen toe als u nodig hebt in een of meer structuurcomponenten. [Meer informatie over inhoudscomponenten](content-components.md)

1. Elke component kan verder worden aangepast met de **[!UICONTROL Settings]** of **[!UICONTROL Style]** in het rechtermenu. U kunt bijvoorbeeld de tekststijl, opvulling of marge van elke component wijzigen. [Meer informatie over uitlijning en opvulling](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Van de **[!UICONTROL Asset picker]** kunt u rechtstreeks de elementen selecteren die in het dialoogvenster **[!UICONTROL Assets library]**. [Meer informatie over middelenbeheer](assets-essentials.md)

   Dubbelklik op de map met uw elementen. Sleep en zet ze neer in een structuurcomponent.

   ![](assets/email_designer_asset_picker.png)

1. Voeg verpersoonlijkingsgebieden in om uw inhoud van profielattributen, publiekslidmaatschappen, Contextuele attributen, en meer aan te passen. [Meer informatie over content personalization](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Klikken **[!UICONTROL Enable condition content]** dynamische inhoud toevoegen en de inhoud aanpassen aan de doelprofielen op basis van voorwaardelijke regels. [Aan de slag met dynamische inhoud](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Klik op de knop **[!UICONTROL Links]** in het linkerdeelvenster om alle URL&#39;s weer te geven van de inhoud die wordt bijgehouden. U kunt de **[!UICONTROL Tracking Type]** of **[!UICONTROL Label]** en toevoegen **[!UICONTROL Tags]** indien nodig. [Meer informatie over koppelingen en bijhouden](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Indien nodig kunt u uw e-mail verder aanpassen door op **[!UICONTROL Switch to code editor]** in het geavanceerde menu. Op deze manier kunt u de broncode van de e-mail bewerken, bijvoorbeeld door tags voor bijhouden of aangepaste HTML toe te voegen. [Meer informatie over de code-editor](code-content.md)

   >[!CAUTION]
   >
   >U kunt niet terugkeren naar de visuele ontwerper voor deze e-mail na het schakelen naar de coderedacteur.

1. Als de inhoud gereed is, klikt u op de knop **[!UICONTROL Simulate content]** om de rendering te controleren. U kunt kiezen voor de weergave Computer of Mobiel. [Meer informatie over een voorbeeld van uw e-mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Wanneer uw inhoud klaar is, klikt u op **[!UICONTROL Save]**.

