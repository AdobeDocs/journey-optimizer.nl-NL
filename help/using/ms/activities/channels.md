---
solution: Journey Optimizer
product: journey optimizer
title: Kanaalactiviteit gebruiken
description: Leer hoe u een kanaalactiviteit toevoegt
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# Kanaalactiviteiten {#channel}

Met Adobe Journey Optimizer kunt u marketingcampagnes automatiseren en uitvoeren op binnenkomende en uitgaande kanalen. U kunt kanaalactiviteiten combineren tot het multi-step campagnecanvas om multi-step campagnes over kanalen te creëren die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd. De gesteunde kanalen zijn vermeld in [ deze pagina ](../../channels/gs-channels.md).

U kunt bijvoorbeeld een welkomstcampagne voor e-mail maken met een reeks berichten via verschillende kanalen, zoals e-mail, SMS, push en direct mail. U kunt ook een vervolgbericht verzenden nadat een klant een aankoop heeft voltooid, of een gepersonaliseerd verjaardagsbericht naar een klant verzenden via SMS.

Door kanaalactiviteiten te gebruiken, kunt u uitvoerige en gepersonaliseerde campagnes tot stand brengen die klanten over veelvoudige touchpoints en aandrijvingsomzettingen in dienst nemen.

## Vereisten {#channel-activity-prereq}

Begin met het ontwikkelen van uw meerfasencampagne met de relevante activiteiten:

* Voordat u een kanaalactiviteit invoegt, moet u het publiek definiëren. Het publiek is het belangrijkste doel van uw levering: de profielen die de berichten ontvangen.

* Om een terugkomende levering te verzenden, begin uw multi-step campagne met a **Planner** activiteit. U kunt a **planner** activiteit voor één-ontsproten enige leveringen ook gebruiken om de contactdatum voor die levering te plaatsen. Deze contactdatum kan ook worden ingesteld in de leveringsinstellingen. Zie [deze sectie](scheduler.md).

## De kanaalactiviteit configureren {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="E-mailactiviteit"
>abstract="De e-mailactiviteit vergemakkelijkt het verzenden van e-mail binnen uw werkstroom, die voor zowel eenmalige als terugkomende berichten toestaat. Hiermee wordt het verzenden van e-mails naar een doel dat binnen dezelfde workflow is berekend, geautomatiseerd. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS-activiteit"
>abstract="De activiteit van SMS vergemakkelijkt het verzenden van SMS binnen uw werkschema, die voor zowel eenmalige als terugkomende berichten toestaat. Het dient om het proces te automatiseren om SMS naar een doel te verzenden dat binnen de zelfde werkschema wordt berekend. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="IOS-activiteit in duwen"
>abstract="De Push iOS-activiteit stroomlijnt het proces voor het verzenden van iOS Push-berichten als onderdeel van uw workflow. Hierdoor kunnen eenmalige en terugkerende berichten worden verzonden, waardoor de verzendende iOS Push-berichten naar een vooraf gedefinieerd doel binnen dezelfde workflow worden geautomatiseerd. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Android-activiteit in duwen"
>abstract="De Push Android-activiteit stroomlijnt het proces voor het verzenden van Android Push-berichten als onderdeel van uw workflow. Hierdoor kunnen eenmalige en terugkerende berichten worden verzonden, waardoor de verzendende Android Push-berichten naar een vooraf gedefinieerd doel binnen dezelfde workflow worden geautomatiseerd. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Directe post"
>abstract="De activiteit Direct-mail vergemakkelijkt direct mail verzenden binnen uw werkschema, die voor zowel eenmalige als terugkomende berichten toestaat. Hiermee wordt het genereren van het extractiebestand geautomatiseerd dat is vereist door directe-mailproviders. U kunt kanaalactiviteiten in het werkstroomcanvas combineren om kanaalworkflows te maken die acties op basis van gedrag en gegevens van de klant kunnen activeren."

Volg onderstaande stappen om een levering in te stellen in het kader van een campagne met meerdere stappen:

1. Voeg een kanaalactiviteit toe: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Push notification (Android)]**, **[!UICONTROL Push notification (iOS)]** of **[!UICONTROL Direct mail]** .

1. Selecteer het **Type van levering**: enige of terugkomende.

   * A **Enige levering** is een één-schot levering, slechts eens verzonden, bijvoorbeeld een zwarte Vrijdag e-mail.
   * A **Terugkomende levering** wordt verzonden veelvoudige tijden die op zijn uitvoeringsfrequentie worden gebaseerd die in a [ wordt bepaald planneractiviteit ](scheduler.md). Elke keer dat de campagne in meerdere stappen wordt uitgevoerd, wordt het publiek opnieuw berekend en wordt de levering verzonden naar het bijgewerkte publiek, met de bijgewerkte inhoud. Dit kan bijvoorbeeld een wekelijkse nieuwsbrief of een terugkerende verjaardagsmail zijn.

1. Selecteer een levering **Malplaatje**. Sjablonen zijn vooraf geconfigureerde leveringsinstellingen die specifiek zijn voor een kanaal. Een ingebouwde sjabloon is beschikbaar voor elk kanaal en wordt standaard vooraf ingevuld.

   ![](../assets/delivery-activity-in-wf.png)

   U kunt het malplaatje van de configuratie van de kanaalactiviteit linkerruit selecteren. Als het eerder geselecteerde publiek niet compatibel is met het kanaal, kunt u geen sjabloon selecteren. Om dit op te lossen, werk **het publiek van de Bouwstijl** activiteit bij om een publiek met de correcte doelafbeelding te selecteren.

1. Klik **creeer levering**. Vervolgens kunt u de berichtinstellingen en inhoud op dezelfde manier definiëren als wanneer u een zelfstandige levering maakt. U kunt de inhoud ook testen en simuleren.

1. Ga terug naar uw workflow. Als u uw werkschema wilt voortzetten, knevel **een uitgaande overgang** optie produceren om een overgang na de kanaalactiviteit toe te voegen.

1. Klik **Begin** om uw multi-step campagne te lanceren.

   Door gebrek, leidt het beginnen van een multi-step campagne tot het stadium van de berichtvoorbereiding, zonder onmiddellijk het bericht te verzenden.

1. Open uw kanaalactiviteit om het verzenden van de **Overzicht te bevestigen &amp;** knoop te verzenden.

1. Van uw leveringsdashboard, verzendt de klik ****.

## Voorbeelden {#cross-channel-workflow-sample}

Hier is een meertrapsgewijs campagnevoorbeeld met een segmentatie en twee leveringen. De campagne in meerdere stappen richt zich op alle klanten die in Parijs wonen en die geïnteresseerd zijn in koffiemachines. Onder deze populatie wordt een e-mail verzonden naar de gewone klanten en een SMS-bericht verzonden naar de VIP-klanten.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

U kunt ook een terugkerende multi-step campagne creëren om elke eerste dag van de maand om 20.00 uur een gepersonaliseerd SMS naar alle klanten te verzenden die in Parijs wonen.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
