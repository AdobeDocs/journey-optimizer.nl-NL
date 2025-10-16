---
title: Help voor externe gegevens opzoeken
description: Uitgebreide gids voor het gebruiken van de Externe Hulp van Gegevens voor dynamische verpersoonlijking in Adobe Journey Optimizer.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: eae8a09a-5d27-4a80-b21f-7f795d800602
source-git-commit: 87245fffb3ad10d51a7500d006dbe69b1905640e
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 0%

---

# Help voor externe gegevens opzoeken

De `externalDataLookup` hulp in de [!DNL Journey Optimizer] verpersoonlijkingsredacteur kan worden gebruikt om gegevens van een extern eindpunt voor gebruik dynamisch te halen voor het produceren van inhoud voor binnenkomende kanalen zoals de op code-gebaseerde Ervaring, Web en in-app kanalen van het Bericht.

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid).

Als u de hulplijn wilt gebruiken, moet u eerst een handeling definiëren in het menu **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** . Een actie is waar u details over een extern eindpunt, zoals URL, GET vs. methode POST, kopbalparameters, vraagparameters, POST lichaamJSON schema en antwoordJSON schema vormt.

Zodra de Actie is bepaald, kan het allebei worden gebruikt:

* Tijdens reizen wordt in een aangepaste handeling inhoud opgehaald,
* In reizen en binnenkomende campagnes, in een externalDataLookup helper om gegevens in een binnenkomende actie te halen.

## Afvoerkanalen en beperkingen

Raadpleeg ook Aangepaste acties in [!DNL Journey Optimizer] Binnenkomende kanalen voor campagnes en reizen#GuardrailandGuidelines.

* **Standaardonderbreking** - door gebrek, [!DNL Journey Optimizer] gebruikt een onderbreking van 300ms wanneer het roepen van een extern eindpunt. Neem contact op met uw Adobe-vertegenwoordiger om deze time-out voor een eindpunt te verhogen.
* **Bladeren van het schema van de Reactie &amp; uitdrukkingsbevestiging** - in de verpersoonlijkingsredacteur, kunt u niet het schema van de eindpuntreactie doorbladeren wanneer het opnemen van uitdrukkingen. [!DNL Journey Optimizer] valideert geen verwijzingen naar JSON-kenmerken van de reactie die in expressies wordt gebruikt.
* **Gesteunde gegevenstypes voor parameters** - de gesteunde datatypes voor de parameters van de ladingsvariabele die via externalDataLookup helper moeten worden vervangen zijn `String`, `Integer`, `Decimal`, `Boolean`, `listString`, `listInt`, `listInteger`, `listDecimal`.
* **auto-verfrist zich voor bijgewerkte acties** - De veranderingen in een configuratie van de Actie worden niet weerspiegeld in de overeenkomstige ExternalDataLookup vraag in levende campagnes en reizen. Om een verandering om te weerspiegelen, moet u om het even welke levende campagnes of reizen kopiëren of wijzigen die de Actie in een externalDataLookup helper gebruiken.
* **Veranderlijke substitutie** - voor nu, wordt het gebruik van variabelen niet gesteund binnen de externalDataLookup helperparameters.
* **Dynamisch weg** - voor nu, wordt de dynamische weg URL niet gesteund.
* **multi-pass het teruggeven** - multi-pass het teruggeven wordt gesteund.
* **Authentificatie** - voor nu, worden de authentificatieopties in de configuratie van de Actie niet gesteund door de externalDataLookup helper. In de tussentijd kunt u voor API-verificatie op basis van sleutels of andere licentietoetsen voor normale tekst deze als headervelden opgeven in de configuratie van Handeling.

## Een handeling configureren en de hulplijn gebruiken

Voer de volgende stappen uit om een handeling te definiëren en de hulplijn voor personalisatie te gebruiken:

1. Creeer een Actie om het eindpunt voor de raadpleging te vormen. Dit hoeft slechts eenmaal te gebeuren voor elk eindpunt en moet door een technische gebruiker worden gedaan. [ Leer hoe te om een douaneactie ](../action/about-custom-action-configuration.md) te vormen

   Noteer de actie-id en kopieer deze.

   ![](assets/external-data-action.png)

1. Maak een binnenkomende campagne of actie voor reizen. Voor dit voorbeeld, tonen wij hoe te om de hulp externalDataLookup in een op code-gebaseerde Actie JSON van de Ervaring te gebruiken, maar het kan op een verpersoonlijkingsgebied in om het even welk binnenkomend kanaal worden gebruikt.

1. Bewerk de inhoud van de actie, ga naar de functie Helper in de verpersoonlijkingseditor en navigeer naar **[!UICONTROL Helper functions]** > **[!UICONTROL Helpers]** .

1. Klik op de knop `+` om de helper externalDataLookup in te voegen. De hulplijnexpressie wordt ingevoegd in de editor, met plaatsaanduidingswaarden voor de `actionId` en `result` .

   ![](assets/external-data-personalization.png)

   Vervang de plaatsaanduidingswaarden als volgt:

   * `actionId`: plak de eerder gekopieerde handelings-id.
   * `result`: stel de naam van uw keuze in. U zult deze resultaatvariabele gebruiken om tot de opgehaalde inhoud toegang te hebben.

1. Voeg om het even welke veranderlijke parameterwaarden toe die als deel van de eindpuntvraag moeten worden overgegaan. Hier ziet u bijvoorbeeld hoe u een taalparameter en een max.-itemparameter kunt doorgeven.

   ![](assets/external-data-personalization-example.png)

