---
solution: Journey Optimizer
product: journey optimizer
title: Geordende campagnes Veelgestelde vragen
description: Veelgestelde vragen over door Journey Optimizer georganiseerde campagnes
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 6a0b4f7da2794f6ffd9af51440f1bca8aa5e7fb1
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 1%

---

# Veelgestelde vragen {#faq-oc}

Hieronder vindt u Veelgestelde vragen over door Adobe Journey Optimizer geordende campagnes.

Wilt u meer details? Gebruik de feedbackopties onder aan deze pagina om je vraag te stellen.

## Wat zijn geordende campagnes? {#what-are-oc}

Geordende campagnes in Adobe Journey Optimizer Help-merken voeren complexe, één-op-veel marketingcampagnes op schaal. Ze zijn ontworpen voor door het merk geïnitieerde betrokkenheid, zoals promoties, seizoenscampagnes of communicatie op basis van account.

Vergeleken met single-send campagnes, brengen zij **orchestratie en het rangschikken** aan uitgaande marketing: de kijkcijfers bewegen zich door een multi-step werkschema samen, eerder dan het ontvangen van een eenmalig blaast.

## Wat kan ik doen met geordende campagnes? {#what-can-i-do}

De belangrijkste mogelijkheden omvatten:

* **publiek op bestelling**: bouw en verfijnen direct doelgroepen gebruikend relationele vragen.
* **Segmentatie van meerdere entiteiten**: Creeer nauwkeurige publiek door klantengegevens met verwante entiteiten (b.v., rekeningen, aankopen, boeken) aan te sluiten.
* **pre-Send Zichtbaarheid**: Zie nauwkeurige publiekscijfers alvorens lanceren om het richten te optimaliseren.
* **MultiStep Workflows**: De gesequeneerde campagnes van de looppas zoals seizoensgebonden bevorderingen, productlanceringen, of loyaliteitsaanbiedingen.

>[!BEGINSHADEBOX]

**Best practices**

* Bepaal a **duidelijke campagnedoelstelling** alvorens werkschema&#39;s te ontwerpen.
* Begin met a **proefpubliek** om tellingen en logica vóór het schrapen te bevestigen.
* Houd segmenteringsregels **zo eenvoudig mogelijk** om prestaties en transparantie te optimaliseren.
* Gebruik **verenigbare noemende overeenkomsten** voor publiek en campagnes om beheer gemakkelijker te maken.

>[!ENDSHADEBOX]


## Welke kanalen worden gesteund? {#channels}

De geordende campagnes steunen **e-mail, SMS, en dupberichten**.


>[!BEGINSHADEBOX]

**Aanbevelingen**

* Pas het kanaal aan de **aard van uw bericht** (b.v., dringend = SMS, gepersonaliseerde aanbiedingen = e-mail, contextafhankelijk = duw) aan.
* Valideer altijd toestemmings- en abonnementsvoorkeuren voordat u een kanaal activeert.
* Test berichtweergave op meerdere apparaten en clients om consistente ervaring te garanderen.

>[!ENDSHADEBOX]


## Hoe zijn geordende campagnes anders dan Reizen? {#oc-vs-journeys}

* **Geordende campagnes**: Best voor **partij, één-aan-vele** campagnes. Het hele publiek beweegt zich samen door het campagnecanvas.
* **Reizen**: Best voor **real time, één-aan-één** overeenkomst. Elke klant beweegt zich door de reis in hun eigen tempo, die door gedrag of gebeurtenissen wordt teweeggebracht.

>[!BEGINSHADEBOX]

**Uiteinde** - Vele organisaties gebruiken **zowel samen** - de Schijven voor teweeggebrachte, reactieve ervaringen, en Geordende campagnes voor geplande, op kalender-gebaseerde initiatieven.

>[!ENDSHADEBOX]

## Wat is segmentatie van meerdere entiteiten? {#multi-entity}

Campagne Orchestration in Adobe Journey Optimizer gebruikt een relationele database. Dit type van gegevensmodel heeft afzonderlijke schema&#39;s van gegevens die via 1 :1 of 1 :many verhoudingen worden verbonden. Dit laat gebruikers toe om een vraag op om het even welk schema te beginnen - niet alleen op ontvankelijk niveau - en dan terug en uit te keren naar andere verwante regelingen, zoals aankopen, producten, boeken of ontvankelijke details die grote flexibiliteit in verstrekken hoe de segmenten en het publiek kunnen worden gecreeerd en
verfijnd.

>[!BEGINSHADEBOX]

**Voorbeeld** - richt alle ontvangers met abonnementen die in volgende 3ad-h0 dagen verlopen: In Campagneorganisatie kan de vraag met het schema van Abonnementen beginnen, enkel de kolom van de vervaldatum van dat schema zoeken en alle abonnementen terugkeren toe te verlopen, dan rollen omhoog aan de ontvankelijke gegevens die met die specifieke abonnementen IDs verwant zijn die resultaten sneller en efficiënter terugkeren dan gegevensmodellen die elke vraag op het niveau beginnen.

>[!ENDSHADEBOX]


## Hoe werkt het gegevensmodel? {#data-model}

De campagnes gebruiken a **relationele gegevensbestand**. Hierdoor kunt u query&#39;s uitvoeren op verschillende gegevenssets (zoals klanten, producten, abonnementen) en deze op flexibele wijze verbinden voor geavanceerde segmentatie.

>[!BEGINSHADEBOX]

**Best practices**

