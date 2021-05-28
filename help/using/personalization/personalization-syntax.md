---
title: Personalisatiesyntaxis
description: Leer hoe u de syntaxis voor personalisatie gebruikt
source-git-commit: 7e20bef085d0fa6983f9ebd84f8cbc3bee2f4542
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 3%

---

# Personalisatiesyntaxis {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

Personalisatie in [!DNL Journey Optimizer] is gebaseerd op de sjabloonsyntaxis genoemd Handlebars.
Voor een volledige beschrijving van de syntaxis Handlebars, verwijs naar [documentatie HandlebarsJS](https://handlebarsjs.com/).

Er worden een sjabloon en een invoerobject gebruikt om HTML of andere tekstindelingen te genereren. Handlebars de malplaatjes kijken als regelmatige teksten met ingebedde uitdrukkingen Handlebars.

Voorbeeld van eenvoudige expressie:

```sql
{{profile.person.name}}
```

waarbij:

* **** profiel is een naamruimte.
* **person.** namis een token dat wordt samengesteld door kenmerken. De kenmerkstructuur wordt gedefinieerd in een Adobe Experience Platform XDM-schema. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).

## Algemene syntaxisregels

Id&#39;s kunnen eender welk unicode-teken zijn, behalve de volgende:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

De syntaxis is hoofdlettergevoelig.

De woorden **true**, **false**, **null** en **undefined** zijn alleen toegestaan in het eerste deel van een padexpressie.

In Handlebars, zijn de waarden die door {expression} worden teruggekeerd **HTML-ontsnapte**. Als de expressie &amp; bevat, wordt de geretourneerde uitvoer met HTML-escape gegenereerd als &amp;. Als u niet wilt dat Handgrepen aan een waarde ontsnappen, gebruikt u de &#39;&#39;drievoudig-streepje&#39;&#39;.

## Profiel

Met deze naamruimte kunt u verwijzen naar alle kenmerken die zijn gedefinieerd in het profielschema dat wordt beschreven in [Adobe Experience Platform-gegevensmodel (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

De attributen moeten in het schema worden bepaald alvorens in een [!DNL Journey Optimizer] verpersoonlijkingsblok wordt van verwijzingen voorzien.

Alle verwijzingen worden bevestigd tegen het Schema van het Profiel met een bevestigingsmechanisme dat in [deze pagina](personalization-validation.md) wordt beschreven.

**Voorbeeldreferenties:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

>[!NOTE]
>
>Leer hoe u profielkenmerken in voorwaarden in [deze sectie](functions/helpers.md#if-function) kunt gebruiken.

## Segmenten{#perso-segments}

Leer hoe u profielkenmerken in voorwaarden in [deze sectie](functions/helpers.md#if-function) kunt gebruiken.

>[!NOTE]
>Raadpleeg [deze sectie](../segment/about-segments.md) voor meer informatie over segmentatie en segmentatieservice.


## Aanbiedingen

Met deze naamruimte kunt u verwijzen naar bestaande aanbiedingen.
Als u naar een aanbieding wilt verwijzen, moet u een pad declareren met de verschillende gegevens die een aanbieding definiëren.

Dit pad heeft de volgende structuur:
0 - &quot;aanbiedingen&quot;: identificeert de weguitdrukking die tot aanbiedingsnamespace behoort
1 - Type: bepaalt het type van aanbiedingsvertegenwoordiging. Geldige waarden zijn &#39;image&#39;, &#39;html&#39; en &#39;text&#39;
2 - Plaatsing-id
3 - Activiteits-id
4 - Bied specifieke kenmerken aan. Afhankelijk van het aanbiedingstype kunnen ondersteunde kenmerken worden gebruikt. Bijvoorbeeld voor afbeeldingen `deliveryUrl`.

Raadpleeg [deze pagina](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api) voor meer informatie over de API voor beslissingen.

Voor meer informatie over de Vertegenwoordiging van Aanbiedingen, verwijs naar [deze pagina](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Alle verwijzingen worden bevestigd tegen het Schema van Aanbiedingen met een bevestigingsmechanisme dat in [deze pagina](personalization-validation.md) wordt beschreven.

**Voorbeeldreferenties:**

* Locatie waar de afbeelding wordt gehost:

   ```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* Doel-URL wanneer u op de afbeelding klikt:

   ```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Tekstinhoud van het aanbod afkomstig van de beslissingsmotor:

   ```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* HTML-inhoud van het aanbod afkomstig van de beslissingsengine:

   ```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Helpers{#helpers-all}

Een helper van Handlebars is een eenvoudig herkenningsteken dat door parameters kan worden gevolgd.
Elke parameter is een expressie Handlebars. Deze helpers kunnen van om het even welke context in een malplaatje worden betreden.

Deze blokhelpers worden geïdentificeerd door # die de helpernaam voorafgaat en vereisen een passende sluiting /, van de zelfde naam.
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
