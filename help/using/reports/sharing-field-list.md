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
source-git-commit: 97c1d0f2e9f8100f70d5c4e40325abddc5e3dfbd
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 3%

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

* **EXTERNAL_KEY_COMPUTATION_ERROR**: Het systeem kon een uniek herkenningsteken (externe sleutel) voor de klant van de gebeurtenisgegevens niet gegevens verwerken.
   * Veelvoorkomende oorzaken: ontbrekende of onjuist gevormde klant-id&#39;s (bijvoorbeeld e-mail, klant-id) in de gebeurtenislading.
   * Problemen oplossen: controleer de gebeurtenisconfiguratie op de vereiste id&#39;s en zorg ervoor dat de gebeurtenisgegevens volledig en correct zijn opgemaakt.
* **NO_INTERESTED_JOURNEYS_FOR_SEGMENTMEMBERSHIP_EVENT**: Een gebeurtenis van de segmentkwalificatie werd ontvangen, maar geen reizen worden gevormd om op dit segment te antwoorden.
   * Veelvoorkomende oorzaken: geen reizen gebruiken het segment als trigger, reizen bevinden zich in concept/stopstatus of segmenten-id&#39;s komen niet overeen.
   * Het oplossen van problemen: Verzeker minstens één reis levend is en voor het segment gevormd, verifieer segment IDs.
* **JOURNEY_INSTANCE_ID_NOT_CREATE**: Het systeem slaagde er niet in om een reisinstantie voor de klant tot stand te brengen.
   * Veelvoorkomende oorzaken: dubbele gebeurtenissen, hoog gebeurtenisvolume, beperkingen aan systeembronnen.
   * Problemen oplossen: deduplicatie implementeren, verkeersspikes vermijden, reisontwerp optimaliseren, contact opnemen met ondersteuning als dit blijvend is.
* **EVENT_WITH_NO_JOURNEY**: Een gebeurtenis werd ontvangen maar geen actieve reis wordt gevormd om aan het te antwoorden.
   * Veelvoorkomende oorzaken: naam/id van gebeurtenis komen niet overeen, reis niet gepubliceerd, verkeerde sandbox/organisatie, testmodus/profiel komen niet overeen.
   * Problemen oplossen: controleer de configuratie van gebeurtenissen en reizen, controleer de status van de reis en gebruik de tools voor foutopsporing.

Voor teruggooi tijdens gepauzeerde reizen:

* **PAUSED_JOURNEY_VERSION**: Keert die op het punt van reisingang voorkwamen
* **JOURNEY_IN_PAUSED_STATE**: Keert terug die gebeurde wanneer de profielen in een reis zijn

Leer meer over deze gebeurtenissen en hoe te om hen in [&#x200B; problemen op te lossen pauzeer een sectie van de Reis &#x200B;](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Aanvullende bronnen

* [&#x200B; de vraagsteekproeven van de Dataset - de Gebeurtenis van de Stap van de Reis &#x200B;](../data/datasets-query-examples.md#journey-step-event).
* [&#x200B; Voorbeelden van vragen - op gebeurtenis-gebaseerde Vragen &#x200B;](query-examples.md#event-based-queries).
* [&#x200B; Ingebouwd schemawoordenboek &#x200B;](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL)

