---
solution: Journey Optimizer
product: journey optimizer
title: Privacyverzoeken
description: Meer weten over privacyverzoeken en de Privacy Service?
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 844c0f8dc9b14d69cbd87893042f048443d7a5e6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 1%

---

# Privacyverzoeken {#track-changes}

Adobe Experience Platform **Privacy Service** verstrekt een RESTful API en gebruikersinterface om u te helpen verzoeken van klantengegevens beheren. Met Privacy Service kunt u verzoeken indienen om toegang te krijgen tot persoonlijke klantgegevens en deze te verwijderen uit Adobe Experience Cloud-toepassingen, waardoor u gemakkelijker kunt voldoen aan wettelijke en organisatorische privacyregels.

Privacy-aanvragen kunnen worden gemaakt en beheerd via het menu **[!UICONTROL Requests]** .

![](assets/requests.png)

Raadpleeg de documentatie bij Adobe Experience Platform voor meer informatie over de Privacy Service en het maken en beheren van privacyverzoeken:

* [ overzicht van de Privacy Service ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl)
* [ het Leiden privacybanen in Privacy Service UI ](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)



## Aanvragen voor privacy van individuele gegevens beheren die u naar Adobe Journey Optimizer kunt verzenden {#data-privacy-requests}

U kunt individuele verzoeken om toegang tot en verwijdering van consumentengegevens vanuit Adobe Journey Optimizer op twee manieren verzenden:

* Door de **Privacy Service UI**. Zie de documentatie [ hier ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide#_blank).
* Door **Privacy Service API**. Zie hier de documentatie [ ](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) en API informatie [ ](https://developer.adobe.com/experience-platform-apis/#_blank).

De Privacy Service steunt twee soorten verzoeken: **gegevenstoegang** en **gegevensschrapping**.

>[!NOTE]
>
>In deze handleiding wordt alleen uitgelegd hoe u privacyverzoeken voor Adobe Journey Optimizer kunt indienen. Als u ook van plan bent om privacyverzoeken voor het de gegevensmeer van het Platform te maken, verwijs naar deze [ gids ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/privacy) naast dit leerprogramma. Voor Echte - tijdklantenprofiel, gelieve te verwijzen naar deze [ gids ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy) en voor de dienst van de Identiteit, gelieve naar deze [ gids ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/privacy) te verwijzen. Voor schrapping en toegangsverzoeken moet u deze individuele systemen roepen om ervoor te zorgen de verzoeken door elk van hen worden behandeld. Als u een privacyaanvraag bij Adobe Journey Optimizer indient, worden de gegevens niet van al deze systemen verwijderd.

Voor **toegangsverzoeken**, specificeer &quot;Adobe Journey Optimizer&quot;van UI (of &quot;CJM&quot;als productcode in API).

Voor **schrapt verzoeken**, naast het &quot;Adobe Journey Optimizer&quot;verzoek, moet u schrappingsverzoeken aan drie stroomopwaartse diensten ook voorleggen om Journey Optimizer te verhinderen de geschrapte gegevens opnieuw uit te werpen. Als deze upstream diensten niet worden gespecificeerd, zal het &quot;Adobe Journey Optimizer&quot;verzoek in de &quot;verwerking&quot;staat blijven tot schrappingsverzoeken voor de upstream diensten worden gecreeerd.

De drie upstream services zijn:

* Profiel (productcode: &quot;profileService&quot;)
* AEP Data Lake (productcode: &quot;AdobeCloudPlatform&quot;)
* Identiteit (productcode: &quot;identiteit&quot;)

## Hoe te om Toegang te creëren en Verzoeken te schrappen

### Vereisten

Als u een aanvraag wilt indienen om gegevens voor Adobe Journey Optimizer te openen of te verwijderen, moet u beschikken over:

* een organisatie-id voor de Adobe
* een herkenningsteken van de Identiteit van de persoon u op en overeenkomstige namespace(s) wilt handelen.Voor meer informatie over identiteit namespaces in Adobe Journey Optimizer en Experience Platform, zie het [ overzicht van identiteitskaart namespace ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).

### Vereiste veldwaarden in Adobe Journey Optimizer voor API-aanvragen

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your Adobe Organization ID Value>

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
