---
solution: Journey Optimizer
product: journey optimizer
title: E-mails alleen verzenden tijdens weekdagen
description: Leer hoe u een reis configureert om e-mailberichten alleen op weekdagen in Adobe Journey Optimizer te verzenden
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: reis, gebruiksgeval, weekdagen, voorwaarde, e-mail, planning
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: e9e215bfb2de955b27e6bc2395df4975d86b17f0
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# E-mails alleen verzenden tijdens weekdagen {#send-emails-only-on-weekdays}

Dit gebruiksgeval toont aan hoe te om een reis in Adobe Journey Optimizer te vormen die e-mails slechts op weekdagen (Maandag door Vrijdag) verzendt. Voor profielen die de reis op weekends (Zaterdag of Zondag) ingaan, worden de e-mails automatisch een rij gevormd en verzonden op Maandag bij een gespecificeerde tijd. Dit zorgt voor een optimale betrokkenheid door berichten te leveren tijdens de werkweek.

## Hoofdlettergebruik

**de Uitdaging**: Zorgen dat de e-mails slechts op weekdagen worden verzonden, alhoewel de profielen de reis op weekends kunnen ingaan. Voor weekendvermeldingen moeten e-mails op maandag in een bepaalde periode in de wachtrij worden geplaatst en worden verzonden.

**de Oplossing**: Gebruik een voorwaardenactiviteit om de dag van de week te identificeren. Voor weekendvermeldingen wacht activiteiten met aangepaste formules de e-mail tot maandag. De weekdagingangen gaan direct aan de e-mail te werk verzendt stap.

Deze aanpak laat u zien hoe u:

* Gebruik een voorwaardenactiviteit om te controleren of de huidige dag zaterdag of zondag is
* Voer Wacht activiteiten met douaneformules voor weekendingangen uit
* E-mailberichten tijdens het weekend van de wachtrij voor levering op maandag op een bepaald uur
* E-mails direct verzenden voor weekdagvermeldingen (maandag-vrijdag)

Deze benadering is ideaal voor:

* E-mailcampagnes van business-to-business (B2B)
* Professionele nieuwsbrieven en communicatie
* Zakelijke aankondigingen
* Productupdates met betrekking tot werk
* Een marketingcampagne waarbij levering in het weekend niet gewenst is

