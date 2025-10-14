---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics-integratie
description: Meer informatie over hoe Adobe Analytics-gegevens in Journey Optimizer kunnen worden gebruikt
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analytics, integration, web sdk, platform
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 0be35e14dba32523a7f28aaaa28d41ee693d44ba
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 5%

---

# Werken met Adobe Analytics-gegevens {#analytics-data}

U kunt alle webgedragsgebeurtenisgegevens benutten die u al vastlegt via Adobe Analytics of Web SDK en die streaming naar Adobe Experience Platform, om reizen te starten en ervaringen voor uw klanten te automatiseren.

Dit werkt alleen met Adobe Analytics als u:

1. Activeer de rapportsuite die u wilt gebruiken. [Meer informatie](#leverage-analytics-data)
1. Schakel Journey Optimizer in om uw Adobe Analytics-gegevensbron te gebruiken. [Meer informatie](#activate-analytics-data)
1. Voeg een specifieke gebeurtenis toe aan uw reis. [Meer informatie](#event-analytic)

>[!NOTE]
>
>Deze sectie is slechts op regel-gebaseerde gebeurtenissen en klanten van toepassing die de gegevens van Adobe Analytics of van het Web SDK moeten gebruiken.
> 
>Als u Adobe Customer Journey Analytics gebruikt, verwijs naar [&#x200B; deze pagina &#x200B;](../reports/cja-ajo.md).
>

## Adobe Analytics- of Web SDK-gegevens configureren {#leverage-analytics-data}

Data coming from Adobe Analytics or Adobe Experience Platform Web SDK need to be enabled to be used in your journeys.

Hiervoor voert u de volgende stappen uit:

1. Browse to the **[!UICONTROL Sources]** menu.

1. In the Adobe Analytics section, select **[!UICONTROL Add data]**

   ![](assets/ajo-aa_1.png)

1. From the list of available Adobe Analytics report suites, select the **[!UICONTROL Report suite]** to enable. Klik vervolgens op **[!UICONTROL Next]** .

   ![](assets/ajo-aa_2.png)

1. Kies of u een standaardschema of een aangepast schema wilt gebruiken.

1. Kies een **[!UICONTROL Dataflow name]** in het scherm **[!UICONTROL Dataflow detail]** .

1. Klik op **[!UICONTROL Finish]** als de configuratie is voltooid.

   ![](assets/ajo-aa_3.png)

Dit laat de bron van Analytics schakelaar voor die rapportreeks toe. Telkens wanneer de gegevens binnenkomen, worden ze omgezet in een Experience-gebeurtenis en verzonden naar Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Learn more about Adobe Analytics source connector in  [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=nl-NL){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=nl-NL){target="_blank"}.

## Deze configuratie activeren {#activate-analytics-data}

Zodra deze configuratie is voltooid, neemt u contact op met Adobe om uw Journey Optimizer-omgeving in staat te stellen deze gegevensbron te gebruiken. Deze stap is alleen vereist voor Adobe Analytics-gegevensbronnen. Dit doet u als volgt:

1. Haal de gegevensbron-id op. Deze informatie is beschikbaar in het gebruikersinterface: doorblader aan de gegevensbron u van het **Dataflows** lusje van het **Bronnen** menu creeerde. De eenvoudigste manier om dit te vinden is door te filteren op Adobe Analytics-bronnen.
1. Neem contact op met de klantenservice van Adobe voor de volgende informatie:

   * Betreft: Adobe Analytics-evenementen mogelijk maken voor reizen

   * Inhoud: schakel mijn omgeving in om AA-gebeurtenissen te gebruiken.

      * Organisatie-id: &quot;XXX@AdobeOrg&quot;

      * Gegevensbron-id: &quot;ID: xxxxx&quot;

1. Als u eenmaal hebt bevestigd dat uw omgeving gereed is, kunt u Adobe Analytics-gegevens tijdens uw reis gebruiken.

## Create a journey with an event using Adobe Analytics or Web SDK data {#event-analytics}

You can now create an event based on Adobe Analytics or Adobe Experience Platform Web SDK data to be used in a journey.

In the example below, learn how to target users who added a product to their carts:

* If the order is completed, users receive a follow-up email two days later to ask for feedbacks.
* If the order is not completed, users receive an email to remind them to complete the order.

1. From Adobe Journey Optimizer, access the **[!UICONTROL Configuration]** menu.

1. Selecteer vervolgens **[!UICONTROL Manage]** op de **[!UICONTROL Events]** -kaart.

   ![](assets/ajo-aa_5.png)

1. Klik op **[!UICONTROL Create event]**. Het deelvenster voor gebeurtenisconfiguratie wordt aan de rechterkant van het scherm geopend.

1. Fill in the **[!UICONTROL Event]** parameters:

   * **[!UICONTROL Name]**: Personalize the name of your **[!UICONTROL Event]**.
   * **[!UICONTROL Type]**: Choose the **[!UICONTROL Unitary]** Type. [Meer informatie](../event/about-events.md)
   * **[!UICONTROL Event ID type]**: Kies het type **[!UICONTROL Rule based]** gebeurtenis-id. [Meer informatie](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: Selecteer Analytics of WebSDK die schema [&#x200B; vóór &#x200B;](#leverage-analytics-data) wordt gecreeerd.
   * **[!UICONTROL Fields]**: selecteer de velden Payload. [Meer informatie](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Event ID condition]**: Bepaal de voorwaarde om de gebeurtenissen te identificeren die uw reis zullen teweegbrengen.

     Here, the Event is triggered when customers add an item to their carts.
   * **[!UICONTROL Profile Identifier]**: Choose a field from your payload fields, or define a formula, to identify the person associated to the event.

   ![](assets/ajo-aa_6.png)

1. When configured, select **[!UICONTROL Save]**.

Now that the event is ready, create a journey to use it.

1. From the **[!UICONTROL Journeys]** menu, open or create a journey. Raadpleeg [deze sectie](../building-journeys/journey-gs.md) voor meer informatie.

1. Voeg uw eerder gevormde gebeurtenis van Analytics aan uw reis toe.

   ![](assets/ajo-aa_8.png)

1. Voeg een gebeurtenis toe die wordt geactiveerd als een bestelling wordt voltooid.

1. Selecteer in uw **[!UICONTROL Event menu]** de opties **[!UICONTROL Define the event timeout]** en **[!UICONTROL Set a timeout path]** .

   ![](assets/ajo-aa_9.png)

1. Voeg een handeling **[!UICONTROL Email]** toe vanaf het time-outpad. This path will be used to send an email to customers who didn&#39;t complete an order to remind them that their carts are still available.

1. Add a **[!UICONTROL Wait]** activity after your main path and set it to the needed duration.

   ![](assets/ajo-aa_10.png)

1. Voeg vervolgens een **[!UICONTROL Email action]** toe. In deze e-mail worden de klanten gevraagd feedback te geven over de geplaatste bestelling.

U kunt nu uw reis testen en publiceren. [Meer informatie](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
