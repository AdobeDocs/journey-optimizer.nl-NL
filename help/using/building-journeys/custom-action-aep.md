---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste acties gebruiken om gebeurtenissen voor reizen in AEP te schrijven
description: Aangepaste acties gebruiken om gebeurtenissen voor reizen in AEP te schrijven
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
source-git-commit: 778ef71a531346774c5e10e296dbf1112fed891d
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Gebruik hoofdletters/kleine letters: gebruik Aangepaste handelingen om gebeurtenissen Journey in Experience Platform te schrijven{#custom-action-aep}

Dit gebruiksgeval verklaart hoe te om douanegebeurtenissen in Adobe Experience Platform van Reizen te schrijven gebruikend de Acties van de Douane en Voor authentiek verklaarde vraag.

## Een IO-project configureren

1. Klik in de Adobe Developer-console op **Project** en opent u uw IO-project.

1. In de **Credentials** sectie, klikken **OAuth Server-to-Server**.

   ![](assets/custom-action-aep-1.png)

1. Klikken **CURL weergeven, opdracht**.

   ![](assets/custom-action-aep-2.png)

1. Kopieer het cURL bevel en sla client_id, client_geheime, Grant_type en werkingsgebied op.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Nadat u uw project in de Adobe Developer-console hebt gemaakt, moet u ontwikkelaars en API-toegangsbeheer de juiste machtigingen geven. Meer informatie in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

## De bron configureren met HTTP API Inlet

1. Maak een eindpunt in Adobe Experience Platform om de gegevens van reizen te schrijven.

1. Klik in Adobe Experience Platform op **Bronnen**, onder **Verbindingen** in het linkermenu. Onder **HTTP-API**, klikt u op **Gegevens toevoegen**.

   ![](assets/custom-action-aep-3.png)

1. Selecteren **Nieuwe account** en inschakelen van verificatie. Klikken op **Verbinden met bron**.

   ![](assets/custom-action-aep-4.png)

1. Klikken op **Volgende** en selecteer de Dataset waar u de gegevens wilt schrijven. Klikken **Volgende** en **Voltooien**.

   ![](assets/custom-action-aep-5.png)

1. Open de nieuwe gegevensstroom. Kopieer de payload van het schema en sla deze op in uw notitiepad.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Aangepaste actie configureren

1. Open Adobe Journey Optimizer en klik op **Configuraties**, onder **Administratie** in het linkermenu. Onder **Handelingen**, klikt u op **Beheren** en klik op **Handeling maken**.

1. Stel de URL in en selecteer de methode Post.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Controleer of de headers (Content-Type, Charset, sandbox-name) zijn geconfigureerd.

   ![](assets/custom-action-aep-7bis.png)

### De verificatie instellen

1. Selecteer de **Type** als **Aangepast** met de volgende Payload.

1. Plak client_gehec, client_id, scope en Grant_type (van de IO projectlading die vroeger wordt gebruikt).

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Gebruik de **Klik om de verificatie te testen** om de verbinding te testen.

   ![](assets/custom-action-aep-8.png)

### De Payload instellen

1. In de **Verzoek** en **Antwoord** velden, plakt u de lading van de eerder gebruikte bronverbinding.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. De configuratie van het veld wijzigen vanuit **Constante** tot **Variabele** voor velden die dynamisch worden ingevuld. Sla de aangepaste handeling op.

## Reis

1. Tot slot gebruik deze douaneactie in een reis om de gebeurtenissen van de douanereis te schrijven.

1. Vul de Versie-id van de reis, Node-id, Node-naam en andere kenmerken volgens uw gebruikscase.

   ![](assets/custom-action-aep-9.png)
