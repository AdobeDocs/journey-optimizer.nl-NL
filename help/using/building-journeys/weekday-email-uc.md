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
source-git-commit: eee9a460fc443be29c1ef407a02c5645869ca11d
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 0%

---

# E-mails alleen verzenden tijdens weekdagen {#send-emails-only-on-weekdays}

Dit gebruiksgeval toont aan hoe te om een reis in Adobe Journey Optimizer te vormen die e-mails slechts op weekdagen (Maandag door Vrijdag) verzendt. Voor profielen die de reis op weekends (Zaterdag of Zondag) ingaan, worden de e-mails automatisch een rij gevormd en verzonden op Maandag bij een gespecificeerde tijd. Dit zorgt voor een optimale betrokkenheid door berichten te leveren tijdens de werkweek.

## Hoofdlettergebruik

**de Uitdaging**: Zorgen dat de e-mails slechts op weekdagen worden verzonden, alhoewel de profielen de reis op weekends kunnen ingaan. Voor weekendvermeldingen moeten e-mails op maandag in een bepaalde periode in de wachtrij worden geplaatst en worden verzonden.

**de Oplossing**: Gebruik een voorwaardenactiviteit om de dag van de week te identificeren. Voor weekendvermeldingen wacht activiteiten met aangepaste formules de e-mail tot maandag. De weekdagingangen gaan direct aan de e-mail te werk verzendt stap.

Deze benadering toont u hoe te om een voorwaardenactiviteit te gebruiken om te controleren als de huidige dag Zaterdag of Zondag is, voert de activiteiten van de Wacht met douaneformules voor weekendingangen uit, rijen weekende-mails voor Maandag levering op een specifiek uur, en verzendt onmiddellijk e-mails voor weekdagingangen (maandag-vrijdag).

Deze benadering is ideaal voor zaken-aan-zaken (B2B) e-mailcampagnes, professionele nieuwsbrieven en mededelingen, zaken-gerelateerde aankondigingen, werk-gerelateerde productupdates, en om het even welke marketing campagne waar de levering in het weekend niet wordt gewenst.

>[!NOTE]
>
>Om dit gebruiksgeval uit te voeren, hebt u een actieve instantie van Adobe Journey Optimizer met een gevormde [ oppervlakte van het e-mailkanaal ](../configuration/channel-surfaces.md), een [ publiek ](../audience/about-audiences.md) of [ gebeurtenis ](../event/about-events.md) nodig om de reis, en een basisbegrip van [ reisvoorwaarden ](condition-activity.md) en [ uitdrukkingen ](expression/expressionadvanced.md) in werking te stellen.


## Implementatiestappen

### Stap 1: Maak uw reis

1. Navigeer naar **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** in Adobe Journey Optimizer.

1. Klik **[!UICONTROL Create Journey]** om [ een nieuwe reis ](journey-gs.md) tot stand te brengen.

1. Vorm de [ reiseigenschappen ](journey-properties.md).

1. Kies het toegangspunt voor uw reis:
   * **[las Publiek](read-audience.md)**: Voor partijcampagnes richtend een specifiek publiek
   * **[Gebeurtenis](../event/about-events.md)**: Voor in real time teweeggebrachte reizen die op klantengedrag worden gebaseerd

### Stap 2: Voeg een Condition-activiteit toe om de dag van de week te controleren

Vlak na het begin van de rit voegt u een **[!UICONTROL Condition]** -activiteit toe om te controleren of de huidige dag zaterdag of zondag is. Hierdoor wordt de workflow dienovereenkomstig vertakt.

1. Sleep een [**[!UICONTROL Condition]**activiteit ](condition-activity.md) naar het canvas na het ingangspunt.

1. Klik op de **[!UICONTROL Condition]** -activiteit om het configuratievenster te openen.

1. Selecteer **[!UICONTROL Time condition]** als voorwaardetype.

1. Selecteer **[!UICONTROL Day of the week]** als de optie voor het filteren van tijd.

1. Voor de **eerste weg (Zaterdag)**, uitgezochte **Zaterdag** slechts. Label dit pad als &quot;zaterdag&quot;.

1. Klik op **[!UICONTROL Add a path]** om een tweede voorwaarde te maken.

1. Voor de **tweede weg (Zondag)**, selecteer **[!UICONTROL Day of the week]** en kies **zondag** slechts. Label dit pad als &quot;zondag&quot;.

   ![ Vormend de Zaterdag en de Zondag voorwaarden in de uitdrukkingsredacteur ](assets/weekday-email-uc-condition-expression.png)


1. Schakel **[!UICONTROL Show path for other cases than the one(s) above]** in om een pad te maken voor weekdagvermeldingen (maandag t/m vrijdag).

>[!NOTE]
>
>De tijdzone die wordt gebruikt voor de evaluatie van de dag van de week, wordt gedefinieerd op het niveau van de reis in de vervoerseigenschappen en niet op het niveau van de conditie. De reis [ timezone ](timezone-management.md) die in de formule wordt gebruikt is de gevormde tijdzone van de reis, niet de ontvanger.

### Stap 3: Configureer wachtactiviteiten voor weekendvermeldingen

Gebruik **[!UICONTROL Wait]** -activiteiten met aangepaste formules voor profielen die op zaterdag of zondag worden ingevoerd om de e-mail uit te stellen tot maandag op het gewenste uur.

Gebruik in de **[!UICONTROL Wait]** -activiteit de volgende formule:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Waarbij:

