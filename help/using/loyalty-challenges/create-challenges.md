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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 0%

---


# Uitdagingen maken {#create-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* [&#x200B; de Uitdagingen van de Loyalty van de Toegang &#x200B;](access-loyalty-challenges.md) - Inventaris en het filtreren
* **creeer uitdagingen** {2 }︎ ◀ u hier **bent - bouw en vorm uitdagingen**
* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Een loyaliteitsprobleem maken"
>abstract="Creeer een loyaliteitsuitdaging om de betrokkenheidsaanbieding te bepalen, inhoudskaarten voor levering te vormen, taken toe te voegen, beloningen op te zetten, en naar keuze overseinen over kanalen te vormen."

## Voordat u begint {#before-you-start}

Voordat u een uitdaging maakt, moet u ervoor zorgen dat:

* Gevormde en bevestigde gegevensopname door bronschakelaars
* Vereiste soorten publiek maken in Experience Platform
* Inhoud (afbeeldingen, tekst, enzovoort) voorbereiden voor uw uitdaging
* De taken en beloningen gedefinieerd die u wilt aanbieden

## Een uitdaging maken {#create-a-challenge}

Voor gedetailleerde stappen voor het creëren van uitdagingen zoals:
* Configuratie van uitdagingseigenschappen
* Uitdagingstypen (Standaard, Streak, Opeenvolgend)
* Selectie publiek
* Datumconfiguratie

## Taken toevoegen {#add-tasks}

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

## Inhoudskaarten configureren {#configure-content-cards}

Voor gedetailleerde stappen bij het configureren van inhoudskaarten, waaronder:
* Instellen van inhoudskaart
* Ontwerp en personalisatie
* Voorvertonen en testen

## Berichten configureren {#configure-messaging}

Voor gedetailleerde stappen bij het vormen van multi-kanaaloverseinen die omvatten:
* Berichtkanalen (in-app, e-mail, push)
* Berichtfasen (opstarten, bezig, voltooid)
* Berichttiming en -triggers

## Reviseren en publiceren {#review-and-publish}

Voordat u uw uitdaging publiceert:

1. **Overzicht alle componenten**: De eigenschappen van de uitdaging, taken, beloningen, inhoud, overseinen
2. **Test de ervaring**: Gebruik testprofielen om inhoud en taaktrekkers te bevestigen
3. **publiceer**: Maak de uitdaging actief voor uw doelpubliek

De automatisch gegenereerde reis wordt geactiveerd op de opgegeven startdatum.

## Volgende stappen {#next-steps}

* [&#x200B; beheert uitdagingen &#x200B;](manage-challenges.md) - Leer hoe te, uitdagingen uit te geven te controleren en te optimaliseren
* [&#x200B; Begrijp Loyalty Uitdagingen &#x200B;](get-started.md) - de eigenschappen en de mogelijkheden van het overzicht
