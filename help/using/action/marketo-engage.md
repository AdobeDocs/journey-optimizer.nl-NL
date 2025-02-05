---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Marketo Engage
description: Leer hoe u de handeling Marketo Engage gebruikt
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: markt, markt om integratie te bevorderen
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: 844c0f8dc9b14d69cbd87893042f048443d7a5e6
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Integreren met Marketo Engage {#integrating-with-marketo-engage}

Sluit een naadloze gegevensintegratie met Marketo Engage aan. Deze specifieke aangepaste handeling in Journey Optimizer ondersteunt de inname van twee sleutelgegevenstypen:

* Personen (profielen): Marketo transformeert profielen naar inzichten die kunnen worden gebruikt.
* Aangepaste objecten: leg uw gegevens af met aangepaste objecten, zoals producten, voor een gepersonaliseerde marketingaanpak.

## Vereisten {#prerequisites}

* De klanteninstantie van Marketo Engage moet IMS-Toegelaten zijn.
* Het exemplaar van het Marketo Engage en de instantie Adobe Experience Platform/Journey Optimizer moeten in de zelfde organisatie zijn.
* De klant moet met **MktoSync worden voorzien: De toegang van de Dienst van de Opname**

## De handeling configureren {#configure-marketo-action}

* Ga naar Beheer > Configuraties > Handelingen en klik op Beheren
* Klik in de lijst Handelingen op Handeling maken. Lees meer op [ de acties van de Douane ](../building-journeys/using-custom-actions.md){target="_blank"}.
* Typ naam, beschrijving en selecteer Adobe Marketo Engage als type handeling

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Klik uitgeven nuttige lading voor uw **Verzoek** en **nuttige ladingen van de Reactie**.
* Voor beide, stel uw lading samen en plak het in specifieke popup.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspect en payloadwaarden configureren
Nota: Om waarden dynamisch over te gaan, voor elke gebiedsverandering **Constante** aan **Variabele**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* Klik **sparen** in het de configuratievenster van het Gebied toen **sparen** voor uw douaneactie.

U kunt nu uw aangepaste handeling op uw toegewijde canvas gebruiken.


## Payloadsyntaxis {#payload-syntax}

### Persoon

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Voorbeeld van de Payload voor Persoon**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Voorbeeld van de Lading voor het Voorwerp van de Douane**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## De handeling gebruiken {#engage-using}

* Sleep de aangepaste handeling naar het canvas van de reis.
* In de **sectie van het Verzoek** parameters, geeft de klik voor elk van de parameters met dynamische waarden uit die u in de nuttige lading hebt gevormd.

![](assets/engage-use-canvas.png){width="70%" align="left"}
