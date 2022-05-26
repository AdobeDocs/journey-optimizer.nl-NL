---
title: E-mailinstellingen configureren
description: Leer hoe u e-mailinstellingen configureert op het niveau van de berichtvoorinstelling
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 13fbe0583affb48269932134ea6bc214180903dd
workflow-type: tm+mt
source-wordcount: '2152'
ht-degree: 1%

---

# E-mailinstellingen configureren {#email-settings}

Definieer de e-mailinstellingen in het specifieke gedeelte van de configuratie van de berichtvoorinstelling. Leer hoe u berichtvoorinstellingen maakt in [deze sectie](message-presets.md).

![](assets/preset-email.png)

## Type e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="De e-mailcategorie definiëren"
>abstract="Selecteer het type berichten dat wordt verzonden wanneer u deze voorinstelling gebruikt: Marketing voor promotieberichten waarvoor toestemming van de gebruiker vereist is, of Transactie voor niet-commerciële berichten, die ook naar niet-geabonneerde profielen in specifieke contexten kunnen worden verzonden."

In de **E-MAILTYPE** selecteert u het type bericht dat wordt verzonden met de voorinstelling: **Marketing** of **Transactioneel**.

* Kies **Marketing** voor promotieberichten: voor deze berichten is toestemming van de gebruiker vereist .

* Kies **Transactioneel** voor niet-commerciële berichten, zoals bevestiging van de bestelling, wachtwoordherstelmeldingen of leveringsgegevens.

>[!CAUTION]
>
>**Transactioneel** berichten kunnen worden verzonden naar profielen die zich niet meer hebben geabonneerd op marketingberichten. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

