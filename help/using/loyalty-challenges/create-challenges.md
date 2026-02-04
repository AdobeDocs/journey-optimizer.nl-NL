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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1432'
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

1. Selecteer de tab **[!UICONTROL Challenges]** en selecteer **[!UICONTROL Create challenge]** .

   ![](assets/challenge-create.png)

1. Kies het uitdagingstype:

   * **[!UICONTROL Standard]**: klanten voltooien een opgegeven aantal taken in elke willekeurige volgorde
   * **[!UICONTROL Streak]**: klanten voltooien dezelfde taak meerdere keren achter elkaar
   * **[!UICONTROL Sequential]**: klanten voltooien taken in een gedefinieerde volgorde

## Vorm de uitdagingsstructuur {#structure}

Op het tabblad Structuur definieert u hoe de uitdaging wordt georganiseerd: de eigenschappen, het schema, de taken die moeten worden voltooid en de beloningen die moeten worden toegekend.

### Definieer de challenge-eigenschappen en gebruik aangepaste metagegevens {#properties}

1. In de de eigenschappen van de Uitdaging ruit, vorm de uitdagingseigenschappen:

   ![](assets/challenge-create-properties.png)

   **Naam**: Ga een beschrijvende naam voor uw uitdaging in. Deze naam wordt weergegeven in de inventaris van uitdagingen en helpt u de uitdaging te identificeren.

   **Beschrijving**: Ga een beschrijving voor uw uitdaging in.

1. Gebruik de sectie **[!UICONTROL Custom metadata]** om aangepaste metagegevens toe te voegen met sleutel-/waardeparen. Deze metagegevens kunnen worden gebruikt voor het bijhouden, segmenteren of integreren met externe systemen.

### Plan de uitdaging {#schedule}

Plan de uitdaging door het pictogram ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Open schedule]** te selecteren.

* **de datum en de tijd van het Begin**: Plaats wanneer de uitdaging aan klanten (formaat: mm/dd/jjjj, — wordt aangeboden:— AM/PM).

* **einddatum en tijd**: Plaats wanneer de uitdaging verloopt en niet meer nieuwe voltooide (formaat: mm/dd/jjjj, —:— AM/PM) goedkeurt.

* **streek van de Tijd**: De uitdaging gebruikt lokale timezone van de ontvanger door gebrek.

* **Taken moeten worden voltooid**: Kies wanneer de klanten taken kunnen voltooien:

   * **[!UICONTROL Any time during challenge]**: Klanten kunnen taken op elk gewenst moment uitvoeren tussen de begin- en einddatum van de uitdaging
   * **[!UICONTROL During specific hours of the day]**: Beperk het voltooien van een taak tot specifieke dagelijkse uren door de opties **[!UICONTROL Start Time]** en **[!UICONTROL End Time]** in te stellen

Het uitdagingsprogramma wordt nu gevormd. U kunt nu de taken toevoegen die klanten moeten uitvoeren.

### Taken toevoegen {#add-tasks}

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen te verdienen. U configureert taaktypen (aanschaf, uitgave, bezoek, betrokkenheid, aangepaste gebeurtenissen), hoeveelheden, productfilters en beloningen.

Afhankelijk van uw uitdagingstype, voltooien de klanten verschillend taken:

* **Standaard uitdagingen**: Voltooi om het even welk gespecificeerd aantal taken in om het even welke orde
* **Streak uitdagingen**: Voltooi de zelfde taak veelvoudige tijden opeenvolgend
* **Opeenvolgende uitdagingen**: Volledige taken in een bepaalde orde

Ga als volgt te werk om taken aan uw uitdaging toe te voegen:

1. Selecteer **[!UICONTROL Tasks]** in de sectie **[!UICONTROL Add task]** .

   ![](assets/challenge-create-add-task.png)

1. De inventaris van Taken opent. Selecteer een of meer taken in de lijst en selecteer **[!UICONTROL Add]** . Selecteer **[!UICONTROL New]** als u een nieuwe taak wilt maken.

   Voor gedetailleerde instructies bij het creëren van en het vormen van taken, zie [ tot taken ](create-tasks.md) leiden.

1. Geef in de sectie **[!UICONTROL Task completion requirement]** op wanneer de uitdaging als voltooid moet worden beschouwd:

   * **[!UICONTROL Customer chooses 1 task to complete]**: De klant kan elke taak selecteren en voltooien om beloningen te verdienen
   * **[!UICONTROL Customer completes specific number of tasks]**: de klant moet een bepaald aantal taken voltooien. Voer het vereiste aantal taken in.

