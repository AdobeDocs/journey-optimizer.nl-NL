---
solution: Journey Optimizer
product: journey optimizer
title: Uw eigen e-mailinhoud coderen
description: Leer hoe u uw eigen e-mailinhoud codeert
feature: Email Design
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: code, HTML, editor
exl-id: 5fb79300-08c6-4c06-a77c-d0420aafca31
source-git-commit: 48b3ef3d2e041ea49d1b0c91cc72ea04237a5e33
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 2%

---

# Uw eigen inhoud coderen {#code-content}

Gebruik de modus **[!UICONTROL Code your own]** om onbewerkte HTML te importeren en/of uw e-mailinhoud te coderen. Deze methode vereist HTML-vaardigheden.

➡️ [Ontdek deze functie in video](#video)

>[!CAUTION]
>
> De beelden van [ Adobe Experience Manager Assets ](../integrations/assets.md) kunnen niet worden van verwijzingen voorzien wanneer het gebruiken van deze methode. De afbeeldingen waarnaar in uw HTML-code wordt verwezen, moeten worden opgeslagen op een openbare locatie.

1. Selecteer **[!UICONTROL Code your own]** op de homepage van E-mail Designer.

   ![](assets/code-your-own.png)

1. Voer de onbewerkte HTML-code in of plak deze.

1. Gebruik het linkerdeelvenster om [!DNL Journey Optimizer] personalisatiemogelijkheden te benutten. [Meer informatie](../personalization/personalize.md)

   ![](assets/code-editor.png)

   >[!NOTE]
   >
   >De personalisatie-editor in de e-mail Designer heeft enkele functiebeperkingen in vergelijking met reisexpressies. [ leer meer over datum/tijdfunctiebeperkingen ](#date-time-limitations)

1. Als u uw e-mailinhoud wilt wissen en uw e-mail wilt starten vanuit een nieuw ontwerp, selecteert u **[!UICONTROL Change your design]** in het optiemenu.

   ![](assets/code-editor-change-design.png)

   >[!NOTE]
   >
   >Met deze handeling wordt de geselecteerde sjabloon geopend in de e-mailtoepassing van de Designer. Daarna kunt u het ontwerp van uw e-mail voltooien of teruggaan naar de code-editor met de optie **[!UICONTROL Switch to code editor]** .

1. Klik op de knop **[!UICONTROL Preview]** om het ontwerp en de personalisatie van berichten te controleren met behulp van testprofielen. [Meer informatie](../content-management/preview-test.md)

   ![](assets/code-editor-preview.png)

1. Zodra uw code klaar is, klik **[!UICONTROL Save]** dan ga terug naar het scherm van de berichtverwezenlijking om uw bericht te voltooien.

   ![](assets/code-editor-save.png)

## Beperkingen van datum- en tijdfunctie {#date-time-limitations}

Wanneer u personalisatie gebruikt in de E-mailcode-editor van de Designer, is de functie `now()` niet beschikbaar voor dynamische datumberekeningen.

>[!IMPORTANT]
>
>De `now()` functie wordt **niet gesteund** in de de uitdrukkingstaal van de Bouwer E-mail. Hoewel `now()` beschikbaar is in reisomstandigheden, kan het niet worden gebruikt in e-mailinhoud of de code-editor.

**Beschikbare alternatieven:**

Gebruik de volgende functies om met huidige datum en tijd in e-mailverpersoonlijking te werken:

* **`getCurrentZonedDateTime()`** - Retourneert de huidige datum en tijd met informatie over de tijdzone. Dit is het aanbevolen alternatief voor `now()` .

  Voorbeeld: `{%= getCurrentZonedDateTime() %}` retourneert `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

* **`currentTimeInMillis()`** - Geeft de huidige tijd in epoch milliseconds.

  Voorbeeld: `{%= currentTimeInMillis() %}`

**geadviseerde alternerende actie:**

Als u datumberekeningen moet uitvoeren in uw e-mailinhoud:

* **precalculate datumgebieden** - bereken vereiste datumwaarden in uw gegevens pijpleiding of profielattributen alvorens e-mail te verzenden, dan verwijzing deze vooraf berekende waarden in uw verpersoonlijking.

  Voorbeeld: `{%= profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate %}`

* **de functies van de de datummanipulatie van het Gebruik** - 2} datum/tijdfuncties [ als ](../personalization/functions/dates.md) of `dayOfYear()` met datumwaarden van profielattributen gebruiken.`diffInDays()`

  Voorbeeld: `{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}`

* **Gebruik gegevens verwerkte attributen** - creeer [ gegevens verwerkte attributen ](../audience/computed-attributes.md) die complexe datumberekeningen uitvoeren, die de resultaten beschikbaar maken als profielattributen.

Leer meer over [ Functies van de Tijd van de Datum in verpersoonlijking ](../personalization/functions/dates.md).
