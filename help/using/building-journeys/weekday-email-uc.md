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
source-git-commit: f8b594a14a1f89f77aa560a4de2b99189046af4f
workflow-type: tm+mt
source-wordcount: '1807'
ht-degree: 0%

---

# E-mails alleen verzenden tijdens weekdagen {#send-emails-only-on-weekdays}

Dit gebruiksgeval toont aan hoe te om een reis in Adobe Journey Optimizer te vormen die e-mails slechts op weekdagen (Maandag door Vrijdag) verzendt. Voor profielen die de reis op weekends (Zaterdag of Zondag) ingaan, worden de e-mails automatisch een rij gevormd en verzonden op Maandag bij een gespecificeerde tijd. Dit zorgt voor een optimale betrokkenheid door berichten te leveren tijdens de werkweek.

## Hoofdlettergebruik

**de Uitdaging**: Zorgen dat de e-mails slechts op weekdagen worden verzonden, alhoewel de profielen de reis op weekends kunnen ingaan. Voor weekendvermeldingen moeten e-mails op maandag in een bepaalde periode in de wachtrij worden geplaatst en worden verzonden.

**de Oplossing**: Gebruik een voorwaardenactiviteit om de dag van de week te identificeren. Voor weekendvermeldingen wacht activiteiten met aangepaste formules de e-mail tot maandag. De weekdagingangen gaan direct aan de e-mail te werk verzendt stap.

Deze benadering toont u hoe te om een voorwaardenactiviteit te gebruiken om te controleren als de huidige dag Zaterdag of Zondag is, voert de activiteiten van de Wacht met douaneformules voor weekendingangen uit, rijen weekende-mails voor Maandag levering op een specifiek uur, en verzendt onmiddellijk e-mails voor weekdagingangen (maandag-vrijdag).

Deze benadering is ideaal voor zaken-aan-zaken (B2B) e-mailcampagnes, professionele nieuwsbrieven en mededelingen, zaken-gerelateerde aankondigingen, werk-gerelateerde productupdates, en om het even welke marketing campagne waar de levering in het weekend niet wordt gewenst.

