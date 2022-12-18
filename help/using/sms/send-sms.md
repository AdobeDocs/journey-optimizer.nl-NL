---
solution: Journey Optimizer
product: journey optimizer
title: Je SMS-bericht bekijken
description: Meer weten over het bekijken en testen van je SMS-bericht in Journey Optimizer?
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 5%

---

# Je SMS-bericht verzenden {#send-sms}

## Je SMS-bericht bekijken {#preview-sms}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u persoonlijke inhoud hebt ingevoegd, kunt u controleren hoe deze inhoud in het bericht wordt weergegeven en daarbij gebruikmaken van testprofielgegevens.

1. Klik op **[!UICONTROL Simulate content]**.

1. Klikken **[!UICONTROL Manage test profiles]** om een testprofiel toe te voegen.

1. Zoek uw testprofiel met de **[!UICONTROL Identity namespace]** en **[!UICONTROL Identity value]** velden. Klik vervolgens op **[!UICONTROL Add profile]**.

   ![](assets/sms_preview_3.png)

1. Nadat u het testprofiel hebt geselecteerd, kunt u het dialoogvenster **[!UICONTROL Add test profile]** venster.

   ![](assets/sms_preview_1.png)

1. Vanuit het venster Voorvertoning en test worden de gegevens van het testprofiel gebruikt in de inhoud van het bericht.

   Voor dit SMS-bericht is de inhoud van beide berichten bijvoorbeeld gepersonaliseerd:

   ![](assets/sms_preview_2.png)

## Je SMS valideren{#sms-preview}

>[!NOTE]
>
> Voor betere leverbaarheid, zou u de telefoonaantallen in de formaten altijd moeten gebruiken die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

U moet ook waarschuwingen controleren in het bovenste gedeelte van de editor.  Sommige zijn eenvoudige waarschuwingen, maar andere kunnen voorkomen dat u het bericht gebruikt. Er kunnen twee typen waarschuwingen optreden:

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een bericht weergegeven als uw SMS-bericht leeg is.

* **Fouten** voorkomt dat u de reis test of activeert zolang deze niet is opgelost. U wordt bijvoorbeeld in een bericht gewaarschuwd dat de onderwerpregel ontbreekt.

![](assets/sms-alert-button.png)

Wanneer uw SMS-bericht klaar is, voltooit u de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [Sms-rapport](../reports/journey-global-report.md#sms-global)
* [Een SMS-bericht maken](create-sms.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
