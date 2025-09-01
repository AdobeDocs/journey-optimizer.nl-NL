---
solution: Journey Optimizer
product: journey optimizer
title: Geordende campagnes Veelgestelde vragen
description: Veelgestelde vragen over door Journey Optimizer georganiseerde campagnes
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 13bc5f91e0e47bf36b9b9921fa926f8a5e2a50d6
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 1%

---

# Veelgestelde vragen {#faq-oc}

Hieronder vindt u Veelgestelde vragen over door Adobe Journey Optimizer geordende campagnes.

Wilt u meer details? Gebruik de feedbackopties onder aan deze pagina om je vraag te stellen.

## Wat zijn georkestreerde campagnes? {#what-are-oc}

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

## Hoe zijn geordende campagnes anders dan reizen? {#oc-vs-journeys}

* **Orchestrated Campaigns**: Best voor **partij, één-aan-vele** campagnes. Het hele publiek beweegt zich samen door het campagnecanvas.
* **Reizen**: Best voor **real time, één-aan-één** overeenkomst. Elke klant beweegt zich door de reis in hun eigen tempo, die door gedrag of gebeurtenissen wordt teweeggebracht.

>[!BEGINSHADEBOX]

**Uiteinde** - Vele organisaties gebruiken **zowel samen** - Schijven voor teweeggebrachte, reactieve ervaringen, en Geordende Campagnes voor geplande, op kalender-gebaseerde initiatieven.

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

Ja. U kunt de profielen van de klant samen met verbonden gegevens (zoals aankopen of abonnementen) gebruiken om inhoud over alle gesteunde kanalen te personaliseren.

>[!BEGINSHADEBOX]

**Aanbevelingen**

* Het gebruik **transactie en gedragsgegevens** om aanbiedingen relevant te maken.
* Combineer **statische attributen** (b.v., loyaliteitrij) met **dynamische degenen** (b.v., laatste aankoopdatum).
* Houd personalisatie beknopt: het overladen van berichten met gegevens kan de leesbaarheid schaden.

>[!ENDSHADEBOX]


## Is zij geïntegreerd met andere Adobe-oplossingen? {#integrations}

* **Customer Journey Analytics**: De rapporten van de organisatie van de campagne zijn beschikbaar.
* **Real-Time CDP**: Het publiek dat in Campagnes wordt gebouwd kan in CDP worden gelezen.
* **Federated Audience Composition (FAC)**: Beschikbaar als toe:voegen-op.

## Hoe zit het met machtigingen en toestemming? {#permissions}

Machtigingen en toestemming worden centraal beheerd in Adobe Experience Platform. De zelfde regels zijn op zowel Reizen als Geordende Campagnes van toepassing om naleving en verenigbare klantenervaring te verzekeren.

>[!BEGINSHADEBOX]

**Best practices**

* Pas **gecentraliseerd bestuur** toe - vermijd het leiden van toestemming afzonderlijk op campagneseniveau.
* Periodiek de gegevens over de toestemming controleren om inconsistenties op te sporen.
* Eerbiedig **kanaal-specifieke opt-outs** - veronderstel geen globale toestemming alle kanalen behandelt.

>[!ENDSHADEBOX]

## Kan ik ad-hocsegmentatie uitvoeren? {#ad-hoc}

Ja. Met **Levende Segmentatie**, kunt u complexe vragen op de plaats bouwen en hen onmiddellijk over uitgaande kanalen activeren.

>[!BEGINSHADEBOX]

**Uiteinden**

* Het gebruik ad-hoc segmentatie voor **tijd-gevoelige behoeften** (b.v., flitsbevorderingen).
* Sla nuttige query&#39;s op en documenteer deze zodat ze opnieuw kunnen worden gebruikt in toekomstige campagnes.
* Valideer het aantal gebruikers vóór activering om te voorkomen dat het publiek te veel of te weinig wordt verzonden.

>[!ENDSHADEBOX]

## Steunt dit besluit? {#decisioning}

Op dit moment worden voor beslissingen geen relationele gegevens van geordende campagnes gebruikt.

## Hoe werkt implementatie in verschillende omgevingen? {#deployment}

Objecten die zijn gemaakt in geordende campagnes (bijv. publiek, workflows) zijn gekoppeld aan de sandbox waarin ze zijn gemaakt. De standaardworkflows voor verpakken en implementeren in verschillende omgevingen (dev, stage, prod) zijn momenteel niet beschikbaar voor geordende campagnes.

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
