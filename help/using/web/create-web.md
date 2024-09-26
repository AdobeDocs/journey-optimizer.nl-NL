---
title: Webervaringen maken
description: Leer hoe u een webpagina ontwerpt en de inhoud ervan bewerkt in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Webervaringen maken {#create-web}

Met [!DNL Journey Optimizer] kunt u de webervaring die u aan uw klanten levert, aanpassen via binnenkomende webcampagnes.

>[!CAUTION]
>
>Momenteel in [!DNL Journey Optimizer] kunt u Webervaringen slechts creëren gebruikend **campagnes**.

[Leer hoe u een webcampagne kunt maken in deze video](#video)

## Een webcampagne maken {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Een webconfiguratie definiëren"
>abstract="Een webconfiguratie kan overeenkomen met één pagina-URL of meerdere pagina&#39;s, zodat u inhoudwijzigingen kunt doorvoeren op een of meerdere webpagina&#39;s."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Een overeenkomende regel voor pagina&#39;s maken"
>abstract="Met een regel voor pagina&#39;s die overeenkomen met een regel, kunt u bijvoorbeeld meerdere URL&#39;s met dezelfde regel als doel instellen. Dit is bijvoorbeeld het geval als u de wijzigingen wilt toepassen op een hoofdbanner op een hele website of een bovenste afbeelding wilt toevoegen die op alle productpagina&#39;s van een website wordt weergegeven."

Volg onderstaande stappen om uw webervaring op te bouwen via een campagne.

>[!NOTE]
>
>Als dit uw eerste keer is creërend een Webervaring, zorg ervoor u de eerste vereisten volgt die in [ worden beschreven deze sectie ](web-prerequisites.md).

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .[Meer informatie](../campaigns/create-campaign.md)


1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketingberichten of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Voltooi de stappen om een Webcampagne, zoals de campagneeigenschappen, [ publiek ](../audience/about-audiences.md), en [ programma ](../campaigns/create-campaign.md#schedule) tot stand te brengen.

1. Selecteer de handeling **[!UICONTROL Web]** .

1. Selecteer of creeer een nieuwe configuratie. [ leer meer op Webconfiguratie ](web-configuration.md)

   ![](assets/web-campaign-steps.png)

Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [ deze pagina ](../campaigns/get-started-with-campaigns.md).

## De webcampagne testen {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Een voorvertoning van uw webbeleving bekijken"
>abstract="Bekijk een simulatie van hoe uw webervaring eruit zal zien."

Zodra u [ uw Webervaring ](edit-web-content.md) gebruikend de Webontwerper creeerde, kunt u testprofielen gebruiken om uw gewijzigde Web-pagina&#39;s voor te vertonen. Als u persoonlijke inhoud hebt ingevoegd, kunt u met behulp van de gegevens van het testprofiel controleren hoe deze inhoud wordt weergegeven.

Klik hiertoe op **[!UICONTROL Simulate content]** in het scherm Inhoud voor webcampagne bewerken of in de webontwerper en voeg vervolgens een testprofiel toe om uw webpagina te controleren aan de hand van de gegevens van het testprofiel.

![](assets/web-designer-preview.png)

U kunt de URL ook in de standaardbrowser openen of de test-URL kopiëren en in een browser plakken. Op deze manier kunt u de koppeling delen met uw team en belanghebbenden die de nieuwe webervaring in een browser kunnen bekijken voordat de campagne live gaat.

>[!NOTE]
>
>Wanneer u de test-URL kopieert, wordt de inhoud weergegeven die is gepersonaliseerd voor het testprofiel dat wordt gebruikt toen de inhoudsimulatie werd gegenereerd in [!DNL Journey Optimizer] .

De gedetailleerde informatie over hoe te om testprofielen en voorproef uw inhoud te selecteren is beschikbaar in de [ sectie van het Beheer van de Inhoud ](../content-management/preview-test.md).

## De webcampagne activeren {#activate-web-campaign}

>[!IMPORTANT]
>
>Vanaf de release van september kunt u met een nieuwe ervaring op het gebied van campagne en trajectactivering het hele goedkeuringsproces beheren. Zo kunt u ervoor zorgen dat campagnes en reizen grondig worden doorgelicht en goedgekeurd door de belanghebbenden voordat u live gaat. Deze functie is beschikbaar in Beperkte Beschikbaarheid. [Meer informatie](../test-approve/gs-approval.md)

Zodra u uw [ montages van de Webcampagne ](#configure-web-campaign) bepaalde en u uw inhoud zoals gewenst het gebruiken van [ Webontwerper ](edit-web-content.md#work-with-web-designer), kunt u uw Webcampagne herzien en activeren. Voer de onderstaande stappen uit.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Selecteer **[!UICONTROL Review to activate]** in uw webcampagne.

1. Controleer en bewerk indien nodig de inhoud, eigenschappen, configuratie, publiek en planning.

1. Selecteer **[!UICONTROL Activate]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Nadat u op **[!UICONTROL Activate]** hebt geklikt, kan het maximaal 15 minuten duren voordat wijzigingen in webcampagnes live op uw website beschikbaar zijn.

Uw webcampagne heeft de status **[!UICONTROL Live]** en is nu zichtbaar voor het geselecteerde publiek. Elke ontvanger van de campagne kan de wijzigingen zien die u met de webontwerper van [!DNL Journey Optimizer] aan uw website hebt toegevoegd.

>[!NOTE]
>
>Als u een schema voor uw Webcampagne hebt bepaald, heeft het de **[!UICONTROL Scheduled]** status tot de begindatum en de tijd worden bereikt.
>
>Als u een webcampagne activeert die invloed heeft op dezelfde pagina&#39;s als een andere campagne die al actief is, worden alle wijzigingen toegepast op uw webpagina&#39;s.

Leer meer bij het activeren van campagnes in [ deze sectie ](../campaigns/review-activate-campaign.md).

## Een webcampagne stoppen {#stop-web-campaign}

Wanneer een webcampagne live is, kunt u deze stoppen om te voorkomen dat uw publiek uw wijzigingen ziet. Voer de onderstaande stappen uit.

1. Selecteer een live campagne in de lijst.

1. Selecteer **[!UICONTROL Stop campaign]** in het bovenste menu.

   ![](assets/web-campaign-stop.png)

1. De wijzigingen die u hebt toegevoegd, zijn niet meer zichtbaar voor het publiek dat u hebt gedefinieerd.

>[!NOTE]
>
>Nadat een webcampagne is gestopt, kunt u deze niet meer bewerken of activeren. U kunt de gedupliceerde campagne alleen dupliceren en activeren.

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u een webcampagne kunt maken, de eigenschappen ervan kunt configureren, beoordelen en publiceren.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)