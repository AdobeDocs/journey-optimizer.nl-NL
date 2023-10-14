---
title: Aan de slag
description: Leer hoe u de bibliotheek-API van de Aanbieding kunt gebruiken om toetsbewerkingen uit te voeren met de beslissingsengine.
feature: Offers, API
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---

# Handleiding voor ontwikkelaars van API voor beheer van beslissingen {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Nieuwe API&#39;s voor besluitvormingsbeheer"
>abstract="Nieuwe API&#39;s voor het maken en beheren van besluitvormingsbeheerobjecten zijn nu beschikbaar. De oudere API&#39;s worden ondersteund tot 27-03-2024."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Nieuwe API&#39;s voor besluitvormingsbeheer"
>abstract="Nieuwe API&#39;s voor het maken en beheren van besluitvormingsbeheerobjecten zijn nu beschikbaar. De oudere API&#39;s worden ondersteund tot 27-03-2024."

Deze handleiding voor ontwikkelaars bevat stappen waarmee u de functie [!DNL Offer Library] API. De gids verstrekt dan steekproefAPI vraag voor het uitvoeren van zeer belangrijke verrichtingen gebruikend de bepalingsmotor.

➡️ [Meer informatie over de componenten van Beslissingsbeheer vindt u in deze video](#video)

## Vereisten {#prerequisites}

Deze handleiding vereist een goed begrip van de volgende onderdelen van Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}: Het gestandaardiseerde kader waarbinnen [!DNL Experience Platform] organiseert de gegevens van de klantenervaring.
   * [Basisbeginselen van de schemacompositie](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target="_blank"}: Leer over de basisbouwstenen van schema&#39;s XDM.
* [Beslissingsbeheer](../../../using/offers/get-started/starting-offer-decisioning.md): Verklaart de concepten en componenten die worden gebruikt voor het nemen van een besluit over de ervaring in het algemeen en het nemen van een besluit in het bijzonder. Toont de strategieën die voor het kiezen van de beste optie worden gebruikt om tijdens de ervaring van een klant voor te stellen.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL is een krachtige taal voor het schrijven van expressies over XDM-instanties. PQL wordt gebruikt om besluitvormingsregels te bepalen.

## API-voorbeeldaanroepen lezen {#reading-sample-api-calls}

Deze gids verstrekt voorbeeld API vraag om aan te tonen hoe te om uw verzoeken te formatteren. Dit zijn paden, vereiste kopteksten en correct opgemaakte ladingen voor aanvragen. Voorbeeld-JSON die wordt geretourneerd in API-reacties, wordt ook verschaft. Voor informatie over de conventies die worden gebruikt in documentatie voor voorbeeld-API-aanroepen raadpleegt u de sectie over [voorbeeld-API-aanroepen lezen](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} in de [!DNL Experience Platform] gids voor probleemoplossing.

## Waarden verzamelen voor vereiste koppen {#gather-values-for-required-headers}

Om vraag te maken aan [!DNL Adobe Experience Platform] API&#39;s, moet u eerst de [verificatiezelfstudie](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. Het voltooien van de zelfstudie over verificatie biedt de waarden voor elk van de vereiste kopteksten in alle [!DNL Experience Platform] API-aanroepen, zoals hieronder wordt getoond:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Alle verzoeken die een nuttige lading (POST, PUT, PATCH) bevatten vereisen een extra kopbal:

* `Content-Type: application/json`

## Volgende stappen {#next-steps}

Dit document bevatte de vereiste kennis die nodig was om oproepen te doen aan de [!DNL Offer Library] API. U kunt nu aan de steekproefvraag verdergaan die in deze ontwikkelaarsgids wordt verstrekt en samen met hun instructies volgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Hoe kan ik-video {#video}

De volgende video is bedoeld om uw begrip van de componenten van Beslissingsbeheer te steunen.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