1. Door gebrek, staan de uitdagingen klanten toe om taken over veelvoudige transacties te voltooien. Als u wilt dat alle taken in één transactie worden uitgevoerd, selecteert u het pictogram ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Settings]** en schakelt u de optie **[!UICONTROL Single transaction]** in.

   ![](assets/challenge-create-single-transaction.png)

### Rente configureren {#rewards}

De beloningen zijn de loyaliteitspunten of de voordelen klanten voor de voltooiing van uitdagingen ontvangen. Vorm hoe en wanneer de beloningen worden geleverd om klantenparticipatie te motiveren.

1. Kies in het vervolgkeuzemenu **[!UICONTROL Reward delivery]** wanneer u beloningen wilt ontvangen:

   * **[!UICONTROL Deliver rewards when challenge is completed]**: Alle beloningen uitreiken wanneer de klant de hele uitdaging heeft voltooid
   * **[!UICONTROL Deliver rewards at task completion milestones as challenge progress is made]**: Gunningspremies die incrementeel worden toegekend aan klanten die afzonderlijke taken uitvoeren (alleen beschikbaar als de uitdaging het voltooien van meer dan één taak vereist)

1. Selecteer uw bonusprovider in de vervolgkeuzelijst. Dit is uw loyaliteitsoplossing die klantenpunten en beloningen beheert.

1. Vorm de beloningsbedragen die op uw geselecteerde leveringsmethode worden gebaseerd:

   +++Restituties leveren wanneer de uitdaging is voltooid

   In het **Aantal [ loyaliteitspunten ] op uitdaging voltooit** gebied, specificeer het totale beloningsbedrag om te geven wanneer de klant de volledige uitdaging voltooit.

   De veldnaam geeft de naam van uw loyaliteitspunten weer, zoals die is gedefinieerd in de geselecteerde provider. Als uw provider bijvoorbeeld &quot;Luminatiepunten&quot; gebruikt, wordt in het veld &quot;Aantal Luminatiepunten bij voltooiing van de aanroep&quot; weergegeven.

   ![](assets/challenge-create-reward-total.png)

   **Voorbeeld**: In het het schermschot hierboven, worden de klanten toegewezen 100 punten wanneer het voltooien van de uitdaging.

   +++

   +++Restituties leveren bij het voltooien van de taak

   Geef beloningsbedragen op voor mijlpalen voor taakvoltooiing. Deze optie staat u toe om progressieve beloningen tot stand te brengen die klantenmotivatie verhogen aangezien zij door de uitdaging vorderen.

   Voor om het even welke taak waar u een beloning wilt leveren, knevel op de beloningsoptie en specificeer hoeveel punten om te gunnen wanneer de klanten die specifieke taak voltooien. U kunt ervoor kiezen alleen bepaalde taken te belonen. Als u bijvoorbeeld 10 taken hebt, kunt u alleen de taken 1, 5 en 10 belonen.

   ![](assets/challenge-create-reward-milestones.png)

   **Voorbeeld**: In het het schermschot hierboven, worden de klanten toegewezen 10 punten wanneer de voltooiing van de eerste taak, en dan 50 extra punten na de voltooiing van de tweede taak, voor een totaal van 60 punten wanneer de uitdaging wordt voltooid.

   >[!TIP]
   >
   >Overweeg hogere beloningswaarden voor recentere taken om klantenbetrokkenheid door de uitdaging te handhaven.

   +++

De uitdagingsstructuur wordt nu gevormd met taken en beloningen. U kunt de inhoudskaarten nu ontwerpen om de uitdaging voor klanten weer te geven.

## Inhoudskaarten configureren {#configure-content-cards}

De kaarten van de inhoud verstrekken de visuele vertegenwoordiging van uw uitdaging op klantenapparaten, tonend uitdagingsinformatie, vooruitgang, en beloningen. Leer meer over [ inhoudskaarten ](../content-card/create-content-card.md).

Om inhoudskaarten voor uw uitdaging te vormen:

1. Navigeer in de challenge-editor naar de tab **[!UICONTROL Content]** .

1. Voer een **[!UICONTROL Name]** in voor de inhoudskaart.

1. Selecteer de gekoppelde **[!UICONTROL Channel configuration]** . De configuraties van het kanaal bepalen hoe en waar uw inhoud aan klanten wordt geleverd. Voor meer informatie, zie {de configuraties van het 0} Kanaal [.](../configuration/channel-surfaces.md)