Wanneer [een bericht maken](../messages/get-started-content.md#create-new-message), moet u een geldige berichtvoorinstelling kiezen die overeenkomt met de categorie die u voor uw bericht hebt geselecteerd.

## Subdomein en IP-pool {#subdomains-and-ip-pools}

In de **DETAILS VAN SUBDOMEIN EN IP-POOL** -sectie, moet u:

1. Selecteer het subdomein dat u wilt gebruiken om de e-mails te verzenden. [Meer informatie](about-subdomain-delegation.md)

1. Selecteer de IP-pool die u aan de voorinstelling wilt koppelen. [Meer informatie](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

U kunt niet doorgaan met het maken van de voorinstelling terwijl de geselecteerde IP-pool zich onder [editie](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status) en is nooit gekoppeld aan het geselecteerde subdomein. Anders, zal de oudste versie van de IP pool/subdomain vereniging nog worden gebruikt. Als dit het geval is, sparen vooraf ingesteld als ontwerp en probeer opnieuw zodra de IP pool heeft **[!UICONTROL Success]** status.

>[!NOTE]
>
>Voor niet-productiemilieu&#39;s, creeert Adobe geen uit-van-de-doos testsubdomeinen noch verleent toegang tot een gedeelde verzendende IP pool. U moet [delegeren uw eigen subdomeinen](delegate-subdomain.md) en gebruik IPs van de pool die aan uw organisatie wordt toegewezen.

## List-Unsubscribe {#list-unsubscribe}

Aan [selecteren, subdomein](#subdomains-and-ip-pools) in de lijst **[!UICONTROL Enable List-Unsubscribe]** weergegeven.

![](assets/preset-list-unsubscribe.png)

Deze optie is standaard ingeschakeld.

Als u deze optie ingeschakeld laat, wordt automatisch een afmeldingskoppeling opgenomen in de e-mailkoptekst, zoals:

![](assets/preset-list-unsubscribe-header.png)

Als u deze optie uitschakelt, wordt er geen koppeling voor afmelden weergegeven in de e-mailkoptekst.

De unsubscribe-koppeling bestaat uit twee elementen:

* An **e-mailadres opzeggen**, waarnaar alle afmeldingsverzoeken worden verzonden.

   In [!DNL Journey Optimizer], is het e-mailadres voor opzeggen het standaardadres **[!UICONTROL Mailto (unsubscribe)]** adres dat wordt weergegeven in de berichtvoorinstelling, gebaseerd op de [geselecteerd subdomein](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* De **abonnement-URL opzeggen**, dit is de URL van de bestemmingspagina waarop de gebruiker wordt omgeleid wanneer deze het abonnement opzegt.

   Als u een [one-click opt-out link](../messages/consent.md#one-click-opt-out) voor een bericht dat is gemaakt met deze voorinstelling, is de URL voor het afmelden van een abonnement de URL die is gedefinieerd voor de koppeling om één klik uit te schakelen.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Als u geen koppeling om te weigeren met één klik toevoegt aan uw berichtinhoud, wordt er geen bestemmingspagina weergegeven voor de gebruiker.

Meer informatie over het toevoegen van een link voor opzeggen van koptekst aan je berichten in [deze sectie](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parameters koptekst{#email-header}

In de **[!UICONTROL HEADER PARAMETERS]** in, voert u de namen en e-mailadressen van de afzender in die zijn gekoppeld aan het type berichten dat met die voorinstelling wordt verzonden.

>[!CAUTION]
>
>De e-mailadressen moeten de geselecteerde [gedelegeerd subdomein](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: De naam van de afzender, zoals de naam van uw merk.

* **[!UICONTROL Sender email]**: Het e-mailadres dat u voor uw communicatie wilt gebruiken. Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com* kunt u *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: De naam die wordt gebruikt wanneer de ontvanger op de knop **Reageren** in hun e-mailclientsoftware.

* **[!UICONTROL Reply to (email)]**: Het e-mailadres dat wordt gebruikt wanneer de ontvanger op de knop **Reageren** in hun e-mailclientsoftware. U moet een adres gebruiken dat op gedelegeerde subdomein wordt bepaald (bijvoorbeeld *reply@marketing.luma.com*), anders worden de e-mails verwijderd.

* **[!UICONTROL Error email]**: Alle fouten die door ISPs na een paar dagen van post worden geproduceerd die (asynchrone stuitingen) worden ontvangen op dit adres.

![](assets/preset-header.png)

>[!NOTE]
>
>Adressen moeten beginnen met een letter (A-Z) en mogen alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

### E-mail doorsturen {#forward-email}

Als je naar een specifiek e-mailadres wilt doorsturen, alle e-mails ontvangen door [!DNL Journey Optimizer] voor het gedelegeerde subdomein, contacteer de Zorg van de Klant van de Adobe. U moet het volgende opgeven:

* Het e-mailadres van uw keuze. Merk op dat het voorwaartse domein van het e-mailadres geen subdomein kan aanpassen dat aan Adobe wordt gedelegeerd.
* De naam van uw sandbox.
* De naam van de voorinstelling waarvoor het e-mailadres (of &quot;antwoord op&quot;) wordt gebruikt.
* De huidige **[!UICONTROL Reply to (email)]** adres ingesteld op het vooraf ingestelde niveau.

>[!NOTE]
>
>Per subdomein kan slechts één voorwaarts e-mailadres aanwezig zijn. Als meerdere voorinstellingen hetzelfde subdomein gebruiken, moet voor alle voorinstellingen hetzelfde e-mailadres worden gebruikt.

Het e-mailadres voor verzending wordt ingesteld door Adobe. Dit kan 3 tot 4 dagen duren.

## BCC-e-mail {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Een BCC-e-mailadres definiëren"
>abstract="U kunt een kopie van verzonden e-mailberichten bewaren door deze naar een BCC-postvak te verzenden. Voer het e-mailadres van uw keuze in, zodat elke verzonden e-mail blind wordt gekopieerd naar dit BCC-adres. Deze functie is optioneel."

U kunt een identieke kopie (of blinde koolstofkopie) van een e-mailbericht verzenden dat is verzonden door [!DNL Journey Optimizer] naar een BCC-postvak. Met deze optionele functie kunt u kopieën behouden van e-mailberichten die u naar uw gebruikers verzendt voor compatibiliteits- en/of archiefdoeleinden. Dit zal onzichtbaar zijn voor de leverende ontvangers.

### BCC-e-mail inschakelen {#enable-bcc}

Om het **[!UICONTROL BCC email]** voert u het e-mailadres van uw keuze in het desbetreffende veld in. U kunt elk extern adres in de juiste indeling opgeven, behalve een e-mailadres dat is gedefinieerd in het gedelegeerde subdomein. Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com*, elk adres zoals *abc@marketing.luma.com* is verboden.

>[!NOTE]
>
>U kunt slechts één BCC-e-mailadres definiëren. Controleer of het BCC-adres voldoende ontvangstcapaciteit heeft om alle e-mails op te slaan die met de huidige voorinstelling worden verzonden.

![](assets/preset-bcc.png)

Alle e-mailberichten die deze voorinstelling gebruiken, worden blind gekopieerd naar het e-mailadres dat u voor BCC hebt opgegeven. Van daaruit kunnen ze worden verwerkt en gearchiveerd met behulp van een extern systeem.

>[!CAUTION]
>
>Het gebruik van de BCC-functie wordt afgeboekt op het aantal berichten waarvoor u een licentie hebt. Schakel deze daarom alleen in in de voorinstellingen die worden gebruikt voor kritieke communicatie die u wilt archiveren. Controleer uw contract op volumes met licentie.

De instelling voor het e-mailadres van de BCC wordt direct opgeslagen en verwerkt op het vooraf ingestelde niveau. Wanneer u [een nieuw bericht maken](../messages/get-started-content.md#create-new-message) Als u deze voorinstelling gebruikt, wordt het BCC-e-mailadres automatisch weergegeven.

![](assets/preset-bcc-in-msg.png)

Nochtans, wordt het adres BCC opgepikt voor het verzenden van mededelingen die de logica hieronder volgen:

* Voor batch- en burstritten geldt deze regel niet voor batch- of burstuitvoering die al was gestart voordat de BCC-instelling werd ingesteld. De wijziging wordt opgepikt bij de volgende herhaling of nieuwe uitvoering.

* Voor transactieberichten, wordt de verandering opgenomen onmiddellijk voor de volgende mededeling (tot één minieme vertraging).

>[!NOTE]
>
>U hoeft geen bericht of reis opnieuw te publiceren om de instelling BCC op te halen.

### Recommendations en beperkingen {#recommendations-limitations}

* Controleer of het BCC-e-mailadres correct is ingesteld. Als dit niet het geval is, kunnen de persoonlijk identificeerbare gegevens van uw klanten (PII) naar een ongewenst adres worden verzonden.

* Om privacyredenen moeten BCC-e-mails worden verwerkt door een archiveringssysteem dat veilig identificeerbare informatie (PII) kan opslaan.

* Deze functie levert mogelijk het BCC-e-mailadres voordat de levering aan de ontvangers plaatsvindt. Dit kan ertoe leiden dat BCC-berichten worden verzonden, ook al hebben de oorspronkelijke leveringen mogelijk [afgezwakt](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Als de e-mails die naar het BCC-adres worden verzonden worden geopend en doorgeklikt, wordt hiermee rekening gehouden bij het openen van de volledige e-mailberichten en het klikken op de verzendanalyse, wat tot onjuiste berekeningen kan leiden bij [rapporten](../reports/message-monitoring.md). Ook het markeren van BCC-e-mails die in uw Postvak IN landen als spam, kan ertoe leiden dat e-mails in de spammap van uw Postvak IN landen.

* De inbox die voor BCC wordt gebruikt, moet correct worden beheerd voor ruimte en levering. Als het postvak inbox bellen retourneert, worden sommige e-mails mogelijk niet ontvangen en worden deze daarom niet gearchiveerd.

>[!CAUTION]
>
>Klik niet op de link Abonnement opzeggen in de e-mails die naar het BCC-adres worden verzonden omdat u het abonnement op de desbetreffende ontvangers meteen opzegt.

### GDPR-conformiteit {#gdpr-compliance}

In verordeningen zoals de GDPR is bepaald dat betrokkenen hun toestemming te allen tijde kunnen wijzigen. Omdat de BCC-e-mails die u met Journey Optimizer verzendt, veilig herkenbare gegevens (PII&#39;s) bevatten, moet u de **[!UICONTROL CJM Email BCC Feedback Event Schema]** deze PII te kunnen beheren in overeenstemming met de GDPR en soortgelijke voorschriften.

Volg de onderstaande stappen om dit te doen.

1. Ga naar **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** en selecteert u **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

   ![](assets/preset-bcc-schema.png)

1. Klik om uit te vouwen **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** dan **[!UICONTROL secondaryRecipientDetail]**.

1. Selecteer **[!UICONTROL originalRecipientAddress]**.

1. In de **[!UICONTROL Field properties]** rechts, omlaag schuiven naar de **[!UICONTROL Identity]** selectievakje.

1. Selecteer het en selecteer ook **[!UICONTROL Primary identity]**.

1. Selecteer een naamruimte in de vervolgkeuzelijst.

   ![](assets/preset-bcc-schema-identity.png)

1. Klik op **[!UICONTROL Apply]**.

>[!NOTE]
>
>Meer informatie over het beheren van privacy en de toepasselijke regels in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target=&quot;_blank&quot;}.

### BCC-rapportagegegevens {#bcc-reporting}

Rapportage als zodanig over BCC is niet beschikbaar in de reis- en berichtrapporten. Nochtans, wordt de informatie opgeslagen op een systeemdataset genoemd **[!UICONTROL AJO BCC Feedback Event Dataset]**. U kunt vragen tegen deze dataset in werking stellen om nuttige informatie voor het zuiveren doel bijvoorbeeld te vinden.

U kunt tot deze dataset door het gebruikersinterface toegang hebben. Selecteren **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** en de **[!UICONTROL Show system datasets]** knevel van de filter om de systeem-geproduceerde datasets te tonen. Leer meer over hoe te om tot datasets in toegang te hebben [deze sectie](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Om vragen tegen deze dataset in werking te stellen, kunt u de Redacteur van de Vraag gebruiken die door wordt verstrekt [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. Selecteer **[!UICONTROL Data management]** > **[!UICONTROL Queries]** en klik op **[!UICONTROL Create query]**. [Meer informatie](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Afhankelijk van welke informatie u zoekt, kunt u de volgende vragen in werking stellen.

1. Voor alle andere hieronder vragen, zult u identiteitskaart van de reisactie nodig hebben. Voer deze query uit om alle actie-id&#39;s op te halen die zijn gekoppeld aan een bepaalde versie-id voor de reis binnen de laatste twee dagen:

       &quot;
       SELECT
       DISTINCT
       CAST(TIMESTAMP AS DATE) ALS EventTime,
       _experience.tripOrchestration.stepEvents.tripVersionID,
       _experience.tripOrchestration.stepEvents.actionName,
       _experience.tripOrchestration.stepEvents.actionID
       FROM trip_step_events
       WAAR
       _experience.tripOrchestration.stepEvents.tripVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&quot; EN
       _experience.tripOrchestration.stepEvents.actionID is niet NULL EN
       TIJDSTEMPEL > NOW() - INTERVAL &#39;2&#39; DAG
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Om de `<journey version id>`parameter, selecteer de overeenkomstige [reisversie](../building-journeys/journey-versions.md) van de **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** -menu. De reisversie-id wordt weergegeven aan het einde van de URL die in uw webbrowser wordt weergegeven.
   >
   >![](assets/preset-bcc-action-id.png)

1. Voer deze query uit om alle bericht-feedbackgebeurtenissen (met name feedbackstatus) op te halen die zijn gegenereerd voor een bepaald bericht dat binnen de laatste twee dagen als doel is ingesteld voor een specifieke gebruiker:

       &quot;
       SELECT
       _experience.customerJourneyManagement.messageExecution.tripVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.tripActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjourneymanagement.messageDeliyfeedback.feedbackStatus AS FeedbackStatus,
       CASE_experience.customerjourneymanagement.messageDeliyfeedback.feedbackStatus
       WANNEER &#39;sent&#39; VERVOLGENS &#39;Sent&#39;
       WANNEER &#39;delay&#39; VERVOLGENS &#39;Opnieuw&#39;
       WANNEER &#39;out_of_band&#39; VERVOLGENS &#39;Bounce&#39;
       WANNEER &#39;stuiteren&#39; VERVOLGENS &#39;stuiteren&#39;
       END ALS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       WAAR
       timestamp > now() - INTERVAL &#39;2&#39; day EN
       _experience.customerJourneyManagement.messageExecution.tripVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&quot; EN
       _experience.customerJourneyManagement.messageExecution.tripActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&quot; EN
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Om de `<journey action id>` parameter, stel de eerste hierboven beschreven vraag in werking gebruikend identiteitskaart van de reisversie. De `<recipient email address>` parameter is het beoogde of werkelijke e-mailadres van de ontvanger.

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

## Parameters opnieuw proberen {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="De periode voor het opnieuw proberen aanpassen"
>abstract="Er worden 3,5 dagen (84 uur) opnieuw geprobeerd wanneer een e-mailbericht mislukt als gevolg van een tijdelijke soft bounce-fout. U kunt deze standaardperiode voor opnieuw proberen aanpassen aan uw wensen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Opnieuw proberen"

U kunt de **Parameters opnieuw proberen**.

![](assets/preset-retry-parameters.png)

Standaard worden de [periode voor opnieuw uitproberen](retries.md#retry-duration) is ingesteld op 84 uur, maar u kunt deze instelling aanpassen aan uw wensen.

U moet een geheel-getalwaarde (in uren of notulen) binnen de volgende waaier ingaan:

* Voor het in de handel brengen van e-mails is de minimale herroepingstermijn 6 uur.
* Voor transactie-e-mailberichten is de minimale herroepingstermijn 10 minuten.
* Voor beide e-mailtypen is de maximale hergebruiksperiode 84 uur (of 5040 minuten).

Meer informatie over nieuwe pogingen in [deze sectie](retries.md).

## URL-tracking {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parameters voor URL-tracking"
>abstract="In deze sectie kunt u automatisch parameters voor bijhouden toevoegen aan de campagne-URL&#39;s in uw e-mailinhoud."

U kunt **[!UICONTROL URL Tracking Parameters]** om de doeltreffendheid van uw marketing inspanningen over kanalen te meten. Deze functie is optioneel.

De parameters die in deze sectie worden gedefinieerd, worden toegevoegd aan het einde van de URL&#39;s die in de inhoud van uw e-mailbericht zijn opgenomen. Vervolgens kunt u deze parameters vastleggen in hulpprogramma&#39;s voor webanalyse, zoals Adobe Analytics of Google Analytics, en verschillende prestatierapporten maken.

![](assets/preset-url-tracking.png)

Drie URL-volgparameters worden automatisch ingevuld als voorbeeld wanneer u een berichtvoorinstelling maakt. U kunt deze bewerken en maximaal 10 volgparameters toevoegen met de opdracht **[!UICONTROL Add new parameter]** knop.

Als u een URL-volgparameter wilt configureren, kunt u rechtstreeks de gewenste waarden invoeren in het dialoogvenster **[!UICONTROL Name]** en **[!UICONTROL Value]** door naar de volgende objecten te navigeren of een keuze te maken in een lijst met vooraf gedefinieerde waarden:

* Reiskenmerken: **Bron-id**, **Bronnaam**, **Id van bronversie**
* Handelingskenmerken: **Handeling-id**, **Naam van handeling**
* Kenmerken offer decisioning: **Offerte-id**, **Naam voorstel**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Selecteer geen map: Blader naar de gewenste map en selecteer een profielkenmerk dat u wilt gebruiken als waarde voor de parameter tracking.

Hieronder staan voorbeelden van URL&#39;s die compatibel zijn met Adobe Analytics en Google Analytics.

* URL die compatibel is met Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Compatibele URL voor Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>U kunt tekstwaarden typen en vooraf gedefinieerde waarden selecteren. Elk **[!UICONTROL Value]** het veld kan in totaal maximaal 255 tekens bevatten.
