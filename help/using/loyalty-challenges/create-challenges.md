---
solution: Journey Optimizer
product: journey optimizer
title: Beleidsuitdagingen maken
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen kunt maken en configureren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: e978d075efbbcb42e7500d921bd8cc3ed1eee890
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 0%

---


# Uitdagingen maken {#create-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [ wordt begonnen met de Uitdagingen van de Loyalty ](get-started.md) - Overzicht, werkschema, eerste vereisten
* [ de Uitdagingen van de Loyalty van de Toegang ](access-loyalty-challenges.md) - Inventaris en het filtreren
* **creeer uitdagingen** {2 }︎ ◀ u hier **bent - bouw en vorm uitdagingen**
* [ creeer taken ](create-tasks.md) - bepaal uitdagingstaken
* [ beheert uitdagingen ](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [ beschikbaarheidslabels ](../rn/releases.md#availability-labels).

## Werking {#how-it-works}

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **[creeer de uitdaging](#create-the-challenge)** - kies het uitdagingstype (Standaard, Streak, of Opeenvolgend) dat het best uw doelstellingen van het loyaliteitsprogramma past.

1. **[vorm de uitdagingsstructuur](#structure)** - bepaal de uitdagingseigenschappen, programma, taken die de klanten moeten voltooien, en beloningen zij zullen verdienen.

1. **[vorm inhoudskaarten](#configure-content-cards)** - de inhoudskaarten van het Ontwerp om uw uitdaging op klantenapparaten visueel te vertegenwoordigen, tonend uitdagingsinformatie, vooruitgang, en beloningen.

1. **[vorm overseinen](#configure-messaging)** (Facultatief) - Opstelling multi-kanaalberichten (in-app, e-mail, duw) voor zeer belangrijke stadia: lancering, lopend, en voltooiing.

1. **[selecteer het uitdagingspubliek](#audience)** - bepaal welke klanten verkiesbaar zijn om aan de uitdaging deel te nemen.

1. **[produceer en activeer de reis](#review-and-publish)** - produceer de bijbehorende reis en activeer het om de uitdaging ter beschikking te stellen van uw doelpubliek.

## Maak de uitdaging {#create-the-challenge}

1. Navigeer naar **[!UICONTROL Loyalty Challenges (Beta)]** in Journey Optimizer.

1. Selecteer de tab **[!UICONTROL Challenges]** en selecteer **[!UICONTROL Create Challenge]** .

   ![](assets/challenge-create.png)

1. Kies het uitdagingstype:

   * **[!UICONTROL Standard]**: klanten voltooien een opgegeven aantal taken in elke willekeurige volgorde
   * **[!UICONTROL Streak]**: klanten voltooien dezelfde taak meerdere keren achter elkaar
   * **[!UICONTROL Sequential]**: klanten voltooien taken in een gedefinieerde volgorde

## Vorm de uitdagingsstructuur {#structure}

In het lusje van de Structuur, bepaal hoe uw uitdaging wordt georganiseerd: zijn eigenschappen, programma, te voltooien taken, en te geven beloningen.

### Definieer de challenge-eigenschappen en gebruik aangepaste metagegevens {#properties}

1. In de de eigenschappen van de Uitdaging ruit, bepaal de uitdagingsmontages:

   ![](assets/challenge-create-properties.png)

   **Naam**: Ga een beschrijvende naam voor uw uitdaging in. Deze naam wordt weergegeven in de lijst met uitdagingen.

   **Beschrijving**: Ga een beschrijving in die het uitdagingsdoel en de doelstellingen verklaart.

1. Gebruik de sectie **[!UICONTROL Custom metadata]** om aangepaste metagegevens toe te voegen met sleutel-/waardeparen. Deze metagegevens kunnen worden gebruikt voor het bijhouden, segmenteren of integreren met externe systemen.

### Plan de uitdaging {#schedule}

Configureer wanneer de uitdaging wordt uitgevoerd door het pictogram ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Open schedule]** te selecteren:

* **de datum en de tijd van het Begin**: Plaats wanneer de uitdaging aan klanten beschikbaar wordt

* **de datum en de tijd van het Eind**: Plaats wanneer de uitdaging verloopt en niet meer nieuwe voltooiing goedkeurt

* **streek van de Tijd**: De uitdaging gebruikt lokale timezone van de ontvanger door gebrek

* **Taken moeten worden voltooid**: Kies wanneer de klanten taken kunnen voltooien:

   * **[!UICONTROL Any time during challenge]**: Klanten kunnen taken op elk gewenst moment uitvoeren tussen de begin- en einddatum van de uitdaging
   * **[!UICONTROL During specific hours of the day]**: Beperk het voltooien van een taak tot specifieke dagelijkse uren door de opties **[!UICONTROL Start Time]** en **[!UICONTROL End Time]** in te stellen

Het uitdagingsprogramma wordt nu gevormd. U kunt nu de taken toevoegen die klanten moeten uitvoeren.

### Taken toevoegen {#add-tasks}

De taken bepalen de specifieke acties klanten moeten voltooien om beloningen te verdienen. U kunt taaktypes (aankoop, uitgeven), hoeveelheden, productfilters, en andere attributen vormen.

Afhankelijk van uw uitdagingstype, voltooien de klanten verschillend taken:

* **Standaard uitdagingen**: Voltooi om het even welk gespecificeerd aantal taken in om het even welke orde\
  *Voorbeeld: Voltooi 3 van 5 taken - maak een aankoop, schrijf een overzicht, verwijs een vriend, aandeel op sociale media, of werk profiel* bij

* **Streak uitdagingen**: Voltooi de zelfde taak veelvoudige tijden opeenvolgend\
  *Voorbeeld: Maak een aankoop voor 7 opeenvolgende dagen om bonusbeloningen te verdienen*

* **Opeenvolgende uitdagingen**: Volledige taken in een bepaalde orde\
  *Voorbeeld: Maak eerst een aankoop, dan schrijf een overzicht, dan aandeel op sociale media - de taken moeten in deze nauwkeurige opeenvolging worden voltooid*

Ga als volgt te werk om taken aan uw uitdaging toe te voegen:

1. Selecteer **[!UICONTROL Tasks]** in de sectie **[!UICONTROL Add task]** .

   ![](assets/challenge-create-add-task.png)

1. De inventaris van Taken opent. Selecteer een of meer taken in de lijst en selecteer **[!UICONTROL Add]** . Selecteer **[!UICONTROL New]** als u een nieuwe taak wilt maken.

   [ leer hoe te om taken ](create-tasks.md) tot stand te brengen en te vormen.

1. Geef in de sectie **[!UICONTROL Task completion requirement]** op wanneer de uitdaging als voltooid wordt beschouwd:

   * **[!UICONTROL Customer chooses 1 task to complete]**: Klanten kunnen elke taak selecteren en voltooien om beloningen te verdienen
   * **[!UICONTROL Customer completes specific number of tasks]**: klanten moeten een bepaald aantal taken voltooien. Geef het vereiste nummer op.

1. Door gebrek, staan de uitdagingen klanten toe om taken over veelvoudige transacties te voltooien. Als u wilt dat alle taken in één transactie worden uitgevoerd, selecteert u het pictogram ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Settings]** en schakelt u de optie **[!UICONTROL Single transaction]** in.

   ![](assets/challenge-create-single-transaction.png)

### Rente configureren {#rewards}

De beloningen zijn de loyaliteitspunten of de voordelen klanten voor de voltooiing van uitdagingen ontvangen. Vorm wanneer en hoe de beloningen worden geleverd.

1. Kies in het vervolgkeuzemenu **[!UICONTROL Reward delivery]** wanneer u beloningen wilt leveren:

   * **[!UICONTROL Deliver rewards when challenge is completed]**: beloningen van de prijs wanneer klanten de hele uitdaging voltooien
   * **[!UICONTROL Deliver rewards at task completion milestones as challenge progress is made]**: Gunningspremies die incrementeel worden toegekend wanneer klanten afzonderlijke taken uitvoeren (alleen beschikbaar voor uitdagingen waarvoor meer dan één taak is vereist)

1. Selecteer de **[!UICONTROL Reward provider]** in de vervolgkeuzelijst. Dit is uw loyaliteitsoplossing die klantenpunten en beloningen beheert.

1. Vorm de beloningsbedragen die op uw geselecteerde leveringsmethode worden gebaseerd:

   +++Restituties leveren wanneer de uitdaging is voltooid

   In het **Aantal van [ loyaliteitspunten ] op uitdaging voltooit** gebied, specificeer het totale beloningsbedrag om te geven wanneer de klanten de volledige uitdaging voltooien.

   De veldnaam geeft de naam van uw loyaliteitspunten weer, zoals die is gedefinieerd in de geselecteerde provider. Als uw provider bijvoorbeeld &quot;Luminatiepunten&quot; gebruikt, wordt in het veld &quot;Aantal Luminatiepunten bij voltooiing van de aanroep&quot; weergegeven.

   ![](assets/challenge-create-reward-total.png)

   **Voorbeeld**: De klanten worden gegund 100 punten wanneer het voltooien van de uitdaging.

   +++

   +++Restituties leveren bij het voltooien van de taak

   Geef beloningsbedragen op voor mijlpalen voor taakvoltooiing. Deze optie staat u toe om progressieve beloningen tot stand te brengen die klantenmotivatie verhogen aangezien zij door de uitdaging vorderen.

   Voor om het even welke taak waar u een beloning wilt leveren, knevel op de beloningsoptie en specificeer hoeveel punten om te gunnen wanneer de klanten die specifieke taak voltooien. U kunt ervoor kiezen alleen bepaalde taken te belonen. Als u bijvoorbeeld 10 taken hebt, kunt u alleen de taken 1, 5 en 10 belonen.

   ![](assets/challenge-create-reward-milestones.png)

   **Voorbeeld**: De klanten worden toegewezen 10 punten wanneer de voltooiing van de eerste taak, toen 50 extra punten na de voltooiing van de tweede taak, voor een totaal van 60 punten wanneer de uitdaging wordt voltooid.

   >[!TIP]
   >
   >Overweeg hogere beloningswaarden voor recentere taken om klantenbetrokkenheid door de uitdaging te handhaven.

   +++

>[!NOTE]
>
>Loyalty Challenges omvat geen ingebouwd grootboeksysteem om beloningssaldi te volgen. Zorg ervoor dat uw geselecteerde bonusprovider de functie voor het bijhouden en aflossen van punten afhandelt.

De uitdagingsstructuur wordt nu gevormd met taken en beloningen. U kunt de inhoudskaarten nu ontwerpen om de uitdaging voor klanten weer te geven.

## Inhoudskaarten configureren {#configure-content-cards}

De kaarten van de inhoud vertegenwoordigen visueel uw uitdaging op klantenapparaten, tonend uitdagingsinformatie, vooruitgang, en beloningen. [ leer meer over inhoudskaarten ](../content-card/create-content-card.md).

Om inhoudskaarten voor uw uitdaging te vormen:

1. Ga naar het tabblad **[!UICONTROL Content]**.

1. Voer een **[!UICONTROL Name]** in voor de inhoudskaart.

1. Selecteer het **[!UICONTROL Channel configuration]**. Kanaalconfiguraties bevatten alle technische parameters voor het verzenden van het bericht, zoals headerparameters, subdomein, mobiele apps, enzovoort. [ leer meer op kanaalconfiguraties ](../configuration/channel-surfaces.md).

1. Selecteer **[!UICONTROL Edit content]** om uw inhoudskaart te ontwerpen.

   ![](assets/challenge-create-content.png)

[ Leer om inhoudskaarten ](../content-card/design-content-card.md) te ontwerpen en te personaliseren.

De inhoudskaart is nu geconfigureerd. U kunt opstellingsoverseinen nu om klanten door de uitdagingslevenscyclus in dienst te nemen.

### Berichten configureren {#configure-messaging}

De berichten van de opstelling multi-channel om klanten in belangrijkste stadia van de uitdagingslevenscyclus in dienst te nemen. Berichten is optioneel, maar wordt aanbevolen om de betrokkenheid van klanten te maximaliseren.

1. Ga naar het tabblad **[!UICONTROL Messaging]**.

1. Berichten configureren voor elke levenscyclusfase:

   ![](assets/challenge-create-messaging.png)

   * **Lancering** bericht: Melden klanten op wanneer de uitdaging begint
   * **In-progress** bericht: Houd klanten betrokken met herinneringen en vooruitgangsupdates
   * **Voltooiing** bericht: Kwalificeer succes en bevestig bonustoewijzing

1. Voor elk stadium, selecteer **[!UICONTROL Add *bericht *van het 0} stadium {om een bericht voor dat stadium tot stand te brengen.]**

1. Kies het gewenste kanaal: **[!UICONTROL In-app]** , **[!UICONTROL Email]** of **[!UICONTROL Push notification]** en selecteer de gekoppelde kanaalconfiguratie.

1. Selecteer het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) en kies **[!UICONTROL Edit]** om uw berichtinhoud te ontwerpen.

   Leer hoe u berichten voor specifieke kanalen maakt:

   * [Leer hoe u in-app-berichten maakt](../in-app/get-started-in-app.md)
   * [Leer hoe u e-mailberichten kunt maken](../email/get-started-email.md)
   * [Meer informatie over het maken van pushmeldingen](../push/get-started-push.md)

1. Herhaal deze stappen voor elk werkgebied en kanaal naar wens.

De overseinenconfiguratie is nu volledig. U kunt nu bepalen welke klanten verkiesbaar zijn om aan de uitdaging deel te nemen.

## Selecteer het publiek van de uitdaging {#audience}

Bepaal welke klanten aan uw loyaliteitsuitdaging kunnen deelnemen.

1. Navigeer naar de tab **[!UICONTROL Audience]** en selecteer **[!UICONTROL Select audience]** .

   ![](assets/challenge-create-audience.png)

1. Selecteer het doelpubliek in de lijst met beschikbare Adobe Experience Platform-doelgroepen.

1. Selecteer **[!UICONTROL Add audience]**.

Uw uitdagingsconfiguratie is nu volledig. U kunt nu de reis genereren die de uitdaging zal afhandelen.

## De reis genereren en activeren {#review-and-publish}

Wanneer uw uitdagingsconfiguratie volledig is, produceer de bijbehorende reis die de uitdagingslevering en klanteninteractie zal ordenen. Selecteer hiervoor **[!UICONTROL Generate Journey]** .

![](assets/challenge-create-generate-journey.png)

Journey Optimizer leidt automatisch tot a [ reis ](../building-journeys/journey-gs.md) in de status van het Ontwerp. De auto-geproduceerde reis verschijnt in uw reisinventaris met het naamformaat &quot;Uitdaging: [ Naam van de Uitdaging ]&quot;.

Herzie de reisconfiguratie indien nodig, dan [ activeer de reis ](../building-journeys/publish-journey.md) om de uitdaging beschikbaar te maken aan klanten.

De reis zal automatisch op uw gespecificeerde datum van de uitdagingsaanvang beginnen en inhoud en berichten volgens uw configuratie leveren.

>[!NOTE]
>
>De auto-geproduceerde reis kan worden aangepast om extra logica of overseinen toe te voegen. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie. Als u de uitdaging later uitgeeft, zullen om het even welke reisaanpassingen verloren gaan wanneer de reis wordt opnieuw geproduceerd.

## Volgende stappen {#next-steps}

* [ beheert uitdagingen ](manage-challenges.md) - geef, controleer, en optimaliseer uw uitdagingen uit
