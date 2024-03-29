---
title: Webervaringen maken
description: Leer hoe u een webpagina ontwerpt en de inhoud ervan bewerkt in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 2%

---

# Webervaringen maken {#create-web}

[!DNL Journey Optimizer] kunt u de webervaring aanpassen die u aan uw klanten via binnenkomende webcampagnes levert.

>[!CAUTION]
>
>Momenteel in [!DNL Journey Optimizer] u kunt alleen webervaringen maken met **campagnes**.

[Leer hoe u een webcampagne kunt maken in deze video](#video)

## Een webcampagne maken {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Een weboppervlak definiëren"
>abstract="Een weboppervlak kan overeenkomen met één pagina-URL of meerdere pagina&#39;s, zodat u inhoudwijzigingen kunt doorvoeren op een of meerdere webpagina&#39;s."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Een overeenkomende regel voor pagina&#39;s maken"
>abstract="Met een regel voor pagina&#39;s die overeenkomen met een regel, kunt u bijvoorbeeld meerdere URL&#39;s met dezelfde regel als doel instellen. Dit is bijvoorbeeld het geval als u de wijzigingen wilt toepassen op een hoofdbanner op een hele website of een bovenste afbeelding wilt toevoegen die op alle productpagina&#39;s van een website wordt weergegeven."

Volg onderstaande stappen om uw webervaring op te bouwen via een campagne.

>[!NOTE]
>
>Als dit de eerste keer is dat u een webervaring maakt, moet u de voorwaarden volgen die worden beschreven in [deze sectie](web-prerequisites.md).

1. Een campagne maken. [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer de **[!UICONTROL Web]** handeling.

1. Definieer een weboppervlak.

   >[!NOTE]
   >
   >Een weboppervlak is een webeigenschap die wordt geïdentificeerd door een URL waar de inhoud wordt geleverd. De URL kan overeenkomen met één pagina of meerdere pagina&#39;s, zodat u wijzigingen kunt doorvoeren op een of meerdere webpagina&#39;s.

   U kunt een van de **[!UICONTROL Page URL]** als u de wijzigingen alleen op één pagina wilt toepassen.

   ![](assets/web-campaign-surface.png)

1. U kunt ook een **[!UICONTROL Pages matching rule]** om meerdere URL&#39;s met dezelfde regel als doel in te stellen, bijvoorbeeld als u de wijzigingen wilt toepassen op een hoofdbanner op een hele website of een bovenste afbeelding wilt toevoegen die op alle productpagina&#39;s van een website wordt weergegeven.

   Selecteer **[!UICONTROL Pages matching rule]** en klik op **[!UICONTROL Create rule]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definieer uw criteria voor de **[!UICONTROL Domain]** en **[!UICONTROL Page]** velden.

   Als u bijvoorbeeld elementen wilt bewerken die op alle pagina&#39;s met vrouwenproducten van uw Luma-website worden weergegeven, selecteert u **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` en **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Sla uw wijzigingen op. De regel wordt weergegeven in het dialoogvenster **[!UICONTROL Create campaign]** scherm.

   ![](assets/web-pages-matching-rule-example.png)

1. Nadat u het weboppervlak hebt gedefinieerd, selecteert u **[!UICONTROL Create]**.

1. Voer de stappen uit om een webcampagne te maken, zoals de eigenschappen van de campagne, [publiek](../audience/about-audiences.md), en [schema](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

## De webcampagne testen {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Een voorvertoning van uw webbeleving bekijken"
>abstract="Bekijk een simulatie van hoe uw webervaring eruit zal zien."

Eenmaal [gemaakt voor uw webervaring](edit-web-content.md) met de webontwerper kunt u testprofielen gebruiken om een voorvertoning van uw gewijzigde webpagina&#39;s weer te geven. Als u persoonlijke inhoud hebt ingevoegd, kunt u met behulp van de gegevens van het testprofiel controleren hoe deze inhoud wordt weergegeven.

Om dit te doen, klik **[!UICONTROL Simulate content]** vanuit het webcampagnebewerkingsinhoudscherm of de webontwerper voegt u vervolgens een testprofiel toe om uw webpagina te controleren met behulp van de testprofielgegevens.

![](assets/web-designer-preview.png)

U kunt de URL ook in de standaardbrowser openen of de test-URL kopiëren en in een browser plakken. Op deze manier kunt u de koppeling delen met uw team en belanghebbenden die de nieuwe webervaring in een browser kunnen bekijken voordat de campagne live gaat.

>[!NOTE]
>
>Wanneer het kopiëren van testURL, is de getoonde inhoud die voor het testprofiel wordt gepersonaliseerd dat wordt gebruikt toen de inhoudsimulatie werd geproduceerd in [!DNL Journey Optimizer].

Gedetailleerde informatie over het selecteren van testprofielen en het weergeven van een voorvertoning van de inhoud is beschikbaar in het dialoogvenster [Inhoud beheren](../content-management/preview-test.md) sectie.

## De webcampagne activeren {#activate-web-campaign}

Zodra u uw [webcampagneinstellingen](#configure-web-campaign) en u hebt de inhoud naar wens bewerkt met de [webontwerper](edit-web-content.md#work-with-web-designer), kunt u uw webcampagne controleren en activeren. Voer de onderstaande stappen uit.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Selecteer in uw webcampagne de optie **[!UICONTROL Review to activate]**.

1. Controleer en bewerk indien nodig de inhoud, eigenschappen, oppervlak, publiek en planning.

1. Selecteer **[!UICONTROL Activate]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Nadat u op **[!UICONTROL Activate]** Het kan tot 15 minuten duren voordat wijzigingen in webcampagnes live op uw website beschikbaar zijn.

Uw webcampagne neemt de **[!UICONTROL Live]** en is nu zichtbaar voor het geselecteerde publiek. Elke ontvanger van de campagne kan de wijzigingen zien die u aan uw website hebt toegevoegd met de opdracht [!DNL Journey Optimizer] webontwerper.

>[!NOTE]
>
>Als u een schema voor uw webcampagne hebt gedefinieerd, heeft deze de **[!UICONTROL Scheduled]** status tot de begindatum en -tijd zijn bereikt.
>
>Als u een webcampagne activeert die invloed heeft op dezelfde pagina&#39;s als een andere campagne die al actief is, worden alle wijzigingen toegepast op uw webpagina&#39;s.

Meer informatie over het activeren van campagnes in [deze sectie](../campaigns/review-activate-campaign.md).

## Een webcampagne stoppen {#stop-web-campaign}

Wanneer een webcampagne live is, kunt u deze stoppen om te voorkomen dat uw publiek uw wijzigingen ziet. Voer de onderstaande stappen uit.

1. Selecteer een live campagne in de lijst.

1. Selecteer in het bovenste menu de optie **[!UICONTROL Stop campaign]**.

   ![](assets/web-campaign-stop.png)

1. De wijzigingen die u hebt toegevoegd, zijn niet meer zichtbaar voor het publiek dat u hebt gedefinieerd.

>[!NOTE]
>
>Nadat een webcampagne is gestopt, kunt u deze niet meer bewerken of activeren. U kunt de gedupliceerde campagne alleen dupliceren en activeren.

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u een webcampagne kunt maken, de eigenschappen ervan kunt configureren, beoordelen en publiceren.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)