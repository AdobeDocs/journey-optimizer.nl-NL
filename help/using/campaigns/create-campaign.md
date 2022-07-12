---
title: Een campagne maken
description: Leer hoe u campagnes kunt maken in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 2%

---


# Een campagne maken {#create-campaign}

>[!NOTE]
>
>Voordat u een nieuwe campagne maakt, moet u een berichtvoorinstelling en een Adobe Experience Platform-segment klaar voor gebruik hebben. Meer informatie vindt u in deze secties:
>
>* [Voorinstellingen voor berichten maken](../configuration/message-presets.md)
>* [Aan de slag met segmenten](../segment/about-segments.md)


## Een campagne configureren {#configure}

U kunt als volgt een campagne opzetten:

1. Toegang krijgen tot **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

1. In de **[!UICONTROL Properties]** in, geeft u op wanneer u de campagne wilt uitvoeren:

   * **[!UICONTROL Scheduled]**: voert de campagne onmiddellijk of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van **marketing** type berichten.
   * **[!UICONTROL API-triggered]**: voer de campagne uit gebruikend een API vraag. API-gestuurde campagnes zijn gericht op het verzenden van **transactie** berichten, d.w.z. berichten die worden verzonden na een actie uitgevoerd door een individu: wachtwoord opnieuw instellen, kaart verlaten enzovoort. [Leer hoe u een campagne activeert met behulp van API&#39;s](api-triggered-campaigns.md)

1. In de **[!UICONTROL Actions]** , kiest u het kanaal en het berichtoppervlak (dat wil zeggen de berichtvoorinstelling) dat u wilt gebruiken om uw bericht te verzenden en klikt u vervolgens op **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Alleen berichtoppervlakken die compatibel zijn met het type campagne (marketing of transactie) worden vermeld in de vervolgkeuzelijst.

1. Geef een titel en een beschrijving voor de campagne op.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In de **[!UICONTROL Actions]** , vorm het bericht om met de campagne te verzenden:

   1. Klik op de knop **[!UICONTROL Edit content]** knoop, dan vorm en ontwerp uw bericht. [Leer hoe te om berichten te vormen](../messages/get-started-content.md).

      Wanneer de inhoud gereed is, klikt u op de pijl om terug te keren naar het scherm voor het maken van de campagne.

      ![](assets/create-campaign-design.png)

   1. In de **[!UICONTROL Actions tracking]** , geeft u op of u wilt bijhouden hoe de ontvangers op uw levering reageren.

      De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd. [Meer informatie over campagnerapporten](campaign-global-report.md)

1. Bepaal het publiek om te richten. Om dit te doen, klik **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-segmenten weer te geven. [Meer informatie over segmenten](../segment/about-segments.md)

   >[!NOTE]
   >
   >Voor API-getriggerde campagnes moet het publiek worden ingesteld via API-aanroep. [Meer informatie](api-triggered-campaigns.md)

   In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Individuen die tot een segment behoren dat niet de geselecteerde identiteit (namespace) onder hun verschillende identiteiten heeft zullen niet door de campagne worden gericht.

1. De begin- en einddatum van de campagne configureren. Door gebrek, worden de Campagnes gevormd om te beginnen zodra zij manueel worden geactiveerd, en om als signalen te beëindigen aangezien het bericht is verzonden eens.

1. Bovendien, kunt u een frequentie voor de uitvoering van de actie specificeren die in de campagne wordt gevormd.

   >[!NOTE]
   >
   >Voor API-getriggerde campagnes is het plannen op een bepaalde datum en tijd met terugkerende acties niet beschikbaar omdat de actie wordt geactiveerd via de API. De begin- en einddatum zijn echter van belang om ervoor te zorgen dat als een API-aanroep vóór na het venster wordt uitgevoerd, de aanroepen een foutmelding krijgen.

   ![](assets/create-campaign-schedule.png)

1. Als u een API-gestuurde campagne maakt, **[!UICONTROL cURL request]** kunt u de **[!UICONTROL Campaign ID]** gebruiken in de API-aanroep. [Meer informatie](api-triggered-campaigns.md)

Als uw campagne gereed is, kunt u deze reviseren en publiceren (zie [Een campagne bekijken en activeren](#review-activate)).

## Een campagne bekijken en activeren {#review-activate}

Zodra uw campagne is gevormd, moet u zijn parameter en inhoud herzien alvorens het te activeren. Ga als volgt te werk om dit te doen:

1. Klik in het scherm Campagneconfiguratie op **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven.

   In het overzicht kunt u uw campagne desgewenst wijzigen en controleren of een parameter onjuist is of ontbreekt.

   >[!IMPORTANT]
   >
   >Als er fouten optreden, kunt u de campagne niet activeren. Los de fouten op voordat u verdergaat.

   ![](assets/create-campaign-alerts.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. De campagne is nu geactiveerd en heeft de **[!UICONTROL Live]** status (of **[!UICONTROL Scheduled]**  als u een begindatum hebt opgegeven). [Meer informatie over de status van campagnes](get-started-with-campaigns.md#statuses)

   Het bericht dat in de campagne wordt gevormd wordt uitgevoerd onmiddellijk of op de gespecificeerde datum.

   >[!NOTE]
   >
   >Als een campagne eenmaal is geactiveerd, blijft deze de status &quot;Live&quot; behouden, zelfs nadat het bericht is uitgevoerd. Als u de status wilt wijzigen, moet u de toepassing handmatig stoppen. [Leer hoe u een campagne kunt stoppen](modify-stop-campaign.md)

1. Nadat een campagne is geactiveerd, kunt u op elk gewenst moment de informatie controleren door deze te openen. Met dit overzicht kunt u statistieken opvragen over het aantal doelprofielen en geleverde en mislukte acties.

   U kunt extra statistieken in specifieke rapporten ook krijgen door te klikken op **[!UICONTROL Reports]** knop. [Meer informatie](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >Berichten die in campagnes worden gemaakt, zijn specifiek voor [!DNL Journey Optimizer] campagnecapaciteiten. Als deze eenmaal zijn gemaakt, zijn ze alleen toegankelijk via campagnes en worden ze niet weergegeven in de **[!UICONTROL Messages]** -menu.

## Aanvullende bronnen

* [Aan de slag met campagnes](get-started-with-campaigns.md)
* [API-gestuurde campagnes maken](api-triggered-campaigns.md)
* [Een campagne wijzigen of stoppen](modify-stop-campaign.md)
* [Campagne live-rapport](campaign-live-report.md)
* [Globaal verslag campagne voeren](campaign-global-report.md)
