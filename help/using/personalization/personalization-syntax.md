---
solution: Journey Optimizer
product: journey optimizer
title: Personalization-syntaxis
description: Leer hoe u de syntaxis van de personalisatie gebruikt.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expressie, editor, syntaxis, personalisatie
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 5e9ce28bf19d2f4406ab4fd395b44b72894928e6
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 1%

---

# Personalization-syntaxis {#personalization-syntax}

Personalization in [!DNL Journey Optimizer] is gebaseerd op de sjabloonsyntaxis Handlebars genoemd. Voor een volledige beschrijving van de syntaxis van Handlebars, verwijs naar [&#x200B; documentatie HandlebarsJS &#x200B;](https://handlebarsjs.com/).

Er worden een sjabloon en een invoerobject gebruikt om HTML of andere tekstopmaak te genereren. Handlebars de malplaatjes kijken als regelmatige teksten met ingebedde uitdrukkingen Handlebars.

Voorbeeld van eenvoudige expressie:

`{{profile.person.name}}`

waarbij:

* `profile` is een naamruimte.
* `person.name` is een token dat wordt samengesteld door kenmerken. De kenmerkstructuur wordt gedefinieerd in een Adobe Experience Platform XDM-schema. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

## Algemene syntaxisregels {#general-rules}

* Id&#39;s kunnen eender welk unicode-teken zijn, behalve de volgende speciale tekens, die zijn gereserveerd voor de syntaxis Handlebars:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* De syntaxis is hoofdlettergevoelig.

* De woorden **waar**, **vals**, **ongeldig** en **niet gedefiniëerd** worden slechts toegestaan in het eerste deel van een weguitdrukking.

* In Handlebars, zijn de waarden die door {{expression}} zijn teruggekeerd **HTML-ontsnapte**. Als de expressie `&` bevat, wordt de geretourneerde uitvoer met escape-teken van HTML gegenereerd als `&amp;` . Als u niet wilt dat Handgrepen aan een waarde ontsnappen, gebruikt u de &#39;&#39;drievoudig-streepje&#39;&#39;.

  Stel dat de waarde van het veld `profile.person.name` &quot;Mark &amp; Mary&quot; is. De syntaxis `{{profile.person.name}}` wordt weergegeven `Mark &amp; Mary` en `{{{profile.person.name}}}` `Mark & Mary` .

* Wat argumenten voor letterlijke functies betreft, ondersteunt de sjabloontaalparser geen enkel unescaped backslash (`\`)-symbool. Aan dit teken moet een extra backslash (`\`) worden toegevoegd. Voorbeeld:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Gereserveerde trefwoorden {#reserved-keywords}

Bepaalde trefwoorden zijn gereserveerd in Profile Query Language (PQL) en kunnen niet rechtstreeks worden gebruikt als veld- of variabelenamen in personalisatie-expressies. Als uw XDM- schema gebieden met namen bevat die gereserveerde sleutelwoorden aanpassen, moet u hen ontsnappen gebruikend backticks (`` ` ``) om hen in uw uitdrukkingen van verwijzingen te voorzien.

**Gereserveerde sleutelwoorden omvatten:**

* `next`
* `last`
* `this`

**Voorbeeld:**

Als uw profielschema een gebied genoemd `next` heeft, moet u het in backticks verpakken:

```
{{profile.person.`next`.name}}
```

Zonder de backticks, zal de verpersoonlijkingsredacteur bevestiging met een fout ontbreken.

## Beschikbare naamruimten {#namespaces}

* **Profiel**

  Dit namespace staat u toe om alle die attributen van verwijzingen te voorzien in het profielschema in [&#x200B; wordt beschreven het Model van Gegevens van Adobe Experience Platform (XDM) documentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

  De attributen moeten in het schema worden bepaald alvorens in een [!DNL Journey Optimizer] verpersoonlijkingsblok wordt van verwijzingen voorzien.

  Voor meer informatie hoe te om profielattributen in voorwaarden te hefboomwerking, verwijs naar [&#x200B; deze sectie &#x200B;](functions/helpers.md#if-function).

  +++Voorbeeldverwijzingen

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Doelgroep**

  Meer over de segmentatiedienst leren, verwijs naar [&#x200B; deze documentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=nl-NL){target="_blank"}.

* **Aanbiedingen**

  Met deze naamruimte kunt u verwijzen naar bestaande aanbiedingen.

  Als u naar een aanbieding wilt verwijzen, moet u een pad declareren met de verschillende gegevens die een aanbieding definiëren. Dit pad heeft de volgende structuur:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  waarbij:

   * `offers` identificeert de padexpressie die hoort bij de aanbiedingsnaamruimte
   * `Type` bepaalt het type van aanbiedingsvertegenwoordiging. Mogelijke waarden zijn: `image` , `html` en `text`
   * `Placement Id` en `Activity Id` zijn plaatsings- en activiteitsidentificatoren
   * `Attributes` zijn specifieke kenmerken die afhankelijk zijn van het aanbiedingstype. Voorbeeld: `deliveryUrl` voor afbeeldingen

  Voor meer informatie over Besluiten API en op de vertegenwoordiging van de Aanbieding, verwijs naar [&#x200B; deze pagina &#x200B;](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  Alle verwijzingen worden bevestigd tegen het Schema van Aanbiedingen met een bevestigingsmechanisme dat op [&#x200B; wordt beschreven deze pagina &#x200B;](../personalization/personalization-build-expressions.md)

  +++Voorbeeldverwijzingen

   * Locatie waar de afbeelding wordt gehost:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * Doel-URL wanneer u op de afbeelding klikt:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Tekstinhoud van het aanbod afkomstig van de beslissingsengine:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * HTML-inhoud van het aanbod afkomstig van de beslissingsmotor:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Helpers {#helpers-all}

Een helper van Handlebars is een eenvoudig herkenningsteken dat door parameters kan worden gevolgd. Elke parameter is een expressie Handlebars. Deze helpers kunnen van om het even welke context in een malplaatje worden betreden.

Deze blokhelpers worden geïdentificeerd door een `#` voorafgaand aan de helpernaam en vereisen een passende sluiting `/`, met dezelfde naam.

Blokken zijn expressies met een blokopening (`{{# }}`) en een sluitend (`{{/}}`).

     voor meer informatie over helperfuncties, verwijs naar [deze sectie] (functions/helpers.md).

## Letterlijke typen {#literal-types}

[!DNL Adobe Journey Optimizer] ondersteunt de volgende letterlijke typen:

| Letterlijk | Definitie |
| ------- | ---------- |
| String | Een gegevenstype dat bestaat uit tekens die worden omringd door dubbele aanhalingstekens. <br> Voorbeelden: `"prospect"` , `"jobs"` , `"articles"` |
| Boolean | Een gegevenstype dat waar of onwaar is. |
| Geheel | Een gegevenstype dat een geheel getal vertegenwoordigt. Het kan positief, negatief, of nul zijn. <br> Voorbeelden: `-201` , `0` , `412` |
| Array | Een gegevenstype dat is samengesteld als een groep andere letterlijke waarden. Er worden vierkante haakjes gebruikt om te groeperen en komma&#39;s om te scheiden tussen verschillende waarden. <br> **Nota:** u kunt tot eigenschappen van punten binnen een serie direct toegang hebben. <br> Voorbeelden: `[1, 4, 7]` , `["US", "FR"]` |

>[!CAUTION]
>
>Het gebruik van **xEvent** variabele is niet beschikbaar in verpersoonlijkingsuitdrukkingen. Elke verwijzing naar xEvent resulteert in validatiefouten.
