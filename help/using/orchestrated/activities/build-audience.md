---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de het publieksactiviteit van de Bouwstijl
description: Leer hoe u de gebruikersactiviteit van de Build gebruikt in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '445'
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
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening [&#128279;](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

Als markeerteken kunt u eenvoudig complexe query&#39;s maken met behulp van een gebruikersvriendelijke interface, zodat ik uw publiek kan segmenteren op basis van een groot aantal criteria en gedragingen om uw campagnes effectiever op te stellen.

Om dit uit te voeren, gebruik **bouwt publiek** richtend activiteit. Met deze activiteit kunt u het publiek definiëren dat de georkestreerde campagne zal starten. Wanneer het verzenden van berichten in de context van een geordende campagne, wordt het berichtpubliek niet bepaald in de kanaalactiviteit, maar in **bouwt publieksactiviteit**.

Om de publieksbevolking te bepalen, kunt u:

* Selecteer een bestaand publiek.
* Selecteer een vooraf gedefinieerd filter.
* Bouw een nieuw publiek met de vraagmodeler door het filtreren criteria te bepalen en te combineren.

>[!NOTE]
>
>Publiek dat van een dossier wordt geladen kan niet worden gericht gebruikend een het publieksactiviteit van de Bouwstijl. Om dit te doen, moet u het dossier van de Lading van de a **gebruiken** activiteit die door a **wordt gevolgd Verzoening** activiteit.


## Vorm de het publieksactiviteit van de Bouwstijl {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Doelgroep"
>abstract="Selecteer uw publiek, de zelfde manier u een publiek gebruikt wanneer het ontwerpen van een nieuwe levering."

Volg deze stappen om **te vormen bouwen publiek** activiteit:

![](../assets/build-audience.png)

1. Voeg a **toe bouwt publiek** activiteit.
1. Definieer een label.
1. Bepaal het publiekstype: **creeer uw eigen** of **leest publiek**.
1. Configureer uw publiek door de stappen uit te voeren die in de onderstaande tabbladen worden beschreven.


Voer de volgende stappen uit om uw eigen query te maken:

1. Selecteer **creeer uw (vraag)**.
1. Kies de **het richten afmeting**. Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel geselecteerd bij de ontvangers.
1. Klik **verdergaan**.
1. Gebruik de vraagmodeler om uw vraag te bepalen. [ leer meer over de modelleerling van de Vraag in deze sectie ](../orchestrated-query-modeler.md)

## Voorbeelden{#build-audience-examples}

Hier is een voorbeeld van een georkestreerde campagne met twee **het publiek van de Bouwstijl** activiteiten. De eerste is gericht op het publiek van pokerspelers, gevolgd door een e-mailbezorging. De tweede is gericht op het VIP-publiek, gevolgd door een SMS-levering.

![](../assets/workflow-audience-example.png)
