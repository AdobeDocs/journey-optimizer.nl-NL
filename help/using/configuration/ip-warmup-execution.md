---
solution: Journey Optimizer
product: journey optimizer
title: Voer het IP-opwarmingsplan uit
description: Leer hoe te om een IP warmlopingsplan in werking te stellen en te controleren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Voer het IP warmlopingsplan uit {#ip-warmup-running}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarming](ip-warmup-gs.md)
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* **[Voer het IP warmlopingsplan uit](ip-warmup-execution.md)**

>[!ENDSHADEBOX]

Als u eenmaal [leidde tot een IP warmup plan](ip-warmup-plan.md) en het bestand geüpload dat u samen met uw leverancier hebt voorbereid, kunt u de fasen en uitvoering in uw abonnement definiëren.

Elke fase bestaat uit verschillende uitvoeringen, waaraan u één campagne toewijst.

## De fasen definiëren {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Campagnepubliek uitsluiten"
>abstract="Selecteer het publiek uit andere campagnes die u van de huidige fase wilt uitsluiten. Dit moet eerder gecontacteerde profielen van andere fasen of andere IP opwarmingsplannen verhinderen opnieuw worden gericht."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Domeingroepen uitsluiten"
>abstract="Selecteer de domeinen die u van de huidige fase wilt uitsluiten. De uitsluiting van het domein vereist een niet-uitgevoerde fase, zodat kunt u een lopende fase moeten verdelen om uitsluitingen toe te voegen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-running.html#split-phase" text="Een fase splitsen"

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. Voor elke fase, selecteer de campagne u met deze fase van het IP warmup plan wilt associëren.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Let op het volgende:

   * Alleen de campagnes met de **[!UICONTROL IP warmup plan activation]** optie ingeschakeld <!--and live?--> zijn beschikbaar voor selectie. [Meer informatie](#create-ip-warmup-campaign)

   * U moet een campagne selecteren die de zelfde oppervlakte gebruikt zoals die voor het huidige IP warmup plan wordt geselecteerd.

   * U kunt geen campagne selecteren die reeds in gebruik in een andere IP opwarmingscampagne is.

1. In de **[!UICONTROL Profile exclusion]** kunt u zien dat de profielen van de vorige reeksen van die fase altijd worden uitgesloten. Als in Run #1 bijvoorbeeld een profiel in de eerste 4800 doelgroepen is opgenomen, zorgt het systeem er automatisch voor dat hetzelfde profiel de e-mail niet ontvangt in Run #2.

1. Van de **[!UICONTROL Campaign audiences excluded]** selecteert u het publiek uit andere <!--executed/live?-->campagnes die u van de huidige fase wilt uitsluiten.

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   Tijdens het uitvoeren van Fase 1 moest u bijvoorbeeld [splitsen](#split-phase) om welke reden dan ook. Daarom kunt u de campagne uitsluiten die in Fase 1 wordt gebruikt, zodat de eerder gecontacteerde profielen van Fase 1 niet inbegrepen in Fase 2 zijn. U kunt campagnes van andere IP warmteopnameplannen ook uitsluiten.

1. Van de **[!UICONTROL Domain groups excluded]** selecteert u de domeinen die u van die fase wilt uitsluiten.

   >[!NOTE]
   >
   >Domeinuitsluiting vereist een niet-uitgevoerde fase, zodat u mogelijk [een actieve fase splitsen](#split-phase) uitsluitingen toevoegen.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Bijvoorbeeld, na het runnen van IP warmte voor sommige dagen, realiseert u dat uw ISP reputatie met een domein (bijvoorbeeld, Adobe) niet goed is en u wenst om het op te lossen zonder uw IP warmup plan tegen te houden. In dat geval kunt u de Adobe-domeingroep uitsluiten.

   >[!NOTE]
   >
   >Als het domein geen uit-van-de-doos domeingroep is, moet u met uw leverbaarheidsadviseur werken om dit domein aan toe te voegen [IP het dossier van het opwarmingsplan](ip-warmup-plan.md#prepare-file) en [uploaden](#re-upload-plan) om dat domein uit te sluiten.

1. U kunt desgewenst een fase toevoegen. Het zal na de laatste huidige fase worden toegevoegd.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Gebruik de **[!UICONTROL Delete phase]** om ongewenste fase te verwijderen.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!CAUTION]
   >
   >U kunt de opdracht **[!UICONTROL Delete]** handeling.
   >
   >Als u alle fasen van het IP warmlopingsplan schrapt, wordt het geadviseerd om een plan opnieuw te uploaden. [Meer informatie](#re-upload-plan)

## De uitvoeringen definiëren {#define-runs}

1. Selecteer een schema voor elke run.

   ![](assets/ip-warmup-plan-send-time.png)

1. Optioneel, kunt u een tijdvenster bepalen waarin de IP warmup campagne kan worden uitgevoerd in het geval dat er om het even welke vertragingen in de segmentatietaak zijn. Als u dit wilt doen, klikt u op het pictogram Eigenschappen linksboven, naast de naam van het plan en gebruikt u de knop **[!UICONTROL Retry run time]** vervolgkeuzelijst voor het selecteren van een duur tot 240 minuten (4 uur).

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Als u bijvoorbeeld een verzendtijd instelt op een bepaalde dag om 21.00 uur en 120 minuten selecteert als de runtime voor opnieuw proberen, is dit een periode van 2 uur voor de uitvoering van de segmentatietaak.

   >[!NOTE]
   >
   >Als geen tijdvenster wordt gespecificeerd, wordt de looppas geprobeerd bij verzendtijd en zal ontbreken als de segmentatietaak niet wordt voltooid.

1. Selecteer indien nodig **[!UICONTROL Edit run]** in het pictogram Meer handelingen. Daar kunt u de aantallen adressen in elke kolom bijwerken. U kunt ook de **[!UICONTROL Last engagement]** in het veld alleen te gebruiken voor de gebruikers die bijvoorbeeld de afgelopen 20 dagen met uw merk hebben gewerkt.

   ![](assets/ip-warmup-plan-edit-run.png)

1. Selecteer de **[!UICONTROL Pause for errors]** als u de uitvoering wilt pauzeren voor het geval er een fout optreedt.<!--can't see the Paused status for runs? Is it failed?-->

   ![](assets/ip-warmup-plan-pause.png)

   Als het beoogde aantal profielen lager is dan verwacht, wordt de uitvoering geannuleerd nadat de segmentatietaak is uitgevoerd.

1. **[!UICONTROL Activate]** de run. Zorg ervoor dat u voldoende tijd hebt gepland om de segmentatietaak uit te voeren.

   ![](assets/ip-warmup-plan-activate.png)

   >[!CAUTION]
   >
   >Elke run moet ten minste 12 uur voor de werkelijke verzendtijd worden geactiveerd. Anders kan de segmentatie niet worden voltooid. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

   <!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

1. De status van deze uitvoering verandert in **[!UICONTROL Live]**. De verschillende uitvoerstatussen worden vermeld in [deze sectie](#monitor-plan). Als de uitvoering van de campagne niet is gestart, kunt u een live run stoppen.<!--why?-->

   ![](assets/ip-warmup-plan-stop-run.png)

   >[!NOTE]
   >
   >Nadat de uitvoering van de campagne is gestart, **[!UICONTROL Stop]** wordt niet meer beschikbaar.

1. Als u een uitvoering wilt toevoegen, selecteert u **[!UICONTROL Add a run below]** van het pictogram met drie punten.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Uw abonnement beheren {#manage-plan}

Op om het even welk punt, als uw IP warmup plan niet zoals verwacht presteert, kunt u de hieronder acties nemen.

### Een fase splitsen {#split-phase}

Als u een nieuwe fase wilt toevoegen die van een specifieke looppas begint, selecteer **[!UICONTROL Split to a new phase option]** van het pictogram met drie punten.

![](assets/ip-warmup-plan-run-split-run.png)

Er wordt een nieuwe fase gemaakt voor de resterende uitvoeringen van de huidige fase.

Als u deze optie bijvoorbeeld selecteert voor Run #4, worden Runs #4 tot en met #8 verplaatst naar een nieuwe fase.

Voer de stappen uit [boven](#define-phases) de nieuwe fase te definiëren.

* U kunt de **[!UICONTROL Replace campaign]** voor die nieuwe fase.

* U kunt ook de vorige campagne uitsluiten, of een domein dat niet goed presteert. Meer informatie over [deze sectie](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Een abonnement markeren als voltooid {#mark-as-completed}

Als uw plan niet goed genoeg presteert of als u het wilt laten vallen om een andere te creëren, kunt u het merken zoals voltooid.

Klik hiertoe op de knop **[!UICONTROL More]** knoop op hoogste recht van het IP warmup plan en selecteer **[!UICONTROL Mark as completed]**.

![](assets/ip-warmup-plan-mark-completed.png)

Deze optie is alleen beschikbaar als alle runnen in het abonnement zijn opgenomen **[!UICONTROL Completed]** of **[!UICONTROL Draft]** status. Als een run **[!UICONTROL Live]**, wordt de optie grijs weergegeven.

De verschillende uitvoerstatussen worden vermeld in [deze sectie](#monitor-plan).

### Upload een IP warmup plan opnieuw {#re-upload-plan}

Als uw IP warmup plan niet zoals verwacht uitvoert (bijvoorbeeld, als u opmerkt dat sommige ISPs uw berichten als spam) merkt, kunt u uw leverbaarheidsdeskundige vragen om opstelling een ander IP dossier van het warmup plan en herupload het gebruikend de overeenkomstige knoop.

![](assets/ip-warmup-re-upload-plan.png)

Alle eerder uitgevoerde looppas zal worden duidelijk aangezien voltooid. Het nieuwe plan wordt getoond onder het eerste plan.

Voer de stappen uit [boven](#define-phases) de fases van het nieuwe plan te bepalen.

>[!NOTE]
>
>De IP details van het warmup plan zullen veranderen zoals per het onlangs geupload dossier. Dit heeft geen invloed op de live en voltooide run.

## Het abonnement controleren {#monitor-plan}

Om het effect van uw plan te meten, kunt u de prestaties van uw IP warmup campagnes controleren gebruikend [!DNL Journey Optimizer] campagneverslagen. Om dit te doen, voor elke voltooide looppas kunt u klikken **[!UICONTROL View reports]** knop. Meer informatie over de campagne-e-mail [live-rapport](../reports/campaign-live-report.md#email-live) en [algemeen rapport](../reports/campaign-global-report.md##email-global).

![](assets/ip-warmup-plan-reports.png)

Het opwarmingsplan van het IP zelf dient ook als een geconsolideerd rapport op één enkele plaats. U kunt elementen controleren zoals het aantal **[!UICONTROL Live]** of **[!UICONTROL Completed]** looppas voor elke fase, en mening hoe uw IP warmup plan vordert.

Een run kan de volgende statussen hebben:

* **[!UICONTROL Draft]** : telkens wanneer een run wordt gemaakt, wanneer [het opstellen van een nieuw plan](ip-warmup-plan.md) of [toevoegen, run](#define-runs) vanuit de gebruikersinterface **[!UICONTROL Draft]** status.
* **[!UICONTROL Live]**: wanneer u een run activeert, neemt deze de **[!UICONTROL Live]** status.
* **[!UICONTROL Completed]**<!--TBC-->: de uitvoering van de campagne voor deze run is voltooid. <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL Cancelled]**: a **[!UICONTROL Live]** uitvoering is geannuleerd met de opdracht **[!UICONTROL Stop]** knop. Deze knop is alleen beschikbaar als de uitvoering van de campagne niet is gestart. [Meer informatie](#define-runs)
* **[!UICONTROL Failed]**: er is een fout aangetroffen door het systeem of de campagne die voor de huidige fase is gebruikt, is gestopt<!--what should the user do in that case?-->.
