---
title: Op code gebaseerde ervaringen maken
description: Leer hoe u code-ervaringen kunt maken in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 3f7d71eecf282b21eb09423378008c3b9ccd7edc
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 1%

---

# Op code gebaseerde ervaringen maken {#create-code-based}

Momenteel in [!DNL Journey Optimizer] u kunt alleen op code gebaseerde ervaringen maken in **campagnes**.

Specifieke instructies en aanbevelingen voor ervaringen op basis van code worden nader beschreven in [deze pagina](code-based-prerequisites.md).

## Een op code gebaseerde campagne maken {#create-code-based-campaign}

Volg de onderstaande stappen om uw op code gebaseerde ervaring op te bouwen via een campagne.

1. Maak een campagne. [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer de **[!UICONTROL Code-based experience]** handeling.

1. Voer het op code gebaseerde ervaringsoppervlak in. [Meer informatie](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >Zorg ervoor dat het oppervlak-URI dat in uw op code gebaseerde campagne wordt gebruikt, overeenkomt met het oppervlak dat in uw eigen implementatie wordt gebruikt. Anders worden de wijzigingen niet doorgevoerd.

1. Selecteer **[!UICONTROL Create]**.

1. Voltooi de stappen om een campagne te creëren, zoals de campagneeigenschappen, [publiek](../audience/about-audiences.md), en [schema](../campaigns/create-campaign.md#schedule). Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

1. Bewerk de inhoud naar wens met behulp van de verpersoonlijkingseditor. [Meer informatie](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## De code-inhoud bewerken {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="De personalisatie-editor gebruiken"
>abstract="Voeg de code die u wilt leveren in en bewerk deze als onderdeel van deze op code gebaseerde ervaringsactie."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html" text="Aan de slag met de personalisatie-editor"

1. Selecteer in het scherm Campagne **[!UICONTROL Edit code]**.

   ![](assets/code-based-campaign-edit-code.png)

1. De [personalisatie-editor](../personalization/personalization-build-expressions.md) wordt geopend. Het is een niet-visuele interface van de ervaringsverwezenlijking die u toestaat om uw code te ontwerpen.

1. U kunt de ontwerpmodus wijzigen van HTML in JSON en andersom.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >Als u de ontwerpmodus wijzigt, gaan al uw huidige code verloren. Zorg er dus voor dat u overschakelt naar een andere modus voordat u begint met ontwerpen.

1. Voer de gewenste code in. U kunt de [!DNL Journey Optimizer] verpersoonlijkingsredacteur met al zijn verpersoonlijking en auteursmogelijkheden. [Meer informatie](../personalization/personalization-build-expressions.md)

1. U kunt desgewenst HTML- of JSON-uitdrukkingsfragmenten toevoegen. [Meer informatie](../personalization/use-expression-fragments.md)

   U kunt ook een deel van de code-inhoud opslaan als een fragment. [Meer informatie](../content-management/fragments.md#save-as-expression-fragment)

1. In op code-gebaseerde campagnes, kunt u de ervaring bepalende eigenschap gebruiken. Selecteer de **[!UICONTROL Decisions]** pictogram van de linkerbalk en klik op **[!UICONTROL Create decision]**. [Meer informatie](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Experience Decisioning is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.


1. Klikken **[!UICONTROL Save and close]** om uw wijzigingen te bevestigen.

Zodra de ontwikkelaar een API- of SDK-aanroep uitvoert om inhoud op te halen voor het geselecteerde oppervlak, worden de wijzigingen toegepast op uw webpagina of app.

## Test de op code gebaseerde campagne {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Een voorvertoning weergeven van uw op code gebaseerde ervaring"
>abstract="Krijg een simulatie van wat uw code-gebaseerde ervaring zal kijken als."

Volg de onderstaande stappen om een voorvertoning weer te geven van uw aangepaste ervaring op basis van code. Gedetailleerde informatie over het selecteren van testprofielen en het weergeven van een voorvertoning van de inhoud is beschikbaar in het dialoogvenster [De inhoudspagina voorvertonen en testen](../content-management/preview-test.md).

>[!CAUTION]
>
>U moet testprofielen beschikbaar hebben om te simuleren welke aanbiedingen aan hen zullen worden geleverd. Leer hoe u [testprofielen maken](../audience/creating-test-profiles.md).

1. Van of de verpersoonlijkings redacteur of geef inhoudsscherm uit, uitgezocht **[!UICONTROL Simulate content]**.

   ![](assets/code-based-campaign-simulate.png)

1. Klikken **[!UICONTROL Manage test profiles]** om een of meer testprofielen te selecteren.

1. Er wordt een voorvertoning van uw aangepaste ervaring op basis van code weergegeven.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## De op code gebaseerde campagne activeren {#activate-code-based-campaign}

Nadat u de campagne op basis van code hebt gedefinieerd en de inhoud naar wens hebt bewerkt met de [op code gebaseerde editor](#edit-code), kunt u deze controleren en activeren. Voer de onderstaande stappen uit.

>[!NOTE]
>
>U kunt ook een voorvertoning van de inhoud van uw campagne weergeven voordat u deze activeert. [Meer informatie](#test-code-based-campaign)

1. Selecteer in uw op code gebaseerde campagne de optie **[!UICONTROL Review to activate]**.

   ![](assets/code-based-campaign-review.png)

1. Controleer en bewerk indien nodig de inhoud, eigenschappen, oppervlak, publiek en planning.

1. Selecteer **[!UICONTROL Activate]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Nadat u op **[!UICONTROL Activate]** Het kan tot 1 minuut duren voordat wijzigingen in op code gebaseerde campagnes live beschikbaar zijn op uw locatie.

Uw op code gebaseerde campagne neemt de **[!UICONTROL Live]** en is nu zichtbaar voor het geselecteerde publiek. Elke ontvanger van uw campagne kan uw wijzigingen zien.

>[!NOTE]
>
>Als u een programma voor uw op code-gebaseerde campagne hebt bepaald, heeft het **[!UICONTROL Scheduled]** status tot de begindatum en -tijd zijn bereikt.
>
>Als u een op code gebaseerde campagne activeert die invloed heeft op dezelfde locaties als een andere campagne die al actief is, worden alle wijzigingen toegepast op uw locaties.

Meer informatie over het activeren van campagnes in [deze sectie](../campaigns/review-activate-campaign.md).

## Een op code gebaseerde campagne stoppen {#stop-code-based-campaign}

Wanneer een code-gebaseerde campagne levend is, kunt u het tegenhouden om uw publiek te verhinderen uw wijzigingen te zien. Voer de onderstaande stappen uit.

1. Selecteer een live campagne in de lijst.

1. Selecteer in het bovenste menu de optie **[!UICONTROL Stop campaign]**.

   ![](assets/code-based-campaign-stop.png)

1. De wijzigingen die u hebt toegevoegd, zijn niet meer zichtbaar voor het publiek dat u hebt gedefinieerd.

>[!NOTE]
>
>Nadat een op code gebaseerde campagne is gestopt, kunt u deze niet meer bewerken of activeren. U kunt de gedupliceerde campagne alleen dupliceren en activeren.

## Op code gebaseerde campagnerapporten

U kunt tot code-gebaseerde campagnerapporten van het scherm van de campagnesamenvatting toegang hebben.

Globale rapporten geven gebeurtenissen weer die zich minstens twee uur geleden hebben voorgedaan en bestrijken gebeurtenissen gedurende een geselecteerde tijdsperiode. In vergelijking hiermee richten Live-rapporten zich op gebeurtenissen die zich in de afgelopen 24 uur hebben voorgedaan, met een minimale tijdsinterval van twee minuten vanaf het plaatsvinden van de gebeurtenis.

### Live-rapport op basis van code {#live-report-code-based}

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL Code-based experience]** bevat de belangrijkste gegevens voor uw apps of webpagina&#39;s. [Meer informatie over live rapporten](../reports/campaign-live-report.md)

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het op code-gebaseerde ervaringsrapport.

De **[!UICONTROL Code-based experience performance]** KPIs detailleert de belangrijkste informatie met betrekking tot de betrokkenheid van uw bezoekers met uw code-gebaseerde ervaringen, zoals:

* **[!UICONTROL Impressions]**: totaal aantal ervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw app/pagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

De **[!UICONTROL Code-based experience summary]** in de grafiek wordt de evolutie van uw ervaringen (indrukken, unieke indrukken en interacties) gedurende de laatste 24 uur getoond.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Globaal rapport op basis van code {#global-report-code-based}

Globaal rapport voor campagnes op basis van code is rechtstreeks toegankelijk vanuit uw campagne via de **[!UICONTROL View report]** knop. [Meer informatie over een globaal rapport](../reports/campaign-global-report.md)

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Code-based experience]** bevat de belangrijkste gegevens voor uw apps of webpagina&#39;s.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het op code-gebaseerde ervaringsrapport.

De **[!UICONTROL Code-based experience performance]** KPI&#39;s geven een gedetailleerde beschrijving van de belangrijkste informatie over de betrokkenheid van uw bezoekers bij uw ervaringen, zoals:

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie de ervaring is opgeleverd.

* **[!UICONTROL Impressions]**: totaal aantal ervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: percentage contracten met uw app/pagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

De **[!UICONTROL Code-based experience summary]** in de grafiek wordt de ontwikkeling van uw ervaringen (unieke indrukken, indrukken en interacties) voor de desbetreffende periode weergegeven.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
