---
solution: Journey Optimizer
product: journey optimizer
title: Criteria voor binnenkomst en vertrek op de reis
description: Leer hoe u effectief kunt beheren wanneer profielen reizen en afsluiten met voorbeelden uit de praktijk en best practices
feature: Journeys, Profiles
role: User
level: Intermediate
hide: true
hidefromtoc: true
keywords: binnenkomst, vertrek, criteria, reis, profiel, toegang, beste praktijken
version: Journey Orchestration
source-git-commit: 9e5b85dec8a58a4d008ab63337589352c0fa5ee6
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 0%

---


# Werken met entry- en exit-criteria {#entry-exit-criteria-guide}

In de organisatie van de klantenervaring, vereist het leveren van het juiste bericht op het juiste ogenblik nauwkeurige controle over wanneer de klanten uw reizen ingaan en weggaan. Het begrip en behoorlijk het vormen van ingang en uitgangscriteria kan het verschil tussen een succesvolle, het betreden campagne en gemiste kansen of berichtvermoeidheid maken.

Deze gids verstrekt praktische begeleiding, praktijkvoorbeelden, en beste praktijken voor het beheren van reis toegang en uitgangscriteria in Adobe Journey Optimizer.

## Wat zijn entry- en exitcriteria? {#what-are-criteria}

