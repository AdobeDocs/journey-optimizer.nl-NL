---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud personaliseren met behulp van gegevens van een extern eindpunt
description: Leer hoe te om gegevens van een extern eindpunt dynamisch te halen om binnenkomende inhoud te personaliseren.
badge: label="Beperkte beschikbaarheid" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---


# Inhoud personaliseren met behulp van gegevens van een extern eindpunt {#data-endpoint}

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid).

Journey Optimizer staat u toe aan hefboomwerking gegevens van een extern eindpunt om uw inhoud in binnenkomende kanalen zoals de op code-gebaseerde Ervaring, Web en in-App kanalen van het Bericht te personaliseren.

Hiervoor is een speciale hulpfunctie, `externalDataLookup` , beschikbaar in de personalisatie-editor. Om helper te gebruiken, moet u a [!DNL Journey Optimizer] **Actie** eerst bepalen waar u details over het externe eindpunt vormt.

## Lees hier meer

### Uitvoering van runtime

Wanneer een binnenkomende actie een externalDataLookup helper omvat, wordt het eindpunt dynamisch geroepen op het ogenblik het verpersoonlijkingsverzoek wordt ontvangen en door [!DNL Adobe Experience Platform] Edge Network verwerkt. Dit betekent het externe eindpunt minstens zo veel gelijktijdige lading en productie moet kunnen behandelen aangezien de cliënt voor de bepaalde oppervlakte naar AEP Edge Network verzendt.

### Verificatie

De opties van de authentificatie in de configuratie van de Actie worden momenteel niet gesteund door externalDataLookup helper.
In de tussentijd kunt u voor API-verificatie op basis van sleutels of andere licentietoetsen voor normale tekst deze als headervelden opgeven in de configuratie van Handeling.
ALLEEN voor Adobe-interne eindpunten: neem contact op met AJO Engineering om op servicetoken gebaseerde verificatie voor een eindpunt in te schakelen.

### Afbeeldingen en beperkingen

Gelieve te verwijzen naar de Acties van de Douane in de Binnenkomende Campagnes van Kanalen van AJO en ook naar Reizen#GuardrailandGuidelines.

AJO gebruikt standaard een time-out van 300 ms wanneer een extern eindpunt wordt aangeroepen. Neem contact op met AJO Engineering om deze time-out voor een eindpunt te vergroten.
In de Personalization Editor kunt u in AJO niet door het schema van de eindpuntreactie bladeren wanneer u expressies invoegt en worden verwijzingen naar JSON-kenmerken van de reactie die in expressies wordt gebruikt, niet gevalideerd.
De ondersteunde datatypen voor parameters van de payload-variabele die via de helper externalDataLookup moeten worden vervangen, zijn String, Integer, Decimaal, Boolean, listString, listInt, listInteger, listDecimal
Wijzigingen in een actieconfiguratie worden niet weerspiegeld in overeenkomende ExternalDataLookup-aanroepen in live campagnes en reizen. Om een verandering om te weerspiegelen, moet u om het even welke levende campagnes of reizen kopiëren of wijzigen die de Actie in een externalDataLookup helper gebruiken.
Het gebruik van variabelen wordt nog niet ondersteund binnen externe parameters van de opzoekhelper.
Dynamisch URL-pad wordt momenteel niet ondersteund.  - Verbeteringen voor inkomende aangepaste handelingen#DynamicPathSegments

## Een handeling maken

Creeer een Actie om het eindpunt voor de raadpleging te vormen. Dit hoeft slechts eenmaal te gebeuren voor elk eindpunt en moet door een technische gebruiker worden gedaan. Zie deze pagina.

Dezelfde handeling kan worden gebruikt in een **[!UICONTROL Custom Action]** -activiteit om inhoud op te halen tijdens een rit, en in een `externalDataLookup` -hulpfunctie om gegevens op te halen in een binnenkomende actie tijdens een rit of campagne.

Blader naar het menu **[!UICONTROL Administration]** / **[!UICONTROL Configurations]** .

Noteer de id van de handeling en kopieer deze voor gebruik in stap 6.


## Uw inhoud aanpassen met opgehaalde gegevens

### Voeg de hulpfunctie aan uw inhoud toe

1. Maak een binnenkomende campagne of actie voor reizen en bewerk de inhoud ervan.

1. Bepaal de plaats van de inhoud waar u gebruiksgegevens wilt gebruiken die van het externe eindpunt worden voorzien en tot de verpersoonlijkingsredacteur toegang hebben.

1. Selecteer het menu Helper-functies en zoek de functie `externalDataLookup` helper.

1. Selecteer deze optie om de bijbehorende syntaxis in uw code in te voegen en de parameterwaarden `actionId` en `result` als volgt te vervangen:

   * `actionId` : plak de gekopieerde handelings-id tijdens het maken van de handeling.
   * `result`: stel deze parameter in op de naam van uw keuze. U zult deze resultaatvariabele gebruiken om tot de opgehaalde inhoud toegang te hebben.

