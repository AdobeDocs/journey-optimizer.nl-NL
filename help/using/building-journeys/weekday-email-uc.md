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
source-git-commit: 72f3396bc662e75efd0f82754bfa964baf51ab8e
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# E-mails alleen verzenden tijdens weekdagen {#send-emails-only-on-weekdays}

Dit gebruiksgeval toont aan hoe te om een reis in Adobe Journey Optimizer te vormen die e-mails slechts op weekdagen (Maandag door Vrijdag) verzendt. Voor profielen die de reis op weekends (Zaterdag of Zondag) ingaan, worden de e-mails automatisch een rij gevormd en verzonden op Maandag bij een gespecificeerde tijd. Dit zorgt voor een optimale betrokkenheid door berichten te leveren tijdens de werkweek.

## Hoofdlettergebruik

**de Uitdaging**: Zorgen dat de e-mails slechts op weekdagen worden verzonden, alhoewel de profielen de reis op weekends kunnen ingaan. Voor weekendvermeldingen moeten e-mails op maandag in een bepaalde periode in de wachtrij worden geplaatst en worden verzonden.

**de Oplossing**: Gebruik een voorwaardenactiviteit om de dag van de week te identificeren. Voor weekendvermeldingen wacht activiteiten met aangepaste formules de e-mail tot maandag. De weekdagingangen gaan direct aan de e-mail te werk verzendt stap.

Deze benadering toont u hoe te om een voorwaardenactiviteit te gebruiken om te controleren als de huidige dag Zaterdag of Zondag is, voert de activiteiten van de Wacht met douaneformules voor weekendingangen uit, rijen weekende-mails voor Maandag levering op een specifiek uur, en verzendt onmiddellijk e-mails voor weekdagingangen (maandag-vrijdag).

Deze benadering is ideaal voor zaken-aan-zaken (B2B) e-mailcampagnes, professionele nieuwsbrieven en mededelingen, zaken-gerelateerde aankondigingen, werk-gerelateerde productupdates, en om het even welke marketing campagne waar de levering in het weekend niet wordt gewenst.

