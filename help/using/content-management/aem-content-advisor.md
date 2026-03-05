---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Manager Content Advisor benaderen
description: Leer hoe u Adobe Experience Manager Content Advisor kunt openen en gebruiken om elementen en inhoudsfragmenten te ontdekken met behulp van semantische zoekopdrachten op basis van AI in Adobe Journey Optimizer.
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 842d69e3-be7f-4a81-8161-6c6ecd571f95
source-git-commit: c9856234149c0f377e625a789c96f1f1f0453000
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Werken met Adobe Experience Manager Content Advisor {#aem-content-advisor}

>[!AVAILABILITY]
>
>Adobe Experience Manager Content Advisor is alleen beschikbaar in workflows voor het ontwerpen van kanalen.

Adobe Experience Manager Content Advisor vervangt deterministische ontdekkingen door gestandaardiseerde, intent-gedreven ontdekking vanaf één enkel oppervlak. Het maakt het mogelijk om Assets en Content Fragments met één AI-processor rechtstreeks te detecteren in workflows voor het ontwerpen van Journey Optimizer, waardoor de productiviteit van de markt en de efficiëntie van de campagne worden verbeterd.

## Beschikbare functies

### Voor Assets {#asset-features}

Adobe Experience Manager Content Advisor biedt de volgende functies voor bedrijfsmiddelen:

* 
  +++ AI semantische zoekopdracht

  Zoeken naar elementen met een natuurlijke taal in plaats van exacte trefwoorden of bestandsnamen. Beschrijf wat u in gewone taal nodig hebt, bijvoorbeeld &quot;koffie in de bergen&quot;, en de AI vindt contextafhankelijke activa gebaseerd op betekenis en inhoud, niet alleen tekstovereenkomsten.

  ![](assets/content-advisor-2.png){zoomable="yes"}

  +++

* 
  +++ Recente zoekgeschiedenis

  Open je recente zoekopdrachten en gebruik trefwoorden en contexten snel opnieuw. Dit bespaart tijd wanneer het werken aan gelijkaardige campagnes of wanneer u vorige onderzoeken moet verfijnen.

  ![](assets/content-advisor-4.png){zoomable="yes"}

  +++ 

* 
  +++ Uploadinstructie

  Upload een kort marketingdocument om automatisch elementen weer te geven die zijn afgestemd op de context van uw campagne. De AI analyseert uw opdracht en stelt relevante elementen voor op basis van de inhoud en vereisten die in het document worden beschreven.

  ![](assets/content-advisor-5.png){zoomable="yes"}

  +++

* 
  +++ Deelvenster Elementinformatie

  Gedetailleerde meta-gegevens en eigenschappen van de mening voor om het even welk middel gebruikend het **pictogram van Info**. Hiertoe behoren de afmetingen van de elementen, de bestandsgrootte, de aanmaakdatum, codes en andere relevante informatie die u helpt geïnformeerde beslissingen te nemen.

  ![](assets/content-advisor-6.png){zoomable="yes"}

  +++

* 
  +++ Deelvenster Dynamische media

  Toegang tot dynamische uitvoeringen, slimme gewassen en wijzigingen ter plaatse op basis van de configuratie van de opslagplaats.

  ![](assets/content-advisor-1.png){zoomable="yes"}

  Het deelvenster Dynamische media biedt toegang tot dynamische uitvoeringen, slimme uitsnijdingen en wijzigingen ter plekke. U kunt opties rechtstreeks in het deelvenster invoeren om aangepaste uitvoeringen te maken.

  **Beschikbaarheid**

  De beschikbaarheid van dynamische media is afhankelijk van de configuratie van de opslagplaats:

   * **Scene7**: Beschikbaar voor gepubliceerde activa (behalve Video en PDF). [ Leer meer op Dynamische de wijzigingstoetsen van Media Scene7 ](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-is-http-modifiers.html){target="_blank"}

   * **OpenAPI**: Beschikbaar voor goedgekeurde activa (behalve Video). [ leer meer op Dynamische Media met modifiers OpenAPI ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/image-profiles.html){target="_blank"}

   * **zowel Scene7 als OpenAPI**: Beschikbaar wanneer beide configuraties bestaan en de activa aan de criteria voldoen.

  **de selectie van de Stapel**

  De knoppen die u ziet, zijn afhankelijk van de configuratie van de opslagplaats:

   * **knoop Scene7 slechts**: De bewaarplaats heeft configuratie Scene7 en de activa wordt gepubliceerd aan Dynamische Media.
   * **knoop OpenAPI slechts**: De bewaarplaats heeft configuratie OpenAPI en de activa wordt goedgekeurd.
   * **Beide knopen**: De Bewaarplaats heeft zowel configuraties als activa wordt gepubliceerd en goedgekeurd.
  +++

### Voor inhoudsfragment {#content-fragment-features}

Adobe Experience Manager Content Advisor biedt de volgende functies voor inhoudsfragmenten:

* 
  +++ Sjabloonweergaveoverzicht 

  Schakel tussen miniaturen en tabelweergaven om door Content Fragments te bladeren in de indeling die het beste bij uw workflow past. De miniatuurweergave biedt visuele context, terwijl de tabelweergave gedetailleerde informatie in een gestructureerde indeling weergeeft.

  ![](assets/content-advisor-7.png){zoomable="yes"}

  +++

* 
  +++ Info, deelvenster 

  Klik op het pictogram **[!UICONTROL Info]** om een rechterdeelvenster te openen met fragmentvariaties, -eigenschappen en **[!UICONTROL Referenced By]** -details. In de sectie **[!UICONTROL Referenced By]** worden alle Adobe Experience Manager-entiteiten weergegeven waarin het fragment wordt gebruikt, met koppelingen om deze verwijzingen rechtstreeks in Adobe Experience Manager weer te geven.

  ![](assets/content-advisor-8.png){zoomable="yes"}

  +++

* 
  +++ Openen in Adobe Experience Manager

  Open snel een inhoudsfragment rechtstreeks in Adobe Experience Manager en bewerk het met het pictogram naast de titel. Dankzij deze naadloze integratie kunt u schakelen tussen Journey Optimizer en Adobe Experience Manager zonder dat u de context verliest.

  ![](assets/content-advisor-9.png){zoomable="yes"}

  +++

* 
  +++ JSON-voorvertoning

  Geef een voorvertoning van de JSON-structuur van inhoudsfragmenten weer in een schone, geordende tabelindeling. Zo krijgt u inzicht in de gegevensstructuur van het fragment en kunt u de inhoud controleren voordat u het fragment in uw campagnes gebruikt.

  ![](assets/content-advisor-10.png){zoomable="yes"}

  +++

## Adobe Experience Manager Content Advisor benaderen {#access}

Ga als volgt te werk om Adobe Experience Manager Content Advisor in Journey Optimizer te openen:

1. Maak een campagne in Adobe Journey Optimizer en voeg een kanaalactie toe, bijvoorbeeld E-mail.

1. Klik op **[!UICONTROL Edit Content]** en vervolgens op **[!UICONTROL Edit Email Body]** om de inhoudeditor te openen.

1. Sleep een HTML- of tekstcomponent naar uw e-mailinhoud.

1. Houd de cursor boven de component en klik op **[!UICONTROL Show the source code]** (voor HTML-componenten) of **[!UICONTROL Add Personalization]** (voor Text-componenten).

1. Kies in de Personalization Editor het toegangspunt voor de inhoud:

   * Als u een element wilt toevoegen, klikt u op **[!UICONTROL Assets]** en vervolgens op **[!UICONTROL Open AEM Content Advisor]** .

     ![](assets/content-advisor-11.png){zoomable="yes"}

   * Als u een Adobe Experience Manager-inhoudsfragment wilt toevoegen, klikt u op **[!UICONTROL AEM Content Fragment]** en vervolgens op **[!UICONTROL Open AEM Content Advisor]** .

     ![](assets/content-advisor-12.png){zoomable="yes"}

1. Selecteer uw Adobe Experience Manager-opslagplaats.

   ![](assets/content-advisor-13.png){zoomable="yes"}

1. Blader naar het element of inhoudsfragment dat u wilt gebruiken en selecteer het. Voeg het fragment vervolgens in de inhoud in.
