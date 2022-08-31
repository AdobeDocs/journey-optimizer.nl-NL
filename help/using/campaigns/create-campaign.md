---
title: Een campagne maken
description: Leer hoe u campagnes kunt maken in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 3%

---

# Een campagne maken {#create-campaign}

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u ervoor zorgen dat u een oppervlaktekanaal (d.w.z. een berichtvoorinstelling) en een Adobe Experience Platform-segment gebruiksklaar hebt. Meer informatie vindt u in deze secties:
>
>* [Kanaaloppervlakken maken](../configuration/channel-surfaces.md)
>* [Aan de slag met segmenten](../segment/about-segments.md)


## Maak uw eerste campagne {#create}

1. Toegang krijgen tot **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >U kunt ook een bestaande live campagne dupliceren om een nieuwe te maken. [Meer informatie](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. In de **[!UICONTROL Actions]** , kiest u het kanaal en het kanaaloppervlak dat u wilt gebruiken om uw bericht te verzenden en klikt u op **[!UICONTROL Create]**.

   Een oppervlak is een configuratie die is gedefinieerd door een [Systeembeheerder](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enz. [Meer informatie](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Alleen kanaaloppervlakken die compatibel zijn met het type marketingcampagne worden weergegeven in de vervolgkeuzelijst.

<!--Only channel surfaces compatible with the campaign type (marketing or transactional) are listed in the drop-down list.-->

1. Geef een titel en een beschrijving voor de campagne op.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In de **[!UICONTROL Actions]** , vorm het bericht om met de campagne te verzenden:

   1. Klik op de knop **[!UICONTROL Edit content]** en vervolgens configureert en ontwerpt u uw berichtinhoud. [Meer informatie over berichten](../messages/get-started-content.md).

      Leer gedetailleerde stappen om uw berichtinhoud tot stand te brengen op de volgende pagina:

      * [Een e-mail maken](../messages/create-email.md)
      * [Pushberichten maken](../messages/create-push.md)
      * [Een SMS-bericht maken](../messages/create-sms.md)
   1. Wanneer de inhoud is gedefinieerd, gebruikt u de **[!UICONTROL Simulate content]** om de inhoud met testprofielen voor te vertonen en te testen. [Meer informatie](../design/preview.md).

   1. Klik op de pijl om terug te gaan naar het scherm Campagne maken.

      ![](assets/create-campaign-design.png)

   1. In de **[!UICONTROL Actions tracking]** in, geeft u op of u wilt bijhouden hoe de ontvangers op uw levering reageren: u kunt klikken volgen en/of opent.

      De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd. [Meer informatie over campagnerapporten](../reports/campaign-global-report.md)


1. Bepaal het publiek om te richten. Om dit te doen, klik **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-segmenten weer te geven. [Meer informatie over segmenten](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Individuen die tot een segment behoren dat niet de geselecteerde identiteit (namespace) onder hun verschillende identiteiten heeft zullen niet door de campagne worden gericht.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. Om uw campagne op een specifieke datum of op een terugkomende frequentie uit te voeren, vorm **[!UICONTROL Schedule]** sectie. [Leer hoe u campagnes kunt plannen](#schedule)

Als uw campagne gereed is, kunt u deze controleren en publiceren. [Meer informatie](#review-activate)

## Een campagne bekijken en activeren {#review-activate}

Zodra uw campagne is gevormd, moet u zijn parameter en inhoud herzien alvorens het te activeren. Ga als volgt te werk om dit te doen:

1. Klik in het scherm Campagneconfiguratie op **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

   >[!IMPORTANT]
   >
   >In het geval van fouten kunt u de campagne niet activeren. Los de fouten op voordat u verdergaat.

   ![](assets/create-campaign-alerts.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. De campagne is nu geactiveerd. Zijn status is **[!UICONTROL Live]**, of **[!UICONTROL Scheduled]** als u een begindatum hebt ingevoerd. [Meer informatie over de status van campagnes](get-started-with-campaigns.md#statuses).

   Het bericht dat in de campagne wordt gevormd wordt verzonden onmiddellijk of op de gespecificeerde datum.

   >[!NOTE]
   >
   >De **[!UICONTROL Completed]** de status wordt automatisch toegewezen aan een campagne drie dagen nadat deze is geactiveerd of op de einddatum van de campagne als deze een terugkerende uitvoering heeft.
   >
   >Als er geen einddatum is opgegeven, blijft de campagne **[!UICONTROL Live]** status. Als u deze wilt wijzigen, moet u de campagne handmatig stoppen. [Leer hoe u een campagne kunt stoppen](modify-stop-campaign.md)

1. Nadat een campagne is geactiveerd, kunt u op elk gewenst moment de informatie controleren door deze te openen. Met dit overzicht kunt u statistieken opvragen over het aantal doelprofielen en geleverde en mislukte acties.

   U kunt extra statistieken in specifieke rapporten ook krijgen door te klikken op **[!UICONTROL Reports]** knop. [Meer informatie](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

## Een campagne plannen {#schedule}

Standaard worden campagnes gestart zodra ze handmatig zijn geactiveerd en eindigen zodra het bericht eenmaal is verzonden.

U kunt een frequentie bepalen waarmee het bericht van de campagne zou moeten worden verzonden. Om dit te doen, gebruik **[!UICONTROL Action triggers]** in het scherm Campagne creëren om te specificeren of de campagne dagelijks, wekelijks, of maandelijks zou moeten worden uitgevoerd.

Als u uw campagne niet meteen na de activering wilt uitvoeren, kunt u een datum en tijd opgeven waarop het bericht moet worden verzonden met de opdracht **[!UICONTROL Campaign start]** optie. De  **[!UICONTROL Campaign end]** kunt u opgeven wanneer een terugkerende campagne niet meer wordt uitgevoerd.

![](assets/create-campaign-schedule.png)
