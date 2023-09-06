---
title: Kwaliteitsaanduidingen voor verzamelingen weergeven
description: Met de verzamelingskwalificatietags kunt u uw voorstellen beter organiseren en sorteren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 1%

---

# Kwaliteitsaanduidingen voor verzamelingen weergeven {#list-tags}

Met de verzamelingsaanduidingen (die voorheen &#39;&#39;tags&#39;&#39; werden genoemd) kunt u uw aanbiedingen beter organiseren en doorlopen. U kunt bijvoorbeeld een label geven aan de zwarte vrijdag-aanbiedingen met de verzamelingsaanduiding &#39;Zwarte vrijdag&#39;. U kunt dan de onderzoeksfunctionaliteit in de Bibliotheek van de Aanbieding gebruiken om van alle aanbiedingen met die inzamelingskwalificatie gemakkelijk de plaats te bepalen.

De bepalende eigenschappen van de inzameling kunnen ook worden gebruikt om aanbiedingen samen in inzamelingen te groeperen. Raadpleeg de zelfstudie voor meer informatie [maken, verzamelingen](../../../offer-library/creating-collections.md).

U kunt een lijst van alle inzamelingsbepalende eigenschappen bekijken door één enkel verzoek van de GET aan uit te voeren [!DNL Offer Library] API.

**API-indeling**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Het eindpuntpad voor persistentie-API&#39;s. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionele queryparameters om resultaten te filteren op. | `limit=2` |

**Verzoek**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Query-parameters gebruiken {#using-query-parameters}

U kunt queryparameters gebruiken om de resultaten te filteren en te pagineren wanneer u bronnen weergeeft.

### Paginering {#paging}

De gemeenschappelijkste vraagparameters voor het pagineren omvatten:

| Parameter | Beschrijving | Voorbeeld |
| --------- | ----------- | ------- |
| `property` | Een optioneel eigenschapsfilter: <br> <ul> - De eigenschappen worden gegroepeerd op AND-bewerking. <br><br> - Parameters kunnen als volgt worden herhaald: property=<property-expr>[&amp;eigenschap=<property-expr2>...] or property=<property-expr1>[,<property-expr2>...] <br><br> - Eigenschapexpressies hebben een indeling [!]field[op]waarde, met op in [==,!=,&lt;=,>=,&lt;,>,~], die reguliere expressies ondersteunen | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Resultaten sorteren op een bepaalde eigenschap. Als u de naam a - before toevoegt (orderby=-name), worden de items op naam gesorteerd in aflopende volgorde (Z-A). Padexpressies hebben de vorm van door punten gescheiden paden. Deze parameter kan als volgt worden herhaald: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Beperk het aantal geretourneerde entiteiten. | `limit=5` |

**Antwoord**

Een succesvolle reactie keert een lijst van inzamelingsbepalende eigenschappen terug die aanwezig zijn.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
