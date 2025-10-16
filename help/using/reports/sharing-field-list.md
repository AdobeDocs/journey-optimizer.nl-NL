---
solution: Journey Optimizer
product: journey optimizer
title: Lijst met gebeurtenisvelden voor stappen
description: Lijst met gebeurtenisvelden voor stappen
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: f9102c10aa58be0e1a7280aa53fd97b3f792b9e9
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 4%

---

# Lijst met gebeurtenisvelden voor stappen {#sharing-field-list}

De gebeurtenisgebieden van de stap worden georganiseerd door categorie.

* Informatievelden voor foutopsporing
* Reisvelden
* Profielvelden
* Gebeurtenisvelden Service

Voor het attribuut identityMap, wordt de primaire identiteit bepaald door gebrek als &quot;primair = waar&quot;.

## debugInfo {#debuginfo-field}

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| requestId | String | De aanvraag-id die Journey Optimizer gebruikt om de stroom van een aanvraag te volgen. |

## reis {#journey-field}

Deze veldgroep wordt gebruikt in het reisschema (met betrekking tot tripStepEvent). Het bevat de volgende velden:

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| ID | String | Identificatiecode voor de opgegeven reis |
| VersionID | String | Id van de reisversie. Deze id vertegenwoordigt de identiteit van een reis |
| name | String | Naam van de reis |
| beschrijving | String | Beschrijving van de reis |
| versie | String | versie, weergegeven als `major`.`minor` |

## profiel {#profile-field}

Deze veldgroep is specifiek voor tripStepEvent: deze gebeurtenis heeft betrekking op de reis en heeft niet de identityMap, die de profielidentiteit beschrijft, als om het even welk.

Voor tripStepEvent, moeten wij gebieden met betrekking tot de identiteit ook toevoegen:

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| ID | String | De profiel-id identificeert het profiel dat tijdens een reis is verzonden/gebruikt. Bijvoorbeeld: foo@adobe.com. |
| namespace | String | In dit veld wordt de naamruimte beschreven waarnaar wordt verwezen door het profiel dat wordt gebruikt in Journey. Bijvoorbeeld e-mail, ECID |

## serviceEvents {#servicevents-field}

Deze mix bevat alle velden die overeenkomen met een profielexporttaak.

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| ID | String | De id van de doelexporttaak die wordt geactiveerd |
| status | String | De status van de doelexporttaak: in de wachtrij, gestart, voltooid |
| exportCountTotal | Geheel | De maximaal mogelijke waarde van de doelexporttaak |
| exportCountRealized | Geheel | Het werkelijke aantal soorten publiek dat via de taak is geëxporteerd |
| exportCountFailed | Geheel | Het aantal doelgroepen is mislukt tijdens het exporteren via de taak |
| exportSegmentID | String | De id van het publiek dat wordt geëxporteerd |
| eventType | String | Het gebeurtenistype dat aangeeft of het een foutgebeurtenis of een info-gebeurtenis is: Info, Error |
| eventCode | String | De foutcode die de reden voor het overeenkomende eventType aangeeft |

Leer meer over eventTypes [&#x200B; in deze sectie &#x200B;](#discarded-events).

## stepEvents {#stepevents-field}

Deze categorie bevat de oorspronkelijke velden voor stapgebeurtenissen. Verwijs naar deze [&#x200B; sectie &#x200B;](../reports/sharing-legacy-fields.md).


## Los verworpen gebeurtenistypen in de gebeurtenissen van de stap van de Reis problemen op  {#discarded-events}

Bij het opvragen van gebeurtenissen met betrekking tot de stap van de reis naar records met `eventCode = 'discard'`, kan er een aantal eventTypes optreden.

Hieronder vindt u definities, algemene oorzaken en stappen voor het oplossen van problemen voor het meest voorkomende verwijderen `eventTypes` :

* EXTERNAL_KEY_COMPUTATION_ERROR: Het systeem kan geen unieke id (externe sleutel) voor de klant berekenen uit de gebeurtenisgegevens.

|---|---|
| **Gemeenschappelijke oorzaken** | Ontbrekende of misvormde klant-id&#39;s (bijvoorbeeld e-mail, klant-id) in de gebeurtenislading. |
| **Problemen oplossen** | Controleer de gebeurtenisconfiguratie op de vereiste id&#39;s, controleer of de gebeurtenisgegevens volledig en correct zijn opgemaakt. |

* NO_INTERESTED_JOURNEYS_FOR_SEGMENTMEMBERSHIP_EVENT: Er is een segmentkwalificatiegebeurtenis ontvangen, maar er zijn geen reizen geconfigureerd om op dit segment te reageren.


|---|---|
| **Gemeenschappelijke oorzaken** | Geen reizen gebruiken het segment als trekker, reizen zijn in ontwerp/gestopt staat, of segment IDs past niet aan. |
| **Problemen oplossen** | Verzeker minstens één reis levend is en voor het segment wordt gevormd, verifieer segment IDs. |

### JOURNEY_INSTANCE_ID_NOT_CREATE: Het systeem kon geen reisinstantie voor de klant maken.

|---|---|
| **Gemeenschappelijke oorzaken** | Dubbele gebeurtenissen, hoog gebeurtenisvolume, beperkingen van de systeembronnen. |
| **Problemen oplossen** | Implementeer deduplicatie, vermijd verkeerspikes, optimaliseer het reisontwerp, neem contact op met support als dit blijvend is. |

### EVENT_WITH_NO_JOURNEY: Er is een gebeurtenis ontvangen, maar er is geen actieve reis geconfigureerd om hierop te reageren

|---|---|
| **Gemeenschappelijke oorzaken** | Naam/id van gebeurtenis komt niet overeen, reis niet gepubliceerd, onjuiste sandbox/organisatie, testmodus/profiel komt niet overeen. |
| **Problemen oplossen** | Verifieer gebeurtenis en reisconfiguratie, controleer reisstatus, gebruik het zuiveren hulpmiddelen. |

Voor teruggooi tijdens gepauzeerde reizen:

* **PAUSED_JOURNEY_VERSION**: Keert die op het punt van reisingang voorkwamen
* **JOURNEY_IN_PAUSED_STATE**: Keert terug die gebeurde wanneer de profielen in een reis zijn

Leer meer over deze gebeurtenissen en hoe te om hen in [&#x200B; problemen op te lossen pauzeer een sectie van de Reis &#x200B;](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Aanvullende bronnen

* [&#x200B; de vraagsteekproeven van de Dataset - de Gebeurtenis van de Stap van de Reis &#x200B;](../data/datasets-query-examples.md#journey-step-event).
* [&#x200B; Voorbeelden van vragen - op gebeurtenis-gebaseerde Vragen &#x200B;](query-examples.md#event-based-queries).
* [&#x200B; Ingebouwd schemawoordenboek &#x200B;](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)

