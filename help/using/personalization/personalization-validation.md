---
title: Validatie van personalisatie
description: Meer informatie over validatie van personalisatie en hoe u problemen kunt oplossen
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---


# Validatie van personalisatie {#personalization-validation}

## Validatiemechanismen

In het scherm van de redacteur van de Uitdrukking, staat **Validate** knoop u toe om uw verpersoonlijkingssyntaxis te bevestigen.

>[!NOTE]
> De validatie wordt automatisch uitgevoerd wanneer u op **Add** klikt om het editorvenster te sluiten.


![](assets/perso_validation1.png)

>[!IMPORTANT]
> Als de verpersoonlijkingssyntaxis ongeldig is, kunt u niet het venster van de uitdrukkingsredacteur sluiten.


## Veelvoorkomende fouten

* **Pad &quot;XYZ&quot; niet gevonden**

Wanneer u probeert te verwijzen naar een veld dat niet in het schema is gedefinieerd.

In dit geval wordt **firstName1** niet gedefinieerd als kenmerk in het profielschema:

```
{{profile.person.name.firstName1}}
```

* **Type mismatch voor variabele &quot;XYZ&quot;. Array verwacht. Gevonden tekenreeks.**

Wanneer u probeert een tekenreeks in plaats van een array te doorlopen:

In dit geval is **product** geen array:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Ongeldige syntaxis voor handgrepen.`‘[XYZ}}’`** gevonden

Wanneer een ongeldige syntaxis voor het stuur wordt gebruikt.

Handlebars uitdrukkingen zijn omringd met **{{expression}**

```
   {{[profile.person.name.firstName}}
```

* **Ongeldige segmentdefinitie**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### Specifieke fouten met betrekking tot aanbiedingen

De fouten met betrekking tot aanbiedingen integratie in een E-mail of Duw bericht hebben het volgende patroon:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

De bevestiging wordt uitgevoerd tijdens de berichtpublicatie of tijdens de bevestiging van de verpersoonlijkingsinhoud in de redacteur van de Uitdrukking.

<table> 
 <thead> 
  <tr> 
   <th> Fouttitel<br /> </th> 
   <th> Validatie/resolutie <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Resource met id placementID en type OfferPlacement niet gevonden <br/>
Bron met id activityID en type OfferActivity niet gevonden<br/></td> 
   <td>Controleren of ActivityID en/of PlacementID beschikbaar zijn</td> 
  </tr> 
   <tr> 
   <td>Bron kan niet worden gevalideerd.</td> 
   <td>Het componenttype in de Placement moet overeenkomen met de aanbiedingType</td> 
  </tr> 
   <tr> 
   <td>De openbare URL komt niet voor in de aanbiedings-id.</td> 
   <td>De afbeeldingsaanbiedingen (alle gepersonaliseerde en reservekopieën die aan de beslissing en het plaatsingspaar zijn gekoppeld) moeten een openbare URL hebben die is gevuld (de bezorgings-URL mag niet leeg zijn).</td> 
  </tr> 
  <tr> 
   <td>Het besluit (voorheen bekend als aanbiedingsactiviteit) bevat niet-profielkenmerken.</td> 
   <td>Het modelgebruik van aanbiedingen mag alleen de profielkenmerken bevatten.</td> 
  </tr> 
  <tr> 
   <td>Er is een fout opgetreden tijdens het ophalen van het beslissingsgebruik.</td> 
   <td>Deze fout kan optreden wanneer de API het aanbiedingsmodel probeert op te halen.</td> 
  </tr>
  <tr> 
   <td>Het aanbiedingskenmerk van kenmerk is ongeldig.</td> 
   <td>Controleer of het aanbiedingskenmerk waarnaar wordt verwezen in het aanbiedingsconcept geldig is. Hier volgen de geldige kenmerken: <br/>
Afbeelding: deliveryURL, linkURL<br/>
Tekst: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>

