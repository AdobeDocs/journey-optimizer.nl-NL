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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---


# Uitdagingen maken {#create-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* [&#x200B; toegang en beheer de Uitdagingen van de Loyalty &#x200B;](access-loyalty-challenges.md) - Overzicht, uitdagingen en taakbeheer
* **creeer uitdagingen** {2 }︎ ◀ u hier **bent - bouw en vorm uitdagingen**
* [&#x200B; creeer taken &#x200B;](create-tasks.md) - bepaal uitdagingstaken

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Maak de uitdaging {#create-the-challenge}

1. Navigeer naar **[!UICONTROL Loyalty Challenges (Beta)]** in Journey Optimizer.

1. Selecteer de tab **[!UICONTROL Challenges]** en selecteer **[!UICONTROL Create Challenge]** .

   ![](assets/challenge-create.png)

1. Kies het uitdagingstype:

   * **[!UICONTROL Standard]**: klanten voltooien een opgegeven aantal taken in elke willekeurige volgorde\
     *Voorbeeld: Voltooi 3 van 5 beschikbare taken*

   * **[!UICONTROL Streak]**: klanten voltooien dezelfde taak meerdere keren achter elkaar\
     *Voorbeeld: Maak een aankoop op 7 opeenvolgende dagen*

   * **[!UICONTROL Sequential]**: klanten voltooien taken in een gedefinieerde volgorde\
     *Voorbeeld: Aankoop → Controle → Aandeel (moet in deze opeenvolging worden voltooid)*

## Vorm de uitdagingsstructuur {#structure}

Definieer op het tabblad **[!UICONTROL Structure]** hoe de uitdaging is ingedeeld: de eigenschappen, het schema, de taken die moeten worden voltooid en de beloningen die moeten worden geleverd.

### Definieer de challenge-eigenschappen en gebruik aangepaste metagegevens {#properties}

1. Definieer in het deelvenster **[!UICONTROL Challenge properties]** de algemene instellingen voor de uitdaging:

   * **[!UICONTROL Name]**: ga een beschrijvende naam voor uw uitdaging in. Deze naam wordt weergegeven in de lijst met uitdagingen.
   * **[!UICONTROL Description]**: ga een beschrijving in die het doel en de doelstellingen van de uitdaging verklaart.

   ![](assets/challenge-create-properties.png)

1. Gebruik de sectie **[!UICONTROL Custom metadata]** om aangepaste metagegevens toe te voegen met sleutel-/waardeparen. Deze metagegevens kunnen worden gebruikt voor het bijhouden of integreren met externe systemen.

### Plan de uitdaging {#schedule}

Configureer wanneer de uitdaging wordt uitgevoerd door het pictogram **[!UICONTROL Open schedule]** te selecteren:

![](assets/challenge-create-schedule.png)

* **[!UICONTROL Start date and time]**: plaats wanneer de uitdaging aan klanten beschikbaar wordt.
* **[!UICONTROL End date and time]**: stel in wanneer de uitdaging vervalt en geen nieuwe voltooide bewerkingen meer accepteert.
* **[!UICONTROL Time zone]**: De uitdaging gebruikt standaard de lokale tijdzone van de ontvanger.
* **[!UICONTROL Tasks must be completed]**: kies wanneer klanten taken kunnen uitvoeren:

   * **[!UICONTROL Any time during challenge]**: Klanten kunnen taken op elk gewenst moment uitvoeren tussen de begin- en einddatum van de uitdaging.
   * **[!UICONTROL During specific hours of the day]**: Beperk het voltooien van een taak tot specifieke dagelijkse uren door de opties **[!UICONTROL Start Time]** en **[!UICONTROL End Time]** in te stellen.

Het uitdagingsprogramma wordt nu gevormd. Voeg vervolgens de taken toe die klanten moeten uitvoeren.

### Taken toevoegen {#add-tasks}

De taken bepalen de specifieke acties klanten moeten voltooien om beloningen te verdienen. U kunt taaktypes (aankoop, uitgeven), hoeveelheden, productfilters, en andere attributen vormen.

Ga als volgt te werk om taken aan uw uitdaging toe te voegen:

1. Selecteer **[!UICONTROL Tasks]** in de sectie **[!UICONTROL Add task]** .

   ![](assets/challenge-create-add-task.png)

1. De lus **[!UICONTROL Tasks Inventory]** wordt geopend. Selecteer een of meer taken in de lijst en selecteer **[!UICONTROL Add]** . Selecteer **[!UICONTROL New]** als u een nieuwe taak wilt maken. [&#x200B; leer hoe te om taken &#x200B;](create-tasks.md) tot stand te brengen en te vormen.

1. Specificeer wanneer de uitdaging als voltooid wordt beschouwd. Beschikbare instellingen zijn afhankelijk van het type uitdaging:

   +++Standaarduitdagingen

   **[!UICONTROL Task completion requirement]** - Kies tussen:

   * **[!UICONTROL Customer chooses 1 task to complete]**: Klanten kunnen elke taak selecteren en voltooien om beloningen te verdienen
   * **[!UICONTROL Customer completes specific number of tasks]**: klanten moeten een bepaald aantal taken voltooien. Specificeer het vereiste aantal - *Voorbeeld: Voltooi 3 van 5 taken*

   +++

   +++Streep uitdagingen

   * **[!UICONTROL Streak type]**:

      * **Opeenvolgend**: De klanten moeten de taak op opeenvolgende dagen zonder onderbrekingen voltooien - *Voorbeeld: Aankoop op Maandag, Dinsdag, Woensdag - ontbrekende een dageinden de stroom*

      * **niet-opeenvolgend**: De klanten kunnen de taak met hiaten tussen voltooiing - *Voorbeeld voltooien: Voltooi 7 aankopen meer dan 30 dagen, met toegelaten onderbrekingen*

   * **[!UICONTROL Streak length]**: Specificeer hoeveel tijden de taak moet worden voltooid - *Voorbeeld: Reeks aan 7 voor een &quot;7 dag aankoopstroom&quot;*

   +++

   +++Opeenvolgende uitdagingen

   **[!UICONTROL Task completion requirement]** - Kies tussen:

   * **[!UICONTROL Customer chooses 1 task to complete]**: Klanten kunnen elke taak selecteren en voltooien om beloningen te verdienen
   * **[!UICONTROL Customer completes specific number of tasks]**: klanten moeten een bepaald aantal taken voltooien in de exacte volgorde die u definieert. Als een taak ontbreekt of wordt overgeslagen, wordt de reeks verbroken. Geef het vereiste aantal op (bijvoorbeeld 3 van de 5 taken voltooien)

   *Voorbeeld: Taak 1 (Aankoop) → Taak 2 (Overzicht) → Taak 3 (Aandeel) - moet in deze orde worden voltooid*

   +++

1. Door gebrek, staan de standaard en opeenvolgende uitdagingen klanten toe om taken over veelvoudige transacties te voltooien. Als u wilt dat alle taken in één transactie worden uitgevoerd, selecteert u het pictogram ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Settings]** en schakelt u de onderstaande optie in.

   ![](assets/challenge-create-single-transaction.png)

Na het toevoegen van taken aan uw uitdaging, vorm de beloningsklanten voor de voltooiing van hen zullen verdienen.

### Rente configureren {#rewards}

De beloningen zijn de loyaliteitspunten of de voordelen klanten voor de voltooiing van uitdagingen ontvangen. Vorm wanneer en hoe de beloningen worden geleverd.

1. Kies in het vervolgkeuzemenu **[!UICONTROL Reward delivery]** wanneer u beloningen wilt leveren:

   * **[!UICONTROL Deliver rewards when challenge is completed]**: beloningen van de prijs wanneer klanten de hele uitdaging voltooien\
     *Voorbeeld: Uitreiking 100 punten na het voltooien van alle 5 taken*

   * **[!UICONTROL Deliver rewards at task completion milestones as challenge progress is made]**: Gunningspremies die incrementeel worden toegekend wanneer klanten afzonderlijke taken uitvoeren (alleen beschikbaar voor uitdagingen waarvoor meer dan één taak is vereist)\
     *Voorbeeld: Toekenning 10 punten na taak 1, 20 punten na taak 2, en 50 punten na taak 3*

1. Selecteer uw bonusprovider. Dit is uw loyaliteitsoplossing die klantenpunten en beloningen beheert.

1. Vorm de beloningsbedragen die op uw geselecteerde leveringsmethode worden gebaseerd:

   +++Restituties leveren wanneer de uitdaging is voltooid

   Specificeer het totale bonusbedrag om te geven wanneer de klanten de volledige uitdaging voltooien.

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

Na het vormen van de uitdagingsstructuur met taken en beloningen, ontwerp de inhoudskaarten om de uitdaging aan klanten te tonen.

## Inhoudskaarten configureren {#configure-content-cards}

De kaarten van de inhoud vertegenwoordigen visueel uw uitdaging op klantenapparaten, tonend uitdagingsinformatie, vooruitgang, en beloningen. [&#x200B; leer meer over inhoudskaarten &#x200B;](../content-card/create-content-card.md).

Om inhoudskaarten voor uw uitdaging te vormen:

1. Navigeer naar het tabblad **[!UICONTROL Content]** en voer een **[!UICONTROL Name]** in voor de inhoudskaart.

1. Selecteer het **[!UICONTROL Channel configuration]**. Kanaalconfiguraties bevatten alle technische parameters voor het verzenden van berichten, zoals headerparameters, subdomein, mobiele apps, enz. [&#x200B; leer meer over kanaalconfiguraties &#x200B;](../configuration/channel-surfaces.md).

1. Selecteer **[!UICONTROL Edit content]** om uw inhoudskaart te ontwerpen. [&#x200B; Leer om inhoudskaarten &#x200B;](../content-card/design-content-card.md) te ontwerpen en te personaliseren.

   ![](assets/challenge-create-content.png)

Na het vormen van de inhoudskaart, opstelling overseinen om klanten door de uitdagingslevenscyclus in dienst te nemen.

### Berichten configureren {#configure-messaging}

De berichten van de opstelling multi-channel om klanten in belangrijkste stadia van de uitdagingslevenscyclus in dienst te nemen. Berichten is optioneel, maar wordt aanbevolen om de betrokkenheid van klanten te maximaliseren.

1. Navigeer naar het tabblad **[!UICONTROL Messaging]** en configureer berichten voor elk levenscyclusstadium:

   * **Lancering** bericht: Melden klanten op wanneer de uitdaging begint
   * **In-progress** bericht: Houd klanten betrokken met herinneringen en vooruitgangsupdates
   * **Voltooiing** bericht: Kwalificeer succes en bevestig bonustoewijzing

1. Voor elk stadium, uitgezochte **[!UICONTROL Add [stage] message]** (waar [ stadium ] Lancering, Bezig, of Voltooiing) vertegenwoordigt om een bericht voor dat stadium tot stand te brengen.

1. Kies het gewenste kanaal: **[!UICONTROL In-app]** , **[!UICONTROL Email]** of **[!UICONTROL Push notification]** en selecteer de gekoppelde kanaalconfiguratie.

1. Selecteer het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) en kies **[!UICONTROL Edit]** om uw berichtinhoud te ontwerpen.

   ![](assets/challenge-create-messaging.png)

Leer hoe u berichten voor specifieke kanalen maakt:

* [In-app berichten](../in-app/get-started-in-app.md)
* [E-mailberichten](../email/get-started-email.md)
* [Pushmeldingen](../push/get-started-push.md)

Na de voltooiing van de overseinenconfiguratie, bepaal welke klanten verkiesbaar zijn om aan de uitdaging deel te nemen.

## Selecteer het publiek van de uitdaging {#audience}

Bepaal welke klanten aan uw loyaliteitsuitdaging kunnen deelnemen.

1. Navigeer naar het tabblad **[!UICONTROL Audience]** en selecteer de knop **[!UICONTROL Select audience]** .

   ![](assets/challenge-create-audience.png)

1. Selecteer het doelpubliek in de lijst met beschikbare Adobe Experience Platform-doelgroepen. [&#x200B; Leer hoe te met publiek &#x200B;](../audience/about-audiences.md) te werken.

1. Selecteer **[!UICONTROL Add audience]**.

Uw uitdaging wordt nu volledig gevormd met zijn structuur, inhoud, overseinen, en doelpubliek. De laatste stap is het genereren en publiceren van de reis.

## De reis genereren en publiceren {#review-and-publish}

Genereer de reis die uw uitdagingslevering en klanteninteractie zal ordenen. Selecteer hiervoor **[!UICONTROL Generate Journey]** .

![](assets/challenge-create-generate-journey.png)

Journey Optimizer leidt automatisch tot a [&#x200B; reis &#x200B;](../building-journeys/journey-gs.md) in de status van het Ontwerp. De auto-geproduceerde reis verschijnt in uw reisinventaris met het naamformaat &quot;Uitdaging: [ Naam van de Uitdaging ]&quot;.

![](assets/challenge-create-journey.png)

Herzie de reisconfiguratie indien nodig, dan publiceer de reis om de uitdaging ter beschikking te stellen van klanten. [&#x200B; leer hoe te om een reis &#x200B;](../building-journeys/publish-journey.md) te publiceren.

De reis zal automatisch op uw gespecificeerde datum van de uitdagingsaanvang beginnen en inhoud en berichten volgens uw configuratie leveren.

>[!NOTE]
>
>De auto-geproduceerde reis kan worden aangepast om extra logica of overseinen toe te voegen. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie. Als u de uitdaging later uitgeeft, zullen om het even welke reisaanpassingen verloren gaan wanneer de reis wordt opnieuw geproduceerd.
