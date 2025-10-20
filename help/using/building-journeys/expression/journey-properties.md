---
solution: Journey Optimizer
product: journey optimizer
title: Journeyeigenschappen
description: Meer informatie over reiseigenschappen
feature: Journeys
role: Engineer
level: Experienced
keywords: reis, expressie, editor, eigenschappen
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Eigenschappen voor reizen {#journey-properties}

In de [ eenvoudige uitdrukkingsredacteur ](../condition-activity.md#about_condition), en in de [ geavanceerde uitdrukkingsredacteur ](../expression/expressionadvanced.md), onder de **Gebeurtenis** en **Gegevensbron** categorieën, kunt u tot de **categorie van de Eigenschappen van de Reis** toegang hebben. Deze categorie bevat technische velden die verband houden met de reis voor een bepaald profiel. Dit is de informatie die door het systeem wordt opgehaald van levende reizen, zoals de reis-ID, of de specifieke fouten die worden aangetroffen.

![](../assets/journey-properties.png)

Het bevat bijvoorbeeld informatie over:

* reisversie: reisversie uid, reisversie uid, instance uid enz.
* fouten: gegevens ophalen, handelingen uitvoeren, enz.
* huidige stap, laatste huidige stap, enz.
* geneste profielen

  De lijst van gebieden is beschikbaar [ in deze sectie ](#journey-properties-fields).

U kunt deze velden gebruiken om expressies te maken. Tijdens de uitvoering van de reis worden de waarden direct van de reis opgehaald.

Hieronder volgen enkele voorbeelden van gebruiksgevallen:

* **Logboek verwierp profielen**: u kunt alle profielen verzenden die van een bericht door een afschilderingsregel aan een derdesysteem voor het registreren doeleinden worden uitgesloten. Hiervoor stelt u een pad in in het geval van een time-out en een fout en voegt u een voorwaarde toe om te filteren op een specifiek fouttype, bijvoorbeeld: &quot;Verwijder mensen door op de regel te tikken&quot;. U kunt de verwijderde profielen vervolgens via een aangepaste handeling naar een systeem van een andere fabrikant duwen.

* **verzendt alarm in het geval van fouten**: u kunt een bericht naar een derdesysteem verzenden telkens als een fout op een bericht voorkomt. Hiervoor stelt u een pad in in het geval van een fout, voegt u een voorwaarde en een aangepaste handeling toe. U kunt bijvoorbeeld een melding verzenden naar een Slack-kanaal met een beschrijving van de aangetroffen fout.

* **verfijnen fouten in het melden**: in plaats van het hebben van enkel één weg voor berichten in fout, kunt u een voorwaarde per foutentype bepalen. Hierdoor kunt u de rapportage verfijnen en alle gegevens van fouttypen weergeven.

## Lijst met velden {#journey-properties-fields}

| Categorie | Veldnaam | Label | Beschrijving |
|---|---|---|------------|
| Reisversie | tripUID | Reis-id | |
| | tripVersionUID | Reisversie-id | |
| | tripVersionName | Naam reisversie | |
| | tripVersionDescription | Beschrijving van reisversie | |
| | tripVersion | Reisversie | |
| Reisexemplaar | instanceUID | Reisexemplaar-id | ID van de instantie |
| | externalKey | Externe sleutel | Individuele identificatie die de reis veroorzaakt |
| | organisationId | Organisatie-id | Merkorganisatie |
| | sandboxName | Naam van sandbox | Naam van de sandbox |
| Identiteit | profileId | Identificatiecode profiel | Identificatiecode van het profiel tijdens de reis |
| | namespace | Naamruimte voor profielidentiteit | Naamruimte van het profiel in de rit (bijvoorbeeld: ECID) |
| Huidig knooppunt | currentNodeId | Huidige knooppunt-id | Identifier van de huidige activiteit (knooppunt) |
| | currentNodeName | Huidige knooppuntnaam | Naam van de huidige activiteit (knooppunt) |
| Vorig knooppunt | previousNodeId | Vorige knooppunt-id | Identifier van de vorige activiteit (knooppunt) |
| | previousNodeName | Vorige knooppunt naam | Naam van de vorige activiteit (knooppunt) |
| Fouten | lastNodeUIDInError | Laatste knooppunt-id in fout | Identifier van de laatste activiteit (knooppunt) in fout |
| | lastNodeNameInError | Laatste knooppuntnaam in fout | Naam van de laatste activiteit (knooppunt) in fout |
| | lastNodeTypeInError | Laatste knooppunttype in fout | Fouttype van de meest recente activiteit (knooppunt) in fout. Mogelijke typen:<ul><li>Gebeurtenissen: gebeurtenissen, reacties, SQ (bijvoorbeeld: kwalificatie als doelgroep)</li><li>Stroombeheer: Einde, Voorwaarde, Wacht</li><li>Handelingen: ACS-handelingen, Springen, Aangepaste handeling</li></ul> |
| | lastErrorCode | Laatste foutcode | Foutcode van de laatste activiteit (knooppunt) in fout. Mogelijke fouten: <ul><li>HTTP-foutcodes</li><li>afgetopt</li><li>timedOut</li><li>fout (voorbeeld: standaard in geval van een onverwachte fout. Dit mag niet of zeer zelden voorkomen.)</li></ul> |
| | lastExecutedActionErrorCode | Foutcode voor laatst uitgevoerde handeling | Foutcode van de laatste foutactie |
| | lastDataFetchErrorCode | Foutcode laatste gegevensophalen | Foutcode van de meest recente gegevensopname van gegevensbronnen |
| Tijd | lastActionExecutionElapsedTime | Uitvoeringstijd laatste handeling verstreken | Tijd besteed aan uitvoering van de laatste handeling |
| | lastDataFetchElapsedTime | Laatste ophalen gegevens verstreken tijd | Tijd besteed aan het uitvoeren van de nieuwste gegevensopname van gegevensbronnen |
