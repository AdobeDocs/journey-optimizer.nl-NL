---
solution: Journey Optimizer
product: journey optimizer
title: Een kanaalactiviteit toevoegen aan een campagne met meerdere stappen
description: Leer hoe u een kanaalactiviteit toevoegt aan een campagne die uit meerdere stappen bestaat
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 1%

---

# Kanaalactiviteiten {#channel}

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


+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](../gs-orchestrated-campaigns.md)<br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](../gs-schemas.md)</li><li>[ Handmatig schema ](../manual-schema.md)</li><li>[ het uploadschema van het Dossier ](../file-upload-schema.md)</li><li>[ Ingest gegevens ](../ingest-data.md)</li></ul>[ toegang en beheer georkestreerde campagnes ](../access-manage-orchestrated-campaigns.md) | [ Zeer belangrijke stappen om een georkestreerde campagne ](../gs-campaign-creation.md)<br/><br/>[ tot stand te brengen en te plannen de campagne ](../create-orchestrated-campaign.md)<br/><br/>[ activiteiten van het Orchestrate ](../orchestrate-activities.md)<br/><br/>[ Begin en de campagne ](../start-monitor-campaigns.md)<br/><br/>[ Meldend ](../reporting-campaigns.md) te controleren | [ Werk met de regelbouwer ](../orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](../build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](../edit-expressions.md)<br/><br/>[ opnieuw op ](../retarget.md) | [ wordt begonnen met activiteiten ](about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](and-join.md) - [ bouwt publiek ](build-audience.md) - [ dimensie van de Verandering ](change-dimension.md) - <b>[ de activiteiten van het Kanaal ](channels.md)</b> - [ combineren ](combine.md) - [ Deduplicatie ](deduplication.md) - [ Verrijking ](enrichment.md) Formeel k [ - ](fork.md) Verzoening [ - ](reconciliation.md) sparen publiek [ - ](save-audience.md) Gesplitst [ - ](split.md) wacht [](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Met [!DNL Adobe Journey Optimizer] kunt u marketingcampagnes automatiseren en uitvoeren via verschillende kanalen: e-mail, SMS en pushberichten. U kunt deze kanaalactiviteiten in het campagnecanvas combineren om kanaalgeorkestreerde campagnes tot stand te brengen die acties kunnen teweegbrengen die op klantengedrag en gegevens worden gebaseerd.

Bijvoorbeeld:
* Verzend een welkomstreeks via e-mail, SMS en push.
* Na aankoop een e-mailvervolgbericht verzenden.
* Verzend gepersonaliseerde verjaardagsgroeten via SMS.

Door kanaalactiviteiten te gebruiken, kunt u uitvoerige en gepersonaliseerde campagnes tot stand brengen die klanten over veelvoudige touchpoints en aandrijvingsomzettingen in dienst nemen.

>[!PREREQUISITES]
>
>Alvorens een kanaalactiviteit toe te voegen, bepaal het doelpubliek gebruikend a [ de publieksactiviteit van de Bouwstijl ](build-audience.md).

## Een kanaalactiviteit toevoegen en de eigenschappen ervan definiëren {#add}

1. Voeg een kanaalactiviteit toe aan het canvas. De beschikbare kanaalactiviteiten zijn **[!UICONTROL Email]** , **[!UICONTROL SMS]** en **[!UICONTROL Push]** .

   ![ beeld dat het canvas met beschikbare activiteiten toont ](../assets/channel-add.png)

1. Selecteer de activiteit en klik op **[!UICONTROL Edit email]** , **[!UICONTROL Edit SMS]** of **[!UICONTROL Edit Push]** afhankelijk van het gekozen kanaal.

   ![ beeld dat het canvas met een e-mailactiviteit toont ](../assets/channel-edit.png)

1. Voer op het tabblad **[!UICONTROL Properties]** een beschrijving in en schakel vervolgens over naar het tabblad **[!UICONTROL Actions]** om de activiteit te configureren.

## De kanaalconfiguratie en -instellingen instellen {#configuration}

Gebruik het tabblad **[!UICONTROL Actions]** om een kanaalconfiguratie voor uw bericht te selecteren en aanvullende instellingen te configureren, zoals het bijhouden van inhoud, het experimenteren met inhoud of meertalige inhoud.

1. Selecteer een kanaalconfiguratie.

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer hoe te de configuraties van het opstellingskanaal ](../../configuration/channel-surfaces.md).

   ![ beeld dat de sectie van Acties ](../assets/channel-actions.png) toont

1. Betrokkenheid bijhouden (voor e-mail en SMS).

   In de sectie **[!UICONTROL Action tracking]** kunt u bijhouden hoe de ontvangers op uw e-mail- of SMS-berichten reageren. De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../../reports/campaign-global-report-cja.md)

1. De modus Snelle levering inschakelen (voor Push).

   De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden. Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd. Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

1. Maak een inhoudexperiment.

   Gebruik de sectie **[!UICONTROL Content experiment]** om meerdere leveringsbehandelingen te definiëren om te meten welke het beste presteert voor uw doelgroep. Klik de **[!UICONTROL Create experiment]** knoop dan de stappen volgen die in deze sectie worden gedetailleerd: [ creeer een inhoudexperiment ](../../content-management/content-experiment.md).

1. Voeg meertalige inhoud toe.

   Gebruik de sectie **[!UICONTROL Languages]** om inhoud in meerdere talen binnen uw campagne te maken. Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** . De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in deze sectie: [ krijgt begonnen met meertalige inhoud ](../../content-management/multilingual-gs.md)

   ![ beeld dat de sectie van het Inhoudexperiment toont ](../assets/channel-experiment.png)

Wanneer uw kanaalactiviteit is gevormd, selecteer het **[!UICONTROL Content]** lusje om zijn inhoud te bepalen.

## De inhoud definiëren {#content}

Schakel over naar het tabblad **[!UICONTROL Content]** om uw bericht te maken. De stappen variëren afhankelijk van het geselecteerde kanaal. Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="email" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Een e-mail maken</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="sms" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Een sms maken</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="duwen" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Een pushmelding maken</strong></a></td>
</tr></table>

Zodra de inhoud is gemaakt, gebruikt u de knop **[!UICONTROL Simulate Content]** om een voorvertoning van uw inhoud weer te geven en deze te testen met testprofielen of voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [Meer informatie](../../content-management/preview-test.md)

![ beeld dat de Simulate knoop van de Inhoud toont ](../assets/channel-simulate.png)

## Volgende stappen {#next}

Wanneer de inhoud van het bericht gereed is, navigeert u met de pijl **[!UICONTROL Back]** terug naar uw georkestreerde campagne. Vervolgens kunt u de activiteiten op het canvas ordenen en de campagne publiceren om de berichten te verzenden. [ Leer hoe te om georkestreerde campagnes te beginnen en te controleren ](../start-monitor-campaigns.md)

![ beeld dat de achterknoop ](../assets/channel-back.png) toont

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
