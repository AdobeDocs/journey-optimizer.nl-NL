---
solution: Journey Optimizer
product: journey optimizer
title: De transportactiviteit Handelingen gebruiken
description: Leer hoe te om een generische activiteit van de Actie toe te voegen om enige acties en multi-actie binnenkomende actiegroepen binnen het reiscanvas te vormen.
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: reis, bericht, push, sms, e-mail, in-app, web, inhoudskaart, op code gebaseerde ervaring
exl-id: 0ed97ffa-8efc-45a2-99ae-7bcb872148d5
source-git-commit: e8f7f5862e3816481680fa999657ae90334ff888
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 0%

---

# De activiteit Handeling gebruiken {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_action_activity"
>title="Actie"
>abstract="De generische **activiteit van de Actie** laat u één enkele inheemse kanaalactie en veelvoudige binnenkomende activiteiten met de capaciteit vormen om optimalisering aan om het even welke ingebouwde kanaalactie toe te voegen."

>[!AVAILABILITY]
>
>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

[!DNL Journey Optimizer] komt met een nieuwe generische **actie** activiteit die toestaat om één enkele ingebouwde kanaalactie, en ook veelvoudige binnenkomende activiteiten te vormen.

Het maakt het mogelijk:

* Een vereenvoudigde native actieconfiguratie binnen het reiscanvas.
* De capaciteit om multi-actie binnenkomende actiegroepen te creëren.
* De mogelijkheid om optimalisatie toe te voegen aan ingebouwde kanaalacties.

