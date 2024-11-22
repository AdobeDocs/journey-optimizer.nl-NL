---
title: Op code gebaseerde ervaringen maken
description: Leer hoe u code-ervaringen kunt maken in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 2%

---

# Op code gebaseerde ervaringen maken {#create-code-based}

In [!DNL Journey Optimizer] kunt u code-gebaseerde ervaringen in een reis of een campagne tot stand brengen.

De specifieke begeleiding en de aanbevelingen voor code-gebaseerde ervaringen zijn gedetailleerd in [ deze pagina ](code-based-prerequisites.md).

## Voeg een op code-gebaseerde ervaring door een reis of een campagne toe {#create-code-based-experience}

Volg de onderstaande stappen om uw op code gebaseerde ervaring op te bouwen via een reis of een campagne.

>[!BEGINTABS]

>[!TAB  voeg een op code-gebaseerde ervaring aan een reis ] toe

Om a **code-gebaseerde ervaring** activiteit aan een reis toe te voegen, volg deze stappen:

1. [ creeer een reis ](../building-journeys/journey-gs.md).

1. Begin uw reis met een [ Gebeurtenis ](../building-journeys/general-events.md) of a [ gelezen activiteit van het publiek ](../building-journeys/read-audience.md).

1. Sleep een **[!UICONTROL Code-based experience]** -activiteit vanuit de **[!UICONTROL Actions]** -sectie van het palet.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >Aangezien **op code-gebaseerde ervaring** een binnenkomende berichtactiviteit is, komt het met een 3 dagen **wachten** activiteit. [Meer informatie](../building-journeys/wait-activity.md#auto-wait-node)

1. Voer een **[!UICONTROL Label]** en **[!UICONTROL Description]** in voor uw bericht.

1. Selecteer of creeer de [ op code-gebaseerde ervaringsconfiguratie ](code-based-configuration.md) aan gebruik.

   ![](assets/code-based-activity-config.png)

1. Selecteer de knop **[!UICONTROL Edit content]** en bewerk de inhoud naar wens met de verpersoonlijkingseditor. [Meer informatie](#edit-code)

   U kunt ook een bestaande inhoudssjabloon gebruiken als basis voor uw code-inhoud. Merk op dat de malplaatjes beschikbaar om te kiezen zijn werkingsgebied aan of HTML of JSON gebaseerd op de kanaalconfiguratie die vooraf is gekozen. [ leer hoe te om inhoudsmalplaatjes ](../content-management/use-content-templates.md) te gebruiken

1. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

1. Zodra uw code-basis ervaring klaar is, voltooi de configuratie en publiceer uw reis om het te activeren. [Meer informatie](../building-journeys/publishing-the-journey.md)

Voor meer informatie over hoe te om een reis te vormen, verwijs naar [ deze pagina ](../building-journeys/journey-gs.md).

>[!TAB  creeer een op code-gebaseerde ervaringscampagne ]

Begin bouwend uw **code-gebaseerde ervaring** door een campagne, volg hieronder de stappen.

1. Maak een campagne. [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer het type campagne dat u wilt uitvoeren

   * **[!UICONTROL Scheduled - Marketing]** : voer de campagne onmiddellijk uit of op een opgegeven datum. De geplande campagnes zijn gericht op het verzenden van **marketing** berichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **[!UICONTROL API-triggered - Marketing/Transactional]** : voer de campagne uit met behulp van een API-aanroep. API-teweeggebrachte campagnes zijn gericht op het verzenden van of **marketing**, of **transactie** berichten, d.w.z. berichten die na een actie worden verzonden die door een individu wordt uitgevoerd: het terugstellen van het wachtwoord, het kartelaankoop enz. [ Leer hoe te om een campagne teweeg te brengen gebruikend APIs ](../campaigns/api-triggered-campaigns.md)

1. Voltooi de stappen om een campagne, zoals de campagneeigenschappen, [ publiek ](../audience/about-audiences.md), en [ programma ](../campaigns/create-campaign.md#schedule) tot stand te brengen. Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

1. Selecteer de handeling **[!UICONTROL Code-based experience]** .

1. Selecteer of creeer de op code-gebaseerde ervaringsconfiguratie. [Meer informatie](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. Bewerk de inhoud naar wens met behulp van de verpersoonlijkingseditor. [Meer informatie](#edit-code)

   U kunt ook een bestaande inhoudssjabloon gebruiken als basis voor uw code-inhoud. Merk op dat de malplaatjes beschikbaar om te kiezen zijn werkingsgebied aan of HTML of JSON gebaseerd op de kanaalconfiguratie die vooraf is gekozen. [ leer hoe te om inhoudsmalplaatjes ](../content-management/use-content-templates.md) te gebruiken

   <!--![](assets/code-based-campaign-edit-content.png)-->

Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

➡️ [ leren hoe te om een code-gebaseerde ervaringscampagne in deze video ](#video) tot stand te brengen

>[!ENDTABS]

## De code-inhoud bewerken {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="De personalisatie-editor gebruiken"
>abstract="Voeg de code die u wilt leveren in en bewerk deze als onderdeel van deze op code gebaseerde ervaringsactie."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html" text="Aan de slag met de personalisatie-editor"

1. Selecteer **[!UICONTROL Edit code]** in het scherm van de reisactiviteit of de campagneeditie.

   ![](assets/code-based-campaign-edit-code.png)

1. De [ verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) opent. Het is een niet-visuele interface van de ervaringsverwezenlijking die u toestaat om uw code te ontwerpen.

1. U kunt de ontwerpmodus wijzigen van HTML in JSON en andersom.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >Als u de ontwerpmodus wijzigt, gaan al uw huidige code verloren. Zorg er dus voor dat u overschakelt naar een andere modus voordat u begint met ontwerpen.

1. Voer de gewenste code in. U kunt de personalisatie-editor van [!DNL Journey Optimizer] gebruiken met al zijn personalisatie- en ontwerpmogelijkheden. [Meer informatie](../personalization/personalization-build-expressions.md)

1. U kunt desgewenst HTML- of JSON-uitdrukkingsfragmenten toevoegen. [ leer hoe ](../personalization/use-expression-fragments.md)

   U kunt ook een deel van de code-inhoud opslaan als een fragment. [ leer hoe ](../content-management/fragments.md#save-as-expression-fragment)

1. Met code-gebaseerde ervaringen, kunt u de eigenschap van het Beslissen gebruiken. Selecteer het pictogram **[!UICONTROL Decision policy]** op de linkerbalk en klik op **[!UICONTROL Add decision policy]** . [Meer informatie](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

1. Klik op **[!UICONTROL Save and close]** om uw wijzigingen te bevestigen.

Zodra uw ontwikkelaar een API- of SDK-aanroep uitvoert om inhoud op te halen voor het oppervlak dat is gedefinieerd in uw kanaalconfiguratie, worden de wijzigingen toegepast op uw webpagina of app.

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u een op code gebaseerde ervaringscampagne kunt maken, de eigenschappen ervan kunt configureren, testen en publiceren.

>[!VIDEO](https://video.tv.adobe.com/v/3428868/?quality=12&learn=on)