➡️ bekijk het geleidelijke [ videoleerprogramma ](#how-to-video)

>[!NOTE]
>
>Om dit gebruiksgeval uit te voeren, hebt u een actieve instantie van Adobe Journey Optimizer met een gevormde [ oppervlakte van het e-mailkanaal ](../configuration/channel-surfaces.md), een [ publiek ](../audience/about-audiences.md) of [ gebeurtenis ](../event/about-events.md) nodig om de reis, en een basisbegrip van [ reisvoorwaarden ](condition-activity.md) en [ uitdrukkingen ](expression/expressionadvanced.md) in werking te stellen.





## Implementatiestappen

### Stap 1: Maak uw reis

1. Navigeer naar **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** in Adobe Journey Optimizer.

1. Klik op **[!UICONTROL Create Journey]** om een nieuwe rit te maken. [ leer meer over het creëren van reizen ](journey-gs.md)

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

1. Sleep een **[!UICONTROL Condition]** -activiteit naar het canvas na het ingangspunt. [ leer meer over de activiteiten van de Voorwaarde ](condition-activity.md)

1. Klik op de Condition-activiteit om het configuratievenster te openen.

1. Selecteer **[!UICONTROL Condition type]** in de sectie **[!UICONTROL Data Source Condition]** . [ leer meer over voorwaardetypes ](condition-activity.md#data_source_condition)

   ![ Vormend de voorwaarde van de Zaterdag in de uitdrukkingsredacteur ](assets/weekday-email-uc-condition-expression.png)


### Stap 3: Vorm de voorwaarde om Zaterdag te identificeren

Maak het eerste voorwaardepad om zaterdag-items te identificeren.

1. Klik op **[!UICONTROL Advanced mode]** om de expressie-editor te openen. [ leer meer over de uitdrukkingsredacteur ](expression/expressionadvanced.md)

1. Voer de volgende expressie in om te controleren of de huidige dag zaterdag is:

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Dit gebruikt de `dayOfWeek()` functie met `now()` om de huidige dag te krijgen. [ leer meer over datumfuncties ](functions/date-functions.md)


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


>[!NOTE]
>
>De functie `dayOfWeek()` retourneert een geheel getal dat de dag van de week vertegenwoordigt, waarbij 1 zondag is en 7 zaterdag. Dit volgt de ISO-8601-norm voor dagnummering.

### Stap 5: Configureer wachtactiviteiten voor weekendvermeldingen

Voor profielen die op Zaterdag of Zondag ingaan, gebruik Wacht activiteiten met douaneformules om e-mail tot Maandag op uw gewenste uur uit te stellen.


**voor de weg van de Zaterdag:**

1. Voeg een **[!UICONTROL Wait]** activiteit toe. [ Leer meer over de activiteiten van de Wacht ](wait-activity.md)

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

   ![ Reis met drie voorwaardenwegen - Zaterdag, Zondag, en Weekdagen ](assets/weekday-email-uc-paths.png)

   **Verklaring**: Deze formule berekent de wachttijd van zaterdag aan Maandag bij 9 AM. De waarde X=2 vertegenwoordigt 2 dagen voorwaarts (zaterdag + 2 dagen = Maandag). [ leer meer over datumfuncties ](functions/date-functions.md#nowWithDelta)

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

### Stap 6: Het pad voor de weekdag configureren

Voor de **Wekdagweg** (maandag-vrijdag):

1. Ga direct door om een **[!UICONTROL Email]** actieactiviteit toe te voegen. Er is geen wachtbewerking nodig voor weekdagvermeldingen. [ Leer meer over e-mailacties ](journeys-message.md)

1. Uw e-mailbericht configureren:
   * Selecteer of creeer uw [ e-mailinhoud ](../email/get-started-email-design.md)
   * Vorm de [ e-mailparameters ](../email/email-settings.md)
   * Opstelling [ verpersoonlijking ](../personalization/personalize.md) zoals nodig

1. Voeg een **[!UICONTROL End]** activiteit na e-mail toe.

### Stap 7: Paden voor weekend samenvoegen voor e-mail

Nadat de activiteiten van de Wacht op zowel de Zaterdag als de wegen van de Zondag, hen samenvoegen aan de zelfde E-mail actieactiviteit:

1. Voeg een handeling **[!UICONTROL Email]** toe vanaf de activiteit voor een zaterdagwachttijd.

1. Maak verbinding met dezelfde e-mailactie vanaf de activiteit Zondag wachten.

1. Het pad op de weekdag moet ook naar deze e-mailactie gaan.

### Stap 8: Test uw reis

Voordat u publiceert, test u de reislogica grondig in de testmodus van Adobe Journey Optimizer om te controleren of alles werkt zoals u had verwacht:

1. Klik op de knop **[!UICONTROL Test]** in de rechterbovenhoek.

1. De testmodus inschakelen. [ Leer hoe te om uw reis ](testing-the-journey.md) te testen

1. Creeer [ testprofielen ](../audience/creating-test-profiles.md) met gesimuleerde ingstijden op verschillende dagen van de week:
   * **ingang van de Zaterdag**: Verifieer het profiel volgt de weg van de Zaterdag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **de ingang van de Zondag**: Verifieer het profiel volgt de weg van de Zondag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **Maandag-Vrijdag ingangen**: Verifieer e-mails onmiddellijk zonder enige wachttijd worden verzonden

1. Controleer de reisvisualisatie om ervoor te zorgen dat de profielen de correcte voorwaardelijke wegen (Zaterdag, Zondag, of weekdag) volgen.

1. Controleer op eventuele fouten of waarschuwingen tijdens de rit. [ Leer over het oplossen van problemenreizen ](troubleshooting.md)

1. Verifieer dat de wachtwoorden de correcte duur voor uw gewenste Maandag leveringstijd berekenen.

>[!IMPORTANT]
>
>Test altijd uw reislogica grondig voordat u publiceert naar productie. Gebruik de Wijze van de Test om verschillende ingangsscenario&#39;s te simuleren en te bevestigen dat de weekendingangen correct voor Maandlevering een rij worden gevormd. [ Leer meer over reis het testen beste praktijken ](testing-the-journey.md)

### Stap 9: Uw reis publiceren

Zodra het testen is voltooid:

1. Klik op **[!UICONTROL Publish]** in de rechterbovenhoek.

1. Bevestig de publicatie. [ Leer meer over het publiceren reizen ](publish-journey.md)

1. Controleer de vervoersprestaties gebruikend [ Reis die ](report-journey.md) rapporteert en [ levende rapporten ](../reports/journey-live-report.md).

## Aanbevolen werkwijzen en overwegingen

### Workflow optimaliseren met verbeterde formules

Verbeter uw werkschema en behandel complexere bedrijfsvereisten:

* **Complexe bedrijfsuren**: Breid de formules uit om voor vakantie, tijdstreken, of specifieke bedrijfsuren voorbij de basisweekdagcontrole van rekenschap te geven.
* **de leveringstijden van de Douane**: Pas de uurparameter (H) in de Wacht formule aan om uw optimale verzendtijd aan te passen. Bijvoorbeeld, als 10 AM betere betrokkenheidspercentages toont, verander de formule om uur 10 te gebruiken.
* **veelvoudige steun van de tijdzone**: Creeer afzonderlijke reizen voor verschillende geografische gebieden om de levering van maandag in de lokale tijdzone van elke ontvanger te verzekeren.

### Tijdzonebeheer

De functie `now()` en de uitvoering van de reis gebruiken de tijdzone die op het reisniveau wordt gevormd. Houd rekening met de volgende belangrijke punten:

* **tijdzone van de Reis**: Zorg de streek van de reistijd aan uw behoeften door dit in de reiseigenschappen te vormen alvorens te publiceren. [ leer meer over timezone beheer ](timezone-management.md)
* **Globaal publiek**: Als uw publiek veelvoudige tijdzones overspant, gebeurt de dag-van-week controle in de gevormde tijdzone van de reis, niet de lokale tijdzone van de ontvanger.
* **Gelokaliseerde het plannen**: Voor tijdzone-specifieke levering, creeer afzonderlijke reizen voor verschillende gebieden of gebruik de tijdzonemontages in de Gelezen activiteit van het Publiek.

### Reisingang en -tijdstip

Vorm uw reistiming die op het ingangstype wordt gebaseerd:

* **las de reizen van het Publiek**: [ Plan het Gelezen Publiek ](read-audience.md#schedule) om in een tijd te teweegbrengen die voor uw publiek steek houdt. De vroege ochtenduitvoeringen (b.v., 6 :00 AM) zijn gemeenschappelijk voor bedrijfsmededelingen.
* **op gebeurtenis-gebaseerde reizen**: De voorwaarde zal onmiddellijk worden geëvalueerd wanneer de gebeurtenis wordt ontvangen. Profielen die in het weekend worden ingevoerd, wachten automatisch tot maandag. [ Leer meer over gebeurtenissen ](../event/about-events.md)
* **wacht onderbrekingsoverwegingen**: Verzeker uw [ montages van de reisonderbreking ](journey-properties.md#timeout) aanpassen de maximum wachttijdperiode (tot 2 dagen van Zaterdag aan Maandag).

### Testen is essentieel

Test altijd uw logica van de reis alvorens aan productie te publiceren:

* De Wijze van de Test van het gebruik **om verschillende ingangsscenario&#39;s te simuleren zonder echte e-mails te verzenden**
* Alle drie paden testen: zaterdag-, zondag- en weekdagvermeldingen
* Controleer of de berekeningen voor tijdsduur wachten correct zijn
* De levering van maandag bevestigen vindt plaats op het opgegeven uur
* Reisvisualisatie controleren om een juiste routeroutering te garanderen

[Meer informatie over het testen van reizen](testing-the-journey.md)

### Herkomst en frequentie

Voor terugkerende campagnes, beheer zorgvuldig opnieuw betreden profiel:

* **vorm re-ingang**: Opstelling de **[!UICONTROL Re-entrance]** montages geschikt. [ leer meer over re-entry montages ](entry-management.md)
* **Consistent gedrag**: Als de profielen de reis kunnen opnieuw ingaan, zullen zij aan de dag-van-week controle telkens onderworpen zijn, die weekendingangen verzekeren altijd voor Maandag een rij worden gevormd.
* **het in kaart brengen van de Frequentie**: Overweeg toevoegend [ frequentie die regels ](../conflict-prioritization/journey-capping.md) begrenzen om over-overseinen te vermijden als de profielen vaak kunnen opnieuw binnengaan.

## Geavanceerde variaties

### Specifieke doeldag

Alleen e-mailberichten verzenden op specifieke dagen (bijvoorbeeld dinsdag en donderdag):

1. **wijzig de voorwaarde** om specifieke dagen te controleren:

   ```javascript
   dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
   ```

2. **voeg wachtactiviteiten** voor alle andere dagen toe die het aantal dagen tot volgende Dinsdag of Donderdag berekenen.

### Verschillende verzendtijden voor verschillende dagen

Maak meerdere paden met verschillende wachtformules voor flexibele planning:

* **Zaterdag → Woensdag levering**: Gebruik `nowWithDelta(4, "days")`
* **Zondag → Dinsdag levering**: Gebruik `nowWithDelta(2, "days")`

Op deze manier kunt u leveringsdagen aanpassen op basis van uw zakelijke vereisten.

### Levering van kantooruren

Zo zorgt u voor levering tijdens kantooruren:

1. **pas de uurparameter** in uw Wacht formule aan. Bijvoorbeeld, voor levering bij 2 PM in plaats van 9 AM:

   ```javascript
   setHours(nowWithDelta(1, "days"), 14)
   ```

2. **voeg een tijdcontrole** (facultatief) toe: voeg een tweede voorwaarde na de Wacht toe om de huidige tijd binnen bedrijfsuren alvorens te verifiëren is.

### Uitsluiting vakantie

U kunt feestdagen uitsluiten van het verzenden van e-mail als volgt:

1. **voeg een voorwaardenweg** toe om specifieke vakantiedata te controleren:

   ```javascript
   toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
   ```

2. **voeg een Wacht activiteit** toe als de voorwaarde een vakantie aanpast, aan vertraging tot de volgende werkdag.

[Meer informatie over functies voor datumvergelijking](functions/date-functions.md)

## Verwante onderwerpen

* [ Ongeveer de activiteiten van de Voorwaarde ](condition-activity.md) - leer hoe te om verschillende wegen in uw reis tot stand te brengen
* [ de voorwaarden van het Gebruik in een reis ](conditions.md) - Gedetailleerde gids op reisvoorwaarden
* [ wacht activiteit ](wait-activity.md) - vorm wachttijdsduur en formules
* [ functies van de Datum ](functions/date-functions.md) - Volledige verwijzing voor datum en tijdfuncties
* [ de redacteur van de Uitdrukking ](expression/expressionadvanced.md) - bouw complexe uitdrukkingen
* [ Test uw reis ](testing-the-journey.md) - bevestigt reislogica alvorens te publiceren
* [ het beheer van de tijdzone ](timezone-management.md) - handvat verschillende tijdstreken in reizen
* [ de beste praktijken van de Reis ](journey-gs.md#best-practices) - Aanbevolen benaderingen voor reisontwerp

## Hoe kan ik-video

Met Adobe Journey Optimizer kun je e-mails alleen op weekdagen verzenden. Deze video toont de geleidelijke implementatie van voorwaardenactiviteiten en Wacht formules aan rij weekendingangen voor Maandlevering.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Aanvullende bronnen

* [ de redacteursdocumentatie van de Uitdrukking ](expression/expressionadvanced.md) - bouw en bevestig reisuitdrukkingen
* [ gids van de ontwerper van de Reis ](using-the-journey-designer.md) - Meester het wegcanvas
* [ overzicht van de de gebruiksgevallen van de Reis ](jo-use-cases.md) - Onderzoek meer reispatronen en voorbeelden
* [ Communautaire blogpost: Hoe te om E-mail slechts op Weekdagen ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} te verzenden - Oorspronkelijke blogpost met gedetailleerde voorbeelden

