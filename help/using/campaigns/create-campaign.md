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
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 2%

---

# Een campagne maken {#create-campaign}

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een oppervlaktekanaal (d.w.z. een berichtvoorinstelling) en een Adobe Experience Platform-publiek hebt die u kunt gebruiken. Meer informatie vindt u in de volgende secties:
>
>* [Kanaaloppervlakken maken](../configuration/channel-surfaces.md)
>* [Aan de slag met het publiek](../audience/about-audiences.md)

Als u een nieuwe campagne wilt maken, opent u de **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**. U kunt ook een bestaande live campagne dupliceren om een nieuwe te maken. [Meer informatie](modify-stop-campaign.md#duplicate)

## Het type campagne en het kanaal kiezen {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="**Geplande campagnes** onmiddellijk of op een bepaalde datum worden uitgevoerd en bedoeld zijn om marketingberichten te verzenden. **API geactiveerd** campagnes worden uitgevoerd gebruikend een API vraag. Zij zijn gericht op het verzenden van ofwel marketingberichten (promotieberichten waarvoor toestemming van de gebruiker vereist is) ofwel transactieberichten (niet-commerciële berichten die ook in specifieke omstandigheden naar niet-geabonneerde profielen kunnen worden verzonden)."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Campagne, categorie"
>abstract="Als u een geplande campagne maakt, kunt u **marketing** tekst wordt automatisch geselecteerd. Voor API-getriggerde campagnes kiest u of u een **marketing** bericht (promotiebericht waarvoor toestemming van de gebruiker vereist is) of **transactie** bericht (niet-commercieel bericht, dat ook naar niet-geabonneerde profielen in specifieke contexten kan worden verzonden)."

1. In de **[!UICONTROL Properties]** , geeft u op hoe u de campagne wilt uitvoeren. Er zijn twee soorten campagnes beschikbaar:

   * **[!UICONTROL Scheduled]**: voer de campagne onmiddellijk of op een bepaalde datum uit. Geplande campagnes zijn gericht op het verzenden van **marketing** berichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **[!UICONTROL API-triggered]**: voer de campagne uit met een API-aanroep. API-gestuurde campagnes zijn gericht op het verzenden van **marketing**, of **transactie** berichten, d.w.z. berichten die worden verzonden na een actie uitgevoerd door een individu: wachtwoordinstelling, winkelwagentje enz. [Leer hoe u een campagne activeert met API&#39;s](api-triggered-campaigns.md)

1. Als u een geplande campagne maakt, kunt u **marketing** tekst wordt automatisch geselecteerd. Voor API-getriggerde campagnes kiest u of u een **marketing** of **transactie** bericht.&quot;

1. In de **[!UICONTROL Actions]** kiest u het kanaal en het kanaaloppervlak dat u wilt gebruiken om uw bericht te verzenden.

   Een oppervlak is een configuratie die door een [Systeembeheerder](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [Meer informatie](../configuration/channel-surfaces.md).

   Alleen kanaaloppervlakken die compatibel zijn met het type marketingcampagne worden weergegeven in de vervolgkeuzelijst.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Als u een pushmeldingscampagne maakt, kunt u de optie **[!UICONTROL Rapid delivery mode]**, een Journey Optimizer-invoegtoepassing die het mogelijk maakt om zeer snelle pushberichten in grote hoeveelheden te verzenden. [Meer informatie](../push/create-push.md#rapid-delivery)

1. Klikken **[!UICONTROL Create]** om de campagne op te zetten.

## De eigenschappen van de campagne definiëren {#create}

1. In de **[!UICONTROL Properties]** een naam en een beschrijving voor de campagne opgeven.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. De **Tags** kunt u Adobe Experience Platform Unified Tags aan uw campagne toewijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [Leer hoe u met tags kunt werken](../start/search-filter-categorize.md#tags)

1. Als u aangepaste of basislabels voor gegevensgebruik aan de campagne wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

## Creeer het bericht en vorm het volgen {#content}

In de **[!UICONTROL Actions]** , maakt u het bericht dat u wilt verzenden met de campagne.

1. Klik op de knop **[!UICONTROL Edit content]** en maak vervolgens uw berichtinhoud.

   Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lood" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>E-mails maken</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Onfrequent" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Pushberichten maken</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validatie" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>SMS-berichten maken</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Wanneer de inhoud is gedefinieerd, gebruikt u de **[!UICONTROL Simulate content]** om de inhoud met testprofielen voor te vertonen en te testen. [Meer informatie](../email/preview.md).

1. Klik op de pijl om terug te gaan naar het scherm Campagne maken.

   ![](assets/create-campaign-design.png)

1. In de **[!UICONTROL Actions tracking]** , geeft u op of u wilt bijhouden hoe de ontvangers op uw levering reageren: u kunt klikken en/of openen bijhouden.

   De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd. [Meer informatie over campagnerapporten](../reports/campaign-global-report.md)

## De doelgroep definiëren {#audience}

Klik op de knop **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-doelgroepen weer te geven. [Meer informatie over publiek](../audience/about-audiences.md)

>[!NOTE]
>
>Voor API-getriggerde campagnes moet het publiek worden ingesteld via API-aanroep. [Meer informatie](api-triggered-campaigns.md)

In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>Individuen die tot een segment behoren dat niet de geselecteerde identiteit (namespace) onder hun verschillende identiteiten heeft zullen niet door de campagne worden gericht.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

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

U kunt een frequentie bepalen waarmee het bericht van de campagne zou moeten worden verzonden. Om dit te doen, gebruik **[!UICONTROL Action triggers]** in het scherm Campagne creëren om te specificeren of de campagne dagelijks, wekelijks, of maandelijks zou moeten worden uitgevoerd.

Als u uw campagne niet meteen na activering wilt uitvoeren, kunt u een datum en tijd opgeven waarop het bericht moet worden verzonden met de opdracht **[!UICONTROL Campaign start]** -optie. De **[!UICONTROL Campaign end]** kunt u opgeven wanneer een terugkerende campagne niet meer wordt uitgevoerd.

![](assets/create-campaign-schedule.png)

Als uw campagne gereed is, kunt u deze controleren en publiceren. [Meer informatie](review-activate-campaign.md)
