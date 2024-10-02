---
title: Op code gebaseerde ervaringen maken
description: Leer hoe u code-ervaringen kunt maken in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 503bedc30c35305537c62f9452f4a2dc07424523
workflow-type: tm+mt
source-wordcount: '1129'
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

   <!--![](assets/code-based-campaign-edit-content.png)-->

Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

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

1. Met code-gebaseerde ervaringen, kunt u de ervaring bepalende eigenschap gebruiken. Selecteer het pictogram **[!UICONTROL Decision policy]** op de linkerbalk en klik op **[!UICONTROL Add decision policy]** . [ Leer meer ](../experience-decisioning/create-decision.md) <!--UI labels TBC + TBC for journeys (visible in UI so probably confirmed) -->

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Experience Decisioning is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.


1. Klik op **[!UICONTROL Save and close]** om uw wijzigingen te bevestigen.

Zodra uw ontwikkelaar een API- of SDK-aanroep uitvoert om inhoud op te halen voor het oppervlak dat is gedefinieerd in uw kanaalconfiguratie, worden de wijzigingen toegepast op uw webpagina of app.

## De op code gebaseerde ervaring testen {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Een voorvertoning weergeven van uw op code gebaseerde ervaring"
>abstract="Krijg een simulatie van wat uw code-gebaseerde ervaring zal kijken als."

Volg de onderstaande stappen om een voorvertoning weer te geven van uw aangepaste ervaring op basis van code. De gedetailleerde informatie over hoe te om testprofielen te selecteren en uw inhoud voor te vertonen is beschikbaar in [ Voorproef en test uw inhoudspagina ](../content-management/preview-test.md).

>[!CAUTION]
>
>U moet testprofielen beschikbaar hebben om te simuleren welke aanbiedingen aan hen zullen worden geleverd. Leer hoe te om [ testprofielen ](../audience/creating-test-profiles.md) tot stand te brengen.

1. Selecteer **[!UICONTROL Simulate content]** tijdens de rit of campagne in de verpersoonlijkingseditor of in het inhoudsscherm.

   ![](assets/code-based-campaign-simulate.png)

1. Klik op **[!UICONTROL Manage test profiles]** om een of meer testprofielen te selecteren.

1. Er wordt een voorvertoning van uw aangepaste ervaring op basis van code weergegeven.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## Uw op code gebaseerde ervaring live maken {#code-based-experience-live}

>[!IMPORTANT]
>
>Vanaf de release van september kunt u met een nieuwe ervaring op het gebied van campagne en trajectactivering het hele goedkeuringsproces beheren. Zo kunt u ervoor zorgen dat campagnes en reizen grondig worden doorgelicht en goedgekeurd door de belanghebbenden voordat u live gaat. Deze functie is beschikbaar in Beperkte Beschikbaarheid. [Meer informatie](../test-approve/gs-approval.md)

Zodra u uw op code-gebaseerde ervaring bepaalde en uw inhoud zoals gewenst gebruikend de [ code-gebaseerde redacteur ](#edit-code) gebruikte, kunt u uw reis of campagne activeren om uw veranderingen zichtbaar aan uw publiek te maken.

U kunt ook een voorvertoning van uw code-gebaseerde ervaringsinhoud weergeven voordat u deze live maakt. [Meer informatie](#test-code-based-experience)

>[!NOTE]
>
>Als u een op code gebaseerde reis/campagne activeert die dezelfde pagina&#39;s beïnvloedt als een andere reis of campagne die al actief is, worden alle wijzigingen toegepast op uw inhoud.
>
>Als meerdere op code gebaseerde reizen of campagnes hetzelfde element of dezelfde elementen van uw inhoud bijwerken, heeft de hoogste prioriteit prioriteit voor de reis/campagne.

### Publish een op code gebaseerde reis {#publish-code-based-journey}

Volg de onderstaande stappen om uw op code gebaseerde ervaring live te maken van een reis.

1. Controleer of uw reis geldig is en of er geen fout optreedt. [Meer informatie](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. Selecteer tijdens de rit de optie **[!UICONTROL Publish]** in de rechterbovenkeuzelijst.

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >Leer meer bij het publiceren reizen in [ deze sectie ](../building-journeys/publishing-the-journey.md).

Uw op code-gebaseerde reis neemt de **[!UICONTROL Live]** status en is nu zichtbaar aan het geselecteerde publiek. Elke ontvanger van uw reis kan uw wijzigingen zien.

>[!NOTE]
>
>Nadat u op **[!UICONTROL Publish]** hebt geklikt, kan het maximaal 15 minuten duren voordat de wijzigingen live beschikbaar zijn.

### Een op code gebaseerde campagne activeren {#activate-code-based-campaign}

1. Selecteer **[!UICONTROL Review to activate]** in uw op code gebaseerde campagne.

   ![](assets/code-based-campaign-review.png)

1. Controleer en bewerk indien nodig de inhoud, eigenschappen, configuratie, publiek en planning.

1. Selecteer **[!UICONTROL Activate]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Leer meer bij het activeren van campagnes in [ deze sectie ](../campaigns/review-activate-campaign.md).

Uw op code gebaseerde campagne neemt de **[!UICONTROL Live]** status en is nu zichtbaar voor het geselecteerde publiek. Elke ontvanger van de campagne kan de wijzigingen zien die u aan uw inhoud hebt toegevoegd.

>[!NOTE]
>
>Nadat u op **[!UICONTROL Activate]** hebt geklikt, kan het 15 minuten duren voordat de wijzigingen live beschikbaar zijn.
>
>Als u een schema voor uw op code-gebaseerde campagne bepaalde, heeft het de **[!UICONTROL Scheduled]** status tot de begindatum en de tijd worden bereikt.

## Een op code gebaseerde reis of campagne stoppen {#stop-code-based-experience}

Wanneer een code-gebaseerde ervaring levend is, kunt u het tegenhouden om uw publiek te verhinderen uw wijzigingen te zien. Voer de onderstaande stappen uit.

1. Selecteer een live reis of campagne in de lijst.

1. Voer de relevante actie uit volgens uw geval:

   * Selecteer **[!UICONTROL Stop campaign]** in het bovenste menu van de campagne.

     ![](assets/code-based-campaign-stop.png)

   * Klik in het bovenste menu van de rit op de knop **[!UICONTROL More]** en selecteer **[!UICONTROL Stop]** .

     ![](assets/code-based-journey-stop.png)

1. De wijzigingen die u hebt toegevoegd, zijn niet meer zichtbaar voor het publiek dat u hebt gedefinieerd.

>[!NOTE]
>
>Nadat een op code gebaseerde reis of campagne is gestopt, kunt u deze niet meer bewerken of activeren. U kunt deze alleen dupliceren en de gedupliceerde reis/campagne activeren.

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

TBC video if existing

## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
