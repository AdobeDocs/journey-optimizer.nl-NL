---
title: Personalisatiesyntaxis
description: Leer hoe u de syntaxis voor personalisatie gebruikt
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 1cf3475d7b2b990db4b2217bb03a47b76692142c
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 3%

---

# Personalisatiesyntaxis {#personalization-syntax}

Personalisatie in [!DNL Journey Optimizer] is gebaseerd op de sjabloonsyntaxis genoemd Handlebars.
Voor een volledige beschrijving van de syntaxis Handlebars, verwijs naar [documentatie HandlebarsJS](https://handlebarsjs.com/).

Er worden een sjabloon en een invoerobject gebruikt om HTML of andere tekstindelingen te genereren. Handlebars de malplaatjes kijken als regelmatige teksten met ingebedde uitdrukkingen Handlebars.

Voorbeeld van eenvoudige expressie:

`{{profile.person.name}}`

waarbij:

* `profile` is een naamruimte.
* `person.name` is een token dat wordt samengesteld door kenmerken. De kenmerkstructuur wordt gedefinieerd in een Adobe Experience Platform XDM-schema. [Meer](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) informatie {target=&quot;_blank&quot;}.

## Algemene syntaxisregels

Id&#39;s kunnen eender welk unicode-teken zijn, behalve de volgende:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

De syntaxis is hoofdlettergevoelig.

De woorden **true**, **false**, **null** en **undefined** zijn alleen toegestaan in het eerste deel van een padexpressie.

In Handlebars, zijn de waarden die door {expression} worden teruggekeerd **HTML-ontsnapte**. Als de expressie `&` bevat, wordt de geretourneerde uitvoer met HTML-escape gegenereerd als `&amp;`. Als u niet wilt dat Handgrepen aan een waarde ontsnappen, gebruikt u de &#39;&#39;drievoudig-streepje&#39;&#39;.

## Profiel

Dit namespace staat u toe om alle die attributen van verwijzingen te voorzien in het profielschema in [Adobe Experience Platform het Model van Gegevens (XDM) documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) {target= &quot;_blank&quot;} wordt beschreven.

De attributen moeten in het schema worden bepaald alvorens in een [!DNL Journey Optimizer] verpersoonlijkingsblok wordt van verwijzingen voorzien.

>[!NOTE]
>
>Leer hoe u profielkenmerken in voorwaarden in [deze sectie](functions/helpers.md#if-function) kunt gebruiken.

**Voorbeeldreferenties:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmenten{#perso-segments}

Leer hoe u profielkenmerken in voorwaarden in [deze sectie](functions/helpers.md#if-function) kunt gebruiken.

>[!NOTE]
>Raadpleeg [deze sectie](../segment/about-segments.md) voor meer informatie over segmentatie en segmentatieservice.

## Aanbiedingen

Met deze naamruimte kunt u verwijzen naar bestaande aanbiedingen.
Als u naar een aanbieding wilt verwijzen, moet u een pad declareren met de verschillende gegevens die een aanbieding definiëren.

Dit pad heeft de volgende structuur:

`offers.Type.[Placement Id].[Activity Id].Attribute`

waarbij:

* `offers` identificeert de weguitdrukking die tot aanbiedingsnamespace behoort
* `Type`  bepaalt het type van aanbiedingsvertegenwoordiging. Mogelijke waarden zijn: `image`, `html` en `text`
* `Placement Id` en  `Activity Id` zijn plaatsings- en activiteitsidentificatoren
* `Attributes` specifieke kenmerken aanbieden die afhankelijk zijn van het soort aanbieding. Voorbeeld: `deliveryUrl` voor afbeeldingen

Voor meer informatie over Besluiten API en over de Vertegenwoordiging van Aanbiedingen, verwijs naar [deze pagina](../../using/offers/api-reference/decisions-api/deliver-offers.md)

Alle verwijzingen worden bevestigd tegen het Schema van Aanbiedingen met een bevestigingsmechanisme dat in [deze pagina](personalization-validation.md) wordt beschreven

**Voorbeeldreferenties:**

* Locatie waar de afbeelding wordt gehost:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* Doel-URL wanneer u op de afbeelding klikt:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Tekstinhoud van het aanbod afkomstig van de beslissingsengine:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML-inhoud van het aanbod afkomstig van de beslissingsengine:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helpers{#helpers-all}

Een helper van Handlebars is een eenvoudig herkenningsteken dat door parameters kan worden gevolgd.
Elke parameter is een expressie Handlebars. Deze helpers kunnen van om het even welke context in een malplaatje worden betreden.

Deze blokhelpers worden geïdentificeerd door # voorafgaand aan de helpernaam en vereisen een passende sluiting /, van de zelfde naam.
Blokkeringen zijn expressies met een blokopening ({{# }}) en een sluitend ({{/}).


>[!NOTE]
>
>Helperfuncties worden beschreven in [deze sectie](functions/helpers.md).

## Letterlijke typen

[!DNL Adobe Journey Optimizer] ondersteunt de volgende letterlijke typen:

| Letterlijk | Definitie |
| ------- | ---------- |
| Tekenreeks | Een gegevenstype dat bestaat uit tekens die tussen dubbele aanhalingstekens staan. <br>Voorbeelden: `"prospect"`, `"jobs"`, `"articles"` |
| Boolean | Een gegevenstype dat waar of onwaar is. |
| Geheel | Een gegevenstype dat een geheel getal vertegenwoordigt. Het kan positief, negatief, of nul zijn. <br>Voorbeelden: `-201`, `0`, `412` |
| Array | Een gegevenstype dat is samengesteld als een groep andere letterlijke waarden. Er worden vierkante haakjes gebruikt om te groeperen en komma&#39;s om te scheiden tussen verschillende waarden. <br> **Opmerking:** u hebt niet rechtstreeks toegang tot eigenschappen van items binnen een array. <br> Voorbeelden: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Het gebruik van **xEvent** variabele is niet beschikbaar in verpersoonlijkingsuitdrukkingen. Elke verwijzing naar xEvent resulteert in validatiefouten.

## URL-personalisatie{#perso-urls}

Met Journey Orchestration kunt u een of meer URL&#39;s in uw bericht aanpassen door er personalisatievelden aan toe te voegen. Dit doet u als volgt:

* Maak een koppeling in uw e-mail- of pushinhoud. Als u meer wilt weten over het maken van koppelingen, raadpleegt u [deze pagina](../message-tracking.md#insert-links)).
* Klik op het verpersoonlijkingspictogram. Dit pictogram is beschikbaar voor deze specifieke typen koppelingen: **Externe koppeling**, **Niet-abonnementskoppeling** en **Opt-Out**.

![](assets/perso-url.png)

>[!NOTE]
>
>In de uitdrukkingsredacteur, wanneer u een gepersonaliseerde URL uitgeeft, zijn de hulpfuncties en segmentlidmaatschap om veiligheidsredenen gehandicapt.

** Voorbeeld van gepersonaliseerde URL&#39;s **

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

