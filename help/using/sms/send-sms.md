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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 2%

---

# Controleer en verzend uw tekstbericht (SMS/MMS){#send-sms}

## Tekstbericht voorvertonen {#preview-sms}

Nadat de inhoud van het bericht is gedefinieerd, kunt u testprofielen gebruiken om de inhoud ervan voor te vertonen. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Klik hiertoe op **[!UICONTROL Simulate content]** en voeg vervolgens een testprofiel toe om uw bericht te controleren aan de hand van de gegevens van het testprofiel.

![](assets/sms_preview_2.png)

De gedetailleerde informatie over hoe te om testprofielen en voorproef uw inhoud te selecteren is beschikbaar in de [ sectie van het Beheer van de Inhoud ](../content-management/preview-test.md).

## Uw inhoud valideren {#sms-validate}

U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

![](assets/sms-alert-button.png)

* **de Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw tekstbericht leeg is.

* **de Fouten** verhinderen u de reis te testen of te activeren, of de campagne te publiceren, zolang zij niet worden opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.


>[!NOTE]
>
> Om uw leverbaarheid te verbeteren, gebruik de telefoonaantallen in de formaten die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

## Uw tekstberichten verzenden {#sms-send}

>[!IMPORTANT]
>
>Vanaf de release van september kunt u met een nieuwe ervaring op het gebied van campagne en trajectactivering het hele goedkeuringsproces beheren. Zo kunt u ervoor zorgen dat campagnes en reizen grondig worden doorgelicht en goedgekeurd door de belanghebbenden voordat u live gaat. Deze functie is beschikbaar in Beperkte Beschikbaarheid. [Meer informatie](../test-approve/gs-approval.md)

Wanneer uw tekstbericht klaar is, voltooi de configuratie van uw [ reis ](../building-journeys/journey-gs.md) of [ campagne ](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [SMS/MMS-rapporten](../reports/journey-global-report-cja-sms.md)
* [Een tekstbericht maken](create-sms.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
