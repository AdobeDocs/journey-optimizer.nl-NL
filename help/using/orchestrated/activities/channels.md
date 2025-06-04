---
solution: Journey Optimizer
product: journey optimizer
title: Een kanaalactiviteit toevoegen aan een campagne met meerdere stappen
description: Leer hoe u een kanaalactiviteit toevoegt aan een campagne die uit meerdere stappen bestaat
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 9606ca5710e6f91159474d76f68cdcbc2128b000
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Kanaalactiviteiten {#channel}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/>[ verzenden berichten met georkestreerde campagnes ](../send-messages.md)<br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-query-modeler.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - [ combineert ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) - [ Fork ](fork.md) opnieuw verzoening ](reconciliation.md) - [ Gesplitst ](split.md) - [ wacht ](wait.md)[ |

{style="table-layout:fixed"}

+++

<br/>

Met Adobe Journey Optimizer kunt u marketingcampagnes automatiseren en uitvoeren op binnenkomende en uitgaande kanalen. U kunt kanaalactiviteiten in het georkestreerde campagnecanvas combineren om kanaalgeorkestreerde campagnes tot stand te brengen die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd. De gesteunde kanalen zijn vermeld op [ deze pagina ](../../channels/gs-channels.md).

U kunt bijvoorbeeld een welkomstcampagne voor e-mail maken met een reeks berichten via verschillende kanalen, zoals e-mail, SMS, push en direct mail. U kunt ook een vervolgbericht verzenden nadat een klant een aankoop heeft voltooid, of een gepersonaliseerd verjaardagsbericht naar een klant verzenden via SMS.

Door kanaalactiviteiten te gebruiken, kunt u uitvoerige en gepersonaliseerde campagnes tot stand brengen die klanten over veelvoudige touchpoints en aandrijvingsomzettingen in dienst nemen.

## Vereisten {#channel-activity-prereq}

Begin uw georkestreerde campagne met de relevante activiteiten te bouwen:

* Voordat u een kanaalactiviteit invoegt, moet u het publiek definiëren. Het publiek is het belangrijkste doel van uw levering: de profielen die de berichten ontvangen.

* Om een terugkomende levering te verzenden, begin uw georkestreerde campagne met a **Planner** activiteit. U kunt a **planner** activiteit voor één-ontsproten enige leveringen ook gebruiken om de contactdatum voor die levering te plaatsen. Deze contactdatum kan ook worden ingesteld in de leveringsinstellingen.

## Een kanaalactiviteit configureren {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="E-mailactiviteit"
>abstract="Met de e-mailactiviteit kunt u e-mails verzenden in uw meerstapscampagne, zowel voor eenmalige als voor terugkerende berichten. Hiermee wordt het proces geautomatiseerd waarbij e-mails worden verzonden naar een doel dat is berekend in dezelfde meerstapscampagne. U kunt kanaalactiviteiten combineren tot een uit meerdere stappen bestaand campagnecanvas om kanaalcampagnes te maken die acties op klantengedrag en gegevens kunnen teweegbrengen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS-activiteit"
>abstract="Met de SMS-activiteit kunt u SMS verzenden binnen uw campagne met meerdere stappen, voor zowel eenmalige als terugkerende berichten. Het dient om het proces te automatiseren om SMS naar een doel te verzenden dat binnen de zelfde multistep campagne wordt berekend. U kunt kanaalactiviteiten combineren tot het campagnecanvas met meerdere stappen om kanaalcampagnes te maken die acties kunnen activeren op basis van het gedrag en de gegevens van de klant."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="IOS-activiteit in duwen"
>abstract="Met de Push iOS-activiteit kunt u iOS Push-berichten verzenden als onderdeel van uw meerstapscampagne. Het maakt het mogelijk om zowel eenmalige als terugkerende meerstapscampagnes uit te voeren, waarbij de verzendende iOS Push-berichten worden geautomatiseerd naar een vooraf gedefinieerd doel binnen dezelfde workflow. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Android-activiteit in duwen"
>abstract="Met het activity ket Push Android verzendt u Android Push-berichten als onderdeel van uw campagne met meerdere stappen. Het laat de levering van zowel eenmalige als terugkomende berichten toe, die de verzendende Push berichten van Android aan een vooraf bepaald doel binnen de zelfde multi-step campagne automatiseren. U kunt kanaalactiviteiten combineren tot het campagnecanvas met meerdere stappen om kanaalcampagnes te maken die acties kunnen activeren op basis van het gedrag en de gegevens van de klant."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Directe post"
>abstract="De direct-mailactiviteit vergemakkelijkt direct mail verzenden binnen uw multi-step campagne, voor zowel eenmalige als terugkomende berichten. Hiermee wordt het genereren van het extractiebestand geautomatiseerd dat is vereist door directe-mailproviders. U kunt kanaalactiviteiten combineren tot het campagnecanvas met meerdere stappen om kanaalcampagnes te maken die acties kunnen activeren op basis van het gedrag en de gegevens van de klant."

Volg onderstaande stappen om een levering in te stellen in het kader van een georkestreerde campagne:

1. Voeg een kanaalactiviteit toe: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Push notification (Android)]**, **[!UICONTROL Push notification (iOS)]** of **[!UICONTROL Direct mail]** .

