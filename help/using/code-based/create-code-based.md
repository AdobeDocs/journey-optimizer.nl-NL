---
title: Op code gebaseerde ervaringen maken
description: Leer hoe u code-ervaringen kunt maken in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 1%

---

# Op code gebaseerde ervaringen maken {#create-code-based}

Momenteel in [!DNL Journey Optimizer] kunt u code-gebaseerde ervaringen in **campagnes** slechts tot stand brengen.

De specifieke begeleiding en de aanbevelingen voor code-gebaseerde ervaringen zijn gedetailleerd in [ deze pagina ](code-based-prerequisites.md).

## Een op code gebaseerde campagne maken {#create-code-based-campaign}

Volg de onderstaande stappen om uw op code gebaseerde ervaring op te bouwen via een campagne.

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** . [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketingberichten of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Voltooi de stappen om een campagne, zoals de campagneeigenschappen, [ publiek ](../audience/about-audiences.md), en [ programma ](../campaigns/create-campaign.md#schedule) tot stand te brengen. Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

1. Selecteer de handeling **[!UICONTROL Code-based experience]** .

1. Selecteer of creeer de op code-gebaseerde ervaringsconfiguratie. [Meer informatie](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. Bewerk de inhoud naar wens met behulp van de verpersoonlijkingseditor. [Meer informatie](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## De code-inhoud bewerken {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="De personalisatie-editor gebruiken"
>abstract="Voeg de code die u wilt leveren in en bewerk deze als onderdeel van deze op code gebaseerde ervaringsactie."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html" text="Aan de slag met de personalisatie-editor"

1. Selecteer **[!UICONTROL Edit code]** in het scherm van de campagneeditie.

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

1. In op code-gebaseerde campagnes, kunt u de ervaring bepalende eigenschap gebruiken. Selecteer het pictogram **[!UICONTROL Decisions]** op de linkerbalk en klik op **[!UICONTROL Create decision]** . [Meer informatie](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Experience Decisioning is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.


1. Klik op **[!UICONTROL Save and close]** om uw wijzigingen te bevestigen.

Zodra uw ontwikkelaar een API- of SDK-aanroep uitvoert om inhoud op te halen voor het oppervlak dat is gedefinieerd in uw kanaalconfiguratie, worden de wijzigingen toegepast op uw webpagina of app.

## Test de op code gebaseerde campagne {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Een voorvertoning weergeven van uw op code gebaseerde ervaring"
>abstract="Krijg een simulatie van wat uw code-gebaseerde ervaring zal kijken als."

Volg de onderstaande stappen om een voorvertoning weer te geven van uw aangepaste ervaring op basis van code. De gedetailleerde informatie over hoe te om testprofielen te selecteren en uw inhoud voor te vertonen is beschikbaar in [ Voorproef en test uw inhoudspagina ](../content-management/preview-test.md).

>[!CAUTION]
>
>U moet testprofielen beschikbaar hebben om te simuleren welke aanbiedingen aan hen zullen worden geleverd. Leer hoe te om [ testprofielen ](../audience/creating-test-profiles.md) tot stand te brengen.

1. Selecteer **[!UICONTROL Simulate content]** in de verpersoonlijkingseditor of in het inhoudsscherm.

   ![](assets/code-based-campaign-simulate.png)

1. Klik op **[!UICONTROL Manage test profiles]** om een of meer testprofielen te selecteren.

1. Er wordt een voorvertoning van uw aangepaste ervaring op basis van code weergegeven.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## De op code gebaseerde campagne activeren {#activate-code-based-campaign}

>[!IMPORTANT]
>
>Vanaf de release van september kunt u met een nieuwe ervaring op het gebied van campagne en trajectactivering het hele goedkeuringsproces beheren. Zo kunt u ervoor zorgen dat campagnes en reizen grondig worden doorgelicht en goedgekeurd door de belanghebbenden voordat u live gaat. Deze functie is beschikbaar in Beperkte Beschikbaarheid. [Meer informatie](../test-approve/gs-approval.md)

Zodra u uw op code-gebaseerde campagne bepaalde en uw inhoud zoals gewenst gebruikend de [ code-gebaseerde redacteur ](#edit-code), kunt u het herzien en activeren. Voer de onderstaande stappen uit.

>[!NOTE]
>
>U kunt ook een voorvertoning van de inhoud van uw campagne weergeven voordat u deze activeert. [Meer informatie](#test-code-based-campaign)

1. Selecteer **[!UICONTROL Review to activate]** in uw op code gebaseerde campagne.

   ![](assets/code-based-campaign-review.png)

1. Controleer en bewerk indien nodig de inhoud, eigenschappen, configuratie, publiek en planning.

1. Selecteer **[!UICONTROL Activate]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Nadat u op **[!UICONTROL Activate]** hebt geklikt, kan het maximaal 1 minuut duren voordat wijzigingen in op code gebaseerde campagnes live beschikbaar zijn op uw locatie.

Uw op code gebaseerde campagne neemt de **[!UICONTROL Live]** status en is nu zichtbaar voor het geselecteerde publiek. Elke ontvanger van uw campagne kan uw wijzigingen zien.

>[!NOTE]
>
>Als u een schema voor uw op code-gebaseerde campagne bepaalde, heeft het de **[!UICONTROL Scheduled]** status tot de begindatum en de tijd worden bereikt.
>
>Als u een op code gebaseerde campagne activeert die invloed heeft op dezelfde locaties als een andere campagne die al actief is, worden alle wijzigingen toegepast op uw locaties.

Leer meer bij het activeren van campagnes in [ deze sectie ](../campaigns/review-activate-campaign.md).

## Een op code gebaseerde campagne stoppen {#stop-code-based-campaign}

Wanneer een code-gebaseerde campagne levend is, kunt u het tegenhouden om uw publiek te verhinderen uw wijzigingen te zien. Voer de onderstaande stappen uit.

1. Selecteer een live campagne in de lijst.

1. Selecteer **[!UICONTROL Stop campaign]** in het bovenste menu.

   ![](assets/code-based-campaign-stop.png)

1. De wijzigingen die u hebt toegevoegd, zijn niet meer zichtbaar voor het publiek dat u hebt gedefinieerd.

>[!NOTE]
>
>Nadat een op code gebaseerde campagne is gestopt, kunt u deze niet meer bewerken of activeren. U kunt de gedupliceerde campagne alleen dupliceren en activeren.

## Op code gebaseerde campagnerapporten

U kunt tot code-gebaseerde campagnerapporten van het scherm van de campagnesamenvatting toegang hebben.

Globale rapporten geven gebeurtenissen weer die zich minstens twee uur geleden hebben voorgedaan en bestrijken gebeurtenissen gedurende een geselecteerde tijdsperiode. In vergelijking hiermee richten Live-rapporten zich op gebeurtenissen die zich in de afgelopen 24 uur hebben voorgedaan, met een minimale tijdsinterval van twee minuten vanaf het plaatsvinden van de gebeurtenis.

### Live-rapport op basis van code {#live-report-code-based}

Vanuit uw campagne **[!UICONTROL Live report]** geeft het tabblad **[!UICONTROL Code-based experience]** de belangrijkste informatie met betrekking tot uw apps of webpagina&#39;s weer. [ Leer meer op levend rapport ](../reports/campaign-live-report.md)

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het op code-gebaseerde ervaringsrapport.

De KPI&#39;s van **[!UICONTROL Code-based experience performance]** bevatten gedetailleerde informatie over de betrokkenheid van uw bezoekers bij uw op code gebaseerde ervaringen, zoals:

* **[!UICONTROL Impressions]**: totaal aantal ervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw app/pagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

In de grafiek van **[!UICONTROL Code-based experience summary]** ziet u de evolutie van uw ervaringen (indrukken, unieke indrukken en interacties) gedurende de laatste 24 uur.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Globaal rapport op basis van code {#global-report-code-based}

Globaal rapport voor campagnes op basis van code is rechtstreeks vanuit uw campagne toegankelijk via de knop **[!UICONTROL View report]** . [ leer meer over globaal rapport ](../reports/campaign-global-report.md)

Vanuit uw campagne **[!UICONTROL Global report]** bevat het tabblad **[!UICONTROL Code-based experience]** de belangrijkste informatie met betrekking tot uw apps of webpagina&#39;s.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het op code-gebaseerde ervaringsrapport.

De KPI&#39;s van **[!UICONTROL Code-based experience performance]** bevatten gedetailleerde informatie over de belangrijkste informatie met betrekking tot de betrokkenheid van uw bezoekers bij uw ervaringen, zoals:

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie de ervaring is opgeleverd.

* **[!UICONTROL Impressions]**: totaal aantal ervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: percentage van de contracten met uw app/pagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

De grafiek van **[!UICONTROL Code-based experience summary]** toont de evolutie van uw ervaringen (unieke beelden, indrukkingen en interacties) voor de betrokken periode.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
