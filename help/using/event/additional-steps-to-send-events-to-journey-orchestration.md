---
title: Aanvullende stappen om gebeurtenissen naar een reis te verzenden
description: Meer informatie over het verzenden van evenementen naar een reis
feature: Gebeurtenissen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 2%

---

# Aanvullende stappen om gebeurtenissen te verzenden {#concept_xrz_n1q_y2b}

Als u gebeurtenissen wilt configureren die naar **[!UICONTROL Streaming Ingestion APIs]** moeten worden verzonden en die in [!DNL Journey Optimizer] moeten worden gebruikt, moet u de volgende stappen uitvoeren:

1. Haal de inlaatURL op van Adobe Experience Platform API&#39;s. Meer informatie vindt u in [Overzicht van de streaming API&#39;s voor insluiting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}.
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

Om de identificatie van de plaats te vergemakkelijken waar om het &quot;gegevens&quot;deel te kleven, kunt u een hulpmiddel van de visualisatie JSON zoals [JSON formatter](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;} gebruiken.

Om het stromen Ingestie APIs problemen op te lossen, verwijs naar [Experience Platform documentatie](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
