---
solution: Journey Optimizer
product: journey optimizer
title: Lijst met gebeurtenisvelden voor stappen
description: Lijst met gebeurtenisvelden voor stappen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 12%

---

# Lijst met gebeurtenisvelden voor stappen {#sharing-field-list}

De gebeurtenisgebieden van de stap worden georganiseerd door categorie.

* Informatievelden voor foutopsporing
* Reisvelden
* Profielvelden
* Gebeurtenisvelden Service

## debugInfo {#debuginfo-field}

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| requestId | Tekenreeks | De aanvraag-id die Journey Optimizer gebruikt om de stroom van een aanvraag te volgen. |

## reis {#journey-field}

Deze veldgroep wordt gebruikt in het reisschema (met betrekking tot tripStepEvent). Het bevat de volgende velden:

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| Id | Tekenreeks | Identificatiecode voor de opgegeven reis |
| VersionID | Tekenreeks | Id van de reisversie. Deze id vertegenwoordigt de identiteit van een reis |
| name | Tekenreeks | Naam van de reis |
| beschrijving | Tekenreeks | Beschrijving van de reis |
| versie | Tekenreeks | versie, weergegeven als `major`.`minor` |

## profiel {#profile-field}

Deze veldgroep is specifiek voor tripStepEvent: Deze gebeurtenis is gerelateerd aan de rit en heeft niet de identityMap, waarin de eventuele profielidentiteit wordt beschreven.

Voor tripStepEvent, moeten wij gebieden met betrekking tot de identiteit ook toevoegen:

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| Id | Tekenreeks | De profiel-id identificeert het profiel dat tijdens een reis is verzonden/gebruikt. Bijvoorbeeld: foo@adobe.com. |
| namespace | Tekenreeks | In dit veld wordt de naamruimte beschreven waarnaar wordt verwezen door het profiel dat wordt gebruikt in Journey. Bijvoorbeeld: E-mail, ECID |

## serviceEvents {#servicevents-field}

Deze mix bevat alle velden die overeenkomen met een profielexporttaak.

| Veldnaam | Type | Beschrijving |
|---|---|------------|
| Id | Tekenreeks | De id van de doelexporttaak die wordt geactiveerd |
| status | Tekenreeks | De status van de doelexporttaak: in de wachtrij, gestart, voltooid |
| exportCountTotal | Geheel | De maximaal mogelijke waarde van de doelexporttaak |
| exportCountRealized | Geheel | Het werkelijke aantal soorten publiek dat via de taak is geëxporteerd |
| exportCountFailed | Geheel | Het aantal doelgroepen is mislukt tijdens het exporteren via de taak |
| exportSegmentID | Tekenreeks | De id van het publiek dat wordt geëxporteerd |
| eventType | Tekenreeks | Het gebeurtenistype dat aangeeft of het een foutgebeurtenis van een info-gebeurtenis is: Info, fout |
| eventCode | Tekenreeks | De foutcode die de reden voor het overeenkomende eventType aangeeft |

## stepEvents {#stepevents-field}

Deze categorie bevat de oorspronkelijke velden voor stapgebeurtenissen. Zie dit [sectie](../reports/sharing-legacy-fields.md).
