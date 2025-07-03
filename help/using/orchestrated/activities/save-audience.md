---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan in een georkestreerde campagne gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Doelgroep opslaan {#save-audience}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ krijgen begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md)<br/><br/>[ creëren en plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek <b>[ - ](save-audience.md)</b> Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++


De **[!UICONTROL Save audience]** -activiteit is een **[!UICONTROL Targeting]** -activiteit waarmee u een bestaand publiek kunt bijwerken of een nieuw publiek kunt maken van de bevolking die eerder in de georkestreerde campagne is gegenereerd. Wanneer deze doelgroepen zijn gemaakt, worden ze toegevoegd aan de lijst met doelgroepen van toepassingen en zijn ze toegankelijk via het menu **[!UICONTROL Audiences]** .

Deze activiteit is bijzonder nuttig om publiekssegmenten te bewaren die binnen de zelfde georkestreerde campagne worden berekend, die hen ter beschikking stellen voor hergebruik in toekomstige campagnes. Het is doorgaans verbonden met andere doelactiviteiten, zoals **[!UICONTROL Build audience]** of **[!UICONTROL Combine]** , om de resulterende populatie vast te leggen en op te slaan.

## Vorm sparen publieksactiviteit {#save-audience-configuration}

Volg deze stappen om **te vormen sparen publiek** activiteit:

1. Voeg a **sparen publiek** activiteit aan uw georkestreerde campagne toe.

1. Op de **drop-down Wijze**, selecteer de actie u wilt uitvoeren:

   * **creeer of werk een bestaand publiek** bij: Bepaal een **etiket van het Publiek**. Als het publiek reeds bestaat, wordt het bijgewerkt; anders, wordt een nieuw publiek gecreeerd.

   * **werk een bestaand publiek** bij: Kies het **Publiek** u van de lijst van bestaand publiek wilt bijwerken.

1. Selecteer de **wijze van de Update** die op bestaand publiek van toepassing is:

   * **vervang publieksinhoud met nieuwe gegevens**: Alle publieksinhoud wordt vervangen, en het oude gegeven wordt verloren. Slechts worden de gegevens van de binnenkomende overgang van **sparen publiek** activiteit behouden. Met deze optie wist u het publiekstype en de doeldimensie van het bijgewerkte publiek.

   * **Volledig publiek met nieuwe gegevens**: De oude publieksinhoud wordt behouden, en de gegevens van de binnenkomende overgang van **sparen publiek** activiteit wordt toegevoegd aan het.

1. Controle **produceert een uitgaande overgang** optie als u een overgang na **wilt toevoegen sparen publiek** activiteit.

De inhoud van het bewaarde publiek is dan beschikbaar in de detailmening van het publiek, dat van het **Publiek** menu kan worden betreden. De kolommen beschikbaar in deze mening beantwoorden aan de kolommen van de binnenkomende overgang van de georkestreerde campagne **sparen publiek** activiteit.

## Voorbeeld {#save-audience-example}

In het volgende voorbeeld ziet u hoe u een eenvoudige publieksupdate maakt. Een planner voert de georkestreerde campagne eens per maand uit. Met een query worden alle profielen opgehaald die zijn geabonneerd op de verschillende beschikbare toepassingen. **sparen publiek** activiteit werkt het publiek door profielen uit te verwijderen die van de dienst sinds laatste georkestreerde campagneuitvoering hebben afgemeld en onlangs ingetekende profielen toevoegen.
