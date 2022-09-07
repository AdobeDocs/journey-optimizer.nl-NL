---
title: Aanbiedingen leveren met de Edge-API voor besluitvorming
description: Met de Adobe Experience Platform Web SDK kunt u persoonlijke aanbiedingen ophalen en renderen die u hebt gemaakt met behulp van API's of de aanbiedingsbibliotheek.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 1%

---

# Aanbiedingen leveren met de Edge-API voor besluitvorming {#edge-decisioning-api}

## Aan de slag en voorwaarden {#edge-overview-and-prerequisites}

De [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) is een client-side JavaScript-bibliotheek waarmee Adobe Experience Cloud-klanten via het Edge Network van Experience Platforms kunnen communiceren met de verschillende services in de Experience Cloud.

De SDK van het Web van de Experience Platform steunt het vragen van de verpersoonlijkingsoplossingen bij Adobe, met inbegrip van Beslissingsbeheer, die u toestaat om gepersonaliseerde aanbiedingen terug te winnen en terug te geven die u gebruikend APIs of de Bibliotheek van de Aanbieding hebt gecreeerd. Raadpleeg de documentatie bij de [een aanbieding maken](../../get-started/starting-offer-decisioning.md).

Er zijn twee manieren om het besluitvormingsbeheer uit te voeren met de [Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Eén manier is gericht op ontwikkelaars en vereist kennis van websites en programmering. De andere manier is door de Adobe Experience Platform-gebruikersinterface te gebruiken voor het instellen van aanbiedingen waarbij alleen naar een klein script moet worden verwezen in de koptekst van de pagina HTML.

Raadpleeg de documentatie bij [beslissingsbeheer](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) voor meer informatie over hoe te om gepersonaliseerde aanbiedingen te leveren gebruikend het Web SDK van het Platform.

>[!NOTE]
>
>Het gebruik van Beslissingsbeheer in Adobe Experience Platform Web SDK is alleen beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Als u deze functie wilt gebruiken, neemt u contact op met de Adobe-accountmanager.

## Adobe Experience Platform Web SDK {#aep-web-sdk}

SDK van het Web van het Platform vervangt de volgende SDKs:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

De SDK heeft deze bibliotheken niet met elkaar gecombineerd en is een nieuwe implementatie. Als u dit wilt gebruiken, moet u eerst de volgende stappen uitvoeren:

1. Zorg ervoor dat uw organisatie over de juiste machtigingen beschikt om de SDK te gebruiken en dat u de machtigingen correct hebt geconfigureerd.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Uw gegevensstroom configureren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) op het tabblad Gegevensverzameling in uw account in de Adobe Experience Cloud.

1. Installeer de SDK. Er zijn meerdere methoden om dit te doen, die op de [De SDK-pagina installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). Deze pagina gaat verder met elke andere implementatiemethode.

Als u de SDK wilt gebruiken, hebt u een [schema](../../../start/get-started-schemas.md) en [datastream](../../../start/get-started-datasets.md) gedefinieerd.

<!-- ****TODO - Configure schema**** -->

Om aanbiedingen te personaliseren, moet u uw personalisatie/profielen afzonderlijk vormen.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Voer een van de volgende twee stappen uit om de SDK voor beslissingsbeheer te configureren:

## Optie 1 - De tagextensie en -implementatie installeren met Starten

Deze optie is gebruiksvriendelijker voor mensen die minder ervaring hebben met coderen.

