---
solution: Journey Optimizer
product: journey optimizer
title: Privacyverzoeken
description: Meer weten over privacyverzoeken en de Privacy Service?
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 1%

---

# Privacyverzoeken {#track-changes}

Adobe Experience Platform **Privacy Service** biedt een RESTful-API en -gebruikersinterface waarmee u verzoeken om klantgegevens kunt beheren. Met Privacy Service kunt u verzoeken indienen om toegang te krijgen tot persoonlijke klantgegevens en deze te verwijderen uit Adobe Experience Cloud-toepassingen, waardoor u gemakkelijker kunt voldoen aan wettelijke en organisatorische privacyregels.

De verzoeken van de privacy kunnen van worden gecreeerd en worden beheerd **[!UICONTROL Requests]** -menu.

![](assets/requests.png)

Raadpleeg de documentatie bij Adobe Experience Platform voor meer informatie over de Privacy Service en het maken en beheren van privacyverzoeken:

* [Overzicht van Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl)
* [Privacy-taken beheren in de gebruikersinterface van de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)



## Aanvragen voor privacy van individuele gegevens beheren die u naar Adobe Journey Optimizer kunt verzenden {#data-privacy-requests}

U kunt individuele verzoeken om toegang tot en verwijdering van consumentengegevens vanuit Adobe Journey Optimizer op twee manieren verzenden:

* Via de **UI PRIVACY SERVICE**. Zie de documentatie [hier](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide#_blank).
* Via de **Privacy Service-API**. Zie de documentatie [hier](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) en API-informatie [hier](https://developer.adobe.com/experience-platform-apis/#_blank).

De Privacy Service ondersteunt twee soorten verzoeken: **gegevenstoegang** en **gegevensverwijdering**.

>[!NOTE]
>
>In deze handleiding wordt alleen uitgelegd hoe u privacyverzoeken voor Adobe Journey Optimizer kunt indienen. Als u ook privacyverzoeken voor het gegevensmeer van het Platform wilt indienen, verwijs naar dit [hulplijn](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/privacy) in aanvulling op deze zelfstudie. Voor het profiel van de klant in real time, gelieve te verwijzen naar dit [hulplijn](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy) en voor Identiteitsdienst, gelieve te verwijzen naar dit [hulplijn](https://experienceleague.adobe.com/en/docs/experience-platform/identity/privacy). Voor schrapping en toegangsverzoeken moet u deze individuele systemen roepen om ervoor te zorgen de verzoeken door elk van hen worden behandeld. Als u een privacyaanvraag bij Adobe Journey Optimizer indient, worden de gegevens niet van al deze systemen verwijderd.

Voor **toegangsverzoeken**, geeft u &quot;Adobe Journey Optimizer&quot; op in de gebruikersinterface (of &quot;CJM&quot; als productcode in de API).

Voor **aanvragen verwijderen** Naast de aanvraag &quot;Adobe Journey Optimizer&quot; moet u ook verwijderingsverzoeken indienen voor drie upstream services om te voorkomen dat Journey Optimizer de verwijderde gegevens opnieuw uitpakt. Als deze upstream diensten niet worden gespecificeerd, zal het &quot;Adobe Journey Optimizer&quot;verzoek in de &quot;verwerking&quot;staat blijven tot schrappingsverzoeken voor de upstream diensten worden gecreeerd.

De drie upstream services zijn:

* Profiel (productcode: &quot;profileService&quot;)
* AEP Data Lake (productcode: &quot;AdobeCloudPlatform&quot;)
* Identiteit (productcode: &quot;identiteit&quot;)

## Hoe te om Toegang te creëren en Verzoeken te schrappen

### Vereisten

Als u een aanvraag wilt indienen om gegevens voor Adobe Journey Optimizer te openen of te verwijderen, moet u beschikken over:

* een IMS-organisatie-id
* Een id van de identiteit van de persoon waarop u wilt optreden en de bijbehorende naamruimte(n). Raadpleeg voor meer informatie over naamruimten in Adobe Journey Optimizer en Experience Platform de klasse [Overzicht van naamruimte in identiteit](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).

### Vereiste veldwaarden in Adobe Journey Optimizer voor API-aanvragen

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### Voorbeeld van GDPR-toegangsaanvraag:

Vanuit de gebruikersinterface:

![](assets/accessrequest.png)

Via de API:

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### Voorbeeld van GDPR-aanvraag verwijderen:

Vanuit de gebruikersinterface:

![](assets/deleterequest.png)

Via de API:

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
