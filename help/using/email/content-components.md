---
solution: Journey Optimizer
product: journey optimizer
title: Onderdelen voor content van e-mailontwerpers gebruiken
description: Leer hoe u inhoudcomponenten in uw e-mails kunt gebruiken
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: componenten, e-mailontwerper, editor, e-mail
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# De inhoudcomponenten van E-mailDesigner gebruiken {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Informatie over inhoudscomponenten"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een e-mail te maken."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Informatie over inhoudscomponenten"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een bestemmingspagina te maken."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Informatie over inhoudscomponenten"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een fragment te maken."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Informatie over inhoudscomponenten"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een sjabloon te maken."

Wanneer u uw e-mailinhoud maakt, **[!UICONTROL Content components]** kunt u uw e-mail verder aanpassen met onbewerkte onderdelen die u kunt bewerken nadat u deze in een e-mail hebt geplaatst.

U kunt zoveel inhoudscomponenten toevoegen als u nodig hebt binnen een of meer structuurcomponenten, die de indeling van uw e-mail definiëren.

## Inhoudscomponenten toevoegen {#add-content-components}

Voer de onderstaande stappen uit om inhoudcomponenten aan uw e-mail toe te voegen en deze aan uw wensen aan te passen.

1. Gebruik in de e-mailontwerper een bestaande inhoud of sleep en zet **[!UICONTROL Structure components]** in uw lege inhoud om de lay-out van uw e-mail te bepalen. [Meer informatie](content-from-scratch.md)

1. Om toegang te krijgen tot **[!UICONTROL Content components]** selecteert u de bijbehorende knop in het linkerdeelvenster van E-mailontwerper.

   ![](assets/email_designer_content_components.png)

1. Sleep de inhoudcomponenten van uw keuze naar keuze binnen de relevante structuurcomponenten.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >U kunt meerdere componenten toevoegen aan één structuurcomponent en aan elke kolom van een structuurcomponent.

