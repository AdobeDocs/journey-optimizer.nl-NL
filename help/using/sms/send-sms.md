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
source-git-commit: d6a46a6db9bcef4def71e915389d725c69d851c3
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---

# Je tekstbericht controleren en verzenden (SMS/MMS){#send-sms}

## Tekstbericht voorvertonen {#preview-sms}

Nadat de inhoud van het bericht is gedefinieerd, kunt u testprofielen of voorbeeldinvoergegevens (die vanuit een CSV/JSON-bestand zijn geüpload of handmatig zijn toegevoegd) gebruiken om de inhoud ervan voor te vertonen. Als u persoonlijke inhoud hebt ingevoegd, kunt u controleren hoe deze inhoud in het bericht wordt weergegeven.

Klik hiertoe op **[!UICONTROL Simulate content]** en controleer het bericht met behulp van de gegevens van het testprofiel.

![](assets/sms_preview_2.png)

De gedetailleerde informatie over hoe te voorproef &amp; test inhoud is beschikbaar in de [&#x200B; sectie van het Beheer van de Inhoud &#x200B;](../content-management/preview-test.md).

### Tekencodering en -beperkingen {#sms-character-limits}

Er wordt een aantal tekens weergegeven wanneer u het menu **[!UICONTROL Simulate content]** opent voor hulp bij het plannen en beheren van uw SMS-berichten.

![](assets/sms_preview_3.png)

Journey Optimizer gebruikt UTF-8-codering in de SMS-editor, zodat u double-byte of Unicode-tekens kunt typen of plakken. Deze tekens worden vervolgens naar de serviceprovider verzonden voor levering. De meeste SMS-providers gebruiken 7-bits GSM-codering voor standaardberichten met een limiet van 160 tekens en schakelen over naar UTF-16 (UCS-2) wanneer niet-GSM-tekens met een limiet van 70 tekens worden gedetecteerd.

Het aantal tekens weerspiegelt niet de variaties die zijn ontstaan door dynamische personalisatie of 7-bits speciale tekens die geen GSM zijn.

>[!IMPORTANT]
>
>Bij de rapportage van Journey Optimizer SMS-berichten wordt geen rekening gehouden met samengevoegde berichten en dynamische personalisatie, waardoor het mogelijk is dat het werkelijke aantal berichten dat door de provider wordt verzonden niet wordt weerspiegeld. Neem voor gedetailleerde informatie over gebruik en facturering contact op met uw Adobe-vertegenwoordiger.
>
>Om beste praktijken te leren voor het minimaliseren van SMS het factureren overages, verwijs naar [&#x200B; Beste praktijken van SMS voor de Optimalisering van het Karakter &#x200B;](sms-cost-optimization.md).

## Uw inhoud valideren {#sms-validate}

>[!NOTE]
>
> Om uw leverbaarheid te verbeteren, gebruik de telefoonaantallen in de formaten die door de leverancier worden gesteund. Twilio en Sinch ondersteunen bijvoorbeeld alleen telefoonnummers in E.164-indeling.

U moet alarm in de hogere sectie van de redacteur controleren. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

![](assets/sms-alert-button.png)

* **de Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw tekstbericht leeg is of als de tekenlimiet bij dynamische inhoud wordt overschreden.

  **de grenzen van het Karakter:** 160 karakters per segment (GSM 7 beetje), 70 voor Unicode/emojis, tot 1500 karakters totaal.

* **de Fouten** verhinderen u de reis te testen of te activeren, of de campagne te publiceren, zolang zij niet worden opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.

De waakzame **&quot;De de tekentekengrens van SMS is overschreden&quot;** kan verschijnen zelfs wanneer uw gesimuleerde bericht korter is omdat de bevestiging de **maximum mogelijke lengte** door alle voorwaardelijke takken, verpersoonlijkingsgebieden, en dynamische inhoud bij hun langst te evalueren berekent.

De bevestiging berekent maximumlengte voor alle mogelijke profielgegevens, terwijl de simulatie daadwerkelijke output voor één testprofiel toont.

## Uw tekstberichten verzenden {#sms-send}

>[!IMPORTANT]
>
> Als uw campagne onderworpen is aan een goedkeuringsbeleid, zult u goedkeuring moeten vragen om uw tekstberichten te kunnen verzenden. [Meer informatie](../test-approve/gs-approval.md)

Wanneer uw tekstbericht klaar is, voltooi de configuratie van uw [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md) of [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) om het te verzenden.

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [SMS/MMS-rapporten](../reports/journey-global-report-cja-sms.md)
* [Een tekstbericht maken](create-sms.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
