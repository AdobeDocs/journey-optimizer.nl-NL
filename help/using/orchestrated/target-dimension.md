---
solution: Journey Optimizer
product: journey optimizer
title: Uw doeldimensie maken
description: Leer hoe te om een relationeel schema aan het klantenprofiel in kaart te brengen
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 70d397614dc0e5b5ce94cc4221a28d47dc9b476d
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---


# Een doeldimensie configureren {#configuration}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md)<br/><br/>[ te creëren vormen een dimensie van het Doel ](target-dimension.md) | <b>[ creeer en programma de campagne ](create-orchestrated-campaign.md)</b><br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

In veel gevallen kan één klantprofiel worden gekoppeld aan meerdere gerelateerde entiteiten, zoals abonnementen, servicecontracten of apparaten, elk met zijn eigen unieke id- en communicatiebehoeften.

Met **Geordende Campagnes**, kunt u gerichte mededelingen op het entiteitniveau nu ontwerpen en leveren, gebruikend **mogelijkheden van het relationele schema van Adobe Experience Platform**. Dit staat u toe om, per entiteit in plaats van per ontvanger te segmenteren, te personaliseren en te rapporteren.

## Uw doeldimensie maken {#targeting-dimension}

Eén klantprofiel kan worden gekoppeld aan meerdere gerelateerde entiteiten, zoals contracten, apparaten of abonnementen, elk met een eigen unieke id. Deze opstelling laat u richten, segmenteren, en rapport over elke entiteit individueel.

Begin door campagneorchestratie op te zetten door een relationeel schema aan het klantenprofiel in kaart te brengen.

1. Open vanuit **[!UICONTROL Administration]** het menu **[!UICONTROL Configurations]** en selecteer **[!UICONTROL Campaign Target Dimension]** .

   ![](assets/target-dimension-1.png)

1. Klik op **[!UICONTROL Create]** om uw **[!UICONTROL Targeting dimension]** -bestand te maken.

1. Kies uw [ eerder gevormd Schema ](gs-schemas.md) &#x200B; van drop-down.

1. Selecteer **[!UICONTROL Identity value]** die de entiteit vertegenwoordigt u wilt richten.

   In dit voorbeeld is het klantprofiel gekoppeld aan meerdere abonnementen, die elk worden vertegenwoordigd door een uniek `crmID` in het `Recipient` -schema. Als u **[!UICONTROL Target Dimension]** instelt om het `Recipient` schema en de `crmID` identiteit te gebruiken, kunt u berichten verzenden op abonnementsniveau in plaats van naar het hoofdklantprofiel, zodat elk contract of elke regel een eigen gepersonaliseerd bericht ontvangt.

   [ leer meer in de documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Klik op **[!UICONTROL Save]** om de installatie te voltooien.

Nadat u de **[!UICONTROL Target Dimension]** hebt geconfigureerd, gaat u verder met het maken en instellen van de **[!UICONTROL Channel Configuration]** en het definiëren van de bijbehorende **[!UICONTROL Execution Details]** .

## De kanaalconfiguratie configureren {#channel-configuration}

Nadat u **[!UICONTROL Target Dimension]** hebt ingesteld, moet u uw e-mail of SMS configureren **[!UICONTROL Channel Configuration]** en de juiste instellingen voor **[!UICONTROL Execution Details]** definiëren. Dit zorgt ervoor dat de berichten worden verzonden gebruikend de correcte identiteit en het richten logica.

1. Begin door uw **[!UICONTROL Channel configuration]** te maken en te configureren.

   U kunt ook een bestaande **[!UICONTROL Channel configuration]** bijwerken.

   ➡️ [ volg de stappen die in deze pagina ](../email/surface-personalization.md) worden gedetailleerd

1. Open vanuit de sectie **[!UICONTROL Execution details]** van uw **[!UICONTROL Channel configuration]** de tab **[!UICONTROL Orchestrated campaigns]** .

   ![](assets/target-dimension-3.png)

1. Klik op **[!UICONTROL Enabled]** om deze compatibel te maken met geordende campagnes.

1. Kies uw leveringsmethode:

   * **[!UICONTROL Target Dimension]**: verzenden naar de primaire entiteit, bijvoorbeeld de ontvanger.

   * **[!UICONTROL Target + Secondary Dimension]**: verzenden met zowel primaire als secundaire entiteiten, bijvoorbeeld ontvanger + contract.

1. Selecteer van drop-down uw [ eerder gecreeerd Doel Dimension ](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Kies onder de sectie **[!UICONTROL Execution Address]** welke **[!UICONTROL Source]** moet worden gebruikt om het bezorgadres op te halen, zoals het e-mailadres of telefoonnummer:

   * **[!UICONTROL Profile]**: selecteer deze optie als het bezorgingsadres, bijvoorbeeld e-mail, rechtstreeks in het hoofdprofiel van de klant wordt opgeslagen.

     Nuttig wanneer het verzenden van berichten naar de belangrijkste klant, niet een specifieke bijbehorende entiteit.

   * **[!UICONTROL Target Dimension]**: Kies deze optie als het bezorgadres is opgeslagen in de verwante entiteit, bijvoorbeeld een ontvanger of abonnement.

     Nuttig wanneer elke ontvanger zijn eigen bezorgadres heeft, zoals een ander e-mailadres of telefoonnummer.

1. Van het **[!UICONTROL Delivery address]** gebied, klik ![ geef pictogram ](assets/do-not-localize/edit.svg) uit om het specifieke gebied te kiezen voor uw berichtlevering te gebruiken.

   ![](assets/target-dimension-4.png)

1. Klik op **[!UICONTROL Submit]** wanneer dit is geconfigureerd.

Uw kanaal is nu klaar om met Geordende Campagnes te gebruiken, en de berichten zullen volgens de geselecteerde doeldimensie worden geleverd.
