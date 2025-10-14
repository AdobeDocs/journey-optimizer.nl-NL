---
title: Ervaringen op basis van code testen
description: Leer hoe u op code gebaseerde ervaringen in Journey Optimizer kunt testen
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 9a1c148c-a6c3-406b-8f2e-1cf8b8239e75
source-git-commit: effc706cfa56eca21cde0f26fe7b6332d3728b74
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Ervaringen op basis van code testen {#test-code-based}

## Een voorvertoning weergeven van uw op code gebaseerde ervaring {#preview-code-based}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Een voorvertoning weergeven van uw op code gebaseerde ervaring"
>abstract="Krijg een simulatie van wat uw code-gebaseerde ervaring zal kijken als."

Volg de onderstaande stappen om een voorvertoning weer te geven van uw aangepaste ervaring op basis van code.

>[!CAUTION]
>
>U moet testprofielen beschikbaar hebben om te simuleren welke aanbiedingen aan hen zullen worden geleverd. Leer hoe te om [&#x200B; testprofielen &#x200B;](../audience/creating-test-profiles.md) tot stand te brengen.

1. Selecteer **[!UICONTROL Simulate content]** tijdens de rit of campagne in de verpersoonlijkingseditor of in het inhoudsscherm.

   ![](assets/code-based-campaign-simulate.png)

1. Klik op **[!UICONTROL Manage test profiles]** om een of meer testprofielen te selecteren.

1. Er wordt een voorvertoning van uw aangepaste ervaring op basis van code weergegeven.

De gedetailleerde informatie over hoe te om testprofielen te selecteren en uw inhoud voor te vertonen is beschikbaar in [&#x200B; deze sectie &#x200B;](../content-management/preview.md).

>[!NOTE]
>
>Momenteel kunt u geen inhoud van het gebruikersinterface in een code-gebaseerde ervaringscampagne of reis simuleren gebruikend [&#x200B; Beslissing &#x200B;](../experience-decisioning/gs-experience-decisioning.md). Een alternerende actie is beschikbaar in [&#x200B; deze sectie &#x200B;](../experience-decisioning/create-decision.md#test-and-publish).


## Voorvertonen op apparaat {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="Een voorvertoning van uw op code gebaseerde ervaring weergeven op een echt apparaat"
>abstract="Bekijk een voorvertoning van uw persoonlijke ervaringen direct in uw browser of op uw mobiele apparaten om te zien hoe ze er op echte apparaten uitzien."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="Een voorvertoning weergeven van uw op code gebaseerde webbeleving op een apparaat"
>abstract="Scan de QR-code of kopieer de koppeling naar de voorvertoning op het apparaat."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="Een voorvertoning weergeven van uw op code gebaseerde mobiele beleving op het apparaat"
>abstract="Scan de QR-code of kopieer de koppeling naar de voorvertoning op het apparaat. Zodra verbonden, ga de speld op het apparaat in. Mogelijk moet u de app opnieuw starten om elke keer dat u de voorbeeldkoppelingen bijwerkt, de wijzigingen te zien."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="De voorvertoningskoppeling vernieuwen om de huidige weergave te weerspiegelen"
>abstract="In de voorvertoning op het apparaat wordt de inhoud weergegeven vanaf het moment dat u de voorvertoningskoppeling hebt gemaakt of vernieuwd. Als u de inhoud hebt gewijzigd of een ander testprofiel of een andere behandeling hebt geselecteerd, vernieuwt u de voorvertoning zodat deze de huidige weergave weerspiegelt."

Wanneer u code-gebaseerde ervaringen voor Web-pagina&#39;s of mobiele apps bouwt, kunt u uw gepersonaliseerde ervaringen op uw browser of op uw mobiele apparaten vooraf bekijken, om te zien hoe deze ervaringen op echte apparaten kijken.

>[!WARNING]
>
>De voorproef op apparaat is niet beschikbaar wanneer het gebruiken van [&#x200B; besluitvormingsbeleid &#x200B;](../experience-decisioning/create-decision.md) of [&#x200B; verpersoonlijking &#x200B;](../personalization/personalization-build-expressions.md) contextafhankelijke attributen.

1. Klik in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL Open preview options]** . De voorproefopties hangen van het platform af dat in uw [&#x200B; wordt geselecteerd code-gebaseerde configuratie &#x200B;](code-based-configuration.md#create-code-based-configuration).

1. Als u het platform van het a [&#x200B; Web &#x200B;](code-based-configuration.md#web) in uw op code-gebaseerde configuratie gebruikt, is het **[!UICONTROL Device preview URL]** read-only gebied vooraf gevuld met URL ingegaan voor de huidige kanaalconfiguratie.

   ![](assets/preview-on-device-web.png)

   U kunt:

   * Selecteer de knop **[!UICONTROL Copy link]** en plak de koppeling in een browsertabblad. U kunt de koppeling ook delen met uw team en belanghebbenden, die de nieuwe ervaring in elke browser kunnen bekijken voordat de wijzigingen live gaan.

   * Klik op **[!UICONTROL Open in new tab]** om de koppeling in uw huidige browser te openen.

   * Scan de QR-code met uw mobiele apparaat om de voorbeeldkoppeling op een mobiele browser te openen.

1. Als u [&#x200B; Mobiele platforms &#x200B;](code-based-configuration.md#mobile) (iOS/Android) in uw op code-gebaseerde configuratie gebruikt, wordt het **[!UICONTROL Deeplink]** read-only gebied vooraf gevuld met de **[!UICONTROL Preview URL]** waarde ingegaan in de kanaalconfiguratie voor het geselecteerde platform.

   Schakel tussen de tabbladen **[!UICONTROL iOS]** en **[!DNL Android]** om een voorvertoning van uw ervaring weer te geven voor het platform van uw keuze.

   ![](assets/preview-on-device-mobile.png)

   U kunt:

   * Selecteer de knop **[!UICONTROL Copy link]** en deel de koppeling met uw team en de betrokkenen, die een voorvertoning van de nieuwe ervaring in een mobiele browser kunnen bekijken voordat de wijzigingen live gaan.

   * Scan de QR-code met uw mobiele apparaat om de voorbeeldkoppeling rechtstreeks in de mobiele toepassing te openen. U moet de SPELD op uw apparaat ingaan om de [&#x200B; Assurance &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}  zitting te vestigen.

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance** is een product van Adobe Experience Cloud om u te helpen inspecteren, beproeven, simuleren, en bevestigen hoe u gegevens verzamelt of ervaringen in uw mobiele app dient. [&#x200B; leer meer &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/assurance/home){target="_blank"} 

1. Als u om het even welk [&#x200B; andere platform &#x200B;](code-based-configuration.md#other) in uw op code-gebaseerde configuratie gebruikt, kies het [&#x200B; oppervlakte URI &#x200B;](code-based-surface.md#surface-uri) dat u van de drop-down lijst wilt voorproef.

   ![](assets/preview-on-device-other.png)

   * Selecteer de knop **[!UICONTROL Copy link]** om de koppeling in een browsertabblad te plakken of de koppeling te delen met uw team en belanghebbenden.

   * Als u meerdere URI&#39;s hebt toegevoegd aan uw configuratie (maximaal 10), kunt u een van deze URI&#39;s selecteren voor een voorvertoning.

1. De verbindingen van de voorproef worden geproduceerd voor het geselecteerde testprofiel en, als u [&#x200B; Experiment van de Inhoud &#x200B;](../content-management/content-experiment.md) in uw reis of campagne, voor de geselecteerde behandeling gebruikt.

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   Wanneer u de inhoud bijwerkt of een ander testprofiel of andere behandeling selecteert, wordt de voorbeeldkoppeling automatisch vernieuwd. U kunt de koppeling naar verschillende tabbladen voor browsers kopiëren en de ervaringen vergelijken.
