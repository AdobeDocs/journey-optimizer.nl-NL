---
solution: Journey Optimizer
product: journey optimizer
title: Voer het IP-opwarmingsplan uit
description: Leer hoe te om een IP warmlopingsplan in werking te stellen en te controleren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 0%

---

# Voer het IP-opwarmingsplan uit {#ip-warmup-running}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* **[Voer het IP-opwarmingsplan uit](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## De fasen definiëren {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Soorten publiek selecteren om uit te sluiten"
>abstract="Selecteer het publiek uit andere campagnes die u van de huidige fase wilt uitsluiten."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Domeingroepen selecteren om uit te sluiten"
>abstract="Selecteer de domeinen die u van de huidige fase wilt uitsluiten."

U moet de campagne en het publiek op faseniveau associëren en zet sommige montages aan zoals nodig voor alle looppas verbonden aan één enkele creatieve/campagne

Op faseniveau, zorgt het systeem ervoor dat eerder gericht + nieuwe profielen worden opgenomen EN op iteratieniveau, zorgt het systeem ervoor dat elke looppas unieke profielen heeft en de telling past wat in plan wordt verklaard

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

## De uitvoeringen definiëren {#define-runs}

1. Selecteer een schema voor elke run. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Selecteer een eindtijd, wat eigenlijk het venster betekent waarbinnen we warmtekrachtcampagne kunnen uitvoeren voor het geval er vertragingen optreden in het uitvoeren van een publiek werk. Indien niet opgegeven, wordt geprobeerd op de begintijd te beginnen en te mislukken. Als er een eindtijd is opgegeven, wordt de runtime tussen dat venster uitgevoerd.

1. Activeer elke run. Zorg ervoor u een tijd vroeg genoeg plant om voor de segmentatietaak toe te laten om worden in werking gesteld. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Elke run moet ten minste 12 uur voor de werkelijke verzendtijd worden geactiveerd. Anders kan de segmentatie niet worden voltooid. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Als de uitvoering van de campagne niet is gestart, kunt u een uitvoering stoppen.<!--why?-->

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

## Het abonnement controleren

Een run kan de volgende statussen hebben<!--TBC with Medha-->:

* **[!UICONTROL Completed]**:
* **[!UICONTROL Failed]**:
* **[!UICONTROL Cancelled]**: u hebt de uitvoering gestopt voordat de uitvoering van de campagne is gestart.

Voordelen :

* De rapporten zullen op campagnereniveau met gelijkaardige mogelijkheden zoals vandaag blijven tonen. Maar het opwarmingsplan van het IP dient ook als een geconsolideerd rapport op één enkele plaats van hoeveel executies werden uitgevoerd enzovoort.

* Één enkele plaats om te beheren en te bekijken hoe IP warm vordert.

* Geconsolideerd rapport op creatief/campagnereniveau zoals alle voor een fase loopt