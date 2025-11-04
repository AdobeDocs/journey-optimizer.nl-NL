---
solution: Journey Optimizer
product: journey optimizer
title: Werken met trapsgewijze gebeurtenissen
description: Leer hoe u in Adobe Journey Optimizer met trapsgewijze gebeurtenissen kunt werken - begrijp wat ze zijn, waarom ze belangrijk zijn en hoe u ze kunt gebruiken voor analyses en optimalisatie
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: transport, stapgebeurtenissen, analyse, rapportage, controle, XDM
source-git-commit: 9320777cfb75fd1370c11b601908644ba17ff21e
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 1%

---

# Werken met trapsgewijze gebeurtenissen {#work-with-journey-step-events}

De gebeurtenissen van de stap van de reis worden automatisch geproduceerd gebeurtenissen die gedetailleerde informatie over elke stap a [&#x200B; profiel &#x200B;](../audience/get-started-profiles.md) vangen neemt aangezien zij door a [&#x200B; reis &#x200B;](../building-journeys/journey.md) in Adobe Journey Optimizer vorderen. Deze gebeurtenissen verstrekken uitvoerige zicht in [&#x200B; vervoersprestaties &#x200B;](../building-journeys/report-journey.md) en laten krachtige analytische mogelijkheden toe.

## Wat zijn trapsgewijze gebeurtenissen? {#what-are-step-events}

De gebeurtenissen van de wegstap zijn systeem-geproduceerde [&#x200B; XDM (het Model van Gegevens van de Ervaring) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"} gebeurtenissen die Adobe Journey Optimizer automatisch leidt en naar [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=nl-NL){target="_blank"} verzendt wanneer een profiel zich van één knoop aan een andere in een reis beweegt. Elke gebeurtenis beantwoordt aan een specifieke [&#x200B; reisactiviteit &#x200B;](../building-journeys/about-journey-activities.md) of overgang in de de reiservaring van de klant.

Er zijn twee belangrijke soorten gebeurtenissen van de reisstap:

- **tripStepEvent**: Gebeurtenissen met betrekking tot individuele profielvooruitgang door reisstappen
- **tripStepProfileEvent**: Gebeurtenissen die extra informatie van de profielcontext omvatten

### Wat veroorzaakt gebeurtenissen van de reisstap? {#event-triggers}

Reisstapgebeurtenissen worden automatisch gegenereerd voor verschillende reisactiviteiten:

- **gebeurtenissen van de Ingang**: Wanneer een profiel [&#x200B; een reis &#x200B;](../building-journeys/entry-management.md) ingaat
- **uitvoering van de Actie**: Wanneer [&#x200B; de berichten &#x200B;](../building-journeys/journeys-message.md) of [&#x200B; douaneacties &#x200B;](../building-journeys/using-custom-actions.md) worden verzonden
- **evaluatie van de Voorwaarde**: Wanneer de profielen door [&#x200B; voorwaarden &#x200B;](../building-journeys/condition-activity.md) en beslissingspunten overgaan
- **wacht activiteiten**: Wanneer de profielen ingaan en weggaan [&#x200B; knopen &#x200B;](../building-journeys/wait-activity.md) wachten
- **de gebeurtenissen van de Uitgang**: Wanneer de profielen voltooien of [&#x200B; een reis &#x200B;](../building-journeys/end-journey.md) weggaan
- **de behandeling van de Fout**: Wanneer de fouten tijdens reisuitvoering voorkomen

>[!NOTE]
>
>De gebeurtenissen van de wegstap worden door gebrek op alle instanties geactiveerd. U kunt niet de [&#x200B; schema&#39;s en datasets &#x200B;](sharing-overview.md) wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Deze schema&#39;s en datasets zijn op read-only wijze.

Leer meer over [&#x200B; de gebeurtenisschema&#39;s van de reisstap &#x200B;](sharing-field-list.md).

## Waarom de gebeurtenissen van de reisstap belangrijk zijn {#why-step-events-matter}

Reisstapgebeurtenissen bieden een kritieke waarde voor organisaties die Adobe Journey Optimizer gebruiken:

### Analyse en bewaking in realtime {#real-time-analytics}

- **Prestaties die van de Reis** volgen: Monitor hoe de profielen door uw reizen in real time stromen gebruikend [&#x200B; levende rapporten &#x200B;](live-report.md)
- **analyse van de Omzetting**: Begrijp drop-off punten en succesvolle omzettingswegen met [&#x200B; reisanalyse &#x200B;](journey-global-report-cja.md)
- **de opsporing van de Fout**: Identificeer en los kwesties problemen op aangezien zij door [&#x200B; controle en alarm &#x200B;](alerts.md) voorkomen

### Gegevensintegratie en inzichten {#data-integration}

- **dwars-platformanalyse**: Combineer reisgegevens met andere [&#x200B; gegevensbronnen van Adobe Experience Platform &#x200B;](../datasource/adobe-experience-platform-data-source.md)
- **Klant 360 mening**: Creeer uitvoerige [&#x200B; klantenprofielen &#x200B;](../audience/get-started-profiles.md) die reisinteractie omvatten
- **modellering van de Attributie**: Verbind de punten van de reisaanraking met stroomafwaartse bedrijfsresultaten gebruikend [&#x200B; Customer Journey Analytics &#x200B;](cja-ajo.md)

### Optimalisatiemogelijkheden {#optimization}

- **A/B testende inzichten**: Analyseer de prestaties van verschillende reiswegen gebruikend [&#x200B; experimenteren &#x200B;](campaign-global-report-cja-experimentation.md)
- **de verhoging van Personalization**: De gegevens van het het reisgedrag van het gebruik om toekomstige ervaringen met [&#x200B; dynamische inhoud te verbeteren &#x200B;](../personalization/dynamic-content.md)
- **Operationele efficiency**: Identificeer knelpunten en optimaliseer [&#x200B; reisontwerp &#x200B;](../building-journeys/using-the-journey-designer.md)

## Hoe de gebeurtenissen van de reisstap te gebruiken {#how-to-use-step-events}

### Toegang tot gebeurtenisgegevens voor stappen {#accessing-data}

Gebeurtenisgegevens voor stap van de reis worden automatisch opgeslagen in Adobe Experience Platform en zijn toegankelijk via:

1. **het Meer van Gegevens vragen**: Gebruik SQL om `journey_step_events` dataset met [&#x200B; de Dienst van de Vraag &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl){target="_blank"} te vragen
2. **Customer Journey Analytics**: Analyseer reisgegevens door [&#x200B; geavanceerde analysehulpmiddelen &#x200B;](cja-ajo.md)
3. **Echt - tijd rapporterend**: De gegevens van de toegang door Journey Optimizer [&#x200B; ingebouwde rapporteringsmogelijkheden &#x200B;](gs-reports.md)
4. **APIs**: Programmatiatically toegang tot gebeurtenisgegevens voor douanetoepassingen

Leer meer over [&#x200B; de toegang tot van datasets &#x200B;](../data/datasets-query-examples.md).

### Belangrijke gegevenspunten beschikbaar {#key-data-points}

Reisstapgebeurtenissen bevatten uitgebreide informatie, waaronder:

- **identificatie van de Reis**: [&#x200B; identiteitskaart van de Reis, versie, en naam &#x200B;](sharing-journey-fields.md)
- **informatie van het Profiel**: [&#x200B; identiteitskaart van het Profiel en bijbehorende identiteiten &#x200B;](sharing-identity-fields.md)
- **Details van de Stap**: [&#x200B; Naam van de Knoop, step type, en uitvoeringsstatus &#x200B;](sharing-common-fields.md)
- **Tijdstempels**: Exacte timing van elke reisstap
- **Resultaten van de Actie**: [&#x200B; de status van het Succes/van de mislukking en uitvoeringsdetails &#x200B;](sharing-execution-fields.md)
- **informatie van de Fout**: Gedetailleerde [&#x200B; foutencodes en beschrijvingen &#x200B;](sharing-field-list.md#discarded-events) wanneer de kwesties voorkomen

Onderzoek alle [&#x200B; beschikbare gebiedsdefinities &#x200B;](sharing-field-list.md).

### Vaak voorkomende gebruiksscenario&#39;s {#common-use-cases}

**Controle van Prestaties**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**analyse van de Fout**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**analyse van de Reis funnel**

- Conversietarieven bijhouden voor elke stap van de reis
- Identificeer waar de profielen het vaakst de reis verlaten
- De tijd meten die in verschillende reisfasen wordt doorgebracht

Leer meer [&#x200B; vraagtechnieken voor de analyse van funnel &#x200B;](query-examples.md#common-queries).

## Monsters en bronnen {#samples-resources}

### Zoekvoorbeelden en sjablonen {#query-examples}

Verken uitvoerige vraagvoorbeelden voor gemeenschappelijke de gebeurtenisanalyse van de reisstap:

- **[de vraagvoorbeelden van de de stapel van de Reis](query-examples.md)**: Klaar-aan-gebruik SQL vragen voor gemeenschappelijke analytische scenario&#39;s
- **[de vraagsteekproeven van de Dataset](../data/datasets-query-examples.md#journey-step-event)**: Voorbeelden van het vragen van de datasets van de de gebeurtenisgebeurtenis van de reisstap
- **[op profiel-gebaseerde vragen](query-examples.md#profile-based-queries)**: De individuele profielreizen van het spoor en interacties

### Velddocumentatie {#field-documentation}

Begrijp de volledige gegevensstructuur van de gebeurtenissen van de wegstap:

- **[de lijst van de de gebeurtenisgebeurtenis van de Reis van de Reis](sharing-field-list.md)**: Uitgebreide verwijzing van alle beschikbare gebieden
- **[Gemeenschappelijke gebieden](sharing-common-fields.md)**: Gedeelde gebieden over tripStepEvent en tripStepProfileEvent
- **[de uitvoeringsgebieden van de Actie](sharing-execution-fields.md)**: Gebieden specifiek voor het volgen van de actieuitvoering
- **[de gebieden van de Reis](sharing-journey-fields.md)**: Reis-specifieke meta-gegevens en herkenningstekens

### Best practices en probleemoplossing {#best-practices}

**optimalisering van Prestaties**

- Gebruik `journeyVersionID` in plaats van `journeyVersionName` voor betere vraagprestaties ([&#x200B; leert meer over reiseigenschappen &#x200B;](../building-journeys/expression/journey-properties.md))
- Filter door datumwaaiers om vraagsnelheid op grote datasets te verbeteren
- De profielidentiteiten van de hefboomwerking die uw [&#x200B; configuratie van de reis namespace &#x200B;](../building-journeys/entry-management.md) aanpassen

**Kwaliteit van Gegevens**

- Regelmatig toezicht voor [&#x200B; verworpen gebeurtenissen &#x200B;](sharing-field-list.md#discarded-events) om gegevenskwesties te identificeren
- Valideer dat de gebeurtenisschema&#39;s uw analysevereisten aanpassen
- Correcte foutafhandeling implementeren in aangepaste query&#39;s

**Analysestrategieën**

- Combineer de gebeurtenissen van de reisstap met [&#x200B; bericht terugkoppelt gegevens &#x200B;](../data/datasets-query-examples.md#message-feedback-event-dataset) voor volledige attributie
- Gebruik tijdgebaseerde analyse om inzicht te krijgen in de snelheid van de reis en knelpunten

### Geavanceerde analysemogelijkheden {#advanced-analytics}

**de integratie van Customer Journey Analytics**
De gebeurtenissen van de wegstap kunnen worden geanalyseerd gebruikend [&#x200B; Customer Journey Analytics &#x200B;](cja-ajo.md) voor:

- Geavanceerde kenmerkmodellen
- Visualisatie van reizen tussen kanalen
- Predictieve analyse van reisresultaten

Leer hoe te [&#x200B; vormen Customer Journey Analytics &#x200B;](report-gs-cja.md) voor de gegevens van Journey Optimizer.

## Aanvullende bronnen {#additional-resources}

### Documentatiekoppelingen {#documentation-links}

- **[stap het delen van de Reis overzicht](sharing-overview.md)**: Begrijpend hoe de gegevens van de reis aan Adobe Experience Platform stromen
- **[Ingebouwd schemawoordenboek &#x200B;](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL){target="_blank"}**: Volledige XDM schemaverwijzing
- **[Journey Optimizer die](report-gs-cja.md)** meldt: Overzicht van rapporteringsmogelijkheden in Journey Optimizer

### Integratiehulplijnen {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Het analyseren van de gegevens van Journey Optimizer in CJA
- **[het beheer van Gegevens](../data/export-datasets.md)**: Het uitvoeren van en het leiden van reisgegevens
- **[Privacy en bestuur](../privacy/audit-logs.md)**: De overwegingen van het bestuur van gegevens voor reisgebeurtenissen


**Volgende stappen:**

- Begin met [&#x200B; het creëren van uw eerste reisrapporten &#x200B;](sharing-overview.md)
- Onderzoek [&#x200B; vraagvoorbeelden &#x200B;](query-examples.md) voor specifieke gebruiksgevallen
- Leer over [&#x200B; beste praktijken van het reisbeheer &#x200B;](../building-journeys/journey.md)
