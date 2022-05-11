---
title: Aanvullende stappen om gebeurtenissen naar een reis te verzenden
description: Meer informatie over het verzenden van evenementen naar een reis
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 03a5741e4f79f6a551eed64364e3a9d36e6473dc
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 4%

---

# Aanvullende stappen om gebeurtenissen te verzenden {#additional-steps-to-send-events}

Om gebeurtenissen te vormen die moeten worden verzonden naar **[!UICONTROL Streaming Ingestion APIs]** en te gebruiken in [!DNL Journey Optimizer], moet u deze stappen volgen:

1. Haal de inlaatURL op van Adobe Experience Platform API&#39;s. Meer informatie in [Overzicht van API&#39;s voor streaming-insluiting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=nl){target=&quot;_blank&quot;}.
1. Kopieer de lading van de payload voorproef in **[!UICONTROL Event]** -menu. Meer informatie in [deze pagina](../event/about-creating.md#define-the-payload-fields).

Vervolgens moet u het gegevenssysteem configureren dat gebeurtenissen naar Streaming Ingestie-API&#39;s stuurt met de door u gekopieerde payload:

1. Stel een POST-API-aanroep in naar de URL van de Streaming Ingestie-API&#39;s (een zogenaamde inlaat).
1. De lading gebruiken die u hebt gekopieerd [!DNL Journey Optimizer] in de hoofdtekst (&quot;gegevenssectie&quot;) van de API-aanroep naar Streaming Ingestie-API&#39;s. Zie hieronder voor een voorbeeld
1. Bepaal waar u alle variabelen in de lading wilt ophalen. Voorbeeld: als de gebeurtenis geacht wordt het adres over te brengen, zal de geplakte lading &quot;adres&quot;tonen: &quot;string&quot;. &quot;string&quot; moet worden vervangen door de variabele die automatisch de juiste waarde invult, de e-mail van de persoon waarnaar een bericht wordt verzonden. Let op: in de voorvertoning van de lading, in de **[!UICONTROL Header]** in deze sectie worden veel waarden automatisch ingevuld die u nodig hebt om uw werk te vergemakkelijken.
1. Selecteer &#39;application/json&#39; als type body.
1. Geef uw organisatie-id in de koptekst door met behulp van de sleutel &quot;x-gw-ims-org-id&quot;. Gebruik voor de waarde uw organisatie-id (&quot;XXX@AdobeOrg&quot;).

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

U kunt een JSON-visualisatiefunctie gebruiken, zoals [JSON-formatter](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Raadpleeg voor het oplossen van problemen met de API&#39;s voor streaming-insluiting [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
