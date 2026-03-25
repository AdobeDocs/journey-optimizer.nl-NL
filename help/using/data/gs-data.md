---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevensbeheer in Journey Optimizer
description: Leer hoe gegevens vanuit en naar Adobe Journey Optimizer stromen, met inbegrip van zeer belangrijke concepten, opstellingsstappen, en gidsen.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ec952f64508618fa14d6f0eb16534209baa1a505
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---


# Aan de slag met gegevensbeheer {#about-data}

Gegevens vormen de basis voor elke reis, beslissing en boodschap die u met [!DNL Adobe Journey Optimizer] afgeeft.

Op deze pagina krijgt u een praktisch beginpunt voor begrip:

* De kernelementen voor gegevensopbouw die door Journey Optimizer worden gebruikt (schema&#39;s, datasets, identiteiten, profielen)
* Hoe Journey Optimizer Adobe Experience Platform-gegevens gebruikt
* Welke stappen van de gegevensopstelling uw team moet voltooien alvorens reizen en campagnes te bouwen
* Waar gaat u verder voor gedetailleerde configuratie en best practices

Gebruik deze handleiding samen met uw gegevenstechnici, beheerders en marketers, zodat iedereen een gemeenschappelijk beeld heeft van hoe gegevens in en uit Journey Optimizer stromen.

>[!TIP]
>Nieuw bij gegevensbeheer in Journey Optimizer? Bekijk het [&#x200B; overzicht van opstellingsgegevens leerprogramma &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} voor een praktische, begin-vriendschappelijke analyse van schema&#39;s, datasets, en bronnen.

## Hoe Journey Optimizer Adobe Experience Platform-gegevens gebruikt {#aep-data}

[!DNL Adobe Journey Optimizer] is gebaseerd op [!DNL Adobe Experience Platform] . Er wordt geen aparte, geïsoleerde gegevensopslag onderhouden. In plaats daarvan wordt dezelfde gegevensbasis gebruikt als andere Experience Cloud-toepassingen.

Schema&#39;s en datasets leven in Adobe Experience Platform. De identiteiten en het [&#x200B; Real-Time Profiel van de Klant &#x200B;](../audience/get-started-profiles.md) worden beheerd door de Dienst van de Identiteit en de Dienst van het Profiel. Journey Optimizer leest profiel- en gebeurtenisgegevens van Adobe Experience Platform om de reisomstandigheden te evalueren, berichten aan te passen en aanbiedingen te selecteren. Het schrijft interactiegegevens — zoals verzenden, openen, klikken, en stuitgebeurtenissen, en de gebeurtenissen van de reisstap — terug naar de datasets van Experience Platform. Het kan extra datasets bij runtime ook opzoeken zonder die gegevens in het profiel te kopiëren.

>[!TIP]
>Beschouw Adobe Experience Platform als uw centrale gegevenslaag en Journey Optimizer als een toepassing die reizen en berichten organiseert met behulp van die gedeelde gegevensbasis.

➡️ [&#x200B; Leer meer over de architectuur van Journey Optimizer &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Belangrijkste gegevensconcepten in Journey Optimizer {#key-concepts}

Wanneer u gegevens in Journey Optimizer gebruikt, zult u verschillende verwante concepten tegenkomen. In de onderstaande tabel vindt u een snel overzicht. In de volgende secties wordt elk concept gedetailleerder uitgelegd.

| Concept | Wat het is | Primair gebruik in Journey Optimizer |
|---|---|---|
| XDM-schema | Regels die uw gegevens vertegenwoordigen, valideren en opmaken (gebouwd uit een klasse + veldgroepen) | Modelprofielkenmerken en gedragsgebeurtenissen |
| Gegevensset | Opslagtabel voor gegevens die in overeenstemming zijn met een schema | Profiel, gebeurtenis en door het systeem gegenereerde gegevens bewaren |
| Source-connector | Streams of batches gegevens van externe systemen naar AEP | Ingest CRM, analytics en webgegevens |
| Gegevensbron | Hiermee worden AEP- of externe velden binnen reizen beschikbaar gemaakt | De reisvoorwaarden van de macht en berichtverpersoonlijking |
| Identiteit | Identificatiecode die uniek een individuele klant vertegenwoordigt | Profielen op kanalen plaatsen |
| Gegevensset opzoeken | Runtimeverwijzing naar AEP-gegevens zonder profielopslag | Berichten verrijken met live-referentiegegevens |

### Schema (XDM-schema) {#schema}

Een schema is een reeks regels die uw gegevens vertegenwoordigen, bevestigen en formatteren. Het bestaat uit a **klasse** (die het basisgedrag bepaalt: verslag of tijd-reeks) en facultatieve **gebiedsgroepen** (die specifieke gebieden toevoegen). De schema&#39;s worden bepaald gebruikend de normen van het Gegevensmodel van de Ervaring (XDM) en leven in Adobe Experience Platform.

XDM bestaat om een echt probleem op te lossen: het zelfde concept — een klant, een aankoop, een product — wordt genoemd en verschillend gestructureerd over bronsystemen. XDM verstrekt een gedeelde taal die deze concepten onder één enkele definitie verenigt, ongeacht waar de gegevens voortkomen. Dit is wat Journey Optimizer toestaat om met gegevens van uw CRM, uw website, uw mobiele app, en uw gegevenspakje tezelfdertijd te werken verenigbaar.

In Journey Optimizer, werkt u typisch met **XDM Individuele schema&#39;s van het Profiel** voor klantenattributen (naam, voorkeur, toestemming) en **XDM ExperienceEvent** schema&#39;s voor gedragsgebeurtenissen (aankopen, paginameningen, sign-ups).

➡️ [&#x200B; Leer meer over schema&#39;s &#x200B;](get-started-schemas.md)

### Gegevensset {#dataset}

Een dataset is een opslag en beheersconstructie voor gegevens die aan een schema in overeenstemming zijn — denk het als lijst met een bepaalde reeks kolommen en rijen. Alle gegevens die door Journey Optimizer worden gebruikt, worden opgeslagen in Adobe Experience Platform-gegevenssets. Dit kunnen profieldatasets zijn (die tot het Profiel van de Klant in real time bijdragen), gebeurtenisdatasets (die gedragsgegevens voor reizen en analyse opslaan), of systeemdatasets automatisch gecreeerd door Journey Optimizer voor het volgen, terugkoppelen, en de gebeurtenissen van de reisstap.

➡️ [&#x200B; Leer meer over datasets &#x200B;](get-started-datasets.md)

### Source-connector {#source-connector}

Een bronschakelaar (die ook als a **wordt bekend bron**) helpt u gegevens van veelvoudige systemen - zoals Adobe Analytics, het Web SDK van Adobe Experience Platform, wolkenopslag (S3, Azure Blob), of de gegevensbestanden van CRM - in Adobe Experience Platform innemen. Naast onbewerkte opname maken connectors het structureren, labelen en verbeteren van gegevens mogelijk met gebruik van Experience Platform-services, inclusief veldtoewijzing aan uw XDM-schema&#39;s en labels voor gegevensbeheer.

➡️ [&#x200B; Leer meer over bronschakelaars &#x200B;](../start/get-started-sources.md)

### Gegevensbron (Journey Optimizer) {#data-source}

Een gegevensbron in Journey Optimizer bepaalt welke velden van Adobe Experience Platform (of externe API&#39;s) worden weergegeven binnen reizen en berichten. Gegevensbronnen die in de gebruikersinterface van Journey Optimizer zijn geconfigureerd, omvatten doorgaans de ingebouwde Adobe Experience Platform-gegevensbron (die kenmerken en gebeurtenissen van het realtime-klantprofiel weergeeft) en optionele externe of aangepaste gegevensbronnen die tijdens de runtime van de reis worden aangeroepen voor extra verrijking. Zij worden gebruikt voor reisvoorwaarden, douaneacties, en berichtverpersoonlijking.

➡️ [&#x200B; Leer meer over gegevensbronnen &#x200B;](../datasource/about-data-sources.md)

>[!NOTE]
>De [&#x200B; Verklarende woordenlijst van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/glossary){target="_blank"} bepaalt &quot;gegevensbron&quot;algemeen als oorsprong van gegevens (een CRM, mobiele app, enz.). In Journey Optimizer, **gegevensbron** heeft een specifieke betekenis: een configuratie UI die controleert welke gebieden binnen reizen en berichten worden blootgesteld.

### Identiteit en realtime profiel van klant {#identity}

Een identiteit is een id die uniek een individuele klant vertegenwoordigt, zoals een cookie-id, apparaat-id, e-mailadres of CRM-id. Identiteiten zijn ingedeeld in naamruimten (e-mail, ECID, CRMID) en meerdere identiteiten voor dezelfde persoon zijn ondergebracht in een eengemaakte identiteitsgrafiek. In real time het Profiel van de Klant gebruikt die grafiek om een holistische mening van elke individuele klant te handhaven door gegevens van veelvoudige kanalen - met inbegrip van online, off-line, CRM, en derdebronnen te combineren.

Een zeer belangrijk concept voor beginners is het **profielfragment** model. Telkens wanneer een klant op een specifiek apparaat of kanaal — uw website, mobiele app, een winkel — met uw merk communiceert, wordt die interactie opgenomen als een profielfragment: een gedeeltelijke weergave van die klant op basis van dat specifieke aanraakpunt. In real-time profiel van de Klant hecht deze fragmenten voortdurend aan elkaar op basis van gedeelde identiteitswaarden en bouwt een volledig, up-to-date profiel. Journey Optimizer leest vanuit dit samengevoegde profiel om de voorwaarden te evalueren, aanbiedingen te selecteren en berichten in real-time aan te passen.

➡️ [&#x200B; Leer meer over identiteiten in Journey Optimizer &#x200B;](../audience/get-started-identity.md)

### Gegevensset opzoeken {#lookup-dataset}

Met een opzoekgegevensset kan Journey Optimizer referentie- of transactiegegevens bij uitvoering ophalen uit een Adobe Experience Platform-gegevensset, zonder die gegevens op te slaan in het realtime-klantprofiel. Dit is handig voor het vaak wijzigen van referentiegegevens (prijzen, voorraad, opslaguren) of transactiegegevens die op het moment van het bericht nodig zijn maar niet in het profiel horen. Journey Optimizer voert de zoekopdracht uit tijdens de reis of tijdens de berichtuitvoering op basis van een sleutel zoals een product-id.

➡️ [&#x200B; Leer meer over raadplegingsdatasets &#x200B;](lookup-aep-data.md)

## Controlelijst voor gereedheid van gegevens {#checklist}

Voordat marketers reizen en campagnes beginnen te maken, moet uw organisatie een reeks stappen voor de gereedheid voor gegevens uitvoeren. Dit zorgt ervoor dat Journey Optimizer de juiste gegevens op het juiste moment en op een compatibele manier kan gebruiken.

>[!NOTE]
>De stappen hieronder impliceren veelvoudige rollen: gegevensingenieurs, beheerders, en marketers. Gebruik deze checklist als gedeeld plan om uw milieu voor te bereiden. De stappen 1-4 worden voltooid in Adobe Experience Platform; de stappen 5-6 worden gevormd in Journey Optimizer.

### &#x200B;1. Definieer uw identiteitsstrategie {#identity-strategy}

Kies een primaire identiteit voor uw klanten (zoals ECID, e-mail, of CRMID) en configureer de bijbehorende naamruimten in Adobe Experience Platform Identity Service. Zorg ervoor dat er identiteitsvelden aanwezig zijn in uw schema&#39;s waarvoor profielen zijn ingeschakeld en controleer of de profielen op de juiste wijze zijn vastgezet in de identiteitsgrafiek.

➡️ [&#x200B; Leer meer over identiteiten in Journey Optimizer &#x200B;](../audience/get-started-identity.md)

### &#x200B;2. Ontwerpschema&#39;s voor profiel- en gebeurtenisgegevens {#design-schemas}

Creeer {de schema&#39;s 1} van het Profiel 1&rbrace; XDM Individueel om klantenattributen zoals naam en contactinformatie, voorkeur en interesses, en het stadium van de levenscyclus of toestemmingsstaat te vangen. **&#x200B;**&#x200B;Creeer **XDM ExperienceEvent** schema&#39;s om gedrags en transactionele gegevens zoals Web en app gebeurtenissen, aankopen, en off-line interactie te vangen. Markeer de juiste velden zo nodig als identiteiten en profielkenmerken.

➡️ [&#x200B; Leer meer over schema&#39;s &#x200B;](get-started-schemas.md)

### &#x200B;3. Gegevenssets maken die geschikt zijn voor profielen {#create-datasets}

In Adobe Experience Platform, creeer datasets die op uw XDM schema&#39;s worden gebaseerd en laat Profiel op om het even welke dataset toe die tot het Profiel van de Klant in real time zou moeten bijdragen. Bevestig dat de systeem-geproduceerde datasets die door Journey Optimizer worden gecreeerd in de werkruimte van Datasets zichtbaar zijn.

➡️ [&#x200B; Leer meer over datasets &#x200B;](get-started-datasets.md)

### &#x200B;4. Gegevens uit uw bronnen invoegen {#ingest-data}

Vorm bronschakelaars voor uw ondernemingssystemen — zoals Adobe Analytics, het Web SDK van Adobe Experience Platform, of uw platforms van CRM en POS — en kaart inkomende gebieden aan uw schema XDM. Valideer dat de gegevens in de correcte datasets en verschijnt in het Profiel van de Klant in real time waar verwacht.

➡️ [&#x200B; Leer meer over bronschakelaars &#x200B;](../start/get-started-sources.md)

➡️ [&#x200B; Leerprogramma: Creeer datasets en neem gegevens in &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

### &#x200B;5. Gegevensbronnen configureren in Journey Optimizer {#configure-data-sources}

Gegevensbronnen zijn een Journey Optimizer-specifiek concept: ze zijn niet waar uw gegevens zich bevinden, maar waar u aangeeft welke velden Journey Optimizer mag lezen tijdens de reis en tijdens de uitvoering van berichten. Voordat een reis een voorwaarde als &quot;is de klant een loyaliteitslid?&quot;kan evalueren of een bericht met een voornaam personaliseren, moeten de relevante profielgebieden door een gegevensbronconfiguratie worden blootgesteld.

Journey Optimizer omvat een ingebouwde [&#x200B; gegevensbron van Adobe Experience Platform &#x200B;](../datasource/adobe-experience-platform-data-source.md) die directe toegang tot de attributen van het Profiel van de Klant in real time geeft. Dit geldt voor het overgrote deel van de gevallen waarin gebruik wordt gemaakt: kenmerken van het leesprofiel voor personalisatie of controle van toestemmings- en voorkeursvelden. U kunt [&#x200B; externe gegevensbronnen &#x200B;](../datasource/external-data-sources.md) ook vormen om derde APIs bij reis runtime te roepen - bijvoorbeeld, om een loyaliteitsscore in real time, een productaanbeveling, of een niveau van de opslaginventaris terug te winnen dat niet in Adobe Experience Platform wordt opgeslagen.

>[!NOTE]
>Directe toegang tot gebeurtenisgegevens via de ingebouwde Adobe Experience Platform-gegevensbron is verouderd en wordt geleidelijk uitgeschakeld. [Meer info](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

Het vormen van gegevensbronnen is een administratieve taak die de volledige gegevenslaag voor reisauteurs en verkopers ontgrendelt. Zodra een gebied door een gegevensbron wordt blootgesteld, wordt het beschikbaar in de bouwer van de reisvoorwaarde, in de redacteurs van de berichtverpersoonlijking, en in aanbieding beslissingsregels - zonder extra ingenieurswerk bij reis-bouwt tijd te vereisen.

➡️ [&#x200B; Leer meer over gegevensbronconfiguratie &#x200B;](../datasource/about-data-sources.md)

### &#x200B;6. Verifieer het volgen, terugkoppel, en reis datasets {#verify-datasets}

Bevestig dat de systeem-geproduceerde datasets van Journey Optimizer beschikbaar in de werkruimte van Datasets zijn. Voer testreizen en -campagnes uit en gebruik vervolgens de Query Editor om te controleren of gebeurtenissen voor verzenden, openen, klikken en stuiteren zijn opgenomen en of gebeurtenissen en statussen voor de stap van de reis correct zijn vastgelegd. Gebruik deze datasets voor aan de gang zijnde controle, het oplossen van problemen, en reis optimalisering.

➡️ [&#x200B; Leer meer over vragen in Journey Optimizer &#x200B;](get-started-queries.md)

## Afbeeldingen en overwegingen voor gegevensontwerp {#guardrails}

Sommige productinstructies en beperkingen kunnen van invloed zijn op de manier waarop u uw gegevensmodel en reizen ontwerpt. Bekijk deze gegevens vroeg om later opnieuw te werken.

>[!IMPORTANT]
>Raadpleeg altijd de [&#x200B; Journey Optimizer guardrails en beperkingen &#x200B;](../start/guardrails.md) pagina voor de meest recente informatie. In de onderstaande samenvattingen worden belangrijke items gemarkeerd, maar deze kunnen zich in de loop der tijd ontwikkelen.

### Journey Optimizer-systeemgegevenssets en TTL {#datasets-ttl}

Journey Optimizer leidt tot verscheidene systeem-geproduceerde datasets voor het volgen, terugkoppelt, en de gebeurtenissen van de reisstap. Vanaf februari 2025, wordt een tijd-aan-levende (TTL) guardrail uitgerold aan sommige van deze datasets, die kan beïnvloeden hoe lang gegevens voor analyse en het oplossen van problemen worden bewaard.

➡️ [&#x200B; Leer meer over datasetTTL guardrails &#x200B;](datasets-ttl.md)

### Streaming segmentering en Journey Optimizer-gebeurtenissen {#streaming-segmentation}

Vanaf 1 november 2024 ondersteunt streaming segmentatie niet langer het verzenden en openen van gebeurtenissen van Journey Optimizer-tracking en het koppelen van gegevenssets. Voor gebruiksgevallen zoals frequentie het in kaart brengen en vermoeidheidsbeheer, gebruik [&#x200B; Bedrijfs Regels &#x200B;](../conflict-prioritization/rule-sets.md) in plaats van het stromen segmenten die op verzendt/open gebeurtenissen worden gebaseerd.

➡️ [&#x200B; Leer meer over datasets &#x200B;](get-started-datasets.md)

### Opzoeken en besluiten van gegevenssets {#lookup-guardrails}

Opzoeken van gegevenssets is ideaal voor veelvoorkomende wijzigingen in kenmerken (inventarisatie, prijsstelling, weer) of gegevens die niet in het realtime-klantprofiel hoeven te worden opgeslagen. Bekijk productspecifieke instructies zoals de limieten van de gegevenssetgrootte en queryuiteinden in de relevante documentatie voordat u de opzoekstrategie ontwerpt.

➡️ [&#x200B; Leer meer over raadplegingsdatasets &#x200B;](lookup-aep-data.md)

## Voorbeeld: gegevens voorbereiden voor een welkomstreis {#example}

In het volgende voorbeeld wordt getoond hoe de concepten op deze pagina in een eenvoudig scenario samenwerken.

1. Een gegevensingenieur leidt tot een [&#x200B; Afzonderlijk schema van het Profiel XDM &#x200B;](get-started-schemas.md) voor klantenattributen (naam, e-mail, loyaliteitrij, toestemming) en een schema XDM ExperienceEvent voor Web sign-up gebeurtenissen.
1. [&#x200B; profiel-toegelaten datasets &#x200B;](get-started-datasets.md) wordt gecreeerd voor elk schema: voor de attributen van CRM en voor sign-up gebeurtenissen.
1. Web en de mobiele teams stromen ondertekeningsgebeurtenissen via het Web SDK van Adobe Experience Platform; het gegeven van CRM wordt opgenomen via a [&#x200B; bronschakelaar &#x200B;](../start/get-started-sources.md).
1. Een beheerder vormt de [&#x200B; gegevensbron van Adobe Experience Platform &#x200B;](../datasource/adobe-experience-platform-data-source.md) in Journey Optimizer en stelt gebieden zoals `profile.person.name.firstName`, `profile.personalEmail.address`, en `profile.loyaltyTier` bloot.
1. Een telleraar [&#x200B; leidt tot een welkome reis &#x200B;](../building-journeys/journey-gs.md) die op een sign-up gebeurtenis luistert en die profielattributen gebruikt om [&#x200B; te personaliseren welkome e-mail &#x200B;](../personalization/personalize.md). Journey Optimizer schrijft verzend en open gebeurtenissen aan het volgen van datasets en registreert reisvooruitgang in de datasets van de de gebeurtenisgebeurtenis van de reisstap.
1. Een ontwikkelaar gebruikt [&#x200B; Redacteur van de Vraag &#x200B;](get-started-queries.md) om te verifiëren dat de gebeurtenissen correct stromen en prestaties (opent, klikt, tijd-te verzenden) analyseert. Het team past de reis en de inhoud aan op basis van deze inzichten.

Deze stroom illustreert hoe schema&#39;s, datasets, bronnen, gegevensbronnen, en vragen samenwerken in een volledig, beginnervriendelijk gebruiksgeval.

## Gerelateerde bronnen {#related-resources}

* **[krijgt begonnen met schema&#39;s](get-started-schemas.md)** - Leer hoe te om schema&#39;s XDM in Adobe Experience Platform tot stand te brengen, de juiste klasse en gebiedsgroepen te kiezen, en uw profielattributen en gedragsgebeurtenissen te modelleren.

* **[Werk met datasets](get-started-datasets.md)** — Begrijp hoe te om profiel-toegelaten en gebeurtenisdatasets tot stand te brengen, gegevensopname te controleren, en de systeem-geproduceerde datasets te onderzoeken die Journey Optimizer automatisch voor het volgen, terugkoppelt, en gebeurtenissen van de reisstap leidt.

* **[vormt gegevensbronnen](../datasource/about-data-sources.md)** - geleidelijke begeleiding bij vestiging de ingebouwde gegevensbron van Adobe Experience Platform en facultatieve externe gegevensbronnen om profielgebieden en externe API reacties binnen uw reizen bloot te stellen.

* **[gegevens van Adobe Experience Platform van het Gebruik (raadpleging)](lookup-aep-data.md)** - ontdek hoe te om berichten bij runtime met verwijzing of transactionele gegevens van de datasets van AEP te verrijken, zonder die gegevens op het Real-Time Profiel van de Klant op te slaan.

* **[krijgen begonnen met vragen](get-started-queries.md)** — de Dienst van de Vraag van het Gebruik om de datasets van Journey Optimizer te analyseren, te verifiëren dat de gebeurtenissen correct stromen, en het bouwen rapporteringsvragen bij verzenden, open, klikken, en stuitgegevens.

* **[krijgen begonnen met profielen](../audience/get-started-profiles.md)** — Onderzoek hoe het Profiel van de Klant in real time in Journey Optimizer werkt en hoe te, individuele klantenprofielen in het Platform UI doorbladeren inspecteren en bevestigen.

* **[het overzichtsleerprogramma van opstellingsgegevens &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}** - een begin-vriendschappelijke videoanalyse van gegevensopstelling in Journey Optimizer, die schema&#39;s, datasets, en bronnen behandelen beëindigen aan eind.

* **[creeer datasets en ingest gegevensleerprogramma &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}** - een hands-on leerprogramma dat toont hoe te om datasets in Adobe Experience Platform tot stand te brengen en gegevens in te voeren gebruikend bronschakelaars, met geleidelijke instructies u in uw eigen zandbak kunt volgen.