1. Gebruik de resultaatvariabele om tot de opgehaalde gegevens toegang te hebben en het in de inhoud voor de binnenkomende actie op te nemen. Hier ziet u bijvoorbeeld hoe u een JSON-array met items kunt retourneren die van het eindpunt zijn opgehaald.

   ![](assets/external-data-personalization-result.png)

## Werking

### Uitvoering van runtime

Wanneer een binnenkomende actie een externalDataLookup helper omvat, wordt het eindpunt dynamisch geroepen op het ogenblik het [!DNL Journey Optimizer] verpersoonlijkingsverzoek wordt ontvangen en door AEP Edge Network verwerkt.

Dit betekent het externe eindpunt minstens zo veel gelijktijdige lading en productie moet kunnen behandelen aangezien de cliënt voor de bepaalde oppervlakte naar AEP Edge Network verzendt.

### Syntaxis

`{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}`

### Parameters doorgeven

Wanneer het externe eindpunt wordt geroepen, zullen alle constante kopbalwaarden, vraagparameters en de waarde van de verzoeklading die in de Actie wordt bepaald met de waarden worden verzonden die in de configuratie van de Actie worden gegeven.

Voor om het even welke veranderlijke kopbalwaarden, vraag/wegparameters of verzoek ladingswaarden, kunt u waarden dynamisch overgaan gebruikend parameters tot de externalDataLookup helper.

Parameternamen:

* Parameters koptekst: `header.<parameter-name>`
* Query-parameters: `query.<parameter-name>`
* Payload-parameters: `payload.<parameter-name>`
* Padparameters: `dynamic_path.<parameter-name>`

Bijvoorbeeld:

```
{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}`
```

Parameterwaarden kunnen vaste waarden zijn of ze kunnen worden gepersonaliseerd door te verwijzen naar profielvelden of andere contextafhankelijke kenmerken, bijvoorbeeld:

```
{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
```

Payload-parameters kunnen worden opgegeven met behulp van puntnotatie voor verwijzing naar geneste JSON-kenmerken, bijvoorbeeld:

```
{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}
```

### Toegang tot het resultaat

Om tot de gegevens toegang te hebben die van een externe vraag van de eindpuntraadpleging worden gehaald, kunt u gebieden van verwijzingen voorzien die in de antwoordlading in de definitie van de Actie worden bepaald gebruikend verpersoonlijkingsuitdrukkingen en helperfuncties.

Bijvoorbeeld, als de antwoordlading in de Actie als dit kijkt:

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

Vervolgens kunt u bijvoorbeeld de beschrijving van de eerste video ophalen en openen in een op code gebaseerde HTML-actie Experience, zoals:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

U kunt bijvoorbeeld de items ophalen en doorlopen om een itemarray te retourneren in een JSON-actie op basis van code zoals deze:

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

## Problemen oplossen

### Time-outs en foutafhandeling

[!DNL Journey Optimizer] gebruikt een strikte onderbreking wanneer het roepen van het externe eindpunt om laag-latentie, hoge productieprestatiekenmerken voor Adobe Experience Platform Edge Network te handhaven.

Als de eindpunttijden uit zijn of er een andere soort fout die het eindpunt bereikt, zal de resultaatvariabele leeg zijn. Verwijzingen naar kenmerken in de resultaatvariabele zijn in dit geval ook leeg. Als u het kenmerk gewoon in de inhoud weergeeft, wordt het kenmerk leeg weergegeven. Als u een arraykenmerk in het resultaat wilt doorlopen, worden geen items geretourneerd.

Als u time-outs of fouten beter wilt afhandelen door fallback-inhoud weer te geven, kunt u controleren of het resultaat van de zoekopdracht leeg is en in dat geval de fallback-inhoud weergeven.

U kunt bijvoorbeeld een fallback-waarde weergeven voor één kenmerk zoals:

```
First video description: {%=result.videos[0].description ?: "none found" %}
```

Of u kunt voorwaardelijk een volledig blok van inhoud als dit teruggeven:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
{%#if result%}
   ... do something with result ...
{%else%}
    ... return fallback content ...
{%/if%}
```

### Foutopsporing

Voor hulp bij foutopsporing worden time-out- en foutgegevens voor externe gegevenszoekopdrachten opgenomen in de Edge Delivery-weergave in Adobe Experience Platform Assurance. Als u de verwachte resultaten voor een externeDataLookup helper in een binnenkomende actie niet ziet, kunt u een zitting van Assurance beginnen, een [!DNL Journey Optimizer] vraag van een Web of mobiele implementatie in werking stellen, en de mening van Edge Delivery gebruiken om onderbreking of foutendetails te controleren.

Bijvoorbeeld:

Onder de sectie Edge Delivery van het betrouwbaarheidsspoor als deel van uitvoeringsdetails is een nieuw blok customActions toegevoegd met verzoek en reactiedetails gelijkend op hieronder. De sectie Fouten zou bij het zuiveren moeten helpen als er om het even welke kwesties terwijl het uitvoeren van douaneactie waren

![](assets/external-data-troubleshoot.png " width=50% ")

## Veelgestelde vragen

* Hoe te om een contextafhankelijk attribuut van het verzoek als parameter tot een externe gegevensraadpleging over te gaan?

  Met het menu Contextafhankelijke kenmerken > DataStream > Gebeurtenis bladert u door het schema Experience Event dat u gebruikt en voegt u het relevante kenmerk in als parameterwaarde zoals deze:

  ```
  {{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}
  ```

* Doet [!DNL Journey Optimizer] om het even welk caching van externe eindpuntreacties?

  Momenteel niet. Deze functie wordt in de toekomst ondersteund.
