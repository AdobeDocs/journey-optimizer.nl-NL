---
solution: Journey Optimizer
product: journey optimizer
title: Geordende campagnes Veelgestelde vragen
description: Veelgestelde vragen over door Journey Optimizer georganiseerde campagnes
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 6a32a60f153ff4880ce974e77bc11eed1e20a7c7
workflow-type: tm+mt
source-wordcount: '1884'
ht-degree: 5%

---

# Veelgestelde vragen {#faq-oc}

Hieronder vindt u Veelgestelde vragen over door Adobe Journey Optimizer geordende campagnes.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [ gemeenschap van Adobe Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

+++ Wat is campagneorkest?

Campagne Orchestration is een eigenschap van Journey Optimizer die enige-stap of multi-step werkschema&#39;s steunt die hefboomwerking de Relationele Datastore om publiek voor het doel van partijovereenkomst te bouwen en te segmenteren.

Het brengt een nieuw type van campagnes aan Journey Optimizer: **Geordende campagnes**. Geordende campagnes helpen merken complexe, één-op-veel marketingcampagnes op schaal uit te voeren. Ze zijn ontworpen voor door het merk geïnitieerde betrokkenheid, zoals promoties, seizoenscampagnes of communicatie op basis van account.

Vergeleken met single-send/actiecampagnes, brengen zij **orchestratie en het rangschikken** aan uitgaande marketing: de kijkcijfers bewegen zich door een multi-step werkschema samen, eerder dan het ontvangen van een eenmalig blaast.

**Meer informatie**

* [Aan de slag met georkestreerde campagnes](gs-orchestrated-campaigns.md)
* [Uw eerste geordende campagne maken](gs-campaign-creation.md)

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

**Meer informatie**

* [Een geordende campagne maken](create-orchestrated-campaign.md)
* [Werken met campagneactiviteiten](activities/about-activities.md)
* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)

+++

+++ Hoe krijg je toegang tot Campagneorganisatie?

Om tot Campagneorganisatie toegang te hebben, moet uw vergunning of de **Journey Optimizer - Campagnes &amp; Reizen** of **Journey Optimizer - het pakket van Campagnes** omvatten. Neem contact op met uw Adobe-vertegenwoordiger om uw licentie te bevestigen en indien nodig bij te werken.

**Meer informatie**

* [Aan de slag met georkestreerde campagnes](gs-orchestrated-campaigns.md)
* [ Adobe Journey Optimizer productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}

+++

+++ Hoe zijn geordende campagnes anders dan Reizen?

* **Geordende campagnes**: Best voor **partij, één-aan-vele** campagnes. De vooruitgang van het publiek in bulk, op een programma.
* **Reizen**: Best voor **real time, één-aan-één** overeenkomst. Elke klant beweegt zich door de reis in hun eigen tempo, die door gedrag of gebeurtenissen wordt teweeggebracht.

**Beste praktijken**: Gebruik hen samen — Reizen voor teweeggebrachte, reactieve ervaringen, en Geordende Campagnes voor geplande, op kalender-gebaseerde initiatieven.

**Meer informatie**

* [Aan de slag met georkestreerde campagnes](gs-orchestrated-campaigns.md)
* [Uw eerste journey maken](../building-journeys/journey-gs.md)
* [Aan de slag met campagnes](../campaigns/get-started-with-campaigns.md)

+++

+++ Wat is segmentatie van meerdere entiteiten?

Campagne Orchestration in Adobe Journey Optimizer gebruikt een relationele database. Dit type van gegevensmodel heeft afzonderlijke schema&#39;s van gegevens die via 1 :1 of 1 :many verhoudingen worden verbonden. Dit laat gebruikers toe om een vraag op om het even welk schema te beginnen - niet alleen op ontvankelijk niveau - en dan terug en uit te keren naar andere verwante regelingen, zoals aankopen, producten, boekingen of ontvankelijke details die grote flexibiliteit in verstrekken hoe de segmenten en het publiek kunnen worden gecreeerd en worden verfijnd.

**Voorbeeld** - richt alle ontvangers met abonnementen die in de volgende 30 dagen verlopen. In Campagneorganisatie kan de vraag met het schema van Abonnementen beginnen, enkel de kolom van de vervaldatum van dat schema zoeken en alle abonnementen terugkeren toe te schrijven aan verlopen, dan rol omhoog aan de ontvankelijke gegevens die met die specifieke abonnementen IDs verwant zijn die resultaten sneller en efficiënter terugkeren dan gegevensmodellen die met elke vraag op het ontvankelijke niveau beginnen.

