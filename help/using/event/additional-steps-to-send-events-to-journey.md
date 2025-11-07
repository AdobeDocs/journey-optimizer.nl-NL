---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende stappen om gebeurtenissen naar een reis te verzenden
description: Meer informatie over het verzenden van evenementen naar een reis
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: stappen, configuratie, reis, gebeurtenissen, stroom, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 2%

---

# Aanvullende stappen om gebeurtenissen te verzenden {#additional-steps-to-send-events}

Voer de volgende stappen uit om gebeurtenissen te configureren die naar **[!UICONTROL Streaming Ingestion APIs]** moeten worden verzonden en die in [!DNL Journey Optimizer] moeten worden gebruikt:

1. Haal de inlaat-URL op van Adobe Experience Platform API&#39;s. Leer meer in [&#x200B; Streaming Ingestie APIs overzicht &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=nl){target="_blank"}.
1. Kopieer de lading van de ladingsvoorproef in het **[!UICONTROL Event]** menu. Leer meer op [&#x200B; deze pagina &#x200B;](../event/about-creating.md#define-the-payload-fields).

Vervolgens moet u het gegevenssysteem configureren dat gebeurtenissen naar Streaming Ingestie-API&#39;s stuurt met de door u gekopieerde payload:

1. Stel een POST API-aanroep in naar de URL van de Streaming Ingestie-API&#39;s (een zogenaamde inlaat).
1. Gebruik de payload die u hebt gekopieerd vanuit [!DNL Journey Optimizer] in de hoofdtekst (&quot;gegevenssectie&quot;) van de API-aanroep naar de API&#39;s voor streaming congestie. Zie hieronder voor een voorbeeld
1. Bepaal waar u alle variabelen in de lading wilt ophalen. Voorbeeld: als de gebeurtenis het adres moet overbrengen, wordt bij de geplakte payload &quot;address&quot;: &quot;string&quot; weergegeven. &quot;string&quot; moet worden vervangen door de variabele die automatisch de juiste waarde invult, de e-mail van de persoon waarnaar een bericht wordt verzonden. In de voorvertoning van de payload vullen we in de sectie **[!UICONTROL Header]** veel waarden die u nodig hebt om uw werk te vergemakkelijken.
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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

Om de identificatie van de plaats te vergemakkelijken waar te om het &quot;gegevens&quot;deel te kleven, kunt u een JSON visualisatiehulpmiddel zoals [&#x200B; JSON formatter &#x200B;](https://jsonformatter.curiousconcept.com){target="_blank"} gebruiken.

Om het stromen Ingestie APIs problemen op te lossen, verwijs naar [&#x200B; documentatie van Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=nl-NL){target="_blank"}.
