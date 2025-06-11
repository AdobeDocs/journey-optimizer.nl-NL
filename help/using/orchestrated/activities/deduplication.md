---
solution: Journey Optimizer
product: journey optimizer
title: De deduplicatieactiviteit gebruiken
description: Leer hoe u de deduplicatieactiviteit gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

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
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening ](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

De **Deduplicatie** activiteit is a **richtend** activiteit. Met deze activiteit kunt u duplicaten verwijderen uit het resultaat of de resultaten van de binnenkomende activiteiten, bijvoorbeeld gedupliceerde profielen in de lijst met ontvangers. De **Deduplicatie** activiteit wordt over het algemeen gebruikt na het richten van activiteiten, en vóór activiteiten die het gebruik van gerichte gegevens toestaan.

## De deduplicatieactiviteit configureren{#deduplication-configuration}

Voer de volgende stappen uit om de **Deduplication** -activiteit te configureren:


1. Voeg a **activiteit 0} Deduplicatie {aan uw geordende campagne toe.**

1. In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt.

![](../assets/deduplication-1.png)

1. In de **sectie van de Montages van de Deduplicatie**, kies hoeveel unieke verslagen om het gebruiken van Duplicaten te houden om gebied te houden. De standaardwaarde is 1, die één record per gedupliceerde groep bijhoudt. Stel de waarde in op 0 om alle duplicaten te behouden.

   Bijvoorbeeld als de records A en B duplicaten van Y zijn en record C een duplicaat van Z is:

   * **als de waarde van het gebied 1** is: Slechts worden de verslagen van Y en van Z bewaard.
   * **als de waarde van het gebied 0** is: Alle verslagen (A, B, C, Y, Z) worden gehouden.
   * **als de waarde van het gebied 2** is: C en Z worden gehouden, plus twee waarden van A, B, en Y, willekeurig of gebaseerd op uw deduplicatiemethode.

1. Kies de Methode van de a **Deduplicatie**, bepaalt dit hoe het systeem besluit welke verslagen van elke groep duplicaten te houden:

   * **Willekeurige selectie**: Selecteert willekeurig het verslag dat uit de duplicaten moet worden gehouden.
   * **Gebruikend een uitdrukking**: Houdt verslagen met de hoogste of laagste die waarde op een uitdrukking wordt gebaseerd u bepaalt.
   * **Niet-lege waarden**: Houdt verslagen waar het geselecteerde gebied niet leeg is, b.v. houd slechts profielen met een telefoonaantal.
   * **na een lijst van waarden**: Staat u toe om specifieke waarden voor één of meerdere gebieden voorrang te geven, b.v. kunt u prioriteit aan verslagen met &quot;Land&quot;geven dat aan Frankrijk wordt geplaatst. Klik **Attribuut** om een gebied te kiezen of een douaneuitdrukking tot stand te brengen. Gebruik **toevoegen knoop** om aangewezen waarden in de prioritaire orde in te gaan.

   ![](../assets/deduplication-2.png)

1. Controleer **aanvult** optie als u wenst om de resterende bevolking uit te buiten. Het complement bestaat uit alle duplicaten. Er wordt dan een aanvullende overgang toegevoegd aan de activiteit.

## Voorbeeld{#deduplication-example}

In het volgende voorbeeld, wordt de activiteit van de a **Deduplicatie** gebruikt om dubbele verslagen uit het doelpubliek te verwijderen alvorens een levering te verzenden. Het publiek wordt eerst gefilterd en worden alleen profielen met een niet-leeg veld E-mail opgenomen. Dan, gebruikt de **Deduplicatie** activiteit het E-mailadres om duplicaten te identificeren en uit te sluiten.

![](../assets/deduplication-3.png)
