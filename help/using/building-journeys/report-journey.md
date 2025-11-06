---
solution: Journey Optimizer
product: journey optimizer
title: De reis publiceren
description: Ontdek hoe je op je reis meldt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# Live melding op de reiscanvas {#report-journey}

Nadat uw reis wordt gepubliceerd, zodra de [ Dry looppas wijze ](journey-dry-run.md) wordt geactiveerd, **Levende Rapportering** metriek van de laatste 24 uren, direct binnen het wegcanvas verstrekt.


>[!AVAILABILITY]
>
>Als u geen gegevens kunt zien in uw live rapport over de reis, moeten uw toegangsrechten worden uitgebreid en de machtiging **[!UICONTROL View journeys report]** worden opgenomen. [Meer informatie](../administration/permissions.md)


De weergegeven gebeurtenissen hebben zich in de afgelopen 24 uur voorgedaan, met een minimuminterval van twee minuten tussen de gebeurtenis en de weergave, meestal binnen vijf minuten.

![](assets/journey_live_report.png)

Voor uw reizen op Levende of [ Droog looppaswijze ](journey-dry-run.md), kunt u controleren:

* **[!UICONTROL Entered profiles]**: Het totale aantal personen dat de reis heeft betreden.
* **[!UICONTROL Exited profiles]**: Het totale aantal personen dat de reis heeft verlaten (inclusief fouten).
* **[!UICONTROL Profiles in error]**: Het totale aantal personen dat tijdens hun reis een fout heeft aangetroffen.
* **[!UICONTROL Discarded profiles]**: Het totale aantal personen dat om een van de volgende redenen van de reis is verwijderd:

   * Voor **de Kwalificatie van het publiek** activiteiten, kan een ontkenning gebeuren als het verwachte werkwoord voor publiekskwalificatie niet aanpast welke reis heeft ontvangen (b.v. &quot;verlaten&quot;in plaats van &quot;gerealiseerd&quot;).
   * Voor **gebeurtenis-teweeggebrachte** reizen, kan een teruggooi gebeuren als het individu probeerde om de reis te spoedig opnieuw binnen te gaan of wanneer de terugkeer niet werd toegestaan.
   * Op **terugkomende** reizen, wordt een teruggooi geteld op elke herhaling als het individu reeds in de reis is en het terugkeerbeleid niet aan &quot;forceer terugkeer&quot;wordt geplaatst.
   * Op **Gelezen de activiteiten van het Publiek**, komt een verwerpen voor als geen identiteit voor het uitgevoerde individu wordt geplaatst, of als ontvangen identiteitsnaamruimte niet verwachte voor de reis aanpast.

Voor elke activiteit binnen elke reis in Levende of [ Droge looppas wijze ](journey-dry-run.md), hebt u toegang tot:

* **[!UICONTROL Entered]**: Het totale aantal personen dat deze activiteit heeft ingevoerd. Voor **de activiteiten van de Actie**, aangezien zij niet op Droog looppas wijze worden uitgevoerd, wijst metrisch op profielen die door overgaan.
* **[!UICONTROL Exited (met exit criteria)]**: Het totale aantal personen dat de reis heeft verlaten van die activiteit, als gevolg van een exit-criterium (inclusief fouten).
* **[!UICONTROL Exited (forced exit)]**: Het totale aantal personen dat de reis heeft verlaten terwijl deze was gepauzeerd vanwege de configuratie van een reisdeskundige. Deze metrische waarde is altijd gelijk aan nul voor reizen in de droge loopwijze.
* **[!UICONTROL Error]**: Het totale aantal personen dat een fout heeft gemaakt met die activiteit.


>[!MORELIKETHIS]
>
>* [Aan de slag met rapportage](../reports/gs-reports.md)
>* [ publiceer uw reis ](publish-journey.md)
>* [ Droog van de Reis ](journey-dry-run.md)
>* [ vormt en volgt uw reismetriek ](success-metrics.md)
>* [ de reisrapporten van de Douane ](../reports/sharing-overview.md)