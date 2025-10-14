---
solution: Journey Optimizer
product: journey optimizer
title: Afkappings-API
description: Meer informatie over het werken met de API voor uitlijnen
feature: Journeys, API
role: Developer
level: Beginner
keywords: extern, API, optimaliseren, aftopping
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 13af123030449d870f44f3470710b0da2c6f4775
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 6%

---

# Werken met de API voor uitsnijden {#work}

Met de API voor uitsnijden kunt u uw configuraties voor uitlijnen maken, configureren en controleren.

Deze sectie bevat algemene informatie over het werken met de API. Een gedetailleerde API beschrijving is beschikbaar in [&#x200B; documentatie van Adobe Journey Optimizer APIs &#x200B;](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

## API-beschrijving van uitlijnen en Postman-verzameling {#description}

In de onderstaande tabel staan de beschikbare opdrachten voor de API voor aftiteling. De gedetailleerde informatie met inbegrip van verzoeksteekproeven, parameters, en antwoordformaten is beschikbaar in de [&#x200B; documentatie van Adobe Journey Optimizer APIs &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/journeys/){target="_blank"}.

| Methode | Pad | Beschrijving |
|---|---|---|
| [!DNL POST] | list/endConfigs | Krijg een lijst van de eindpunt die configuraties begrenzen |
| [!DNL POST] | /endConfigs | Creeer een eindpunt het bedekken configuratie |
| [!DNL POST] | /endConfigs/`{uid}`/opstellen | Implementeer een configuratie voor het afdekken van eindpunten |
| [!DNL POST] | /endConfigs/`{uid}`/undeploy | Maak een eindpunt onbruikbaar dat configuratie begrenst |
| [!DNL POST] | /endConfigs/`{uid}`/canDeploy | Controle als een eindpunt het begrenzen configuratie kan worden opgesteld of niet |
| [!DNL PUT] | /endConfigs/`{uid}` | Een configuratie voor het afdekken van eindpunten bijwerken |
| [!DNL GET] | /endConfigs/`{uid}` | Retrireer een eindpunt dat configuratie begrenst |
| [!DNL DELETE] | /endConfigs/`{uid}` | Een configuratie voor een uitlijningselement verwijderen |

Wanneer een configuratie wordt gecreeerd of bijgewerkt, automatisch wordt een controle uitgevoerd om de syntaxis en de integriteit van de lading te waarborgen.
Als sommige problemen voorkomen, keert de verrichting waarschuwing of fouten terug om u te helpen de configuratie verbeteren.

Bovendien is een inzameling van Postman beschikbaar [&#x200B; hier &#x200B;](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) om u in uw het testen configuratie te helpen.

Deze inzameling is opstelling geweest om de Variabele die inzameling van Postman te delen via __[de Integraties van de Console van Adobe I/O wordt geproduceerd &#x200B;](https://console.adobe.io/integrations) > probeert het uit > Download voor Postman__, die een dossier van het Milieu van Postman met de geselecteerde integratiewaarden produceert.

Eenmaal gedownload en geüpload naar Postman moet u drie variabelen toevoegen: `{JO_HOST}`,`{BASE_PATH}` en `{SANDBOX_NAME}`.
* `{JO_HOST}` : [!DNL Journey Optimizer] URL van gateway.
* `{BASE_PATH}` : ingangspunt voor de API.
* `{SANDBOX_NAME}`: de header **x-sandbox-name** (bijvoorbeeld &#39;prod&#39;) die overeenkomt met de sandboxnaam waar de API-operaties zullen plaatsvinden. Zie het [sandboxoverzicht](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl){target="_blank"} voor meer informatie.

## Eindpuntconfiguratie

Hier is de basisstructuur van een eindpuntconfiguratie:

```json
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>De **maxHttpConnections** parameter is facultatief. Zo kunt u het aantal verbindingen beperken dat Journey Optimizer opent voor het externe systeem.
>
>De maximale waarde die kan worden ingesteld, is 400. Als niets wordt gespecificeerd, dan kan het systeem tot veelvoudige duizenden verbindingen afhankelijk van het dynamische schrapen van het systeem openen.
>
>Wanneer de configuratie voor plafonnering wordt geïmplementeerd, als er geen `maxHttpConnections` -waarde is ingesteld, wordt een standaardwaarde `maxHttpConnections = -1` toegevoegd aan de configuratie die wordt geïmplementeerd en gebruikt Journey Optimizer de standaardwaarde van het systeem.

Voorbeeld:

```json
{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>De configuratie zal slechts actief na het roepen van **&#x200B;**&#x200B;eindpunt opstellen.

## Waarschuwing en fouten

Wanneer a **canDeploy** methode wordt geroepen, bevestigt het proces de configuratie en keert de bevestigingsstatus terug die door zijn Unieke identiteitskaart wordt geïdentificeerd, of:

```json
"ok" or "error"
```

De mogelijke fouten zijn:

* **ERR_ENDPOINTCONFIG_100**: het in kaart brengen van config: ontbrekende of ongeldige URL
* **ERR_ENDPOINTCONFIG_101**: het in kaart brengen van config: misvormde url
* **ERR_ENDPOINTCONFIG_102**: het in kaart brengen van config: misvormde url: vervangingsklank in url niet toegestaan in gastheer :port
* **ERR_ENDPOINTCONFIG_103**: het in kaart brengen van config: ontbrekende methodes van HTTP
* **ERR_ENDPOINTCONFIG_104**: het in kaart brengen van config: geen bepaalde vraagclassificatie
* **ERR_ENDPOINTCONFIG_107**: het in kaart brengen van config: ongeldige maximum vraagtelling (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: het maximum config: ongeldige maximum vraagtelling (periodInMS)
* **ERR_ENDPOINTCONFIG_111**: het in kaart brengen van config: kan geen eindpunt config tot stand brengen: ongeldige lading
* **ERR_ENDPOINTCONFIG_112**: het begrenzen config: kan geen eindpunt config tot stand brengen: het verwachten van een nuttige lading JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: ongeldige de dienstnaam `<!--<given value>-->`: moet &quot;dataSource&quot;of &quot;actie&quot;zijn

De mogelijke waarschuwing is:

**ERR_ENDPOINTCONFIG_106**: het in kaart brengen van config: maximum de verbindingen van HTTP niet bepaald: geen beperking door gebrek

## Gebruiksscenario’s

Deze sectie bevat een overzicht van de belangrijkste gebruiksgevallen voor het beheer van configuraties met begrenzingen in [!DNL Journey Optimizer] en de bijbehorende API-opdrachten die nodig zijn om het gebruiksscenario te implementeren.

De details op elk API bevel zijn beschikbaar in de [&#x200B; API beschrijving &amp; inzameling van Postman &#x200B;](#description).

+++Een nieuwe configuratie voor uitlijnen maken en implementeren

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`create`** - Maakt een nieuwe configuratie.
1. **`candeploy`** - Controleert of de configuratie kan worden opgesteld.
1. **`deploy`** - Implementeert de configuratie.

+++

+++Update en stel een het maximum configuratie (nog niet opgesteld) op

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`get`** - Hiermee worden details van een specifieke configuratie opgehaald.
1. **`update`** - Hiermee wijzigt u de configuratie.
1. **`candeploy`** - Controleert de geschiktheid voor implementatie.
1. **`deploy`** - Implementeert de configuratie.

+++

+++Implementeer en verwijder een geïmplementeerde configuratie voor plafonnering

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`undeploy`** - implementeert de configuratie ongedaan.
1. **`delete`** - Verwijdert de configuratie.

+++

+++Een geïmplementeerde uitlijningsconfiguratie in één stap verwijderen

In slechts één API-aanroep kunt u de configuratie met behulp van de parameter `forceDelete` verwijderen en de implementatie ervan ongedaan maken.

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`delete`(met `forceDelete` parameter)** - Dwingt schrapping van een opgestelde configuratie in één enkele stap.

+++

+++Een reeds geïmplementeerde configuratie voor plafonnering bijwerken

>[!NOTE]
>
>Een herplaatsing wordt vereist na het bijwerken van een reeds opgestelde configuratie.

API-aanroepen voor gebruik:
1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`get`** - Hiermee worden details van een specifieke configuratie opgehaald.
1. **`update`** - Hiermee wijzigt u de configuratie.
1. **`undeploy`** - Hiermee verwijdert u de configuratie voordat u wijzigingen aanbrengt.
1. **`candeploy`** - Controleert de geschiktheid voor implementatie.
1. **`deploy`** - Implementeert de bijgewerkte configuratie.

+++
