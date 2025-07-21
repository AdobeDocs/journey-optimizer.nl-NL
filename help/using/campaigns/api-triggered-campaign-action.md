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
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---


# De actie voor de door de API geactiveerde campagne configureren {#api-action}

Gebruik het tabblad **[!UICONTROL Actions]** om een kanaalconfiguratie voor uw bericht te selecteren en aanvullende instellingen te configureren, zoals het bijhouden van inhoud, het experimenteren met inhoud of meertalige inhoud.

1. **kies het kanaal**.

   Navigeer naar de tab **[!UICONTROL Actions]** , klik op de knop **[!UICONTROL Add action]** en selecteer het communicatiekanaal.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >Welke kanalen beschikbaar zijn, is afhankelijk van uw licentiemodel en invoegtoepassingen.
   >
   >Voor door API geactiveerde campagnes zijn alleen de kanalen voor e-mail, SMS en pushmeldingen beschikbaar.

1. **selecteer een kanaalconfiguratie**

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer hoe te de configuraties van het opstellingskanaal ](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **creeer een inhoudexperiment**

   Gebruik de sectie **[!UICONTROL Content experiment]** om meerdere leveringsbehandelingen te definiëren om te meten welke het beste presteert voor uw doelgroep. Klik de **[!UICONTROL Create experiment]** knoop dan de stappen volgen die in deze sectie worden gedetailleerd: [ creeer een inhoudexperiment ](../content-management/content-experiment.md).

1. **voeg meertalige inhoud** toe

   Gebruik de sectie **[!UICONTROL Languages]** om inhoud in meerdere talen binnen uw campagne te maken. Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** . De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in deze sectie: [ krijgt begonnen met meertalige inhoud ](../content-management/multilingual-gs.md)

Afhankelijk van het geselecteerde communicatiekanaal zijn aanvullende instellingen beschikbaar. Vouw de onderstaande secties uit voor meer informatie.

+++**pas het begrenzen regels** toe (E-mail, Duw, SMS)

Selecteer in de vervolgkeuzelijst **[!UICONTROL Business rules]** een regel die is ingesteld om de afkapregels toe te passen op uw campagne. De reeksen van de kanaalregel van hefboomwerking staat u toe om frequentie het begrenzen door communicatie type te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. [ leer hoe te met regelreeksen ](../conflict-prioritization/rule-sets.md) werken

+++

+++**Overeenkomst van het Spoor** (E-mail, SMS).

In de sectie **[!UICONTROL Action tracking]** kunt u bijhouden hoe de ontvangers op uw e-mail- of SMS-berichten reageren. De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

+++

+++**laat Snelle leveringswijze** toe (Duw).

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden. Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd. Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

+++

## Volgende stappen {#next}

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u zijn inhoud ontwerpen. [Meer informatie](api-triggered-campaign-content.md)
