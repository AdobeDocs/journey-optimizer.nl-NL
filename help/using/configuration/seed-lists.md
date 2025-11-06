---
solution: Journey Optimizer
product: journey optimizer
title: Zaadlijsten
description: Meer informatie over het gebruik van zaadlijsten in Journey Optimizer
feature: Seed Lists, Channel Configuration
topic: Content Management
role: User
level: Intermediate
keywords: zaadlijst, zaadlijst, zaad, configuratie
exl-id: 0172f6bc-da8b-4a83-a0fc-4ed41324568f
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 2%

---

# zaadlijsten gebruiken {#seed-lists}

Met zaadlijsten in [!DNL Journey Optimizer] kunt u automatisch specifieke zaadadressen opnemen in uw leveringen.

>[!CAUTION]
>
>Deze functie is momenteel alleen van toepassing op het e-mailkanaal.

Seed-adressen worden gebruikt om ontvangers die niet aan de gedefinieerde doelcriteria voldoen, doelgericht te benaderen. Op deze manier kunnen ontvangers die buiten het bereik van de levering vallen, de levering ontvangen, net als elke andere doelontvanger.

Zaadadressen zijn geen echte profielen en testprofielen, omdat deze geen profieldetails bevatten. Het zijn alleen ontvangers die behoren tot interne belanghebbenden die in het systeem zijn opgeslagen. Wanneer zij in een specifieke campagne of een specifieke reis worden geselecteerd, worden zij opgenomen op het tijdstip van uitvoering van de levering, wat betekent dat zij een kopie van de levering voor verzekeringsdoeleinden ontvangen.

* Door leveringen te ontvangen op hetzelfde moment en onder dezelfde voorwaarden als uw klanten, kunt u met zaadlijsten de e-mailkopieën controleren die worden verzonden om ervoor te zorgen dat alle weergaveformaten, afbeeldingen en koppelingen correct zijn. Bovendien kunt u de werkelijke berichten die aan uw ontvangers zijn verzonden, bijhouden.

  Bijvoorbeeld:

  +++ Als u een marketingmanager bent:

  U wilt dat al uw teamleden tegelijkertijd met uw klanten kopieën van verzonden berichten ontvangen. Op deze manier kan uw team ervoor zorgen dat berichten worden verzonden met de verwachte lay-out, actieve URL&#39;s, correcte tekst en beelden - allen zoals gepland vóór uitvoering.

  +++

  +++ Als u eigenaar van het product bent:

  U moet het spoor van daadwerkelijke berichten houden die naar klanten worden verzonden. Uw team en de leiding zijn wellicht geïnteresseerd in bepaalde campagnes en moeten op ad-hocbasis worden toegevoegd om kopieën van de boodschap op het moment van levering te ontvangen.

  +++

* Een andere reden voor het gebruik van zaadlijsten is de bescherming van uw mailinglijst. Door zaadadressen in te voegen in uw mailinglijst kunt u zien of het door een derde wordt gebruikt, aangezien de zaadadressen het bevat de leveringen ontvangen die naar uw mailinglijst worden verzonden.