Bekijk het geleidelijke [&#x200B; videoleerprogramma &#x200B;](#how-to-video) bij de bodem van deze pagina om de volledige implementatie te zien.

## Vereisten

Voor het implementeren van dit gebruiksgeval hebt u het volgende nodig:

* Een actieve Adobe Journey Optimizer-instantie
* Een gevormd [&#x200B; oppervlakte van het e-mailkanaal &#x200B;](../configuration/channel-surfaces.md)
* Een [&#x200B; publiek &#x200B;](../audience/about-audiences.md) of [&#x200B; gebeurtenis &#x200B;](../event/about-events.md) om de reis teweegte brengen
* Het fundamentele begrip van [&#x200B; reisvoorwaarden &#x200B;](condition-activity.md) en [&#x200B; uitdrukkingen &#x200B;](expression/expressionadvanced.md)

## Implementatiestappen

### Stap 1: Maak uw reis

1. Navigeer naar **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** in Adobe Journey Optimizer.

1. Klik op **[!UICONTROL Create Journey]** om een nieuwe rit te maken. [&#x200B; leer meer over het creëren van reizen &#x200B;](journey-gs.md)

1. Vorm de reis eigenschappen:
   * **Naam**: De Campagne van de E-mail van de weekdag
   * **Beschrijving**: verzendt e-mails slechts op weekdagen (maandag-vrijdag)
   * Stel de juiste naamruimte in voor uw gebruik

[Meer informatie over eigenschappen van reizen](journey-properties.md)

1. Kies het toegangspunt voor uw reis:
   * **[las Publiek](read-audience.md)**: Voor partijcampagnes richtend een specifiek publiek
   * **[Gebeurtenis](../event/about-events.md)**: Voor in real time teweeggebrachte reizen die op klantengedrag worden gebaseerd

### Stap 2: Voeg een Condition-activiteit toe om de dag van de week te controleren

Vlak na het begin van de rit voegt u een **[!UICONTROL Condition]** -activiteit toe om te controleren of de huidige dag zaterdag of zondag is. Hierdoor wordt de workflow dienovereenkomstig vertakt.

1. Sleep een **[!UICONTROL Condition]** -activiteit naar het canvas na het ingangspunt. [&#x200B; leer meer over de activiteiten van de Voorwaarde &#x200B;](condition-activity.md)

1. Klik op de Condition-activiteit om het configuratievenster te openen.

1. Selecteer **[!UICONTROL Condition type]** in de sectie **[!UICONTROL Data Source Condition]** . [&#x200B; leer meer over voorwaardetypes &#x200B;](condition-activity.md#data_source_condition)

### Stap 3: Vorm de voorwaarde om Zaterdag te identificeren

Maak het eerste voorwaardepad om zaterdag-items te identificeren.

1. Klik op **[!UICONTROL Advanced mode]** om de expressie-editor te openen. [&#x200B; leer meer over de uitdrukkingsredacteur &#x200B;](expression/expressionadvanced.md)

1. Voer de volgende expressie in om te controleren of de huidige dag zaterdag is:

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Dit gebruikt de `dayOfWeek()` functie met `now()` om de huidige dag te krijgen. [&#x200B; leer meer over datumfuncties &#x200B;](functions/date-functions.md)

   ![&#x200B; Vormend de voorwaarde van de Zaterdag in de uitdrukkingsredacteur &#x200B;](assets/weekday-email-uc-condition-expression.png)

1. Klik op **[!UICONTROL Ok]** om de voorwaarde op te slaan.

1. Label dit pad als &quot;zaterdag&quot;.

### Stap 4: Een tweede voorwaardenpad toevoegen voor zondag

1. Klik in de Condition-activiteit op **[!UICONTROL Add a path]** om een tweede voorwaarde te maken.

1. Voer in de expressieeditor voor het tweede pad het volgende in:

   ```javascript
   dayOfWeek(now()) == 1
   ```

   Dit controleert of de huidige dag zondag is.

1. Label dit pad als &quot;zondag&quot;.

1. Schakel **[!UICONTROL Show path for other cases than the one(s) above]** in om een pad te maken voor weekdagvermeldingen (maandag t/m vrijdag).

   **Dag van weekwaarden:**
   * 1 = zondag
   * 2 = maandag
   * 3 = dinsdag
   * 4 = woensdag
   * 5 = donderdag
   * 6 = vrijdag
   * 7 = zaterdag

>[!NOTE]
>
>De functie `dayOfWeek()` retourneert een geheel getal dat de dag van de week vertegenwoordigt, waarbij 1 zondag is en 7 zaterdag. Dit volgt de ISO-8601-norm voor dagnummering.

### Stap 4: Configureer wachtactiviteiten voor weekendvermeldingen

Voor profielen die op Zaterdag of Zondag ingaan, gebruik Wacht activiteiten met douaneformules om e-mail tot Maandag op uw gewenste uur uit te stellen.

![&#x200B; Reis met drie voorwaardenwegen - Zaterdag, Zondag, en Weekdagen &#x200B;](assets/weekday-email-uc-paths.png)

**voor de weg van de Zaterdag:**

1. Voeg een **[!UICONTROL Wait]** activiteit toe. [&#x200B; Leer meer over de activiteiten van de Wacht &#x200B;](wait-activity.md)

1. Selecteer **[!UICONTROL Duration]** als type wait.

1. Klik op **[!UICONTROL Advanced mode]** om een aangepaste formule in te voeren.

1. Voer de volgende formule in om tot maandag om 9.00 uur te wachten:

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   Of gebruik deze alternatieve formule:

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   **Verklaring**: Deze formule berekent de wachttijd van zaterdag aan Maandag bij 9 AM. De waarde X=2 vertegenwoordigt 2 dagen voorwaarts (zaterdag + 2 dagen = Maandag). [&#x200B; leer meer over datumfuncties &#x200B;](functions/date-functions.md#nowWithDelta)

**voor de weg van de Zondag:**

1. Voeg een **[!UICONTROL Wait]** activiteit toe.

1. Selecteer **[!UICONTROL Duration]** als type wait.

1. Klik op **[!UICONTROL Advanced mode]** om een aangepaste formule in te voeren.

1. Voer de volgende formule in om tot maandag om 9.00 uur te wachten:

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **Verklaring**: Deze formule wacht 1 dag (zondag + 1 dag = Maandag) en plaatst de tijd aan 9 AM. De waarde X=1 vertegenwoordigt 1 dag voorwaarts, en H=9 vertegenwoordigt 9 AM.

>[!TIP]
>
>U kunt de parameter uur (H) aanpassen voor elk moment dat u de e-mail op maandag wilt verzenden. Wijzig bijvoorbeeld 9 in 10 voor 10.00 uur of 14 voor 2.00 uur.

### Stap 5: Vorm de weekdagweg

Voor de **Wekdagweg** (maandag-vrijdag):

1. Ga direct door om een **[!UICONTROL Email]** actieactiviteit toe te voegen. Er is geen wachtbewerking nodig voor weekdagvermeldingen. [&#x200B; Leer meer over e-mailacties &#x200B;](journeys-message.md)

1. Uw e-mailbericht configureren:
   * Selecteer of creeer uw [&#x200B; e-mailinhoud &#x200B;](../email/get-started-email-design.md)
   * Vorm de [&#x200B; e-mailparameters &#x200B;](../email/email-settings.md)
   * Opstelling [&#x200B; verpersoonlijking &#x200B;](../personalization/personalize.md) zoals nodig

1. Voeg een **[!UICONTROL End]** activiteit na e-mail toe.

### Stap 6: Paden voor weekend samenvoegen voor e-mail

Nadat de activiteiten van de Wacht op zowel de Zaterdag als de wegen van de Zondag, hen samenvoegen aan de zelfde E-mail actieactiviteit:

1. Voeg een handeling **[!UICONTROL Email]** toe vanaf de activiteit voor een zaterdagwachttijd.

1. Maak verbinding met dezelfde e-mailactie vanaf de activiteit Zondag wachten.

1. Het pad op de weekdag moet ook naar deze e-mailactie gaan.


### Stap 7: Test uw reis

Voordat u publiceert, test u de reislogica grondig in de testmodus van Adobe Journey Optimizer om te controleren of alles werkt zoals u had verwacht:

1. Klik op de knop **[!UICONTROL Test]** in de rechterbovenhoek.

1. De testmodus inschakelen. [&#x200B; Leer hoe te om uw reis &#x200B;](testing-the-journey.md) te testen

1. Creeer [&#x200B; testprofielen &#x200B;](../audience/creating-test-profiles.md) met gesimuleerde ingstijden op verschillende dagen van de week:
   * **ingang van de Zaterdag**: Verifieer het profiel volgt de weg van de Zaterdag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **de ingang van de Zondag**: Verifieer het profiel volgt de weg van de Zondag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **Maandag-Vrijdag ingangen**: Verifieer e-mails onmiddellijk zonder enige wachttijd worden verzonden

1. Controleer de reisvisualisatie om ervoor te zorgen dat de profielen de correcte voorwaardelijke wegen (Zaterdag, Zondag, of weekdag) volgen.

1. Controleer op eventuele fouten of waarschuwingen tijdens de rit. [&#x200B; Leer over het oplossen van problemenreizen &#x200B;](troubleshooting.md)

1. Verifieer dat de wachtwoorden de correcte duur voor uw gewenste Maandag leveringstijd berekenen.

>[!IMPORTANT]
>
>Test altijd uw reislogica grondig voordat u publiceert naar productie. Gebruik de Wijze van de Test om verschillende ingangsscenario&#39;s te simuleren en te bevestigen dat de weekendingangen correct voor Maandlevering een rij worden gevormd. [&#x200B; Leer meer over reis het testen beste praktijken &#x200B;](testing-the-journey.md)

### Stap 8: Uw reis publiceren

Zodra het testen is voltooid:

1. Klik op **[!UICONTROL Publish]** in de rechterbovenhoek.

1. Bevestig de publicatie. [&#x200B; Leer meer over het publiceren reizen &#x200B;](publish-journey.md)

1. Controleer de vervoersprestaties gebruikend [&#x200B; Reis die &#x200B;](report-journey.md) rapporteert en [&#x200B; levende rapporten &#x200B;](../reports/journey-live-report.md).

## Aanbevolen werkwijzen en overwegingen

### Workflow optimaliseren met verbeterde formules

Om uw werkschema te verbeteren en complexere bedrijfsvereisten te behandelen:

* **Complexe bedrijfsuren**: Breid de formules uit om voor vakantie, tijdstreken, of specifieke bedrijfsuren voorbij de basisweekdagcontrole van rekenschap te geven.

* **de leveringstijden van de Douane**: Pas de uurparameter (H) in de Wacht formule aan om uw optimale verzendtijd aan te passen. Bijvoorbeeld, als 10 AM betere betrokkenheidspercentages toont, verander de formule om uur 10 te gebruiken.

* **de veelvoudige steun van de tijdzone**: Overweeg het creëren van afzonderlijke reizen voor verschillende geografische gebieden om de levering van maandag in de lokale tijdzone van elke ontvanger te verzekeren.

### Tijdzonebeheer

De functie `now()` en de uitvoering van de reis gebruiken de tijdzone die op het reisniveau wordt gevormd. Overweeg het volgende:

* **tijdzone van de Reis**: Zorg de streek van de reistijd past uw behoeften aan. Vorm dit in de reis eigenschappen alvorens te publiceren. [&#x200B; leer meer over timezone beheer &#x200B;](timezone-management.md).

* **Globaal publiek**: Als uw publiek veelvoudige tijdzones overspant, gebeurt de dag-van-week controle in de gevormde tijdzone van de reis, niet de lokale tijdzone van de ontvanger.

* **Gelokaliseerde het plannen**: Voor tijdzone-specifieke levering, creeer afzonderlijke reizen voor verschillende gebieden of gebruik de tijdzonemontages in de Gelezen activiteit van het Publiek.

### Reisingang en -tijdstip

* **las de reizen van het Publiek**: Voor partijreizen, [&#x200B; plant het Gelezen Publiek &#x200B;](read-audience.md#schedule) om in een tijd te teweegbrengen die voor uw publiek steek houdt. De vroege ochtenduitvoeringen (b.v., 6 :00 AM) zijn gemeenschappelijk voor bedrijfsmededelingen.

* **op gebeurtenis-gebaseerde reizen**: De voorwaarde zal onmiddellijk worden geëvalueerd wanneer de gebeurtenis wordt ontvangen. Profielen die in het weekend worden ingevoerd, wachten automatisch tot maandag. [&#x200B; Leer meer over gebeurtenissen &#x200B;](../event/about-events.md)

* **wacht onderbrekingsoverwegingen**: Verzeker uw [&#x200B; montages van de reisonderbreking &#x200B;](journey-properties.md#timeout) aanpassen de maximum wachttijdperiode (tot 2 dagen van Zaterdag aan Maandag).

### Testen is essentieel

Zoals benadrukt in de implementatiegids, test altijd uw reislogica om alles te bevestigen werkt zoals verwacht:

* De Wijze van de Test van het gebruik **om verschillende ingangsscenario&#39;s te simuleren zonder echte e-mails te verzenden**
* Alle drie paden testen: zaterdag-, zondag- en weekdagvermeldingen
* Controleer of de berekeningen voor tijdsduur wachten correct zijn
* De levering van maandag bevestigen vindt plaats op het opgegeven uur
* Reisvisualisatie controleren om een juiste routeroutering te garanderen

### Herkomst en frequentie

* Configureer voor terugkerende campagnes de **[!UICONTROL Re-entrance]** -instellingen op de juiste wijze. [&#x200B; leer meer over re-entry montages &#x200B;](entry-management.md)

* Als de profielen de reis kunnen opnieuw ingaan, zullen zij aan de dag-van-week controle elke keer onderworpen zijn, die ervoor zorgen de weekendingangen altijd voor Maandag in de rij worden geplaatst.

* Overweeg het toevoegen van [&#x200B; frequentie die regels &#x200B;](../conflict-prioritization/journey-capping.md) begrenzen om over-overseinen te vermijden als de profielen vaak kunnen opnieuw binnengaan.

## Geavanceerde variaties

### Specifieke doeldag

Wijzig de voorwaarde als u e-mailberichten alleen op specifieke dagen wilt verzenden (bijvoorbeeld dinsdag en donderdag):

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Voor alle andere dagen, voeg een activiteit van de Wacht toe die het aantal dagen tot volgende Dinsdag of Donderdag berekent.

### Verschillende verzendtijden voor verschillende dagen

U kunt meerdere paden maken met verschillende wachtformules voor verschillende gedragingen in het weekend:

* **Zaterdag → Woensdag levering**: Gebruik `nowWithDelta(4, "days")`
* **Zondag → Dinsdag levering**: Gebruik `nowWithDelta(2, "days")`

Dit staat meer flexibiliteit in uw verzendend programma toe.

### Levering van kantooruren

Om levering tijdens bedrijfsuren te verzekeren, pas de uurparameter in uw Wacht formule aan. Bijvoorbeeld, voor levering bij 2 PM in plaats van 9 AM:

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

U kunt ook een tweede voorwaarde toevoegen na de Wacht om te controleren of de huidige tijd binnen kantooruren alvorens te verzenden is.

### Uitsluiting vakantie

Als u feestdagen wilt uitsluiten, voegt u een extra voorwaardepad toe dat controleert op specifieke datums:

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Als de voorwaarde een vakantie aanpast, voeg een Wacht activiteit toe om tot de volgende werkdag uit te stellen. [&#x200B; leer meer over de functies van de datumvergelijking &#x200B;](functions/date-functions.md)

## Verwante onderwerpen

* [&#x200B; Ongeveer de activiteiten van de Voorwaarde &#x200B;](condition-activity.md) - leer hoe te om verschillende wegen in uw reis tot stand te brengen
* [&#x200B; de voorwaarden van het Gebruik in een reis &#x200B;](conditions.md) - Gedetailleerde gids op reisvoorwaarden
* [&#x200B; wacht activiteit &#x200B;](wait-activity.md) - vorm wachttijdsduur en formules
* [&#x200B; functies van de Datum &#x200B;](functions/date-functions.md) - Volledige verwijzing voor datum en tijdfuncties
* [&#x200B; de redacteur van de Uitdrukking &#x200B;](expression/expressionadvanced.md) - bouw complexe uitdrukkingen
* [&#x200B; Test uw reis &#x200B;](testing-the-journey.md) - bevestigt reislogica alvorens te publiceren
* [&#x200B; het beheer van de tijdzone &#x200B;](timezone-management.md) - handvat verschillende tijdstreken in reizen
* [&#x200B; de beste praktijken van de Reis &#x200B;](journey-gs.md#best-practices) - Aanbevolen benaderingen voor reisontwerp

## Hoe kan ik-video

Met Adobe Journey Optimizer kun je e-mails alleen op weekdagen verzenden. Deze video toont de geleidelijke implementatie van voorwaardenactiviteiten en Wacht formules aan rij weekendingangen voor Maandlevering.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Aanvullende bronnen

* [&#x200B; de redacteursdocumentatie van de Uitdrukking &#x200B;](expression/expressionadvanced.md) - bouw en bevestig reisuitdrukkingen
* [&#x200B; gids van de ontwerper van de Reis &#x200B;](using-the-journey-designer.md) - Meester het wegcanvas
* [&#x200B; overzicht van de de gebruiksgevallen van de Reis &#x200B;](jo-use-cases.md) - Onderzoek meer reispatronen en voorbeelden
* [&#x200B; Communautaire blogpost: Hoe te om E-mail slechts op Weekdagen &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} te verzenden - Oorspronkelijke blogpost met gedetailleerde voorbeelden