>[!NOTE]
>
>U kunt ook aangepaste handelingen instellen om uw berichten te verzenden in [!DNL Journey Optimizer] . [Meer informatie](#recommendation)

## Een actie toevoegen aan een reis  {#add-action}

Volg onderstaande stappen om een ingebouwde kanaalactie aan een reis toe te voegen.

1. Begin uw reis met een [ Gebeurtenis ](general-events.md) of a [ gelezen activiteit van het publiek ](read-audience.md).

1. Sleep vanuit de sectie **[!UICONTROL Actions]** van het palet een **[!UICONTROL Action]** -activiteit naar het canvas.

1. Selecteer de ingebouwde kanaalactiviteit u in uw reis wilt gebruiken.

   ![](assets/journey-action-type-cbe.png)

1. Voeg een label toe aan de handeling en selecteer **[!UICONTROL Configure action]** .

   ![](assets/journey-action-configure.png){width="80%"}

1. U wordt geleid aan het **[!UICONTROL Actions]** lusje van het de configuratiescherm van de reisactie.

   Selecteer de configuratie die u voor het geselecteerde kanaal wilt gebruiken.

   ![](assets/journey-action-actions-tab.png)

1. Als u een binnenkomend kanaal hebt geselecteerd, kunt u meerdere acties toevoegen. [Meer informatie](#multi-action)

1. Configureer uw activiteit volgens het geselecteerde kanaal. Leer hoe te om ingebouwde kanaalacties in [ te vormen deze sectie ](journeys-message.md).

1. Gebruik de sectie **[!UICONTROL Optimization]** om inhoudexperimenten uit te voeren, of hefboomwerking het richten van regels, of geavanceerde combinaties van zowel experimenteren als richten te gebruiken.

   Deze verschillende opties en de te volgen stappen zijn gedetailleerd in [ deze sectie ](../campaigns/campaigns-message-optimization.md).

1. Gebruik de sectie **[!UICONTROL Languages]** om inhoud in meerdere talen te maken binnen de actie. Klik hiertoe op de knop **[!UICONTROL Add languages]** en selecteer de gewenste **[!UICONTROL Language settings]** .

   De gedetailleerde informatie over hoe te opstelling en gebruik meertalige mogelijkheden zijn beschikbaar in [ deze sectie ](../content-management/multilingual-gs.md).

Afhankelijk van het geselecteerde communicatiekanaal zijn aanvullende instellingen beschikbaar. Vouw de onderstaande secties uit voor meer informatie.

+++**pas het begrenzen regels** toe (E-mail, Directe post, Duw, SMS)

Selecteer in de vervolgkeuzelijst **[!UICONTROL Business rules]** een regel die is ingesteld om afdekkingsregels toe te passen op de actie die u uitvoert.

De reeksen van de kanaalregel van hefboomwerking staat u toe om frequentie het begrenzen door communicatie type te plaatsen om het overbelasten van klanten met gelijkaardige berichten te verhinderen.

[Leer hoe u met regelsets werkt](../conflict-prioritization/rule-sets.md)

+++

+++**Overeenkomst van het Spoor** (E-mail, SMS).

In de sectie **[!UICONTROL Action tracking]** kunt u bijhouden hoe de ontvangers op uw e-mail- of SMS-berichten reageren.

De trackingresultaten zijn toegankelijk vanaf het reisverslag zodra de reis is uitgevoerd.

[Meer informatie over reisrapporten](../reports/journey-global-report-cja.md)

+++

+++**laat Snelle leveringswijze** toe (Duw).

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

+++

+++**wijs prioritaire scores** toe (Web, in-app, op code-gebaseerd)

In de **[!UICONTROL Conflict management]** sectie, kunt u een prioritaire score aan de reisactie toewijzen, toestaand u om aan een binnenkomende actie voorrang te geven wanneer er veelvoudige reisacties of campagnes gebruikend de zelfde kanaalconfiguratie zijn.

Standaard wordt de prioriteitsscore voor de actie overgenomen van de algemene prioriteitsscore voor de reis.

[Leer hoe u prioriteitsscores kunt toewijzen aan kanaalhandelingen](../conflict-prioritization/priority-scores.md#priority-action)

+++

+++**plaats extra leveringsregels** (de kaarten van de Inhoud)

Voor reizen met een inhoudskaart kunt u aanvullende leveringsregels inschakelen om de gebeurtenis(sen) en criteria te kiezen die het bericht activeren.

[Leer hoe u inhoudskaarten maakt](../content-card/create-content-card.md)

+++

+++**bepaalt trekkers** (in-app)

Voor in-app berichten kunt u de knop **[!UICONTROL Edit triggers]** gebruiken om de gebeurtenis(sen) en criteria te kiezen die uw bericht activeren.

[Leer hoe u een bericht in de app maakt](../in-app/create-in-app.md)

+++

## Meerdere binnenkomende handelingen toevoegen {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action_journey"
>title="Meerdere binnenkomende handelingen toevoegen"
>abstract="U kunt verschillende binnenkomende acties selecteren binnen één enkele reis. Met deze functie kunt u meerdere op code gebaseerde ervaringen, In-app-berichten, Content Cards of Web-acties tegelijk op verschillende locaties aanbieden, waarbij elke actie een specifieke inhoud bevat."

Om uw reis orchestratie te vereenvoudigen, kunt u verscheidene binnenkomende acties binnen één enkele reisactie bepalen.

>[!NOTE]
>
>Deze capaciteit is alleen beschikbaar voor binnenkomende kanalen. Uitgaande kanalen zoals E-mail worden momenteel niet ondersteund.

Met deze capaciteit kunt u verschillende op code gebaseerde ervaringen, In-app-berichten, Content Cards of Web-acties op verschillende locaties tegelijk aanbieden, zonder dat u meerdere reisacties hoeft te maken. Het maakt de inzet van uw reis gemakkelijker en maakt een vlottere rapportering mogelijk, waarbij alle gegevens in één enkele reis worden geconsolideerd.

U kunt bijvoorbeeld een op code gebaseerde ervaring naar meerdere eindpunten met iets verschillende inhoud verzenden. Om dit te doen, creeer veelvoudige code-gebaseerde acties binnen de zelfde reisactie, elk met een verschillende eindpuntconfiguratie.

Volg de onderstaande stappen om meerdere binnenkomende acties in één knooppunt voor handelingen tijdens de rit te definiëren.

1. Begin uw reis met een [ Gebeurtenis ](general-events.md) of a [ gelezen activiteit van het publiek ](read-audience.md).

1. Sleep vanuit de sectie **[!UICONTROL Actions]** van het palet een **[!UICONTROL Action]** -activiteit naar het canvas.

1. Selecteer **[!UICONTROL Multi action]** als actietype.

   ![](assets/journey-multi-action.png)

1. Voeg indien nodig een label toe en selecteer **[!UICONTROL Configure action]** .

   ![](assets/journey-multi-action-configure.png){width="60%"}

1. U wordt geleid aan het **[!UICONTROL Actions]** lusje van het de configuratiescherm van de reisactie.

   ![](assets/journey-multi-action-configuration.png){width="70%"}

1. Selecteer een binnenkomende actie (**code-Gebaseerde ervaring**, **In-app bericht**, **Kaart van de Inhoud** of **Web**) van de **[!UICONTROL Actions]** sectie.

1. Selecteer de kanaalconfiguratie en definieer een specifieke inhoud voor die actie.

1. Gebruik de knop **[!UICONTROL Add action]** om een andere binnenkomende actie in de vervolgkeuzelijst te selecteren.

   ![](assets/journey-multi-action-add.png){width="80%"}

1. Ga op dezelfde manier verder om meer acties toe te voegen. U kunt tot 10 binnenkomende acties in een groep van de reisactie toevoegen.

Zodra de reis [&#128279;](publishing-the-journey.md) levend is, worden alle acties gelijktijdig geactiveerd.
<!--
## Next steps {#next}

Once your action is configured, you can design its content. [Learn more]-->
