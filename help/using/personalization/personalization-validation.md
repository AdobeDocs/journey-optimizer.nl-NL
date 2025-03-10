---
solution: Journey Optimizer
product: journey optimizer
title: Personalization-validatie
description: Leer meer over verpersoonlijkingsbevestiging en hoe te om problemen op te lossen.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressie, editor, validatie, fouten, personalisatie
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Personalization-validatie {#personalization-validation}

## Validatiemechanismen {#validation-mechanisms}

In het **verpersoonlijkingsredacteur** scherm, gebruik **bevestigt** knoop om uw verpersoonlijkingssyntaxis te controleren.

>[!NOTE]
> De bevestiging wordt automatisch uitgevoerd wanneer u op **klikt voeg** knoop toe om het editorvenster te sluiten.
>

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Als de verpersoonlijkingssyntaxis ongeldig is, kunt u niet het venster van de verpersoonlijkingsredacteur sluiten.
>

## Algemene fouten {#common-errors}

* **Weg &quot;XYZ&quot;niet gevonden**

Wanneer u probeert te verwijzen naar een veld dat niet in het schema is gedefinieerd.

In dit geval **firstName1** wordt niet bepaald als attribuut in het profielschema:

```
{{profile.person.name.firstName1}}
```

* **Type wanverhouding voor veranderlijke &quot;XYZ&quot;. Array verwacht. Gevonden tekenreeks.**

Wanneer u probeert een tekenreeks in plaats van een array te doorlopen:

In dit geval **product** is geen serie:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Ongeldige zakbalksyntaxis. Gevonden`‘[XYZ}}’`**

Wanneer een ongeldige syntaxis voor het stuur wordt gebruikt.

Handlebars-expressies worden omringd met **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Ongeldige segmentdefinitie**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Specifieke fouten met betrekking tot aanbiedingen {#specific-errors}

De fouten met betrekking tot aanbiedingen integratie in een E-mail of Duw bericht hebben het volgende patroon:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

De bevestiging wordt uitgevoerd tijdens de bevestiging van de verpersoonlijkingsinhoud in de verpersoonlijkingsredacteur.

<table> 
 <thead> 
  <tr> 
   <th> Fouttitel <br /> </th> 
   <th> Validatie/resolutie <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Bron met id placementID en type OfferPlacement niet gevonden <br/>
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
   <td>De beslissing bevat niet-profielkenmerken.</td> 
   <td>Het modelgebruik van aanbiedingen mag alleen de profielkenmerken bevatten.</td> 
  </tr> 
  <tr> 
   <td>Er is een fout opgetreden tijdens het ophalen van het beslissingsgebruik.</td> 
   <td>Deze fout kan optreden wanneer de API het aanbiedingsmodel probeert op te halen.</td> 
  </tr>
  <tr> 
   <td>Het aanbiedingskenmerk van kenmerk is ongeldig.</td> 
   <td>Controleer of het aanbiedingskenmerk waarnaar wordt verwezen in het aanbiedingsconcept geldig is. Hier volgen de geldige kenmerken: <br/>
Afbeelding: deliveryURL, linkURL <br/>
Tekst: inhoud <br/>
HTML: inhoud<br/></td> 
  </tr> 
 </tbody> 
</table>
