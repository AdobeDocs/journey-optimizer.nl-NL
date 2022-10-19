---
solution: Journey Optimizer
product: journey optimizer
title: Personalisatiesyntaxis
description: Leer hoe u de syntaxis van de personalisatie gebruikt.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 3%

---

# Personalisatiesyntaxis {#personalization-syntax}

Personalisatie in [!DNL Journey Optimizer] is gebaseerd op de sjabloonsyntaxis met de naam Handlebars.
Voor een volledige beschrijving van de syntaxis Handlebars, verwijs naar [HandlebarsJS documentatie](https://handlebarsjs.com/).

Er worden een sjabloon en een invoerobject gebruikt om HTML of andere tekstindelingen te genereren. Handlebars de malplaatjes kijken als regelmatige teksten met ingebedde uitdrukkingen Handlebars.

Voorbeeld van eenvoudige expressie:

`{{profile.person.name}}`

waarbij:

* `profile` is een naamruimte.
* `person.name` is een token dat wordt samengesteld door kenmerken. De kenmerkstructuur wordt gedefinieerd in een Adobe Experience Platform XDM-schema. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

## Algemene syntaxisregels {#general-rules}

Id&#39;s kunnen eender welk unicode-teken zijn, behalve de volgende:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

De syntaxis is hoofdlettergevoelig.

De woorden **true**, **false**, **null** en **ongedefinieerd** zijn alleen toegestaan in het eerste deel van een padexpressie.

In Handlebars, zijn de waarden teruggekeerd door {{expression}} zijn **HTML-ontsnapt**. Als de expressie `&`, dan wordt de teruggekeerde HTML-beschermde output geproduceerd zoals `&amp;`. Als u niet wilt dat Handgrepen aan een waarde ontsnappen, gebruikt u de &#39;&#39;drievoudig-streepje&#39;&#39;.

Wat argumenten voor letterlijke functies betreft, ondersteunt de parser voor sjabloontaal geen enkele backslash zonder escape-teken (`\`). Dit teken moet met een extra backslash (`\`). Voorbeeld :

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Profiel

Met deze naamruimte kunt u verwijzen naar alle kenmerken die zijn gedefinieerd in het profielschema dat wordt beschreven in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

De attributen moeten in het schema worden bepaald alvorens in a wordt van verwijzingen voorzien [!DNL Journey Optimizer] verpersoonlijkingsblok.

>[!NOTE]
>
>Leer hoe u onder de volgende omstandigheden profielkenmerken kunt gebruiken [deze sectie](functions/helpers.md#if-function).

**Voorbeeldreferenties:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmenten{#perso-segments}

Leer hoe u onder de volgende omstandigheden profielkenmerken kunt gebruiken [deze sectie](functions/helpers.md#if-function).

>[!NOTE]
>Voor meer informatie over segmentatie en segmentatieservice raadpleegt u [deze sectie](../segment/about-segments.md).

## Aanbiedingen {#offers-syntax}

Met deze naamruimte kunt u verwijzen naar bestaande aanbiedingen.
Als u naar een aanbieding wilt verwijzen, moet u een pad declareren met de verschillende gegevens die een aanbieding definiëren.

Dit pad heeft de volgende structuur:

`offers.Type.[Placement Id].[Activity Id].Attribute`

waarbij:

* `offers` identificeert de weguitdrukking die tot aanbiedingsnamespace behoort
* `Type`  bepaalt het type van aanbiedingsvertegenwoordiging. Mogelijke waarden zijn: `image`, `html` en `text`
* `Placement Id` en `Activity Id` zijn plaatsing- en activiteitsidentificatoren
* `Attributes` specifieke kenmerken aanbieden die afhankelijk zijn van het soort aanbieding. Voorbeeld: `deliveryUrl` voor afbeeldingen

Voor meer informatie over Besluiten API en over de Vertegenwoordiging van Aanbiedingen, verwijs naar [deze pagina](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Alle verwijzingen worden bevestigd tegen het Schema van Aanbiedingen met een bevestigingsmechanisme dat in wordt beschreven [deze pagina](personalization-validation.md)

**Voorbeeldreferenties:**

* Locatie waar de afbeelding wordt gehost:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* Doel-URL wanneer u op de afbeelding klikt:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Tekstinhoud van het aanbod afkomstig van de beslissingsengine:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML inhoud van het aanbod afkomstig van de beslissingsmotor:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helpers{#helpers-all}

Een helper van Handlebars is een eenvoudig herkenningsteken dat door parameters kan worden gevolgd.
Elke parameter is een expressie Handlebars. Deze helpers kunnen van om het even welke context in een malplaatje worden betreden.

Deze blokhelpers worden geïdentificeerd door # voorafgaand aan de helpernaam en vereisen een passende sluiting /, van de zelfde naam.
Blokken zijn expressies met een blokopening ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>Helperfuncties worden beschreven in [deze sectie](functions/helpers.md).

## Letterlijke typen {#literal-types}

[!DNL Adobe Journey Optimizer] ondersteunt de volgende letterlijke typen:

| Letterlijk | Definitie |
| ------- | ---------- |
| Tekenreeks | Een gegevenstype dat bestaat uit tekens die tussen dubbele aanhalingstekens staan. <br>Voorbeelden: `"prospect"`, `"jobs"`, `"articles"` |
| Boolean | Een gegevenstype dat waar of onwaar is. |
| Geheel | Een gegevenstype dat een geheel getal vertegenwoordigt. Het kan positief, negatief, of nul zijn. <br>Voorbeelden: `-201`, `0`, `412` |
| Array | Een gegevenstype dat is samengesteld als een groep andere letterlijke waarden. Er worden vierkante haakjes gebruikt om te groeperen en komma&#39;s om te scheiden tussen verschillende waarden. <br> **Opmerking:** U hebt niet rechtstreeks toegang tot eigenschappen van items binnen een array. <br> Voorbeelden: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Het gebruik van **xEvent** variable is not available in personalization expressions. Elke verwijzing naar xEvent resulteert in validatiefouten.

## URL-personalisatie{#perso-urls}

Persoonlijke URL&#39;s sturen ontvangers naar specifieke pagina&#39;s van een website of naar een gepersonaliseerde microsite, afhankelijk van de profielkenmerken. In Adobe Journey Optimizer kunt u personalisatie toevoegen aan URL&#39;s in de inhoud van uw bericht. U kunt URL-aanpassing toepassen op tekst en afbeeldingen en profielgegevens of contextafhankelijke gegevens gebruiken.

Met Journey Optimizer kunt u een of meer URL&#39;s in uw bericht aanpassen door er personalisatievelden aan toe te voegen. Volg onderstaande stappen om een URL aan te passen:

1. Maak een koppeling in de inhoud van het bericht. [Meer informatie](../design/message-tracking.md#insert-links)
1. Selecteer de kenmerken in het verpersoonlijkingspictogram. Het verpersoonlijkingspictogram is alleen beschikbaar voor deze typen koppelingen: **Externe koppeling**, **Koppeling met abonnement opheffen** en **Uitschakelen**.

![](assets/perso-url.png)

>[!NOTE]
>
>In de uitdrukkingsredacteur, wanneer u een gepersonaliseerde URL uitgeeft, zijn de hulpfuncties en segmentlidmaatschap om veiligheidsredenen gehandicapt.

**Voorbeeld van gepersonaliseerde URL&#39;s**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Spaties worden niet ondersteund in de personalisatietokens die in URL&#39;s worden gebruikt.
