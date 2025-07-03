---
solution: Journey Optimizer
product: journey optimizer
title: De afstemmingsactiviteit gebruiken
description: Leer hoe u de verzoeningsactiviteit kunt gebruiken in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---

# Afstemming {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Afstemmingsactiviteit"
>abstract="De **Verzoening** activiteit is a **richtend** activiteit die u toestaat om het verband tussen Adobe Journey Optimizer en de gegevens in een het werklijst te bepalen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Selectieveld Afstemmen"
>abstract="Selectieveld Afstemmen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Afstemming maken, voorwaarde"
>abstract="Afstemming maken, voorwaarde"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Afstemming genereren"
>abstract="Afstemming genereren"


+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ krijgen begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Toegang en beheert georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md)<br/><br/>[ creëren en plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ de activiteiten van het Kanaal ](channels.md) - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening <b>[ - ](reconciliation.md)</b> sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

De **[!UICONTROL Reconciliation]** -activiteit is een **[!UICONTROL Targeting]** -activiteit waarmee u de koppeling kunt definiëren tussen de gegevens in Adobe Journey Optimizer en de gegevens in een werktabel, bijvoorbeeld gegevens die uit een extern bestand zijn geladen.

Met de activiteit **[!UICONTROL Enrichment]** kunt u aanvullende gegevens toevoegen aan uw georkestreerde campagne, bijvoorbeeld door gegevens uit meerdere bronnen te combineren of te koppelen aan een tijdelijke bron. De **[!UICONTROL Reconciliation]** -activiteit wordt daarentegen gebruikt om niet-geïdentificeerde of externe gegevens te koppelen aan bestaande bronnen in de database.

**[!UICONTROL Reconciliation]** vereist dat de verwante records al in het systeem bestaan. Als u bijvoorbeeld een aankoopbestand importeert waarin producten, tijdstempels en klantgegevens worden vermeld, moeten zowel de producten als de klanten al aanwezig zijn in de database om de koppeling tot stand te brengen.

## De afstemmingsactiviteit configureren {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Doeldimensie"
>abstract="Selecteer de nieuwe doeldimensie. Met een dimensie kunt u de doelgroep definiëren: ontvangers, abonnees van apps, operators, abonnees, enzovoort. Standaard is de huidige doeldimensie geselecteerd."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Afstemmingsregels"
>abstract="Selecteer afstemmingsregels die u wilt gebruiken voor de deduplicatie. Om attributen te gebruiken, selecteer de **Eenvoudige attributen** optie en kies de bron en bestemmingsgebieden. Om uw eigen verzoeningsvoorwaarde tot stand te brengen gebruikend de vraagmodeler, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie."
>additional-url="https://experienceleague.adobe.com/en/docs/campaign-web/v8/query-database/query-modeler-overview" text="Werken met de querymodelfunctie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Doeldimensie selecteren"
>abstract="Selecteer het richten afmeting voor uw binnenkomende gegevens met elkaar in overeenstemming te brengen."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html#targeting-dimensions" text="Doelafmetingen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Niet-compatibele gegevens behouden"
>abstract="Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werklijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Afstemmingskenmerk"
>abstract="Selecteer het kenmerk dat u wilt gebruiken om gegevens op elkaar af te stemmen en klik op Bevestigen."

Voer de volgende stappen uit om de **[!UICONTROL Reconciliation]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Reconciliation]** activiteit aan uw werkschema toe.

1. Kies een nieuwe doeldimensie om te bepalen wie u richt zoals ontvangers of abonnees.

1. Stel de velden in die u wilt gebruiken om inkomende gegevens af te stemmen op bestaande profielen.

1. Selecteer **[!UICONTROL Simple attributes]** als u gegevens met behulp van basisvelden wilt afstemmen.

1. Stel de overeenkomende velden in:

   * **[!UICONTROL Source]**: geeft een lijst weer van de binnenkomende gegevensvelden.

   * **[!UICONTROL Destination]**: verwijst naar velden in de geselecteerde doeldimensie.

   Er treedt een overeenkomst op wanneer beide waarden gelijk zijn, bijvoorbeeld wanneer **[!UICONTROL Email]** de profielen definieert.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Klik op **[!UICONTROL Add rule]** als u meer overeenkomende regels wilt toevoegen. Er moet aan alle voorwaarden worden voldaan voordat een overeenkomst plaatsvindt.

1. Kies **[!UICONTROL Advanced reconciliation conditions]** voor complexere voorwaarden. Gebruik [ vraagmodeler ](../orchestrated-rule-builder.md) om douanelogica te bepalen.

1. Als u wilt filteren welke gegevens moeten worden afgestemd, klikt u op **[!UICONTROL Create filter]** en definieert u uw voorwaarde in de querymodelfunctie.

1. Door gebrek, worden de niet afgedekte verslagen gehouden in de uitgaande overgang en in de werklijst opgeslagen. Schakel de optie **[!UICONTROL Keep unreconciled data]** in als u deze wilt verwijderen.

## Voorbeeld {#example-reconciliation}

In dit voorbeeld wordt de **[!UICONTROL Reconciliation]** -activiteit in Adobe Journey Optimizer gebruikt om ervoor te zorgen dat e-mails alleen naar herkende klanten worden verzonden. De gegevens lopen door een **[!UICONTROL Read Audience]** -activiteit die gericht is op gebruikers met eerdere bestellingen. De **[!UICONTROL Reconciliation]** -activiteit komt deze inkomende gegevens vervolgens overeen met de bestaande profielen in de database via het e-mailveld.

![](../assets/workflow-reconciliation-sample-1.0.png)
