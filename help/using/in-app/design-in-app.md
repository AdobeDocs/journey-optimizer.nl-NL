---
title: In-app-inhoud ontwerpen
description: Leer hoe u inhoud in de app ontwerpt in Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, ontwerp, opmaak
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# In-app-inhoud ontwerpen {#design-content}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_content"
>title="In-app-inhoud definiëren"
>abstract="Pas de inhoud en de stijl van uw in-app berichten aan. U kunt ook media- en actieknoppen toevoegen om uw berichten aantrekkelijker en effectiever te maken."

U kunt de inhoud in de app bewerken om ervaringsopties te configureren:

* In een **[!UICONTROL Campaign]** van de **[!UICONTROL Action]** om de berichtinhoud te configureren, klikt u op de knop **[!UICONTROL Edit content]** knop.

  ![](assets/edit-in-app-content.png)

* In een **[!UICONTROL Journey]** in het geavanceerde menu van uw In-app **[!UICONTROL Action]** kunt u uw inhoud ontwerpen met de **[!UICONTROL Edit content]** knop.

  ![](assets/design_inapp_journey.png)

De **[!UICONTROL Advanced formatting]** als u schakelt, worden aanvullende opties geactiveerd om de ervaring aan te passen.

Nadat u het bericht in de app hebt gemaakt en de inhoud ervan hebt gedefinieerd en gepersonaliseerd, kunt u het bericht controleren en activeren. Vervolgens worden de meldingen verzonden volgens het campagneprogramma. Meer informatie in [deze pagina](send-in-app.md).

## Berichtlay-out {#message-layout}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_layout"
>title="In-app-inhoud definiëren"
>abstract="De berichtlay-out voorziet u van algemeen gebruikte malplaatjes om uw bericht te voorzien. Aangepaste indeling biedt opties voor het uploaden of samenstellen van aangepaste HTML-berichten."

Van de **[!UICONTROL Message Layout]** , selecteert u een van de vier verschillende indelingsopties waaruit u kunt kiezen, afhankelijk van uw berichtenbehoeften.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL Fullscreen]**: Dit type lay-out bedekt het volledige scherm van uw publieksapparaten.

  De klasse ondersteunt media (afbeeldingen, video), tekst en knopcomponenten.

* **[!UICONTROL Modal]**: Deze lay-out wordt weergegeven in een groot waarschuwingsvenster en de toepassing is nog steeds zichtbaar op de achtergrond.

  De klasse ondersteunt media (afbeeldingen, video), tekst en knopcomponenten.

* **[!UICONTROL Banner]**: Dit type lay-out wordt weergegeven als een waarschuwingsbericht voor het native besturingssysteem.

  U kunt alleen een **[!UICONTROL Header]** en **[!UICONTROL Body]** aan uw bericht.

* **[!UICONTROL Custom]**: In de modus Aangepast bericht kunt u een van de vooraf geconfigureerde HTML-berichten rechtstreeks importeren en bewerken.

   * Selecteren **[!UICONTROL Compose]** om de onbewerkte HTML-code in te voeren of te plakken.

     Gebruik het linkerdeelvenster om de personalisatiemogelijkheden van Journey Optimizer te benutten. Raadpleeg voor meer informatie hierover [deze sectie](../personalization/personalize.md).

   * Selecteren **[!UICONTROL Import]** om het HTML- of ZIP-bestand met uw HTML-inhoud te importeren.

## Inhoud, tabblad {#content-tab}

Van de **Inhoud** kunt u de inhoud van het bericht en de stijl van het dialoogvenster **Sluiten** knop. U kunt ook media toevoegen aan uw melding in de app en actieknoppen toevoegen vanaf dit tabblad.

### Knop Sluiten {#close-button}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_close"
>title="Kies de Stijl van uw Dichte knoop."
>abstract="In de sectie Knop Sluiten kunt u opties selecteren voor het selecteren van variaties van de knop Sluiten van het bericht en kunt u een aangepaste afbeelding uploaden."

