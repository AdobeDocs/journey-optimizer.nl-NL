---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met georkestreerde campagnes
description: Meer informatie over hoe u aan de slag kunt gaan met georkestreerde campagnes
short-description: Ontdek de belangrijkste kenmerken en gebruiksscenario's van georkestreerde campagnes.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
source-git-commit: 9619ffd2cde677c0c83ee1b53f232c41b5faaa9a
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 3%

---


# Aan de slag met georkestreerde campagnes {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campagnes_overview_orchestrated"
>abstract="<b> Splitsen van de Campagne de orchestratie </b><br/>, combineren, verrijken en manipuleren relationele datasets om uw publiek <br/><br/> te bepalen <b> Van de hefboomwerking multi-entiteitgegevens </b><br/> leren hoe de Geordende campagnes uit relationele datasets kunnen voordeel halen om gegevens voor segmentatie &amp; verpersoonlijking <br/><br/><b> Ad-hoc segmentatie &amp; de nauwkeurige tellingen </b><br/> bouwen uw segment stap voor stap met nauwkeurige tellingen <br/><br/><b> Beschikbare kanalen </b><br/> E-mail, SMS, Push berichten"

Campagne in [!DNL Adobe Journey Optimizer] biedt geavanceerde, merkgestarte marketingcampagnes via verschillende kanalen, waarmee u op grote schaal betrokkenheid, inkomsten en klantenloyaliteit kunt stimuleren.

>[!IMPORTANT]
>
>Om tot Campagneorganisatie toegang te hebben, moet uw vergunning of de **Journey Optimizer - Campagnes &amp; Reizen** of **Journey Optimizer - het pakket van Campagnes** omvatten. Neem contact op met uw Adobe-vertegenwoordiger om uw licentie te bevestigen en indien nodig bij te werken.

Hoewel de marketing over de kanalen essentieel is, maken de geordende campagnes het naadloos. Met een visuele, belemmering-en-dalingsinterface, kunt u complexe marketing werkschema&#39;s ontwerpen en automatiseren, van segmentatie aan berichtlevering, over veelvoudige kanalen. Alles gebeurt in één intuïtieve omgeving, gebouwd voor snelheid, controle en efficiëntie.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [ ontdekt Geordende campagnes in video ](#video-oc)

## Kernmogelijkheden

Campagne wordt opgebouwd rond vier pijlers:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Op verzoek publiek" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b> Op bestelling publiek </b><br/> direct vraag over datasets om publiekssegmenten tot stand te brengen gebruikend om het even welke combinatie gegevenstypes en dimensies.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentering en verzending van meerdere entiteiten" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b> Multi-entiteitsegmentatie &amp; het verzenden van </b><br/> gaat voorbij op persoon-gebaseerde campagnes-gebruik entiteiten zoals productcatalogi, opslagplaatsen, of de dienstgegevens om met precisie te richten.<br/><br/>
Ondersteuning voor verzending op meerdere niveaus, waarbij één bericht wordt verzonden per profiel en per bijbehorende secundaire entiteit. Deze secundaire entiteiten kunnen contactadressen, reserveringen, abonnementen, contracten, of andere verbonden gegevens omvatten. Zo kunt u bijvoorbeeld campagnes verzenden naar alle bekende adressen van een profiel of voor elke reservering die aan dat profiel is gekoppeld.</td></tr>
<tr style="border: 0;">
<td><img alt="Zichtbaarheid vóór verzending en precisie" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b> pre-verzend zicht &amp; precisie </b><br/> krijgt nauwkeurige segmentatietelling en volledig campagnewerkingsgebied vóór lancering, die nauwkeurigheid en vertrouwen verzekert.</td></tr>
<tr style="border: 0;">
<td><img alt="Workflows voor meerdere stappen" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b> multi-step campagnewerkschema's </b><br/> Ontwerp multi-stappen campagnes, van dagelijkse berichten aan complexe campagnes zoals seizoensgebonden promoties of belangrijke productlanceringen.</td></tr>
</table>