Bekijk het geleidelijke [ videoleerprogramma ](#how-to-video) bij de bodem van deze pagina om de volledige implementatie te zien.

## Vereisten

Om dit gebruiksgeval uit te voeren, hebt u een actieve instantie van Adobe Journey Optimizer met een gevormde [ oppervlakte van het e-mailkanaal ](../configuration/channel-surfaces.md), een [ publiek ](../audience/about-audiences.md) of [ gebeurtenis ](../event/about-events.md) nodig om de reis, en een basisbegrip van [ reisvoorwaarden ](condition-activity.md) en [ uitdrukkingen ](expression/expressionadvanced.md) in werking te stellen.

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

+++**optimaliseer werkschema met verbeterde formules**

Om uw werkschema te verbeteren en complexere bedrijfsvereisten te behandelen, kunt u de formules tot vakantie, tijdzones, of specifieke kantooruren na de basisweekdagcontrole uitbreiden. Pas de uurparameter (H) in de Wacht formule aan om uw optimaal te passen verzendt tijd-voor voorbeeld, als 10 AM betere betrokkenheidstarieven toont, verander de formule om uur 10 te gebruiken. Als u meerdere tijdzones wilt ondersteunen, kunt u overwegen aparte reizen voor verschillende geografische regio&#39;s te maken om ervoor te zorgen dat de levering op maandag plaatsvindt in de lokale tijdzone van elke ontvanger.

+++

+++**Tijdzonebeheer**

De functie `now()` en de uitvoering van de reis gebruiken de tijdzone die op het reisniveau wordt gevormd. Verzeker de streek van de reistijd uw behoeften door dit in de reiseigenschappen te vormen alvorens te publiceren ([ leer meer over timezone beheer ](timezone-management.md)). Als uw publiek veelvoudige tijdzones overspant, merk op dat de dag-van-week controle in de gevormde tijdzone van de reis, niet de lokale tijdzone van de ontvanger gebeurt. Voor tijdzone-specifieke levering, creeer afzonderlijke reizen voor verschillende gebieden of gebruik de tijdzonemontages in de Gelezen activiteit van de Publiek.

+++

+++**ingang en timing van de Reis**

Voor partijreizen, [ programma het Gelezen publiek ](read-audience.md#schedule) om in een tijd teweeg te brengen die voor uw publiek-vroege ochtenduitvoeringen (b.v., 6 :00 AM) geschikt is gemeenschappelijk voor bedrijfsmededelingen. Voor op gebeurtenis-gebaseerde reizen, zal de voorwaarde onmiddellijk worden geëvalueerd wanneer de gebeurtenis wordt ontvangen, en de profielen die op weekends ingaan zullen automatisch tot Maandag wachten ([ leren meer over gebeurtenissen ](../event/about-events.md)). Verzeker uw [ montages van de reisonderbreking ](journey-properties.md#timeout) aanpassen het maximum wachttijdperiode (tot 2 dagen van Zaterdag aan Maandag).

+++

+++**het Testen is essentieel**

Zoals benadrukt in de implementatiegids, test altijd uw reislogica om alles te bevestigen werkt zoals verwacht. De Wijze van de Test van het gebruik **om verschillende ingangsscenario&#39;s te simuleren zonder echte e-mails te verzenden.** Test alle drie wegen (de ingangen van de Zaterdag, de ingangen van de Zondag, en de ingangen van de weekdag), verifieer de berekeningen van de Wacht duur correct zijn, bevestig de levering van maandag op het gespecificeerde uur, en controleer reis visualisatie om juiste weg te verzekeren die verplettert.

+++

+++**Wedertoegang en frequentie**

Voor terugkomende campagnes, vorm de **[!UICONTROL Re-entrance]** montages geschikt ([ Leer meer over re-entry montages ](entry-management.md)). Als de profielen de reis kunnen opnieuw ingaan, zullen zij aan de dag-van-week controle elke keer onderworpen zijn, die ervoor zorgen de weekendingangen altijd voor Maandag in de rij worden geplaatst. Overweeg het toevoegen van [ frequentie die regels ](../conflict-prioritization/journey-capping.md) begrenzen om over-overseinen te vermijden als de profielen vaak kunnen opnieuw binnengaan.

+++

## Geavanceerde variaties

+++**Specifieke dag het richten**

Wijzig de voorwaarde als u e-mailberichten alleen op specifieke dagen wilt verzenden (bijvoorbeeld dinsdag en donderdag):

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Voor alle andere dagen, voeg een activiteit van de Wacht toe die het aantal dagen tot volgende Dinsdag of Donderdag berekent.

+++

+++**Verschil verzendt tijden voor verschillende dagen**

U kunt meerdere paden maken met verschillende wachtformules voor verschillende gedragingen in het weekend. Gebruik bijvoorbeeld `nowWithDelta(4, "days")` voor levering op zaterdag en woensdag of `nowWithDelta(2, "days")` voor levering op zondag en dinsdag. Dit staat meer flexibiliteit in uw verzendend programma toe.

+++

+++**levering Bedrijfsuren**

Om levering tijdens bedrijfsuren te verzekeren, pas de uurparameter in uw Wacht formule aan. Bijvoorbeeld, voor levering bij 2 PM in plaats van 9 AM:

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

U kunt ook een tweede voorwaarde toevoegen na de Wacht om te controleren of de huidige tijd binnen kantooruren alvorens te verzenden is.

+++

+++**Uitsluiting van de Vakantie**

Als u feestdagen wilt uitsluiten, voegt u een extra voorwaardepad toe dat controleert op specifieke datums:

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Als de voorwaarde een vakantie aanpast, voeg een Wacht activiteit toe om tot de volgende werkdag uit te stellen. [ leer meer over de functies van de datumvergelijking ](functions/date-functions.md)

+++

## Verwante onderwerpen

| Onderwerp | Beschrijving |
|-------|-------------|
| [ Ongeveer de activiteiten van de Voorwaarde ](condition-activity.md) | Leer hoe u verschillende paden kunt maken voor uw reis |
| [ de voorwaarden van het Gebruik in een reis ](conditions.md) | Gedetailleerde gids over reisomstandigheden |
| [Wachtactiviteit](wait-activity.md) | De wachttijden en formules configureren |
| [ functies van de Datum ](functions/date-functions.md) | Volledige referentie voor datum- en tijdfuncties |
| [ de redacteur van de Uitdrukking ](expression/expressionadvanced.md) | Complexe expressies maken |
| [ Test uw reis ](testing-the-journey.md) | Reislogica valideren vóór publicatie |
| [Tijdzonebeheer](timezone-management.md) | Verschillende tijdzones tijdens reizen afhandelen |
| [ de beste praktijken van de Reis ](journey-gs.md#best-practices) | Aanbevolen benaderingen voor reisontwerp |

## Hoe kan ik-video

Met Adobe Journey Optimizer kun je e-mails alleen op weekdagen verzenden. Deze video toont de geleidelijke implementatie van voorwaardenactiviteiten en Wacht formules aan rij weekendingangen voor Maandlevering.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Aanvullende bronnen

| Bron | Beschrijving |
|----------|-------------|
| [ de redacteursdocumentatie van de Uitdrukking ](expression/expressionadvanced.md) | Trajectexpressies maken en valideren |
| [ gids van de ontwerper van de Reis ](using-the-journey-designer.md) | Het canvas van de reis besturen |
| [ overzicht van de de gebruikscase van de Reis ](jo-use-cases.md) | Meer reispatronen en voorbeelden bekijken |
| [ Communautaire blogpost: Hoe te om E-mail slechts op Weekdagen te verzenden ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} | Oorspronkelijk blogbericht met gedetailleerde voorbeelden |

