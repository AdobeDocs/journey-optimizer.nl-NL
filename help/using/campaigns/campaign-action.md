---
solution: Journey Optimizer
product: journey optimizer
title: Campagne configureren
description: Leer hoe te om de campagneactie te vormen.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: maken, optimaliseren, campagne, oppervlak, berichten
exl-id: fed96e48-2e54-4bd4-ae17-77434d1b90eb
source-git-commit: 8205d248d986cdc1a2262705c58524c2434265f5
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Campagne configureren {#action-campaign-action}

Gebruik het tabblad **[!UICONTROL Actions]** om een kanaalconfiguratie voor uw bericht te selecteren en aanvullende instellingen te configureren, zoals het bijhouden van inhoud, het experimenteren met inhoud of meertalige inhoud.



1. **kies het kanaal**

   Navigeer naar de tab **[!UICONTROL Actions]** , klik op de knop **[!UICONTROL Add action]** en selecteer het communicatiekanaal.

   ![](assets/create-campaign-add-action.png)


   >[!NOTE]
   >
   >De gesteunde kanalen zijn: [ E-mail ](../email/get-started-email.md), [ SMS/MMS/RCS ](../sms/get-started-sms.md), [ Push berichten ](../push/get-started-push.md), [ WhatsApp ](../whatsapp/get-started-whatsapp.md), [ LIJN ](../line/get-started-line.md), [ Directe post ](../direct-mail/get-started-direct-mail.md), [ in-app ](../in-app/get-started-in-app.md), [ Web ](../web/get-started-web.md), [} op code-gebaseerde ervaringen ](../code-based/get-started-code-based.md).
   >
   >Welke kanalen beschikbaar zijn, is afhankelijk van uw licentiemodel en invoegtoepassingen.

   Als u een binnenkomend kanaal selecteert (code-based ervaring, In-app bericht, de Actie van de Kaart van de Inhoud of van het Web), kunt u meer binnenkomende acties toevoegen - voor een totaal van tot 10 acties in één enkele campagne. [ leer hoe ](#multi-action)

1. **selecteer een kanaalconfiguratie**

   Een configuratie wordt bepaald door de Beheerder van het a [ Systeem ](../start/path/administrator.md). Het bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer hoe te de configuraties van het opstellingskanaal ](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Optimalisering van de Leverage**

   Gebruik de sectie **[!UICONTROL Optimization]** om inhoudexperimenten uit te voeren, of hefboomwerking het richten van regels, of geavanceerde combinaties van zowel experimenteren als richten te gebruiken. Deze verschillende opties en de te volgen stappen zijn gedetailleerd in [ deze sectie ](campaigns-message-optimization.md).
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **voeg meertalige inhoud** toe

   Gebruik de sectie **[!UICONTROL Languages]** om inhoud in meerdere talen binnen uw campagne te maken. Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** . De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in [ deze sectie ](../content-management/multilingual-gs.md).

Afhankelijk van het geselecteerde communicatiekanaal zijn aanvullende instellingen beschikbaar. Vouw de onderstaande secties uit voor meer informatie.

+++**pas het begrenzen regels** toe (E-mail, Directe post, Duw, SMS)

Selecteer in de vervolgkeuzelijst **[!UICONTROL Business rules]** een regel die is ingesteld om de afkapregels toe te passen op uw campagne. De reeksen van de kanaalregel van hefboomwerking staat u toe om frequentie het begrenzen door communicatie type te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen. [ leer hoe te met regelreeksen ](../conflict-prioritization/rule-sets.md) werken

+++

+++**Overeenkomst van het Spoor** (E-mail, SMS).

In de sectie **[!UICONTROL Action tracking]** kunt u bijhouden hoe de ontvangers op uw e-mail- of SMS-berichten reageren. De resultaten van het bijhouden van de campagne zijn toegankelijk vanuit het campagnerapport nadat de campagne is uitgevoerd. [ leer meer over campagnerapporten ](../reports/campaign-global-report-cja.md)

+++

+++**laat Snelle leveringswijze** toe (Duw).

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden. Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd. Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++**wijs prioritaire scores** toe (Web, in-app, op code-gebaseerd)

Wijs een prioritaire score aan de campagne toe staat u toe om aan een binnenkomende campagne voorrang te geven wanneer er een opgelegde beperking zoals een frequentiegrens is. Voer een numerieke waarde in (tussen 0 en 100). Let op: hoe hoger het getal, hoe hoger de prioriteit. [ Leer hoe te om prioritaire scores aan reizen &amp; campagnes toe te wijzen ](../conflict-prioritization/priority-scores.md)

+++

+++**plaats extra leveringsregels** (de kaarten van de Inhoud)

Voor inhoudskaartcampagnes kunt u aanvullende leveringsregels inschakelen om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. [ leer hoe te om inhoudskaarten ](../content-card/create-content-card.md) tot stand te brengen

+++

+++**bepaalt trekkers** (in-app)

Voor in-app berichten kunt u de knop **[!UICONTROL Edit triggers]** gebruiken om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren. [ Leer hoe te om een In-app bericht ](../in-app/create-in-app.md) te creëren

+++

## Meerdere binnenkomende handelingen toevoegen {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action"
>title="Meerdere binnenkomende handelingen toevoegen"
>abstract="U kunt meerdere binnenkomende acties selecteren in één campagne. Met deze functie kunt u meerdere op code gebaseerde ervaringen, In-app-berichten, Content Cards of Web-acties tegelijk op verschillende locaties aanbieden, waarbij elke actie een specifieke inhoud bevat."

Om uw campagneorchestratie te vereenvoudigen, kunt u verscheidene binnenkomende acties binnen één enkele campagne bepalen, elke actie die een specifieke inhoud bevat.

>[!NOTE]
>
>Deze capaciteit is alleen beschikbaar voor binnenkomende kanalen. Uitgaande kanalen zoals E-mail worden momenteel niet ondersteund.

Met deze capaciteit kunt u verschillende op code gebaseerde ervaringen, In-app-berichten, Content Cards of Web-acties op verschillende locaties tegelijk aanbieden zonder dat u meerdere campagnes hoeft te maken. Het maakt de plaatsing van uw campagne gemakkelijker en staat voor vlottere rapportering toe, met alle gegevens geconsolideerd in één enkele campagne.

U kunt bijvoorbeeld een op code gebaseerde ervaring naar meerdere eindpunten met iets verschillende inhoud verzenden. Om dit te doen, creeer veelvoudige op code-gebaseerde acties binnen de zelfde campagne, elk met een verschillende eindpuntconfiguratie.

Voer de onderstaande stappen uit als u meerdere binnenkomende acties in een campagne wilt definiëren.

1. Selecteer een binnenkomende actie (**code-Gebaseerde ervaring**, **In-app bericht**, **Kaart van de Inhoud** of **Web**) van de **[!UICONTROL Actions]** sectie.

1. Selecteer de kanaalconfiguratie en definieer een specifieke inhoud voor die actie.

1. Gebruik de knop **[!UICONTROL Add action]** om een andere binnenkomende actie in de vervolgkeuzelijst te selecteren.

   ![](assets/create-campaign-multi-action.png){width="80%"}

1. Ga op dezelfde manier verder om meer acties toe te voegen. U kunt maximaal 10 binnenkomende acties toevoegen aan een campagne.

Zodra de campagne [ levend ](review-activate-campaign.md) is, worden alle acties gelijktijdig geactiveerd.

## Volgende stappen {#next}

Zodra uw actie van de campagne klaar is, kunt u zijn inhoud ontwerpen. [Meer informatie](campaign-content.md)
