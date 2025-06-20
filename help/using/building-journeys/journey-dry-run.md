---
solution: Journey Optimizer
product: journey optimizer
title: Reizen op reis
description: Leer hoe u een reis publiceert in de modus Dry (Droge uitvoering)
feature: Journeys
role: User
level: Intermediate
badge: label="Beperkte beschikbaarheid" type="Informative"
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 8f3d619adfb7b2f3dd876da7a3a6eba1fda6dd6b
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# Reizen op reis {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Droge uitvoermodus"
>abstract="Deze reis is in Dry run. Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken.  Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Een rit publiceren in de modus Droog"
>abstract="De Reizen van de Reizen is een speciale wijze van de reispublicatie in Adobe Journey Optimizer die reisartsen toestaat om een reis te testen gebruikend echte productiegegevens. Nadat u de reis hebt ontworpen, voert u een droge run uit om te bevestigen dat deze functioneel is en dat de stappen correct zijn. Met deze publicatiemodus kunt u een reis roken zonder dat u de communicatie naar een profiel hoeft te sturen."

Reis Dry run is een speciale publicatiemodus in Adobe Journey Optimizer die reisartsen in staat stelt een reis te testen met behulp van echte productiegegevens zonder contact op te nemen met echte klanten of profielinformatie bij te werken.  Deze functie helpt reisartsen vertrouwen te winnen in hun reisontwerp en doelgroep voordat ze het live publiceren.


>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid) en wordt globaal geïmplementeerd in een toekomstige release.


## Belangrijkste voordelen {#journey-dry-run-benefits}

Reis Dry-run versterkt het vertrouwen van de arts en het succes van de reis door veilige, gegevensgestuurde tests van klantreizen mogelijk te maken met behulp van echte productiegegevens, zonder het risico van contact met klanten of het wijzigen van profielinformatie. Deze functie stelt reisartsen in staat om het bereik van het publiek en de logica van de vertakking te valideren voordat ze live gaan, zodat de ritten op de gewenste zakelijke doelen zijn afgestemd.

Met de Rondleiding van de Droog van de Reis, kunt u kwesties vroeg identificeren, het richten strategieën optimaliseren, en het reisontwerp verbeteren dat op daadwerkelijke gegevens-geen veronderstellingen wordt gebaseerd. Dry-run is direct geïntegreerd in het reiscanvas en biedt intuïtieve rapportage en zichtbaarheid in belangrijke prestatie-indicatoren, zodat teams betrouwbaar kunnen herhalen en goedkeuringswerkstromen kunnen stroomlijnen. Dit verbetert de operationele efficiëntie, vermindert het opstartrisico en leidt tot betere resultaten van de klantenservice.

Uiteindelijk, verbetert deze eigenschap tijd-aan-waarde en vermindert reismislukkingen.

Op reis is er een droge run:

1. **Veilig testend milieu**: De profielen op Droog looppaswijze worden niet gecontacteerd, die geen risico verzekeren om mededelingen te verzenden of levende gegevens te beïnvloeden.
1. **de inzichten van het publiek**: De artsen van de reis kunnen publieksbereikbaarheid bij diverse vervoerknopen, met inbegrip van opt-outs, uitsluitingen, en andere voorwaarden voorspellen.
1. **in real time terugkoppelt**: De metriek wordt getoond direct in het wegcanvas, gelijkend op levende rapportering, toelatend reisartsen om hun reisontwerp te verfijnen.


