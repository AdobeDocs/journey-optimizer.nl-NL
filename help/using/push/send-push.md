---
solution: Journey Optimizer
product: journey optimizer
title: Uw pushmelding bekijken en testen
description: Leer hoe u uw pushmelding in Journey Optimizer kunt bekijken en testen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 4%

---

# Uw pushmelding bekijken en testen {#send-push}

## Een voorbeeld van uw pushmelding bekijken {#preview-push}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

1. Klik op **[!UICONTROL Simulate content]**.

1. Klikken **[!UICONTROL Manage test profiles]** om een testprofiel toe te voegen.

1. Zoek uw testprofiel met de **[!UICONTROL Identity namespace]** en **[!UICONTROL Identity value]** velden. Klik vervolgens op **[!UICONTROL Add profile]**.

   ![](assets/push_preview_1.png)

1. Nadat u het testprofiel hebt geselecteerd, kunt u het dialoogvenster **[!UICONTROL Add test profile]** venster.

1. Van de **Voorvertonen en testen** worden de gegevens van het testprofiel toegevoegd aan de inhoud van het bericht.

   Selecteer het type apparaat waarvan u een voorvertoning van inhoud wilt weergeven: **[!UICONTROL iOS]** of **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Uw pushmelding valideren {#push-validate}


U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken.

* **Fouten** voorkomen dat u de reis test of activeert zolang deze niet is opgelost, zoals:

   * **[!UICONTROL The push version of the message is empty]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van het pushbericht ontbreekt. Leer hoe u inhoud voor pushmeldingen definieert in [deze sectie](create-push.md).

   * **[!UICONTROL Surface doesn't exist]**: U kunt uw bericht niet gebruiken als het geselecteerde oppervlak wordt verwijderd na het maken van het bericht. Als deze fout optreedt, selecteert u een ander oppervlak in het bericht **[!UICONTROL Properties]**. Meer informatie over kanaaloppervlakken in [deze sectie](../configuration/channel-surfaces.md).

   * **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe u de inhoud van uw pushmelding beheert in [deze sectie](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Voor betere leverbaarheid, zou u de telefoonaantallen in de formaten altijd moeten gebruiken die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

## Uw pushmelding verzenden{#push-send}

Wanneer uw pushbericht klaar is, voltooit u de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Pushkanaal configureren](push-configuration.md)
* [Pushmeldingenrapport](../reports/journey-global-report.md#push-global)
* [Een pushmelding maken](create-push.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)

