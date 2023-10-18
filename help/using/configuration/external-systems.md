---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer integreren met externe systemen
description: Leer de beste praktijken bij het integreren van Journey Optimizer met externe systemen
feature: Integrations
role: User
level: Beginner
keywords: extern, API, optimaliseren, aftopping
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 30%

---

# Integreren met externe systemen {#external-systems}

Deze pagina bevat de verschillende instructies die Journey Optimizer biedt bij de integratie van een extern systeem, evenals de beste werkwijzen: hoe u de beveiliging van uw externe systeem kunt optimaliseren met behulp van de API voor plafonnering, hoe u de time-out van de reis kunt configureren en hoe nieuwe pogingen werken.

Met Journey Optimizer kunt u verbindingen met externe systemen configureren via aangepaste gegevensbronnen en aangepaste handelingen. Zo kunt u bijvoorbeeld uw reizen verrijken met gegevens die afkomstig zijn van een extern reserveringssysteem, of berichten verzenden via een systeem van derden, zoals Epsilon of Facebook.

Wanneer u een extern systeem integreert, kunt u verschillende problemen tegenkomen, kan het systeem traag zijn, kan het niet langer reageren of kan het een groot volume mogelijk niet verwerken. Journey Optimizer biedt verschillende instructies om uw systeem te beschermen tegen overbelasting.

Alle externe systemen hebben verschillende prestaties. U moet de configuratie aan uw gebruiksgevallen aanpassen.

Wanneer Journey Optimizer een aanroep naar een externe API uitvoert, worden de technische instructies als volgt uitgevoerd:

1. De het in kaart brengen of throttling regels worden toegepast: als het maximumtarief wordt bereikt, worden de resterende vraag verworpen of een rij gevormd.

2. Time-out en probeer het opnieuw: als de begrenzende of vertragingsregel wordt vervuld, probeert Journey Optimizer de vraag uit te voeren tot het eind van de onderbrekingsduur wordt bereikt.

## API&#39;s uitlijnen en vertragen {#capping}

### Informatie over API&#39;s voor uitlijnen en draaien

Wanneer u een databron of een actie configureert, maakt u een verbinding met een systeem om extra informatie op te halen voor gebruik in uw journeys of om berichten of API-oproepen te versturen.

Journey-API&#39;s ondersteunen tot 5000 gebeurtenissen per seconde, maar sommige externe systemen of API&#39;s hebben mogelijk geen equivalente verwerkingscapaciteit. Om overbelasting van deze systemen te voorkomen, kunt u de **Afbeelding** en **Throttling** API&#39;s om het aantal verzonden gebeurtenissen per seconde te beperken.

Telkens wanneer een API-oproep wordt uitgevoerd door journeys, passeert deze de API-engine. Als de limiet die is ingesteld in de API wordt bereikt, wordt de aanroep afgewezen als u de API voor uitsnijden gebruikt, of gedurende maximaal 6 uur in de wachtrij geplaatst en zo snel mogelijk verwerkt in de volgorde waarin deze is ontvangen als u de API voor rotatie gebruikt.

Stel bijvoorbeeld dat u voor uw externe systeem een regel voor afkappen of beperken hebt gedefinieerd van 100 oproepen per seconde. Uw systeem wordt opgeroepen door een aangepaste actie in 10 verschillende journeys. Indien één journey 200 oproepen per seconde ontvangt, gebruikt deze de 100 beschikbare slots en de 100 resterende slots verwijderen of in een wachtrij plaatsen. Aangezien het maximumaantal is overschreden, hebben de andere 9 journeys geen slot meer. Deze granulariteit helpt het externe systeem te beschermen tegen overbelasting en vastlopen.

>[!IMPORTANT]
>
>**Afkappingsregels** worden op sandboxniveau geconfigureerd voor een specifiek eindpunt (de opgeroepen URL), maar globaal voor alle journeys van deze sandbox. De bedekking is beschikbaar op zowel gegevensbronnen als douaneacties.
>
>**Beperkingsregels** worden voor productiesandboxen alleen geconfigureerd voor een specifiek eindpunt, maar globaal voor alle journeys in alle sandboxes. U kunt slechts één beperkingsconfiguratie per organisatie hebben. Throtting is alleen beschikbaar voor aangepaste handelingen.

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:

* [Afkappings-API](capping.md)
* [API voor beperken](throttling.md)

Een gedetailleerde beschrijving van de API&#39;s is beschikbaar in [Adobe Journey Optimizer API-documentatie](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Capaciteit gegevensbronnen en aangepaste acties {#capacity}

