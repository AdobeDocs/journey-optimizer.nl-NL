---
solution: Journey Optimizer
product: journey optimizer
title: Een contentexperiment maken
description: Leer hoe u een content-experiment kunt maken in uw campagnes
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: inhoud, experiment, meerdere, publiek, behandeling
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 6999f52a3426aa252f31440189ba9d1a7118dd0a
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 1%

---

# Een inhoudexperiment maken {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Inhoudsexperiment"
>abstract="U kunt verkiezen om de berichtinhoud, onderwerp, of afzender te variëren om veelvoudige behandelingen te bepalen en de beste combinatie voor uw publiek te bepalen."

>[!NOTE]
>
>Alvorens met de Experimenteer van de Inhoud te beginnen, zorg ervoor dat uw rapporteringsconfiguratie voor uw douanedatasets wordt geplaatst. Meer informatie in [deze sectie](reporting-configuration.md).

Met het Journey Optimizer Content Experiment kunt u meerdere leveringsbehandelingen definiëren om te meten welke het beste presteert voor uw doelgroep. U kunt kiezen om de leveringsinhoud, het onderwerp, of de afzender te variëren. Het betrokken publiek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke het beste in termen van gespecificeerde metrisch werkt.

![](../rn/assets/do-not-localize/experiment.gif)


In het onderstaande voorbeeld is de leveringsdoelstelling opgesplitst in twee groepen, die elk 45% van de doelpopulatie vertegenwoordigen, en een holdoutgroep van 10%, die de levering niet zal ontvangen.

Elke persoon in het doelpubliek ontvangt één versie van een e-mail, met een onderwerpregel die één van de volgende twee is:

* een rechtstreekse bevordering van een aanbod van 10 % voor de nieuwe collectie en een afbeelding .
* de andere reclame maakt alleen reclame voor een speciale aanbieding zonder dat de 10 % korting zonder afbeelding wordt opgegeven .

Het doel is hier te zien of zullen de ontvangers met e-mail afhankelijk van het ontvangen experiment interactie aangaan. Daarom zullen wij kiezen **[!UICONTROL Email Opens]** als het primaire doel metrisch in deze Content Experiment.

![](assets/content_experiment.png)

## Uw campagne maken {#campaign-experiment}

1. Van de **[!UICONTROL Campaigns]** pagina, klikt u **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. Selecteer vervolgens het kanaal **[!UICONTROL Surface]** wilt gebruiken voor deze levering en klikt u op **[!UICONTROL Create]**. Raadpleeg voor meer informatie de [Kanaaloppervlakken](../configuration/channel-surfaces.md) pagina.

   In dit voorbeeld kiezen we ervoor een campagne te verzenden met e-mails.

   ![](assets/content_experiment_2.png)

1. Stel de **[!UICONTROL Properties]** van je levering:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Description]**

1. Bepaal het publiek om te richten. Om dit te doen, klik **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-doelgroepen weer te geven. [Meer informatie over publiek](../audience/about-audiences.md)

   In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. In de **[!UICONTROL Actions tracking]** , geeft u op of u wilt bijhouden hoe de ontvangers op uw levering reageren: u kunt klikken en/of openen bijhouden.

   De resultaten van het bijhouden van de campagne zijn toegankelijk via het campagnerapport nadat de campagne is uitgevoerd.

1. Om uw campagne op een specifieke datum of op een terugkomende frequentie uit te voeren, vorm **[!UICONTROL Schedule]** sectie. [Meer informatie](create-campaign.md)

1. Klikken **[!UICONTROL Edit content]** om uw levering aan te passen.

   ![](assets/content_experiment_17.png)

1. Van de **[!UICONTROL Edit content]** begin de behandeling A aan te passen.

   Voor deze behandeling zullen wij het speciale aanbod rechtstreeks in de onderwerpregel specificeren en personalisatie toevoegen.

   ![](assets/content_experiment_5.png)