![](assets/in_app_web_design_2.png)

Kies de optie **[!UICONTROL Style]** van uw **[!UICONTROL Close button]**.

Beschikbare stijlen zijn:

* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** via een media-URL of uw middelen.

+++Meer opties met geavanceerde opmaak

Als de **[!UICONTROL Advanced formatting mode]** is ingeschakeld, kunt u controleren **[!UICONTROL Color]** om de kleur en dekking van de knop te kiezen.

+++

### Media {#add-media}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_media"
>title="Voeg media toe aan uw bericht in de app om een aantrekkelijke ervaring voor de eindgebruiker te creëren."
>abstract="Geef een directe koppeling naar de inhoud op of gebruik de kiezer voor middelen om media in Essentiële elementen te selecteren om aan uw bericht toe te voegen."

De **[!UICONTROL Media]** kunt u media toevoegen aan uw In-app-bericht om een aantrekkelijke ervaring voor de eindgebruiker te creëren.

![](assets/in_app_web_design_3.png)

Typ uw media-URL of klik op de knop **[!UICONTROL Select Assets]** om elementen die in uw middelenbibliotheek zijn opgeslagen, rechtstreeks toe te voegen aan uw In-app-bericht. [Meer informatie over middelenbeheer](../content-management/assets.md).
U kunt ook een **[!UICONTROL Alternative text]** voor toepassingen voor schermlezen.

+++Meer opties met geavanceerde opmaak

Als de **[!UICONTROL Advanced formatting mode]** is ingeschakeld, kunt u de **[!UICONTROL Max height]** en **[!UICONTROL Max width]** van uw media.

+++

### Inhoud {#title-body}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_content"
>title="Als u uw bericht wilt samenstellen, voert u de inhoud in de velden Koptekst en Hoofdtekst in."
>abstract="Hier kan zowel de koptekst als de hoofdtekst worden toegevoegd. Als u personalisatietokens wilt opnemen, opent u het dialoogvenster voor personalisatie."

Als u uw bericht wilt samenstellen, voert u de inhoud in het dialoogvenster **[!UICONTROL Header]** en **[!UICONTROL Body]** velden.

![](assets/in_app_web_design_4.png)

Gebruik de **[!UICONTROL Personalization]** pictogram om personalisatie toe te voegen. Meer informatie over personalisatie in de Adobe Journey Optimizer personalization editor [in deze sectie](../personalization/personalize.md).

+++Meer opties met geavanceerde opmaak

Als de **[!UICONTROL Advanced formatting mode]** is ingeschakeld, kunt u kiezen voor uw **[!UICONTROL Header]** en **[!UICONTROL Body]**:

* de **[!UICONTROL Font]**
* de **[!UICONTROL Pt size]**
* de **[!UICONTROL Font Color]**
* de **[!UICONTROL Alignment]**
+++

### Knoppen {#add-buttons}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_buttons"
>title="Voeg knoppen toe waarmee gebruikers kunnen communiceren met uw In-app-bericht."
>abstract="Deze sectie zal u toestaan om vraag-aan-actie knopen aan uw bericht toe te voegen. U kunt aangepaste tekst en doelen voor elke knop opnemen."

Voeg knoppen toe waarmee gebruikers kunnen communiceren met uw In-app-bericht.

![](assets/in_app_web_design_5.png)

Zo past u de knop aan:

1. Bewerk het veld Knop #1 (primaire). U kunt ook de opdracht **[!UICONTROL Personalization]** pictogram voor het definiëren van inhoud en aanpassingsgegevens.

1. Kies uw **[!UICONTROL Interact event]** Hiermee definieert u de actie van de knop nadat gebruikers er interactie mee hebben gehad.

1. Voer de URL van uw web in of selecteer deze in het dialoogvenster **[!UICONTROL Target]** veld.

1. Klik op **[!UICONTROL Add button]**.