1. Selecteer het **Type van levering**: enige of terugkomende.

   * A **Enige levering** is een één-schot levering, slechts eens verzonden, bijvoorbeeld een zwarte Vrijdag e-mail.
   * A **Terugkomende levering** wordt verzonden veelvoudige tijden die op zijn uitvoeringsfrequentie worden gebaseerd. Elke keer dat de georkestreerde campagne wordt uitgevoerd, wordt het publiek opnieuw berekend en wordt de levering verzonden naar het bijgewerkte publiek, met de bijgewerkte inhoud. Dit kan bijvoorbeeld een wekelijkse nieuwsbrief of een terugkerende verjaardagsmail zijn.

1. Selecteer een levering **Malplaatje**. Sjablonen zijn vooraf geconfigureerde leveringsinstellingen die specifiek zijn voor een kanaal. Een ingebouwde sjabloon is beschikbaar voor elk kanaal en wordt standaard vooraf ingevuld.

   ![](../assets/delivery-activity-in-wf.png)

   U kunt het malplaatje van de configuratie van de kanaalactiviteit linkerruit selecteren. Als het eerder geselecteerde publiek niet compatibel is met het kanaal, kunt u geen sjabloon selecteren. Om dit op te lossen, werk **het publiek van de Bouwstijl** activiteit bij om een publiek met de correcte doelafbeelding te selecteren.

1. Klik **creeer levering**. Vervolgens kunt u de berichtinstellingen en inhoud op dezelfde manier definiëren als wanneer u een zelfstandige levering maakt. U kunt de inhoud ook testen en simuleren.

1. Ga terug naar uw workflow. Als u uw werkschema wilt voortzetten, knevel **een uitgaande overgang** optie produceren om een overgang na de kanaalactiviteit toe te voegen.

1. Klik **Begin** om uw georkestreerde campagne te lanceren.

   Door gebrek, leidt het beginnen van een geordende campagne tot de fase van de berichtvoorbereiding, zonder onmiddellijk het bericht te verzenden.

1. Open uw kanaalactiviteit om het verzenden van de **Overzicht te bevestigen &amp;** knoop te verzenden.

1. Van uw leveringsdashboard, verzendt de klik ****.

## Voorbeelden {#cross-channel-workflow-sample}

Hier is een kanaalgeorkestreerd campagnevoorbeeld met een segmentatie en twee leveringen. De georkestreerde campagne richt zich op alle klanten die in Parijs wonen en die geïnteresseerd zijn in koffiemachines. Onder deze populatie wordt een e-mail verzonden naar de gewone klanten en een SMS-bericht verzonden naar de VIP-klanten.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

U kunt ook een terugkerende georkestreerde campagne maken om elke eerste dag van de maand om 20.00 uur een gepersonaliseerd sms naar alle klanten in Parijs te sturen.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