>[!CAUTION]
>
>* Machtigingen voor het starten van de droge runtime zijn beperkt tot gebruikers met de machtiging op hoog niveau van **[!DNL Publish journeys]** . Machtigingen om Dry Run te stoppen zijn beperkt tot gebruikers met de machtiging op hoog niveau van **[!DNL Manage journeys]** . Leer meer over het beheren van [!DNL Journey Optimizer] de toegangsrechten van gebruikers in [ deze sectie ](../administration/permissions-overview.md).
>
>* Alvorens het beginnen gebruiken van het Droge looppas vermogen, [ lees uit de Grafieken en Beperkingen ](#journey-dry-run-limitations).


## Een droge run starten {#journey-dry-run-start}

U kunt de functie Dry-run gebruiken in elke conceptreis zonder fouten.

Voer de volgende stappen uit om de droog-uitvoering te activeren:

1. Open de reis die u wilt testen.
1. Klik op de **Droog looppas** knoop.

   ![ Begin de reis droge looppas ](assets/dry-run-button.png)

1. Bevestig de publicatie.

   Een statusbericht, **Activerend Dry looppas**, verschijnt terwijl de overgang gebeurt.

1. Zodra geactiveerd, gaat de reis **Droog looppas** wijze in.

## Een droge run controleren {#journey-dry-monitor}

Zodra de publicatie van de modus Dry is gestart, kunt u de uitvoering van de reis visualiseren en bepalen hoe profielen door de vertakkingen en knooppunten van de rit worden doorlopen.

Metrische gegevens worden direct op het canvas van de reis weergegeven.

![ Monitor de runtime van de reisdroge uitvoering ](assets/dry-run-metrics.png)

Voor elke activiteit kunt u controleren:

* **[!UICONTROL Entered]**: Het totale aantal personen dat deze activiteit heeft ingevoerd.
* **[!UICONTROL Exited (met exit criteria)]**: Het totale aantal personen dat de reis heeft verlaten uit die activiteit, als gevolg van uitstapcriteria.
* **[!UICONTROL Exited (forced exit)]**: Het totale aantal personen dat de reis heeft verlaten terwijl deze was gepauzeerd vanwege de configuratie van een reisdeskundige. Deze metrische waarde is altijd gelijk aan nul voor reizen in de droge loopwijze.
* **[!UICONTROL Error]**: Het totale aantal personen dat een fout heeft gemaakt met die activiteit.


Op het niveau van de reis, kunt u controleren:

* Het totale aantal **binnengaan profielen**
* Het totale aantal van **Verlaten profielen**
* Het totale aantal **Profielen in fout**
* Het totale aantal **Verworpen profielen** in de reis

U kunt tot de **Laatste rapporten van 24 uren** en **Al-tijdrapporten** voor de Dry looppas ook toegang hebben. Om tot deze rapporten toegang te hebben, klik het **rapport van de Mening** knoop op de hoger-juiste hoek van het wegcanvas.

![ heb toegang tot de rapporten voor de runtime van de reisdroge uitvoering ](assets/dry-run-report.png)

>[!CAUTION]
>
> Het melden van gegevens is beschikbaar slechts wanneer de Droog looppas **actief** is.  Zodra gestopt, zullen de rapportgegevens niet meer toegankelijk zijn. Gebruik de **knoop van de Uitvoer** boven de rapporten om hen indien nodig te downloaden.


## Een droge run stoppen {#journey-dry-run-stop}

De droge looppas reizen **moeten** manueel worden tegengehouden.

Klik de **Dichte** knoop om de test te beëindigen, en klik **terug naar Ontwerp** om te bevestigen.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Afvoerkanalen en beperkingen {#journey-dry-run-limitations}

* De droge-uitvoeringsmodus is niet beschikbaar voor reizen die reactiegebeurtenissen bevatten
* Profielen in de droge-uitvoeringsmodus worden geteld voor controleerbare profielen
* Reizen in de droge-uitvoeringsmodus worden meegeteld voor de live-reisquota
* Droge ritten hebben geen invloed op de bedrijfsregels
* Wanneer het creëren van een nieuwe reisversie, als een vorige reisversie **Levend** is, dan wordt de droge looppasactivering niet toegestaan op de nieuwe versie.
* De looppas van de Droog van de reis produceert stepEvents. Deze stepEvents hebben een specifieke vlag en Dry run ID:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` retourneert `true` als de droog-uitvoering is geactiveerd, anders `false`
   * `_experience.journeyOrchestration.stepEvents.dryRunID` retourneert de id van een droge runtime-instantie

* Tijdens de Dry-run wordt de reis uitgevoerd met de volgende specifieke kenmerken:

   * **de actieknooppunten van het Kanaal** met inbegrip van E-mail, SMS of Push berichten worden niet uitgevoerd
   * **de acties van de Douane** worden onbruikbaar gemaakt tijdens Droog looppas, en hun reacties worden geplaatst aan ongeldig
   * **wacht knopen** worden overgeslagen tijdens Dry looppas.
     <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
   * **gegevensbronnen**, met inbegrip van externe gegevensbronnen, worden uitgevoerd door gebrek