---
solution: Journey Optimizer
product: journey optimizer
title: Werken met trapsgewijze gebeurtenissen
description: Leer hoe u in Adobe Journey Optimizer met trapsgewijze gebeurtenissen kunt werken - begrijp wat ze zijn, waarom ze belangrijk zijn en hoe u ze kunt gebruiken voor analyses en optimalisatie
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: transport, stapgebeurtenissen, analyse, rapportage, controle, XDM
hide: true
hidefromtoc: true
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 1%

---

# Werken met trapsgewijze gebeurtenissen {#work-with-journey-step-events}

Gebeurtenissen met een stap naar een reis zijn automatisch gegenereerde gebeurtenissen die gedetailleerde informatie vastleggen over elke stap die een profiel uitvoert tijdens een reis in Adobe Journey Optimizer. Deze gebeurtenissen bieden uitgebreide zichtbaarheid in de prestaties van de reis en bieden krachtige analysemogelijkheden.

## Wat zijn trapsgewijze gebeurtenissen? {#what-are-step-events}

De gebeurtenissen van de wegstap zijn systeem-geproduceerde (het Model van Gegevens van de Ervaring) gebeurtenissen XDM die Adobe Journey Optimizer automatisch creeert en naar Adobe Experience Platform verzendt wanneer een profiel zich van één knoop aan een andere in een reis beweegt. Elke gebeurtenis komt overeen met een specifieke actie of overgang in de reiservaring van de klant.

Er zijn twee belangrijke soorten gebeurtenissen van de reisstap:

- **tripStepEvent**: Gebeurtenissen met betrekking tot individuele profielvooruitgang door reisstappen
- **tripStepProfileEvent**: Gebeurtenissen die extra informatie van de profielcontext omvatten

### Wat veroorzaakt gebeurtenissen van de reisstap? {#event-triggers}

Reisstapgebeurtenissen worden automatisch gegenereerd voor verschillende reisactiviteiten:

- **de gebeurtenissen van de Ingang**: Wanneer een profiel een reis ingaat
- **uitvoering van de Actie**: Wanneer de berichten worden verzonden of de douaneacties worden uitgevoerd
- **evaluatie van de Voorwaarde**: Wanneer de profielen door besluitvormingspunten overgaan
- **wacht activiteiten**: Wanneer de profielen ingaan en weggaan wachtknopen
- **de gebeurtenissen van de Uitgang**: Wanneer de profielen een reis voltooien of weggaan
- **de behandeling van de Fout**: Wanneer de fouten tijdens reisuitvoering voorkomen

>[!NOTE]
>
>De gebeurtenissen van de wegstap worden door gebrek op alle instanties geactiveerd. U kunt niet de schema&#39;s en datasets wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Deze schema&#39;s en datasets zijn op read-only wijze.

## Waarom de gebeurtenissen van de reisstap belangrijk zijn {#why-step-events-matter}

Reisstapgebeurtenissen bieden een kritieke waarde voor organisaties die Adobe Journey Optimizer gebruiken:

### Analyse en bewaking in realtime {#real-time-analytics}

- **het prestaties volgen van de Reis**: Monitor hoe de profielen door uw reizen in real time stromen
- **analyse van de Omzetting**: Begrijp drop-off punten en succesvolle omzettingswegen
- **de opsporing van de Fout**: Identificeer en los kwesties problemen op aangezien zij voorkomen

### Gegevensintegratie en inzichten {#data-integration}

- **dwars-platformanalyse**: Combineer reisgegevens met andere gegevensbronnen van Adobe Experience Platform
- **Klant 360 mening**: Creeer uitvoerige klantenprofielen die reisinteractie omvatten
- **modellering van de Attributie**: Verbind reis aanraakpunten met stroomafwaartse bedrijfsresultaten

### Optimalisatiemogelijkheden {#optimization}

- **A/B testende inzichten**: Analyseer de prestaties van verschillende reiswegen
- **de verhoging van Personalization**: De gegevens van het het reisgedrag van het gebruik om toekomstige ervaringen te verbeteren
- **Operationele efficiency**: Identificeer knelpunten en optimaliseer reisontwerp

## Hoe de gebeurtenissen van de reisstap te gebruiken {#how-to-use-step-events}

