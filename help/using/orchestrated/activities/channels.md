---
solution: Journey Optimizer
product: journey optimizer
title: Een kanaalactiviteit toevoegen aan een campagne met meerdere stappen
description: Leer hoe u een kanaalactiviteit toevoegt aan een campagne die uit meerdere stappen bestaat
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 85d322e5855c6e658a3a93dc0f3d644ef79437b5
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Kanaalactiviteiten {#channel}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ worden begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](../configuration-steps.md)<br/><br/>[ Zeer belangrijke stappen voor georkestreerde campagneverwezenlijking ](../gs-campaign-creation.md) | [ creeer een georkestreerde campagne ](../create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](../orchestrate-activities.md)<br/><br/><br/>[ Begin en controleer de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) | [ Werk met de Vraag Modeler ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uitdrukkingen ](../edit-expressions.md) uit | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - **[de activiteiten van het Kanaal](channels.md)** - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Met [!DNL Adobe Journey Optimizer] kunt u marketingcampagnes automatiseren en uitvoeren op verschillende kanalen. U kunt kanaalactiviteiten in het georkestreerde campagnecanvas combineren om kanaalgeorkestreerde campagnes tot stand te brengen die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd.

U kunt bijvoorbeeld een welkomstcampagne voor e-mail maken met een reeks berichten via verschillende kanalen, zoals e-mail, SMS en push. U kunt ook een vervolgbericht verzenden nadat een klant een aankoop heeft voltooid, of een gepersonaliseerd verjaardagsbericht naar een klant verzenden via SMS.

Door kanaalactiviteiten te gebruiken, kunt u uitvoerige en gepersonaliseerde campagnes tot stand brengen die klanten over veelvoudige touchpoints en aandrijvingsomzettingen in dienst nemen. Ondersteunde kanalen zijn E-mail, SMS en Push.

## Vereisten {#channel-activity-prereq}

Begin uw georkestreerde campagne met de relevante activiteiten te bouwen:

* Voordat u een kanaalactiviteit invoegt, moet u het publiek definiëren. Het publiek is het belangrijkste doel van uw levering: de profielen die de berichten ontvangen. [ leren hoe te om de het publieksactiviteit van de Bouwstijl te gebruiken ](build-audience.md)

* Als u een terugkerende levering wilt verzenden, start u de georkestreerde campagne met een **[!UICONTROL Scheduler]** -activiteit. U kunt ook een **[!UICONTROL Scheduler]** -activiteit gebruiken voor eenmalige leveringen om de contactdatum voor die levering in te stellen. Deze contactdatum kan ook worden ingesteld in de leveringsinstellingen. [ LEarn hoe te om een georkestreerde campagne te plannen ](../create-orchestrated-campaign.md#schedule)

## Een kanaalactiviteit configureren {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="E-mailactiviteit"
>abstract="Met de e-mailactiviteit kunt u e-mails verzenden binnen uw georkestreerde campagne, voor zowel eenmalige als terugkerende berichten. Hiermee wordt het proces geautomatiseerd waarbij e-mails worden verzonden naar een doel dat is berekend binnen dezelfde georkestreerde campagne. U kunt kanaalactiviteiten combineren tot een uit meerdere stappen bestaand campagnecanvas om kanaalcampagnes te maken die acties op klantengedrag en gegevens kunnen teweegbrengen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS-activiteit"
>abstract="Met de SMS-activiteit kunt u SMS verzenden binnen uw georkestreerde campagne voor zowel eenmalige als terugkerende berichten. Het dient om het proces te automatiseren om SMS naar een doel te verzenden dat binnen de zelfde georkestreerde campagne wordt berekend. U kunt kanaalactiviteiten combineren tot het campagnecanvas met meerdere stappen om kanaalcampagnes te maken die acties kunnen activeren op basis van het gedrag en de gegevens van de klant."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Push-activiteit"
>abstract="Met de pushactiviteit kunt u pushmeldingen verzenden als onderdeel van uw georkestreerde campagne. Het laat de levering van zowel eenmalige als terugkerende georkestreerde campagnes toe, die de verzendende Push berichten aan een vooraf bepaald doel binnen de zelfde georkestreerde campagne automatiseren. U kunt kanaalactiviteiten in het campagnecanvas combineren om kanaalcampagnes te creëren die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Directe post"
>abstract="De direct-mailactiviteit vergemakkelijkt direct mail verzenden binnen uw georkestreerde campagne, voor zowel eenmalige als terugkomende berichten. Hiermee wordt het genereren van het extractiebestand geautomatiseerd dat is vereist door directe-mailproviders. U kunt kanaalactiviteiten in het georkestreerde campagnecanvas combineren om kanaalcampagnes te creëren die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd."

Volg onderstaande stappen om een levering in te stellen in het kader van een georkestreerde campagne.

### Een kanaalactiviteit toevoegen en de eigenschappen ervan definiëren {#add}

1. Voeg een kanaalactiviteit toe aan het canvas. De beschikbare kanaalactiviteiten zijn **[!UICONTROL Email]** , **[!UICONTROL SMS]** en **[!UICONTROL Push]** .

   ![ beeld dat het canvas met beschikbare activiteiten toont ](../assets/channel-add.png)

1. Selecteer de toegevoegde activiteit en klik **[!UICONTROL Edit Email]**, **[!UICONTROL Edit SMS]**, of **[!UICONTROL Edit Push]** knoop afhankelijk van het gekozen kanaal.

   ![ beeld dat het canvas met een e-mailactiviteit toont ](../assets/channel-edit.png)

1. Voer op het tabblad **[!UICONTROL Properties]** een beschrijving in voor uw campagne.

### De kanaalconfiguratie en -instellingen instellen {#configuration}

1. Selecteer het tabblad **[!UICONTROL Actions]** en kies de kanaalconfiguratie die u voor uw bericht wilt gebruiken.

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer hoe te de configuraties van het opstellingskanaal ](../../configuration/channel-surfaces.md).

1. Voor e-mail en SMS gebruikt u de volgende opties om te controleren hoe de ontvangers reageren op uw e-mail- of SMS-berichten.

   De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

1. Voor pushberichten gebruikt u de optie **[!UICONTROL Rapid delivery mode]** om snelle berichten te verzenden naar een publieksgrootte van minder dan 30M op een pushkanaal.

   De snelle leveringswijze is een **[!DNL Journey Optimizer]** toe:voegen-op die zeer snelle drukknop toestaat die in grote volumes verzendt. [Meer informatie](../push/create-push.md#rapid-delivery)

1. In de sectie **[!UICONTROL Content experiment]** kunt u meerdere leveringsbehandelingen definiëren om te meten welke het beste presteert voor uw doelgroep.

   Om dit te doen, klik de **[!UICONTROL Create experiment]** knoop dan de stappen volgen die in deze sectie worden gedetailleerd: [ creeer een mogelijkheden van het inhoudexperiment ](../../content-management/content-experiment.md).

1. Met de sectie **[!UICONTROL Languages]** kunt u inhoud maken in meerdere talen binnen uw campagne.

   Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** . De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in deze sectie: [ krijgt begonnen met meertalige inhoud ](../../content-management/multilingual-gs.md)

### De inhoud definiëren {#content}

Selecteer de tab **[!UICONTROL Content]** om de inhoud van het bericht te definiëren. Het maken van de inhoud is afhankelijk van het geselecteerde kanaal.

Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="email" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong> E-mail </strong></a></div></td>
<td><a href="../sms/../create-sms.md"><img alt="sms" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong> SMS </strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="duwen" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong> Push bericht </strong></a></div></td>
</tr></table>

Zodra de inhoud is gedefinieerd, gebruikt u de knop **[!UICONTROL Simulate content]** om een voorvertoning van uw inhoud weer te geven en deze te testen met testprofielen of voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [Meer informatie](../content-management/preview-test.md).

## Volgende stappen {#next}

Navigeer met de pijl **[!UICONTROL Back]** terug naar uw georkestreerde campagne.

![ beeld dat de achterknoop ](../assets/channel-back.png) toont

U kunt nu de activiteiten op het canvas ordenen en de campagne publiceren om de berichten te verzenden. [ Leer hoe te om georkestreerde campagnes te beginnen en te controleren ](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
