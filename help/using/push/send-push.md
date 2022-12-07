---
solution: Journey Optimizer
product: journey optimizer
title: Uw pushmelding verzenden
description: Leer hoe u uw pushmelding in Journey Optimizer kunt bekijken en testen
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Uw pushmelding verzenden {#send-push}

## Een voorbeeld van uw pushmelding bekijken {#preview-push}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u persoonlijke inhoud hebt ingevoegd, kunt u controleren hoe deze inhoud in het bericht wordt weergegeven en daarbij gebruikmaken van testprofielgegevens.

1. Klik op **[!UICONTROL Simulate content]**.

1. Klikken **[!UICONTROL Manage test profiles]** om een testprofiel toe te voegen.

1. Zoek uw testprofiel met de **[!UICONTROL Identity namespace]** en **[!UICONTROL Identity value]** velden. Klik vervolgens op **[!UICONTROL Add profile]**.

   ![](assets/push_preview_1.png)

1. Pas de hierboven beschreven stappen toe om een testprofiel te selecteren en

   ![](assets/push_preview_2.png)

1. In de pushvoorvertoning worden de gegevens van het testprofiel gebruikt in de berichtinhoud.

   Selecteer het type apparaat waarvan u een voorvertoning van inhoud wilt weergeven: **[!UICONTROL iOS]** of **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Uw pushmelding valideren {#push-validate}

>[!NOTE]
>
> Voor betere leverbaarheid, zou u de telefoonaantallen in de formaten altijd moeten gebruiken die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

U moet ook waarschuwingen controleren in het bovenste gedeelte van de editor.  Sommige zijn eenvoudige waarschuwingen, maar andere kunnen voorkomen dat u het bericht gebruikt. Er kunnen twee typen waarschuwingen optreden:

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken.

* **Fouten** voorkomen dat u de reis test of activeert zolang deze niet is opgelost, zoals:

   * **[!UICONTROL The push version of the message is empty]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van het pushbericht ontbreekt. Leer hoe u inhoud voor pushmeldingen definieert in [deze sectie](create-push.md).

   * **[!UICONTROL Surface doesn't exist]**: U kunt uw bericht niet gebruiken als het geselecteerde oppervlak wordt verwijderd na het maken van het bericht. Als deze fout optreedt, selecteert u een ander oppervlak in het bericht **[!UICONTROL Properties]**. Meer informatie over kanaaloppervlakken in [deze sectie](../configuration/channel-surfaces.md).

   * **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe u de inhoud van uw pushmelding beheert in [deze sectie](../push/create-push.md).

![](assets/push_alert.png)

Wanneer uw pushmelding gereed is, voltooit u de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) om het te verzenden.