**criteria van de Ingang** bepalen de voorwaarden waaronder het a [&#x200B; klantenprofiel &#x200B;](../audience/get-started-profiles.md) kwalificeert om een specifieke reis in te gaan. Profielen kunnen worden ingevoerd op basis van:

* **[gedrag van de Klant](../event/about-events.md)** - De acties die door klanten worden genomen brengen reisingang in real time, zoals het maken van een aankoop, het verlaten van een kar, of het openen van uw mobiele app teweeg.

* **[de attributen van het Profiel](../audience/get-started-profiles.md)** - de kenmerken van de Klant bepalen geschiktheid die op gegevens wordt gebaseerd die in hun profiel, zoals loyaliteitsrij, plaats, leeftijd, of communicatie voorkeur worden opgeslagen.

* **[Externe gebeurtenissen](../event/about-creating-business.md)** - Bedrijfs of milieu trekkers die veelvoudige klanten gelijktijdig, zoals lage inventarisalarm, weersomstandigheden, of prijsveranderingen beïnvloeden.

* **[lidmaatschap van het publiek](../audience/about-audiences.md)** - het behoren tot een specifiek publiekssegment laat gerichte reizen voor groepen zoals klanten met een hoge waarde, inactieve gebruikers, of nieuwe abonnees toe.

**de criteria van de Uitgang** bepalen wanneer en hoe een profiel verlaat of van een reis wordt verwijderd:

* **de voltooiing van de Reis** - Profielen sluiten automatisch wanneer zij het [&#x200B; eind van alle reiswegen &#x200B;](end-journey.md) bereiken, die de ontworpen ervaring voltooien.

* **metrische verwezenlijking van het Succes** - de uitgang van Profielen wanneer zij het [&#x200B; reisdoel &#x200B;](success-metrics.md) voltooien, zoals het maken van een aankoop of het downloaden van een app, die onnodige follow-upmededelingen elimineren.

* **op voorwaarde-Gebaseerde** - de uitgang van Profielen wanneer [&#x200B; specifieke voorwaarden &#x200B;](condition-activity.md), als inactiviteit over een vastgestelde periode of veranderingen in profielattributen worden voldaan.

* **op gebeurtenis-Gebaseerde** - de uitgang van Profielen wanneer [&#x200B; specifieke gebeurtenissen &#x200B;](../event/about-events.md) voorkomen, zoals abonnementsannulering of productterugkeer.

* **de diskwalificatie van het publiek** - de uitgang van Profielen wanneer zij niet meer aan de [&#x200B; criteria van het doelpubliek &#x200B;](../audience/about-audiences.md) voldoen, die berichten verzekeren blijven relevant.

## Waarom toelatings- en uitreiscriteria van belang zijn {#why-they-matter}

Een correcte definitie van entry- en exit-criteria levert een aanzienlijke bedrijfswaarde op:

* **Relevantie**: Slechts gaan de juiste klanten de reis in, die overeenkomst en omzettingspercentages verhogen door het meest aangewezen publiek in de optimale tijd te richten.

* **Efficiëntie**: Verhindert klanten in irrelevante reizen blijven, die onnodige mededelingen, operationele kosten, en klantenergernis verminderen.

* **Personalization**: Laat dynamisch het maken van ervaringen toe die op gegevens en gedrag in real time worden gebaseerd, creërend zinvollere klanteninteractie.

* **Naleving**: Helpt frequentie het begrenzen te beheren en overmededeling te vermijden, die klantenvoorkeur en regelgevende vereisten respecteren terwijl het handhaven van merkreputatie.

## Voorbeelden van reizen die binnenkomen en vertrekken in de praktijk {#real-world-examples}

Hier zijn algemene scenario&#39;s die aantonen hoe entry- en exit-criteria in de praktijk werken:

**Welkome campagne voor nieuwe abonnees**

* **Ingang**: De profielen gaan de reis in wanneer zij aan een nieuwsbrief intekenen
* **Uitgang**: De uitgang van profielen zodra zij een welkome reeks e-mails of na een vastgestelde tijd hebben voltooid als zij niet in dienst nemen
* **Voordeel**: Zorgt ervoor dat de nieuwe abonnees tijdig onboarding ontvangen terwijl het vermijden van herhalend overseinen

**Verlaten wortelterugwinning**

* **Ingang**: De klanten gaan de reis in als zij punten aan een karretje toevoegen maar voltooien controle niet binnen 24 uren
* **Uitgang**: De profielen gaan weg wanneer zij de aankoop voltooien of na 7 dagen als geen aankoop wordt gemaakt
* **Voordeel**: De omzettingen van aandrijving door geschikte herinneringen zonder het spammen van ongeïnteresseerde klanten

**Loyalty programmabetrokkenheid**

* **Ingang**: De klanten voegen zich bij de reis na het bereiken van een bepaalde drempel van loyaliteitspunten
* **Uitgang**: De uitgang van profielen na het terugkeren van beloningen of indien inactief gedurende 60 dagen
* **Voordeel**: Houdt high-value klanten betrokken bij gepersonaliseerde aanbiedingen en vermijdt communicatie moeheid

**Product terugkoppelt inzameling**

* **Ingang**: De klanten gaan de reis na het ontvangen van een gebeurtenis van de de bevestigingsbevestiging van de productlevering in
* **Uitgang**: De uitgang van profielen zodra terugkoppelt wordt voorgelegd of na 10 dagen als geen reactie
* **Voordeel**: Vangt waardevolle terugkoppelt onmiddellijk zonder klanten met blijvende verzoeken te irriteren

## Hoe te om de criteria van de reisingang te vormen {#configure-entry}

>[!BEGINSHADEBOX]

**leer alles u over de Criteria van de Ingang hier moet weten:**

* **[gebeurtenis-Gebaseerde Trekkers](../event/about-events.md)**: De gebeurtenissen van het gebruik zoals &quot;profielverwezenlijking,&quot;uitgevoerde transactie,&quot;of douanegebeurtenissen om van een reis af te schoppen. [&#x200B; vorm gebeurtenissen &#x200B;](../event/about-creating.md) in **[!UICONTROL Administration]** > **[!UICONTROL Events]**, bepaal [&#x200B; gebeurtenisschema en gebieden &#x200B;](../event/experience-event-schema.md), dan voeg de gebeurtenis van het **[!UICONTROL Events]** palet in [&#x200B; reisontwerper &#x200B;](using-the-journey-designer.md) toe.

* **[publiek-Gebaseerde Ingang](read-audience.md)**: De reizen van het doel aan profielen die tot specifiek publiek behoren, of als eenmalig partij of op een terugkerend programma. [&#x200B; creeer publiek &#x200B;](../audience/creating-a-segment-definition.md) in het **[!UICONTROL Audiences]** menu, dan voeg a **[!UICONTROL Read Audience]** activiteit toe en [&#x200B; vorm het programma &#x200B;](journey-properties.md#schedule).

* **[Ingang van de Kwalificatie van het publiek](audience-qualification-events.md)**: De reizen van de trekker wanneer de profielen voor of uitgang uit specifiek publiek in real time kwalificeren. Bepaal [&#x200B; het stromen publiek &#x200B;](../audience/about-audiences.md), voeg een **[!UICONTROL Audience Qualification]** gebeurtenis van het **[!UICONTROL Events]** palet toe, en kies het trekkertype.

* **[Filters van Attributen](condition-activity.md)**: Verfijn ingencriteria door gebeurtenissen of publiek met profielattributen en context te combineren gebruikend logica AND/OR. Het gebruik [&#x200B; voorwaarden &#x200B;](conditions.md) om [&#x200B; profielattributen &#x200B;](../audience/get-started-profiles.md), gebeurtenissen, of [&#x200B; externe gegevens &#x200B;](../datasource/about-data-sources.md) van verwijzingen te voorzien.

* **[Vensters van de Tijd en het Plannen](journey-properties.md#schedule)**: Plaats tijdelijke beperkingen om reizen te houden geschikt en relevant. Vorm [&#x200B; programma&#39;s op Gelezen de activiteiten van het Publiek &#x200B;](read-audience.md), gebruik [&#x200B; wacht activiteiten &#x200B;](wait-activity.md), en voeg [&#x200B; op tijd-gebaseerde voorwaarden &#x200B;](conditions.md) toe om timing te controleren.

>[!ENDSHADEBOX]

## Hoe de criteria voor het verlaten van de reis instellen {#configure-exit}

>[!BEGINSHADEBOX]

**leer alles u over de Criteria van de Uitgang hier moet weten:**

* **[Voltooiing van de Reis](end-journey.md)**: De profielen gaan automatisch weg nadat zij de definitieve reisstap bereiken. Ontwerpen van reispaden naar einde bij **[!UICONTROL End]** -activiteiten.

* **[Metrische Verwezenlijking van het Succes](journey-properties.md#exit-criteria)**: Bepaal succesmetriek (als aankoop of abonnement) en uitgangsprofielen op voltooiing. Klik **[!UICONTROL Show exit criteria]** pictogram, selecteer **[!UICONTROL Add exit criteria]**, en kies een [&#x200B; Gebeurtenis &#x200B;](../event/about-events.md) of [&#x200B; Publiek &#x200B;](../audience/about-audiences.md) als uitgangstrekker.

* **[Onderbreking van de Inactiviteit](wait-activity.md)**: De profielen van de uitgang als geen overeenkomst binnen een vastgestelde timeframe voorkomt. De Criteria van de uitgang van het gebruik [&#x200B; met publiek dat laatste betrokkenheidsdatum controleert, plaatst &#x200B;](journey-properties.md#exit-criteria) activiteiten [&#x200B; met bepaalde duur wachten, en gebruik &#x200B;](wait-activity.md) voorwaarden [&#x200B; om op activiteit te controleren.](condition-activity.md)

* **[Regels van de Wederopneming](entry-management.md)**: Beslis als de profielen de reis veelvoudige tijden of slechts eens kunnen opnieuw ingaan, afhankelijk van uw campagnestrategie. Vorm **[!UICONTROL Re-entrance]** montages in reis **[!UICONTROL Properties]** om wachttijden te plaatsen, gedwongen re-ingang toe te laten, of gebruik [&#x200B; supplementaire herkenningstekens &#x200B;](supplemental-identifier.md) voor context-specifieke re-ingang.

>[!ENDSHADEBOX]

## Gedetailleerde reisvoorbeelden {#journey-examples}

Raadpleeg de volgende gedocumenteerde gebruiksgevallen voor stapsgewijze implementatierichtlijnen met volledige technische details:

* **[Klant op het instappen reis &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - Bouw gepersonaliseerde welkomstervaringen met publiekskwalificatie, gebeurtenisonderbreking, en op doel-gebaseerde uitgang

* **[Verlaten kartterugwinning &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - herhaal verloren verkoop met gebeurtenis-teweeggebrachte reizen, playbooks, en kanaal verpletterend

* **[campagnes van de re-overeenkomst &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - terugwinning inactieve klanten met gedrag gericht en betaalde media activering

* **[verzendt berichten naar abonnees](message-to-subscribers-uc.md)** - de abonnementenlijsten van het doel met Gelezen Publiek en gepersonaliseerde inhoud

* **[verzend multi-kanaalberichten](journeys-uc.md)** - combineer e-mail en duw met reactiegebeurtenissen en multi-path logica

* **[verzendt e-mails slechts op weekdagen](weekday-email-uc.md)** - de mededelingen van het programma gebruikend op tijd-gebaseerde voorwaarden en wacht formules

>[!TIP]
>
>Doorblader alle beschikbare gebruiksgevallen in de [&#x200B; bibliotheek van de de gebruiksgevallen van de Reis &#x200B;](jo-use-cases.md) voor meer patronen en implementaties, met inbegrip van [&#x200B; oprijlevering &#x200B;](ramp-up-deliveries-uc.md), [&#x200B; de patronen van de ervaringsgebeurtenis &#x200B;](exp-event-lookup.md), en [&#x200B; verwijderend profielen uit levende reizen &#x200B;](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Aanbevolen werkwijzen voor het beheer van toegang en vertrek {#best-practices}

**Duidelijke definitie**

* Documenteer uw entry en exit logica alvorens reizen te bouwen om marketing en analyseteams in overeenstemming te brengen
* Stroomdiagrammen maken met toegangspunten, reispaden en uitgangsvoorwaarden
* Duidelijk bedrijfsregels definiëren: &quot;Profielen sluiten wanneer X plaatsvindt OF na Y dagen&quot;
* Beschrijvende labels gebruiken: &quot;Afsluiten - Aankoop voltooid&quot; en niet &quot;Afsluiten 1&quot;
* [&#x200B; reizen van de markering &#x200B;](../start/search-filter-categorize.md#tags) constant voor het melden en het filtreren

**vermijd overlappende reizen**

* [&#x200B; actieve reizen van de Controle &#x200B;](journey-ui.md) alvorens gelijkaardige degenen te lanceren om conflicten te verhinderen
* [&#x200B; van de hefboomwerking het conflictenbeheer &#x200B;](../conflict-prioritization/conflicts.md) en [&#x200B; prioritaire scores &#x200B;](../conflict-prioritization/priority-scores.md) om overlappingen op te lossen en ritten voorrang te geven
* Ontwerpreizen die elkaar aanvullen in plaats van met elkaar te concurreren

>[!NOTE]
>
>Voor geavanceerde scenario&#39;s zoals automatisch het verwijderen van profielen wanneer zij voor hoog-prioritaire reizen kwalificeren, gebruik [&#x200B; reis het in kaart brengen &amp; arbitrage &#x200B;](../conflict-prioritization/journey-capping.md) in plaats van uitgangscriteria.

**Monitor en optimaliseer**

* Het ingangstarief van het spoor, uitgangstarief, en voltooiingstarief voor elke reis die [&#x200B; reisrapporten gebruiken &#x200B;](../reports/journey-global-report-cja.md)
* De metriek van het succes van de monitor [&#x200B; &#x200B;](success-metrics.md): percentage dat via succes metrische voltooiing met betrekking tot onderbreking weggaat
* [&#x200B; ingang en uitgangscriteria van de Test &#x200B;](testing-the-journey.md) met diverse profielscenario&#39;s alvorens te lanceren
* Aanpassen op basis van gegevens: bij hoge vroegtijdige uitgangen beoordeelt u de relevantie van de entry-criteria; bij een lage mate van succes analyseert u de inhoud en de timing
* Alle actieve reizen driemaandelijks controleren

**Respect frequentiecaps**

* Plaats aangewezen [&#x200B; re-ingang wacht periodes &#x200B;](entry-management.md) of maak re-ingang voor eenmalige reizen onbruikbaar
* Het gebruik [&#x200B; frequentie capping regels &#x200B;](../conflict-prioritization/rule-sets.md) om over-mededeling te verhinderen
* De frequentiemetriek in rapportering controleren om naleving te verzekeren

>[!NOTE]
>
>Om frequentiegrenzen en de plafonds van de reisingang over veelvoudige reizen te beheren, gebruik [&#x200B; reis het in kaart brengen &amp; arbitrage &#x200B;](../conflict-prioritization/journey-capping.md) en [&#x200B; frequentie het in kaart brengen door kanaal &#x200B;](../conflict-prioritization/channel-capping.md).

## Conclusie {#conclusion}

De criteria voor het betreden en verlaten van de reis zijn de grondvesten aan het leveren van gepersonaliseerde, geschikte, en efficiënte klantenervaringen met Adobe Journey Optimizer. Door zorgvuldig deze voorwaarden te creëren, kunnen de marketers overeenkomst opvoeren, wrijving verminderen, en sterkere klantenverhoudingen bouwen.

Begin door uw klantentrekkers en uitgangspunten duidelijk in kaart te brengen, grondig te testen, en resultaten te controleren om uw reisorchestratie onophoudelijk te verfijnen.

## Gerelateerde bronnen {#related-resources}

**Technische documentatie**

* [&#x200B; het toegangsbeheer van het Profiel &#x200B;](entry-management.md) - Gedetailleerde technische gids voor ingangscontroles
* [&#x200B; eigenschappen van de Reis en uitgangscriteria &#x200B;](journey-properties.md) - Volledige configuratieverwijzing
* [&#x200B; hoe de reizen &#x200B;](end-journey.md) beëindigen - het beheer van de levenscyclus van de Reis
* [&#x200B; Supplementaire herkenningstekens &#x200B;](supplemental-identifier.md) - Geavanceerde hertoelatingsscenario&#39;s
* [&#x200B; de ontwerper van de Reis &#x200B;](using-the-journey-designer.md) - bouw en ontwerpreizen

**Zelfstudies en voorbeelden**

* [&#x200B; de gebruiksgevallen van de Reis &#x200B;](jo-use-cases.md) - Volledige reisvoorbeelden en patronen
* [&#x200B; Klant op het instappen video &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* [&#x200B; Verlaten kart video &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* [&#x200B; Communautaire blog: De Criteria van de Ingang en van de Uitgang &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**Verwante mogelijkheden**

* [kwalificatiegebeurtenissen voor het publiek](audience-qualification-events.md)
* [Metrische gegevens en doelstellingen van succes](success-metrics.md)
* [Conflictbeheer](../conflict-prioritization/conflicts.md)
* [Frequentiecorrectie](../conflict-prioritization/rule-sets.md)
* [Reizen testen](testing-the-journey.md)
* [Voorwaardeactiviteit](condition-activity.md)
* [Reactiegebeurtenissen](reaction-events.md)
* [Wachtactiviteit](wait-activity.md)
