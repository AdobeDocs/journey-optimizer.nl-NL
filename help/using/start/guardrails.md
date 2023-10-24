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
source-git-commit: 59693650e3745471729a2d37998d6622a1a3c521
workflow-type: tm+mt
source-wordcount: '1646'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#limitations}

De rechten, de productbeperkingen en de prestatiegaranties worden vermeld in [Adobe Journey Optimizer-productbeschrijvingspagina](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

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

* Het aantal activiteiten op een reis is beperkt tot 50. Het aantal activiteiten wordt weergegeven in de linkerbovensectie van het reiscanvas. Dit zal helpen in leesbaarheid, QA en het oplossen van problemen.
* Tijdens het publiceren van reizen worden de schaal en de stabiliteit automatisch aangepast om een maximale doorvoer en stabiliteit te garanderen. Aangezien u dichtbij de mijlpaal van 100 levende reizen in één keer, zult u een bericht over deze verwezenlijking zien verschijnen in UI. Als u deze melding ziet en uw reizen moet verlengen tot meer dan 100 rechtstreekse reizen tegelijk, maak dan een ticket voor de klantenservice en wij helpen u uw doelstellingen te bereiken.
* Wanneer u een publiekskwalificatie gebruikt op een reis, kan het tot 10 minuten duren voordat de activiteit van de publiekskwalificatie actief is en naar profielen luistert die het publiek binnenkomen of verlaten.

### Algemene acties {#general-actions-g}

* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht. Retries wordt uitgevoerd voor alle HTTP-fouten, behalve voor HTTP 401, 403 en 404.
* De ingebouwde **Reactie** kunt u reageren op acties die buiten de box vallen. Meer informatie in [deze pagina](../building-journeys/reaction-events.md). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen.
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.
* Een profiel kan niet meerdere keren op dezelfde reis tegelijk aanwezig zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet. [Meer informatie](../building-journeys/end-journey.md)

### Journeyversies {#journey-versions-g}

* Een reis die begint met een gebeurtenisactiviteit in v1 kan niet met iets anders beginnen dan een gebeurtenis in verdere versies. U kunt geen reis beginnen met een **Poortkwalificatie** gebeurtenis.
* Een reis die begint met een **Poortkwalificatie** activiteit in v1 moet altijd beginnen met een **Poortkwalificatie** in verdere versies.
* Het publiek en de naamruimte die zijn gekozen in **Poortkwalificatie** (eerste knooppunt) kan niet worden gewijzigd in nieuwe versies.
* De re-entry regel moet het zelfde in alle reisversies zijn.
* Een reis die begint met een **Publiek lezen** kan niet met een andere gebeurtenis in volgende versies beginnen.
* U kunt geen nieuwe versie maken van een leestoegang met incrementeel lezen. Je moet de reis dupliceren.

### Aangepaste acties {#custom-actions-g}

* Voor alle aangepaste handelingen wordt een begrenzingslimiet van 150.000 aanroepen over 30 seconden gedefinieerd. Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. U moet hiermee rekening houden bij reizen voor uw publiek door een juiste leessnelheid te definiëren (5000 profielen/s wanneer aangepaste handelingen worden gebruikt). Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen. Zie [deze pagina](../configuration/external-systems.md).
* De URL van de aangepaste handeling ondersteunt geen dynamische parameters.
* Methoden voor POST, PUT en GET worden ondersteund
* De naam van de queryparameter of -header mag niet beginnen met &quot;.&quot; of &quot;$&quot;
* IP-adressen zijn niet toegestaan
* Interne adressen van Adoben (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.
* Ingebouwde aangepaste handelingen kunnen niet worden verwijderd.

### Gebeurtenissen {#events-g}

* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.
* Zakelijke evenementen kunnen niet worden gebruikt in combinatie met monitaire evenementen of kwalificatieactiviteiten voor het publiek.
* Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De terugkeer van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.
* Journey Optimizer vereist dat gebeurtenissen worden gestreamd naar Data Collection Core Service (DCCS) om een reis te kunnen activeren. Gebeurtenissen in batch of gebeurtenissen uit interne Journey Optimizer-gegevenssets (Berichtfeedback, E-mailtracking, enz.) kan niet worden gebruikt om een reis te starten. Als u gestreamde gebeurtenissen niet kunt ophalen, maakt u een publiek op basis van deze gebeurtenissen en gebruikt u de optie **Publiek lezen** in plaats daarvan. De kwalificatie van het publiek kan technisch worden gebruikt, maar kan stroomafwaartse uitdagingen veroorzaken die op de gebruikte acties worden gebaseerd.

### Gegevensbronnen {#data-sources-g}

* De externe gegevensbronnen kunnen binnen een klantenreis worden gebruikt om externe gegevens in echt op te zoeken - tijd. Deze bronnen moeten bruikbaar zijn via REST API, JSON ondersteunen en het volume van aanvragen kunnen verwerken.
* Interne adressen van Adoben (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.

### Reizen en profiel maken {#journeys-limitation-profile-creation}

Er is een vertraging verbonden aan het maken/bijwerken van een op API gebaseerd profiel in Adobe Experience Platform. Het doel van het Niveau van de Dienst (SLT) in termen van latentie is &lt; 1 min van opname aan Verenigd Profiel voor 95th percentiel van verzoeken, bij een volume van 20K Verzoeken per seconde (RPS).

Als een reis gelijktijdig aan een profielverwezenlijking wordt teweeggebracht en onmiddellijk controleert/informatie van de Dienst van het Profiel terugwint, zou het niet behoorlijk kunnen werken.

U kunt uit één van deze twee oplossingen kiezen:

* Voeg een wachttijdactiviteit toe na de eerste gebeurtenis om Adobe Experience Platform de tijd te geven die nodig is om de opname naar de profielservice uit te voeren.

* Stel een reis in die niet onmiddellijk gebruikmaakt van het profiel. Als de reis bijvoorbeeld is ontworpen om het aanmaken van een account te bevestigen, kan de ervaringsgebeurtenis informatie bevatten die nodig is om het eerste bevestigingsbericht te verzenden (voornaam, achternaam, e-mailadres, enz.).

### Doelgroep lezen {#read-segment-g}

* Gestroomlijnde doelgroepen zijn altijd up-to-date, maar batchdoelgroepen worden niet berekend tijdens het ophalen. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
* Voor reizen die gebruikmaken van een activiteit van het leespubliek is er een maximumaantal reizen dat precies op hetzelfde moment kan beginnen. Het systeem zal tests uitvoeren, maar u moet vermijden dat meer dan vijf reizen (met Leespubliek, gepland of &quot;zo snel mogelijk&quot; te starten) op precies hetzelfde tijdstip beginnen door deze over een bepaalde tijd te verspreiden, bijvoorbeeld 5 tot 10 minuten uit elkaar.

### Expression-editor {#expression-editor}

* U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een leespubliek, een kwalificatie Audience of een activiteit voor een zakelijke gebeurtenis. Je moet een nieuw publiek maken en een onpublieksvoorwaarde in de reis gebruiken.


### Beperkingen van activiteiten in de app {#in-app-activity-limitations}

* Deze functie is momenteel niet beschikbaar voor klanten in de gezondheidszorg.

* Personalisatie kan alleen profielkenmerken bevatten.

* De weergave in de app is gekoppeld aan de duur van de rit. Dit houdt in dat wanneer de reis voor een profiel afloopt, alle in-app-berichten binnen die reis niet meer worden weergegeven voor dat profiel.  Het is daarom niet mogelijk om een bericht in de app rechtstreeks te stoppen van een reisactiviteit. In plaats daarvan moet u de volledige reis beëindigen om te voorkomen dat de berichten in de app naar het profiel worden weergegeven.

* In de testmodus is de weergave in de app afhankelijk van de levensduur van de rit. Om te voorkomen dat de reis te vroeg eindigt tijdens de test, past u de **[!UICONTROL Wait time]** waarde voor uw **[!UICONTROL Wait]** activiteiten.

* **[!UICONTROL Reaction]** activiteiten kunnen niet worden gebruikt om te reageren op een geopende In-app of klik.

* Er kan een activeringsvertraging optreden tussen het moment dat een gebruikersprofiel een in-app-activiteit op het canvas bereikt en het moment waarop het bericht in de app wordt weergegeven.

* De inhoud van berichten in de app is beperkt tot 2 MB. Het opnemen van grote afbeeldingen kan het publicatieproces belemmeren.

## Audiëntenguardrails {#audience}

* U kunt maximaal 10 publiekscomposities in een bepaalde sandbox publiceren. Als u deze drempel hebt bereikt, moet u een samenstelling schrappen om ruimte vrij te maken en nieuwe te publiceren.

## Garanties voor besluitvormingsbeheer {#decision-management}

### Prestatiegerichten {#performance-guardrails}

De leveringstijd komt overeen met het aantal beslissingsreacties dat binnen een bepaalde tijd door de app-service van het beslissingsbeheer kan worden geleverd. Het aantal besluiten per seconde wordt in onderstaande tabel aangegeven.

| API | Besluiten per seconde |
|---------|----------|
| API-aanvragen voor besluitvorming | 500 per seconde |
| Aanvragen voor Edge-API voor besluitvorming | 5000 per seconde |

### Beperkingen {#offers-limitations}

De beperkingen van het besluitvormingsbeheer worden hieronder vermeld.

* **Goedgekeurde persoonlijke aanbiedingen + alternatieven** - Tot 10.000 gecombineerde goedgekeurde persoonlijke aanbiedingen en goedgekeurde alternatieven.
* **Besluiten** - Tot 10.000 besluiten.
* **Live beslissingen** - Offer decisioning App Service ondersteunt maximaal 1.000 Live-beslissingen.
* **Per reactie geretourneerde voorstellen** - Offer decisioning ondersteunt maximaal 100 aanbiedingen die per aanvraag worden teruggestuurd over alle besluitvormingsgebieden in aanvraag.
* **Verzamelingen** - Tot 10.000 verzamelingen.
* **Verzamelingen per beslissing** - Tot 30 verzamelingen per beslissing.
* **Beslissingsregels + rangschikkingsfuncties** Tot 10.000 gecombineerde besluitvormingsregels en rangordefuncties.
* **Plaatsen** - Tot 1.000 Plaatsen.
* **Plaatsingen per besluit** - Tot 30 plaatsen per besluit.
* **Beoordelingsmethode per besluit** - Offer decisioning App Service ondersteunt maximaal 30 ranking-functies per besluit.
* **AI-beoordelingsmodel** - Offer decisioning App Service ondersteunt maximaal vijf AI-waarderingsmodellen.
* **Verzamelingskwalificatie per aanbieding of verzameling** - Offer decisioning App Service biedt ondersteuning voor maximaal 20 verzamelingskwalificatie in één persoonlijke aanbieding of enkele verzameling.
* **Totaal aantal verzamelingskwalificaties** - Offer decisioning App Service ondersteunt maximaal 1.000 Collectieve Kwalificatoren.