---
solution: Journey Optimizer
product: journey optimizer
title: Geordende campagnes Veelgestelde vragen
description: Veelgestelde vragen over door Journey Optimizer georganiseerde campagnes
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 1%

---

# Veelgestelde vragen {#faq-oc}

Hieronder vindt u Veelgestelde vragen over door Adobe Journey Optimizer geordende campagnes.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [ gemeenschap van Adobe Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

+++ Wat is campagneorkest?

Campagne Orchestration is een eigenschap van Journey Optimizer die enige-stap of multi-step werkschema&#39;s steunt die hefboomwerking de Relationele Datastore om publiek voor het doel van partijovereenkomst te bouwen en te segmenteren.

Het brengt een nieuw type van campagnes aan Journey Optimizer: **Geordende campagnes**. Geordende campagnes helpen merken complexe, één-op-veel marketingcampagnes op schaal uit te voeren. Ze zijn ontworpen voor door het merk geïnitieerde betrokkenheid, zoals promoties, seizoenscampagnes of communicatie op basis van account.

Vergeleken met single-send/actiecampagnes, brengen zij **orchestratie en het rangschikken** aan uitgaande marketing: de kijkcijfers bewegen zich door een multi-step werkschema samen, eerder dan het ontvangen van een eenmalig blaast.

+++

+++ Wat kan ik doen met een geordende campagne?

De belangrijkste mogelijkheden omvatten:

* **publiek op bestelling**: bouw en verfijnen direct doelgroepen gebruikend relationele vragen.
* **Segmentatie van meerdere entiteiten**: Creeer nauwkeurige publiek door klantengegevens met verwante entiteiten (b.v., rekeningen, aankopen, boeken) aan te sluiten.
* **pre-Send Zichtbaarheid**: Zie nauwkeurige publiekscijfers alvorens lanceren om het richten te optimaliseren.
* **MultiStep Workflows**: De gesequeneerde campagnes van de looppas zoals seizoensgebonden bevorderingen, productlanceringen, of loyaliteitsaanbiedingen.

**Best practices**

* Bepaal a **duidelijke campagnedoelstelling** alvorens werkschema&#39;s te ontwerpen.
* Begin met a **proefpubliek** om tellingen en logica vóór het schrapen te bevestigen.
* Houd segmenteringsregels **zo eenvoudig mogelijk** om prestaties en transparantie te optimaliseren.
* Gebruik **verenigbare noemende overeenkomsten** voor publiek en campagnes om beheer gemakkelijker te maken.

+++

+++ Hoe toegang te krijgen tot Campagneorchestratie?

Om tot Campagneorganisatie toegang te hebben, moet uw vergunning of de **Journey Optimizer - Campagnes &amp; Reizen** of **Journey Optimizer - het pakket van Campagnes** omvatten. Neem contact op met uw Adobe-vertegenwoordiger om uw licentie te bevestigen en indien nodig bij te werken.

Leer meer over het verlenen van vergunningen van het Organiseren van de Campagne model in [ Adobe Journey Optimizer productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++ Hoe zijn geordende campagnes anders dan Reizen?

* **Geordende campagnes**: Best voor **partij, één-aan-vele** campagnes. De vooruitgang van het publiek in bulk, op een programma.
* **Reizen**: Best voor **real time, één-aan-één** overeenkomst. Elke klant beweegt zich door de reis in hun eigen tempo, die door gedrag of gebeurtenissen wordt teweeggebracht.

**Beste praktijken**: Gebruik hen samen — Reizen voor teweeggebrachte, reactieve ervaringen, en Geordende Campagnes voor geplande, op kalender-gebaseerde initiatieven.


+++

+++ Wat is segmentatie van meerdere entiteiten?

Campagne Orchestration in Adobe Journey Optimizer gebruikt een relationele database. Dit type van gegevensmodel heeft afzonderlijke schema&#39;s van gegevens die via 1 :1 of 1 :many verhoudingen worden verbonden. Dit laat gebruikers toe om een vraag op om het even welk schema te beginnen - niet alleen op ontvankelijk niveau - en dan terug en uit te keren naar andere verwante regelingen, zoals aankopen, producten, boeken of ontvankelijke details die grote flexibiliteit in verstrekken hoe de segmenten en het publiek kunnen worden gecreeerd en
verfijnd.


**Voorbeeld** - richt alle ontvangers met abonnementen die in de volgende 30 dagen verlopen. In Campagneorganisatie kan de vraag met het schema van Abonnementen beginnen, enkel de kolom van de vervaldatum van dat schema zoeken en alle abonnementen terugkeren toe te schrijven aan verlopen, dan rol omhoog aan de ontvankelijke gegevens die met die specifieke abonnementen IDs verwant zijn die resultaten sneller en efficiënter terugkeren dan gegevensmodellen die met elke vraag op het ontvankelijke niveau beginnen.

+++

+++ Hoe werkt het gegevensmodel?

De campagnes gebruiken a **relationele gegevensbestand**. Hierdoor kunt u query&#39;s uitvoeren op verschillende gegevenssets (zoals klanten, producten, abonnementen) en deze op flexibele wijze verbinden voor geavanceerde segmentatie.

**Best practices**

* Organiseer datasets zodat **verhoudingen (treedt toe)** bedrijfslogica weerspiegelen.
* Vermijd onnodige verbindingen om query&#39;s uitvoerbaar te houden.
* Valideer de monsterresultaten voordat u grootschalige extracties uitvoert.


+++

+++ Kan ik berichten met relationele gegevens personaliseren?

Ja. In Campagne Orchestration kan een ontvankelijk profiel dat als &quot;Entiteit van Mensen&quot;wordt bekend worden bijgewerkt en dat gegeven voor verpersoonlijking wordt gebruikt. Daarnaast kunnen verrijkte gegevens van gekoppelde entiteiten in de relationele database ook worden gebruikt voor personalisatie. U kunt de profielen van de klant samen met verbonden gegevens (zoals aankopen of abonnementen) gebruiken om inhoud over alle gesteunde kanalen te personaliseren.


**Aanbevelingen**

* Het gebruik **transactie en gedragsgegevens** om aanbiedingen relevant te maken.
* Combineer **statische attributen** (b.v., loyaliteitrij) met **dynamische degenen** (b.v., laatste aankoopdatum).
* Houd personalisatie beknopt: het overladen van berichten met gegevens kan de leesbaarheid schaden.


+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Welke kanalen worden gesteund?

U kunt Geordende campagnes tot stand brengen om **e-mails**, **SMS**, en **dupberichten** te verzenden.

+++

+++ Kunnen meerdere communicaties en verschillende kanalen worden gelanceerd binnen dezelfde geordende campagne?

Ja, geordende campagnes ondersteunen kanaalorkestorkest.

+++

+++ Zijn de geordende campagnemalplaatjes beschikbaar?

Nr, kunt u campagnemalplaatjes niet bepalen of gebruiken, maar u kunt inhoudsmalplaatjes voor uw mededelingen gebruiken.

+++

+++ Is de inhoudsontwerper voor berichten specifiek voor Geordende campagnes?

Nee, de inhoudsontwerper, inclusief de e-mail-Designer, is overal in Journey Optimizer beschikbaar.

+++

+++ Hoe zijn de verschillende kanalen verbonden in geordende campagnes?

De component en runtime van het kanaal worden gebruikt voor alle Journey Optimizer-campagnes, maar de ondersteunde kanalen verschillen.

+++


+++ Kunnen geordende campagnes verbinding maken met uitgaande kanalen (web, inApp)?

Nee, uitgaande kanalen worden niet ondersteund in geordende campagnes.

+++

+++ Hoe zit het met machtigingen en toestemming?

Machtigingen en toestemming voor geordende campagnes en reizen worden centraal beheerd in Adobe Experience Platform. Deze instellingen worden toegepast op beide oplossingen voor elke ontvanger voordat deze wordt verzonden.


**Best practices**

* Pas **gecentraliseerd bestuur** toe - vermijd het leiden van toestemming afzonderlijk op campagneseniveau.
* Periodiek de gegevens over de toestemming controleren om inconsistenties op te sporen.
* Eerbiedig **kanaal-specifieke opt-outs** - veronderstel geen globale toestemming alle kanalen dekt.

+++


+++ Kan ik ad-hocsegmentatie uitvoeren in geordende campagnes?

In Campagne Orchestration, verwijzen wij naar ad hoc segmentatie als &quot;Levende segmentatie&quot;waar u tot alle gegevens kunt toegang hebben beschikbaar in de relationele opslag in echt - tijd, een complexe vraag bovenop het bouwen en het resultaat voor onmiddellijke activering door uitgaande kanalen (bijvoorbeeld E-mail + SMS).


**Uiteinden**

* Het gebruik ad-hoc segmentatie voor **tijd-gevoelige behoeften** (b.v., flitsbevorderingen).
* Sla nuttige query&#39;s op en documenteer deze zodat ze opnieuw kunnen worden gebruikt in toekomstige campagnes.
* Valideer het aantal gebruikers vóór activering om te voorkomen dat het publiek te veel of te weinig wordt verzonden.

+++


+++ Heeft Campagne Orchestration alleen toegang tot gegevens die via batch zijn geladen, of kan het ook vragen in real time bijgewerkte tabellen (zoals Analytics-gegevens)?

Journey Optimizer Campaign Orchestration kan eerst een ad-hocquery bouwen boven op modelgebaseerde schema&#39;s. Modelgebaseerde schema&#39;s ondersteunen alleen op dit moment Batch-bronnen. Daarnaast biedt de toepassing ondersteuning voor gebruikers van elk type Adobe Experience Platform Audience.

+++

+++ Steunt geordende campagnes beslissingen?

Ja. Beslissing kan relationele gegevens uit geordende campagnes gebruiken. Zodra model-gebaseerd schema met schema&#39;s XDM wordt verbonden, kunnen de gegevens XDM in besluit worden gebruikt.

+++


+++ Hoe werkt implementatie in verschillende omgevingen?

Objecten die zijn gemaakt in geordende campagnes (bijv. publiek, workflows) zijn gekoppeld aan de sandbox waarin ze zijn gemaakt. De standaardworkflows voor verpakken en implementeren in verschillende omgevingen (Dev, Stage, Prod) zijn momenteel niet beschikbaar voor geordende campagnes.

**Best practices**

* Handhaaf **afzonderlijke zandbakken** voor experimenteren, QA, en productie.
* Documentconfiguraties grondig om handmatige replicatie mogelijk te maken, indien nodig.
* Richt zich op governance teams om configuratiedrift tussen milieu&#39;s te verminderen.

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Wat is het verband tussen de Ontvanger en de Entiteiten van het Profiel?

De segmentatie wordt uitgevoerd op Ontvangers terwijl het verzenden tegen het Profiel van Adobe Experience Platform. De het doelafmeting van de Ontvanger breidt het verenigde Profiel met extra gegevens uit die voor segmentatie binnen Geordende campagnes worden gebruikt, terwijl de Ontvanger met Profiel bij runtime voor het verzenden van berichten en het toestemmingsbeleid en bedrijfsregels in overeenstemming wordt gebracht. Deze afstemming is nuttig voor het verenigen van bedrijfsregels en het toepassen van toestemming op profielniveau

![](assets/recipients-and-profiles.png)

+++

+++ In welke gevallen wordt aangeraden de ontvanger te gebruiken in combinatie met de profielentiteiten?

Het antwoord &#39;Ja&#39; stelt de beste gegevensopslag voor - maar bevestigt altijd de beste aanpak op basis van uw gebruikscase en beperkingen met uw Adobe-vertegenwoordiger.

| Relationele winkel | Real-Time Customer Profile |
|---------|----------|
| Is de bron al relationeel? | Is de bron van de gegevensstroom? |
| Bent u van plan om gegevens als-it voor het op de markt brengen van gebruiksgevallen in te voeren? | Is gegevensversheid een belangrijke vereiste? |
| Is er een groot volume historische gegevens (`>` 2 maanden) die voor het op de markt brengen van activeringsgebruiksgevallen nodig zijn? | Zijn er scenario&#39;s waarin acties of besluiten op het moment gegevens vereisen? |
| Zijn er ad-hocbehoeften aan publiekscreatie, evaluatie, en activering? | Kunnen de gedragsgegevens worden beperkt tot `<` 90 dagen met behulp van vooraf samengestelde aggregaten? |
|  | Zijn gegevens nodig voor het personaliseren van berichten in real time? |

+++

+++ Wat is het maximumaantal activiteiten per geordende campagne?

Het aantal activiteiten in een geordende campagne is beperkt tot 500.

+++

+++ Is het mogelijk om verbeteringen uit te voeren om extra gegevens toe te voegen?

Ja, u kunt gegevens verrijken van de relationele winkel en van het Adobe Experience Platform-publiek.

+++

+++ Moeten alle filters via publiek worden gedefinieerd of kan een bepaald type filter worden geconfigureerd?

De geordende campagnes steunen Vooraf bepaalde Filters: u kunt een vraag als filter bepalen en opslaan, en het toevoegen aan uw favorieten om in verdere segmentatietaken opnieuw te worden gebruikt.

+++


## Aanvullende bronnen

Raadpleeg de volgende bronnen voor meer informatie en updates:

* [Gestroomlijnde campagnes zorgen en beperkingen](../orchestrated/guardrails.md)
* [Begin met schema&#39;s en datasets in Geordende campagnes](../orchestrated/gs-schemas.md)
* [Uw eerste geordende campagne maken](../orchestrated/gs-campaign-creation.md)
* [ de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