1. [Een tag-eigenschap maken](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [De insluitcode toevoegen](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Installeer en vorm de uitbreiding van SDK van het Web van het Platform met de Datastream u door de configuratie van &quot;Datstream&quot;dropdown te selecteren creeerde. Zie de documentatie op [extensions](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![Extensie configureren](../../assets/configure-sdk-extension.png)

1. Maak de noodzakelijke [Gegevenselementen](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). Bij het absolute minimum, moet u een Identiteitskaart van SDK van het Web van het Platform en een gegevenselement van de Objecten van SDK van het Web van het Platform XDM tot stand brengen.

   ![Identiteitskaart](../../assets/sdk-identity-map.png)

   ![XDM-object](../../assets/xdm-object.png)

1. Maak uw [Regels](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Voeg een Platform SDK toe verzendt de actie van de Gebeurtenis en voegt relevante decisionsScopes aan de configuratie van die actie toe

   ![Aanbieding renderen](../../assets/rule-render-offer.png)

   ![Aanvraag](../../assets/rule-request-offer.png)

1. [Maken en publiceren](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) een bibliotheek met alle relevante regels, gegevenselementen en extensies die u hebt geconfigureerd.

## Optie 2 - Handmatig implementeren met behulp van de geïntegreerde zelfstandige versie

Hier zijn de stappen nodig om besluitvormingsbeheer te gebruiken gebruikend de prebuilt standalone installatie van Web SDK. In deze handleiding wordt ervan uitgegaan dat dit de eerste keer is dat u de SDK implementeert, zodat alle stappen mogelijk niet op u van toepassing zijn. Deze gids veronderstelt ook enige ontwikkelervaring.

Neem het volgende JavaScript-fragment op uit Option 2: De vooraf gebouwde stand-alone versie op [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) in de `<head>` van uw pagina HTML.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

U hebt twee id&#39;s nodig vanuit uw Adobe-account om de SDK-configuratie in te stellen: de edgeConfigId en uw orgId. edgeConfigId is het zelfde als uw identiteitskaart DataStream, die u in de Eerste vereisten zou moeten gevormd hebben.

Ga naar Gegevensverzameling en selecteer uw DataStream om de edgeConfigID/datastream-id te zoeken. Ga naar uw profiel om uw orgId te zoeken.

De SDK in JavaScript configureren volgens de instructies op deze pagina. U zult altijd edgeConfigId en orgId in de configuratiefunctie gebruiken. De documentatie beschrijft ook welke facultatieve parameters voor uw configuratie bestaan. De uiteindelijke configuratie ziet er misschien ongeveer als volgt uit:

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

Installeer de extensie Foutopsporing Chrome voor gebruik met foutopsporing. Dat is hier te vinden: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Meld u vervolgens aan bij uw account in het foutopsporingsprogramma. Ga vervolgens naar Logs en controleer of u bent verbonden met de juiste werkruimte. Kopieer nu de base64 gecodeerde versie van het beslissingsbereik van uw aanbieding.

Wanneer u uw website bewerkt, neemt u het script op met de configuratie en de `sendEvent` functie om het beslissingsbereik naar Adobe te sturen.

**Voorbeeld**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

Zie het volgende voorbeeld voor een voorbeeld van hoe te om de reactie te behandelen:

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

Met het foutopsporingsprogramma kunt u controleren of u verbinding hebt gemaakt met het Edge-netwerk.

>[!NOTE]
>
>Als u geen verbinding met de rand ziet in de logboeken, moet u de advertentieblokkering mogelijk uitschakelen.

Ga terug naar de manier waarop je voorstel hebt gemaakt en de gebruikte opmaak. Op basis van de criteria die in het besluit zijn opgenomen, wordt een voorstel met de informatie die u hebt opgegeven bij het maken van het voorstel in de Adobe Experience Platform, aan u teruggestuurd.

In dit voorbeeld is de JSON die moet worden geretourneerd:

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Verwerk het reactieobject en parseer de benodigde gegevens. Aangezien u veelvoudige besluitvormingswerkingsgebied in één kunt verzenden `sendEvent` vraag, zou uw reactie lichtjes verschillend kunnen kijken.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

In dit voorbeeld was het pad dat nodig was om de aanbiedingsspecifieke details op de webpagina af te handelen en te gebruiken: `result['decisions'][0]['items'][0]['data']['content']`

De JS-variabelen instellen:

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## Beperkingen

Sommige aanbodbeperkingen worden momenteel niet ondersteund door de mobiele Edge-workflows voor beleving, bijvoorbeeld Afdekkingen. De waarde van het gebied van het Afschilderen specificeert het aantal tijden een aanbieding over alle gebruikers kan worden voorgesteld. Zie voor meer informatie [Beperkingen aan een aanbieding toevoegen](../../offer-library/add-constraints.md#capping).
