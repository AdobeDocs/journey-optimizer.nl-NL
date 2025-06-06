---
solution: Journey Optimizer
product: journey optimizer
title: Reizen op reis
description: Leer hoe u een reis publiceert in de modus Dry (Droge uitvoering)
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beperkte beschikbaarheid" type="Informative"
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 9ac387f073d8f0384e20cb2d8fe327efe4b8ecde
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Reizen op reis {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Droog je reis"
>abstract="Nadat u de reis hebt ontworpen, voert u een droge run uit om te bevestigen dat deze functioneel is en dat de stappen correct zijn. Met deze publicatiemodus kunt u een reis roken zonder dat u de communicatie naar een profiel hoeft te sturen."

De Reizen van de Dry looppas is een speciale wijze van de reispublicatie in Adobe Journey Optimizer die marketers toestaat om een reis te testen gebruikend echte productiegegevens zonder echte klanten te contacteren of profielinformatie bij te werken.  Met deze functie kunnen marketers vertrouwen winnen in hun doelgericht ontwerp van hun reis en doelgroep voordat ze deze live publiceren.


>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.


## Belangrijkste voordelen {#journey-dry-run-benefits}

Reis Dry-run versterkt het vertrouwen van de arts en het succes van de reis door veilige, gegevensgestuurde tests van klantreizen mogelijk te maken met behulp van echte productiegegevens, zonder het risico van contact met klanten of het wijzigen van profielinformatie. Met deze functie kunnen marketers het bereik van het publiek en de logica van de vertakking valideren voordat ze live gaan, zodat de ritten op de beoogde bedrijfsdoelen zijn afgestemd.

Met de Rondleiding van de Droog van de Reis, kunt u kwesties vroeg identificeren, het richten strategieën optimaliseren, en het reisontwerp verbeteren dat op daadwerkelijke gegevens-geen veronderstellingen wordt gebaseerd. Dry-run is direct geïntegreerd in het reiscanvas en biedt intuïtieve rapportage en zichtbaarheid in belangrijke prestatie-indicatoren, zodat teams betrouwbaar kunnen herhalen en goedkeuringswerkstromen kunnen stroomlijnen. Dit verbetert de operationele efficiëntie, vermindert het opstartrisico en leidt tot betere resultaten van de klantenservice.

Uiteindelijk verbetert deze functie tijd-aan-waarde, vermindert het wegmislukkingen, en versterkt Adobe positie als vertrouwd platform voor het orchestreren van gepersonaliseerde, high-impact reizen.

Op reis is er een droge run:

1. **Veilig testend milieu**: De profielen op Droog looppaswijze worden niet gecontacteerd, die geen risico verzekeren om mededelingen te verzenden of levende gegevens te beïnvloeden.
1. **Inzichten van het publiek**: De handelaars kunnen publieksbereikbaarheid bij diverse vervoerknopen, met inbegrip van opt-outs, uitsluitingen, en andere voorwaarden voorspellen.
1. **in real time terugkoppelt**: De metriek wordt getoond direct in het wegcanvas, gelijkend op levende rapportering, toelatend marketers om hun reisontwerp te verfijnen.

## Een droge run starten {#journey-dry-run-start}

U kunt de functie Dry-run gebruiken in elke conceptreis zonder fouten.

Voer de volgende stappen uit om de droog-uitvoering te activeren:

1. Open de reis die u wilt testen.
1. Klik op de **Droog looppas** knoop.

   ![ Begin de reis droge looppas ](assets/dry-run-button.png)

1. De publicatie bevestigen

   Een statusbericht, **Activerend Dry looppas**, verschijnt terwijl de overgang gebeurt.

1. Als de rit eenmaal is geactiveerd, gaat deze naar de modus Droog.

Tijdens de Dry-run wordt de reis uitgevoerd met de volgende specifieke kenmerken:

* **de actieknooppunten van het Kanaal** met E-mail, SMS of de Duw berichten worden niet uitgevoerd.
* **de acties van de Douane** worden onbruikbaar gemaakt tijdens Droog looppas, en hun reacties worden geplaatst aan ongeldig.
* **wacht knopen** worden overgeslagen tijdens Dry looppas.
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **Externe gegevensbronnen** worden uitgevoerd door gebrek.

>[!NOTE]
>
> * Profielen in de modus Droog worden geteld voor inzetbare profielen.
> * Droge ritten hebben geen invloed op de bedrijfsregels. Een profiel in een droge rit wordt bijvoorbeeld niet uitgesloten van andere ritten vanwege regels zoals `1 journey per day` .

## Een droge run controleren {#journey-dry-monitor}

Zodra de publicatie van de modus Dry is gestart, kunt u de uitvoering van de reis visualiseren en bepalen hoe profielen door de vertakkingen en knooppunten van de rit worden doorlopen.

Metrische gegevens worden direct op het canvas van de reis weergegeven.

![ Monitor de runtime van de reisdroge uitvoering ](assets/dry-run-metrics.png)

Voor elke activiteit kunt u controleren:

* **[!UICONTROL Entered]**: Het totale aantal personen dat deze activiteit heeft ingevoerd.
* **[!UICONTROL Exited (met exit criteria)]**: Het totale aantal personen dat de reis heeft verlaten uit die activiteit, als gevolg van uitstapcriteria.
* **[!UICONTROL Exited (forced exit)]**: Het totale aantal personen dat is vertrokken wanneer de reis is gepauzeerd.
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

Droge ritten moeten handmatig worden stopgezet. Klik de **Dichte** knoop om de test te beëindigen, en te bevestigen.

Na 14 dagen wordt bij Droge ritten automatisch de status Concept gebruikt.
