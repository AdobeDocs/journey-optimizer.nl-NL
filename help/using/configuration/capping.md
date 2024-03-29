---
solution: Journey Optimizer
product: journey optimizer
title: Afkappings-API
description: Meer informatie over het werken met de API voor uitlijnen
feature: Journeys, API
role: User
level: Beginner
keywords: extern, API, optimaliseren, aftopping
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 26%

---

# Werken met de API voor uitsnijden {#work}

Met de API voor uitsnijden kunt u uw configuraties voor uitlijnen maken, configureren en controleren.

Deze sectie bevat algemene informatie over het werken met de API. Een gedetailleerde API-beschrijving is beschikbaar in [Adobe Journey Optimizer API-documentatie](https://developer.adobe.com/journey-optimizer-apis/).

## Beschrijving van API voor uitlijnen

| Methode | Pad | Beschrijving |
|---|---|---|
| [!DNL POST] | list/endConfigs | Krijg een lijst van de eindpunt die configuraties begrenzen |
| [!DNL POST] | /endConfigs | Creeer een eindpunt het bedekken configuratie |
| [!DNL POST] | /endConfigs/`{uid}`/implementatie | Implementeer een configuratie voor het afdekken van eindpunten |
| [!DNL POST] | /endConfigs/`{uid}`/uninstall | Maak een eindpunt onbruikbaar dat configuratie begrenst |
| [!DNL POST] | /endConfigs/`{uid}`/canDeploy | Controle als een eindpunt het begrenzen configuratie kan worden opgesteld of niet |
| [!DNL PUT] | /endConfigs/`{uid}` | Een configuratie voor het afdekken van eindpunten bijwerken |
| [!DNL GET] | /endConfigs/`{uid}` | Retrireer een eindpunt dat configuratie begrenst |
| [!DNL DELETE] | /endConfigs/`{uid}` | Een configuratie voor een uitlijningselement verwijderen |

Wanneer een configuratie wordt gecreeerd of bijgewerkt, automatisch wordt een controle uitgevoerd om de syntaxis en de integriteit van de lading te waarborgen.
Als sommige problemen voorkomen, keert de verrichting waarschuwing of fouten terug om u te helpen de configuratie verbeteren.

## Eindpuntconfiguratie

Hier is de basisstructuur van een eindpuntconfiguratie:

```
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
>De **maxHttpConnections** parameter is optioneel. Zo kunt u het aantal verbindingen beperken dat Journey Optimizer opent voor het externe systeem.
>
>De maximale waarde die kan worden ingesteld, is 400. Als niets wordt gespecificeerd, dan kan het systeem tot veelvoudige duizenden verbindingen afhankelijk van het dynamische schrapen van het systeem openen.
>
>Wanneer de het plafonneren configuratie wordt opgesteld, als geen &quot;maxHttpConnection&quot;waarde is verstrekt, wordt het gebrek &quot;maxHttpConnection = -1&quot;toegevoegd in de opgestelde configuratie, betekenend dat Journey Optimizer de standaardwaarde van het systeem zal gebruiken.

### Voorbeeld:

```
`{
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

## Waarschuwing en fouten

Wanneer een **canDeploy** De methode wordt geroepen, bevestigt het proces de configuratie en keert de bevestigingsstatus terug die door zijn Unieke identiteitskaart wordt geïdentificeerd, of:

```
"ok" or "error"
```

De mogelijke fouten zijn:

* **ERR_ENDPOINTCONFIG_100**: configuratie beperken: ontbrekende of ongeldige URL
* **ERR_ENDPOINTCONFIG_101**: config.capping: onjuist gevormde URL
* **ERR_ENDPOINTCONFIG_102**: config.capping: onjuist gevormde url: wildchar in url niet toegestaan in host:port
* **ERR_ENDPOINTCONFIG_103**: config.capping: ontbrekende HTTP-methoden
* **ERR_ENDPOINTCONFIG_104**: het maximum config: geen bepaalde vraagclassificatie
* **ERR_ENDPOINTCONFIG_107**: het in kaart brengen config: ongeldige maximumvraagtelling (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: het in kaart brengen config: ongeldige maximum vraagtelling (periodInMS)
* **ERR_ENDPOINTCONFIG_111**: het begrenzen config: kan geen eindpunt config tot stand brengen: ongeldige lading
* **ERR_ENDPOINTCONFIG_112**: het begrenzen config: kan geen eindpunt config tot stand brengen: het verwachten van een JSON nuttige lading
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: ongeldige servicenaam `<!--<given value>-->`: moet &#39;dataSource&#39; of &#39;action&#39; zijn

De mogelijke waarschuwing is:

**ERR_ENDPOINTCONFIG_106**: config.max. HTTP-verbindingen niet gedefinieerd: standaard geen beperking

## Gebruiksscenario&#39;s

In deze sectie zult u de vijf belangrijkste gebruik-gevallen vinden die u kunt uitvoeren om uw het capteren configuratie binnen te beheren [!DNL Journey Optimizer].

Voor hulp bij het testen en configureren is [hier](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) een Postman-verzameling beschikbaar.

Deze Postman-verzameling is opgezet om de Postman Variabele verzameling te delen die is gegenereerd via __[Adobe I/O Console-integraties](https://console.adobe.io/integrations) > Uitproberen > Downloaden voor Postman__, wat een Postman-omgevingsbestand genereert met de geselecteerde integratiewaarden.

Eenmaal gedownload en geüpload naar Postman moet u drie variabelen toevoegen: `{JO_HOST}`,`{BASE_PATH}` en `{SANDBOX_NAME}`.
* `{JO_HOST}`: [!DNL Journey Optimizer] Gateway-URL
* `{BASE_PATH}`: ingangspunt voor de API. 
* `{SANDBOX_NAME}`: de header **x-sandbox-name** (bijvoorbeeld &#39;prod&#39;) die overeenkomt met de sandboxnaam waar de API-operaties zullen plaatsvinden. Zie het [sandboxoverzicht](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl) voor meer informatie.

In het volgende gedeelte vindt u de geordende lijst van Rest-API-aanroepen om het gebruiksscenario uit te voeren.

Gebruiksscenario n°1: **Het creëren en de plaatsing van een nieuwe het maximum configuratie**

1. list
1. create
1. candeploy
1. deploy

Gebruiksscenario n°2: **Een configuratie voor uitlijnen bijwerken en implementeren die nog niet is geïmplementeerd**

1. list
1. get
1. update
1. candeploy
1. deploy

Gebruiksscenario n°3: **Implementeer en verwijder een geïmplementeerde configuratie voor plafonnering**

1. list
1. undeploy
1. delete

Gebruiksscenario n°4: **Verwijder een configuratie voor geïmplementeerde uiteinden.**

In slechts één API-oproep kunt u de configuratie deïmplementeren en verwijderen met behulp van de parameter forceDelete.
1. list
1. delete, met parameter forceDelete

Gebruiksscenario n°5: **Een reeds geïmplementeerde configuratie voor plafonnering bijwerken**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