1. Selecteer **[!UICONTROL Edit content]** om uw inhoudskaart te ontwerpen.

   ![](assets/challenge-create-content.png)

Voor meer informatie bij het ontwerpen van en het aanpassen van inhoudskaarten, zie [ de inhoudskaarten van het Ontwerp ](../content-card/design-content-card.md).

De inhoudskaart is nu geconfigureerd. U kunt opstellingsoverseinen nu om klanten door de uitdagingslevenscyclus in dienst te nemen.

### Berichten configureren {#configure-messaging}

De berichten van de opstelling multi-channel om klanten in belangrijkste stadia van de uitdagingslevenscyclus in dienst te nemen.

1. Ga naar het tabblad **[!UICONTROL Messaging]**.

1. Berichten configureren voor elke levenscyclusfase:

   ![](assets/challenge-create-messaging.png)

   * **de berichten van de Lancering**: Melden klanten op wanneer de uitdaging begint en verstrekken aanvankelijke details
   * **In-progress berichten**: Houd klanten betrokken tijdens de uitdaging met herinneringen, vooruitgangsupdates, en aanmoediging om verder te gaan
   * **de berichten van de Voltooiing**: Kwalificeer succes, bevestig bonustoewijzing, en stel volgende uitdagingen of acties voor

1. Voor elk stadium, selecteer **[!UICONTROL Add *bericht *van het 0} stadium {om een bericht voor dat stadium tot stand te brengen.]**

1. Kies het gewenste kanaal: **[!UICONTROL In-app]** , **[!UICONTROL Email]** of **[!UICONTROL Push notification]** en selecteer de gekoppelde kanaalconfiguratie.

1. Selecteer het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) en kies **[!UICONTROL Edit]** om uw berichtinhoud te ontwerpen.

   Raadpleeg voor meer informatie over het maken van berichten voor specifieke kanalen:

   * [Documentatie voor in-app berichten](../in-app/get-started-in-app.md)
   * [E-mailberichten](../email/get-started-email.md)
   * [Documentatie voor pushmeldingen](../push/get-started-push.md)

1. Herhaal deze stappen voor elk werkgebied en kanaal naar wens.

De overseinenconfiguratie is nu volledig. U kunt nu bepalen welke klanten verkiesbaar zijn om aan de uitdaging deel te nemen.

## Selecteer het publiek van de uitdaging {#audience}

Bepaal welke klanten verkiesbaar zijn om aan uw loyaliteitsuitdaging deel te nemen.

1. Navigeer naar het tabblad **[!UICONTROL Audience]** en klik op de knop **[!UICONTROL Select audience]** .

   ![](assets/challenge-create-audience.png)

1. Alle beschikbare Adobe Experience Platform-soorten publiek worden weergegeven. Selecteer het gewenste publiek in de lijst.

1. Selecteer **[!UICONTROL Add audience]** om uw selectie te bevestigen.

Uw uitdagingsconfiguratie is nu volledig. U kunt nu de reis genereren die de uitdaging zal afhandelen.

## De reis genereren en activeren {#review-and-publish}

Wanneer uw uitdagingsconfiguratie volledig is, produceer de bijbehorende reis die de uitdagingslevering en klanteninteractie zal ordenen. Selecteer hiervoor **[!UICONTROL Generate Journey]** .

![](assets/challenge-create-generate-journey.png)

Journey Optimizer leidt automatisch tot a [ reis ](../building-journeys/journey-gs.md) in de status van het Ontwerp. De auto-geproduceerde reis verschijnt in uw reisinventaris met het naamformaat &quot;Uitdaging: [ Naam van de Uitdaging ]&quot;.

Herzie de reisconfiguratie indien nodig, dan [ activeer de reis ](../building-journeys/publish-journey.md) om de uitdaging beschikbaar te maken aan klanten.

De reis zal automatisch op uw gespecificeerde datum van de uitdagingsaanvang beginnen en inhoud en berichten volgens uw configuratie leveren.

>[!NOTE]
>
>De auto-geproduceerde reis kan worden aangepast indien nodig om extra logica of overseinen toe te voegen. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie. Als u de uitdaging later uitgeeft, zullen om het even welke reisaanpassingen verloren gaan wanneer de reis wordt opnieuw geproduceerd.

## Volgende stappen {#next-steps}

* [ beheert uitdagingen ](manage-challenges.md) - Leer hoe te, uitdagingen uit te geven te controleren en te optimaliseren
* [ Begrijp Loyalty Uitdagingen ](get-started.md) - de eigenschappen en de mogelijkheden van het overzicht
