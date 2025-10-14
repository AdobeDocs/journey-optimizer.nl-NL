---
solution: Journey Optimizer
product: journey optimizer
title: API voor beperken
description: Leer hoe u met de Throttling-API werkt
feature: Journeys, API
role: Developer
level: Beginner
keywords: extern, API, optimaliseren, aftopping
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 13af123030449d870f44f3470710b0da2c6f4775
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 48%

---

# Werken met de beperkings-API

Met de Throttling-API kunt u uw throttling-configuraties maken, configureren en controleren om het aantal gebeurtenissen dat per seconde wordt verzonden te beperken.

Deze sectie bevat algemene informatie over het werken met de API. Een gedetailleerde API beschrijving is beschikbaar in [&#x200B; documentatie van Adobe Journey Optimizer APIs &#x200B;](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

## Lees hier meer

* **Één configuratie per organisatie:** slechts wordt één configuratie momenteel toegestaan per organisatie. Er moet een configuratie worden gedefinieerd in een productiesandbox (opgegeven via `x-sandbox-name` in de koppen).
* **organisatie-vlakke toepassing:** de configuratie van A wordt toegepast op organisatieniveau.
* **API grens behandeling:** wanneer de grens die in API wordt geplaatst wordt bereikt, worden de verdere gebeurtenissen een rij gevormd tot 6 uren. Deze waarde kan niet worden gewijzigd.
* **`maxHttpConnections`parameter:** De `maxHttpConnections` parameter is een optionele parameter die beschikbaar is in de API voor uitsnijden, zodat u alleen het aantal verbindingen kunt beperken dat Journey Optimizer opent voor het externe systeem. [&#x200B; Leer hoe te met het Kappen API &#x200B;](../configuration/capping.md) te werken

  Als u het aantal verbindingen wilt beperken maar die externe vraag ook wilt vertragen, kunt u twee configuraties, één throttling en één het in kaart brengen, op het zelfde eindpunt vormen. Beide configuraties kunnen voor één eindpunt coëxisteren. Als u &#39;maxHttpConnections&#39; wilt instellen voor een vertraagd eindpunt, gebruikt u de Throttling-API om de vertragingsdrempel en de Capping-API in te stellen om &#39;maxHttpConnections&#39; in te stellen. Wanneer u de API voor uitsnijden aanroept, kunt u de drempelwaarde voor uitlijnen instellen op iets hoger dan de drempelwaarde voor vertragen, zodat de uitlijningsregel in feite nooit wordt toegepast.

## Throttling API description &amp; Postman collection {#description}

In de onderstaande tabel staan de beschikbare opdrachten voor de vertragings-API. De gedetailleerde informatie met inbegrip van verzoeksteekproeven, parameters, en antwoordformaten is beschikbaar in de [&#x200B; documentatie van Adobe Journey Optimizer APIs &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Methode | Pad | Beschrijving |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | Ontvang een lijst van de beperkingsconfiguraties |
| [!DNL POST] | /throttlingConfigs | Een beperkingsconfiguratie maken |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | Beperkingsconfiguratie implementeren |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | Implementatie van een beperkingsconfiguratie ongedaan maken |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | Controleren of een beperkingsconfiguratie kan worden geïmplementeerd of niet |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | Een beperkingsconfiguratie bijwerken |
| [!DNL GET] | /throttlingConfigs/`{uid}` | Een beperkingsconfiguratie ophalen |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | Een beperkingsconfiguratie verwijderen |

Bovendien is een inzameling van Postman beschikbaar [&#x200B; hier &#x200B;](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json){target="_blank"} om u in uw het testen configuratie te helpen.

Deze inzameling is opstelling geweest om de Variabele die inzameling van Postman te delen via **[de Integraties van de Console van Adobe I/O wordt geproduceerd &#x200B;](https://console.adobe.io/integrations) > probeert het uit > Download voor Postman**, die een dossier van het Milieu van Postman met de geselecteerde integratiewaarden produceert.

Eenmaal gedownload en geüpload naar Postman moet u drie variabelen toevoegen: `{JO_HOST}`,`{BASE_PATH}` en `{SANDBOX_NAME}`.

* `{JO_HOST}` : [!DNL Journey Optimizer] URL van gateway.
* `{BASE_PATH}` : ingangspunt voor de API.
* `{SANDBOX_NAME}`: de header **x-sandbox-name** (bijvoorbeeld &#39;prod&#39;) die overeenkomt met de sandboxnaam waar de API-operaties zullen plaatsvinden. Zie het [sandboxoverzicht](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl){target="_blank"} voor meer informatie.

## Beperkingsconfiguratie {#configuration}

Dit is de structuur van een beperkingsconfiguratie. De attributen **name** en **description** zijn optioneel.

```json
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

Voorbeeld:

```json
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>De configuratie zal slechts actief na het roepen van **&#x200B;**&#x200B;eindpunt opstellen.

## Fouten

Bij het maken of bijwerken van een configuratie valideert het proces de gegeven configuratie en retourneert de validatiestatus die wordt geïdentificeerd door de unieke ID, ofwel:

```json
"ok" or "error"
```

>[!IMPORTANT]
>
>De attributen **maxThroughput**, **urlPattern** en **methods** zijn verplicht.
>
>**maxThroughput**-waarde moet tussen 200 en 5000 liggen.

Bij het maken, verwijderen of implementeren van een beperkingsconfiguratie kunnen de volgende fouten optreden:

* **ERR_THROTTLING_CONFIG_100**: beperkingsconfig: `<mandatory attribute>` vereist
* **ERR_THROTTLING_CONFIG_101**: beperkingsconfig: maxThroughput is vereist en moet groter zijn dan of gelijk aan 200 en kleiner dan of gelijk aan 5.000
* **ERR_THROTTLING_CONFIG_104**: beperkingsconfig: niet-welgevormd URL-patroon
* **ERR_THROTTLING_CONFIG_105**: beperkingsconfig: jokers zijn niet toegestaan in het hostgedeelte van het URL-patroon
* **ERR_THROTTLING_CONFIG_106**: beperkingsconfig: ongeldige payload
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**, &quot;Kan een geïmplementeerde beperkingsconfiguratie niet verwijderen. Implementatie ongedaan maken voordat deze wordt verwijderd&quot;
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**, &quot;Kan beperkingsconfiguratie niet verwijderen: onverwachte fout&quot;
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**, &quot;Kan beperkingsconfiguratie niet implementeren: onverwachte fout &quot;
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**, &quot;Kan beperkingsconfig niet ongedaan maken: onverwachte fout&quot;
* **THROTTLING_CONFIG_GET_ERROR: 1460**, &quot;Kan geen beperkingsconfiguratie krijgen: onverwachte fout&quot;
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**, &quot;Kan beperkingsconfiguratie niet bijwerken: runtime versie is niet actief&quot;
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**, &quot;Kan beperkingsconfiguratie niet bijwerken: onverwachte fout&quot;
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**, &quot;Operatie niet toegestaan op beperkingsconfig: non prod sandbox&quot;
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**, &quot;Kan geen beperkingsconfiguratie maken: onverwachte fout&quot;
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**, &quot;Kan geen beperkingsconfiguratie maken: slechts één configuratie toegestaan per org&quot;
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 1466**, &quot;Kan beperkingsconfiguratie niet implementeren: reeds geïmplementeerd&quot;
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 1467**, &quot;beperkingsconfig niet gevonden&quot;
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 1468**, &quot;Kan beperkingsconfiguratie niet verwijderen: nog niet geïmplementeerd&quot;

**Voorbeelden van fouten**

Als u probeert een configuratie te maken op een non-prod sandbox:

```json
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

Als deze sandbox niet bestaat:

```json
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

Wanneer u probeert een andere configuratie te maken:

```json
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## Configuratie levenscyclus op runtimeniveau {#config}

Wanneer een configuratie ge-deïmplementeerd is, wordt deze gemarkeerd als inactief op runtimeniveau en worden lopende gebeurtenissen gedurende 24 uur verwerkt. Deze wordt dan verwijderd in de runtimeservice.

Nadat een configuratie is ge-deïmplementeerd, kunt u de configuratie bijwerken en opnieuw implementeren. Daardoor wordt een nieuwe runtimeconfiguratie gemaakt die in aanmerking wordt genomen bij de toekomstige uitvoering van acties.

Bij het bijwerken van een geïmplementeerde configuratie wordt onmiddellijk rekening gehouden met de nieuwe waarden. De onderliggende systeembronnen worden automatisch aangepast. Dit is optimaal in vergelijking met het deïmplementeren en dan opnieuw implementeren van de configuratie.

## Voorbeelden van reacties {#responses}

**Maken - POST**

```json
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**Update - PUT**

```json
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**Lezen (na update) - GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**Lezen (na implementatie) - GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## Gebruiksscenario’s {#uc}

Deze sectie bevat een overzicht van de belangrijkste gebruiksgevallen voor het beheer van configuraties met vertraagde installatie in [!DNL Journey Optimizer] en de bijbehorende API-opdrachten die nodig zijn om de gebruiksaanwijzing te implementeren.

De details op elk API bevel zijn beschikbaar in de [&#x200B; API beschrijving &amp; inzameling van Postman &#x200B;](#description).

+++Het creëren en de plaatsing van een nieuwe throttling configuratie

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`create`** - Maakt een nieuwe configuratie.
1. **`candeploy`** - Controleert of de configuratie kan worden opgesteld.
1. **`deploy`** - Implementeert de configuratie.

+++

+++Werk en stel een throttling configuratie (nog niet opgesteld) bij

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`get`** - Hiermee worden details van een specifieke configuratie opgehaald.
1. **`update`** - Hiermee wijzigt u de configuratie.
1. **`candeploy`** - Controleert de geschiktheid voor implementatie.
1. **`deploy`** - Implementeert de configuratie.

+++

+++Implementeer en verwijder een geïmplementeerde throttingconfiguratie

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`undeploy`** - implementeert de configuratie ongedaan.
1. **`delete`** - Verwijdert de configuratie.

+++

+++Een geïmplementeerde vertragingsconfiguratie verwijderen

In slechts één API-aanroep kunt u de configuratie met behulp van de parameter `forceDelete` verwijderen en de implementatie ervan ongedaan maken.

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`delete`(met `forceDelete` parameter)** - Dwingt schrapping van een opgestelde configuratie in één enkele stap.

+++

+++Een reeds geïmplementeerde configuratie voor vertragen bijwerken

>[!NOTE]
>
>Het is niet nodig om de configuratie te deïmplementeren alvorens bij te werken

API-aanroepen voor gebruik:

1. **`list`** - Hiermee worden bestaande configuraties opgehaald.
1. **`get`** - Hiermee worden details van een specifieke configuratie opgehaald.
1. **`update`** - Hiermee wijzigt u de configuratie.

+++
