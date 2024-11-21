---
solution: Journey Optimizer
product: journey optimizer
title: Een campagne maken
description: Meer informatie over het maken van campagnes in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: maken, optimaliseren, campagne, oppervlak, berichten
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Een campagne maken {#create-campaign}

Als u een nieuwe campagne wilt maken, opent u het menu **[!UICONTROL Campaigns]** en klikt u op **[!UICONTROL Create campaign]** . U kunt ook een bestaande live campagne dupliceren om een nieuwe te maken. [Meer informatie](modify-stop-campaign.md#duplicate)

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een kanaalconfiguratie (d.w.z. een berichtoppervlak) hebt en een Adobe Experience Platform-publiek klaar voor gebruik. Meer informatie vindt u in de volgende secties:
>
>* [ creeer kanaalconfiguraties ](../configuration/channel-surfaces.md)
>* [ krijgen begonnen met publiek ](../audience/about-audiences.md)

## Het type campagne selecteren {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="**Geplande campagnes** worden uitgevoerd onmiddellijk of op een gespecificeerde datum en zijn bedoeld om berichten van het marketingtype te verzenden. **API-teweeggebrachte** campagnes worden uitgevoerd gebruikend een API vraag. Zij zijn gericht op het verzenden van ofwel marketingberichten (promotieberichten waarvoor toestemming van de gebruiker vereist is) ofwel transactieberichten (niet-commerciële berichten die ook in specifieke omstandigheden naar niet-geabonneerde profielen kunnen worden verzonden)."

Wanneer u een nieuwe campagne maakt, moet u eerst het type campagne selecteren. Er zijn drie soorten campagnes beschikbaar:

1. **[!UICONTROL Scheduled - Marketing]** - Deze campagnes worden onmiddellijk of op een gespecificeerde datum uitgevoerd. De geplande campagnes zijn gericht op het verzenden van **marketing** berichten, of creeer binnenkomende acties. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

1. **[!UICONTROL API-triggered - Marketing]** - Deze campagnes worden uitgevoerd met een API-aanroep. Selecteer dit type campagne om gepersonaliseerde marketing mededelingen naar gericht publiek te verzenden.  [ Leer hoe te om een campagne teweeg te brengen gebruikend APIs ](api-triggered-campaigns.md)

1. **[!UICONTROL API-triggered - Transactional]** - Hetzelfde als voor API-geactiveerde marketingcampagnes, worden deze campagnes uitgevoerd met behulp van een API-aanroep. API-teweeggebrachte transactiecampagnes zijn gericht op het verzenden van **transactie** berichten, d.w.z. berichten die na een actie worden verzonden die door een individu wordt uitgevoerd: verzoek om het terugstellen van het wachtwoord, kartaankoop, enz.  [ Leer hoe te om een campagne teweeg te brengen gebruikend APIs ](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

## De eigenschappen van de campagne definiëren {#create}

Wanneer de campagne is gemaakt, moet u de eigenschappen ervan definiëren. Volg de onderstaande stappen:

1. Voer in de sectie **[!UICONTROL Properties]** de naam en een beschrijving voor uw campagne in.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. (facultatief) Gebruik het **gebied van Markeringen** om Adobe Experience Platform Verenigde Markeringen aan uw campagne toe te wijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [ Leer hoe te met markeringen ](../start/search-filter-categorize.md#tags) te werken.

1. (optioneel) U kunt de toegang tot deze campagne beperken op basis van toegangslabels. Blader naar de knop **[!UICONTROL Manage access]** boven aan deze pagina om een toegangsbeperking toe te voegen. Zorg ervoor dat u alleen labels selecteert waarvoor u gemachtigd bent. [ leer meer op het Toegangsbeheer van het Niveau van Objecten ](../administration/object-based-access.md).

## Het campagnepubliek definiëren {#audience}

Nu kunt u het publiek van uw campagne selecteren. Een publiek is een groep personen die vergelijkbare gedragingen en/of kenmerken delen.

>[!IMPORTANT]
>
>* Het gebruik van publiek en attributen van [ publiekssamenstelling ](../audience/get-started-audience-orchestration.md) is momenteel niet beschikbaar voor gebruik met het Schild van de Gezondheidszorg of Privacy en het Schild van de Veiligheid.
>
>* Voor API-getriggerde campagnes moet het publiek worden ingesteld via API-aanroep.


Voer de volgende stappen uit om de doelgroep van een geplande marketingcampagne te bepalen:

1. In de **sectie van het publiek**, klik de **[!UICONTROL Select audience]** knoop om de lijst van beschikbare publiek van Adobe Experience Platform te tonen. Leer meer over publiek in [ deze sectie ](../audience/about-audiences.md).

1. Kies in het veld **[!UICONTROL Identity type]** het type sleutel dat u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. U kunt een bestaand identiteitstype gebruiken of een nieuw type maken met de Adobe Experience Platform Identity Service. De standaard naamruimten van de Identiteit zijn vermeld in [ deze pagina ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard) {target="_blank"}.

   Per campagne is slechts één identiteitstype toegestaan. Individuen die tot een segment behoren dat niet het geselecteerde identiteitstype onder hun verschillende identiteiten heeft kunnen niet door de campagne worden gericht.

   ![](assets/create-campaign-namespace.png)

   Leer meer over identiteitstypes en namespaces in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl) {target="_blank"}.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->



## Creeer het bericht en vorm het volgen {#content}

U kunt nu de inhoud van het bericht definiëren. Volg de onderstaande stappen:

1. Selecteer het communicatiekanaal in de sectie **[!UICONTROL Actions]** .

   De lijst met beschikbare kanalen is afhankelijk van uw licentiemodel en invoegtoepassingen. Voor API-getriggerde campagnes zijn alleen de kanalen voor e-mail, SMS en pushmeldingen beschikbaar.

1. Selecteer de kanaalconfiguratie.

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [Meer informatie](../configuration/channel-surfaces.md).

   Alleen kanaalconfiguraties die compatibel zijn met het type marketingcampagne worden vermeld in de vervolgkeuzelijst.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Als u een pushmeldingscampagne maakt, kunt u **[!UICONTROL Rapid delivery mode]** inschakelen. Dit is een Journey Optimizer-invoegtoepassing waarmee zeer snelle pushberichten in grote volumes kunnen worden verzonden. [Meer informatie](../push/create-push.md#rapid-delivery)

1. Klik op de knop **[!UICONTROL Edit content]** om uw bericht te maken en te ontwerpen. Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lood" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong> creeer e-mails </strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Onfrequent" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong> creeer dupberichten </strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validatie" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong> creeer SMS berichten </strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

   Wanneer de inhoud is gedefinieerd, gebruikt u de knop **[!UICONTROL Simulate content]** om een voorvertoning van de inhoud weer te geven en de inhoud met testprofielen te testen. [Meer informatie](../content-management/preview-test.md). Klik op de linkerpijl om terug te bladeren naar het scherm Campagne maken.

   ![](assets/create-campaign-design.png)

1. (optioneel) In de sectie **[!UICONTROL Content experiment]** kunt u met de knop **[!UICONTROL Create experiment]** uittesten welke inhoud het beste werkt. De experimenteringsmogelijkheden van de inhoud zijn gedetailleerd in [ deze sectie ](../content-management/content-experiment.md).

1. Geef in de sectie **[!UICONTROL Actions tracking]** op of u wilt bijhouden hoe de ontvangers op de levering reageren: u kunt klikken en/of openen bijhouden.

   De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

## De campagne plannen {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Campagne"
>abstract="De campagnes beginnen standaard bij handmatige activering en eindigen direct nadat het bericht eenmaal is verzonden. U hebt de flexibiliteit om een specifieke datum en tijd voor het te verzenden bericht te plaatsen. Bovendien kunt u een einddatum opgeven voor terugkerende of API-gestuurde campagnes. In de triggers van Actie kunt u de verzendfrequentie van berichten ook configureren om deze aan te passen aan uw voorkeuren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Start campagne"
>abstract="Geef een datum en tijd op waarop het bericht moet worden verzonden."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Einde campagne"
>abstract="Geef op wanneer een terugkerende campagne moet stoppen met uitvoeren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="actieftriggers voor campagne"
>abstract="Definieer de frequentie waarmee het campagnebericht moet worden verzonden."

Standaard worden geplande campagnes gestart zodra ze handmatig zijn geactiveerd en eindigen zodra het bericht eenmaal is verzonden.

Als u de campagne niet meteen na activering wilt uitvoeren, kunt u met de optie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden. Met de optie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren.

![](assets/create-campaign-schedule.png)

Voor e-mail-, sms- en pushberichtcampagnes kunt u een frequentie definiëren waarmee het campagnebericht moet worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

## Overige instellingen {#settings}

Sommige instellingen gelden specifiek voor het communicatiekanaal dat voor de campagne is geselecteerd, of worden gebruikt voor specifieke gebruiksgevallen. Deze worden hieronder nader toegelicht.

* Voor e-mail, kunt u specifieke IP campagnes van de opwarmingsPlan tot stand brengen. Lees meer in [deze sectie](../configuration/ip-warmup-campaign.md).
* Voor het web, in-app en op code gebaseerd kanaal, kunt u een prioritaire score aan uw campagne toewijzen. Lees meer in [deze sectie](../conflict-prioritization/priority-scores.md).
* Voor inhoudskaartcampagnes kunt u aanvullende leveringsregels inschakelen om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. Lees meer in [deze sectie](../content-card/create-content-card.md).
* Voor in-app berichten kunt u de knop **[!UICONTROL Edit triggers]** gebruiken om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. Lees meer in [deze sectie](../in-app/create-in-app.md).

## Volgende stappen {#next}

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u het herzien en activeren. [Meer informatie](review-activate-campaign.md)
