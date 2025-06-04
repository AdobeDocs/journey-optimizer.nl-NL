---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit Splitsen gebruiken
description: Leer hoe u de activiteit Splitsen gebruikt in een geordende campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 0%

---

# Splitsen {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Gesplitste activiteit"
>abstract="De **Gesplitste** activiteit staat u toe om inkomende populaties in veelvoudige subsets te segmenteren die op verschillende selectiecriteria, zoals het filtreren regels of populatiegrootte worden gebaseerd."

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](send-messages.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de Vraag Modeler ](orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uitdrukkingen ](edit-expressions.md) uit | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ combineert ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) - [ Fork ](activities/fork.md) opnieuw verzoening ](activities/reconciliation.md) - [ Gesplitst ](activities/split.md) - [ wacht ](activities/wait.md)[ |

{style="table-layout:fixed"}

+++

<br/><br/>

De **Gesplitste** activiteit is a **richtend** activiteit die u toestaat om inkomende populaties in veelvoudige subsets te segmenteren die op verschillende selectiecriteria, zoals het filtreren regels of bevolkingsgrootte worden gebaseerd.

## De activiteit Splitsen configureren {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmenten voor splitsingsactiviteit"
>abstract="Voeg zoveel subsets toe als u wilt om de binnenkomende populatie te segmenteren.<br/></br> wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gesegmenteerd over de verschillende ondergroepen in de orde zij aan de activiteit worden toegevoegd. Voordat u de georkestreerde campagne start, moet u de subsets met de pijlknoppen in de gewenste volgorde plaatsen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Activiteitsfilter splitsen"
>abstract="Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en configureert u de gewenste filterregel met de querymodelfunctie. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Limiet voor gesplitste activiteit"
>abstract="Als u het aantal profielen wilt beperken dat door de subset wordt geselecteerd, schakelt u de optie **[!UICONTROL Enable limit]** in en geeft u het aantal of de percentages van de populatie op die u wilt opnemen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Splitsen op activiteit"
>abstract="Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Om dit te doen, knevel op **het sorteren** optie toe. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Splitsen genereert complement"
>abstract="Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Om dit te doen, op **van een knevel te voorzien produceert complement** optie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Alle subsets in dezelfde tabel genereren"
>abstract="Schakel deze optie in en uit om alle subsets te groeperen in één uitvoerovergang."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Lege overgang overslaan"
>abstract="Schakel de optie **[!UICONTROL Skip empty transition]** in en uit om de uitvoerovergang voor deze subset uit te schakelen als de binnenkomende populatie leeg is."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Overlappende uitvoerpopulaties inschakelen"
>abstract=" Met de optie **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren. Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria. Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria."

Volg deze stappen om de **Gesplitste** activiteit te vormen:

1. Voeg a **Gesplitste** activiteit aan uw geordende campagne toe.

1. Het deelvenster voor activiteitenconfiguratie wordt geopend met een standaardsubset. Klik **toevoegen segment** knoop om zo vele ondergroepen toe te voegen zoals gewenst om de inkomende bevolking te segmenteren.

   ![](../assets/workflow-split.png)

   >[!IMPORTANT]
   >
   >Wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gesegmenteerd over de verschillende ondergroepen in de orde zij aan de activiteit worden toegevoegd. Als de eerste subset bijvoorbeeld 70% van de oorspronkelijke populatie herstelt, past de volgende toegevoegde subset zijn selectiecriteria alleen toe op de resterende 30%, enzovoort.
   >
   >Voordat u de georkestreerde campagne start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst. Hiervoor gebruikt u de pijlknoppen om de positie van een subset te wijzigen.

1. Nadat subsets zijn toegevoegd, toont de activiteit evenveel uitvoerovergangen als er subsets zijn. We raden u ten zeerste aan het label van elke subset te wijzigen om deze gemakkelijk te identificeren in het georkestreerde campagneccanvas.

1. Vorm hoe elke ondergroep de inkomende bevolking zou moeten filtreren. Ga als volgt te werk om dit te doen:

   1. Open de subset om de eigenschappen ervan weer te geven.

   1. Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en configureert u de gewenste filterregel met de querymodelfunctie. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database.

   1. Als u het aantal profielen wilt beperken dat door de subset wordt geselecteerd, schakelt u de optie **[!UICONTROL Enable limit]** in en geeft u het aantal of de percentages van de populatie op die u wilt opnemen.

   1. Als u een overgang wilt uitschakelen als de binnenkomende populatie leeg is, schakelt u de optie **[!UICONTROL Skip empty transition]** in of uit. Als geen profiel overeenkomt met de subset, gaat de georkestreerde campagne niet over naar de volgende activiteit.

      ![](../assets/workflow-split-subset.png)

1. Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Schakel hiertoe de optie **[!UICONTROL Generate complement]** in.

   ![](../assets/workflow-split-complement.png)

   >[!NOTE]
   >
   >Met de optie **[!UICONTROL Generate all subsets in the same table]** kunt u alle subsets groeperen in één uitvoerovergang.

1. Met de optie **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren:

   * Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria.
   * Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria. De beste manier is om exclusieve criteria te hanteren.

De activiteit wordt nu gevormd. Bij de uitvoering van de georkestreerde campagne wordt de bevolking opgedeeld in de verschillende ondergroepen, in de volgorde waarin ze aan de activiteit zijn toegevoegd.

## Voorbeeld{#split-example}

In het volgende voorbeeld wordt de activiteit **[!UICONTROL Split]** gebruikt om een publiek in verschillende subsets te segmenteren op basis van het communicatiekanaal dat we willen gebruiken:

* **Subset 1 &quot;duw&quot;**: Deze ondergroep omvat alle profielen die onze mobiele toepassing hebben geïnstalleerd.
* **Subset 2 &quot;sms&quot;**: De mobiele telefoongebruikers: Voor de resterende bevolking die niet in Subset 1 viel, past subset 2 een het filtreren regel toe om profielen met mobiele telefoons in het gegevensbestand te selecteren.
* **Complementeer overgang**: Deze overgang vangt alle resterende profielen die Subset 1 of Subset 2 niet aanstemden. Het bevat met name profielen die de mobiele toepassing niet hebben geïnstalleerd en geen mobiele telefoon hebben, zoals gebruikers die de mobiele app niet hebben geïnstalleerd of die geen geregistreerd mobiel nummer hebben.

![](../assets/workflow-split-example.png)
