---
solution: Journey Optimizer
product: journey optimizer
title: De reis Publish
description: Ontdek hoe je op je reis meldt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publiceren, reizen, live, geldigheid, controle
source-git-commit: 9b4ff0325d099252a5785aa13cfe0f1fe42acac6
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Live melding op de reiscanvas {#report-journey}

>[!NOTE]
>
>Als u geen gegevens kunt zien in uw live rapport over de reis, moeten uw toegangsrechten worden uitgebreid en de machtiging **[!UICONTROL View journeys report]** worden opgenomen. [Meer informatie](../administration/permissions.md)

Nadat uw reis wordt gepubliceerd, **Levende Rapportering** verstrekt metriek van de laatste 24 uren, direct binnen het wegcanvas.

De weergegeven gebeurtenissen hebben zich in de afgelopen 24 uur voorgedaan, met een minimuminterval van twee minuten tussen de gebeurtenis en de weergave, meestal binnen vijf minuten.

![](assets/journey_live_report.png)

Voor uw live reis hebt u toegang tot:

* **[!UICONTROL Entered profiles]**: Het totale aantal personen dat de reis heeft verlaten (inclusief fouten).
* **[!UICONTROL Exited profiled]**: Het totale aantal personen dat de reis heeft verlaten uit die activiteit, als gevolg van uitstapcriteria.
* **[!UICONTROL Profiles in error]**: Het totale aantal personen dat tijdens hun reis een fout heeft aangetroffen.
* **[!UICONTROL Discarded profiles]**: Het totale aantal personen dat om een van de volgende redenen van de reis is verwijderd:

   * Voor **de Kwalificatie van het publiek** activiteiten, kan een ontkenning gebeuren als het verwachte werkwoord voor publiekskwalificatie niet aanpast welke reis heeft ontvangen (b.v. &quot;verlaten&quot;in plaats van &quot;gerealiseerd&quot;).
   * Voor **gebeurtenis-teweeggebrachte** reizen, kan een teruggooi gebeuren als het individu probeerde om de reis te spoedig opnieuw binnen te gaan of wanneer de terugkeer niet werd toegestaan.
   * Op **terugkomende** reizen, wordt een teruggooi geteld op elke herhaling als het individu reeds in de reis is en het terugkeerbeleid niet aan &quot;forceer terugkeer&quot;wordt geplaatst.
   * Op **Gelezen de activiteiten van het Publiek**, komt een verwerpen voor als geen identiteit voor het uitgevoerde individu wordt geplaatst, of als ontvangen identiteitsnaamruimte niet verwachte voor de reis aanpast.

Voor elke activiteit binnen elke levende reis hebt u toegang tot:

* **[!UICONTROL Entered]**: Het totale aantal personen dat deze activiteit heeft ingevoerd.
* **[!UICONTROL Exited (met exit criteria)]**: Het totale aantal personen dat de reis heeft verlaten uit die activiteit, als gevolg van uitstapcriteria.
* **[!UICONTROL Error]**: Het totale aantal personen dat een fout heeft gemaakt met die activiteit.
