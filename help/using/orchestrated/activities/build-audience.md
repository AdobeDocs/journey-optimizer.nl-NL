---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de het publieksactiviteit van de Bouwstijl
description: Leer hoe u de gebruikersactiviteit van de Build gebruikt in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# publiek opbouwen {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Activiteit voor publiek opbouwen"
>abstract="**bouwt publieksactiviteit** toestaat u om het publiek te bepalen dat de georkestreerde campagne zal ingaan. Wanneer het verzenden van berichten in de context van een geordende campagne, wordt het berichtpubliek niet bepaald in de kanaalactiviteit, maar in **bouwt publieksactiviteit**."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening [&#128279;](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Als een markeerteken kunt u complexe publiekssegmenten maken via een intuïtieve interface, zodat u gebruikers kunt richten op basis van een groot aantal criteria en gedragingen om uw campagnes effectiever op maat te maken.

Om dit te doen, gebruik **bouwt publiek** richtend activiteit. Deze activiteit bepaalt het publiek dat de georkestreerde campagne ingaat. Wanneer het verzenden van berichten als deel van een georkestreerde campagne, wordt het publiek bepaald in **het publiek van de Bouwstijl** activiteit, niet binnen de georkestreerde campagne.

## Vorm de het publieksactiviteit van de Bouwstijl {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Doelgroep"
>abstract="Selecteer uw publiek, de zelfde manier u een publiek gebruikt wanneer het ontwerpen van een nieuwe levering."

Volg deze stappen om **te vormen bouwen publiek** activiteit:

1. Voeg a **toe bouwt publiek** activiteit.

   ![](../assets/build-audience.png)

1. Definieer een label.

1. Configureer uw publiek door de stappen uit te voeren die in de onderstaande tabbladen worden beschreven.

1. Kies de **het richten afmeting**. Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel geselecteerd bij de ontvangers.

1. Klik **verdergaan**.

1. Gebruik de vraagmodeler om uw vraag te bepalen. [ leer meer over de modelleerling van de Vraag in deze sectie ](../orchestrated-rule-builder.md)

1. Geef op of een uitgaande overgang moet worden gegenereerd wanneer het publiek leeg is.

## Voorbeelden{#build-audience-examples}

Hier is een voorbeeld van een georkestreerde campagne met twee **het publiek van de Bouwstijl** activiteiten. De eerste doelen zijn profielen met items in hun winkelwagentje, gevolgd door een e-maillevering. De tweede richt profielen met een verlanglijst, gevolgd door een levering van SMS.

![](../assets/build-audience-2.png)