## Uw inhoudexperiment configureren {#configure-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_dimension"
>title="Dimension"
>abstract="Kies de specifieke dimensie die u wilt bijhouden voor uw expert, zoals specifieke kliks of weergaven van specifieke pagina&#39;s."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_success_metric"
>title="Metrisch met succes"
>abstract="Succesvolle maatstaf wordt gebruikt om de best presterende behandeling in een experiment bij te houden en te evalueren. Ben zeker aan opstelling uw dataset voor bepaalde metriek alvorens het te gebruiken."

1. Wanneer uw bericht wordt gepersonaliseerd, van de pagina van het campagneresamenvatting, klik **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren.

   ![](assets/content_experiment_3.png)

1. Selecteer de **[!UICONTROL Success metric]** u wilt instellen voor uw experiment.

   In dit voorbeeld selecteert u **[!UICONTROL Email open]** om te testen of profielen hun e-mails openen als de promotiecode zich op de onderwerpregel bevindt.

   ![](assets/content_experiment_11.png)

1. Wanneer u een experiment instelt met de In-app of het webkanaal en de optie **[!UICONTROL Inbound Clicks]**, **[!UICONTROL Unique Inbound Clicks]** , **[!UICONTROL Page Views]** , of **[!UICONTROL Unique Page Views metrics]** de **[!UICONTROL Click Action]**  kunt u klikken en weergaven op specifieke pagina&#39;s nauwkeurig bijhouden en controleren.

   ![](assets/content_experiment_20.png)

1. Klikken **[!UICONTROL Add treatment]** zoveel nieuwe behandelingen te creëren als nodig is.

   ![](assets/content_experiment_8.png)

1. Wijzig de **[!UICONTROL Title]** van uw behandeling om ze beter te onderscheiden.

1. Kies of u een **[!UICONTROL Holdout]** groeperen voor levering. Deze groep zal geen inhoud van deze campagne ontvangen.

   Als u de schakelbalk inschakelt, neemt dit automatisch 10% van uw bevolking in beslag. Indien nodig kunt u dit percentage aanpassen.

   ![](assets/content_experiment_12.png)

1. Vervolgens kunt u een exact percentage toewijzen aan elk **[!UICONTROL Treatment]** of schakelt u gewoon de **[!UICONTROL Distribute evenly]** schakelbalk.

   ![](assets/content_experiment_13.png)

1. Klikken **[!UICONTROL Create]** wanneer uw configuratie wordt geplaatst.

## Uw behandelingen ontwerpen {#treatment-experiment}

1. Van de **[!UICONTROL Edit content]** Selecteer uw behandeling B om de inhoud te wijzigen.

   Hier kiezen we ervoor het aanbod niet op te geven in het **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_18.png)

1. Klikken **[!UICONTROL Edit email body]** om uw behandeling verder aan te passen B.

   ![](assets/content_experiment_9.png)

1. Na het ontwerpen van uw behandelingen klikt u op **[!UICONTROL More actions]** voor toegang tot opties met betrekking tot uw behandelingen: **[!UICONTROL Rename]**, **[!UICONTROL Duplicate]** en **[!UICONTROL Delete]**.

   ![](assets/content_experiment_7.png)

1. Indien nodig, toegang tot **[!UICONTROL Experiment settings]** om de configuratie van uw behandelingen te wijzigen.

   ![](assets/content_experiment_19.png)

1. Als de inhoud van het bericht is gedefinieerd, klikt u op de knop **[!UICONTROL Simulate content]** om de rendering van uw levering te beheren en personalisatie-instellingen te controleren met testprofielen. [Meer informatie](../email/preview.md)

1. Wanneer uw inhoudexperiment gereed is, kunt u vanuit de overzichtspagina van de campagne op **[!UICONTROL Review to activate]** om een overzicht van de campagne weer te geven. Waarschuwt de weergave als een parameter onjuist is of ontbreekt.

   ![](assets/content_experiment_15.png)

1. Controleer of uw campagne correct is geconfigureerd en klik vervolgens op **[!UICONTROL Activate]** om het te starten.

   ![](assets/content_experiment_14.png)

Na het vormen van uw experimenteren en campagne, kunt u het succes van uw levering met het rapport van de Campagne volgen. [Meer informatie](../reports/campaign-global-report.md#experimentation-report)
