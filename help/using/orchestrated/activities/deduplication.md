---
solution: Journey Optimizer
product: journey optimizer
title: De deduplicatieactiviteit gebruiken
description: Leer hoe u de deduplicatieactiviteit gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 15%

---

# Deduplicatie {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Velden om duplicaten te identificeren"
>abstract="In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Deduplicatieactiviteit"
>abstract="De **Deduplicatie** activiteit staat u toe om duplicaten in de resultaten van de binnenkomende activiteiten te schrappen. Het wordt meestal gebruikt na doelgerichte activiteiten en vóór activiteiten die het gebruik van gerichte gegevens mogelijk maken."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, op **van een knevel voorzien produceer complement** optie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Instellingen voor deduplicatie"
>abstract="Als u duplicaten van binnenkomende gegevens wilt verwijderen, definieert u de deduplicatiemethode in de onderstaande velden. Standaard wordt slechts één record bewaard. U moet ook de deduplicatiemodus selecteren op basis van een expressie of een kenmerk. Standaard wordt de record die buiten de duplicaten moet blijven, willekeurig geselecteerd."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening [&#128279;](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

De **Deduplicatie** activiteit is a **richtend** activiteit. Met deze activiteit kunt u duplicaten verwijderen uit het resultaat of de resultaten van de binnenkomende activiteiten, bijvoorbeeld gedupliceerde profielen in de lijst met ontvangers. De **Deduplicatie** activiteit wordt over het algemeen gebruikt na het richten van activiteiten, en vóór activiteiten die het gebruik van gerichte gegevens toestaan.

## De deduplicatieactiviteit configureren{#deduplication-configuration}

Voer de volgende stappen uit om de **Deduplication** -activiteit te configureren:

![](../assets/workflow-deduplication.png)

1. Voeg a **activiteit 0&rbrace; Deduplicatie &lbrace;aan uw geordende campagne toe.**

1. In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt.

1. In de **montages van de Deduplicatie** sectie, selecteer het aantal unieke **Duplicaten om** te houden. De standaardwaarde voor dit veld is 1. Met de waarde 0 kunt u alle duplicaten behouden.

   Stel bijvoorbeeld dat records A en B worden beschouwd als duplicaten van record Y en dat een record C wordt beschouwd als duplicaat van record Z:

   * Als de waarde van het veld 1 is: alleen de records Y en Z blijven behouden.
   * Als de waarde van het veld 0 is: alle records blijven behouden.
   * Als de waarde van het veld 2 is: de records C en Z blijven behouden en twee records van A, B en Y blijven behouden, bij toeval of afhankelijk van de daarna geselecteerde deduplicatiemethode.

1. Selecteer de **methode van de Deduplicatie** aan gebruik:

   * **Willekeurige selectie**: Selecteert willekeurig het verslag dat uit de duplicaten moet worden gehouden.
   * **Gebruikend een uitdrukking**: Behoud de verslagen waarin de waarde van de ingevoerde uitdrukking de kleinste of grootste is.
   * **Niet-lege waarden**: houd de verslagen waarvoor de uitdrukking niet leeg is.
   * **na een lijst van waarden**: Bepaal een waardeprioriteit voor één of meerdere gebieden. Om de waarden te bepalen, klik **Attribuut** om een gebied te selecteren of een uitdrukking tot stand te brengen, dan voeg de waarde(n) in de aangewezen lijst toe. Om een nieuw gebied te bepalen, klik **toevoegen knoop** boven de lijst van waarden wordt gevestigd die.

1. Controleer **aanvult** optie als u wenst om de resterende bevolking uit te buiten. Het complement bestaat uit alle duplicaten. Er wordt dan een aanvullende overgang toegevoegd aan de activiteit.

## Voorbeeld{#deduplication-example}

In het volgende voorbeeld gebruikt u een deduplicatie-activiteit om duplicaten uit te sluiten van het doel voordat u een levering verzendt. De geïdentificeerde gedupliceerde profielen worden toegevoegd aan een specifiek publiek dat indien nodig opnieuw kan worden gebruikt. Kies het **E-mail** adres om de duplicaten te identificeren. Houd 1 ingang en selecteer de **Willekeurige** deduplicatiemethode.

![](../assets/workflow-deduplication-example.png)