**Meer informatie**

* [Begin met schema&#39;s en datasets](gs-schemas.md)
* [Vorm een het richten dimensie](target-dimension.md)
* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)

+++

+++ Hoe werkt het gegevensmodel?

De campagnes gebruiken a **relationele gegevensbestand**. Hierdoor kunt u query&#39;s uitvoeren op verschillende gegevenssets (zoals klanten, producten, abonnementen) en deze op flexibele wijze verbinden voor geavanceerde segmentatie.

**Best practices**

* Organiseer datasets zodat **verhoudingen (treedt toe)** bedrijfslogica weerspiegelen.
* Vermijd onnodige verbindingen om query&#39;s uitvoerbaar te houden.
* Valideer de monsterresultaten voordat u grootschalige extracties uitvoert.

**Meer informatie**

* [Begin met schema&#39;s en datasets](gs-schemas.md)
* [Handmatig een schema maken](manual-schema.md)
* [Samenvattingsgegevens](ingest-data.md)

+++

+++ Kan ik berichten met relationele gegevens personaliseren?

Ja. In Campagne Orchestration kan een ontvankelijk profiel dat als &quot;Entiteit van Mensen&quot;wordt bekend worden bijgewerkt en dat gegeven voor verpersoonlijking wordt gebruikt. Daarnaast kunnen verrijkte gegevens van gekoppelde entiteiten in de relationele database ook worden gebruikt voor personalisatie. U kunt de profielen van de klant samen met verbonden gegevens (zoals aankopen of abonnementen) gebruiken om inhoud over alle gesteunde kanalen te personaliseren.

**Aanbevelingen**

* Het gebruik **transactie en gedragsgegevens** om aanbiedingen relevant te maken.
* Combineer **statische attributen** (b.v., loyaliteitrij) met **dynamische degenen** (b.v., laatste aankoopdatum).
* Houd personalisatie beknopt: het overladen van berichten met gegevens kan de leesbaarheid schaden.

**Meer informatie**

* [De verrijkingsactiviteit gebruiken](activities/enrichment.md)
* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)

+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Kan ik een live georkestreerde campagne terugzetten naar concept?

Ja, in specifieke situaties. De optie **[!UICONTROL Back to draft]** is ontworpen als een herstelmechanisme om de publicatie van een campagne ongedaan te maken en de status van een campagne te herstellen.

Deze optie is beschikbaar voor geplande campagnes die op uitvoering wachten, of voor live campagnes met uitvoeringsfouten. [ Leer hoe te om een levende campagne terug naar ontwerp terug te keren ](start-monitor-campaigns.md#back-to-draft)

+++

+++ Welke kanalen worden gesteund?

U kunt Geordende campagnes tot stand brengen om **e-mails**, **SMS**, **duw berichten** en **directe post** te verzenden.

**Meer informatie**

* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)
* [Werken met campagneactiviteiten](activities/about-activities.md)

+++

+++ Kunnen meerdere communicaties en verschillende kanalen worden gelanceerd binnen dezelfde geordende campagne?

Ja, geordende campagnes ondersteunen kanaalorkestorkest. U kunt e-mail, SMS, dupbericht, en direct-mail activiteiten in een multi-step campagnecanvas combineren om uitvoerige klantenervaringen tot stand te brengen.

**Meer informatie**

* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)
* [Werken met campagneactiviteiten](activities/about-activities.md)

+++

+++ Zijn de geordende campagnemalplaatjes beschikbaar?

Nr, kunt u campagnemalplaatjes niet bepalen of gebruiken, maar u kunt inhoudsmalplaatjes voor uw mededelingen gebruiken.

**Meer informatie**

* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)
* [Een geordende campagne maken](create-orchestrated-campaign.md)

+++

+++ Is de inhoudsontwerper voor berichten specifiek voor Geordende campagnes?

Nee, de inhoudsontwerper, inclusief de e-mail-Designer, is overal in Journey Optimizer beschikbaar.

**Meer informatie**

* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)
* [De verrijkingsactiviteit gebruiken](activities/enrichment.md)

+++

+++ Hoe zijn de verschillende kanalen verbonden in geordende campagnes?

De component en runtime van het kanaal worden gebruikt voor alle Journey Optimizer-campagnes, maar de ondersteunde kanalen verschillen. Geordende campagnes ondersteunen e-mail, SMS, pushberichten en direct mail.

