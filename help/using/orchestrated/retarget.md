---
solution: Journey Optimizer
product: journey optimizer
title: Gestroomlijnde campagnes met Adobe Journey Optimizer starten en volgen
description: Leer hoe u georkestreerde campagnes met Adobe Journey Optimizer kunt starten en volgen.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
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

De geordende campagne verstrekt twee belangrijkste gegevensbronnen voor dit:

- **Feedback van het Bericht**: vangt op levering betrekking hebbende gebeurtenissen, b.v. verzonden bericht, geopend, teruggestuurd, enz.

- **E-mail die** volgen: vangt gebruikersacties b.v. klikt en opent.

## Een regel voor opnieuw toewijzen op basis van feedback maken

De op feedback-Gebaseerde Terugkomende Regel staat u toe om ontvangers opnieuw te richten die op de gebeurtenissen worden gebaseerd van de berichtlevering in de **Terugkoppeling van het Bericht** dataset wordt gevangen. Deze gebeurtenissen omvatten uitkomsten zoals berichten die worden verzonden, geopend, teruggestuurd of gemarkeerd als spam.

Gebruikend deze gegevens, kunt u regels bepalen om ontvangers te identificeren die een vorig bericht maar niet met het in dienst genomen, toelatend follow-upmededeling die op specifieke leveringsstatussen wordt gebaseerd.

1. Creeer een nieuwe **Geordende Campagne**.

2. Voeg a **toe bouwt de activiteit van het publiek** en plaatst de het richten dimensie aan **Ontvanger (caas)**.

3. In de **Bouwer van de Regel**, klik **Voorwaarde** toevoegen en selecteer **Terugkoppeling van het Bericht** van de Plukker van Attributen. Klik **bevestigen**.

4. Voeg een voorwaarde voor **Status van de Terugkoppeling** toe en plaats de waarde aan **Verstuurd Bericht**.

5. Een specifieke georkestreerde campagne als doel instellen:

   - Voeg nog een voorwaarde toe, zoek naar `entity` en navigeer naar:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selecteer **Geordende Naam van de Campagne** en specificeer de campagnenaam.

6. Om een specifiek bericht of een activiteit binnen die georkestreerde campagne te richten:

   - Voeg nog een voorwaarde toe, zoek naar `entity` en navigeer naar:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selecteer **Geordende Naam van de Actie van de Campagne** en specificeer de naam van de campagneactie.

     De namen van de acties kunnen worden gevonden door het ![ pictogram van de Informatie ](assets/do-not-localize/info-icon.svg) naast een activiteit in het canvas te klikken.

   >[!TIP]
   >
   >In plaats van het gebruiken van namen, kunt u door **identiteitskaart van de Campagne** (UUID) ook filtreren, die in uw eigenschappen van de Campagne kan worden gevonden.

## Een op reeksspatiëring gebaseerde herrichtingsregel maken

Het volgen-Gebaseerde opnieuw richten van regel richt ontvangers die op hun interactie met een bericht worden gebaseerd, gebruikend gegevens van de **E-mail die** dataset volgen. Hiermee worden gebruikersacties vastgelegd, zoals het openen van e-mail en het klikken op koppelingen.

Om ontvangers opnieuw te richten die op berichtinteractie (b.v., open of klik) worden gebaseerd, gebruik de **E-mail die** entiteit volgen als volgt:

1. Creeer een nieuwe **Geordende Campagne**, dan voeg a **toe 3} activiteit van het publiek van de Bouwstijl {met** Ontvanger (camera&#39;s) **als het richten dimensie om zich op vorige georkestreerde campagneontvangers te concentreren.**

1. Voeg een nieuwe voorwaarde voor **E-mail het Volgen** toe. Klik **bevestigen** om tot &quot;E-mail het Volgen zoals&quot;voorwaarde te leiden bestaat.

1. Binnen die voorwaarde, voeg een voorwaarde toe en onderzoek naar **het Type van Interactie** attributen.

1. Van de opties van de douanevoorwaarde, gebruik **inbegrepen in** als exploitant en selecteer één of meerdere waarden afhankelijk van uw gebruiksgeval. Bijvoorbeeld:
   - **Geopend Bericht**
   - **Geklikte Verbinding van het Bericht**

1. De volgende gegevens aan een specifieke campagne koppelen:

   - Voeg een voorwaarde toe in het blok E-mailtracking.

   - Navigeer naar `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign` .

   - Voeg voorwaarden voor zowel **Geordende Naam van de Campagne** toe en, indien nodig, **Geordende Naam van de Actie van de Campagne**.

     De namen van de acties kunnen worden gevonden door het ![ pictogram van de Informatie ](assets/do-not-localize/info-icon.svg) naast een activiteit in het canvas te klikken.

   >[!TIP]
   >
   >In plaats van het gebruiken van namen, kunt u door **identiteitskaart van de Campagne** (UUID) ook filtreren, die in uw eigenschappen van de Campagne kan worden gevonden.
