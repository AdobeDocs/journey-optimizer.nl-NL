---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Marketo Engage
description: Leer hoe u de handeling Marketo Engage gebruikt
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: markt, markt om integratie te bevorderen
source-git-commit: 6a49f4b2e0220b1c875b42f70dcb44f3405c6ad2
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Integreren met Marketo Engage {#integrating-with-marketo-engage}

Sluit een naadloze gegevensintegratie met Marketo Engage aan. Deze specifieke aangepaste handeling in Journey Optimizer ondersteunt de inname van twee sleutelgegevenstypen:

* Personen (profielen): Marketo transformeert profielen naar inzichten die kunnen worden gebruikt.
* Aangepaste objecten: leg uw gegevens af met aangepaste objecten, zoals producten, voor een gepersonaliseerde marketingaanpak.

## Vereisten {#prerequisites}

* De klanteninstantie van Marketo Engage moet IMS-Toegelaten zijn.
* Marketo Engage-instantie en AEP/AJO-instantie moeten zich in dezelfde IMS Org bevinden. +link
* De klant moet zijn voorzien van MktoSync: Toegang tot Ingestieservice (NOTA AAN ADD HIER + verbinding)

## De handeling configureren {#configure-marketo-action}

* Ga naar Beheer > Configuraties > Handelingen en klik op Beheren
* Klik in de lijst Handelingen op Handeling maken. Meer informatie over het maken van aangepaste handelingen vindt u hier (+link)
* Typ naam, beschrijving en selecteer Adobe Marketo Engage als type handeling

![](assets/engage-customaction-creation.png)

* Klik uitgeven nuttige lading voor uw **Verzoek** en **nuttige ladingen van de Reactie**.
* Voor beide, stel uw lading samen en plak het in specifieke popup.

![](assets/engage-customaction-payload.png)

* Inspect en payloadwaarden configureren
Nota: Om waarden dynamisch over te gaan, voor elke gebiedsverandering **Constante** aan **Variabele**.

![](assets/engage-customaction-payload-fields.png)

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

* Sleep de aangepaste handeling naar het canvas van de reis. (Zie hoe u een aangepaste handeling / koppeling kunt gebruiken)
* In de parameters van het Verzoek, geeft de klik voor elk van de parameters met dynamische waarden uit die u in de lading hebt gevormd.

![](assets/engage-use-canvas.png)

