---
solution: Journey Optimizer
product: journey optimizer
title: Je SMS-bericht bekijken en testen
description: Meer weten over het bekijken en testen van je SMS-bericht in Journey Optimizer?
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 5%

---

# Je SMS-bericht bekijken en testen {#send-sms}

## Je SMS bekijken {#preview-sms}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

1. Klik op **[!UICONTROL Simulate content]**.

1. Klikken **[!UICONTROL Manage test profiles]** om een testprofiel toe te voegen.

1. Zoek uw testprofiel met de **[!UICONTROL Identity namespace]** en **[!UICONTROL Identity value]** velden. Klik vervolgens op **[!UICONTROL Add profile]**.

   ![](assets/sms_preview_3.png)

1. Nadat u het testprofiel hebt geselecteerd, kunt u het dialoogvenster **[!UICONTROL Add test profile]** venster.

1. Van de **Voorvertonen en testen** worden de gegevens van het testprofiel toegevoegd aan de inhoud van het bericht.

   ![](assets/sms_preview_2.png)


## Je SMS valideren{#sms-validate}

U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw SMS-bericht leeg is.

* **Fouten** voorkomt u dat u de reis test of activeert, of de campagne publiceert, zolang deze niet is opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Om uw leverbaarheid te verbeteren, gebruik de telefoonaantallen in de formaten die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

## SMS verzenden{#sms-send}

Wanneer uw SMS-bericht klaar is, voltooit u de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [Sms-rapport](../reports/journey-global-report.md#sms-global)
* [Een SMS-bericht maken](create-sms.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
