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
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 6%

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

Deze veldgroep is specifiek voor tripStepEvent: deze gebeurtenis heeft betrekking op de reis en heeft niet de identityMap, die de profielidentiteit beschrijft, indien aanwezig.

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
| eventType | String | Het gebeurtenistype dat aangeeft of het een foutgebeurtenis in de info-gebeurtenis is: Info, Error |
| eventCode | String | De foutcode die de reden voor het overeenkomende eventType aangeeft |

## stepEvents {#stepevents-field}

Deze categorie bevat de oorspronkelijke velden voor stapgebeurtenissen. Zie dit [sectie](../reports/sharing-legacy-fields.md).