* Organiseer datasets zodat **verhoudingen (treedt toe)** bedrijfslogica weerspiegelen.
* Vermijd onnodige verbindingen om query&#39;s uitvoerbaar te houden.
* Valideer de monsterresultaten voordat u grootschalige extracties uitvoert.

>[!ENDSHADEBOX]

## Kan ik berichten met deze gegevens personaliseren? {#personalization}

Ja. In Campagne Orchestration kan een ontvankelijk profiel dat als &quot;Entiteit van Mensen&quot;wordt bekend worden bijgewerkt en dat gegeven voor verpersoonlijking wordt gebruikt. Daarnaast kunnen verrijkte gegevens van gekoppelde entiteiten in de relationele database ook worden gebruikt voor personalisatie. U kunt de profielen van de klant samen met verbonden gegevens (zoals aankopen of abonnementen) gebruiken om inhoud over alle gesteunde kanalen te personaliseren.

>[!BEGINSHADEBOX]

**Aanbevelingen**

* Het gebruik **transactie en gedragsgegevens** om aanbiedingen relevant te maken.
* Combineer **statische attributen** (b.v., loyaliteitrij) met **dynamische degenen** (b.v., laatste aankoopdatum).
* Houd personalisatie beknopt: het overladen van berichten met gegevens kan de leesbaarheid schaden.

>[!ENDSHADEBOX]


## Is zij geïntegreerd met andere Adobe-oplossingen? {#integrations}

Ja. Campagneorchestratie is native geïntegreerd met:

* **Customer Journey Analytics**: De rapporten van de organisatie van de campagne zijn beschikbaar.
* **Real-Time CDP**: Het publiek dat in Campagnes wordt gebouwd kan in Real-Time CDP worden gelezen.
* **Federated Audience Composition (FAC)**: Beschikbaar als toe:voegen-op.

## Hoe zit het met machtigingen en toestemming? {#permissions}

Machtigingen en toestemming voor geordende campagnes en reizen worden centraal beheerd in Adobe Experience Platform. Deze instellingen worden toegepast op beide oplossingen voor elke ontvanger voordat deze wordt verzonden.

>[!BEGINSHADEBOX]

**Best practices**

* Pas **gecentraliseerd bestuur** toe - vermijd het leiden van toestemming afzonderlijk op campagneseniveau.
* Periodiek de gegevens over de toestemming controleren om inconsistenties op te sporen.
* Eerbiedig **kanaal-specifieke opt-outs** - veronderstel geen globale toestemming alle kanalen dekt.

>[!ENDSHADEBOX]

## Kan ik ad-hocsegmentatie uitvoeren? {#ad-hoc}

In Campagne Orchestration, verwijzen wij naar ad hoc segmentatie als &quot;Levende segmentatie&quot;waar u tot alle gegevens kunt toegang hebben beschikbaar in de relationele opslag in echt - tijd, een complexe vraag bovenop het bouwen en het resultaat voor onmiddellijke activering door uitgaande kanalen (bijvoorbeeld E-mail + SMS).

>[!BEGINSHADEBOX]

**Uiteinden**

* Het gebruik ad-hoc segmentatie voor **tijd-gevoelige behoeften** (b.v., flitsbevorderingen).
* Sla nuttige query&#39;s op en documenteer deze zodat ze opnieuw kunnen worden gebruikt in toekomstige campagnes.
* Valideer het aantal gebruikers vóór activering om te voorkomen dat het publiek te veel of te weinig wordt verzonden.

>[!ENDSHADEBOX]


## Steunt dit besluit? {#decisioning}

Op dit moment wordt bij beslissingen geen gebruik gemaakt van relationele gegevens van geordende campagnes.

## Hoe werkt implementatie in verschillende omgevingen? {#deployment}

Objecten die zijn gemaakt in geordende campagnes (bijv. publiek, workflows) zijn gekoppeld aan de sandbox waarin ze zijn gemaakt. De standaardworkflows voor verpakken en implementeren in verschillende omgevingen (Dev, Stage, Prod) zijn momenteel niet beschikbaar voor geordende campagnes.

>[!BEGINSHADEBOX]

**Best practices**

* Handhaaf **afzonderlijke zandbakken** voor experimenteren, QA, en productie.
* Documentconfiguraties grondig om handmatige replicatie mogelijk te maken, indien nodig.
* Richt zich op governance teams om configuratiedrift tussen milieu&#39;s te verminderen.

>[!ENDSHADEBOX]

## Zijn er aanbevolen procedures voor het uitvoeren van campagnes op schaal? {#scale}

Ja, volg de onderstaande aanbevolen procedures:

* **campagnes van het Plan rond bedrijfscalendars** (productlanceringen, seizoenspieken) om volume en middelen te richten.
* Gebruik **publiek voorproeven** alvorens te verzenden om de verwachte grootte te bevestigen en verrassingen te vermijden.
* Waar mogelijk, **stagger verzendt tijden** om overweldigende stroomafwaartse systemen (b.v., callcenters, websites) te vermijden.
* Vestig a **controle routine** - spoorleveringslogboeken, foutentarieven, en opt-outs na elk verzenden.
* Looppas **post-campagneanalyse** in Customer Journey Analytics om het richten en het orchestreren voor de volgende cyclus te verfijnen.



>[!MORELIKETHIS]
>
>* [ Geordende campagnes begeleiden &amp; beperkingen ](../orchestrated/guardrails.md)
>* [ worden begonnen met schema&#39;s en datasets in Geordende campagnes ](../orchestrated/gs-schemas.md)
>* [ creeer uw eerste Geordende campagne ](../orchestrated/gs-campaign-creation.md)
>* [ de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
