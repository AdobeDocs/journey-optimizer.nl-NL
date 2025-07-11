---
solution: Journey Optimizer
product: journey optimizer
title: Gestroomlijnde campagnes met Adobe Journey Optimizer starten en volgen
description: Leer hoe u georkestreerde campagnes met Adobe Journey Optimizer kunt starten en volgen.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: b1bee7a5ee05e0e535a982c31bafafdc760d21ae
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opnieuw gerichte query&#39;s maken {#retarget}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/><b>[ opnieuw op ](retarget.md)</b> | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Documentatie in uitvoering

>[!ENDSHADEBOX]

Met Opnieuw toewijzen kunt u op basis van de manier waarop ze op een vorige georkestreerde campagne hebben gereageerd, een follow-up geven aan de ontvangers. U kunt bijvoorbeeld een tweede e-mail verzenden naar profielen die wel een tweede e-mail hebben ontvangen maar niet op de eerste hebben geklikt.

**[!UICONTROL Orchestrated Campaign]** biedt hiervoor twee belangrijke gegevensbronnen:

* **[!UICONTROL Message Feedback]**: legt gebeurtenissen vast die betrekking hebben op de levering, zoals verzonden, geopend, teruggestuurd, enz. bericht.
* **[!UICONTROL Email Tracking]**: legt gebruikersacties vast, bijvoorbeeld klikken en openen.

## Een regel voor opnieuw toewijzen op basis van feedback maken {#feedback-retarget}

De op feedback-Gebaseerde Terugkomende Regel staat u toe om ontvangers opnieuw te richten die op de gebeurtenissen worden gebaseerd van de berichtlevering in de **Terugkoppeling van het Bericht** dataset wordt gevangen. Deze gebeurtenissen omvatten uitkomsten zoals berichten die worden verzonden, geopend, teruggestuurd of gemarkeerd als spam.

Gebruikend deze gegevens, kunt u regels bepalen om ontvangers te identificeren die een vorig bericht ontvingen toelatend follow-upmededeling die op specifieke leveringsstatussen wordt gebaseerd.

1. Maak een nieuwe **[!UICONTROL Orchestrated Campaign]** .

1. Voeg een **[!UICONTROL Build Audience]** -activiteit toe en stel de doeldimensie in op **[!UICONTROL Recipient (caas)]** .

1. Klik in de **[!UICONTROL Rule Builder]** op **[!UICONTROL Add Condition]** en selecteer **[!UICONTROL Message Feedback]** in de **[!UICONTROL Attributes Picker]** . Klik **[!UICONTROL Confirm]** om de Terugkoppeling van het a **Bericht tot stand te brengen bestaat zoals** voorwaarde.

   ![](assets/retarget_1.png)

1. Kies het kenmerk **[!UICONTROL Feedback Status]** om gebeurtenissen voor berichtlevering als doel in te stellen.

+++ Gedetailleerd, stap voor stap

   1. Voeg een andere voorwaarde toe die is gekoppeld aan het kenmerk **[!UICONTROL Message feedback]** .

   1. Zoek het kenmerk **[!UICONTROL Feedback Status]** en klik op **[!UICONTROL Confirm]** .

      ![](assets/retarget_3.png)

   1. Kies in het menu **[!UICONTROL Custom condition]** welke leveringsstatus u wilt bijhouden in de vervolgkeuzelijst **[!UICONTROL Value]** .

      ![](assets/retarget_4.png)

+++

1. Kies het kenmerk **[!UICONTROL Orchestrated Campaign Name]** om een specifieke georkestreerde campagne als doel in te stellen.

+++ Gedetailleerd, stap voor stap

   1. Voeg een andere voorwaarde toe die is gekoppeld aan het kenmerk **[!UICONTROL Message feedback]** , zoek naar **[!UICONTROL entity]** en navigeer naar:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Selecteer **[!UICONTROL Orchestrated Campaign Name]**.

      ![](assets/retarget_5.png)

   1. Geef in het menu **[!UICONTROL Custom condition]** de naam van de campagne op in het veld **[!UICONTROL Value]** .

+++

1. Kies het kenmerk **[!UICONTROL Orchestrated Campaign Action Name]** om een specifiek bericht of een specifieke activiteit in een geordende campagne als doel in te stellen.

+++ Gedetailleerd, stap voor stap

   1. Voeg een andere voorwaarde toe die is gekoppeld aan het kenmerk **[!UICONTROL Message feedback]** , zoek naar **[!UICONTROL entity]** en navigeer naar:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Selecteer **[!UICONTROL Orchestrated Campaign Action Name]**.

      ![](assets/retarget_6.png)

   1. Geef in het menu **[!UICONTROL Custom condition]** de naam van de actie voor de campagne op in het veld **[!UICONTROL Value]** .

      De namen van de acties kunnen worden gevonden door het ![ pictogram van de Informatie ](assets/do-not-localize/info-icon.svg) naast een activiteit in het canvas te klikken.

   ++

1. U kunt ook filteren op **[!UICONTROL Campaign ID]** (UUID), die u vindt in de campagneeigenschappen.

## Een op reeksspatiëring gebaseerde herrichtingsregel maken

Het volgen-Gebaseerde opnieuw richten van regel richt ontvangers die op hun interactie met een bericht worden gebaseerd, gebruikend gegevens van de **[!UICONTROL Email Tracking]** dataset. Hiermee worden gebruikersacties vastgelegd, zoals het openen van e-mail en het klikken op koppelingen.

Gebruik de entiteit **[!UICONTROL Email Tracking]** als volgt om ontvangers opnieuw te richten op basis van berichtinteractie (bijvoorbeeld openen of klikken):

1. Maak een nieuwe **[!UICONTROL Orchestrated Campaign]** .

1. Voeg een **[!UICONTROL Build Audience]** -activiteit toe en stel de doeldimensie in op **[!UICONTROL Recipient (caas)]** om de focus op vorige georkestreerde campagneontvangers te richten.

1. Klik in de **[!UICONTROL Rule Builder]** op **[!UICONTROL Add Condition]** en selecteer **[!UICONTROL Email Tracking]** in de **[!UICONTROL Attributes Picker]** .

   Klik **[!UICONTROL Confirm]** om a **E-mail het Volgen tot stand te brengen bestaat zoals** voorwaarde.

   ![](assets/retarget_2.png)

1. Als u de interactie van profielen met een bericht wilt aanwijzen, voegt u een andere voorwaarde toe die is gekoppeld aan het kenmerk **[!UICONTROL Email tracking]** en zoekt u het kenmerk **[!UICONTROL Interaction Type]** .

   ![](assets/retarget_7.png)

1. Gebruik in de opties voor aangepaste voorwaarden **[!UICONTROL Included in]** als de operator en selecteer een of meer waarden, afhankelijk van het gebruikte hoofdlettergebruik, bijvoorbeeld **[!UICONTROL Message Opened]** of **[!UICONTROL Message Link Clicked]** .

   ![](assets/retarget_8.png)

1. Om de volgende gegevens aan een specifieke campagne te associëren, voeg een nieuwe **[!UICONTROL Message feedback]** voorwaarde toe en volg de stappen die [ in deze sectie ](#feedback-retarget) worden gedetailleerd.
