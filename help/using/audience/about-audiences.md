---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over Adobe Experience Platform-publiek
description: Leer hoe u met het publiek van Adobe Experience Platform kunt werken
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Platform-publiek {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="Met Adobe Experience Platform kunt u eenvoudig segmentdefinities maken door gebruik te maken van realtime klantprofielgegevens. Zo kunt u doelgroepen maken die de unieke gedragingen en voorkeuren van uw klanten vastleggen."

[!DNL Journey Optimizer] stelt u in staat om Adobe Experience Platform-publiek rechtstreeks vanuit de **[!UICONTROL Audiences]** en gebruikt u deze voor reizen of campagnes.

Meer informatie in het dialoogvenster [Adobe Experience Platform Segmentation Service-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Soorten publiek gebruiken in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt het publiek benutten in **[!DNL Journey Optimizer]** op verschillende manieren:

* Kies een publiek voor een **campagne**, waarbij het bericht wordt verzonden naar alle personen die tot het geselecteerde publiek behoren. [Leer hoe u het publiek van een campagne definieert](../campaigns/create-campaign.md#define-the-audience-audience).

* Een **Lees publiek** Orchestratie-activiteit op een reis om ervoor te zorgen dat alle individuen in het publiek de reis betreden en de berichten ontvangen inbegrepen in uw reis.

  Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden. [Leer hoe te om een Gelezen publieksactiviteit te vormen](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Gebruik de **Poortkwalificatie** gebeurtenisactiviteit op een reis om ervoor te zorgen dat individuen de reis betreden of vooruit gaan op basis van de toegang tot en het vertrek van Adobe Experience Platform-gebruikers.

  U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg voor meer informatie over het gebruik van deze activiteit [Leer hoe te om een de kwalificatieactiviteit van het Publiek te vormen](../building-journeys/audience-qualification-events.md).

* Gebruik de **Voorwaarde** activiteit op een reis om voorwaarden op te bouwen die op het lidmaatschap van het publiek worden gebaseerd. [Meer informatie over het gebruik van soorten publiek in omstandigheden](../building-journeys/condition-activity.md#using-a-segment).

## Methoden voor de evaluatie van het publiek{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer worden publiek op basis van segmentdefinities gegenereerd met behulp van een van de volgende twee evaluatiemethoden:

* **Streaming segmentering**: De profiellijst voor het publiek wordt bijgewerkt in real time aangezien de nieuwe gegevens in het systeem stromen.

  Streaming segmentatie is een doorlopend proces voor gegevensselectie dat uw publiek bijwerkt als reactie op gebruikersactiviteit. Zodra een segmentdefinitie is gebouwd en het resulterende publiek is bewaard, wordt de segmentdefinitie toegepast op inkomende gegevens aan Journey Optimizer. Dit betekent dat individuen worden toegevoegd of uit het publiek verwijderd aangezien hun profielgegevens veranderen, ervoor zorgen dat uw doelpubliek altijd relevant is.

* **Batchsegmentatie**: De profiellijst voor het publiek wordt om de 24 uur geëvalueerd.

  De segmentatie van de partij is een alternatief aan het stromen segmentatie die alle profielgegevens in één keer door segmentdefinities verwerkt. Zo maakt u een momentopname van het publiek die u kunt opslaan en exporteren voor gebruik. Nochtans, in tegenstelling tot het stromen segmentatie, werkt de partijsegmentatie niet onophoudelijk de publiekslijst in real time bij, en de nieuwe gegevens die binnen na het partijproces komen zullen niet in het publiek tot het volgende partijproces worden weerspiegeld.&quot;

De bepaling tussen partijsegmentatie en het stromen segmentatie wordt gemaakt door het systeem voor elk publiek, dat op de ingewikkeldheid en de kosten wordt gebaseerd om de regel van de segmentdefinitie te evalueren. U kunt de evaluatiemethode voor elk publiek in bekijken in **[!UICONTROL Evaluation method]** kolom van de publiekslijst.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Als de **[!UICONTROL Evaluation method]** de kolom niet toont, moet u het toevoegen gebruikend configuratieknoop op de hoogste recht van de lijst.

Nadat u een publiek voor het eerst hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.