* **X** is het aantal dagen te wachten:
   * Het gebruik **2** voor Zaterdag (wacht tot Maandag)
   * Gebruik **1** voor Zondag (wacht tot Maandag)
* **H** is het uur u wilt verzenden (b.v., **9** voor 9 AM)


**Voorbeeld voor Zaterdag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Voorbeeld voor Zondag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Om dit in uw reis uit te voeren:

1. Op de **weg van de Zaterdag**, voeg a **[!UICONTROL Wait]** activiteit na de voorwaarde toe.

1. Selecteer **[!UICONTROL Duration]** als type wait.

1. Klik op **[!UICONTROL Advanced mode]** om de aangepaste formule in te voeren.

1. Enter: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![ Reis met drie voorwaardenwegen - Zaterdag, Zondag, en Weekdagen ](assets/weekday-email-uc-paths.png)

1. Herhaal de zelfde stappen voor de **weg van de Zondag**, gebruikend: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Voor complexere kantooruren (b.v., verzend slechts tussen 9.00 uur en 5.00 uur op weekdagen), kunt u de formule en de voorwaarden verder verbeteren.

### Stap 4: Wekdagtak

Voor profielen die van maandag tot en met vrijdag ingaan, ga aan de e-mail stap zoals gebruikelijk te werk.

1. Voor de **Wekdagweg** (de &quot;andere gevallen&quot;weg), ga direct te werk om een **[!UICONTROL Email]** actieactiviteit toe te voegen. Er is geen **[!UICONTROL Wait]** activiteit nodig voor weekdagvermeldingen.

1. Configureer uw e-mailbericht naar wens.

### Stap 5: Voltooi de transportstroom

Na de **[!UICONTROL Wait]** -activiteiten op zowel de paden van zaterdag als van zondag, moeten alle drie de paden (zaterdag, zondag en weekdagen) doorlopen naar dezelfde **[!UICONTROL Email]** -actieactiviteit. Voeg een **[!UICONTROL End]** activiteit na e-mail toe.

### Overzicht van visuele workflow

De volledige reisworkflow volgt deze logica:

* **Begin** → **[!UICONTROL Condition]**: Is het zaterdag of Zondag?
   * **ja (Zaterdag):** **[!UICONTROL Wait]** tot Maandag 9 AM → **[!UICONTROL Send email]**
   * **ja (Zondag):** **[!UICONTROL Wait]** tot Maandag 9 AM → **[!UICONTROL Send email]**
   * **Nr (Maandag-Vrijdag):** **[!UICONTROL Send email]** onmiddellijk

Dit zorgt ervoor dat alle e-mails alleen op weekdagen worden verzonden, waarbij weekendberichten automatisch in de wachtrij worden geplaatst voor levering op maandag.

### Stap 6: Test uw reis

Voordat u publiceert, test u de reislogica grondig in de testmodus van Adobe Journey Optimizer om te controleren of alles werkt zoals u had verwacht:

1. Klik op de knop **[!UICONTROL Test]** in de rechterbovenhoek.

1. Laat [ testwijze ](testing-the-journey.md) toe.

1. Creeer [ testprofielen ](../audience/creating-test-profiles.md) met gesimuleerde ingstijden op verschillende dagen van de week:
   * **ingang van de Zaterdag**: Verifieer het profiel volgt de weg van de Zaterdag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **de ingang van de Zondag**: Verifieer het profiel volgt de weg van de Zondag, wacht en ontvangt e-mail op Maandag in het gespecificeerde uur
   * **Maandag-Vrijdag ingangen**: Verifieer e-mails onmiddellijk zonder enige wachttijd worden verzonden

1. Controleer de reisvisualisatie om ervoor te zorgen dat de profielen de correcte voorwaardelijke wegen (Zaterdag, Zondag, of weekdag) volgen.

1. Controle voor om het even welke [ fouten of waarschuwingen ](troubleshooting.md) in de reis.

1. Verifieer dat de wachtwoorden de correcte duur voor uw gewenste Maandag leveringstijd berekenen.

>[!IMPORTANT]
>
>Test altijd uw reislogica op testwijze om ervoor te zorgen de activiteiten van de Wacht zich zoals verwacht gedragen. Gebruik de Wijze van de Test om verschillende ingangsscenario&#39;s te simuleren en te bevestigen dat de weekendingangen correct voor Maandlevering een rij worden gevormd. Zie [ reis testende beste praktijken ](testing-the-journey.md) voor meer details.

### Stap 7: Uw reis publiceren

Zodra het testen is voltooid:

1. Klik op **[!UICONTROL Publish]** in de rechterbovenhoek.

1. Bevestig de [ publicatie ](publish-journey.md).

1. Controleer de vervoersprestaties gebruikend [ Reis die ](report-journey.md) rapporteert en [ levende rapporten ](../reports/journey-live-report.md).


## Verwante onderwerpen

* Leer hoe te om verschillende wegen in uw reis met [ te creëren de activiteiten van de Voorwaarde ](condition-activity.md)
* Gedetailleerde gids op [ gebruikend voorwaarden in een reis ](conditions.md)
* Vorm wachttijdsduur en formules met [ wachten activiteit ](wait-activity.md)
* Volledige verwijzing voor [ datumfuncties ](functions/date-functions.md)
* Bouw complexe uitdrukkingen met de [ redacteur van de Uitdrukking ](expression/expressionadvanced.md)
* Aanbevolen benaderingen voor [ reisontwerp en beste praktijken ](journey-gs.md#best-practices)
