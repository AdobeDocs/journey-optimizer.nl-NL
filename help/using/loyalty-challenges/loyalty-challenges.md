---
solution: Journey Optimizer
product: journey optimizer
title: Loyalty Challenges
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen kunt maken en beheren om aansprekende loyaliteitsprogramma's te maken.
feature: Loyalty challenges
topic: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
version: Journey Orchestration
source-git-commit: b68c2610cbaaa8dbd86deb677562185e08d517ea
workflow-type: tm+mt
source-wordcount: '4963'
ht-degree: 0%

---


# Loyalty Challenges {#loyalty-challenges}

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Met Loyalty Challenges kunt u persoonlijke serviceaanbiedingen voor uw klanten maken, zodat u op grote schaal loyaliteitsprogramma&#39;s kunt organiseren. U kunt uitdagingen ontwerpen met specifieke taken en mijlpalen, klanten belonen voor het voltooien ervan en de ervaring leveren via Adobe Journey Optimizer-kanalen.

>[!BEGINSHADEBOX]
>
>**In deze gids:**
>
>* [ Overzicht ](#overview) - begrijp welke Uitdagingen Loyalty aanbieden
>* [ hoe het ](#how-it-works) werkt - geleidelijke werkschema van opstelling aan controle
>* [ Vereisten ](#prerequisites) - de gegevensopname van de opstelling en toestemmingen
>* [ de Uitdagingen van de Loyalty van de Toegang ](#access) - open het menu en de meningsuitdagingen
>* [ creeer uitdagingen ](#create-challenges) - bouw nieuwe loyaliteitsuitdagingen
>* [ creeer taken ](#create-tasks) - bepaal wat de klanten moeten doen
>* [ beheert uitdagingen ](#manage-challenges) - geef uit, controleer, en optimaliseer
>
>[!ENDSHADEBOX]

## Overzicht {#overview}

Loyalty Challenges laat u toe om gepersonaliseerde betrokkenheidsaanbiedingen te ontwerpen en op te stellen die klanten motiveren om specifieke acties te voltooien en beloningen te verdienen. De functie biedt een volledige oplossing voor het maken van loyaliteitsprogramma&#39;s op schaal, van het definiëren van taken en mijlpalen tot het leveren van inhoud en het volgen van prestaties langs kanalen. U kunt drie soorten uitdagingservaringen tot stand brengen, beloningen vormen, multi-kanaalberichten verzenden bij zeer belangrijke levenscyclusstadia, en prestaties controleren door automatisch geproduceerde reizen-allen terwijl het handhaven van integratie met uw extern systeem van het loyaliteitsbeheer.

## Werking {#how-it-works}

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **de gegevensopname van de opstelling** - Vorm de bronschakelaars van Experience Platform (als Capillary) aan ingeste loyaliteitsgebeurtenisgegevens die klantenacties en vooruitgang volgen.

2. **creeer een uitdaging** - bepaal de basisuitdagingseigenschappen met inbegrip van naam, type (Norm, Streak, of Opeenvolgend), publiek, en datumwaaier.

3. **voegt taken** toe - bepaal de specifieke acties klanten, met inbegrip van taaktypes (aankoop, uitgeven, bezoek, enz.), hoeveelheden, productfilters, en beloningen moeten voltooien.

4. **de inhoudskaarten van het Ontwerp** - creeer de visuele vertegenwoordiging van uw uitdaging gebruikend de inhoudskaarten van Journey Optimizer die op klantenapparaten tonen.

5. **vorm overseinen** (Facultatief) - Opstelling multi-kanaalberichten (in-app, e-mail, duw) voor zeer belangrijke stadia: lancering, lopend, en voltooiing.

6. **Overzicht en publiceer** - test uw uitdaging met testprofielen, dan publiceer het om het ter beschikking te stellen van uw doelpubliek.

7. **Auto-Geproduceerde reis** - wanneer u publiceert, leidt Journey Optimizer automatisch tot een reis die de levering en het overseinen van de inhoudskaart orkestreert.

8. **activeer reis** - de auto-geproduceerde reis activeert op uw datum van het uitdagingsbegin en beheert alle klanteninteractie.

9. **prestaties van de Monitor** - de participatie van het spoor, voltooiingstarieven, beloningsdistributie, en berichtovereenkomst door ingebouwde rapporten en het wegcanvas.

>[!NOTE]
>
>De automatisch gegenereerde reis wordt weergegeven in uw reisvoorraad en kan indien nodig worden aangepast. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie.

## Belangrijkste mogelijkheden

Loyalty-uitdagingen gebruiken voor:

* **creeer drie soorten uitdagingen**:
   * **Norm**: De klanten voltooien om het even welk aantal taken om beloningen te verdienen.
   * **Streak**: De klanten voltooien de zelfde taak veelvoudige tijden.
   * **Opeenvolgend**: De klanten voltooien taken in een specifieke orde.

* **de uitdagingsinhoud van het Ontwerp**: De inhoudskaarten van Journey Optimizer van het gebruik om de visuele vertegenwoordiging van uw uitdaging op klantenapparaten tot stand te brengen. De kaarten van de inhoud tonen de uitdagingsinformatie, vooruitgang, en beloningen op het apparaat van de klant.

* **de taakvereisten van de opstelling**: Bepaal welke klanten moeten doen om beloningen te verdienen, die omvatten:
   * Taaktypen (aankoop, bedrag uit te geven, bezoek, enz.)
   * Hoeveelheidsvereisten
   * Productinclusies/uitsluitingen waarbij gebruik wordt gemaakt van SKU&#39;s
   * Aangepaste kenmerken en voorwaarden

* **vorm beloningen**: Bepaal beloningen die de klanten of bij taakvoltooiing of na de voltooiing van de volledige uitdaging verdienen

* **verzendt berichten**: Lever berichten over veelvoudige kanalen (in-app, e-mail, duw) in zeer belangrijke stadia:
   * **Lancering**: Wanneer de uitdaging begint
   * **Bezig**: Wanneer de klanten door partway zijn
   * **Volledig**: Wanneer de klanten de uitdaging beëindigen

* **prestaties van het Spoor**: De monitor automatisch geproduceerde reizen en de prestaties van de overzichtsuitdaging

### Belangrijke beperkingen {#limitations}

* **Geen grootboeksysteem**: De Uitdagingen van de Loyalty volgen geen monetaire waarden of puntsaldi. Wanneer de klanten een uitdaging voltooien en een beloning verdienen, roept Journey Optimizer uw extern systeem van het loyaliteitsbeheer om punttoewijzing te behandelen.

* **de selectie van het publiek slechts**: U kunt bestaand publiek selecteren maar kan geen nieuw publiek van de Uitdagingen UI van de Loyalty tot stand brengen.

## Vereisten {#prerequisites}

Voordat u Loyalty Challenges gaat gebruiken, moet u controleren of u beschikt over:

* Instellingen voor gegevensinvoer

  Loyalty Challenges baseert zich op gegevens die door de bronschakelaars van Experience Platform worden opgenomen om klantenvooruitgang en taakvoltooiing te volgen.

   1. **vorm een gesteunde bronschakelaar**: Momenteel, is de Capillaire schakelaar algemeen beschikbaar. Aanvullende connectors zijn gepland.

   2. **bevestigt gegevensopname**: Zorg ervoor dat de loyaliteitsgebeurtenissen en de klantengegevens in Experience Platform stromen en beschikbaar in Journey Optimizer.

  Zie voor gedetailleerde instructies:

   * [ Experience Platform brondocumentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
   * [Bronconnectors configureren in Journey Optimizer](../start/get-started-sources.md)

* Vereiste machtigingen {#required-permissions}

Als u Loyalty Challenges wilt gebruiken, hebt u de juiste machtigingen in Journey Optimizer nodig. Neem contact op met de beheerder als u de functie niet kunt openen.

## Loyalty-uitdagingen openen {#access}

Toegang krijgen tot Loyalty-uitdagingen:

1. Selecteer in Adobe Journey Optimizer **[!UICONTROL Loyalty challenges]** in het navigatiemenu aan de linkerkant.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. De inventaris van de Uitdagingen van de Loyalty toont alle bestaande uitdagingen met informatie zoals:
   * Naam en beschrijving van uitdaging
   * Status (concept, live, gestopt, enz.)
   * Uitdagingstype (Standaard, Streak, Opeenvolgend)
   * Begin- en einddatum
   * Laatste wijzigingsdatum

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Selecteer **[!UICONTROL Create challenge]** om een nieuwe uitdaging te beginnen maken.

### Uitdagingen voor zoeken en filteren {#search-filter}

Gebruik de zoek- en filtermogelijkheden om snel specifieke uitdagingen te vinden:

#### Zoeken {#search}

Voer een naam of trefwoorden voor de vraag in om te zoeken naar overeenkomende uitdagingen in het veld **[!UICONTROL Search]** .

#### Filteren op status {#filter-by-status}

Uitdagingen met specifieke statussen weergeven in **[!UICONTROL Filter by status]** :

* Concept
* Gepland
* Live
* Voltooid
* Gestopt
* Gearchiveerd

#### Filteren op type {#filter-by-type}

Alleen Standard-, Streak- of Opeenvolgende uitdagingen weergeven met **[!UICONTROL Filter by type]**.

#### Filteren op datum {#filter-by-date}

Met **[!UICONTROL Filter by date]** kunt u uitdagingen binnen een specifiek datumbereik weergeven.

#### Filteren op labels {#filter-by-tags}

Uitdagingen weergeven met specifieke tags die zijn toegepast met **[!UICONTROL Filter by tags]** .


**[!UICONTROL Discount]**: geef een kortingscode of waarde op.

* Type korting invoeren (percentage of vast bedrag)
* Waarde van korting invoeren
* U kunt desgewenst kortingscode opgeven of het systeem een code laten genereren

**[!UICONTROL Free item]**: een gratis product of service verlenen.

* Geef het item SKU of de beschrijving op
* Geef aan hoe het gratis object moet worden geclaimd

**[!UICONTROL Custom reward]**: Definieer een aangepast beloningstype.

* Geef een bonusbeschrijving op
* Verstrek relevante codes of identificatoren
* Vorm hoe de beloning wordt geleverd of geclaimd

#### Voorbeeld van terugbetalingsconfiguratie {#reward-example}

**Uitdaging**: &quot;Uitdaging van de Lover van de Koffie&quot;

**Taak 1**: Koop 3 kassen

* Achterwaarts: 30 punten (10 punten per koffie)
* Timing: na voltooiing van de taak

**Taak 2**: Probeer 2 nieuwe seizoensgebrande dranken

* Achterwaarts: 50 punten
* Timing: na voltooiing van de taak

**de voltooiingsbeloning van de uitdaging**:

* Reward: gratis koffie + 100 bonuspunten
* Timing: Na alle taken voltooid

**Totaal mogelijke beloningen**: 180 punten + 1 vrije koffie

### Geavanceerde taakkenmerken {#advanced-attributes}

Voor geavanceerd gebruik kunt u aanvullende taakkenmerken configureren:

**[!UICONTROL Custom conditions]**: voeg aangepaste logica of voorwaarden toe die verder gaan dan de standaardtaaktypen met behulp van Experience Platform-segmenten of -regels.

**[!UICONTROL Geofencing]**: (Voor bezoektaken) Vereist u bezoeken aan specifieke locaties die worden gedefinieerd door geografische coördinaten en straal.

**[!UICONTROL Time-based requirements]**: vereisen dat taken worden voltooid tijdens specifieke uren, dagen of datumbereiken.

**[!UICONTROL Cooldown period]**: stel een minimale tijd in tussen taakvoltooiing om snelle herhaalde handelingen te voorkomen.

**[!UICONTROL Task dependencies]**: (Voor Opeenvolgende uitdagingen) Bepaal eerste vereisten die moeten worden voltooid alvorens deze taak beschikbaar wordt.

## Uitdagingen maken {#create-challenges}

Creeer een loyaliteitsuitdaging om de betrokkenheidsaanbieding te bepalen, inhoudskaarten voor levering te vormen, taken toe te voegen, beloningen op te zetten, en naar keuze overseinen over kanalen te vormen.

### Voordat u begint {#before-you-start}

Voordat u een uitdaging maakt, moet u ervoor zorgen dat:

* Gevormde en bevestigde gegevensopname door bronschakelaars
* Vereiste soorten publiek maken in Experience Platform
* Inhoud (afbeeldingen, tekst, enzovoort) voorbereiden voor uw uitdaging
* De taken en beloningen gedefinieerd die u wilt aanbieden

### Een uitdaging maken {#create-a-challenge}

Een nieuwe loyaliteitsuitdaging creëren:

1. Selecteer in Journey Optimizer **[!UICONTROL Loyalty challenges]** in het navigatiemenu aan de linkerkant.

2. Selecteer **[!UICONTROL Create challenge]** in de rechterbovenhoek.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. In het scherm van uitdagingseigenschappen, vorm het volgende:

#### Basiseigenschappen {#basic-properties}

**[!UICONTROL Name]**: ga een beschrijvende naam voor uw uitdaging in. Deze naam wordt weergegeven in de voorraad en wordt opgenomen in de automatisch gegenereerde naam van de rit.

**[!UICONTROL Description]**: (Optioneel) Voeg een beschrijving toe om u en uw team te helpen het doel en de details van deze uitdaging te begrijpen.

**[!UICONTROL Challenge type]**: Selecteer het type uitdaging dat u wilt maken:

* **[!UICONTROL Standard]**: klanten kunnen een willekeurig aantal opgegeven taken voltooien om de beloning te verdienen. Voorbeeld: &quot;Deze maand 5 aankopen doen.&quot;

* **[!UICONTROL Streak]**: klanten moeten dezelfde taak herhaaldelijk uitvoeren. Voorbeeld: &quot;Bezoek onze winkel tien keer achter elkaar.&quot;

* **[!UICONTROL Sequential]**: klanten moeten taken in een bepaalde volgorde uitvoeren. Voorbeeld: &quot;Maak eerst een aankoop, schrijf vervolgens een revisie en verwijs vervolgens een vriend.&quot;

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Start date]**: selecteer wanneer de uitdaging actief wordt en beschikbaar voor klanten.

**[!UICONTROL End date]**: selecteer wanneer de uitdaging verloopt. Klanten die de uitdaging op dit moment nog niet hebben voltooid, kunnen de beloning niet meer verdienen.

#### Selectie publiek {#audience-selection}

**[!UICONTROL Select audience]**: kies het publiek dat voor deze uitdaging in aanmerking komt. U kunt alleen bestaande soorten publiek selecteren. U kunt geen nieuwe soorten publiek maken via de gebruikersinterface voor Loyalty Challenges.

Om publiek tot stand te brengen of te verfijnen, zie [ publiek in Journey Optimizer ](../audience/about-audiences.md) bouwen.

1. Selecteer **[!UICONTROL Save as draft]** om uw uitdaging te blijven vormen.

## Taken maken {#create-tasks}

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen in een loyaliteitsuitdaging te verdienen. U kunt taaktypes, hoeveelheden, productvereisten, en beloningswaarden vormen om het in dienst nemen en gepersonaliseerde loyaliteitservaringen tot stand te brengen.

### Taakoverzicht {#task-overview}

Elke taak vertegenwoordigt een meetbare actie die tot uitdagingsvoltooiing bijdraagt. Afhankelijk van uw uitdagingstype (Standaard, Streak, of Opeenvolgend), voltooien de klanten taken verschillend:

* **Standaard uitdagingen**: De klanten voltooien om het even welk gespecificeerd aantal taken in om het even welke orde
* **de uitdagingen van de Streak**: De klanten voltooien achtereenvolgens de zelfde taak veelvoudige tijden
* **Opeenvolgende uitdagingen**: De klanten voltooien taken in een bepaalde orde

### Een taak toevoegen {#add-task}

Om een taak aan uw uitdaging toe te voegen:

1. Open de uitdaging of maak een nieuwe.

2. Ga naar de sectie **[!UICONTROL Tasks]** .

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

3. Selecteer **[!UICONTROL Add task]** of **[!UICONTROL Create new task]** .

4. In het scherm van de taakverwezenlijking, vorm de volgende eigenschappen.

### Taakeigenschappen {#task-properties}

#### Basistaakinformatie {#basic-info}

**[!UICONTROL Task name]**: voer een beschrijvende naam in voor de taak. Deze naam is zichtbaar voor u en uw team, maar wordt mogelijk niet weergegeven aan klanten, afhankelijk van het ontwerp van uw inhoudskaart.

**[!UICONTROL Task description]**: (Optioneel) Voeg details toe over het taakdoel of de vereisten.

**[!UICONTROL Task type]**: Selecteer het type handeling dat klanten moeten uitvoeren. De beschikbare taaktypes omvatten:

* **[!UICONTROL Purchase]**: de klant maakt een aankooptransactie
* **[!UICONTROL Spend amount]**: de klant geeft een bepaald geldbedrag door
* **[!UICONTROL Visit]**: de klant bezoekt een fysieke locatie of een digitale eigenschap
* **[!UICONTROL Engagement]**: de klant werkt met inhoud, zoals het bekijken van een video of het lezen van een artikel
* **[!UICONTROL Custom event]**: de klant activeert een aangepaste gebeurtenis die door uw gegevensinvoer wordt bijgehouden

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

#### Hoeveelheidsvereisten {#quantity-requirements}

**[!UICONTROL Required quantity]**: geef op hoe vaak de klant de taak moet uitvoeren om deze te voltooien.

Bijvoorbeeld:

* Voor een aankooptaak: &quot;2 objecten kopen&quot; (hoeveelheid = 2)
* Voor een taak voor het betalen van bedragen: &quot;Besteed $50&quot; (hoeveelheid = 50)
* Voor een bezoektaak: &quot;Bezoek 5 keer&quot; (hoeveelheid = 5)

**[!UICONTROL Tracking period]**: (Optioneel) Definieer het tijdvenster voor het voltooien van deze taak:

* Per challenge duration (standaardwaarde)
* Per dag
* Per week
* Per maand
* Aangepast datumbereik

### Filteren van producten en SKU {#product-filtering}

Voor de taken Aankoop en Kosten kunt u opgeven welke producten in aanmerking komen voor het uitvoeren van taken.

#### Productinclusies {#product-inclusions}

Bepaal welke producten of categorieën op de taak tellen:

1. Selecteer **[!UICONTROL Add product criteria]**.

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

2. Kies hoe in aanmerking komende producten moeten worden gedefinieerd:
   * **[!UICONTROL By SKU]**: specifieke product-SKU-codes invoeren
   * **[!UICONTROL By category]**: Selecteer productcategorieën in de catalogus
   * **[!UICONTROL By attribute]**: filteren op productkenmerken, zoals merk, grootte, kleur of aangepaste kenmerken

3. Voer de product-id&#39;s in of selecteer deze:

   **Voorbeeld - door SKU**:

   ```text
   SKU001, SKU002, SKU003
   ```

   **Voorbeeld - door categorie**:

   * Beverages > Koffie
   * Bakkerij > Poostenrijk

   **Voorbeeld - door attribuut**:

   * Merk = &quot;Premium Brand&quot;
   * Categorie = &quot;Seizoenitems&quot;
   * Prijs > $20

4. Selecteer **[!UICONTROL Add]** om de productcriteria op te slaan.

#### Productuitsluitingen {#product-exclusions}

U kunt desgewenst uitsluiten dat bepaalde producten naar de taak worden afgeteld:

1. Selecteer **[!UICONTROL Add exclusions]**.

2. Gebruik dezelfde filtermethoden als bij productinclusies om aan te geven welke producten moeten worden uitgesloten.

3. Gemeenschappelijke uitsluitingsscenario&#39;s:

   * Verkoop- of opruimposten
   * Cadeaukaarten
   * Promotie- of gratis objecten
   * Specifieke merken of categorieën

>[!NOTE]
>
>**Insluiting en uitsluitingslogica**: Wanneer zowel de opneming als de uitsluitingen worden bepaald:
>
>* Producten moeten voldoen aan inclusiecriteria
>* Producten die voldoen aan uitsluitingscriteria worden verwijderd, zelfs als ze overeenkomen met inclusies
>* Als er geen inclusies zijn gedefinieerd, komen alle producten in aanmerking, behalve die welke expliciet zijn uitgesloten

#### Voorbeelden van productfiltering {#product-filtering-examples}

##### Voorbeeld 1: Koffieprobleem {#example-1}

* Taaktype: Aanschaffen
* Vereiste hoeveelheid: 3
* Inclusief: Categorie = &quot;Beverages > Koffie&quot;
* Resultaat: Klant moet 3 koffiedranken kopen

##### Voorbeeld 2: Premium-uitgaven {#example-2}

* Taaktype: bestedingsbedrag
* Vereist aantal: $100
* Inclusief: Merk = &quot;Premium Brand&quot;
* Uitsluitingen: categorie = &quot;goedkeuring&quot;
* Resultaat: de klant moet $100 uitgeven aan Premium Brand-objecten, exclusief klaringsobjecten

##### Voorbeeld 3: Specifieke productaankoop {#example-3}

* Taaktype: Aanschaffen
* Vereiste hoeveelheid: 1
* Inclusies: SKU = &quot;NEWPRODUCT2024&quot;
* Resultaat: de klant moet het specifieke product kopen met SKU &quot;NEWPRODUCT2024&quot;

### Rente configureren {#configure-rewards}

Bepaal welke klanten verdienen voor het uitvoeren van taken. De beloningen kunnen op het taakniveau of op het uitdagingsniveau worden verleend nadat alle taken volledig zijn.

#### Reward timing {#reward-timing}

Kies wanneer klanten beloningen ontvangen:

**[!UICONTROL After task completion]**: Klanten ontvangen direct na het voltooien van deze specifieke taak een beloning (ook wel &quot;progressieve beloningen&quot; of &quot;milestone-beloningen&quot; genoemd).

**[!UICONTROL After challenge completion]**: Klanten ontvangen pas een beloning nadat ze alle vereiste taken in de uitdaging hebben uitgevoerd (ook wel &#39;definitieve beloningen&#39; of &#39;grote prijzen&#39; genoemd).

>[!TIP]
>
>U kunt beide beloningstypen combineren in één uitdaging om de betrokkenheid gedurende de hele reis van de klant te behouden. Bijvoorbeeld:
>
>* Geef 10 punten na elke taakvoltooiing (progressieve beloningen)
>* Geef 100 extra punten na het voltooien van de hele uitdaging (uiteindelijke beloning)

#### Soorten en waarden achterwaarts {#reward-types}

**[!UICONTROL Points]**: De loyaliteit van de prijs wijst aan de rekening van de klant.

* Voer het aantal punten in (bijvoorbeeld 100)
* De punten worden meegedeeld aan uw extern loyaliteitsbeheerssysteem via API

## Inhoudskaarten configureren {#configure-content-cards}

Inhoudskaarten zijn de belangrijkste manieren waarop klanten op hun apparaten voor uitdagingen staan. U moet een inhoudskaart voor uw uitdaging vormen.

1. Navigeer in uw uitnodiging naar de tab **[!UICONTROL Content]** .

2. Selecteer **[!UICONTROL Edit content]** om de inhoudskaarteditor te openen.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Configureer de eigenschappen van de inhoudskaart:

   **[!UICONTROL Configuration name]**: voer een naam in voor deze inhoudskaartconfiguratie.

   **[!UICONTROL Configuration]**: selecteer of maak een inhoudskaartconfiguratie. Dit bepaalt technische montages voor hoe de inhoudskaart wordt geleverd.

4. Ontwerp in de inhoudskaart redacteur, uw uitdagingskaart:

   * Voeg tekst toe om de uitdaging, de taken, en de beloningen te beschrijven
   * Afbeeldingen of andere visuele elementen opnemen
   * De verpersoonlijking van het gebruik om klant-specifieke informatie te omvatten
   * Voortgangsindicatoren weergeven indien van toepassing
   * Call-to-action-knoppen toevoegen

   De inhoudcard-editor biedt dezelfde mogelijkheden als andere Journey Optimizer-kanalen. Voor gedetailleerde begeleiding, zie [ de inhoudskaarten van het Ontwerp ](../content-card/design-content-card.md).

5. Selecteer **[!UICONTROL Save]** om de configuratie van de inhoudskaart op te slaan.

>[!NOTE]
>
>De inhoudskaart wordt geleverd door de auto-geproduceerde reis. Het wordt getoond aan in aanmerking komende publieksleden wanneer de uitdaging actief is.

## Berichten configureren {#configure-messaging}

U kunt naar keuze berichten vormen die naar klanten in zeer belangrijke stadia van de uitdagingslevenscyclus moeten worden verzonden. Het overseinen is beschikbaar voor drie stadia:

* **[!UICONTROL Launch]**: verzend een bericht wanneer de uitdaging actief wordt
* **[!UICONTROL In progress]**: verzend een bericht wanneer klanten door de uitdaging partway zijn
* **[!UICONTROL Complete]**: verzend een bericht wanneer klanten de uitdaging voltooien

### Berichten toevoegen {#add-messages}

1. Navigeer in uw uitnodiging naar de tab **[!UICONTROL Messaging]** .

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Selecteer het werkgebied waaraan u het bericht Starten, Bezig of Voltooien wilt toevoegen.

3. Selecteer **[!UICONTROL Add message]**.

4. Kies het kanaal voor uw bericht:
   * **[!UICONTROL In-app]**: een bericht weergeven in uw toepassing
   * **[!UICONTROL Email]**: een e-mailmelding verzenden
   * **[!UICONTROL Push]**: een pushmelding verzenden

5. Selecteer **[!UICONTROL Edit content]** om de inhoudeditor voor het geselecteerde kanaal te openen.

6. Ontwerp uw bericht met de standaardinhoudseditor:
   * Tekst, afbeeldingen en andere inhoudselementen toevoegen
   * De verpersoonlijking van het gebruik om klant-specifieke informatie te omvatten
   * Neem uitdagingsdetails zoals vooruitgang of beloningen op
   * Dynamische inhoud toevoegen op basis van klantkenmerken of gedrag

   Zie voor kanaalspecifieke richtlijnen:
   * [In-app berichten maken](../in-app/create-in-app.md)
   * [E-mails maken](../email/create-email.md)
   * [Pushberichten maken](../push/create-push.md)

7. Selecteer **[!UICONTROL Save]** om uw bericht op te slaan.

8. Herhaal deze stappen om berichten voor andere stadia of kanalen toe te voegen zoals nodig.

>[!NOTE]
>
>U kunt meerdere berichten per werkgebied toevoegen, zodat u klanten op verschillende kanalen kunt bereiken. U kunt bijvoorbeeld zowel een e-mail als een pushmelding verzenden wanneer een challenge wordt gestart.

### Berichttiming en -triggers {#message-timing}

**berichten van de Lancering**: Verzonden wanneer de uitdaging aan het in aanmerking komende publiek actief wordt.

**lopend berichten**: Teweeggebracht wanneer de klanten een gespecificeerd vooruitgangspunt bereiken. U kunt de triggervoorwaarden configureren op basis van:

* Aantal voltooide taken
* Percentage van de voltooide uitdaging
* Specifieke taak voltooid
* Tijd verstreken sinds aanvechtingstijd

**Volledige berichten**: Verzonden wanneer de klanten met succes alle vereiste taken voltooien.

>[!TIP]
>
>**Beste praktijken voor overseinen**:
>
>* Houd berichten beknopt en concentreer zich op de uitdaging
>* Geef de waarde en beloningen duidelijk weer
>* Gebruik consistente branding en toon
>* Duidelijke oproepen tot actie opnemen
>* De berichten van de test alvorens uw uitdaging te publiceren

## Reizen genereren en aanpassen {#generate-journey}

Wanneer u een uitdaging opslaat waarvoor inhoud en berichten zijn geconfigureerd, genereert Journey Optimizer automatisch een reis op de achtergrond.

### Hoe het genereren van reizen werkt {#journey-generation-process}

1. Wanneer u een challenge opslaat en **[!UICONTROL Generate journey]** selecteert, maakt Journey Optimizer een nieuwe reis.

2. De reis wordt automatisch genoemd gebaseerd op de uitdagingsnaam (b.v., &quot;Uitdaging: [ Uw Naam van de Uitdaging ]&quot;).

3. Het reiscanvas omvat:
   * **[!UICONTROL Read audience]** activiteit met het geselecteerde publiek
   * **kaart van de Inhoud** leveringsactie
   * **de activiteiten van het Bericht** voor om het even welke berichten u (Lanceer, Bezig, Voltooid) vormde
   * **wacht** en **Voorwaarde** activiteiten zoals nodig gebaseerd op uw configuratie

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. De reis verschijnt in uw reisinventaris en is zichtbaar aan alle gebruikers met aangewezen toestemmingen.

### Bekijk de gegenereerde reis {#view-journey}

De automatisch gegenereerde reis weergeven:

1. Navigeer naar **[!UICONTROL Journeys]** in het navigatiemenu links.

2. Zoek de reis door uitdagingsnaam, of filter door markeringen als u hen hebt toegewezen.

3. Selecteer de reis om zijn canvas en configuratie te bekijken.

### De reis aanpassen {#customize-journey}

U kunt de auto-geproduceerde reis uitgeven om douanelogica, extra activiteiten, of geavanceerde configuraties toe te voegen.

>[!IMPORTANT]
>
>**Belangrijke overwegingen wanneer het uitgeven van reizen**:
>
>* De veranderingen die aan het wegcanvas **worden aangebracht synchroniseren niet terug** aan de Uitdagingen UI van de Loyalty
>* De uitdaging blijft de bron van de waarheid voor de definitie van de kernervaring
>* Journey Optimizer geeft een waarschuwing weer wanneer u de aangepaste bewerkingsmodus opent
>* Als u veranderingen in taken, beloningen, of eigenschappen van de kernuitdaging moet aanbrengen, geef hen in de UI van de Uitdagingen van de Loyalty, niet de reis uit
>* Aangepaste reisbewerkingen zijn geschikt voor geavanceerde routering, timing of integratie-logica

De reis aanpassen:

1. Open de gegenereerde reis vanuit de reisvoorraad.

2. Journey Optimizer geeft een waarschuwing over aangepaste bewerkingen weer. Lees de waarschuwing zorgvuldig door en erken deze.

3. Breng de gewenste wijzigingen aan met het canvas van de reis:
   * Aanvullende activiteiten toevoegen (wachten, voorwaarden, handelingen)
   * Geavanceerde tijdinstellingen of frequentieregels configureren
   * Aangepaste acties of integratie toevoegen
   * De voorwaarden voor publieksinvoer wijzigen

4. Test uw wijzigingen grondig voordat u gaat publiceren.

5. Publiceer de reis als u klaar bent.

Voor gedetailleerde reis die begeleiding uitgeeft, zie [ reizen bouwen ](../building-journeys/journey-gs.md).

### Reiscanvasoverwegingen {#journey-considerations}

Wanneer u werkt met automatisch gegenereerde reizen:

* **kan publiek in reis** niet uitgeven: Als u het publiek moet veranderen, doe dit in de Uitdagingen UI van de Loyalty en regenerate de reis.

* **de inhoudsupdates van het Bericht**: De veranderingen in berichtinhoud zouden in de Uitdagingen UI moeten worden aangebracht Loyalty om consistentie te handhaven.

* **de status van de Reis**: De reisstatus (Ontwerp, Levend, Geconstrueerd) wordt beheerd onafhankelijk van de uitdagingsstatus.

* **het Testen**: Test de volledige uitdagingservaring, niet alleen de reis, om alle componenten te verzekeren werken correct samen.

## Reviseren en publiceren {#review-and-publish}

Voordat u uw uitdaging publiceert:

1. **Overzicht alle componenten**:
   * Eigenschappen en datums van uitdagingen
   * Taken en taakvereisten
   * Rewards-configuratie
   * Ontwerp van inhoudskaart
   * Inhoud en timing van berichten
   * Gegenereerde reisstructuur

2. **Test de ervaring**:
   * Testprofielen gebruiken om de rendering van inhoud te valideren
   * Controleren of taken correct worden geactiveerd op basis van testgegevens
   * De logica voor bonustoewijzing verifiëren
   * Het overseinen van de test over alle gevormde kanalen
   * Evalueer de uitvoering van de reis met testpubliek

3. **publiceer uw uitdaging**:
   * Indien gereed, selecteert u **[!UICONTROL Publish]** in de challenge-eigenschappen
   * De uitdaging wordt actief op de gespecificeerde begindatum
   * De automatisch gegenereerde reis wordt geactiveerd
   * Leden van een publiek die in aanmerking komen, kunnen de uitdaging zien en hieraan deelnemen

## Uitdagingen beheren {#manage-challenges}

Na het creëren van en het publiceren van loyaliteitsuitdagingen, kunt u hen bekijken, uitgeven, controleren en optimaliseren om ervoor te zorgen zij de gewenste resultaten voor uw loyaliteitsprogramma leveren.

### Uitdagingsstatus {#challenge-statuses}

Elke uitdaging beweegt zich door een levenscyclus die door zijn status wordt weerspiegeld:

**[!UICONTROL Draft]**: Uitdaging wordt gemaakt of bewerkt, maar nog niet gepubliceerd. U kunt om het even welke veranderingen in ontwerpuitdagingen aanbrengen.

**[!UICONTROL Scheduled]**: Uitdaging wordt gepubliceerd en wordt actief op de begindatum. Klanten kunnen de geplande uitdagingen nog niet zien of hieraan deelnemen.

**[!UICONTROL Live]**: Uitdaging is actief en klanten in het in aanmerking komende publiek kunnen deze zien en hieraan deelnemen. Deze status wordt weergegeven wanneer de huidige datum tussen de begin- en einddatum ligt.

**[!UICONTROL Completed]**: De uitdaging heeft zijn einddatum bereikt of alle doelstellingen zijn verwezenlijkt. Klanten kunnen niet langer deelnemen, maar u kunt historische gegevens en resultaten bekijken.

**[!UICONTROL Stopped]**: Uitdaging is handmatig gestopt voordat de bewerking is voltooid. Klanten kunnen niet langer deelnemen. Als u een niet-uitgevoerde taak opnieuw wilt activeren, moet u deze dupliceren en een nieuwe versie maken.

**[!UICONTROL Archived]**: De uitdaging is gearchiveerd voor organisatorische doeleinden. Gearchiveerde uitdagingen kunnen worden opgehaald met behulp van filters, maar zijn verborgen in de standaardweergave.

### Uitdagingsdetails weergeven {#view-details}

Om gedetailleerde informatie over een uitdaging te bekijken:

1. Klik in de inventaris op de naam van de uitdaging of selecteer het menu **[!UICONTROL More actions]** (drie punten) en kies **[!UICONTROL View details]** .

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. Het scherm van de uitdagingsdetails toont:

   **[!UICONTROL Overview]** tab:
   * Basiseigenschappen (naam, beschrijving, type, datums)
   * Huidige status en levenscyclusinformatie
   * Publiek-informatie
   * Aanmaakgeschiedenis en wijzigingshistorie

   **[!UICONTROL Tasks]** tab:
   * Lijst van alle taken in de uitdaging
   * Taaktypen, -vereisten en -voorwaarden
   * Gevormde beloningen per taak

   **[!UICONTROL Content]** tab:
   * Configuratie en voorvertoning van inhoudskaart
   * Visuele teruggeven van hoe de uitdaging aan klanten lijkt

   **[!UICONTROL Messaging]** tab:
   * Gevormde berichten voor Lanceren, Bezig, en Volledige stadia
   * Kanaaltoewijzingen en voorvertoningen van inhoud

   **[!UICONTROL Performance]** tabblad (voor Live- en Voltooide uitdagingen):
   * Metrische gegevens voor deelname
   * Voltooiingsgraad
   * Retourdistributie
   * Berichtgevingsstatistieken

### Uitdagingen bewerken {#edit-challenges}

U kunt uitdagingen afhankelijk van hun huidige status uitgeven.

#### Concepten bewerken {#edit-draft}

Voor uitdagingen in **[!UICONTROL Draft]** status:

1. Klik op de naam van de uitdaging of selecteer **[!UICONTROL Edit]** in het menu Handelingen.

2. Wijzig om het even welk aspect van de uitdaging:
   * Basiseigenschappen
   * Taken en beloningen
   * Inhoudskaarten
   * Berichten
   * Selectie publiek

3. Selecteer **[!UICONTROL Save as draft]** om wijzigingen op te slaan zonder te publiceren of **[!UICONTROL Publish]** om de uitdaging actief te maken.

#### Gepubliceerde uitdagingen bewerken {#edit-published}

Voor uitdagingen die **[!UICONTROL Scheduled]** of **[!UICONTROL Live]** zijn:

>[!IMPORTANT]
>
>**Gevolgen van het uitgeven van levende uitdagingen**: De veranderingen in levende uitdagingen kunnen klanten reeds deelnemende beïnvloeden. Overweeg het volgende voordat u wijzigingen aanbrengt:
>
>* Het wijzigen van taakvereisten kan de vooruitgang van de klant ongeldig maken
>* Het veranderen van beloningen kan inconsistenties veroorzaken voor klanten die reeds beloningen hebben verdiend
>* Wijzigingen in het publiek kunnen klanten uitsluiten die voorheen in aanmerking kwamen
>* Wijzigingen in inhoud worden direct aan klanten weergegeven
>
>Voor significante veranderingen, denk het tegenhouden van de huidige uitdaging en het creëren van een nieuwe versie.

**Beperkte het uitgeven voor levende uitdagingen**:

U kunt deze wijzigingen doorvoeren in de dagelijkse uitdagingen zonder ze te stoppen:

* Uitdagingsbeschrijving bijwerken (intern-onder ogen ziet)
* De visuele en tekstweergave van een inhoudskaart wijzigen
* Berichteninhoud bijwerken
* Einddatum aanpassen (alleen verlengen, niet verkorten)
* Tags toevoegen of wijzigen

**Veranderingen die uitdagingsduplicatie** vereisen:

Als u deze eigenschappen wilt wijzigen, moet u de controle dupliceren en een nieuwe versie maken:

* Uitdagingstype (Standaard, Streak, Opeenvolgend)
* Taakvereisten en -voorwaarden
* Rendwaarden en toewijzingsregels
* Begindatum (voor live-uitdagingen)
* Publiek (grote veranderingen)

### Een uitdaging dupliceren {#duplicate-challenge}

Het dupliceren leidt tot een exemplaar van een bestaande uitdaging die u als nieuwe uitdaging kunt wijzigen en publiceren:

1. Selecteer in de inventaris het menu **[!UICONTROL More actions]** (drie punten) voor de uitdaging die u wilt dupliceren.

2. Selecteer **[!UICONTROL Duplicate]**.

3. In het dialoogvenster Overlappingen:
   * Ga een nieuwe naam voor de gedupliceerde uitdaging in
   * Wijzig desgewenst de beschrijving
   * Kies of u publieksinstellingen wilt kopiëren
   * Kies of u berichtconfiguraties wilt kopiëren

4. Selecteer **[!UICONTROL Duplicate]**.

5. De gedupliceerde uitdaging wordt geopend in de conceptmodus, waar u wijzigingen kunt aanbrengen voordat u publiceert.

**Gemeenschappelijke dubbel scenario&#39;s**:

* Hervat een succesvolle uitdaging voor een nieuwe tijdsperiode
* Variaties maken voor een uitdaging voor verschillende soorten publiek
* Taken of beloningen voor een nieuwe versie bijwerken
* Een gestopt of voltooid probleem opnieuw activeren

### Een uitdaging beëindigen {#stop-challenge}

Om een levende of geplande uitdaging vóór zijn natuurlijke einddatum tegen te houden:

1. Selecteer de uitdaging in de inventaris.

2. Selecteer **[!UICONTROL Stop challenge]** in het menu Handelingen.

3. Controleer in het bevestigingsdialoogvenster het effect:
   * Klanten die momenteel deelnemen, kunnen geen voortgang meer maken
   * Klanten die taken hebben voltooid maar niet de volledige uitdaging hebben, ontvangen geen definitieve beloningen
   * De bijbehorende reis wordt gestopt
   * De uitdaging kan niet opnieuw worden begonnen (moet dupliceren om opnieuw te gebruiken)

4. Selecteer **[!UICONTROL Stop]** om te bevestigen.

>[!NOTE]
>
>**die tegen** stopt: Een tegengehouden uitdaging beëindigt voortijdig en volgt niet het normale voltooiingsproces. Klanten ontvangen al toegewezen gedeeltelijke beloningen, maar geen definitieve beloningen voor het voltooien van uitdagingen. Overweeg het vroege eind aan beïnvloede klanten mee te delen.

### Archiefuitdagingen {#archive}

Archiveer voltooid of opgehouden uitdagingen om uw voorraad te organiseren:

1. Selecteer het menu **[!UICONTROL More actions]** (drie punten) voor de uitdaging.

2. Selecteer **[!UICONTROL Archive]**.

3. De uitdaging beweegt zich aan gearchiveerde status en is verborgen van de standaardinventarismening.

Gearchiveerde uitdagingen weergeven:

1. Pas in de inventaris het filter **[!UICONTROL Status]** toe.

2. Selecteer **[!UICONTROL Archived]**.

3. Gearchiveerde uitdagingen worden weergegeven met dezelfde informatie als actieve uitdagingen.

Een uitdaging ongedaan maken:

1. Zoek de gearchiveerde uitdaging met behulp van filters.

2. Selecteer **[!UICONTROL Unarchive]** in het menu Handelingen.

3. De uitdaging keert op zijn vorige status (Voltooid of Gestopt) terug.

### Uitdagingen verwijderen {#delete}

Verwijder uitdagingen die u niet meer nodig hebt:

>[!IMPORTANT]
>
>**Schrapping is permanent**: De geschrapte uitdagingen kunnen niet worden teruggekregen. Alleen uitdagingen verwijderen die u zeker niet nodig hebt in de toekomst. Overweeg archivering in plaats van verwijderen om historische records te onderhouden.

**de regels van de Schrapping**:

* U kunt alleen uitdagingen verwijderen in de status **[!UICONTROL Draft]**
* Gepubliceerde, geplande, live of voltooide uitdagingen kunnen niet worden verwijderd
* Om een gepubliceerde uitdaging te verwijderen, moet u het eerst tegenhouden, dan het archiveren

Een conceptcontrole verwijderen:

1. Selecteer het menu **[!UICONTROL More actions]** (drie punten) voor de uitdaging.

2. Selecteer **[!UICONTROL Delete]**.

3. Bevestig de verwijdering in het bevestigingsvenster.

## Monitorprestaties {#monitor-performance}

Houd bij hoe klanten met uw uitdagingen omgaan met behulp van ingebouwde prestatiemetriek.

### Prestatiewaarden {#performance-metrics}

Het lusje van Prestaties toont zeer belangrijke metriek voor levende en voltooide uitdagingen:

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Participation metrics]**:

* **Totale in aanmerking komende klanten**: Aantal klanten in het doelpubliek
* **Ingeschreven klanten**: Aantal klanten die of met de uitdaging bekeken in dienst genomen
* **het tarief van de Inschrijving**: Percentage van in aanmerking komende klanten die ingeschreven
* **Actieve deelnemers**: Aantal klanten die momenteel vooruitgang maken

**[!UICONTROL Completion metrics]**:

* **voltooide Klanten**: Aantal klanten die alle taken beëindigden
* **het tarief van de Voltooiing**: Percentage ingeschreven klanten die de uitdaging voltooiden
* **Gemiddelde voltooiingstijd**: Gemiddelde tijd van inschrijving aan voltooiing
* **voltooide Taken**: Het totale aantal individuele die taken over alle klanten worden voltooid

**[!UICONTROL Reward metrics]**:

* **Totaal verdeelde beloningen**: Som van alle toegewezen beloningen
* **Beloningen door type**: Uitsplitsing door punten, kortingen, vrije punten, enz.
* **Gemiddelde beloning per klant**: Gemiddelde beloningswaarde voor deelnemende klanten

**[!UICONTROL Engagement metrics]**:

* **de kaartindrukkingen van de Inhoud**: Aantal tijden de uitdaging werd getoond
* **kaart van de Inhoud klikt**: Aantal tijden klanten interactie hadden met de uitdagingskaart
* **levering van het Bericht**: Aantal berichten die voor Lancering, Bezig, en Volledige stadia worden verzonden
* **Overeenkomst van het Bericht**: Open tarieven, klik tarieven voor berichten door stadium en kanaal

### Prestatierapporten weergeven {#view-reports}

Voor toegang tot gedetailleerde prestatiegegevens:

1. Open de challenge en navigeer aan het **[!UICONTROL Performance]** lusje.

2. Selecteer het datumbereik voor rapportage (Vandaag, Laatste 7 dagen, Laatste 30 dagen, Aangepast bereik).

3. Metrische gegevens bekijken op:
   * **Overzicht**: Samenvatting op hoog niveau van zeer belangrijke metriek
   * **Chronologie**: De tendensen van prestaties in tijd
   * **Uitsplitsing**: De metriek die door klantenattributen, kanalen, of taken wordt gesegmenteerd

4. Exporteer rapporten met de knop **[!UICONTROL Export]** voor verdere analyse.

### Bewaak de gegenereerde reis {#monitor-journey}

De automatisch gegenereerde reis bevat waardevolle uitvoeringsgegevens:

1. Selecteer in de details over de vraag **[!UICONTROL View journey]** om de bijbehorende reis te openen.

2. In de reiscanvas, herzie:
   * **rapport van de Reis**: Algemene uitvoeringsstatistieken
   * **de rapporten van de Activiteit**: Prestaties van individuele activiteiten
   * **Ingang en uitgangsmetriek**: Hoeveel klanten ingegaan en weggegaan
   * **Logboeken van de Fout**: Om het even welke uitvoeringskwesties of mislukkingen

3. Reisbewaking gebruiken om na te gaan:
   * Problemen waarbij klanten wegvallen
   * Technische problemen in verband met de levering
   * Berichtprestaties per kanaal
   * Optimalisatiemogelijkheden voor timing

Voor gedetailleerde reismonitorbegeleiding, zie [ uw reizen ](../building-journeys/report-journey.md) controleren.

### Uitdagingen optimaliseren {#optimize}

Gebruik prestatiegegevens om de huidige en toekomstige uitdagingen te verbeteren:

**[!UICONTROL Test variations]**: Maak dubbele uitdagingen met verschillende taken, beloningen of berichten om de prestaties te vergelijken.

**[!UICONTROL Adjust timing]**: Wijzig de duur van de uitdaging of de taakdeadlines op basis van de voltooiingspatronen.

**[!UICONTROL Refine audience]**: Breid of versmal publieksselectie uit op basis van betrokkenheid en voltooiingstarieven.

**[!UICONTROL Update content]**: vernieuw inhoudskaarten en berichten om interesse en duidelijkheid te behouden.

**[!UICONTROL Reward optimization]**: pas beloningswaarden aan om kosten en deelname in evenwicht te brengen.

**[!UICONTROL Task difficulty]**: wijzig taakvereisten als deze te gemakkelijk of te moeilijk zijn op basis van voltooiingsgegevens.

## Taakvalidatie en -tests {#validation-testing}

Alvorens uw uitdaging te publiceren, bevestig dat de taken correct worden gevormd:

1. **de taaklogica van 0} Controle:**
   * Controleren of de vereisten voor de hoeveelheid realistisch zijn
   * Zorg ervoor dat de criteria voor productfiltering correct zijn
   * Bevestig beloningen correct worden gevormd

2. **Test met testprofielen**:
   * Testprofielen maken die verschillende klantscenario&#39;s vertegenwoordigen
   * Verstuur testgebeurtenissen door uw gegevensinvoer pijpleiding
   * Controleren of taken correct worden geactiveerd
   * Bevestigen dat beloningen zijn toegewezen zoals verwacht

3. **de gegevenstoewijzing van het Overzicht**:
   * Zorg ervoor dat de inkomende gebeurtenisgegevens correct worden toegewezen aan de taakvereisten
   * Valideer dat SKU&#39;s, categorieën en kenmerken overeenkomen tussen uw bronsysteem en Journey Optimizer
   * Testen van randen (ontbrekende gegevens, ongeldige waarden enz.)

## Best practices {#best-practices}

### Uitdaging creëren

**Begin eenvoudig**: Voor uw eerste uitdaging, begin met een eenvoudige standaarduitdaging om met het proces vertrouwd te maken.

**Test grondig**: Test altijd uw uitdaging met testprofielen en publiek alvorens aan uw volledige klantenbasis te publiceren.

**Duidelijke mededeling**: Zorg klanten begrijpen wat zij moeten doen, wat zij, en tegen wanneer zullen verdienen.

**Realistische timing**: Plaats aangewezen begin en einddata, toestaand klanten genoeg tijd om de uitdaging te voltooien.

**Verschijnende beloningen**: Maak beloningen waardevol en relevant voor uw publiek om participatie te drijven.

### Taakconfiguratie

**Duidelijke vereisten**: Maak taakvereisten duidelijk en haalbaar. Vermijd al te complexe omstandigheden.

**Passende moeilijkheid**: De taakmoeilijkheid van het saldo met beloningswaarde. Complexere taken zouden meer beloningen moeten opleveren.

**Product het filtreren nauwkeurigheid**: Het tweemaal controleren SKUs, categorieën, en attributen om nauwkeurige product aanpassing te verzekeren.

**Progressieve beloningen**: De beloningen van het gebruik milestone (na taakvoltooiing) om klantenbetrokkenheid door de uitdaging te handhaven.

**Flexibiliteit**: Voor Standaard uitdagingen, sta flexibiliteit in toe hoe de klanten taken voltooien om verschillend gedrag en voorkeur aan te passen.

### Beheer en toezicht

**Regelmatige controle**: De uitdagingsprestaties van de controle minstens wekelijks voor levende uitdagingen om kwesties vroegtijdig te identificeren.

**Duidelijke het noemen**: De beschrijvende namen van het gebruik die op het uitdagingsdoel, het publiek, of de tijdspanne voor gemakkelijke organisatie wijzen.

**de markeringen van het Gebruik**: Pas verenigbare markeringen toe om uitdagingen door campagne, seizoen, publiekssegment, of andere relevante attributen te categoriseren.

**de veranderingen van het Document**: Houd nota&#39;s op waarom u veranderingen in uitdagingen voor toekomstig verwijzing en het leren aanbracht.

**altijd Archief**: De voltooide uitdagingen van het archief regelmatig om uw inventaris beheerbaar te houden.

**Communiceer veranderingen**: Als u een levende uitdaging wijzigt, informeer beïnvloede klanten over veranderingen die hun participatie beïnvloeden.

**analyseert na voltooiing**: De prestaties van het overzicht na elke uitdaging beëindigt om lessen te identificeren die voor toekomstige uitdagingen worden geleerd.

**Graduele rollout**: Voor nieuwe uitdagingstypes of significante veranderingen, overweeg aanvang met een kleiner publiek vóór volledige plaatsing.

**de controle van de Versie**: De duidelijke versie van het gebruik in uitdagingsnamen wanneer het creëren van herhalingen (b.v., &quot;Uitdaging 2024 van de Vakantie - v2&quot;).

## Problemen oplossen {#troubleshooting}

**Uitdaging die niet aan klanten** verschijnt:

* Controleren of de uitdaging de status Live heeft
* Controleren of klanten zich in het in aanmerking komende publiek bevinden
* Bevestig dat de configuratie van de inhoudskaart juist is
* Bekijk de logboeken voor de uitvoering van de reis voor leveringsproblemen

**Lage participatiecijfers**:

* Zichtbaarheid van inhoudskaart en beroep bekijken
* Controleren of berichten de waarde duidelijk meedelen
* Zorg ervoor dat taken haalbaar zijn en dat beloningen aantrekkelijk zijn
* Controleren of doelgroepen geschikt zijn

**Taken teweegbrengend niet**:

* Verifieer het gegeven correct van bronschakelaars wordt opgenomen
* Controleren of gebeurteniskenmerken overeenkomen met taakvereisten
* De geschiktheid van het publiek controleren

**beloningen die** niet toewijzen:

* Bevestig beloningsconfiguratie correct is
* De verbinding met het externe systeem voor loyaliteitsbeheer controleren
* Controleren op fouten in leveringslogs voor beloning

**het filtreren van het Product het niet werken**:

* SKU-codes en categorienamen valideren
* Controleer of de kenmerktoewijzing correct is
* Testen met aankoopgegevens van monster

**Reis die niet** produceert:

* Bevestig alle vereiste configuratie volledig is
* Controleren op fouten op het tabblad Berichten
* Controleren of de inhoudskaart is geconfigureerd
* Logboeken van systeemfouten controleren

**gegevens van Prestaties tonen niet**:

* Toestaan dat gegevens worden doorgegeven (maximaal 24 uur)
* Controleren of gebeurtenissen correct worden bijgehouden
* Status van gegevensinvoer controleren
* Zorg ervoor dat de klant deelneemt

## Beta-feedback {#beta-feedback}

Tijdens de bètafase is uw feedback nuttig om ons te helpen bij het verbeteren van Loyalty Challenges. Deel uw ervaring, vragen en suggesties met uw Adobe-vertegenwoordiger of via de bèta-feedbackkanalen die tijdens het afspelen worden aangeboden.

## Verwante onderwerpen {#related-topics}

* [Stimuleer het publiek in Journey Optimizer](../audience/about-audiences.md)
* [Inhoudskaarten ontwerpen](../content-card/design-content-card.md)
* [In-app berichten maken](../in-app/create-in-app.md)
* [E-mails maken](../email/create-email.md)
* [Pushberichten maken](../push/create-push.md)
* [Reizen samenstellen](../building-journeys/journey-gs.md)
* [Uw reizen volgen](../building-journeys/report-journey.md)
* [ Experience Platform brondocumentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Bronconnectors configureren in Journey Optimizer](../start/get-started-sources.md)
