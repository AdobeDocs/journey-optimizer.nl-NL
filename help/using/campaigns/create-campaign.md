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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 1%

---

# Een campagne maken {#create-campaign}

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een kanaalconfiguratie (d.w.z. een berichtoppervlak) hebt en een Adobe Experience Platform-publiek klaar voor gebruik. Meer informatie vindt u in de volgende secties:
>
>* [ creeer kanaalconfiguraties ](../configuration/channel-surfaces.md)
>* [ krijgen begonnen met publiek ](../audience/about-audiences.md)

Als u een nieuwe campagne wilt maken, opent u het menu **[!UICONTROL Campaigns]** en klikt u op **[!UICONTROL Create campaign]** . U kunt ook een bestaande live campagne dupliceren om een nieuwe te maken. [Meer informatie](modify-stop-campaign.md#duplicate)

## Het type campagne kiezen {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="**Geplande campagnes** worden uitgevoerd onmiddellijk of op een gespecificeerde datum en zijn bedoeld om berichten van het marketingtype te verzenden. **API-teweeggebrachte** campagnes worden uitgevoerd gebruikend een API vraag. Zij zijn gericht op het verzenden van ofwel marketingberichten (promotieberichten waarvoor toestemming van de gebruiker vereist is) ofwel transactieberichten (niet-commerciële berichten die ook in specifieke omstandigheden naar niet-geabonneerde profielen kunnen worden verzonden)."

1. Selecteer het type campagne dat u wilt uitvoeren

   * **[!UICONTROL Scheduled - Marketing]** : voer de campagne onmiddellijk uit of op een opgegeven datum. De geplande campagnes zijn gericht op het verzenden van **marketing** berichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **[!UICONTROL API-triggered - Marketing/Transactional]** : voer de campagne uit met behulp van een API-aanroep. API-teweeggebrachte campagnes zijn gericht op het verzenden van of **marketing**, of **transactie** berichten, d.w.z. berichten die na een actie worden verzonden die door een individu wordt uitgevoerd: het terugstellen van het wachtwoord, het kartelaankoop enz. [ Leer hoe te om een campagne teweeg te brengen gebruikend APIs ](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. Klik op **[!UICONTROL Create]** om de campagne te maken.

## De eigenschappen van de campagne definiëren {#create}

1. Geef in de sectie **[!UICONTROL Properties]** een naam en een beschrijving voor de campagne op.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. Het **gebied van Markeringen** staat u toe om Adobe Experience Platform Verenigde Markeringen aan uw campagne toe te wijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [ leer hoe te met markeringen ](../start/search-filter-categorize.md#tags) werken

1. Klik op de knop **[!UICONTROL Manage access]** als u aangepaste of basislabels voor gegevensgebruik aan de campagne wilt toewijzen. [ leer meer op het Toegangsbeheer van het Niveau van Objecten (OLA) ](../administration/object-based-access.md)

## Het campagnepubliek definiëren {#audience}

Definieer de doelgroep voor de campagne en voer de volgende stappen uit:

>[!IMPORTANT]
>
>Het gebruik van publiek en attributen van [ publiekssamenstelling ](../audience/get-started-audience-orchestration.md) is momenteel niet beschikbaar voor gebruik met het Schild van de Gezondheidszorg of Privacy en het Schild van de Veiligheid.
>
>Voor API-getriggerde campagnes moet het publiek worden ingesteld via API-aanroep.

1. In de **sectie van het publiek**, klik de **[!UICONTROL Select audience]** knoop om de lijst van beschikbare publiek van Adobe Experience Platform te tonen. [ leer meer op publiek ](../audience/about-audiences.md)

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren.

   Individuen die tot een segment behoren dat niet de geselecteerde identiteit (namespace) onder hun verschillende identiteiten heeft zullen niet door de campagne worden gericht. [ Leer meer op namespaces ](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Creeer het bericht en vorm het volgen {#content}

1. Selecteer of maak een nieuwe configuratie in de sectie **[!UICONTROL Actions]** .

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

1. Wanneer de inhoud is gedefinieerd, gebruikt u de knop **[!UICONTROL Simulate content]** om een voorvertoning van de inhoud weer te geven en de inhoud met testprofielen te testen. [Meer informatie](../content-management/preview-test.md).

1. Klik op de pijl om terug te gaan naar het scherm Campagne maken.

   ![](assets/create-campaign-design.png)

1. Geef in de sectie **[!UICONTROL Actions tracking]** op of u wilt bijhouden hoe de ontvangers op de levering reageren: u kunt klikken en/of openen bijhouden.

   De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

## De campagne plannen {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Campagne"
>abstract="Standaard worden campagnes gestart bij handmatige activering en worden ze onmiddellijk beëindigd nadat het bericht eenmaal is verzonden. Desalniettemin hebt u de flexibiliteit om een specifieke datum en tijd voor het te verzenden bericht te plaatsen. Bovendien kunt u een einddatum opgeven voor terugkerende of API-gestuurde campagnes. In de triggers van Actie kunt u de verzendfrequentie van berichten ook configureren om deze aan te passen aan uw voorkeuren."

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

Standaard worden campagnes gestart zodra ze handmatig zijn geactiveerd en eindigen zodra het bericht eenmaal is verzonden.

U kunt een frequentie bepalen waarmee het bericht van de campagne zou moeten worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

Als u de campagne niet meteen na activering wilt uitvoeren, kunt u met de optie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden. Met de optie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een terugkerende campagne niet meer wordt uitgevoerd.

![](assets/create-campaign-schedule.png)

Als uw campagne gereed is, kunt u deze controleren en publiceren. [Meer informatie](review-activate-campaign.md)
