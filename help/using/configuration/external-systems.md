---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer integreren met externe systemen
description: Leer de beste praktijken bij het integreren van Journey Optimizer met externe systemen
role: User
level: Beginner
keywords: extern, API, optimaliseren, aftopping
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 40afc1c0e0ae55dfbec45ff0b22170d6345a8e46
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 1%

---

# Integreren met externe systemen {#external-systems}

Deze pagina bevat de verschillende instructies die Journey Optimizer biedt bij de integratie van een extern systeem, en de aanbevolen procedures: hoe u de beveiliging van uw externe systeem kunt optimaliseren met behulp van de API voor aftopping, hoe u de time-out van de reis kunt configureren en hoe nieuwe pogingen werken.

Met Journey Optimizer kunt u verbindingen met externe systemen configureren via aangepaste gegevensbronnen en aangepaste handelingen. Zo kunt u bijvoorbeeld uw reizen verrijken met gegevens die afkomstig zijn van een extern reserveringssysteem, of berichten verzenden via een systeem van derden, zoals Epsilon of Facebook.

Wanneer u een extern systeem integreert, kunt u verschillende problemen tegenkomen, kan het systeem traag zijn, kan het niet langer reageren of kan het een groot volume mogelijk niet verwerken. Journey Optimizer biedt verschillende instructies om uw systeem te beschermen tegen overbelasting.

Alle externe systemen hebben verschillende prestaties. U moet de configuratie aan uw gebruiksgevallen aanpassen.

Wanneer Journey Optimizer een aanroep naar een externe API uitvoert, worden de technische instructies als volgt uitgevoerd:

1. Er worden afdekregels of vertragingsregels toegepast: als het maximumtarief wordt bereikt, worden de resterende vraag verworpen of een rij gevormd.

2. Time-out en opnieuw proberen: als de het begrenzen regel wordt vervuld, probeert Journey Optimizer om de vraag uit te voeren tot het eind van de onderbrekingsduur wordt bereikt.

## API&#39;s uitlijnen en vertragen {#capping}

### Informatie over API&#39;s voor uitlijnen en draaien

Wanneer het vormen van een gegevensbron of een actie, vestigt u een verbinding aan een systeem om of extra informatie terug te winnen om in uw reizen te gebruiken of berichten of API vraag te verzenden.

Reis-API&#39;s ondersteunen maximaal 5000 gebeurtenissen per seconde, maar sommige externe systemen of API&#39;s hebben mogelijk geen equivalente doorvoer. Om overbelasting van deze systemen te voorkomen, kunt u de **Afbeelding** en **Throttling** API&#39;s om het aantal verzonden gebeurtenissen per seconde te beperken.

Telkens wanneer een API-aanroep door reizen wordt uitgevoerd, loopt deze door de API-engine. Als de limiet die is ingesteld in de API wordt bereikt, wordt de aanroep afgewezen als u de API voor uitsnijden gebruikt, of gedurende maximaal 6 uur in de wachtrij geplaatst en zo snel mogelijk verwerkt in de volgorde waarin deze is ontvangen als u de API voor rotatie gebruikt.

Stel bijvoorbeeld dat u voor uw externe systeem een regel hebt gedefinieerd voor het bijsnijden of vertragen van 100 aanroepen per seconde. Uw systeem wordt opgeroepen door een aangepaste actie tijdens 10 verschillende reizen. Als één reis 200 vraag per seconde ontvangt, zal het de 100 beschikbare groeven gebruiken en zal verwerpen of de 100 resterende groeven in de rij plaatsen. Aangezien het maximumtarief is overschreden, zullen de overige 9 reizen geen slots meer hebben. Deze granulariteit helpt het externe systeem te beschermen tegen overbelasting en vastlopen.

>[!IMPORTANT]
>
>**Afdekregels** worden geconfigureerd op sandboxniveau voor een specifiek eindpunt (de URL wordt aangeroepen), maar globaal voor alle reizen van die sandbox.
>
>**Throtatieregels** alleen geconfigureerd zijn op productiestanddozen, voor een specifiek eindpunt maar globaal voor alle reizen over alle sandboxen. U kunt slechts één throttling configuratie per organisatie hebben.

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:

* [API voor uitlijnen](capping.md)
* [Throttling API](throttling.md)

Een gedetailleerde beschrijving van de API&#39;s is beschikbaar in [Adobe Journey Optimizer API-documentatie](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Gegevensbronnen en aangepaste handelingscapaciteit {#capacity}

Voor **externe gegevensbronnen**, is het maximumaantal oproepen per seconde beperkt tot 15. Als deze limiet wordt overschreden, worden eventuele aanvullende aanroepen genegeerd of in een wachtrij geplaatst, afhankelijk van de gebruikte API. Het is mogelijk om deze grens voor privé externe gegevensbronnen te verhogen door Adobe te contacteren om het eindpunt in de lijst van gewenste personen op te nemen, maar dit is geen optie voor openbare externe gegevensbronnen. * [Leer hoe te om gegevensbronnen te vormen](../datasource/about-data-sources.md).