Voor **externe gegevensbronnen** is het maximum aantal oproepen per seconde beperkt tot 15. Als deze limiet wordt overschreden, worden alle verdere oproepen ofwel afgewezen ofwel in de wachtrij geplaatst, afhankelijk van de gebruikte API. Het is mogelijk om deze limiet te verhogen voor externe privédatabronnen door contact op te nemen met Adobe om het eindpunt op te nemen in de lijst van gewenste personen, maar dit is geen optie voor externe openbare databronnen. * [Leer hoe u databronnen kunt configureren](../datasource/about-data-sources.md).

>[!NOTE]
>
>Als een databron een aangepaste authenticatie gebruikt met een ander eindpunt dan het eindpunt dat voor de databron wordt gebruikt, moet u contact opnemen met Adobe om ook dat eindpunt in de lijst van gewenste personen op te nemen.

Voor **aangepaste acties** moet u de capaciteit van uw externe API evalueren. Als Journey Optimizer bijvoorbeeld 1000 oproepen per seconde verstuurt en uw systeem slechts 100 oproepen per seconde kan ondersteunen, moet u een afkappings- of beperkingsconfiguratie definiëren zodat uw systeem niet verzadigd raakt. [Ontdek hoe u acties kunt configureren](../action/action.md)

## Time-out en opnieuw proberen{#timeout}

Als de het maximum afschilderen of vertragen regel wordt vervuld, dan wordt de onderbrekingsregel toegepast.

In elke reis, kunt u een onderbrekingsduur bepalen. Dit staat u toe om een maximumduur te plaatsen wanneer het roepen van een extern systeem. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. Zie [deze pagina](../building-journeys/journey-gs.md#timeout_and_error).

Deze onderbreking is globaal aan alle externe vraag (externe API vraag in douaneacties en douanegegevensbronnen). De standaardwaarde is 30 seconden.

Tijdens de gedefinieerde time-outduur probeert Journey Optimizer het externe systeem aan te roepen. Na de eerste vraag, kan een maximum van drie herpogingen worden uitgevoerd tot het eind van onderbrekingsduur wordt bereikt. Het aantal pogingen kan niet worden gewijzigd.

Bij elke poging wordt één sleuf gebruikt. Als u een maximum van 100 vraag per seconde hebt en elk van uw vraag vereist twee herpogingen, daalt het tarief aan 30 vraag per seconde (elke vraag gebruikt 3 groeven: de eerste vraag en twee herpogingen).

De waarde voor de time-outduur is afhankelijk van het gebruiksgeval. Als u uw bericht snel wilt verzenden, bijvoorbeeld wanneer de client de winkel binnengaat, wilt u geen lange time-out instellen. Hoe langer de time-out is, hoe meer items in de wachtrij worden geplaatst. Dit kan de prestaties sterk beïnvloeden. Als Journey Optimizer 1000 vraag per seconden uitvoert, kan het houden van 5 of 15 seconden van gegevens het systeem snel overweldigen.

Laten we een voorbeeld nemen voor een time-out van 5 seconden.

* De eerste vraag duurt minder dan 5 seconden: de vraag is succesvol, wordt niet opnieuw uitgevoerd.
* De eerste vraag duurt langer dan 5 seconden: de vraag wordt geannuleerd en er is geen retry. Het wordt geteld als een time-outfout in de rapportage.
* De eerste vraag ontbreekt na 2 seconden (het externe systeem keert een fout terug): 3 seconden worden verlaten voor herpogingen, als het begrenzen van groeven beschikbaar is.
   * Als één van de drie pogingen succesvol vóór het eind van 5 seconden is, wordt de vraag uitgevoerd, en er is geen fout.
   * Als het einde van de time-outduur tijdens de pogingen wordt bereikt, wordt de aanroep geannuleerd en geteld als een time-outfout in de rapportage.

## Veelgestelde vragen{#faq}

**Hoe kan ik een het in kaart brengen of throttling regel vormen? Is er een standaardregel?**

Standaard is er geen regel voor het aftappen of vertragen. De regels worden bepaald op zandbakniveau voor een specifiek eindpunt (geroepen URL), gebruikend het Kappen of het Draaien API. Zie [deze sectie](../configuration/external-systems.md#capping).

**Hoeveel pogingen worden uitgevoerd? Kan ik het aantal pogingen veranderen of een minimumwachttijd tussen pogingen bepalen?**

Voor een bepaalde vraag, kan een maximum van drie pogingen na de eerste vraag worden uitgevoerd, tot het eind van onderbrekingsduur wordt bereikt. Het aantal pogingen en de tijd tussen elke keer opnieuw proberen kunnen niet worden gewijzigd. Zie [deze sectie](../configuration/external-systems.md#timeout).

**Waar kan ik de onderbreking vormen? Is er een maximumwaarde?**

In elke reis, kunt u een onderbrekingsduur bepalen. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. De duur van de onderbreking moet tussen 1 seconde en 30 seconden zijn. Zie [deze sectie](../configuration/external-systems.md#timeout) en [deze pagina](../building-journeys/journey-gs.md#timeout_and_error).