1. Pas de opmaakkenmerken voor elke component aan met de opdracht **[!UICONTROL Component settings]** aan de rechterkant. U kunt bijvoorbeeld de tekststijl, opvulling of marge van elke component wijzigen. [Meer informatie over uitlijning en opvulling](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Container {#container}

U kunt een eenvoudige container toevoegen waarin u een andere inhoudscomponent kunt toevoegen. Op deze manier kunt u een specifieke stijl op de container toepassen. Deze stijl verschilt van de binnenste component.

Voeg bijvoorbeeld een **[!UICONTROL Container]** en voegt vervolgens een [Knop](#button) in die container. U kunt een specifieke achtergrond voor de container, en een andere voor de knoop gebruiken.

![](assets/email_designer_container_component.png)

## Knop {#button}

Gebruik de **[!UICONTROL Button]** om een of meerdere knoppen in te voegen in uw e-mail en uw e-mailpubliek om te leiden naar een andere pagina.

1. Van **[!UICONTROL Content components]**, slepen en neerzetten **[!UICONTROL Button]** in een **[!UICONTROL Structure component]**.

1. Klik op de knop die u net hebt toegevoegd om de tekst aan te passen en toegang te krijgen tot de knop **[!UICONTROL Components settings]** in het rechterdeelvenster van E-mailontwerper.

   ![](assets/email_designer_button_component.png)

1. In de **[!UICONTROL Link]** , voegt u de URL toe waarnaar u wilt omleiden wanneer u op de knop klikt.

1. Kies hoe de doelgroep wordt omgeleid met de **[!UICONTROL Target]** vervolgkeuzelijst:

   * **[!UICONTROL None]**: Hiermee opent u de koppeling in hetzelfde frame als waarop u hebt geklikt (standaard).
   * **[!UICONTROL Blank]**: Hiermee opent u de koppeling in een nieuw venster of op een nieuw tabblad.
   * **[!UICONTROL Self]**: Hiermee opent u de koppeling in hetzelfde frame als waarop u hebt geklikt.
   * **[!UICONTROL Parent]**: Hiermee opent u de koppeling in het bovenliggende frame.
   * **[!UICONTROL Top]**: Hiermee opent u de koppeling in de volledige tekst van het venster.

   ![](assets/email_designer_button_link.png)

1. U kunt de knop verder aanpassen door opmaakkenmerken te wijzigen, zoals **[!UICONTROL Border]**, **[!UICONTROL Size]**, **[!UICONTROL Margin]**, enz. van de **[!UICONTROL Component settings]** venster.

## Tekst {#text}

Gebruik de **[!UICONTROL Text]** om tekst in te voegen in uw e-mail, en de stijl (rand, grootte, opvulling, enz.) aan te passen met de **[!UICONTROL Component settings]** venster.

![](assets/email_designer_text_component.png)

1. Van **[!UICONTROL Content components]**, slepen en neerzetten **[!UICONTROL Text]** in een **[!UICONTROL Structure component]**.

1. Klik op de nieuwe component om de tekst aan te passen en toegang te krijgen tot de component **[!UICONTROL Components Settings]** in het rechterdeelvenster van de E-mailontwerper.

1. Wijzig de tekst met de volgende opties beschikbaar op de werkbalk:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: u kunt uw tekst vet, cursief, onderstrepen of doorhalen.
   * **Uitlijning wijzigen**: kiest u tussen links, rechts, centreren of uitvullen voor de tekst.
   * **[!UICONTROL Create list]**: Voeg opsommingstekens of nummers toe aan uw tekst.
   * **[!UICONTROL Set heading]**: Voeg maximaal zes kopniveaus aan uw tekst toe.
   * **Fontgrootte**: Selecteer de tekengrootte van de tekst in pixels.
   * **[!UICONTROL Edit image]**: Voeg een afbeelding of een element toe aan uw tekstcomponent. [Meer informatie over middelenbeheer](assets-essentials.md)
   * **[!UICONTROL Show the source code]**: de broncode van de tekst weergeven. Het kan niet worden gewijzigd.
   * **[!UICONTROL Duplicate]**: Voeg een kopie van de tekstcomponent toe.
   * **[!UICONTROL Delete]**: Verwijder de geselecteerde tekstcomponent uit uw e-mail.
   * **[!UICONTROL Add personalization]**: Voeg verpersoonlijkingsgebieden toe om de inhoud van uw profielgegevens aan te passen. [Meer informatie over content personalization](../personalization/personalize.md)
   * **[!UICONTROL Enable conditional content]**: Voeg voorwaardelijke inhoud toe om de inhoud van de component aan de beoogde profielen aan te passen. [Meer informatie over dynamische inhoud](../personalization/get-started-dynamic-content.md)

1. Pas de andere opmaakkenmerken aan, zoals tekstkleur, lettertypefamilie, rand, opvulling, marge, enzovoort. van de **[!UICONTROL Component settings]** venster.

## Scheidingslijn {#divider}

Gebruik de **[!UICONTROL Divider]** om een scheidingslijn in te voegen om de lay-out en inhoud van uw e-mail te ordenen.

U kunt opmaakkenmerken zoals lijnkleur, -stijl en -hoogte aanpassen vanuit het dialoogvenster **[!UICONTROL Component settings]** venster.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Gebruik de **[!UICONTROL HTML]** om de verschillende onderdelen van uw bestaande HTML te kopiëren en te plakken. Hierdoor kunt u gratis modulaire HTML-componenten maken om externe inhoud opnieuw te gebruiken.

1. Van **[!UICONTROL Content Components]**, slepen en neerzetten **[!UICONTROL HTML]** in een **[!UICONTROL Structure component]**.

1. Klik op de zojuist toegevoegde component en selecteer vervolgens **[!UICONTROL Show the source code]** van de contextafhankelijke werkbalk om uw HTML toe te voegen.

   ![](assets/email_designer_html_component.png)

1. Kopieer en plak de HTML-code die u aan uw e-mail wilt toevoegen en klik op **[!UICONTROL Save]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Om een externe inhoud eenvoudig compatibel te maken met de e-mailontwerper, raadt Adobe u aan een geheel nieuw bericht te maken en de inhoud van uw bestaande e-mail naar componenten te kopiëren.

## Afbeelding {#image}

Gebruik de **[!UICONTROL Image]** om een afbeeldingsbestand van uw computer in te voegen in uw e-mailinhoud.

1. Van **[!UICONTROL Content components]**, slepen en neerzetten **[!UICONTROL Image]** in een **[!UICONTROL Structure component]**.

1. Klikken **[!UICONTROL Browse]** om een afbeeldingsbestand te kiezen uit uw elementen.

   Meer informatie over [!DNL Assets Essentials], zie [Adobe Experience Manager Assets Essentials-documentatie](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Klik op de nieuwe component en stel de afbeeldingseigenschappen in met de opdracht **[!UICONTROL Components settings]** deelvenster:

   * **[!UICONTROL Image title]** Hiermee kunt u een titel voor de afbeelding definiëren.
   * **[!UICONTROL Alt text]** Hiermee kunt u het bijschrift definiëren dat aan de afbeelding is gekoppeld. Dit komt overeen met het kenmerk alt HTML.

   ![](assets/email_designer_10.png)

1. Pas de andere opmaakkenmerken aan, zoals marge, rand, enz. of u voegt een koppeling toe om uw publiek om te leiden naar een andere inhoud vanuit de **[!UICONTROL Component settings]** venster.

## Video {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Video-instellingen"
>abstract="Gebruik deze component om een video in te voegen in uw e-mail. Video&#39;s werken niet voor alle e-mailclients. We raden u aan een fallback-afbeelding in te stellen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Video-instellingen"
>abstract="Gebruik deze component om een video in te voegen in uw openingspagina. Video&#39;s werken niet op alle berichtclients. We raden u aan een fallback-afbeelding in te stellen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Video-instellingen"
>abstract="Gebruik deze component om een video in te voegen in uw fragment. Video&#39;s werken niet op alle berichtclients. We raden u aan een fallback-afbeelding in te stellen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Video-instellingen"
>abstract="Gebruik deze component om een video in uw sjabloon in te voegen. Video&#39;s werken niet op alle berichtclients. We raden u aan een fallback-afbeelding in te stellen."

Gebruik de **[!UICONTROL Video]** om een video in te voegen in uw e-mailinhoud via een URL-koppeling.

1. Van **[!UICONTROL Content Components]**, slepen en neerzetten **[!UICONTROL Video]** component in een **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Klik op de nieuwe component.

1. In de **[!UICONTROL Video link]** van het **[!UICONTROL Components settings]** toevoegen.

   ![](assets/email_designer_18.png)

1. U kunt een **[!UICONTROL Poster image]** op uw video om een afbeelding op te geven die moet worden weergegeven totdat uw publiek op de afspeelknop klikt.

1. Pas de andere opmaakkenmerken aan, zoals stijl, marge, rand, enzovoort. van de **[!UICONTROL Component settings]** venster.

## Social {#social}

Gebruik de **[!UICONTROL Social]** om koppelingen naar pagina&#39;s met sociale media in te voegen in uw e-mailinhoud.

1. Van **[!UICONTROL Content Components]**, slepen en neerzetten **[!UICONTROL Social]** in een **[!UICONTROL Structure component]**.

1. Klik op de nieuwe component.

1. In de **[!UICONTROL Social]** van het **[!UICONTROL Components settings]** kiest u welke sociale media u wilt toevoegen of verwijderen.

   ![](assets/email_designer_20.png)

1. Kies de grootte van de pictogrammen in het desbetreffende veld.

1. Klik op elk van uw pictogrammen voor sociale media om het dialoogvenster **[!UICONTROL URL]** waarnaar uw publiek wordt omgeleid.

   ![](assets/email_designer_21.png)

1. U kunt de pictogrammen van elk van uw sociale media desgewenst ook wijzigen in het dialoogvenster **[!UICONTROL Image]** veld.

1. Pas de andere opmaakkenmerken aan, zoals stijl, marge, rand, enzovoort. van de **[!UICONTROL Component settings]** venster.

## Offertebeslissing {#offer-decision}

Gebruik de **[!UICONTROL Offer decision]** om aanbiedingen in te voegen in uw berichten. De [beslissingsbeheer](../offers/get-started/starting-offer-decisioning.md) engine kiest de beste aanbieding voor uw klanten.

Leer hoe u persoonlijke aanbiedingen kunt toevoegen aan een e-mailbericht in [deze sectie](add-offers-email.md).

