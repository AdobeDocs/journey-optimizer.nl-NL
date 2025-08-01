---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met geordende campagnes
description: Leer hoe u begint met geordende campagnes
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Aan de slag met geordende campagnes {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campagnes_overview_orchestrated"
>abstract="<b> Splitsen van de Campagne de orchestratie </b><br/>, combineren, verrijken en manipuleren relationele datasets om uw publiek <br/><br/> te bepalen <b> Van de hefboomwerking multi-entiteitgegevens </b><br/> leren hoe Geordende campagnes uit relationele datasets kunnen voordeel halen om gegevens voor segmentatie &amp; verpersoonlijking <br/><br/><b> Ad-hoc segmentatie &amp; nauwkeurige tellingen </b><br/> te verrijken bouwt uw segment stap voor stap met nauwkeurige tellingen <br/><br/><b> Beschikbare kanalen </b><br/> E-mail, SMS, Push berichten, Directe post"

+++ Inhoudsopgave

| Welkom bij Geordende campagnes | Start uw eerste geordende campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| <b>[ wordt begonnen met Geordende campagnes ](gs-orchestrated-campaigns.md)</b><br/><br/> creeer en beheer relationele Schema&#39;s en Datasets:</br> <ul><li>[ worden begonnen met Schema&#39;s en Datasets ](gs-schemas.md)</li><li>[ Handmatig schema ](manual-schema.md)</li><li>[ het uploadschema van het Dossier ](file-upload-schema.md)</li><li>[ Ingest gegevens ](ingest-data.md)</li></ul>[ toegang en beheer Geordende campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Zeer belangrijke stappen om een Geordende campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/>[ bouwt uw eerste vraag ](build-query.md)<br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [&#128279;](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

De inhoud op deze pagina is niet definitief en kan worden gewijzigd.

>[!ENDSHADEBOX]

Campagne in [!DNL Adobe Journey Optimizer] biedt geavanceerde, merkgestarte marketingcampagnes via verschillende kanalen, waarmee u op grote schaal betrokkenheid, inkomsten en klantenloyaliteit kunt stimuleren.

Hoewel de marketing over de kanalen essentieel is, maken de geordende campagnes het naadloos. Met een visuele, belemmering-en-dalingsinterface, kunt u complexe marketing werkschema&#39;s ontwerpen en automatiseren, van segmentatie aan berichtlevering, over veelvoudige kanalen. Alles gebeurt in één intuïtieve omgeving, gebouwd voor snelheid, controle en efficiëntie.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Kernmogelijkheden

Campagne wordt opgebouwd rond vier pijlers:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Op verzoek publiek" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b> Op bestelling publiek </b><br/> direct vraag over datasets om publiekssegmenten tot stand te brengen gebruikend om het even welke combinatie gegevenstypes en dimensies.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentering en verzending van meerdere entiteiten" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b> Multi-entiteitsegmentatie &amp; het verzenden van </b><br/> gaat voorbij op persoon-gebaseerde campagnes-gebruik entiteiten zoals productcatalogi, opslagplaatsen, of de dienstgegevens om met precisie te richten.<br/><br/>
Ondersteuning voor verzending op meerdere niveaus, waarbij één bericht wordt verzonden per profiel en per bijbehorende secundaire entiteit. Deze secundaire entiteiten kunnen contactadressen, reserveringen, abonnementen, contracten, of andere verbonden gegevens omvatten. Zo kunt u bijvoorbeeld campagnes verzenden naar alle bekende adressen van een profiel of voor elke reservering die aan dat profiel is gekoppeld.</td></tr>
<tr style="border: 0;">
<td><img alt="Zichtbaarheid vóór verzending en precisie" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b> pre-verzend zicht &amp; precisie </b><br/> krijgt nauwkeurige segmentatietelling en volledig campagnewerkingsgebied vóór lancering, die nauwkeurigheid en vertrouwen verzekert.</td></tr>
<tr style="border: 0;">
<td><img alt="Workflows voor meerdere stappen" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b> multi-step campagnewerkschema's </b><br/> Ontwerp multi-stappen campagnes, van dagelijkse berichten aan complexe campagnes zoals seizoensgebonden promoties of belangrijke productlanceringen.</td></tr>
</table>

## Geordende campagnes en reizen

Hoewel de geordende visualisatie van campagnes gelijkenissen vertoont met reizen, lost het verschillende doeleinden en gebruiksgevallen op:

* **reizen** - 1 tot 1 canvas waar elk profiel door de verschillende stappen bij hun eigen tempo reist. De staat van elke klant wordt gehandhaafd binnen zijn context om acties in real time teweeg te brengen.

* **Geordende campagnes** - in tegenstelling tot reizen, werken de georchetseerde campagnes gebruikend een partijcanvas dat segmenten berekent. Alle profielen worden samen verwerkt.

Beide canvas&#39;s zijn geoptimaliseerd voor hun respectieve gebruiksgevallen: Journey canvas publiceert een reis die de neiging heeft langer te leven, terwijl het canvas van de Campagne voor herhalende en stijgende looppas van een partijcampagne wordt ontworpen.

## Vereisten

Voordat u gaat werken met geordende campagnes, is het van essentieel belang dat u over de juiste machtigingen beschikt. De toegang tot Geordende campagnes wordt beperkt tot gebruikers die aan relevante **[!UICONTROL Product Profile]**, zoals Geordende de Beheerder van de Campagne, Geordende Begeleider van de Campagne, Geordende Beheerde Manager van de Campagne, of de Geordende Kijker van de Campagne worden toegewezen.

Als u geen toegang hebt tot geordende campagnefuncties, neemt u contact op met uw beheerder om de benodigde machtigingen aan te vragen.

➡️ [ Leer meer over productprofielen met betrekking tot Geordende Campagnes ](../administration/ootb-product-profiles.md)

## Laten we dieper duiken

Nu je begrijpt wat georcherstreerde campagnes zijn, is het tijd om dieper in deze documentatiegedeelten te duiken om met de functie te gaan werken.

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
