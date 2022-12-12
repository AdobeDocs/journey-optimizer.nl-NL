---
solution: Journey Optimizer
product: journey optimizer
title: Een campagne maken
description: Leer hoe u campagnes kunt maken in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 5f8a765eefe4033a642c46e18be518d29b196bc3
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Een campagne maken {#create-campaign}

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een oppervlaktekanaal (d.w.z. een berichtvoorinstelling) en een Adobe Experience Platform-segment klaar hebt voor gebruik. Meer informatie vindt u in deze secties:
>
>* [Kanaaloppervlakken maken](../configuration/channel-surfaces.md)
>* [Aan de slag met segmenten](../segment/about-segments.md)


## Uw eerste campagne maken {#create}

1. Toegang krijgen tot **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >U kunt ook een bestaande live campagne dupliceren om een nieuwe te maken. [Meer informatie](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. In de **[!UICONTROL Properties]** , geeft u op hoe u de campagne wilt uitvoeren:

   * **[!UICONTROL Scheduled]**
   * **[!UICONTROL API-triggered]**

   Raadpleeg dit voor meer informatie over het type campagne en de bijbehorende betrokkenheid [sectie](#campaigntype).

1. In de **[!UICONTROL Actions]** , kiest u het kanaal en het kanaaloppervlak dat u wilt gebruiken om uw bericht te verzenden en klikt u op **[!UICONTROL Create]**.

   Een oppervlak is een configuratie die is gedefinieerd door een [Systeembeheerder](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enz. [Meer informatie](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Alleen kanaaloppervlakken die compatibel zijn met het type marketingcampagne worden weergegeven in de vervolgkeuzelijst.

1. Geef een titel en een beschrijving voor de campagne op.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Als u aangepaste of basislabels voor gegevensgebruik aan de campagne wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

## Het bericht maken {#content}

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

1. In de **[!UICONTROL Actions tracking]** in, geeft u op of u wilt bijhouden hoe de ontvangers op uw levering reageren: u kunt klikken volgen en/of opent.

   De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd. [Meer informatie over campagnerapporten](../reports/campaign-global-report.md)

## Het publiek definiëren {#audience}

1. Bepaal het publiek om te richten. Om dit te doen, klik **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platforms weer te geven. [Meer informatie over segmenten](../segment/about-segments.md)

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
>id="ajo_campaigns_schedule_start"
>title="Start campagne"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Einde campagne"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="actieftriggers voor campagne"
>abstract="TBC"

1. Om uw campagne op een specifieke datum of op een terugkomende frequentie uit te voeren, vorm **[!UICONTROL Schedule]** sectie. [Leer hoe u campagnes kunt plannen](#schedule)

1. Als u aangepaste of basislabels voor gegevensgebruik aan de campagne wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

Als uw campagne gereed is, kunt u deze controleren en publiceren. [Meer informatie](#review-activate)

## Type campagne {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="Voor een marketingbericht door een verzenddatum op te geven, wordt de **Gepland** type is het meest geschikt. Als u echter transactieberichten wilt verzenden, zoals het opnieuw instellen van het wachtwoord of het opgeven van de kaart, kunt u **API geactiveerd** type is de beste keuze."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Campagne, categorie"
>abstract="De waarde van de categorie wordt direct geassocieerd met de waarde van het campagnetype. Het campagneretype voor de **Marketing** categorie en door de API geactiveerd type voor de categorie **Transactioneel**"

Er zijn twee soorten campagnes beschikbaar:

* **[!UICONTROL Scheduled]**: voert de campagne onmiddellijk of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van **marketing** type berichten.

* **[!UICONTROL API-triggered]**: voer de campagne uit gebruikend een API vraag. API-gestuurde campagnes zijn gericht op het verzenden van **transactie** berichten, d.w.z. berichten die worden verzonden na een actie uitgevoerd door een individu: wachtwoord opnieuw instellen, kaart verlaten enzovoort. [Leer hoe u een campagne activeert met behulp van API&#39;s](api-triggered-campaigns.md)