### Toegang tot gebeurtenisgegevens voor stappen {#accessing-data}

Gebeurtenisgegevens voor stap van de reis worden automatisch opgeslagen in Adobe Experience Platform en zijn toegankelijk via:

1. **Vraagstukken van het meer van Gegevens**: Gebruik SQL om de `journey_step_events` dataset te vragen
2. **Customer Journey Analytics**: Analyseer reisgegevens door geavanceerde analysehulpmiddelen
3. **Real-time rapporterend**: De gegevens van de toegang door ingebouwde Journey Optimizer rapporteringsmogelijkheden
4. **APIs**: Programmatiatically toegang tot gebeurtenisgegevens voor douanetoepassingen

### Belangrijke gegevenspunten beschikbaar {#key-data-points}

Reisstapgebeurtenissen bevatten uitgebreide informatie, waaronder:

- **identificatie van de Reis**: Identiteitskaart van de reis, versie, en naam
- **informatie van het Profiel**: Identiteitskaart van het profiel en bijbehorende identiteiten
- **Details van de Stap**: De naam van het knooppunt, stappentype, en uitvoeringsstatus
- **Tijdstempels**: Exacte timing van elke reisstap
- **Resultaten van de Actie**: De status van het Succes/van de mislukking en uitvoeringsdetails
- **informatie van de Fout**: Gedetailleerde foutencodes en beschrijvingen wanneer de kwesties voorkomen

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

- Gebruik `journeyVersionID` in plaats van `journeyVersionName` voor betere queryprestaties
- Filter door datumwaaiers om vraagsnelheid op grote datasets te verbeteren
- Hefboomprofiel-id&#39;s die overeenkomen met de configuratie van de naamruimte van uw reis

**Kwaliteit van Gegevens**

- Regelmatig toezicht voor [&#x200B; verworpen gebeurtenissen &#x200B;](sharing-field-list.md#discarded-events) om gegevenskwesties te identificeren
- Valideer dat de gebeurtenisschema&#39;s uw analysevereisten aanpassen
- Correcte foutafhandeling implementeren in aangepaste query&#39;s

**Analysestrategieën**

- Gebeurtenissen voor de stap van de reis combineren met feedbackgegevens voor volledige toewijzing
- Gebruik tijdgebaseerde analyse om inzicht te krijgen in de snelheid van de reis en knelpunten
- Cohortanalyses maken om verschillende reisvariaties te vergelijken

### Geavanceerde analysemogelijkheden {#advanced-analytics}

**de integratie van Customer Journey Analytics**
Reisstapgebeurtenissen kunnen met Customer Journey Analytics worden geanalyseerd voor:

- Geavanceerde kenmerkmodellen
- Visualisatie van reizen tussen kanalen
- Predictieve analyse van reisresultaten

**Beslissing in real time**
Gebeurtenispatronen voor stap gebruiken voor:

- In real-time personalisatie activeren
- Dynamische optimalisatie van reizen implementeren
- Contextgebonden aanbevelingen voor de beste actie inschakelen

## Aanvullende bronnen {#additional-resources}

### Documentatiekoppelingen {#documentation-links}

- **[stap het delen van de Reis overzicht](sharing-overview.md)**: Begrijpend hoe de gegevens van de reis aan Adobe Experience Platform stromen
- **[Ingebouwd schemawoordenboek &#x200B;](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL)**: Volledige XDM schemaverwijzing
- **[Journey Optimizer die](report-gs-cja.md)** meldt: Overzicht van rapporteringsmogelijkheden in Journey Optimizer

### Integratiehulplijnen {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Het analyseren van de gegevens van Journey Optimizer in CJA
- **[het beheer van Gegevens](../data/export-datasets.md)**: Het uitvoeren van en het leiden van reisgegevens
- **[Privacy en bestuur](../privacy/audit-logs.md)**: De overwegingen van het bestuur van gegevens voor reisgebeurtenissen

Reisstapgebeurtenissen vormen de basis voor geavanceerde reisanalyses in Adobe Journey Optimizer. Door deze gebeurtenissen effectief te begrijpen en te gebruiken, kunt u diepgaande inzichten in klantengedrag bereiken, reisprestaties optimaliseren, en meer gepersonaliseerde ervaringen voor uw klanten creëren.
