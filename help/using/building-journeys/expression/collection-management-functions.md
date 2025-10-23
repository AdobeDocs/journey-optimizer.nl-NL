---
solution: Journey Optimizer
product: journey optimizer
title: Functies voor het beheer van verzamelingen
description: Meer informatie over gegevenstypen in functies voor verzamelingsbeheer
feature: Journeys
role: Developer
level: Experienced
keywords: query, collecties, functies, lading, reis
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 1%

---

# Functies voor het beheer van verzamelingen {#collection-management-functions}


## Over queryverzamelingsfuncties

De uitdrukkingstaal introduceert ook een reeks functies aan vraaginzamelingen. Deze functies worden hieronder uitgelegd.

In het volgende voorbeeld gebruiken we de gebeurtenislading die een verzameling bevat:

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

## De all(`<condition>`) functie

De functie **[!UICONTROL all]** laat de definitie van een filter op een bepaalde inzameling toe door een booleaanse uitdrukking te gebruiken.

```json
<listExpression>.all(<condition>)
```

Zo kunt u onder alle gebruikers van de app de toepassingen ophalen met IOS 13 (Booleaanse expressie &quot;app used == IOS 13&quot;). Het resultaat van deze functie is de gefilterde lijst met items die overeenkomen met de booleaanse expressie (bijvoorbeeld: app-gebruiker 1, app-gebruiker 34, app-gebruiker 432).

Bij een Source Condition-activiteit van Data kunt u controleren of het resultaat van de functie **[!UICONTROL all]** null is of niet. U kunt deze **[!UICONTROL all]** functie ook combineren met andere functies, zoals **[!UICONTROL count]** . Voor meer informatie, zie [ de activiteit van de Voorwaarde van Source van Gegevens ](../condition-activity.md#data_source_condition).


>[!CAUTION]
>
>Het gebruik van ervaringsgebeurtenissen in reisexpressies/omstandigheden wordt niet ondersteund. Als uw gebruikscase het gebruik van ervaringsgebeurtenissen vereist, overweeg alternatieve methodes. [Meer informatie](../exp-event-lookup.md)

### Voorbeeld 1

We willen controleren of een gebruiker een specifieke versie van een toepassing heeft geïnstalleerd. Hiervoor krijgen we alle pushberichttokens die zijn gekoppeld aan mobiele toepassingen waarvoor de versie 1.0 is. Vervolgens voeren we een voorwaarde uit met de functie **[!UICONTROL count]** om te controleren of de geretourneerde lijst met tokens ten minste één element bevat.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Het resultaat is waar.

### Voorbeeld 2

Hier gebruiken we de functie **[!UICONTROL count]** om te controleren of er pushberichttokens in de verzameling aanwezig zijn.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


Het resultaat is waar.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Het resultaat van de uitdrukking is **3**.


>[!NOTE]
>
>* Wanneer de het filtreren voorwaarde in **allen ()** functie leeg is, zal de filter alle elementen in de lijst terugkeren. **Nochtans, om het aantal elementen van een inzameling te tellen, wordt de alle functie niet vereist.**
>
>* `currentEventField` is alleen beschikbaar wanneer u gebeurtenisverzamelingen manipuleert, `currentDataPackField` wanneer u gegevensbronverzamelingen manipuleert en `currentActionField` wanneer u aangepaste actieverzamelingen bewerkt.
>
>  Wanneer u verzamelingen verwerkt met `all` , `first` en `last` , wordt elk element van de verzameling een voor een herhaald. `currentEventField` , `currentDataPackField` en `currentActionField` komen overeen met het element dat wordt herhaald.


## De eerste (`<condition>`) en laatste (`<condition>`) functies

De functies **[!UICONTROL first]** en **[!UICONTROL last]** laten ook de definitie van een filter op de inzameling toe terwijl het terugkeren van het eerste/laatste element van de lijst die de filter ontmoet.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Voorbeeld 1

Deze expressie retourneert het eerste pushmeldingtoken dat is gekoppeld aan mobiele toepassingen waarvoor de versie 1.0 is.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

Het resultaat is `token_1` .

### Voorbeeld 2

Deze expressie retourneert het laatste pushmeldingtoken dat is gekoppeld aan mobiele toepassingen waarvoor de versie 1.0 is.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Het resultaat is `token_2` .

## De functie at(`<index>`)

Met de functie **[!UICONTROL at]** kunt u naar een specifiek element in een verzameling verwijzen op basis van een index.
Index 0 is de eerste index van de verzameling.

_`<listExpression>`.at(`<index>`)_

### Voorbeeld

Deze expressie retourneert de tweede token voor pushmeldingen van de lijst.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Het resultaat is `token_2` .