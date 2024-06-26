---
solution: Journey Optimizer
product: journey optimizer
title: Voer het IP-opwarmingsplan uit
description: Leer hoe te om een IP warmlopingsplan in werking te stellen en te controleren
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: cd95614329e6efdc7ac4b6e0a5c683757a14b379
workflow-type: tm+mt
source-wordcount: '2462'
ht-degree: 0%

---

# Voer het IP warmlopingsplan uit {#ip-warmup-running}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Ga aan de slag met IP-opwarmingsplannen](ip-warmup-gs.md)
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
>abstract="Selecteer campagnes om hun publiek uit te sluiten van de huidige fase. Hierdoor wordt voorkomen dat eerder gecontacteerde profielen opnieuw worden aangewezen; alleen diegenen die via de reis hebben gecommuniceerd, worden uitgesloten."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Domeingroepen uitsluiten"
>abstract="Selecteer de domeinen die u van de huidige fase wilt uitsluiten. De uitsluiting van het domein vereist een niet-uitgevoerde fase, zodat kunt u een lopende fase moeten verdelen om uitsluitingen toe te voegen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html#split-phase" text="Een fase splitsen"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="Definieer de fasen van uw abonnement"
>abstract="Elke fase bestaat uit verschillende uitvoeringen, waaraan u één campagne toewijst."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. Selecteer de campagne u met de eerste fase van het IP opwarmingsplan wilt associëren.

   >[!NOTE]
   >
   >U kunt geen campagne selecteren die reeds in gebruik in een ander IP warmlopingsplan is. Nochtans, kan de zelfde campagne in één of meerdere fasen van het zelfde IP warmup plan worden gebruikt.

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* Alleen de campagnes met de **[!UICONTROL IP warmup plan activation]** ingeschakeld zijn beschikbaar voor selectie. [Meer informatie](#create-ip-warmup-campaign)
   >
   >* Slechts zijn de campagnes die de zelfde oppervlakte gebruiken zoals het geselecteerde IP warmup plan beschikbaar voor selectie.

1. Wanneer een campagne voor de huidige fase is geselecteerd, worden de secties voor het uitsluiten van profielen, campagnepubliek en domeingroepen weergegeven.

   >[!NOTE]
   >
   >Nadat een run is geactiveerd, kunnen de uitsluitingen niet meer worden gewijzigd, tenzij u [de uitvoering splitsen](#split-phase) naar een nieuwe fase.

   1. Van de **[!UICONTROL Domain groups excluded]** selecteert u de domeinen die u van die fase wilt uitsluiten.

      >[!NOTE]
      >
      >De uitsluiting van het domein vereist een niet uitgevoerde fase zodat zou u kunnen nodig hebben [een actieve fase splitsen](#split-phase) uitsluitingen toevoegen.

      ![](assets/ip-warmup-plan-exclude-domains.png)

      Bijvoorbeeld, na het runnen van IP warmte voor sommige dagen, realiseert u dat uw ISP reputatie met een domein (bijvoorbeeld, Adobe) niet goed is en u wenst om het op te lossen zonder uw IP warmup plan tegen te houden. In dat geval kunt u de Adobe-domeingroep uitsluiten.

      >[!NOTE]
      >
      >U kunt alleen een aangepaste domeingroep uitsluiten die is toegevoegd aan de [Sjabloon voor IP-opwarmingsplan](ip-warmup-plan.md#prepare-file). Als dit niet het geval is, werk het malplaatje met de groep van het douanedomein bij u wilt uitsluiten en [uploaden van het abonnement](#re-upload-plan).

   1. Van de **[!UICONTROL Campaign for exclusion of profiles]** selecteert u de campagnes die u wilt uitsluiten van de huidige fase.

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      Tijdens het uitvoeren van Fase 1 moest u bijvoorbeeld [splitsen](#split-phase) om welke reden dan ook. Daarom kunt u de campagne uitsluiten die in Fase 1 wordt gebruikt, zodat de eerder gecontacteerde profielen van Fase 1 niet inbegrepen in Fase 2 zijn. U kunt campagnes van andere IP warmteopnameplannen ook uitsluiten.

   1. Van de **[!UICONTROL Journeys for exclusion of profiles]** selecteert u de ritten met het publiek dat u wilt uitsluiten van de huidige fase.

+++ Als u de optie Transparanten voor uitsluiting van profielen wilt gebruiken, moet u een relatie tot stand brengen tussen de schema&#39;s Feedbackgebeurtenis voor AJO-berichten en Record voor AJO-entiteiten.

      1. Een aangepaste **Naamruimte** Dit wordt gebruikt als het type identiteit voor de onderstaande stappen.

      1. Toegang tot Adobe Experience Platform, vanaf de **Schemas** , selecteert u de **Recordschema AJO-entiteit** en stelt de **_id** veld als primaire identiteit en selecteer de eerder gemaakte naamruimte als de **Naamruimte identiteit**.

      1. Van de **Schemas** , selecteert u de **AJO Message Feedback Event-schema** en navigeer naar de **_messageID** veld. Selecteren **Relatie toevoegen** en kiest u **Recordschema AJO-entiteit** als de **Referentieschema** en de eerder gemaakte naamruimte als **Naamruimte voor verwijzingen**.
+++

   1. In de **[!UICONTROL Profiles targeted in previous runs]** kunt u zien dat de profielen van de vorige reeksen van die fase altijd worden uitgesloten. Als in Run #1 bijvoorbeeld een profiel in de eerste 4800 doelgroepen is opgenomen, zorgt het systeem er automatisch voor dat hetzelfde profiel de e-mail niet ontvangt in Run #2.

      >[!NOTE]
      >
      >Deze sectie kan niet worden bewerkt.

1. Indien nodig kunt u de campagne vervangen door **[!UICONTROL Replace]** knop. U kunt **[!UICONTROL Clear]** de geselecteerde campagne met **[!UICONTROL Clear]** knop. Deze actie zal niet alleen de campagne maar ook andere fasepleigenschappen zoals de Uitsluiting van de Groep van het Domein, Campagne, de Uitsluiting van de Reis, en anderen ontruimen. Na het ontruimen, kunt u of onmiddellijk of op een recentere tijd een nieuwe campagne kiezen.

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >Deze handeling is alleen mogelijk voordat de eerste uitvoering van de fase wordt geactiveerd. Nadat een run is geactiveerd, kan de campagne niet worden vervangen, tenzij u [de uitvoering splitsen](#split-phase) naar een nieuwe fase.

1. U kunt desgewenst een fase toevoegen. Het zal na de laatste fase worden toegevoegd.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Gebruik de **[!UICONTROL Delete phase]** om ongewenste fase te verwijderen. Deze actie is alleen beschikbaar als er geen uitvoering wordt uitgevoerd in een fase. <!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >U kunt de opdracht **[!UICONTROL Delete phase]** handeling.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >Als u alle fasen van het IP warmlopingsplan schrapt, wordt het geadviseerd om een plan opnieuw te uploaden. [Meer informatie](#re-upload-plan)

## De uitvoeringen definiëren {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="Elke uitvoering definiëren"
>abstract="Definieer en activeer elke uitvoering voor alle fasen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="Filter op betrokkenheid"
>abstract="Deze kolom is een filter dat alleen gericht is op de gebruikers die de afgelopen 20 dagen bijvoorbeeld met uw merk zijn verbonden. U kunt deze instelling ook wijzigen via het dialoogvenster **Uitvoeren bewerken** -optie."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="Een tijdvenster instellen"
>abstract="U kunt een tijdvenster bepalen waarin de IP warmup campagne kan worden uitgevoerd voor het geval dat er om het even welke vertragingen in de segmentatietaak zijn."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="Uitvoeren annuleren met publieksfouten"
>abstract="Selecteer deze optie als u een uitvoering wilt annuleren als de gekwalificeerde profielen kleiner zijn dan de doelprofielen nadat het publiek voor die uitvoering is geëvalueerd."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="De gekwalificeerde profielen weergeven"
>abstract="In deze kolom wordt het aantal gekwalificeerde profielen weergegeven. Als het publiek voor een run is geëvalueerd en er meer doelprofielen zijn dan gekwalificeerde profielen, wordt de run nog steeds uitgevoerd, tenzij de **Activering annuleren in geval van fouten** is ingeschakeld. In dit geval wordt de uitvoering geannuleerd."

1. Selecteer een schema voor elke looppas om ervoor te zorgen het op de gespecificeerde tijd wordt uitgevoerd.

   ![](assets/ip-warmup-plan-send-time.png)

1. Naar keuze, kunt u een tijdvenster bepalen waarin de IP warmup campagne kan worden uitgevoerd in het geval dat er om het even welke vertragingen in zijn [publieksevaluatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}. Als u dit wilt doen, klikt u op het pictogram Eigenschappen linksboven, naast de naam van het plan en gebruikt u de knop **[!UICONTROL Retry run time]** vervolgkeuzelijst voor het selecteren van een duur tot 240 minuten (4 uur).

   >[!NOTE]
   >
   >De pogingen gebeuren elke 30 minuten tot het eind van het bepaalde tijdvenster.

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Als u bijvoorbeeld een verzendtijd instelt op een bepaalde dag om 9.00 uur en 120 minuten selecteert als de runtime voor opnieuw proberen, is het mogelijk dat de runtime wordt uitgevoerd met een periode van 2 uur (9.00 - 11.00 uur) voor onverwachte vertragingen in de publieksevaluatie.

   >[!NOTE]
   >
   >Als geen tijdvenster wordt gespecificeerd, wordt de looppas geprobeerd bij verzendt tijd en zal ontbreken als de publieksevaluatie niet wordt voltooid.

1. Selecteer indien nodig **[!UICONTROL Edit run]** in het pictogram Meer handelingen. Daar kunt u de aantallen adressen in elke kolom bijwerken. U kunt ook de **[!UICONTROL Last engaged]** in het veld alleen te gebruiken voor de gebruikers die bijvoorbeeld de afgelopen 20 dagen met uw merk hebben gewerkt.

   >[!NOTE]
   >
   >U wordt aangeraden deze nummers aan te passen in overleg met uw leverancier.

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >Als u geen periode van de overeenkomst op een looppas wilt toepassen, ga 0 in **[!UICONTROL Last engaged]** veld.

1. Selecteer de **[!UICONTROL Cancel activated runs in case of errors]** als de gekwalificeerde profielen kleiner zijn dan de doelprofielen, kunt u een uitvoering annuleren nadat het publiek voor die uitvoering is geëvalueerd. In dat geval neemt de run de **[!UICONTROL Failed]** status.

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL Activate]** de run. [Meer informatie](#activate-run)

1. De status van deze uitvoering verandert in **[!UICONTROL Live]**, wat betekent dat het systeem het verzoek om de uitvoering te plannen heeft geaccepteerd.

   >[!NOTE]
   >
   >De verschillende uitvoerstatussen worden vermeld in [deze sectie](#monitor-plan).

1. Als de uitvoering van de campagne niet is gestart, kunt u een live uitvoering annuleren. Deze actie annuleert eigenlijk het runtime programma - het stopt niet het verzenden.

   ![](assets/ip-warmup-plan-stop-run.png)

1. Als u concepten, live of voltooide uitvoering wilt dupliceren, selecteert u **[!UICONTROL Duplicate run]**. Tijdens duplicatie wordt het menu Bewerken weergegeven, zodat gebruikers de opties **[!UICONTROL Total target profiles]** en de **[!UICONTROL Send time]** indien nodig.

   ![](assets/ip-warmup-duplicate.png)

## Runnen activeren {#activate-run}

Selecteer de optie **[!UICONTROL Activate]** knop. Dan kunt u de volgende looppas op een dagelijkse basis activeren.

Wanneer het runnen van veelvoudige IP warmup plannen gelijktijdig, allen gericht de zelfde IP pool en domeinen, is het cruciaal om de potentiële gevolgen te voorzien. Bijvoorbeeld, als ISP een dagelijkse grens van 100 e-mail afdwingt, zou het runnen van verscheidene plannen die op de zelfde domeinen richten deze drempel kunnen overschrijden.

Zorg ervoor dat u voldoende tijd hebt gepland om de [publieksevaluatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} uit te voeren.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>Elke run moet ten minste 12 uur voor de werkelijke verzendtijd worden geactiveerd. Anders is het mogelijk dat de publieksevaluatie niet is voltooid.

Wanneer u een run activeert, worden automatisch meerdere soorten publiek gemaakt.

* Indien de eerste uitvoering van een fase wordt geactiveerd:

   * An [publiek](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html){target="_blank"} wordt gemaakt voor het (eventuele) uitgesloten campagnepubliek, met de volgende naamgevingsconventie: `<warmupName>-Phase<phaseNo>-Audience Exclusion `.

   * Er wordt een publiek gemaakt voor de (eventuele) uitgesloten domeingroepen, met de volgende naamgevingsconventie: `<warmupName>-Phase<phaseNo>-Domain Exclusion`.

   * Er wordt een ander publiek gecreëerd voor het (eventuele) uitgesloten reispubliek, met de volgende naamgevingsconventie: `<warmupName>-Phase<phaseNo>-Journey Audience Exclusion`.

  >[!NOTE]
  >
  >Het publiek wordt opgeschoond nadat het warmtekrachtplan als voltooid is gemarkeerd.
  >
  >Het systeem creëert geen nieuw publiek voor het geval er geen wijziging optreedt in het uitgesloten campagnepubliek, het uitgesloten reispubliek of domeingroepen voor volgende fasen.

* Bij het activeren van een uitvoering:

   * Er wordt een ander publiek gemaakt voor het laatste betrokkenheidsfilter, met de volgende naamgevingsconventie: `<warmupName>-Phase<phaseNo>_Run<runNo>-Engagement Filter`.

     >[!NOTE]
     >
     >Het publiek wordt opgeruimd nadat het opwarmingsplan is voltooid.
     >
     >Het systeem maakt geen nieuw publiek voor het geval er geen wijziging optreedt in het laatste betrokkenheidsfilter voor volgende fasen.

   * An [publiekscompositie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html){target="_blank"} wordt gemaakt voor het publiek waarnaar de campagne wordt verzonden, met de volgende naamgevingsconventie: `<warmupName>-Phase<phaseNo>-Run<runNo>`.

     >[!NOTE]
     >
     >Voor elke run wordt een nieuwe publiekscompositie gemaakt. Met een grens van 10, moeten de gebruikers die veelvoudige campagnes, reizen, en IP warmup plannen gelijktijdig gebruiken gepubliceerde publiekssamenstellingen van plan zijn om binnen deze grens voor parallelle verrichtingen te blijven.
     >
     >De publiekssamenstelling (en vandaar het outputpubliek) wordt schoongemaakt wanneer de volgende herhaling wordt geactiveerd.

   * Er wordt een uitvoerpubliek gemaakt met de volgende naamgevingsconventie: `IP Warmup Audience-<warmupName>-Phase<phaseNo>-Run<runNo>`.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## Het abonnement controleren {#monitor-plan}

Om uw IP warmup plan met succes uit te voeren, moet u de rapporten controleren, looppas activeren en hun status op een dagelijkse basis controleren.

### De sectie Hooglichten gebruiken {#highlights}

Als de eerste uitvoering voor een fase is geactiveerd, wordt de **[!UICONTROL Highlights]** wordt weergegeven.

Het biedt een snel overzicht van de huidige runtime en de komende run. Vanuit deze sectie kunt u ook de volgende uitvoering bewerken en activeren.

![](assets/ip-warmup-plan-highlights.png)

### De status van uitvoering controleren {#run-statuses}

Het IP warmup plan zelf dient als geconsolideerd rapport op één enkele plaats. U kunt elementen controleren zoals het aantal **[!UICONTROL Live]** of **[!UICONTROL Completed]** looppas voor elke fase, en mening hoe uw IP warmup plan vordert.

>[!NOTE]
>
>Als beste praktijken, wordt het geadviseerd om uw IP opwarmingsplan op een dagelijkse basis te controleren.

Een run kan de volgende statussen hebben:

* **[!UICONTROL Draft]** : telkens wanneer een run wordt gemaakt, wanneer [het opstellen van een nieuw plan](ip-warmup-plan.md) of [toevoegen, run](#define-runs) vanuit de gebruikersinterface **[!UICONTROL Draft]** status.
* **[!UICONTROL Live]**: wanneer u een run activeert, neemt deze de **[!UICONTROL Live]** status. Het betekent dat het systeem het verzoek om de runtime te plannen heeft aanvaard - niet dat het verzenden is begonnen. Op dit moment kunt u de status van de live run bekijken door op de knop **[!UICONTROL View status]** in de tabel. Zo kunt u bijhouden hoeveel doelprofielen daadwerkelijk zijn gekwalificeerd.
* **[!UICONTROL Completed]**: de uitvoering van de campagne voor deze run is voltooid. U kunt tot een gedetailleerd looplooprapport toegang hebben door te klikken op **[!UICONTROL View report]** in de tabel. Met deze optie kunt u de status van de e-maillevering van de uitvoering bijhouden, inclusief de specifieke onderverdelingen voor domeingroepen voor uitgebreide controle. De bijbehorende campagne wordt ingesteld als Gestopt.[Meer informatie](#reports)
* **[!UICONTROL Cancelled]**: a **[!UICONTROL Live]** uitvoering is geannuleerd met de opdracht **[!UICONTROL Cancel]** knop.[Meer informatie](#define-runs)
* **[!UICONTROL Failed]**: er is een fout aangetroffen door het systeem of de campagne die voor de huidige fase is gebruikt, is gestopt of u hebt de optie **[!UICONTROL Cancel activated runs in case of errors]** en er is een fout opgetreden. Als een run mislukt, kunt u een andere run plannen voor de volgende dag.

### Rapporten gebruiken {#reports}

Meer in het algemeen, om het effect van uw plan te meten, kunt u de prestaties van uw IP warmup campagnes controleren gebruikend [!DNL Journey Optimizer] campagneverslagen. Om dit te doen, voor elke voltooide looppas kunt u klikken **[!UICONTROL View reports]** knop. Meer informatie over de campagne-e-mail [live-rapport](../reports/campaign-live-report.md#email-live) en [algemeen rapport](../reports/campaign-global-report.md#email-global).

![](assets/ip-warmup-plan-reports.png)

U kunt de rapporten ook openen via het dialoogvenster [Het menu Campagnes](../campaigns/modify-stop-campaign.md#access) omdat uw plan verschillende campagnes zou kunnen gebruiken.


## Uw abonnement beheren {#manage-plan}

Op om het even welk punt, als uw IP warmup plan niet zoals verwacht presteert, kunt u de hieronder acties nemen.

### Een fase splitsen {#split-phase}

Als u een nieuwe fase wilt toevoegen die van een specifieke looppas begint, selecteer **[!UICONTROL Split runs to a new phase]** van het pictogram Meer handelingen.

![](assets/ip-warmup-plan-run-split-run.png)

Er wordt een nieuwe fase gemaakt voor de resterende uitvoeringen van de huidige fase.

Als u deze optie bijvoorbeeld selecteert voor Run #4, worden Runs #4 tot en met #8 verplaatst naar een nieuwe fase vlak na de huidige fase.

Voer de stappen uit [boven](#define-phases) de nieuwe fase te definiëren.

* U kunt de **[!UICONTROL Replace]** of **[!UICONTROL Clear]** opties voor die nieuwe fase.

* U kunt ook de vorige campagne uitsluiten, of een domein dat niet goed presteert. Meer informatie over [deze sectie](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Upload een IP warmup plan opnieuw {#re-upload-plan}

Als uw IP warmup plan niet zoals verwacht uitvoert (bijvoorbeeld, als u opmerkt dat sommige ISPs uw berichten als spam) merkt, kunt u uw leverbaarheidsdeskundige vragen om opstelling een ander IP dossier van het warmup plan en herupload het gebruikend de overeenkomstige knoop.

![](assets/ip-warmup-re-upload-plan.png)

Alle eerder uitgevoerde looppas zal read-only zijn. Het nieuwe plan wordt getoond onder het eerste plan.

Voer de stappen uit [boven](#define-phases) de fases van het nieuwe plan te bepalen.

>[!NOTE]
>
>De IP details van het warmup plan zullen veranderen zoals per het onlangs geupload dossier. De eerder uitgevoerde looppas (ongeacht hun [status](#monitor-plan)) worden niet beïnvloed.

Laten we een voorbeeld nemen:

* Met het aanvankelijke IP warmup plan, had Fase 2 9 looppas.

* Er zijn vier uitvoeringen uitgevoerd (ongeacht of dit is mislukt, voltooid of geannuleerd)<!--as long as a run has been attempted, it is an executed run-->).

* Als u een nieuw plan opnieuw uploadt, zal Fase 2 met de eerste 4 uitgevoerde looppas op read-only wijze gaan.

* De resterende 5 looppas (die in ontwerpstaat zijn) wordt verplaatst naar een nieuwe fase (Fase 3) die volgens het onlangs geüploade plan verschijnt.

### Een abonnement markeren als voltooid {#mark-as-completed}

Als uw IPs met het gewenste volume werd opgewarmd, of als uw plan niet goed genoeg presteert of als u het wilt laten vallen om een andere te creëren, kunt u het merken zoals voltooid.

Klik hiertoe op de knop **[!UICONTROL More]** knoop op hoogste recht van het IP warmup plan en selecteer **[!UICONTROL Mark as completed]**.

![](assets/ip-warmup-plan-mark-completed.png)

Deze optie is alleen beschikbaar als alle runnen in het abonnement zijn opgenomen **[!UICONTROL Completed]** of **[!UICONTROL Draft]** status. Als een run **[!UICONTROL Live]**, wordt de optie grijs weergegeven.

De verschillende uitvoerstatussen worden vermeld in [deze sectie](#monitor-plan).