>[!NOTE]
>
>Als een gegevensbron een douaneauthentificatie met een verschillend eindpunt dan gebruikt voor de gegevensbron gebruikt, moet u Adobe contacteren om dat eindpunt in de lijst van gewenste personen ook te omvatten.

Voor **aangepaste handelingen**, moet u de capaciteit van uw externe API evalueren. Bijvoorbeeld, als Journey Optimizer 1000 vraag per seconde verzendt en uw systeem slechts 100 vraag per seconde kan steunen, moet u een het in kaart brengen of het gooien configuratie bepalen zodat uw systeem niet verzadigt. [Leer hoe u handelingen configureert](../action/action.md)

## Time-out en opnieuw proberen{#timeout}

Als de het maximum afschilderen of vertragen regel wordt vervuld, dan wordt de onderbrekingsregel toegepast.

In elke reis, kunt u een onderbrekingsduur bepalen. Dit staat u toe om een maximumduur te plaatsen wanneer het roepen van een extern systeem. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. Zie [deze pagina](../building-journeys/journey-gs.md#timeout_and_error).

Deze onderbreking is globaal aan alle externe vraag (externe API vraag in douaneacties en de bronnen van douanegegevens). De standaardwaarde is 30 seconden.

Tijdens de gedefinieerde time-outduur probeert Journey Optimizer het externe systeem aan te roepen. Na de eerste vraag, kan een maximum van drie herpogingen worden uitgevoerd tot het eind van onderbrekingsduur wordt bereikt. Het aantal pogingen kan niet worden gewijzigd.

Bij elke poging wordt één sleuf gebruikt. Als u een maximum van 100 vraag per seconde hebt en elk van uw vraag vereist twee herpogingen, daalt het tarief aan 30 vraag per seconde (elke vraag gebruikt 3 groeven: de eerste oproep en twee pogingen).

De waarde voor de time-outduur is afhankelijk van het gebruiksgeval. Als u uw bericht snel wilt verzenden, bijvoorbeeld wanneer de client de winkel binnengaat, wilt u geen lange time-out instellen. Hoe langer de time-out is, hoe meer items in de wachtrij worden geplaatst. Dit kan de prestaties sterk beïnvloeden. Als Journey Optimizer 1000 vraag per seconden uitvoert, kan het houden van 5 of 15 seconden van gegevens het systeem snel overweldigen.

Laten we een voorbeeld nemen voor een time-out van 5 seconden.

* De eerste vraag duurt minder dan 5 seconden: de vraag succesvol is, wordt geen opnieuw uitgevoerd.
* De eerste vraag duurt langer 5 seconden: de oproep wordt geannuleerd en er wordt niet opnieuw geprobeerd. Het wordt geteld als een time-outfout in de rapportage.
* De eerste vraag ontbreekt na 2 seconden (het externe systeem keert een fout terug): 3 seconden over voor nieuwe pogingen, als er afsluitende sleuven beschikbaar zijn.
   * Als één van de drie pogingen succesvol vóór het eind van 5 seconden is, wordt de vraag uitgevoerd, en er is geen fout.
   * Als het einde van de time-outduur tijdens de pogingen wordt bereikt, wordt de aanroep geannuleerd en geteld als een time-outfout in de rapportage.

## Veelgestelde vragen{#faq}

**Hoe kan ik een het in kaart brengen of throttling regel vormen? Is er een standaardregel?**

Standaard is er geen regel voor het aftappen of vertragen. De regels worden bepaald op zandbakniveau voor een specifiek eindpunt (geroepen URL), gebruikend het Kappen of het Draaien API. Zie [deze sectie](../configuration/external-systems.md#capping).

**Hoeveel pogingen worden uitgevoerd? Kan ik het aantal pogingen veranderen of een minimumwachttijd tussen pogingen bepalen?**

Voor een bepaalde vraag, kan een maximum van drie pogingen na de eerste vraag worden uitgevoerd, tot het eind van onderbrekingsduur wordt bereikt. Het aantal pogingen en de tijd tussen elke keer opnieuw proberen kunnen niet worden gewijzigd. Zie [deze sectie](../configuration/external-systems.md#timeout).

**Waar kan ik de onderbreking vormen? Is er een maximumwaarde?**

In elke reis, kunt u een onderbrekingsduur bepalen. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. De time-outduur moet liggen tussen 1 en 30 seconden. Zie [deze sectie](../configuration/external-systems.md#timeout) en [deze pagina](../building-journeys/journey-gs.md#timeout_and_error).