>[!NOTE]
>
>Varianten worden ondersteund, inclusief meertalige en experimenteringsvarianten. Elk zaadadres ontvangt één enkel exemplaar van elke variant van het zelfde bericht, b.v. verschillende versies van a [&#x200B; inhoudsexperiment &#x200B;](../content-management/get-started-experiment.md). Voor voorwaardelijke inhoud worden geen afzonderlijke e-mails met zaad verzonden.

## De zaadlijsten openen {#access-seed-lists}

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** en selecteer **[!UICONTROL Seed list]** om de reeds gemaakte zaadlijsten te openen.

<!--
>[!CAUTION]
>
>Permissions to view, export and manage the seed lists are restricted to [Journey Administrators](../administration/ootb-product-profiles.md#journey-administrator). Learn more about managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

>[!CAUTION]
>
>U moet de machtiging **[!UICONTROL Manage Seedlist]** hebben om zaadlijsten te kunnen weergeven, bewerken en beheren.

![](assets/seed-list-access.png)

U kunt zaadlijsten zoeken op naam en/of filteren op de gebruiker die de lijst heeft gemaakt of op de aanmaakdatum. Als deze optie is geselecteerd, kunt u het filter wissen dat boven op de lijst wordt weergegeven.

![](assets/seed-list-filtering.png)

Gebruik de knop **[!UICONTROL Delete]** om een item permanent te verwijderen.

>[!CAUTION]
>
>Het is niet mogelijk om een zaadlijst te schrappen die in een actieve [&#x200B; campagne &#x200B;](../campaigns/review-activate-campaign.md) of [&#x200B; reis &#x200B;](../building-journeys/publish-journey.md) wordt gebruikt. U moet de campagne/reis deactiveren, of het uitgeven om een andere configuratie te gebruiken die niet de geselecteerde zaadlijst heeft. [&#x200B; leer meer over het gebruiken van een zaadlijst &#x200B;](#use-seed-list)

U kunt op de naam van een zaadlijst klikken om deze te bewerken. <!--Use the **[!UICONTROL Edit]** button to edit a seed list.-->

## Een zaadlijst maken {#create-seed-list}

>[!CONTEXTUALHELP]
>id="ajo_seed_list_details"
>title="Een zaadlijst definiëren"
>abstract="Gebruik een zaadlijst om specifieke interne adressen aan uw leveringspubliek voor verzekeringsdoeleinden automatisch toe te voegen. Met zaadlijsten kunt u de berichtkopieën controleren die worden verzonden om ervoor te zorgen dat alle weergave-elementen correct zijn en uw mailinglijst beveiligen. Deze functie is momenteel alleen van toepassing op het e-mailkanaal."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="Wat zijn zaadlijsten?"

>[!CONTEXTUALHELP]
>id="ajo_seed_addresses"
>title="De zaadlijst invullen"
>abstract="Selecteer de adressen die op de leveringstijd zullen worden omvat en een nauwkeurige kopie van uw bericht zullen ontvangen. U kunt een CSV-bestand importeren of handmatig e-mailadressen invoeren."

Voer de onderstaande stappen uit om een zaadlijst te maken.

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Seed list]** .

1. Selecteer de knop **[!UICONTROL Create seed list]**.

   <!--![](assets/seed-list-create-button.png)-->

1. Vul de gegevens in. Begin door een naam toe te voegen.

   ![](assets/seed-list-details.png)

   >[!NOTE]
   >
   >Namen moeten beginnen met een letter (A-Z) en alleen alfanumerieke tekens of speciale tekens ( _, ., -) bevatten.

1. Selecteer het kanaal. Momenteel is alleen het e-mailkanaal beschikbaar.

1. Selecteer een testprofiel. Omdat de zaadadressen geen profieldetails omvatten, zal dit testprofiel slechts worden gebruikt om de verpersoonlijkingsgegevens in het bericht te tonen dat naar de zaadadressen wordt verzonden.

   >[!NOTE]
   >
   >Er kan slechts één testprofiel tegelijk worden geselecteerd.

1. Voeg de zaadadressen toe u uw leveringen aan wilt verzenden. U kunt een CSV-bestand importeren of handmatig e-mailadressen invoeren.

   ![](assets/seed-list-email-addresses.png)

   >[!NOTE]
   >
   >U kunt beide opties combineren, maar het totale aantal adressen in een zaadlijst mag niet groter zijn dan 300.

1. Klik op **[!UICONTROL Create]** om te bevestigen. De nieuw gecreëerde zaadlijst toont in het [&#x200B; scherm van de zaadlijst &#x200B;](#access-seed-lists).

## Een zaadlijst gebruiken in een campagne of reis {#use-seed-list}

Nu uw zaadlijst wordt gecreeerd, kunt u het in om het even welke campagne of reis gebruiken om de overeenkomstige zaadadressen in uw leveringen te omvatten. Volg de onderstaande stappen om dit te doen.

>[!CAUTION]
>
>Berichten die naar zaadadressen worden verzonden zijn niet inbegrepen in reis of campagnerapporten.

1. Maak een configuratie en selecteer het kanaal **[!UICONTROL Email]** . [Meer informatie](../email/email-settings.md)

1. Selecteer de zaadlijst van uw keus in de [&#x200B; overeenkomstige sectie &#x200B;](../email/email-settings.md#seed-list).

   >[!NOTE]
   >
   >Er kan slechts één zaadlijst tegelijk worden geselecteerd.

   ![](assets/seed-list-surface.png)

1. Verzend de configuratie.

1. Creeer a [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) of a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md).

1. Selecteer de **[!UICONTROL Email]** actie en selecteer de [&#x200B; configuratie &#x200B;](channel-surfaces.md) met inbegrip van de zaadlijst die voor u relevant is.

   ![](assets/seed-list-campaign-email.png)

1. Activeer uw [&#x200B; campagne &#x200B;](../campaigns/review-activate-campaign.md) of publiceer uw [&#x200B; reis &#x200B;](../building-journeys/publish-journey.md).

Telkens wanneer een e-mailbericht naar uw klanten wordt verstuurd via die campagne of die reis, zullen de e-mailadressen op de geselecteerde zaadlijst het ook in de zelfde voorwaarden, tezelfdertijd en met de zelfde inhoud ontvangen zoals de beoogde ontvangers.

>[!NOTE]
>
>[&#x200B; de wijze van de Test &#x200B;](../building-journeys/testing-the-journey.md) reizen verzenden geen e-mail naar de zaadlijst. Om uw e-mailinhoud te controleren, gebruik de [&#x200B; voorproef en test &#x200B;](../content-management/preview-test.md) functionaliteit alvorens uw bericht te verzenden.
>
>Voor terugkerende ritten, wordt de e-maillevering verzonden naar de zaadadressen bij elke reis uitvoering, op voorwaarde dat minstens één profiel de e-mailknoop bereikt.
