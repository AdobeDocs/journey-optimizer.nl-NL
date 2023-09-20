---
solution: Journey Optimizer
product: journey optimizer
title: Voer een IP warmlopingsplan uit
description: Leer hoe te om een IP warmup plan uit te voeren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: 1ac68f1b3a9657ce71a653011ab92fb817ca80b0
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 1%

---

# Voer een IP warmlopingsplan uit {#ip-warmup}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!AVAILABILITY]
>
>De IP warmup eigenschap is momenteel beschikbaar als bèta om gebruikers slechts te selecteren. Neem contact op met de klantenservice van de Adobe om deel te nemen aan het bètaprogramma.

Met [!DNL Journey Optimizer], kunt u IP warmteopwerkschema&#39;s op een gestandaardiseerde en efficiënte manier direct van het gebruikersinterface uitvoeren die de beste praktijken voor optimale leverbaarheid volgt.

>[!CAUTION]
>
>Deze functie geldt alleen voor het e-mailkanaal.

Wanneer e-mails met een nieuw platform worden verzonden, zijn internetproviders (ISP&#39;s) verdacht van IP-adressen die niet worden herkend. Als er plotseling grote hoeveelheden e-mails worden verzonden, markeren de ISP&#39;s deze vaak als spam.

Als u wilt voorkomen dat spam wordt gemarkeerd, kunt u het verzonden volume progressief verhogen met de functie voor IP-warmteopruimingsplannen. Met een nieuwe optie in het menu Beheer kunt u dit gemakkelijker doen in plaats van complexe reizen te maken. Dit zou een vlotte ontwikkeling van de startfase moeten verzekeren en u toelaten om het algemene tarief van ongeldige adressen te verminderen.

>[!NOTE]
>
>Meer weten over het verbeteren van je e-mailreputatie dankzij de opwarming van de IP in [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Here are the main steps:

1. You get a deliverability plan from the deliverability consulting team.

1. Create a campaign - marketer [Learn more](#create-ip-warmup-campaign)

1. Your associated practitioner (customer's practitioner/ACS consultant/partner consultant) creates a IP warmup object in project and uploads a plan.

    The CSV manifests itself like below with numbers showing up with/without domain bifurcation. Below screen shows one phase (creative) with associated runs (The plan obviously has more such phases)

1. Practitioner associates the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

1. Then start to execute on every day basis by simply clicking the play button

1. Reports will continue to show up at campaign level with similar capabilities as today. NO enhancements in BETA. But the IP warmup plan also serves as a consolidated report at one single place of how many executions were done and so on

Benefits are as follows:

* No more creation of daily journeys and associated testing

* Standardization on Campaign which will be easy for practitioners too

* No more pain of creating queries, audiences and testing those as system will create the audiences. At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* Single place to manage and view how IP warm is progressing.

* Consolidated report at creative/campaign level as all runs for a phase 

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

De belangrijkste stappen om een IP opwarmingsplan uit te voeren zijn als volgt:

* [IP-warmtecampagnes maken](#create-ip-warmup-campaign)
* [Een IP-opwarmingsplan definiëren](#define-ip-warmup-plan)

## IP-warmtecampagnes maken {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activeer de IP optie van het warmlopingsplan"
>abstract="Selecteer de optie voor activering van het IP-opwarmingsplan. Zodra de campagne levend is, kan het met een IP warmlopingsplan worden geassocieerd."

U moet één of meerdere campagnes met een specifieke toegelaten optie tot stand brengen zodat zij in een IP warmup plan kunnen worden gebruikt. Voer de onderstaande stappen uit.

1. Een [oppervlak](channel-surfaces.md) voor het domein en IPs die u voor uw warmlopingsplan hebt geïdentificeerd.

1. Een [campagne](../campaigns/create-campaign.md) en selecteert u de [E-mail](../email/create-email.md#create-email-journey-campaign) handeling.

1. Selecteer de oppervlakte die u voor IP warmte-up creeerde.

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Klik op **[!UICONTROL Create]**.

1. Selecteer in de sectie **[!UICONTROL Schedule]** de optie **[!UICONTROL IP warmup plan activation]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   De campagne [schema](../campaigns/create-campaign.md#schedule) zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald.

1. [Activeren](../campaigns/review-activate-campaign.md) de campagne. Zodra levend, is het klaar voor gebruik in een IP warmup plan.

>[!NOTE]
>
>Voor een levende campagne met IP warmup plan geactiveerd, **[!UICONTROL Delete]** de knoop is beschikbaar tot het met een IP warmup plan wordt geassocieerd.

Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

## Een IP-opwarmingsplan definiëren {#define-ip-warmup-plan}

### IP-opwarmingsplannen beheren {#manage-ip-warmup-plans}

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]**. Alle IP warmup die plannen tot nu toe worden gecreeerd worden getoond.

   ![](assets/ip-warmup-filter-list.png)

1. U kunt filteren op de status. De verschillende statussen zijn:

   * **Niet gestart**: er is geen run uitgevoerd
   * **In uitvoering**: zodra een run is gestart <!--or is done?-->
   * **Gepauzeerd**
   * **Voltooid**: alle uitvoeringen in het plan zijn uitgevoerd

1. Om een IP warmup plan te schrappen, selecteer **[!UICONTROL Delete]** naast een lijstitem en het verwijderen bevestigen.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Het geselecteerde IP warmup plan zal permanent worden geschrapt.

### Creeer een IP warmlopingsplan {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specificeer uw IP warmtekrachtplan"
>abstract="Download het malplaatje CSV en vul het met gegevens voor IP warmup fasen en doelaantal profielen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Een marketingoppervlak selecteren"
>abstract="U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="Kanaaloppervlakken instellen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="IP-warmtecampagnes maken"

>[!CAUTION]
>
>Om IP warmup plannen tot stand te brengen, uit te geven en te schrappen, moet u hebben **[!UICONTROL Deliverability Consultant]** toestemming.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

Wanneer een of meer live campagnes met de **[!UICONTROL IP warmup plan activation]** toegelaten optie wordt geactiveerd, kunt u hen met een IP warmlopingsplan associëren.

>[!CAUTION]
>
>Werk samen met uw leverancier om ervoor te zorgen dat uw IP het malplaatje van het warmlopingsplan correct opstelling is. <!--TBC-->

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** en klik vervolgens op **[!UICONTROL Create IP warmup plan]**.

   ![](assets/ip-warmup-create-plan.png)

1. Vul de IP details van het warmlopingsplan in: geef het een naam en een beschrijving.

   ![](assets/ip-warmup-plan-details.png)

1. Selecteer een [oppervlak](channel-surfaces.md). Alleen marketingoppervlakken zijn beschikbaar voor selectie. [Meer informatie over e-mailtypen](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >U moet de zelfde oppervlakte selecteren zoals die in de campagne wordt geselecteerd u met uw IP warmup plan wilt associëren. [Leer hoe te om een IP warmup campagne te creëren](#create-ip-warmup-campaign)

1. Upload het dossier van Excel dat uw IP warmup plan bevat<!--which formats are allowed?-->. U kunt de sjabloon gebruiken die door het leveringsteam wordt aangeboden.<!--TBC?--> [Meer informatie](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Klik op **[!UICONTROL Create]**. Het aantal fasen dat is gedefinieerd in het bestand dat u hebt geüpload, wordt automatisch weergegeven voor elke fase. [Meer informatie](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### Upload een IP warmup plan opnieuw {#re-upload-plan}

U kunt een ander IP warmlopingsplan opnieuw uploaden gebruikend de overeenkomstige knoop.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>De IP details van het warmup plan zullen veranderen zoals per het onlangs geupload dossier. De volledige looppas en de geactiveerde looppas worden niet beïnvloed.

### Het bestand met het abonnement uploaden {#upload-plan}

Hieronder is een voorbeeld van een dossier dat een IP warmlopingsplan bevat.

![](assets/ip-warmup-sample-file.png)

Elke fase komt overeen met een periode die bestaat uit meerdere uitvoeringen, waaraan u één campagne toewijst.

Voor elke run hebt u een bepaald aantal ontvangers en u zult een datum definiëren waarop deze run wordt uitgevoerd.

U kunt zoveel kolommen hebben als u wilt voor de domeinen u aan wilt leveren. In dit voorbeeld hebt u drie kolommen: Gmail, Adobe en andere. Dit houdt in dat

Het idee is meer looppas in de eerste fasen te hebben en het aantal gerichte adressen geleidelijk te verhogen terwijl het verminderen van het aantal looppas.

### De fasen definiëren {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Soorten publiek selecteren om uit te sluiten"
>abstract="Selecteer het publiek uit andere campagnes die u van de huidige fase wilt uitsluiten."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Domeingroepen selecteren om uit te sluiten"
>abstract="Selecteer de domeinen die u van de huidige fase wilt uitsluiten."

1. Voor elke fase, selecteer de campagne u met deze fase van het IP warmup plan wilt associëren.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Let op het volgende:

   * Alleen de campagnes met de **[!UICONTROL IP warmup plan activation]** optie ingeschakeld <!--and live?--> zijn beschikbaar voor selectie. [Meer informatie](#create-ip-warmup-campaign)

   * U moet een campagne selecteren die de zelfde oppervlakte gebruikt zoals die voor het huidige IP warmup plan wordt geselecteerd.

   * U kunt geen campagne selecteren die reeds in gebruik in een andere IP opwarmingscampagne is.

1. Voor elke fase geldt het volgende:

   * **[!UICONTROL Profile exclusion]** - De profielen uit de vorige fasen van die fase zijn altijd uitgesloten. Bijvoorbeeld, als op run #1 Leo behandeld werd in de eerste 6300 mensen die worden gericht, zal het systeem automatisch ervoor zorgen dat Leo de post niet krijgt in looppas #2.

   * **[!UICONTROL Campaign audiences excluded]** - Selecteer een publiek uit een ander publiek <!--executed/live?-->campagnes die u van de huidige fase wilt uitsluiten.

     U kunt bijvoorbeeld een fase uitvoeren en deze om welke reden dan ook splitsen. In een dergelijk geval, in fase 2, zou u de campagne willen omvatten die in fase 1 in deze sectie wordt gebruikt zodat in fase 2, eerder gecontacteerde mensen van fase 1 niet inbegrepen zijn. Dit kan niet alleen met campagnes worden gedaan die in zelfde IP warmup plan maar ook van een ander IP warmup plan worden gebruikt.

   * **[!UICONTROL Domains groups excluded]** - Selecteer de domeinen u van die fase, bijvoorbeeld Gmail wilt uitsluiten. <!--??-->

     Na het runnen van IP warmte voor sommige dagen, realiseert u dat ISP reputatie met een domein zeg hotmail niet goed is en u wenst om het met ISP op te lossen maar wenst niet om IP warmup plan tegen te houden. In dat geval kunt u de telefonische hotmail voor de domeingroep in de uitgesloten categorie plaatsen.

     >[!NOTE]
     >
     >De uitsluiting van het domein vereist een niet-uitgevoerde fase zodat kunt u een lopende fase moeten verdelen om uitsluitingen toe te voegen. Op dezelfde manier als domeingroep geen OOTB domeingroep is, dan kunt u domeingroep in Excel moeten tot stand brengen en uploaden en dan het zelfde uitsluiten.

   ![](assets/ip-warmup-plan-phase-1.png)

1. U kunt desgewenst een fase toevoegen. Deze fase wordt toegevoegd na de laatste huidige fase. Gebruik de **[!UICONTROL Delete phase]** om ongewenste fase te verwijderen.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >U kunt de opdracht **[!UICONTROL Delete]** handeling.
   >
   >Als u alle fasen van het IP warmlopingsplan schrapt, adviseren wij om een plan opnieuw te uploaden.

### De uitvoeringen definiëren {#define-runs}

1. Selecteer een schema voor elke run. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Selecteer een eindtijd, wat eigenlijk het venster betekent waarbinnen we warmtekrachtcampagne kunnen uitvoeren voor het geval er vertragingen optreden in het uitvoeren van een publiek werk. Indien niet opgegeven, wordt geprobeerd op de begintijd te beginnen en te mislukken. Als er een eindtijd is opgegeven, wordt de runtime tussen dat venster uitgevoerd.

1. Activeer elke run. Zorg ervoor u een tijd vroeg genoeg plant om voor de segmentatietaak toe te laten om worden in werking gesteld. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Elke run moet ten minste 12 uur voor de werkelijke verzendtijd worden geactiveerd. Anders kan de segmentatie niet worden voltooid. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

1. Als de uitvoering van de campagne niet is gestart, kunt u een uitvoering stoppen.

   Nadat de uitvoering van de campagne is gestart, **[!UICONTROL Stop]** wordt niet meer beschikbaar. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Als u een uitvoering wilt toevoegen, selecteert u **[!UICONTROL Add a run below]** van het pictogram met drie punten.

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. Als u op elk gewenst moment een andere campagne wilt gebruiken die begint bij een specifieke uitvoering, selecteert u de optie **[!UICONTROL Split to a new phase option]** van het pictogram met drie punten. Er wordt een nieuwe fase gemaakt voor de resterende uitvoeringen van de huidige fase. Voer de stappen uit [boven](#define-phases) de nieuwe fase te definiëren.

   Als u deze optie bijvoorbeeld selecteert voor uitvoering #4, worden de stappen #4 tot en met #8 verplaatst naar een nieuwe fase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

Een run kan de volgende statussen hebben<!--TBC with Medha-->:

* **[!UICONTROL Completed]**:
* **[!UICONTROL Failed]**:
* **[!UICONTROL Cancelled]**: u hebt de uitvoering gestopt voordat de uitvoering van de campagne is gestart.

