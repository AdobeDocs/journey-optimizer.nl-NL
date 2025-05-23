---
title: Aan de slag
description: Leer hoe u de bibliotheek-API van de Aanbieding kunt gebruiken om toetsbewerkingen uit te voeren met de beslissingsengine.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 1%

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

Deze handleiding voor ontwikkelaars bevat stappen waarmee u de API van [!DNL Offer Library] kunt gaan gebruiken. De gids verstrekt dan steekproefAPI vraag voor het uitvoeren van zeer belangrijke verrichtingen gebruikend de bepalingsmotor.

➡️ [ leer meer over de componenten van het Beheer van het Besluit in deze video ](#video)

## Vereisten {#prerequisites}

Deze handleiding vereist een goed begrip van de volgende onderdelen van Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System] ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"} : Het gestandaardiseerde kader waardoor [!DNL Experience Platform] de gegevens van de klantenervaring organiseert.
   * [ Grondbeginselen van schemacompositie ](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=nl-NL){target="_blank"} : Leer over de basisbouwstenen van schema&#39;s XDM.
* [ Beheer van het Besluit ](../../../using/offers/get-started/starting-offer-decisioning.md): Verklaart de concepten en de componenten die voor Beslissing in het algemeen en besluitvormingsbeheer in het bijzonder worden gebruikt. Toont de strategieën die voor het kiezen van de beste optie worden gebruikt om tijdens de ervaring van een klant voor te stellen.
* [[!DNL Profile Query Language (PQL)] ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=nl-NL){target="_blank"} : PQL is een krachtige taal om uitdrukkingen over instanties te schrijven XDM. PQL wordt gebruikt om beslissingsregels te definiëren.

## API-voorbeeldaanroepen lezen {#reading-sample-api-calls}

Deze gids verstrekt voorbeeld API vraag om aan te tonen hoe te om uw verzoeken te formatteren. Dit zijn paden, vereiste kopteksten en correct opgemaakte ladingen voor aanvragen. Voorbeeld-JSON die wordt geretourneerd in API-reacties, wordt ook verschaft. Voor informatie over de overeenkomsten die in documentatie voor steekproef API vraag worden gebruikt, zie de sectie op [ hoe te om voorbeeld API vraag ](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=nl-NL#how-do-i-format-an-api-request){target="_blank"} te lezen  in de [!DNL Experience Platform] het oplossen van problemengids.

## Waarden verzamelen voor vereiste koppen {#gather-values-for-required-headers}

Om vraag aan [!DNL Adobe Experience Platform] APIs te maken, moet u het [ authentificatieleerprogramma ](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=nl-NL){target="_blank"}  eerst voltooien. Als u de zelfstudie over verificatie voltooit, krijgt u de waarden voor elk van de vereiste headers in alle API-aanroepen van [!DNL Experience Platform] , zoals hieronder wordt getoond:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Alle verzoeken die een lading (POST, PUT, PATCH) bevatten vereisen een extra kopbal:

* `Content-Type: application/json`

## Volgende stappen {#next-steps}

Dit document bevatte de vereiste kennis die nodig was om aanroepen uit te voeren naar de [!DNL Offer Library] API. U kunt nu aan de steekproefvraag verdergaan die in deze ontwikkelaarsgids wordt verstrekt en samen met hun instructies volgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12) -->

