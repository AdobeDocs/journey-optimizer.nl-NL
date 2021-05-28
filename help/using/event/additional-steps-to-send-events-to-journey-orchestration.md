---
title: Aanvullende stappen om gebeurtenissen naar een reis te verzenden
description: Meer informatie over het verzenden van evenementen naar een reis
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Aanvullende stappen om gebeurtenissen te verzenden {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

Als u gebeurtenissen wilt configureren die naar **[!UICONTROL Streaming Ingestion APIs]** moeten worden verzonden en die in [!DNL Journey Optimizer] moeten worden gebruikt, moet u de volgende stappen uitvoeren:

1. Haal de inlaatURL op van Adobe Experience Platform API&#39;s. Meer informatie vindt u in [Overzicht van de API&#39;s voor streaming insluiting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html).
1. Kopieer de lading van de nuttige ladingsvoorproef in **[!UICONTROL Event]** menu. Meer informatie vindt u op [deze pagina](../event/about-creating.md#define-the-payload-fields).

Vervolgens moet u het gegevenssysteem configureren dat gebeurtenissen naar Streaming Ingestie-API&#39;s stuurt met de door u gekopieerde payload:

1. Stel een POST-API-aanroep in naar de URL van de Streaming Ingestie-API&#39;s (een zogenaamde inlaat).
1. Gebruik de nuttige lading u van [!DNL Journey Optimizer] in het lichaam (&quot;gegevenssectie&quot;) van de API vraag aan Streaming Ingestie APIs kopieerde. Zie hieronder voor een voorbeeld
1. Bepaal waar u alle variabelen in de lading wilt ophalen. Voorbeeld: als de gebeurtenis geacht wordt het adres over te brengen, zal de geplakte lading &quot;adres&quot;tonen: &quot;string&quot;. &quot;string&quot; moet worden vervangen door de variabele die automatisch de juiste waarde invult, de e-mail van de persoon waarnaar een bericht wordt verzonden. Let op: in de voorvertoning van de lading, in de sectie **[!UICONTROL Header]**, vullen wij vele waarden automatisch die worden verwacht om uw werk te vergemakkelijken.
1. Selecteer &#39;application/json&#39; als type body.
1. Geef uw IMS-organisatie-id in de koptekst door met behulp van de sleutel &quot;x-gw-ims-org-id&quot;. Gebruik voor de waarde uw IMS-organisatie-id (&quot;XXX@AdobeOrg&quot;).

Hier volgt een voorbeeld van een gebeurtenis Streaming ingestie-API&#39;s:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Als u de locatie waar het &quot;data&quot;-deel moet worden geplakt gemakkelijker wilt kunnen identificeren, kunt u een JSON-visualisatieprogramma gebruiken, zoals [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)

Raadpleeg deze [pagina](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html) voor informatie over het oplossen van problemen met de Streaming-API&#39;s.
