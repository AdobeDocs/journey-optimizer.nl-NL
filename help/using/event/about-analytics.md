---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics-integratie
description: Meer informatie over hoe Adobe Analytics-gegevens in Journey Optimizer kunnen worden gebruikt
feature: Reporting, Integrations
topic: Administration
role: Admin
level: Intermediate
keywords: analyse, integratie, web sdk, platform
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 6%

---

# Werken met Adobe Analytics-gegevens {#analytics-data}

U kunt alle webgedragsgebeurtenisgegevens die u al vastlegt via Adobe Analytics of Web SDK, en streaming naar Adobe Experience Platform gebruiken om reizen te starten en ervaringen voor uw klanten te automatiseren.

Dit werkt alleen met Adobe Analytics als u:

1. Activeer de rapportsuite die u wilt gebruiken. [Meer informatie](#leverage-analytics-data)
1. Schakel Journey Optimizer in om uw Adobe Analytics-gegevensbron te gebruiken. [Meer informatie](#activate-analytics-data)
1. Voeg een specifieke gebeurtenis toe aan uw reis. [Meer informatie](#event-analytic)

>[!NOTE]
>
>Deze sectie is slechts op regel-gebaseerde gebeurtenissen en klanten van toepassing die Adobe Analytics of de gegevens van SDK van het Web moeten gebruiken.
> 
>Als u Adobe Customer Journey Analytics gebruikt, raadpleegt u [deze pagina](../reports/cja-ajo.md).
>

## Adobe Analytics- of Web SDK-gegevens configureren {#leverage-analytics-data}

Gegevens die afkomstig zijn van Adobe Analytics of Adobe Experience Platform Web SDK moeten kunnen worden gebruikt tijdens uw reizen.

Volg de onderstaande stappen om dit te doen:

1. Bladeren naar de **[!UICONTROL Sources]** -menu.

1. Selecteer in de sectie Adobe Analytics de optie **[!UICONTROL Add data]**

   ![](assets/ajo-aa_1.png)

1. Selecteer in de lijst met beschikbare Adobe Analytics-rapportsuite de **[!UICONTROL Report suite]** om in te schakelen. Klik vervolgens op **[!UICONTROL Next]**.

   ![](assets/ajo-aa_2.png)

1. Kies of u een standaardschema of een aangepast schema wilt gebruiken.

1. Van de **[!UICONTROL Dataflow detail]** scherm, kies een **[!UICONTROL Dataflow name]**.

1. Nadat de configuratie is voltooid, klikt u op **[!UICONTROL Finish]**.

   ![](assets/ajo-aa_3.png)

Dit laat de bron van Analytics schakelaar voor die rapportreeks toe. Telkens wanneer de gegevens binnenkomen, worden ze omgezet in een Experience-gebeurtenis en verzonden naar Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Meer informatie over de Adobe Analytics-bronconnector in  [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target="_blank"}.

## Deze configuratie activeren {#activate-analytics-data}

Zodra deze configuratie wordt gedaan, contacteer Adobe om uw milieu van Journey Optimizer toe te laten om deze gegevensbron te gebruiken. Deze stap is alleen vereist voor Adobe Analytics-gegevensbronnen. Dit doet u als volgt:

1. Haal de gegevensbron-id op. Deze informatie is beschikbaar in de gebruikersinterface: blader naar de gegevensbron u van het **Gegevensstromen** tabblad van het **Bronnen** -menu. De eenvoudigste manier om dit te vinden is door te filteren op Adobe Analytics-bronnen.
1. Neem contact op met de klantenservice van de Adobe met de volgende gegevens:

   * Betreft: Adobe Analytics-evenementen mogelijk maken voor reizen

   * Inhoud: schakel mijn omgeving in om AA-gebeurtenissen te gebruiken.

      * Organisatie-id: &quot;XXX@AdobeOrg&quot;

      * Gegevensbron-id: &quot;ID: xxxxx&quot;

1. Als u eenmaal hebt bevestigd dat uw omgeving gereed is, kunt u Adobe Analytics-gegevens tijdens uw reis gebruiken.

## Een reis maken met een gebeurtenis met Adobe Analytics of Web SDK-gegevens {#event-analytics}

U kunt nu een gebeurtenis maken op basis van Adobe Analytics- of Adobe Experience Platform Web SDK-gegevens die u tijdens een rit wilt gebruiken.

In het onderstaande voorbeeld leert u hoe u gebruikers die een product aan hun winkelwagentjes hebben toegevoegd, kunt aanspreken:

* Als de bestelling is voltooid, ontvangen gebruikers twee dagen later een vervolgbericht om feedback te vragen.
* Als de bestelling niet is voltooid, ontvangen gebruikers een e-mail om hen eraan te herinneren de bestelling te voltooien.

1. Vanuit Adobe Journey Optimizer opent u de **[!UICONTROL Configuration]** -menu.

1. Selecteer vervolgens **[!UICONTROL Manage]** van de **[!UICONTROL Events]** kaart.

   ![](assets/ajo-aa_5.png)

1. Klik op **[!UICONTROL Create event]**. Het deelvenster voor gebeurtenisconfiguratie wordt aan de rechterkant van het scherm geopend.

1. Vul de **[!UICONTROL Event]** parameters:

   * **[!UICONTROL Name]**: Pas de naam van uw **[!UICONTROL Event]**.
   * **[!UICONTROL Type]**: Kies de optie **[!UICONTROL Unitary]** Type. [Meer informatie](../event/about-events.md)
   * **[!UICONTROL Event ID type]**: Kies de optie **[!UICONTROL Rule based]** Type gebeurtenis-id. [Meer informatie](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: Selecteer het schema Analytics of WebSDK [gemaakt vóór](#leverage-analytics-data).
   * **[!UICONTROL Fields]**: Selecteer de velden Payload. [Meer informatie](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Event ID condition]**: Bepaal de voorwaarde om de gebeurtenissen te identificeren die uw reis zullen teweegbrengen.

     Hier wordt de gebeurtenis geactiveerd wanneer klanten een item aan hun winkelwagentjes toevoegen.
   * **[!UICONTROL Profile Identifier]**: Kies een veld in uw payload-velden of definieer een formule om de persoon te identificeren die aan de gebeurtenis is gekoppeld.

   ![](assets/ajo-aa_6.png)

1. Indien geconfigureerd, selecteert u **[!UICONTROL Save]**.

Nu de gebeurtenis klaar is, maak een reis om het te gebruiken.

1. Van de **[!UICONTROL Journeys]** openen of een reis maken. Raadpleeg [deze sectie](../building-journeys/journey-gs.md) voor meer informatie.

1. Voeg uw eerder gevormde gebeurtenis van Analytics aan uw reis toe.

   ![](assets/ajo-aa_8.png)

1. Voeg een gebeurtenis toe die wordt geactiveerd als een bestelling wordt voltooid.

1. Van uw **[!UICONTROL Event menu]**, selecteert u de **[!UICONTROL Define the event timeout]** en **[!UICONTROL Set a timeout path]** opties.

   ![](assets/ajo-aa_9.png)

1. Voeg vanaf het onderbrekingspad een **[!UICONTROL Email]** handeling. Dit pad wordt gebruikt om een e-mail te sturen naar klanten die geen bestelling hebben voltooid om hen eraan te herinneren dat hun winkelwagentjes nog steeds beschikbaar zijn.

1. Voeg een **[!UICONTROL Wait]** activiteit na uw belangrijkste weg en plaats het aan de gewenste duur.

   ![](assets/ajo-aa_10.png)

1. Voeg vervolgens een **[!UICONTROL Email action]**. In deze e-mail worden de klanten gevraagd feedback te geven over de geplaatste bestelling.

U kunt nu uw reis testen en publiceren. [Meer informatie](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
