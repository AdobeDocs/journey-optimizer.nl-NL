---
solution: Journey Optimizer
product: journey optimizer
title: De actie voor de door de API geactiveerde campagne configureren
description: Leer hoe u de door de API geactiveerde campagneactie configureert.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
exl-id: 322e035c-7370-40c9-b1cb-3428bc26e874
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# De actie voor de door de API geactiveerde campagne configureren {#api-action}

Gebruik het tabblad **[!UICONTROL Actions]** om een kanaalconfiguratie voor uw bericht te selecteren en aanvullende instellingen te configureren, zoals het bijhouden van inhoud, het experimenteren met inhoud of meertalige inhoud.

1. **kies het kanaal**.

   Navigeer naar de tab **[!UICONTROL Actions]** , klik op de knop **[!UICONTROL Add action]** en selecteer het communicatiekanaal.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >Voor meer informatie over de gesteunde kanalen, verwijs naar de lijst in deze sectie: [ Kanalen in reizen &amp; campagnes ](../channels/gs-channels.md#channels). Welke kanalen beschikbaar zijn, is afhankelijk van uw licentiemodel en invoegtoepassingen.
   >
   >Door de API geactiveerde campagnes voor hoge doorvoer ondersteunen momenteel alleen het e-mailkanaal.

1. **selecteer een kanaalconfiguratie**

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer hoe te de configuraties van het opstellingskanaal ](../configuration/channel-surfaces.md)

   ![](assets/api-triggered-create-campaign-action.png)

1. **Optimalisering van de Leverage**

   Gebruik de sectie **[!UICONTROL Message Optimization]** om inhoudexperimenten uit te voeren, of hefboomwerking het richten van regels, of geavanceerde combinaties van zowel experimenteren als richten te gebruiken. Deze verschillende opties en de te volgen stappen zijn gedetailleerd in deze sectie: [ Optimalisering in campagnes ](../content-management/gs-message-optimization.md).
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **voeg meertalige inhoud** toe

   Gebruik de sectie **[!UICONTROL Languages]** om inhoud in meerdere talen binnen uw campagne te maken. Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** . De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in deze sectie: [ krijgt begonnen met meertalige inhoud ](../content-management/multilingual-gs.md)

Afhankelijk van het geselecteerde communicatiekanaal zijn aanvullende instellingen beschikbaar. Vouw de onderstaande secties uit voor meer informatie.

+++**pas het begrenzen regels** toe (E-mail, Duw, SMS)

Selecteer in de vervolgkeuzelijst **[!UICONTROL Business rules]** een regel die is ingesteld om de afkapregels toe te passen op uw campagne. De reeksen van de kanaalregel van hefboomwerking staan u toe om frequentie het begrenzen door communicatie type te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. [ leer hoe te met regelreeksen ](../conflict-prioritization/rule-sets.md) werken

+++

+++**Overeenkomst van het Spoor** (E-mail, SMS).

In de sectie **[!UICONTROL Action tracking]** kunt u bijhouden hoe de ontvangers op uw e-mail- of SMS-berichten reageren. De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

+++

+++**laat Snelle leveringswijze** toe (Duw).

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden. Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd. Leer hoe te om Snelle leveringswijze voor de Duw berichten [ op deze pagina ](../push/create-push.md#rapid-delivery) toe te laten.

Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

## Volgende stappen {#next}

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u zijn inhoud ontwerpen. [Meer informatie](api-triggered-campaign-content.md)