**Meer informatie**

* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)
* [Afvoerkanalen en beperkingen](guardrails.md)

+++


+++ Kunnen geordende campagnes verbinding maken met uitgaande kanalen (web, inApp)?

Nee, binnenkomende kanalen zoals web en in-app worden niet ondersteund in geordende campagnes. Alleen uitgaande kanalen (e-mail, SMS, pushberichten en direct mail) worden ondersteund.

**Meer informatie**

* [Afvoerkanalen en beperkingen](guardrails.md)
* [Een kanaalactiviteit toevoegen aan een geordende campagne](activities/channels.md)

+++

+++ Hoe zit het met machtigingen en toestemming?

Machtigingen en toestemming voor geordende campagnes en reizen worden centraal beheerd in Adobe Experience Platform. Deze instellingen worden toegepast op beide oplossingen voor elke ontvanger voordat deze wordt verzonden.

**Best practices**

* Pas **gecentraliseerd bestuur** toe - vermijd het leiden van toestemming afzonderlijk op campagneseniveau.
* Periodiek de gegevens over de toestemming controleren om inconsistenties op te sporen.
* Eerbiedig **kanaal-specifieke opt-outs** - veronderstel geen globale toestemming alle kanalen dekt.

**Meer informatie**

* [Aan de slag met georkestreerde campagnes](gs-orchestrated-campaigns.md)
* [Afvoerkanalen en beperkingen](guardrails.md)

+++


+++ Kan ik ad-hocsegmentatie uitvoeren in geordende campagnes?

In Campagne Orchestration, verwijzen wij naar ad hoc segmentatie als &quot;Levende segmentatie&quot;waar u tot alle gegevens kunt toegang hebben beschikbaar in de relationele opslag in echt - tijd, een complexe vraag bovenop het bouwen en het resultaat voor onmiddellijke activering door uitgaande kanalen (bijvoorbeeld E-mail + SMS).

**Uiteinden**

* Het gebruik ad-hoc segmentatie voor **tijd-gevoelige behoeften** (b.v., flitsbevorderingen).
* Sla nuttige query&#39;s op en documenteer deze zodat ze opnieuw kunnen worden gebruikt in toekomstige campagnes.
* Valideer het aantal gebruikers vóór activering om te voorkomen dat het publiek te veel of te weinig wordt verzonden.

**Meer informatie**

* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)
* [Gebruik de het publieksactiviteit van de Bouwstijl](activities/build-audience.md)
* [Vorm een het richten dimensie](target-dimension.md)

+++


+++ Heeft Campagne Orchestration alleen toegang tot gegevens die via batch zijn geladen, of kan het ook vragen in real time bijgewerkte tabellen (zoals Analytics-gegevens)?

Journey Optimizer Campaign Orchestration kan ad-hocquery&#39;s bouwen boven op relationele schema&#39;s. Relationele schema&#39;s ondersteunen alleen Batch-bronnen voor nu. Bovendien ondersteunt het publiek Lees hier activiteiten van elk type Adobe Experience Platform Audience.

**Meer informatie**

