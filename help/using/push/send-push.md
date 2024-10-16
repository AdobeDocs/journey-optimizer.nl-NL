---
solution: Journey Optimizer
product: journey optimizer
title: Controleer en verzend uw pushmelding
description: Meer weten over het controleren en verzenden van pushberichten in Journey Optimizer?
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# Controleer en verzend uw pushmelding {#send-push}

## Een voorbeeld van uw pushmelding bekijken {#preview-push}

Nadat de inhoud van het bericht is gedefinieerd, kunt u testprofielen gebruiken om de inhoud ervan voor te vertonen. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Klik hiertoe op **[!UICONTROL Simulate content]** en voeg vervolgens een testprofiel toe. Vervolgens kunt u het type apparaat selecteren dat u wilt voorvertonen met inhoud: **[!UICONTROL iOS]** of **[!UICONTROL Android]** .

![](assets/push_preview_3.png)

De gedetailleerde informatie over hoe te om testprofielen en voorproef uw inhoud te selecteren is beschikbaar in de [ sectie van het Beheer van de Inhoud ](../content-management/preview-test.md).

## Uw pushmelding valideren {#push-validate}

U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **de Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken.

* **de Fouten** verhinderen u de reis te testen of te activeren zolang zij niet, zoals worden opgelost:

   * **[!UICONTROL The push version of the message is empty]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van de pushmelding ontbreekt. Leer hoe te om de inhoud van het pushbericht in [ te bepalen deze sectie ](create-push.md).

   * **[!UICONTROL configuration doesn't exist]**: u kunt het bericht niet gebruiken als de configuratie die u hebt geselecteerd, wordt verwijderd na het maken van het bericht. Als deze fout voorkomt, selecteer een andere configuratie in het bericht **[!UICONTROL Properties]**. Leer meer op kanaalconfiguraties in [ deze sectie ](../configuration/channel-surfaces.md).

   * **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe te om uw inhoud van het pushbericht in [ te beheren deze sectie ](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Voor betere leverbaarheid, zou u de telefoonaantallen in de formaten altijd moeten gebruiken die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

## Uw pushmelding verzenden{#push-send}

>[!IMPORTANT]
>
>Vanaf de release van september kunt u met een nieuwe ervaring op het gebied van campagne en trajectactivering het hele goedkeuringsproces beheren. Zo kunt u ervoor zorgen dat campagnes en reizen grondig worden doorgelicht en goedgekeurd door de belanghebbenden voordat u live gaat. Deze functie is beschikbaar in Beperkte Beschikbaarheid. [Meer informatie](../test-approve/gs-approval.md)

Wanneer uw duw bericht klaar is, voltooi de configuratie van uw [ reis ](../building-journeys/journey-gs.md) of [ campagne ](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Pushkanaal configureren](push-configuration.md)
* [Pushmeldingenrapport](../reports/journey-global-report-cja-push.md)
* [Een pushmelding maken](create-push.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)

