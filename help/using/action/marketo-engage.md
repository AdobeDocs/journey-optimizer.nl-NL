---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Marketo Engage
description: Meer informatie over het gebruik van de Marketo Engage-actie
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: markt, markt om integratie te bevorderen
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Integreren met Marketo Engage {#integrating-with-marketo-engage}

Sluit een naadloze gegevensintegratie met Marketo Engage aan. Er is een specifieke aangepaste actie beschikbaar op uw reizen om Adobe Journey Optimizer en Marketo Engage te integreren. Deze aangepaste handeling ondersteunt de opname van twee sleutelgegevenstypen:

* **Personen** (Profielen): Marketo zet profielen in actionable inzichten om.
* **de Voorwerpen van de Douane**: Tailor uw gegevens met douanevoorwerpen, zoals producten, voor een gepersonaliseerde marketing benadering.

## Vereisten {#prerequisites}

Aan deze integratie zijn de volgende voorwaarden verbonden:

* De klanteninstantie van Marketo Engage moet zijn ingeschakeld voor IMS
* Marketo Engage-exemplaar en Adobe Experience Platform/Journey Optimizer-exemplaar moeten zich binnen dezelfde organisatie bevinden
* De klant moet met **MktoSync worden voorzien: De toegang van de Dienst van de Opname**

## De handeling configureren {#configure-marketo-action}


In Journey Optimizer moet u een aangepaste handeling voor Marketo Engage configureren. Voer de volgende stappen uit:

1. Selecteer **[!UICONTROL Configurations]** in de sectie van het menu van het Beleid.
1. Klik in de sectie **[!UICONTROL Actions]** op **[!UICONTROL Create Action]** . Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.
1. Ga Naam, Beschrijving in, en selecteer **Adobe Marketo Engage** als **Type van Actie**
   ![](assets/engage-customaction-creation.png){width="40%" align="left"}
1. Klik **uitgeven nuttige lading** pictogram voor uw **Verzoek** en **nuttige lading van de Reactie**.
1. Voor beide, stel uw lading samen en kleef het in specifieke popup.
   ![](assets/engage-customaction-payload.png){width="70%" align="left"}
1. Waarden voor nuttige lading controleren en configureren

   Nota: Om waarden dynamisch over te gaan, voor elke gebiedsverandering **Constante** aan **Variabele**.

   ![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Klik **sparen** in het de configuratiescherm van het Gebied, dan **sparen** uw douaneactie.

U kunt nu uw aangepaste handeling gebruiken op het canvas van uw reis.

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

Voor elke gevormde actie, is een de actieactiviteit van Marketo Engage beschikbaar in het palet van de reisontwerper.

Voer de volgende stappen uit om het te gebruiken:

1. Sleep de aangepaste handeling naar het canvas van de reis.

1. Voer het label en de beschrijving van deze handeling in.

1. In de **sectie van het Verzoek** parameters, klik **geef** pictogram voor elk van de parameters uit en selecteer de dynamische waarden die u in de nuttige lading hebt gevormd.

![](assets/engage-use-canvas.png){width="70%" align="left"}
