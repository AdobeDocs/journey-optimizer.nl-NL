---
solution: Journey Optimizer
product: journey optimizer
title: Ondersteuning voor archivering in Journey Optimizer
description: Leer hoe u berichten kunt archiveren
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: archief, berichten, HIPAA, BCC, e-mails
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 1%

---

# Ondersteuning voor archivering {#archiving-support}

## Berichten archiveren {#about-archiving}

Regels zoals HIPAA schrijven voor dat [!DNL Journey Optimizer] een manier moet bieden om berichten te archiveren die naar individuen zijn verzonden. Als uw klanten een claim indienen, moeten zij een kopie van het verzonden bericht kunnen krijgen voor controledoeleinden.

* Voor het e-mailkanaal biedt [!DNL Journey Optimizer] een ingebouwde BCC-e-mailfunctie. [Meer informatie](#bcc-email)

* Bovendien, voor alle kanalen, kunt u het gebied van het &quot;Malplaatje&quot;in de **Dataset van de Entiteit** gebruiken, die de details van de niet-gepersonaliseerde berichtmalplaatjes bevat. Exporteer de dataset met dit veld om metagegevens op te slaan, zoals: wie het bericht heeft verzonden, naar wie en wanneer. Persoonlijke gegevens worden niet geëxporteerd. Alleen de sjabloon (indeling en structuur van het bericht) wordt in aanmerking genomen. [Meer informatie](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] heeft geen eigen ondersteuning voor de archiveringsvereisten voor SMS. Voor specifieke archiefsteun, werk met uw verkoper van SMS (Sinch, Infobip, of Twilio).

## BCC gebruiken voor e-mailberichten {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Een BCC-e-mailadres definiëren"
>abstract="U kunt een kopie van verzonden e-mailberichten bewaren door deze naar een BCC-postvak te verzenden. Voer het e-mailadres van uw keuze in, zodat elke verzonden e-mail blind wordt gekopieerd naar dit BCC-adres. Merk op dat het BCC adresdomein van om het even welk subdomein moet verschillend zijn dat aan Adobe wordt gedelegeerd. Deze functie is optioneel."

U kunt BCC (blind carbon copy) van een e-mail die door [!DNL Journey Optimizer] wordt verzonden naar een speciaal BCC-adres verzenden. Met deze optionele functie kunt u kopieën behouden van e-mailberichten die u naar uw gebruikers verzendt voor compatibiliteits- en/of archiefdoeleinden. Het BCC-adres is niet zichtbaar voor andere ontvangers van het bericht.

### BCC-e-mail inschakelen {#enable-bcc}

Om de **[!UICONTROL BCC email]** optie toe te laten, ga het e-mailadres van uw keus op het specifieke gebied van de [ kanaalconfiguratie ](channel-surfaces.md) (d.w.z. vooraf ingesteld bericht) in. U kunt elk extern adres opgeven in de juiste indeling, behalve een e-mailadres dat is gedefinieerd voor een subdomein dat is gedelegeerd aan Adobe. Bijvoorbeeld, als u *marketing.luma.com* subdomain aan Adobe delegeerde, wordt om het even welk adres als *abc@marketing.luma.com* verboden.

>[!CAUTION]
>
>U kunt slechts één BCC-e-mailadres definiëren. Zorg ervoor dat het BCC-adres voldoende ontvangstcapaciteit heeft om alle e-mails op te slaan die met de huidige kanaalconfiguratie worden verzonden.
>
>Meer aanbevelingen worden vermeld in [ deze sectie ](#bcc-recommendations-limitations).

>[!NOTE]
>
>Als u de add-on aanbieding van het Schild van de Gezondheid hebt gekocht, moet u ervoor zorgen dat ISP van uw BCC adres het protocol TLS 1.2 steunt.

![](assets/preset-bcc.png)

Zodra configuratie wordt gedaan, worden alle e-mailberichten die op deze configuratie worden gebaseerd blind-gekopieerd aan het BCC e-mailadres u inging. Van daar, kunnen de berichten worden verwerkt en worden gearchiveerd gebruikend een extern systeem.

>[!CAUTION]
>
>Het gebruik van uw BCC-functie wordt afgeteld bij het aantal berichten waarvoor u een licentie hebt. Vandaar, laat slechts het in de configuraties toe die voor kritieke mededelingen worden gebruikt die u wenst te archiveren. Controleer uw contract op volumes met licentie.

De instelling voor het e-mailadres van de BCC wordt direct opgeslagen en verwerkt op configuratieniveau. Als u een nieuw bericht maakt met deze configuratie, wordt het BCC-e-mailadres automatisch weergegeven.

![](assets/preset-bcc-in-msg.png)

Nochtans, wordt het adres BCC opgepikt voor het verzenden van mededelingen na de hier beschreven logica [ ](../email/email-settings.md).

### Aanbevelingen en beperkingen {#bcc-recommendations-limitations}

* Om ervoor te zorgen dat uw privacy wordt nageleefd, moeten BCC-e-mails worden verwerkt door een archiveringssysteem dat PII&#39;s (Secure Persoonlijke Identifier Information) kan opslaan.

* Aangezien de berichten gevoelige of privé gegevens, zoals persoonlijk identificeerbare informatie (PII) kunnen bevatten, zorg ervoor het adres BCC correct is, en beveilig de toegang tot berichten.

* De inbox die voor BCC wordt gebruikt, moet correct worden beheerd voor ruimte en levering. Als het postvak inbox bellen retourneert, worden sommige e-mails mogelijk niet ontvangen en worden deze daarom niet gearchiveerd.

* De berichten kunnen aan het BCC e-mailadres vóór de doelontvangers worden geleverd. BCC de berichten kunnen ook worden verzonden alhoewel de originele berichten [ ](../reports/suppression-list.md#delivery-failures) kunnen hebben teruggestuurd.

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Open of klik niet door de e-mail die naar het adres BCC wordt verzonden aangezien het in het totaal wordt overwogen opent en klikt van verzendt analyse, die sommige misberekeningen in [ rapporten ](../reports/report-gs-cja.md) kon veroorzaken.

* Markeer geen berichten als spam in de BCC-postvak, omdat dit invloed heeft op alle andere e-mails die naar dit adres worden verzonden.

>[!CAUTION]
>
>Klik niet op de koppeling Abonnement opzeggen in de e-mails die naar het BCC-adres worden verzonden, omdat u het abonnement op de desbetreffende ontvangers meteen opzegt.

### GDPR-conformiteit {#gdpr-compliance}

In verordeningen zoals de GDPR is bepaald dat betrokkenen hun toestemming te allen tijde kunnen wijzigen. Omdat de BCC-e-mails die u met Journey Optimizer verzendt, veilig herkenbare gegevens (PII&#39;s) bevatten, moet u de **[!UICONTROL CJM Email BCC Feedback Event Schema]** bewerken om deze PII te kunnen beheren in overeenstemming met GDPR en soortgelijke regels.

Volg de onderstaande stappen om dit te doen.

1. Ga naar **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** en selecteer **[!UICONTROL CJM Email BCC Feedback Event Schema]** .

   ![](assets/preset-bcc-schema.png)

1. Klik om **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]** uit te vouwen.

1. Selecteer **[!UICONTROL originalRecipientAddress]**.

1. Schuif in de **[!UICONTROL Field properties]** aan de rechterkant omlaag naar het selectievakje **[!UICONTROL Identity]** .

1. Selecteer het en selecteer ook **[!UICONTROL Primary identity]**.

1. Selecteer een naamruimte in de vervolgkeuzelijst.

   ![](assets/preset-bcc-schema-identity.png)

1. Klik op **[!UICONTROL Apply]**.

>[!NOTE]
>
>Leer meer over het beheren van Privacy en de toepasselijke verordeningen in de [ documentatie van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl){target="_blank"}.

### BCC-rapportagegegevens {#bcc-reporting}

Rapportage als zodanig over BCC is niet beschikbaar in de reis- en berichtrapporten. De informatie wordt echter opgeslagen in een systeemgegevensset met de naam **[!UICONTROL AJO BCC Feedback Event Dataset]** . U kunt vragen tegen deze dataset in werking stellen om nuttige informatie voor het zuiveren doel bijvoorbeeld te vinden.

Selecteer **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** om via de gebruikersinterface toegang te krijgen tot deze gegevensset. Leer meer over hoe te om tot datasets in [ toegang te hebben deze sectie ](../data/get-started-datasets.md#access-datasets).

<!--![](assets/preset-bcc-dataset.png)-->

Om vragen tegen deze dataset in werking te stellen, kunt u de Redacteur van de Vraag gebruiken die door de [ Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} wordt verstrekt. Selecteer **[!UICONTROL Data management]** > **[!UICONTROL Queries]** en klik op **[!UICONTROL Create query]** om het bestand te openen. [Meer informatie](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Afhankelijk van welke informatie u zoekt, kunt u de volgende vragen in werking stellen.

1. Voor alle andere hieronder vragen, zult u identiteitskaart van de reisactie nodig hebben. Voer deze query uit om alle actie-id&#39;s op te halen die zijn gekoppeld aan een bepaalde versie-id voor de reis binnen de laatste twee dagen:

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Om de `<journey version id>` parameter te krijgen, selecteer de overeenkomstige [ reisversie ](../building-journeys/journey.md#uc-journey) van **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** menu. De reisversie-id wordt weergegeven aan het einde van de URL die in uw webbrowser wordt weergegeven.
   >
   >![](assets/preset-bcc-action-id.png)

1. Voer deze query uit om alle bericht-feedbackgebeurtenissen (met name feedbackstatus) op te halen die zijn gegenereerd voor een bepaald bericht dat binnen de laatste twee dagen als doel is ingesteld voor een specifieke gebruiker:

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Als u de parameter `<journey action id>` wilt ophalen, voert u de eerste hierboven beschreven query uit met de id van de reisversie. De parameter `<recipient email address>` is het beoogde of feitelijke e-mailadres van de ontvanger.

1. Voer deze query uit om alle BCC-bericht-feedbackgebeurtenissen op te halen die zijn gegenereerd voor een bepaald bericht dat is gericht op een specifieke gebruiker in de laatste 2 dagen:

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. Voer deze query uit om alle geadresseerde adressen op te halen die het bericht niet hebben ontvangen, terwijl de BCC-vermelding ervan in de laatste 30 dagen bestaat:

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```

### Koptekst van bericht gebruiken om BCC-kopie en verzonden e-mailgegevens te combineren {#bcc-header}

Wanneer uw BCC-e-mailkopieën worden gearchiveerd op een extern systeem, kunt u de gegevens over de bijbehorende verzonden e-mails ophalen met een header die in het bericht staat.

Elk e-mailbericht bevat nu een koptekst met de naam `x-message-profile-id` . De waarde van deze koptekst verschilt per profiel: deze is uniek voor elke verzonden e-mail en voor de bijbehorende BCC-e-mailkopie.

De `x-message-profile-id` kopbal wordt ook opgeslagen in de volgende systeemdatasets: [ Dataset van de Gebeurtenis van de Feedback van het Bericht van AJO ](../data/datasets-query-examples.md#message-feedback-event-dataset) (verzonden e-mails) en [ Dataset van de Gebeurtenis van de BCC van AJO BCC ](#bcc-reporting) (exemplaren BCC). U kunt deze datasets vragen om het exemplaar BCC en overeenkomstige daadwerkelijke e-mail met elkaar in overeenstemming te brengen.

* Selecteer **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** om deze gegevenssets te openen via de gebruikersinterface. Leer meer over hoe te om tot datasets in [ toegang te hebben deze sectie ](../data/get-started-datasets.md#access-datasets).

* Gebruik de Redacteur van de Vraag die door de [ Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} wordt verstrekt. Selecteer **[!UICONTROL Data management]** > **[!UICONTROL Queries]** en klik op **[!UICONTROL Create query]** om het bestand te openen. [Meer informatie](../data/get-started-queries.md)

Hieronder volgen enkele voorbeeldquery&#39;s die u kunt uitvoeren om informatie op te halen die overeenkomt met uw BCC-kopieën.

**Vraag 1**

U kunt als volgt de BCC-gebeurtenis gekoppeld krijgen aan de corresponderende feedbackgebeurtenis voor de werkelijke e-mail met de campagneactiedetails:

```
SELECT
  mfe.timestamp AS OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  bcc._experience.customerJourneyManagement.emailChannelContext.address AS BCCEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.campaignID AS CampaignID,
  mfe._experience.customerJourneyManagement.messageExecution.campaignActionID AS CampaignActionID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN ajo_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = '<x-message-profile-id>'
ORDER BY mfe.timestamp DESC;
```

**Vraag 2**

U kunt als volgt de BCC-gebeurtenis gekoppeld krijgen aan de corresponderende feedbackgebeurtenis voor de werkelijke e-mail met de details van de reisactie:

```
SELECT
  mfe.timestamp AS OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  bcc._experience.customerJourneyManagement.emailChannelContext.address AS BCCEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AS journeyActionID,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionInstanceID AS JourneyVersionInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN ajo_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = '<x-message-profile-id>'
ORDER BY mfe.timestamp DESC;
```
