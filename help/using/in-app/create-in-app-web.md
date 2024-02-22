---
title: Het webkanaal in de app configureren
description: Leer hoe te om het Web in-app kanaal in de inzameling van Gegevens te vormen
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 2%

---

# Een Web In-app-bericht maken {#create-in-app-web}

## Het webkanaal in de app configureren {#configure-web-inapp}

Volg onderstaande stappen om uw Web in-app kanaal in te stellen:

* Installeer de Web SDK markeringsuitbreiding om Web in-app Overseinen te steunen. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

* Pas de triggers aan. Het Berichten van het Web in-app steunt twee types van trekkers: Verzonden gegevens naar platform en Hand trekkers. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-in-app-messaging.html)

## Maak uw Web In-app berichtcampagne {#create-inapp-web-campaign}

1. Toegang krijgen tot de **[!UICONTROL Campaigns]** en klik vervolgens op **[!UICONTROL Create campaign]**.

1. In de **[!UICONTROL Properties]** , selecteert u wanneer het type uitvoering van de campagne: Gepland of API-geactiveerd. Meer informatie over campagneretypen in [deze pagina](../campaigns/create-campaign.md#campaigntype).

1. In de **[!UICONTROL Actions]** in, kiest u **[!UICONTROL In-app message]**. Van de **[!UICONTROL Send to]** vervolgkeuzelijst selecteert u Web.

   ![](assets/in_app_web_surface_1.png)

1. Definieer een App-oppervlak. U hebt twee opties om wijzigingen aan te brengen:

   * U kunt een van de **[!UICONTROL Page URL]** om wijzigingen toe te passen op een specifieke pagina.

   * U kunt een regel maken om meerdere URL&#39;s met hetzelfde patroon als doel in te stellen.

+++ Hoe te om een de passende regel van Pagina&#39;s te bouwen.

      1. Selecteren **[!UICONTROL Pages matching rule]** als App-oppervlak.
      1. Klik op **[!UICONTROL Create rule]**.

         ![](assets/in_app_web_surface_3.png)

      1. In de **[!UICONTROL Edit surface rule]** uw criteria voor het **[!UICONTROL Domain]** en **[!UICONTROL Page]** velden.
      1. Verbeter uw criteria vanuit de voorwaarde-dropdowns.

         Als u bijvoorbeeld elementen wilt bewerken die op alle pagina&#39;s met verkoopproducten van uw Luma-website worden weergegeven, selecteert u Domein > Begint met > Lumma en Pagina > Bevat > Verkoop.

         ![](assets/in_app_web_surface_4.png)

      1. Sla uw wijzigingen op. De regel wordt weergegeven in het dialoogvenster **[!UICONTROL Create campaign]** scherm.

+++

   ![](assets/in_app_web_surface_2.png)

1. Als het oppervlak van uw app is geselecteerd en geconfigureerd, klikt u op **[!UICONTROL Create]**.

## Uw webberichtcampagne in de app definiëren {#configure-inapp}

1. Van de **[!UICONTROL Properties]** in, voert u de **[!UICONTROL Title]** en de **[!UICONTROL Description]** beschrijving.

1. Als u aangepaste of basislabels voor gegevensgebruik wilt toewijzen aan het bericht in de app, selecteert u **[!UICONTROL Manage access]**. [Meer informatie](../administration/object-based-access.md).

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare publiek van Adobe Experience Platform te richten. [Meer informatie](../audience/about-audiences.md).

   ![](assets/in_app_web_surface_5.png)

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. In de **[!UICONTROL Action]** menu, kunt u de montages vinden die eerder zoals **[!UICONTROL App surface]**. U kunt hier indien nodig wijzigingen aanbrengen of uw regel bijwerken door op **[!UICONTROL Edit Rule]**.

1. Klikken **[!UICONTROL Create experiment]** om uw inhoud te configureren experimenteert u en maakt u behandelingen om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../campaigns/content-experiment.md)

1. Klikken **[!UICONTROL Edit triggers]** om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. Met regelbuilders kunnen gebruikers criteria en waarden opgeven die, wanneer ze voldoen, een set handelingen activeren, zoals het verzenden van een bericht in de app.

   1. Klik op de vervolgkeuzelijst Gebeurtenis om de trigger zo nodig te wijzigen.

      +++Zie beschikbare triggers.

      | Pakket | Trigger | Definitie |
      |---|---|---|
      | Platform | Gegevens verzonden naar platform | Wordt geactiveerd wanneer de mobiele app een Edge Experience-gebeurtenis uitgeeft om gegevens naar Adobe Experience Platform te verzenden. Meestal de API-aanroep [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) uit de extensie AEP Edge. |
      | Handmatig | Handmatige trigger | Twee bijbehorende gegevenselementen: een sleutel, die een constante is die de gegevensset definieert (bijvoorbeeld geslacht, kleur, prijs), en een waarde, die een variabele is die tot de set behoort (bijvoorbeeld man/vrouw, groen, 100). |

+++

   1. Klikken **[!UICONTROL Add condition]** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria.

   1. Kies de optie **[!UICONTROL Or]** voorwaarde als u meer wilt toevoegen **[!UICONTROL Triggers]** om uw regel verder uit te breiden.

      ![](assets/in_app_web_surface_8.png)

   1. Kies de optie **[!UICONTROL And]** voorwaarde als u een aangepast item wilt toevoegen **[!UICONTROL Trait]** en perfectioneer uw regel beter.

      +++Zie beschikbare Traits.

      | Pakket | Trait | Definitie |
      |---|---|---|
      | Platform | XDM-gebeurtenistype | Wordt geactiveerd wanneer aan het opgegeven gebeurtenistype wordt voldaan. |
      | Platform | XDM-waarde | Wordt geactiveerd wanneer aan de opgegeven XDM-waarde wordt voldaan. |
+++

      ![](assets/in_app_web_surface_9.png)

   1. Klikken **[!UICONTROL Make group]** om triggers samen te groeperen.

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is. De volgende opties zijn beschikbaar:

   * **[!UICONTROL Everytime]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Once]**: Alleen dit bericht weergeven als de in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.
   * **[!UICONTROL X number of times]**: Dit bericht wordt X-tijd weergegeven.

1. Kies zo nodig welke **[!UICONTROL Day of the week]** of **[!UICONTROL Time of day]** Het bericht in de app wordt weergegeven.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

   ![](assets/in_app_web_surface_6.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

   ![](assets/in_app_web_surface_7.png)

**Verwante onderwerpen:**

* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)