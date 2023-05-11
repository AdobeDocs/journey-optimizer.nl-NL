---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-instructies en beperkingen
description: Meer informatie over Journey Optimizer guardrails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#limitations}

De rechten, de productbeperkingen en de prestatiegaranties worden vermeld in [Adobe Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

U moet zich ook bewust zijn van [Gardrails voor gegevens in realtime klantprofiel voordat u begint](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html){target="_blank"}.

Hieronder vindt u aanvullende instructies en beperkingen bij het gebruik [!DNL Adobe Journey Optimizer].

## Ondersteunde browsers {#browsers}

Adobe [!DNL Journey Optimizer] -interface is ontworpen om optimaal te werken in de nieuwste versie van Google Chrome. Mogelijk kunt u problemen ondervinden bij het gebruik van bepaalde functies in oudere versies of andere browsers.

## Berichtgidsen {#message-guardrails}

* U kunt geen bijlagen aan een e-mailbericht toevoegen met [!DNL Journey Optimizer].
* U kunt niet hetzelfde verzendende domein gebruiken om berichten te verzenden van [!DNL Adobe Journey Optimizer] en van een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] bijvoorbeeld.


## Handleidingen voor landingspagina&#39;s {#lp-guardrails}

* Slechts één **Formulier** kan in één primaire pagina worden gebruikt.
* De **Formulier** kan niet worden gebruikt in subpagina&#39;s.
* U kunt geen preheader toevoegen aan een openingspagina.
* U kunt de **Uw eigen code schrijven** bij het ontwerpen van een primaire landingspagina.

## Reisgeleiders {#journeys-guardrails}

### Algemene reisgeleiders {#journeys-guardrails-journeys}

* Het aantal activiteiten op een reis is beperkt tot 50. Het aantal activiteiten wordt weergegeven in de linkerbovensectie van het reiscanvas.
* Het aantal **Levende reizen** in één organisatie geldt een limiet van 100 per sandbox. Wanneer deze limiet is bereikt, kunt u geen nieuwe rit meer publiceren.

### Algemene acties {#general-actions-g}

* Er is geen verzendvertraging.
* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht.
* De ingebouwde **Reactie** kunt u reageren op acties die buiten de box vallen. Meer informatie in [deze pagina](../building-journeys/reaction-events.md). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen.
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.
* Gewoonlijk kan een profiel niet meerdere keren op dezelfde reis tegelijk aanwezig zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet. [Meer informatie](../building-journeys/end-journey.md)

### Journeyversies {#journey-versions-g}

* Een reis die begint met een gebeurtenisactiviteit in v1 kan niet met iets anders beginnen dan een gebeurtenis in verdere versies. U kunt geen reis beginnen met een **Segmentkwalificatie** gebeurtenis.
* Een reis die begint met een **Segmentkwalificatie** activiteit in v1 moet altijd beginnen met een **Segmentkwalificatie** in verdere versies.
* Het segment en de naamruimte die zijn gekozen in **Segmentkwalificatie** (eerste knooppunt) kan niet worden gewijzigd in nieuwe versies.
* De re-entry regel moet het zelfde in alle reisversies zijn.
* Een reis die begint met een **Segment lezen** kan niet met een andere gebeurtenis in volgende versies beginnen.
* U kunt geen nieuwe versie van een read segment reis met stijgende lees tot stand brengen. Je moet de reis dupliceren.

### Aangepaste acties {#custom-actions-g}

* De URL van de aangepaste handeling ondersteunt geen dynamische parameters.
* Alleen methoden voor het aanroepen van POSTEN en PUTTEN worden ondersteund
* De naam van de queryparameter of -header mag niet beginnen met &quot;.&quot; of &quot;$&quot;
* IP-adressen zijn niet toegestaan
* Interne Adobe-adressen (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.
* Ingebouwde aangepaste handelingen kunnen niet worden verwijderd.

### Gebeurtenissen {#events-g}

* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.
* Zakelijke evenementen kunnen niet worden gebruikt in combinatie met eenheidsgebeurtenissen of segmentkwalificatieactiviteiten.
* Eenheidstrajecten (te beginnen met een evenement of segmentkwalificatie) bevatten een geleider die voorkomt dat ritten voor dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De terugkeer van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.
* Journey Optimizer vereist dat gebeurtenissen naar de Dienst van de Kern van de Gegevensverzameling (DCCS) worden gestroomd om een reis te kunnen teweegbrengen. Gebeurtenissen in batch of gebeurtenissen uit interne Journey Optimizer-gegevenssets (Berichtfeedback, E-mailtracking, enz.) kan niet worden gebruikt om een reis te starten. Als u gestreamde gebeurtenissen niet kunt ophalen, maakt u een segment op basis van deze gebeurtenissen en gebruikt u de optie **Segment lezen** in plaats daarvan. De segmentkwalificatie kan technisch worden gebruikt, maar kan stroomafwaartse uitdagingen veroorzaken die op de gebruikte acties worden gebaseerd.

### Gegevensbronnen {#data-sources-g}

* De externe gegevensbronnen kunnen binnen een klantenreis worden gebruikt om externe gegevens in echt op te zoeken - tijd. Deze bronnen moeten bruikbaar zijn via REST API, JSON ondersteunen en het volume van aanvragen kunnen verwerken.
* Interne Adobe-adressen (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.

### Reizen en profiel maken {#journeys-limitation-profile-creation}

Er is een vertraging verbonden aan het maken/bijwerken van een op API gebaseerd profiel in Adobe Experience Platform. Het doel van het Niveau van de Dienst (SLT) in termen van latentie is &lt; 1 min van opname aan Verenigd Profiel voor 95th percentiel van verzoeken, bij een volume van 20K Verzoeken per seconde (RPS).

Als een reis tezelfdertijd aan een profielverwezenlijking wordt teweeggebracht en onmiddellijk controleert/informatie van de Dienst van het Profiel terugwint, zou het niet behoorlijk kunnen werken.

U kunt uit één van deze twee oplossingen kiezen:

* Voeg een wachttijdactiviteit toe na de eerste gebeurtenis om Adobe Experience Platform de tijd te geven die nodig is om de opname naar de profielservice uit te voeren.

* Stel een reis in die niet onmiddellijk gebruikmaakt van het profiel. Als de reis bijvoorbeeld is ontworpen om het aanmaken van een account te bevestigen, kan de ervaringsgebeurtenis informatie bevatten die nodig is om het eerste bevestigingsbericht te verzenden (voornaam, achternaam, e-mailadres, enz.).

### Segment lezen {#read-segment-g}

* De stromen segmenten zijn altijd bijgewerkt maar de partijsegmenten zullen niet bij herwinningstijd worden berekend. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
* Voor ritten die een activiteit van het Leessegment gebruiken, is er een maximumaantal reizen dat op het nauwkeurige zelfde ogenblik kan beginnen. Het systeem voert de controles uit, maar vermijd dat meer dan vijf reizen (met Leessegment, gepland of &quot;zo snel mogelijk&quot; te starten) op hetzelfde tijdstip beginnen door ze over een bepaalde tijd te verspreiden, bijvoorbeeld 5 tot 10 minuten na elkaar.

### Expression-editor {#expression-editor}

* U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een Leessegment, een Segmentkwalificatie of een zakelijke gebeurtenisactiviteit. U moet een nieuw segment tot stand brengen en een insegmentvoorwaarde in de reis gebruiken.


