---
title: Journey Optimizer-instructies en beperkingen
description: Meer informatie over Journey Optimizer guardrails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 80a5edec92377753e6bfd96699591b1a87e25248
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#limitations}

De rechten, de productbeperkingen en de prestatiegaranties worden vermeld in [Adobe Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Hieronder vindt u aanvullende instructies en beperkingen bij het gebruik [!DNL Adobe Journey Optimizer].

## Berichtgidsen {#message-guardrails}

* U kunt geen bijlagen aan een e-mailbericht toevoegen met [!DNL Journey Optimizer].
* U kunt niet hetzelfde verzendende domein gebruiken om berichten te verzenden van [!DNL Adobe Journey Optimizer] en van een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] bijvoorbeeld.


## Garanties voor besluitvormingsbeheer {#offer-guardrails}

Prestatiegerichten en statische limieten voor het besluitvormingsbeheer worden vermeld in de [Adobe Offer decisioning App Service, productbeschrijvingspagina](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Handleidingen voor landingspagina&#39;s {#lp-guardrails}

* Slechts één **Formulier** kan in één primaire pagina worden gebruikt.
* De **Formulier** kan niet worden gebruikt in subpagina&#39;s.
* U kunt geen preheader toevoegen aan een openingspagina.
* U kunt de **Uw eigen code schrijven** bij het ontwerpen van een primaire landingspagina.

## Reisgeleiders {#journeys-guardrails}

### Algemene acties {#general-actions-g}

* Er is geen verzendvertraging.
* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht.
* De ingebouwde **Reactie** kunt u reageren op acties die buiten de box vallen. Meer informatie in [deze pagina](../building-journeys/reaction-events.md). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen.
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.
* Er is vandaag de dag een technische beperking in de ritten die een profiel verhindert om meerdere keren aanwezig te zijn op dezelfde reis, tegelijkertijd. Een profiel kan een reis (gebaseerd op een het plaatsen) nog opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet.
* In de meeste gevallen kan een profiel niet meerdere keren tegelijk op dezelfde reis aanwezig zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet. [Meer informatie](../building-journeys/journey-end.md)

### Berichthandeling {#message-action-g}

* Wanneer u een multikanaalbericht toevoegt, worden twee berichten verzonden.

### Journeyversies {#journey-versions-g}

* Een reis die begint met een gebeurtenisactiviteit in v1 kan niet met iets anders beginnen dan een gebeurtenis in verdere versies. U kunt geen reis beginnen met een **Segmentkwalificatie** gebeurtenis.
* Een reis die begint met een **Segmentkwalificatie** activiteit in v1 moet altijd beginnen met een **Segmentkwalificatie** in verdere versies.
* Het segment en de naamruimte die zijn gekozen in **Segmentkwalificatie** (eerste knooppunt) kan niet worden gewijzigd in nieuwe versies.
* De re-entry regel moet het zelfde in alle reisversies zijn.
* Een reis die begint met een **Segment lezen** kan niet met een andere gebeurtenis in volgende versies beginnen.

### Aangepaste acties {#custom-actions-g}

* De URL van de aangepaste handeling ondersteunt geen dynamische parameters.
* Alleen methoden voor het aanroepen van POSTEN en PUTTEN worden ondersteund
* De naam van de queryparameter of -header mag niet beginnen met &quot;.&quot; of &quot;$&quot;
* IP-adressen zijn niet toegestaan
* Interne Adobe-adressen (.adobe.) zijn niet toegestaan.

### Gebeurtenissen {#events-g}

* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.

### Gegevensbronnen {#data-sources-g}

* De externe gegevensbronnen kunnen binnen een klantenreis worden gebruikt om externe gegevens in echt op te zoeken - tijd. Deze bronnen moeten bruikbaar zijn via REST API, JSON ondersteunen en het volume van aanvragen kunnen verwerken.

### Reizen en profiel maken {#journeys-limitation-profile-creation}

Er is een vertraging verbonden aan het maken/bijwerken van een op API gebaseerd profiel in Adobe Experience Platform. Het doel van het Niveau van de Dienst (SLT) in termen van latentie is &lt; 1 min van opname aan Verenigd Profiel voor 95th percentiel van verzoeken, bij een volume van 20K Verzoeken per seconde (RPS).

Als een reis tezelfdertijd aan een profielverwezenlijking wordt teweeggebracht en onmiddellijk controleert/informatie van de Dienst van het Profiel terugwint, zou het niet behoorlijk kunnen werken.

U kunt uit één van deze twee oplossingen kiezen:

* Voeg een wachttijdactiviteit toe na de eerste gebeurtenis om Adobe Experience Platform de tijd te geven die nodig is om de opname naar de profielservice uit te voeren.

* Stel een reis in die niet onmiddellijk gebruikmaakt van het profiel. Als de reis bijvoorbeeld is ontworpen om het aanmaken van een account te bevestigen, kan de ervaringsgebeurtenis informatie bevatten die nodig is om het eerste bevestigingsbericht te verzenden (voornaam, achternaam, e-mailadres, enz.).

### Segment lezen {#read-segment-g}

* De stromen segmenten zijn altijd bijgewerkt maar de partijsegmenten zullen niet bij herwinningstijd worden berekend. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
