---
solution: Journey Optimizer
product: journey optimizer
title: De reis publiceren
description: Ontdek hoe je op je reis meldt
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---

# Live melding op de reiscanvas {#report-journey}

Nadat uw reis wordt gepubliceerd, zodra de [ Dry looppas wijze ](journey-dry-run.md) wordt geactiveerd, **Levende Rapportering** metriek van de laatste 24 uren, direct binnen het wegcanvas verstrekt.


>[!AVAILABILITY]
>
>Als u geen gegevens kunt zien in uw live rapport over de reis, moeten uw toegangsrechten worden uitgebreid en de machtiging **[!UICONTROL View journeys report]** worden opgenomen. [Meer informatie](../administration/permissions.md)


De weergegeven gebeurtenissen hebben zich in de afgelopen 24 uur voorgedaan, met een minimuminterval van twee minuten tussen de gebeurtenis en de weergave, meestal binnen vijf minuten.

![ Reis levende rapportdashboard die prestaties metriek in real time toont ](assets/journey_live_report.png)

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

## Problemen met ontbrekende rapportgegevens oplossen {#troubleshooting-missing-data}

Als u de verwachte gegevens niet ziet in uw reisrapporten, overweeg het volgende:

* **de naamsynchronisatie van de Reis**: Verifieer dat de reisnaam in [!DNL Adobe Journey Optimizer] de naam aanpast die in de rapporteringsdataset wordt opgeslagen. Als deze namen niet overeenkomen, worden de rapportgegevens mogelijk niet correct weergegeven.

* **Gegevens verfrissen timing**: Na het bijwerken van een reisnaam of configuratie, sta voldoende tijd voor de gegevens toe om zich te verfrissen. Gegevens worden meestal binnen een paar minuten gerapporteerd, maar in sommige gevallen kan het langer duren.

* **toestemmingen van de Toegang**: Zorg u de noodzakelijke toestemmingen hebt om reisrapporten te bekijken. Als er geen gegevens worden weergegeven, controleert u met de beheerder of u de machtiging **[!UICONTROL View journeys report]** hebt ingeschakeld. [ leer meer over toestemmingen ](../administration/permissions.md)

* **status van de Reis**: Het melden van gegevens is slechts beschikbaar voor gepubliceerde reizen of reizen die op [ lopen Droog looppaswijze ](journey-dry-run.md). Met een conceptrit worden geen rapportgegevens gegenereerd.

Neem contact op met uw Adobe-beheerder of Adobe voor hulp als er problemen blijven optreden nadat u deze items hebt gecontroleerd.

>[!MORELIKETHIS]
>
>* [Aan de slag met rapportage](../reports/gs-reports.md)
>* [ publiceer uw reis ](publish-journey.md)
>* [ Droog van de Reis ](journey-dry-run.md)
>* [ vormt en volgt uw reismetriek ](success-metrics.md)
>* [ de reisrapporten van de Douane ](../reports/sharing-overview.md)