1. Voeg om het even welke veranderlijke parameterwaarden toe die als deel van de eindpuntvraag moeten worden overgegaan. Hier ziet u bijvoorbeeld hoe u een taalparameter en een max.-itemparameter kunt doorgeven.

### Persoonlijk maken met opgehaalde gegevens

Om tot de gegevens toegang te hebben die van een externe vraag van de eindpuntraadpleging worden gehaald, kunt u gebieden van verwijzingen voorzien die in de antwoordlading in de definitie van de Actie worden bepaald gebruikend verpersoonlijkingsuitdrukkingen en helperfuncties.

Gebruik de variabele `result` om toegang te krijgen tot de opgehaalde gegevens en deze in te voegen in de inhoud voor de binnenkomende actie. Hier ziet u bijvoorbeeld hoe u een JSON-array met items kunt retourneren die van het eindpunt zijn opgehaald.

Neem het onderstaande voorbeeld, waar de antwoordlading in de Actie als volgt is gevormd:

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Personalization voorbeeld 1 - Geef de beschrijving van de eerste video weer in een op code gebaseerde HTML-actie Experience:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization-voorbeeld 2 - Retourneer een itemarray in een JSON-actie op basis van code:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Time-outs en foutafhandeling

AJO gebruikt een strikte onderbreking wanneer het roepen van het externe eindpunt om laag-latentie, hoge productieprestatiekenmerken voor AEP Edge Network te handhaven.

Als de eindpunttijden uit zijn of er een andere soort fout die het eindpunt bereikt, zal de resultaatvariabele leeg zijn. Verwijzingen naar kenmerken in de resultaatvariabele zijn in dit geval ook leeg. Als u het kenmerk gewoon in de inhoud weergeeft, wordt het kenmerk leeg weergegeven. Als u een arraykenmerk in het resultaat wilt doorlopen, worden geen items geretourneerd.

Als u time-outs of fouten beter wilt afhandelen door fallback-inhoud weer te geven, kunt u controleren of het resultaat van de zoekopdracht leeg is en in dat geval de fallback-inhoud weergeven.

U kunt bijvoorbeeld een fallback-waarde weergeven voor één kenmerk zoals:

Eerste videobeschrijving: {%=result.videos [ 0 ].description ?: &quot;niets vond&quot; %)


Of u kunt voorwaardelijk een volledig blok van inhoud als dit teruggeven:

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
... iets doen met resultaat..
{%else%}
... terugvalinhoud..
{%/if%}
Foutopsporing
Voor hulp bij foutopsporing worden time-out- en foutgegevens voor externe gegevenszoekopdrachten opgenomen in de Edge Delivery-weergave in AEP Assurance. Als u de verwachte resultaten voor een externalDataLookup-hulp in een binnenkomende actie niet ziet, kunt u een Assurance-sessie starten, een AJO-aanroep starten vanuit een web- of mobiele implementatie en de Edge Delivery-weergave gebruiken om te controleren op time-out- of foutdetails.

Bijvoorbeeld:

In het gedeelte Edge Delivery over het betrouwbaarheidsinterval als onderdeel van uitvoeringsdetails is een nieuw blok customActions toegevoegd met

dezelfde vraag- en antwoordgegevens als hieronder. De sectie Fouten zou bij het zuiveren moeten helpen als er om het even welke kwesties terwijl het uitvoeren van douaneactie waren

## Veelgestelde vragen

+++Hoe te om een contextueel attribuut van het verzoek als parameter tot een externe gegevensraadpleging over te gaan?

Gebruik het menu Contexual Attributes > DataStream > Event om door het schema Experience Event te bladeren dat u gebruikt en voeg het relevante kenmerk als parameterwaarde als volgt in:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++Doet AJO om het even welk caching van externe eindpuntreacties?

Momenteel niet. Deze functie wordt in de toekomst ondersteund.

+++









Syntaxis
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Parameters doorgeven
Wanneer het externe eindpunt wordt geroepen, zullen alle constante kopbalwaarden, vraagparameters en de waarde van de verzoeklading die in de Actie wordt bepaald met de waarden worden verzonden die in de configuratie van de Actie worden gegeven.

Voor om het even welke veranderlijke kopbalwaarden, vraag/wegparameters of verzoek ladingswaarden, kunt u waarden dynamisch overgaan gebruikend parameters tot de externalDataLookup helper.

Parameternamen:

Parameters koptekst: koptekst.<parameter-name>
Query-parameters: query.<parameter-name>
Payload-parameters: payload.<parameter-name>
Padparameters: dynamic_path.<parameter-name>
Bijvoorbeeld:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
Parameterwaarden kunnen vaste waarden zijn of ze kunnen worden gepersonaliseerd door te verwijzen naar profielvelden of andere contextafhankelijke kenmerken, bijvoorbeeld:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
Payload-parameters kunnen worden opgegeven met behulp van puntnotatie voor verwijzing naar geneste JSON-kenmerken, bijvoorbeeld:

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}