* [Begin met schema&#39;s en datasets](gs-schemas.md)
* [Samenvattingsgegevens](ingest-data.md)
* [De publieksactiviteit Lezen gebruiken](activities/read-audience.md)

+++

+++ Steunt geordende campagnes beslissingen?

Nee, geordende campagnes ondersteunen geen beslissingsmogelijkheden. Voor beslissingsfuncties gebruikt u standaard Journey Optimizer-reizen of actiecampagnes.

**Meer informatie**

* [Aan de slag met Experience Decisition](../experience-decisioning/gs-experience-decisioning.md)
* [Uw eerste journey maken](../building-journeys/journey-gs.md)
* [Aan de slag met campagnes](../campaigns/get-started-with-campaigns.md)

+++


+++ Hoe werkt implementatie in verschillende omgevingen?

Objecten die zijn gemaakt in geordende campagnes (bijv. publiek, workflows) zijn gekoppeld aan de sandbox waarin ze zijn gemaakt. De standaardworkflows voor verpakken en implementeren in verschillende omgevingen (Dev, Stage, Prod) zijn momenteel niet beschikbaar voor geordende campagnes.

**Best practices**

* Handhaaf **afzonderlijke zandbakken** voor experimenteren, QA, en productie.
* Documentconfiguraties grondig om handmatige replicatie mogelijk te maken, indien nodig.
* Richt zich op governance teams om configuratiedrift tussen milieu&#39;s te verminderen.

**Meer informatie**

* [Aan de slag met georkestreerde campagnes](gs-orchestrated-campaigns.md)
* [Afvoerkanalen en beperkingen](guardrails.md)

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

De segmentatie wordt uitgevoerd op Ontvangers terwijl het verzenden tegen het Profiel van Adobe Experience Platform. De het doelafmeting van de Ontvanger breidt het verenigde Profiel met extra gegevens uit die voor segmentatie binnen Geordende campagnes worden gebruikt, terwijl de Ontvanger met Profiel bij runtime voor het verzenden van berichten en het toestemmingsbeleid en bedrijfsregels in overeenstemming wordt gebracht. Deze afstemming is nuttig voor het verenigen van bedrijfsregels en het toepassen van toestemming op profielniveau.

![](assets/recipients-and-profiles.png)

**Meer informatie**

* [Vorm een het richten dimensie](target-dimension.md)
* [Begin met schema&#39;s en datasets](gs-schemas.md)
* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)

+++

+++ In welke gevallen wordt aangeraden de ontvanger te gebruiken in combinatie met de profielentiteiten?

Het antwoord &#39;Ja&#39; stelt de beste gegevensopslag voor - maar bevestigt altijd de beste aanpak op basis van uw gebruikscase en beperkingen met uw Adobe-vertegenwoordiger.

| Relationele winkel | Real-Time Customer Profile |
|---------|----------|
| Is de bron al relationeel? | Is de bron van de gegevensstroom? |
| Bent u van plan om gegevens als-it voor het op de markt brengen van gebruiksgevallen in te voeren? | Is gegevensversheid een belangrijke vereiste? |
| Is er een groot volume historische gegevens (`>` 2 maanden) die voor het op de markt brengen van activeringsgebruiksgevallen nodig zijn? | Zijn er scenario&#39;s waarin acties of besluiten op het moment gegevens vereisen? |
| Zijn er ad-hocbehoeften aan publiekscreatie, evaluatie, en activering? | Kunnen de gedragsgegevens worden beperkt tot `<` 90 dagen met behulp van vooraf berekende aggregaten? |
|  | Zijn gegevens nodig voor het personaliseren van berichten in real time? |

**Meer informatie**

* [Vorm een het richten dimensie](target-dimension.md)
* [Begin met schema&#39;s en datasets](gs-schemas.md)
* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)

+++

+++ Wat is het maximumaantal activiteiten per geordende campagne?

Het aantal activiteiten in een geordende campagne is beperkt tot 500.

**Meer informatie**

* [Afvoerkanalen en beperkingen](guardrails.md)
* [Werken met campagneactiviteiten](activities/about-activities.md)

+++

+++ Is het mogelijk om verbeteringen uit te voeren om extra gegevens toe te voegen?

Ja, u kunt gegevens verrijken van de relationele winkel en van het Adobe Experience Platform-publiek. Gebruik de verrijkingsactiviteit om uw publieksgegevens met extra attributen van verwante regelingen te verbeteren.

**Meer informatie**

* [De verrijkingsactiviteit gebruiken](activities/enrichment.md)
* [De afstemmingsactiviteit gebruiken](activities/reconciliation.md)

+++

+++ Moeten alle filters via publiek worden gedefinieerd of kan een bepaald type filter worden geconfigureerd?

Geordende campagnes ondersteunen vooraf gedefinieerde filters: u kunt een query definiëren en opslaan als een filter, deze toevoegen aan uw favorieten en deze opnieuw gebruiken voor verdere segmentatietaken. Vooraf gedefinieerde filters kunnen parameters bevatten, zodat u waarden kunt invoeren op het moment van gebruik. [ Leer hoe te met vooraf bepaalde filters ](predefined-filters.md) te werken.

**Meer informatie**

* [Bouw uw regel gebruikend de vraagmodeler](build-query.md)
* [Gebruik de het publieksactiviteit van de Bouwstijl](activities/build-audience.md)
* [Werken met vooraf gedefinieerde filters](orchestrated-rule-builder.md)

+++


## Aanvullende bronnen

Raadpleeg de volgende bronnen voor meer informatie en updates:

* [Gestroomlijnde campagnes zorgen en beperkingen](guardrails.md)
* [Begin met schema&#39;s en datasets in Geordende campagnes](gs-schemas.md)
* [Uw eerste geordende campagne maken](gs-campaign-creation.md)
* [ de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
