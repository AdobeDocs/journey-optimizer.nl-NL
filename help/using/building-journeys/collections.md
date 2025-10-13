---
solution: Journey Optimizer
product: journey optimizer
title: Verzamelingen doorgeven aan aangepaste handelingsparameters
description: Leer hoe u verzamelingen dynamisch doorgeeft in Journey Optimizer met behulp van aangepaste handelingen
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 8a94f9081c4f7fe158c084d02642d5bbba33dca2
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# Verzamelingen doorgeven aan aangepaste handelingsparameters {#passing-collection}

U kunt een verzameling doorgeven in aangepaste handelingsparameters die bij uitvoering dynamisch worden gevuld.

Er worden twee typen verzamelingen ondersteund:

* **Eenvoudige inzamelingen**

  Gebruik eenvoudige verzamelingen voor lijsten met basiswaarden, zoals tekenreeksen, getallen of regeleinden. Deze zijn handig wanneer u alleen een lijst met items zonder extra eigenschappen hoeft door te geven.

  Bijvoorbeeld een lijst met apparaattypen:

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* **de inzamelingen van Objecten**

  Gebruik objectverzamelingen wanneer elk item meerdere velden of eigenschappen bevat. Deze worden doorgaans gebruikt om gestructureerde gegevens door te geven, zoals productdetails, gebeurtenisrecords of itemkenmerken.

  Bijvoorbeeld:

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```

>[!NOTE]
>
>Geneste arrays in verzamelingen worden slechts gedeeltelijk ondersteund in aangepaste handelingen voor opvragingsladingen. Voor details, zie [ Beperkingen ](#limitations).

## Algemene procedure {#general-procedure}

In deze sectie gebruiken we het volgende JSON-payload-voorbeeld. Dit is een array van objecten met een veld dat een eenvoudige verzameling is.

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

U ziet dat `products` een array van twee objecten is. U moet ten minste één object hebben.

1. Maak een aangepaste handeling. Leer meer op [ deze pagina ](../action/about-custom-action-configuration.md).

1. Plak in de sectie **[!UICONTROL Action parameters]** het JSON-voorbeeld. De weergegeven structuur is statisch: bij het plakken van de lading worden alle velden gedefinieerd als constanten.

   ![](assets/uc-collection-1.png)

1. Pas indien nodig de veldtypen aan. De volgende veldtypen worden ondersteund voor verzamelingen: listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject

   >[!NOTE]
   >
   >Het veldtype wordt automatisch afgeleid op basis van het voorbeeld van de payload.

1. Als u objecten dynamisch wilt doorgeven, moet u ze instellen als variabelen. In dit voorbeeld stellen we `products` in als variabele. Alle objectvelden in het object worden automatisch ingesteld op variabelen.

   >[!NOTE]
   >
   >Het eerste object van het ladingsvoorbeeld wordt gebruikt om de velden te definiëren.

1. Definieer voor elk veld het label dat op het canvas van de reis wordt weergegeven.

   ![](assets/uc-collection-2.png){width="70%" align="left"}

1. Maak uw reis en voeg de aangepaste actie toe die u hebt gemaakt. Leer meer op [ deze pagina ](../building-journeys/using-custom-actions.md).

1. Definieer in de sectie **[!UICONTROL Action parameters]** de arrayparameter (`products` in ons voorbeeld) met de geavanceerde expressie-editor.

   ![](assets/uc-collection-3.png)

1. Typ voor elk van de volgende objectvelden de corresponderende veldnaam in het XDM-bronschema. Als de namen identiek zijn, is dit niet nodig. In ons voorbeeld hoeven we alleen `product id` en &quot;color&quot; te definiëren.

   ![](assets/uc-collection-4.png){width="50%" align="left"}

Voor het matrixveld kunt u ook de geavanceerde expressie-editor gebruiken om gegevensbewerkingen uit te voeren. In het volgende voorbeeld, gebruiken wij de [ filter ](functions/functionfilter.md) en [ ](functions/functionintersect.md) functies doorsnijden:

![](assets/uc-collection-5.png)

## Beperkingen {#limitations}

Hoewel verzamelingen in aangepaste acties flexibiliteit bieden voor het doorgeven van dynamische gegevens, zijn er bepaalde structurele beperkingen die u moet kennen:

* **Steun voor Geneste Arrays in de Acties van de Douane**

  Adobe Journey Optimizer steunt genestelde series van voorwerpen in douaneactie **antwoordladloads**, maar deze steun is beperkt in **verzoeklading**.

  In request-payloads worden geneste arrays alleen ondersteund wanneer ze een vast aantal items bevatten, zoals gedefinieerd in de aangepaste actieconfiguratie. Bijvoorbeeld, als een genestelde serie altijd precies drie punten omvat, kan het als constante worden gevormd. Wanneer het aantal items dynamisch moet zijn, kunnen alleen niet-geneste arrays (arrays op het onderste niveau) als variabelen worden gedefinieerd.

  Voorbeeld:

   1. Het volgende voorbeeld illustreert a **niet-gesteund gebruiksgeval**.

      In dit voorbeeld bevat de productarray een geneste array (`locations`) met een dynamisch aantal items. Deze array wordt niet ondersteund in aanvraagladingen.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. Ondersteund, bijvoorbeeld met vaste items die zijn gedefinieerd als constanten.

      In dit geval worden de geneste locaties vervangen door vaste velden (`location1`, `location2` ), zodat de laadgegevens geldig blijven in de ondersteunde configuratie.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* **het Testen inzamelingen**: Om inzamelingen te testen gebruikend testwijze, moet u de wijze van de codemening gebruiken. Merk op dat de wijze van de codemening niet voor bedrijfsgebeurtenissen wordt gesteund, zodat in dat geval, kunt u slechts een inzameling verzenden die één enkel element bevat.


## Bijzondere gevallen{#examples}

Voor heterogene typen en arrays van arrays wordt de array gedefinieerd met het listAny-type. U kunt alleen afzonderlijke items toewijzen, maar u kunt de array niet wijzigen in een variabele.

![](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

Voorbeeld van een heterogeen type:

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

Voorbeeld van array van arrays:

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

## Aanvullende bronnen

Blader in de onderstaande secties voor meer informatie over het configureren, gebruiken en oplossen van problemen met aangepaste handelingen:

* [ worden begonnen met douaneacties ](../action/action.md) - leer wat een douaneactie is en hoe zij u met uw derdesystemen helpen verbinden
* [ vorm uw douaneacties ](../action/about-custom-action-configuration.md) - leer hoe te om een douaneactie tot stand te brengen en te vormen
* [ de douaneacties van het Gebruik ](../building-journeys/using-custom-actions.md) - leer hoe te om douaneacties in uw reizen te gebruiken
* [ het oplossen van problemen van de Actie van de Douane ](../action/troubleshoot-custom-action.md) - Leer hoe te om een douaneactie problemen op te lossen

