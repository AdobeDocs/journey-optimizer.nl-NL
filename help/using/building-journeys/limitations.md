---
solution: Journey Optimizer
product: journey optimizer
title: Reisbeperkingen
description: Meer informatie over reisbeperkingen
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: reizen, beperking
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Beperkingen {#journey-limitations}

Hier zijn beperkingen met betrekking tot het gebruik van reizen.

## Algemene actiedrempels {#action-limitations}

* Er is geen verzendvertraging. 
* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht. 
* De ingebouwde **Reactie** -gebeurtenis kunt u reageren op acties die buiten de box vallen (zie deze [page](../building-journeys/reaction-events.md)). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen. 
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.

## Beperkingen van reisversies {#journey-versions-limitations}

* Een reis die begint met een gebeurtenisactiviteit in v1 kan niet met iets anders beginnen dan een gebeurtenis in verdere versies. U kunt geen reis beginnen met een **Poortkwalificatie** gebeurtenis.
* Een reis die begint met een **Poortkwalificatie** activiteit in v1 moet altijd beginnen met een **Poortkwalificatie** in verdere versies.
* Het publiek en de naamruimte die zijn gekozen in **Poortkwalificatie** (eerste knooppunt) kan niet worden gewijzigd in nieuwe versies.
* De re-entry regel moet het zelfde in alle reisversies zijn.
* Een reis die begint met een **Publiek lezen** kan niet met een andere gebeurtenis in volgende versies beginnen.

## Beperkingen voor aangepaste handelingen {#custom-actions-limitations}

* De URL van de aangepaste handeling ondersteunt geen dynamische parameters. 
* Alleen methoden voor het aanroepen van POSTEN en PUTTEN worden ondersteund. 
* De naam van de queryparameter of -header mag niet beginnen met &quot;.&quot; of &quot;$&quot;. 
* IP-adressen zijn niet toegestaan. 
* Interne Adobe-adressen (.adobe.) zijn niet toegestaan.

## Beperkingen voor gebeurtenissen {#events-limitations}

* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.

## Beperkingen op gegevensbronnen {#data-sources-limitations}

* De externe gegevensbronnen kunnen binnen een klantenreis worden gebruikt om externe gegevens in real time op te zoeken. Deze bronnen moeten bruikbaar zijn via REST API, JSON ondersteunen en het volume van aanvragen kunnen verwerken.

## Reizen die tegelijkertijd met het maken van een profiel beginnen {#journeys-limitation-profile-creation}

Er is een vertraging verbonden aan het maken/bijwerken van een op API gebaseerd profiel in Adobe Experience Platform. Het doel van het Niveau van de Dienst (SLT) in termen van latentie is &lt; 1 min van opname aan Verenigd Profiel voor 95th percentiel van verzoeken, bij een volume van 20K Verzoeken per seconde (RPS).

Als een Reis gelijktijdig aan een profielverwezenlijking wordt teweeggebracht en onmiddellijk controleert/informatie van de Dienst van het Profiel terugwint, zou het niet behoorlijk kunnen werken.

U kunt uit één van deze twee oplossingen kiezen:

* Voeg een wachttijdactiviteit toe na de eerste gebeurtenis om Adobe Experience Platform de tijd te geven die nodig is om de opname naar de profielservice uit te voeren.

* Stel een reis in die niet onmiddellijk gebruikmaakt van het profiel. Als de reis bijvoorbeeld is ontworpen om het maken van een account te bevestigen, kan de ervaringsgebeurtenis informatie bevatten die nodig is om het eerste bevestigingsbericht te verzenden (voornaam, achternaam, e-mailadres, enz.).

## Beperkingen van het publiek lezen {#read-audiences-limitations}

* Gestroomlijnde doelgroepen zijn altijd up-to-date, maar batchdoelgroepen worden niet berekend tijdens het ophalen. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
