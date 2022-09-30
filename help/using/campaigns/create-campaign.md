---
title: Een campagne maken
description: Leer hoe u campagnes kunt maken in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: bb1a9b35ce93f9b0ba635a89e781856f19b7d655
workflow-type: tm+mt
source-wordcount: '825'
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

1. In de **[!UICONTROL Properties]** in, geeft u op wanneer u de campagne wilt uitvoeren:

   * **[!UICONTROL Scheduled]**: voert de campagne onmiddellijk of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van **marketing** type berichten.
   * **[!UICONTROL API-triggered]**: voer de campagne uit gebruikend een API vraag. API-gestuurde campagnes zijn gericht op het verzenden van **transactie** berichten, d.w.z. berichten die worden verzonden na een actie uitgevoerd door een individu: wachtwoord opnieuw instellen, kaart verlaten enzovoort. [Leer hoe u een campagne activeert met behulp van API&#39;s](api-triggered-campaigns.md)

1. In de **[!UICONTROL Actions]** , kiest u het kanaal en het kanaaloppervlak dat u wilt gebruiken om uw bericht te verzenden en klikt u op **[!UICONTROL Create]**.

   Een oppervlak is een configuratie die is gedefinieerd door een [Systeembeheerder](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enz. [Meer informatie](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Alleen kanaaloppervlakken die compatibel zijn met het type marketingcampagne worden weergegeven in de vervolgkeuzelijst.

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

   >[!NOTE]
   >
   >Voor API-getriggerde campagnes moet het publiek worden ingesteld via API-aanroep. [Meer informatie](api-triggered-campaigns.md)

   In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie over naamruimten](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Individuen die tot een segment behoren dat niet de geselecteerde identiteit (namespace) onder hun verschillende identiteiten heeft zullen niet door de campagne worden gericht.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. Om uw campagne op een specifieke datum of op een terugkomende frequentie uit te voeren, vorm **[!UICONTROL Schedule]** sectie. [Leer hoe u campagnes kunt plannen](#schedule)

1. Als u aangepaste of basislabels voor gegevensgebruik aan de campagne wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Meer informatie over OLA (Object Level Access Control)](../administration/object-based-access.md)

Als uw campagne gereed is, kunt u deze controleren en publiceren. [Meer informatie](#review-activate)

## Een campagne plannen {#schedule}

Standaard worden campagnes gestart zodra ze handmatig zijn geactiveerd en eindigen zodra het bericht eenmaal is verzonden.

U kunt een frequentie bepalen waarmee het bericht van de campagne zou moeten worden verzonden. Om dit te doen, gebruik **[!UICONTROL Action triggers]** in het scherm Campagne creëren om te specificeren of de campagne dagelijks, wekelijks, of maandelijks zou moeten worden uitgevoerd.

Als u uw campagne niet meteen na de activering wilt uitvoeren, kunt u een datum en tijd opgeven waarop het bericht moet worden verzonden met de opdracht **[!UICONTROL Campaign start]** optie. De  **[!UICONTROL Campaign end]** kunt u opgeven wanneer een terugkerende campagne niet meer wordt uitgevoerd.

![](assets/create-campaign-schedule.png)

## Snelle leveringsmodus {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Snelle leveringsmodus"
>abstract="De snelle leveringswijze is een toe:voegen-op van Journey Optimizer die u hoge snelheidsuitgaven van niet-gepersonaliseerde berichten aan publiek onder 30M profielen laat uitvoeren."

De snelle leveringswijze, die vroeger als wijze van de Borst bij reizen wordt bekend, is een [!DNL Journey Optimizer] een invoegtoepassing waarmee via campagnes zeer snel pushberichten op grote volumes kunnen worden verzonden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Voor meer informatie over prestaties bij gebruik van de modus Snelle levering raadpleegt u [Adobe Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).


### Vereisten {#prerequisites}

Snelle levering overseinen komt met de volgende vereisten:

* Snelle levering is beschikbaar voor **[!UICONTROL Scheduled]** alleen campagnes, en niet beschikbaar voor API-gestuurde campagnes;
* In het pushbericht is geen personalisatie toegestaan.
* Het doelpubliek moet minder dan 30M profielen bevatten,
* U kunt tot 5 campagnes gelijktijdig uitvoeren gebruikend de Snelle leveringswijze.

### Modus Snelle levering activeren

1. Maak een pushmeldingscampagne en schakel de optie **[!UICONTROL Rapid delivery]** optie.

![](assets/create-campaign-burst.png)

1. Vorm de berichtinhoud en selecteer het publiek om te richten. [Leer een campagne maken](#create)

   >[!IMPORTANT]
   >
   >Zorg ervoor dat de inhoud van het bericht geen personalisatie omvat, en dat het publiek minder dan 30M profielen bevat.

1. Controleer en activeer uw campagne op de gebruikelijke manier. In de testmodus worden berichten niet verzonden via de snelle leveringsmodus. [Leer hoe u een campagne kunt beoordelen en activeren](review-activate-campaign.md)
