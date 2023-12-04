---
solution: Journey Optimizer
product: journey optimizer
title: Tekstberichten controleren en testen
description: Leer hoe je tekstberichten kunt controleren en verzenden in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 9ac8a3ddad165f728c09baacb9d380d4611fd58a
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---

# Controleer en verzend uw tekstbericht (SMS/MMS) {#send-sms}

## Tekstbericht voorvertonen {#preview-sms}

Nadat de inhoud van het bericht is gedefinieerd, kunt u testprofielen gebruiken om de inhoud ervan voor te vertonen. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Om dit te doen, klik **[!UICONTROL Simulate content]** Voeg vervolgens een testprofiel toe om uw bericht te controleren met behulp van de gegevens van het testprofiel.

![](assets/sms_preview_2.png)

Gedetailleerde informatie over het selecteren van testprofielen en het weergeven van een voorvertoning van de inhoud is beschikbaar in het dialoogvenster [Inhoud beheren](../content-management/preview-test.md) sectie.

## Uw inhoud valideren {#sms-validate}

U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

![](assets/sms-alert-button.png)

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw tekstbericht leeg is.

* **Fouten** voorkomt u dat u de reis test of activeert, of de campagne publiceert, zolang deze niet is opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.


>[!NOTE]
>
> Om uw leverbaarheid te verbeteren, gebruik de telefoonaantallen in de formaten die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

## Uw tekstberichten verzenden {#sms-send}

Wanneer uw tekstbericht klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [SMS/MMS-rapporten](../reports/journey-global-report.md#sms-global)
* [Een tekstbericht maken](create-sms.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
