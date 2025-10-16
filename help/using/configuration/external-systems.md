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
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '1615'
ht-degree: 18%

---

# Integreren met externe systemen {#external-systems}

Deze pagina bevat de verschillende instructies die Journey Optimizer biedt bij de integratie van een extern systeem, evenals de beste werkwijzen: hoe u de beveiliging van uw externe systeem kunt optimaliseren met behulp van de API voor plafonnering, hoe u de time-out van de reis kunt configureren en hoe nieuwe pogingen werken.

Met Journey Optimizer kunt u verbindingen met externe systemen configureren via aangepaste gegevensbronnen en aangepaste handelingen. Zo kunt u bijvoorbeeld uw reizen verrijken met gegevens die afkomstig zijn van een extern reserveringssysteem, of berichten verzenden via een systeem van derden, zoals Epsilon of Facebook.

Wanneer u een extern systeem integreert, kunt u verschillende problemen tegenkomen, kan het systeem traag zijn, kan het niet langer reageren of kan het een groot volume mogelijk niet verwerken. Journey Optimizer biedt verschillende instructies om uw systeem te beschermen tegen overbelasting.

Alle externe systemen hebben verschillende prestaties. U moet de configuratie aan uw gebruiksgevallen aanpassen.

Wanneer Journey Optimizer een aanroep naar een externe API uitvoert, worden de technische instructies als volgt uitgevoerd:

1. De het in kaart brengen of throttling regels worden toegepast: als het maximumtarief wordt bereikt, worden de resterende vraag verworpen of een rij gevormd.

1. Time-out en probeer het opnieuw: als de begrenzende of vertragingsregel wordt vervuld, probeert Journey Optimizer de vraag uit te voeren tot het eind van de onderbrekingsduur wordt bereikt.