>[!NOTE]
>
>Voor meer informatie over de gesteunde kanalen, verwijs naar de lijst in deze sectie: [ Kanalen in reizen &amp; campagnes ](../channels/gs-channels.md#channels).
>
>Welke kanalen beschikbaar zijn, is afhankelijk van uw licentiemodel en invoegtoepassingen.

## Geordende campagnes en reizen

Hoewel de geordende visualisatie van campagnes gelijkenissen vertoont met reizen, lost het verschillende doeleinden en gebruiksgevallen op:

* **reizen** - 1 tot 1 canvas waar elk profiel door de verschillende stappen bij hun eigen tempo reist. De staat van elke klant wordt gehandhaafd binnen zijn context om acties in real time teweeg te brengen.

* **Geordende campagnes** - in tegenstelling tot reizen, werken de Geordende campagnes gebruikend een partijcanvas dat segmenten berekent. Alle profielen worden samen verwerkt.

Beide canvas&#39;s zijn geoptimaliseerd voor hun respectieve gebruiksgevallen: Journey canvas publiceert een reis die de neiging heeft langer te leven, terwijl het canvas van de Campagne voor herhalende en stijgende looppas van een partijcampagne wordt ontworpen.

## Wat zit er in een geordende campagne? {#gs-ms-campaign-inside}

Het geordende campagnecanvas is een voorstelling van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![ beeld dat een Geordend campagnecanvas ](assets/canvas-example.png) toont

Elke geordende campagne bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De [ diverse activiteiten ](activities/about-activities.md) worden vertegenwoordigd op het canvas door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een geordend campagnecanvas kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkomende acties is.

* **Overgangen**: De overgangen verbinden een bronactiviteit met een bestemmingsactiviteit en bepalen hun opeenvolging.

* **Worktables**: De werklijst bevat alle informatie die door de overgang wordt gedragen. Voor elke geordende campagne worden verschillende worktables gebruikt. De gegevens in deze tabellen kunnen worden gebruikt gedurende de gehele levenscyclus van de geordende campagne.


## Introductievideo {#video-oc}

Leer de belangrijkste concepten en mogelijkheden beschikbaar met Geordende campagnes.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## Laten we dieper duiken

Nu u een inzicht hebt in wat georkestreerde campagnes zijn, is het tijd om dieper in deze documentatiesecties te duiken beginnen met het werken met de eigenschap.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Campagnes openen en beheren" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Configuratiestappen</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lood" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong> creeer een Geordende campagne </strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Onfrequent" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong> Werk met activiteiten </strong></a>
</div>
<p></td>
</tr></table>

## Aanvullende bronnen

* **[bouwt uw eerste regel](build-query.md)** - Meester de regelbouwer om gerichte vragen tot stand te brengen en uw publiek met precisie te segmenteren gebruikend relationele gegevens.
* **[creeer relationele schema&#39;s](gs-schemas.md)** - begrijp hoe te opstelling en relationele schema&#39;s te vormen aan hefboomwerking multi-entiteitgegevens in uw campagnes.
* **[Meldend voor Geordende campagnes](reporting-campaigns.md)** - spoor en analyseer uw campagneprestaties met gedetailleerde rapporteringsmetriek en inzichten.
* **[Begin en controleer campagnes](start-monitor-campaigns.md)** - leer beste praktijken voor lanceringscampagnes en controle hun uitvoering in real time.
* **[Grafieken en beperkingen](guardrails.md)** - herzie belangrijke gidsen, beperkingen, en beste praktijken om optimale campagneprestaties te verzekeren.
* **[Veelgestelde Vragen](orchestrated-campaigns-faq.md)** - vind antwoorden aan gemeenschappelijke vragen over Geordende campagneeigenschappen, mogelijkheden, en gebruiksgevallen.
* **[Geordende campagnezelfstudies ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/orchestrated-campaigns/introduction-to-orchestrated-campaigns){target="_blank"}** - Onderzoek geleidelijke videoleerprogramma&#39;s die eigenschappen en beste praktijken behandelen.