+++Meer opties met geavanceerde opmaak

Als de **[!UICONTROL Advanced formatting mode]** is ingeschakeld, kunt u kiezen voor uw **[!UICONTROL Buttons]**:

* de **[!UICONTROL Font]**
* de **[!UICONTROL Pt size]**
* de **[!UICONTROL Font Color]**
* de **[!UICONTROL Alignment]**
* de **[!UICONTROL Button style]**
* de **[!UICONTROL Radius]**
* de **[!UICONTROL Button color]**

+++

## Het tabblad Instellingen {#settings-tab}

Van de **Instellingen** kunt u de berichtlay-out definiëren en een voorvertoning van uw In-app-bericht weergeven. U hebt ook toegang tot geavanceerde opmaakopties.

### Voorvertoning {#preview-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_preview"
>title="Geef een voorvertoning weer van uw bericht in de app."
>abstract="Dit is de voorvertoningsafbeelding die wordt weergegeven wanneer uw bericht naar het berichtenoverzicht van het apparaat wordt verzonden."

>[!NOTE]
>
>Voorvertoning is alleen beschikbaar voor mobiele berichten in de app.

![](assets/in_app_content_6.png)

De **[!UICONTROL App Preview]** kunt u een achtergrond toevoegen achter uw In-app-bericht:

* Een medium via een URL-koppeling.

* Een middel uit uw bibliotheek van Activa.

* Een achtergrondkleur.

### Layout {#layout-options}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_layout"
>title="Bepaal de berichtlay-out van uw In-app bericht."
>abstract="In deze sectie kunt u een achtergrond toevoegen aan uw In-app-bericht. Hiervoor moet de overname van de gebruikersinterface zijn ingeschakeld."

![](assets/in_app_web_design_6.png)

De **[!UICONTROL Background image]** kunt u een achtergrond toevoegen aan uw In-app-bericht:

* Een medium via een URL-koppeling.

* Een achtergrondkleur.

### Bericht {#message-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_advanced"
>title="Definieer de geavanceerde instellingen voor berichten."
>abstract="In deze sectie kunt u de inhoud in de app aanpassen, met name wanneer Geavanceerde opmaak is ingeschakeld."

![](assets/in_app_web_design_7.png)

Met de optie UI-overname, die standaard is ingeschakeld, kunt u de achtergrond achter uw In-app-bericht donkerder maken om de focus op uw inhoud te benadrukken.

+++Meer opties met geavanceerde opmaak

Als de **[!UICONTROL Advanced formatting mode]** is ingeschakeld, kunt u uw bericht verder personaliseren met de volgende opties:

* **[!UICONTROL Customize gestures]**: hiermee kunt u aanpassen wat de interactie met een veegbeweging van de gebruiker is. Als sluiten is geselecteerd, kunt u een aangepaste interactie-gebeurtenis en/of doelbestemming toevoegen.

* **[!UICONTROL Customize UI takeover]**: hiermee kunt u een kleur selecteren die op de achtergrond en de dekking wordt weergegeven.

* **[!UICONTROL Customize size]**: hiermee kunt u de breedte en hoogte van uw In-app-melding aanpassen.

* **[!UICONTROL Customize position]**: hiermee kunt u de positie van uw In-app-berichten op het scherm van uw gebruikers aanpassen. U kunt de verticale en horizontale uitlijning wijzigen.

* **[!UICONTROL Customize animation]** Met : kunt u de animaties Weergeven en Afwijzen aanpassen, bijvoorbeeld als u een melding in de app links of boven op het apparaat van de gebruiker verschijnt.

* **[!UICONTROL Message round corner]**: hiermee kunt u ronde hoeken toevoegen aan uw In-app-melding door het dialoogvenster **[!UICONTROL Corner radius]**.

+++

**Verwante onderwerpen:**

* [In-app-bericht maken](create-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u uw In-app-berichten kunt ontwerpen en testen.

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