>[!TIP]
>
>We raden u aan om minstens een buffer van één minuut te laten staan tussen de periode van de symbolische vervaldatum van de externe API en de Journey Optimizer-instelling [`cacheDuration` ](../datasource/external-data-sources.md#custom-authentication-access-token) , met name bij zware werklasten, om te voorkomen dat de vervaldatumproblemen en 401 fouten niet worden opgelost.

## API&#39;s uitlijnen en vertragen {#capping}

### Informatie over API&#39;s voor uitlijnen en draaien

Wanneer u een databron of een actie configureert, maakt u een verbinding met een systeem om extra informatie op te halen voor gebruik in uw journeys of om berichten of API-oproepen te versturen.

Journey-API&#39;s ondersteunen tot 5.000 gebeurtenissen per seconde, maar sommige externe systemen of API&#39;s hebben mogelijk geen equivalente verwerkingscapaciteit. Om het overbelasten van deze systemen te verhinderen, kunt u het **Aftappen** en **Throttling** APIs gebruiken om het aantal gebeurtenissen te beperken die per seconde worden verzonden.

Telkens wanneer een API-oproep wordt uitgevoerd door journeys, passeert deze de API-engine. Als de limiet die is ingesteld in de API wordt bereikt, wordt de aanroep afgewezen als u de API voor uitsnijden gebruikt, of gedurende maximaal 6 uur in de wachtrij geplaatst en zo snel mogelijk verwerkt in de volgorde waarin deze is ontvangen als u de API voor rotatie gebruikt.

Bijvoorbeeld, laten wij zeggen dat u een het begrenzen of vertragen regel van 200 vraag per seconde voor uw extern systeem hebt bepaald. Uw systeem wordt opgeroepen door een aangepaste actie in 10 verschillende journeys. Indien één journey 300 oproepen per seconde ontvangt, gebruikt deze de 200 beschikbare slots en de 100 resterende slots verwijderen of in een wachtrij plaatsen. Aangezien het maximumaantal is overschreden, hebben de andere 9 journeys geen slot meer. Deze granulariteit helpt het externe systeem te beschermen tegen overbelasting en vastlopen.

>[!IMPORTANT]
>
>**het Bedekken van regels** wordt gevormd op zandbakniveau, voor een specifiek eindpunt (geroepen URL) maar globaal aan alle reizen van die zandbak. De bedekking is beschikbaar op zowel gegevensbronnen als douaneacties.
>
>**Beperkingsregels** worden voor productiesandboxen alleen geconfigureerd voor een specifiek eindpunt, maar globaal voor alle journeys in alle sandboxes. U kunt slechts één throttling configuratie per organisatie hebben. Throtting is alleen beschikbaar voor aangepaste handelingen.
>
>De **maxCallsCount** waarde moet groter zijn dan 1.

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:

* [Afkappings-API](capping.md)
* [API voor beperken](throttling.md)

Een gedetailleerde beschrijving van APIs is beschikbaar in [ documentatie van Adobe Journey Optimizer APIs ](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Capaciteit gegevensbronnen en aangepaste acties {#capacity}

Voor **externe gegevensbronnen** is het maximum aantal oproepen per seconde beperkt tot 15. Als deze limiet wordt overschreden, worden alle verdere oproepen ofwel afgewezen ofwel in de wachtrij geplaatst, afhankelijk van de gebruikte API. Het is mogelijk om deze limiet te verhogen voor externe privédatabronnen door contact op te nemen met Adobe om het eindpunt op te nemen in de lijst van gewenste personen, maar dit is geen optie voor externe openbare databronnen. * [Leer hoe u databronnen kunt configureren](../datasource/about-data-sources.md).

>[!NOTE]
>
>Als een databron een aangepaste authenticatie gebruikt met een ander eindpunt dan het eindpunt dat voor de databron wordt gebruikt, moet u contact opnemen met Adobe om ook dat eindpunt in de lijst van gewenste personen op te nemen.

Voor **aangepaste acties** moet u de capaciteit van uw externe API evalueren. Bijvoorbeeld, als Journey Optimizer 1000 vraag per seconde verzendt en uw systeem slechts 200 vraag per seconde kan steunen, moet u een het maximum bepalen of het vertragen configuratie zodat uw systeem niet verzadigt. [Ontdek hoe u acties kunt configureren](../action/action.md)

>[!NOTE]
>
>Aangezien de reacties nu worden gesteund, zou u douaneacties in plaats van gegevensbronnen voor externe gegevensbronnen moeten gebruiken-gevallen. Voor meer informatie over reacties, zie deze [ sectie ](../action/action-response.md)

## Eindpunten met een langzame responstijd {#response-time}

Wanneer een eindpunt een reactietijd meer dan 0.75 seconden heeft, worden zijn vraag van de douaneactie verpletterd door de specifieke **langzame dienst van de douaneactie** in plaats van de standaarddienst.

Deze trage dienst van de douaneactie past een het maximum van 150.000 vraag toe om de 30 seconden. De limiet wordt afgedwongen via een schuifvenster, dat op elke milliseconde binnen die periode van 30 seconden kan beginnen. Zodra het venster volledig is, worden de extra vraag verworpen met het begrenzen van fouten. Het systeem wacht niet op het volgende vaste interval, maar begint onmiddellijk na het bereiken van de drempel van 30 seconden te begrenzen.

Omdat de langzame eindpunten vertragingen over alle een rij gevormde acties in de pijpleiding kunnen veroorzaken, wordt het geadviseerd om douaneacties met eindpunten niet te vormen die langzame reactietijden hebben. Verpletterend dergelijke acties aan de langzame dienst helpt algemene systeemprestaties beschermen en verhindert toegevoegde latentie voor andere douaneacties.

## Time-out en opnieuw proberen {#timeout}

Als de het maximum afschilderen of vertragen regel wordt vervuld, dan wordt de onderbrekingsregel toegepast.

In elke reis, kunt u een onderbrekingsduur bepalen. Dit staat u toe om een maximumduur te plaatsen wanneer het roepen van een extern systeem. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. Zie [deze pagina](../building-journeys/journey-properties.md#timeout_and_error).

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

Om het in kaart brengen of het vertragen regels tot stand te brengen, gelieve te verwijzen naar [ deze sectie ](../configuration/external-systems.md#capping). Door gebrek, is er geen throttling regel maar een maximum van 300.000 vraag over één minuut die voor alle douaneacties, per gastheer en per zandbak wordt bepaald. Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen.

**hoeveel pogingen worden uitgevoerd? Kan ik het aantal pogingen veranderen of een minimumwachttijdperiode tussen pogingen bepalen?**

Voor een bepaalde vraag, kan een maximum van drie pogingen na de eerste vraag worden uitgevoerd, tot het eind van onderbrekingsduur wordt bereikt. Het aantal pogingen en de tijd tussen elke keer opnieuw proberen kunnen niet worden gewijzigd. Zie [deze sectie](../configuration/external-systems.md#timeout).

**waar kan ik onderbreking vormen? Is er een maximumwaarde?**

In elke reis, kunt u een onderbrekingsduur bepalen. De duur van de onderbreking wordt gevormd in de eigenschappen van een reis. De duur van de onderbreking moet tussen 1 seconde en 30 seconden zijn. Verwijs naar [ deze sectie ](../configuration/external-systems.md#timeout) en [ deze pagina ](../building-journeys/journey-properties.md#timeout_and_error).

**wat is het maximum aantal verbindingen die door Journey Optimizer worden geopend wanneer de douaneacties worden gebruikt?**

Met de IP toegelaten volmacht en een throttling configuratie die op het gerichte eindpunt wordt bepaald, is het aantal verbindingen gebaseerd op het tarief (die schattingen, niet gewaarborgde aantallen zijn):

* tussen 200 en 2000 c/s: 50 aansluitingen
* tussen 2000 en 3000: 75 aansluitingen
* tussen 3000 en 4000: 100 aansluitingen
* tussen 4000 en 5000: 125 aansluitingen

Als geen throttling configuratie op een eindpunt wordt bepaald, wordt de motor van Journey Optimizer ontworpen om omhoog te schrapen en het kan aan een hoog aantal verbindingen (meer dan 2.000) krijgen. Om beperkt aantal verbindingen te krijgen, moeten de klanten een throttling configuratie gebruiken.
