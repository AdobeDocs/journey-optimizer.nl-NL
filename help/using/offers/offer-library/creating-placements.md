---
title: Plaatsingen maken
description: Leer hoe u plaatsingen voor uw aanbiedingen kunt maken
badge: label="Verouderd" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 1%

---

# Plaatsingen maken {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="Plaatsing"
>abstract="Een plaatsing is een container die wordt gebruikt om aanbiedingen te tonen. Het helpt ervoor te zorgen dat de juiste aanbiedingsinhoud op de juiste plaats binnen uw bericht verschijnt. Plaatsen worden gemaakt via het menu &quot;Componenten&quot;."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_request"
>title="Instellingen aanvragen"
>abstract="Schakel de optie **[!UICONTROL Allow Duplicates across placements]** in om ervoor te zorgen dat het systeem rekening houdt met dezelfde aanbieding voor meerdere plaatsingen. Gebruik het veld **[!UICONTROL Request offer]** om het aantal geretourneerde voorstellen aan te passen. Als u bijvoorbeeld 2 selecteert, worden de beste 2 aanbiedingen weergegeven voor het geselecteerde beslissingsbereik."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement_response"
>title="Responsindeling"
>abstract="Met de opties **[!UICONTROL Include content]** en **[!UICONTROL Include metadata]** kunt u opgeven of de inhoud en metagegevens van de aanbieding moeten worden geretourneerd in de API-reactie. U kunt alleen alle metagegevens of specifieke velden opnemen. De waarde voor Inclusief metagegevens is standaard ingesteld op true."

Een plaatsing helpt ervoor te zorgen dat de juiste aanbiedingsinhoud op de juiste plaats binnen uw bericht verschijnt. Wanneer u inhoud aan een aanbieding toevoegt, wordt u gevraagd een plaatsing te selecteren waarin die inhoud kan worden weergegeven.

➡️ [ Leer hoe te plaatsen in deze video ](#video) tot stand te brengen

In het onderstaande voorbeeld zijn er drie plaatsen die overeenkomen met verschillende typen inhoud (afbeelding, tekst, HTML).

![](../assets/offers_placement_schema.png)

De lijst met plaatsen is toegankelijk in het menu **[!UICONTROL Components]** . Er zijn filters beschikbaar waarmee u plaatsingen kunt ophalen op basis van een specifiek kanaal of specifieke inhoud.

![](../assets/placements_filter.png)

Voer de volgende stappen uit om een plaatsing te maken:

1. Klik op **[!UICONTROL Create placement]**.

   ![](../assets/offers_placement_creation.png)

1. Definieer de eigenschappen van de plaatsing:

   * **[!UICONTROL Name]**: De naam van de plaatsing. Zorg ervoor dat u een betekenisvolle naam definieert om deze eenvoudiger op te halen.
   * **[!UICONTROL Channel type]**: Het kanaal waarvoor de plaatsing wordt gebruikt.
   * **[!UICONTROL Content type]**: Het type inhoud dat de plaatsing mag weergeven: Tekst, HTML, Afbeeldingskoppeling of JSON.
   * **[!UICONTROL Description]**: Een beschrijving van de plaatsing (optioneel).

   ![](../assets/offers_placement_creation_properties.png)

1. De secties **[!UICONTROL Request settings]** en **[!UICONTROL Response format]** bevatten aanvullende parameters:

   * **[!UICONTROL Allow Duplicates across placements]**: Bepaal of hetzelfde aanbod meerdere keren op verschillende plaatsen kan worden voorgesteld. Als deze optie is ingeschakeld, overweegt het systeem dezelfde aanbieding voor meerdere plaatsingen. Standaard is de parameter ingesteld op false.

     Als deze optie voor om het even welke plaatsing in een beslissingsverzoek aan vals wordt geplaatst, zullen alle plaatsen in het verzoek het &quot;vals&quot;plaatsen erven.

   * **[!UICONTROL Request offer]**: Standaard wordt één aanbieding van het beslissingsbereik geretourneerd voor elk profiel. Met deze optie kunt u het aantal geretourneerde voorstellen aanpassen. Als u bijvoorbeeld 2 selecteert, worden de beste 2 aanbiedingen weergegeven voor het geselecteerde beslissingsbereik.

   * **[!UICONTROL Include content]** / **[!UICONTROL Include metadata]** : geef op of de inhoud en metagegevens van de aanbieding moeten worden geretourneerd in de API-reactie. U kunt alleen alle metagegevens of specifieke velden opnemen. De waarde voor Inclusief metagegevens is standaard ingesteld op true.

   Deze parameters kunnen ook direct in uw API verzoek worden geplaatst als u met [ Beslissing API ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html) werkt. Als u deze echter configureert in de gebruikersinterface, kunt u tijd besparen omdat u deze niet in elke API-aanvraag hoeft door te geven. Merk op dat als u de parameters zowel in gebruikersinterface als het API verzoek vormt, de waarden van het API verzoek over degenen van de interface zullen prevaleren.

   >[!NOTE]
   >
   >Als u met [ Edge beslist API ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?) werkt, kunt u niet deze parameters in uw verzoek plaatsen. U moet ze in dit scherm definiëren.
   >
   >Als u met de [ Bevestiging API van de Partij ](../api-reference/offer-delivery-api/batch-decisioning-api.md) werkt, kunt u deze parameters of in dit scherm of in uw API verzoek plaatsen. Als parameterwaarden niet overeenkomen tussen het scherm en het APi-verzoek, worden de aanvraagwaarden gebruikt.

1. Klik op **[!UICONTROL Save]** om te bevestigen.

1. Zodra de plaatsing wordt gecreeerd, toont het in de plaatsingslijst. U kunt het selecteren om zijn eigenschappen te tonen en het uit te geven.

   ![](../assets/placement_created.png)

## Hoe kan ik-video{#video}

Leer hoe u plaatsingen in het besluitvormingsbeheer kunt maken.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

