---
solution: Journey Optimizer
product: journey optimizer
title: De geavanceerde expressie-editor gebruiken
description: Geavanceerde expressies maken
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: expressie, voorwaarde, use-case, gebeurtenissen
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 1%

---

# Geavanceerde expressievoorbeelden{#advanced-expression-examples}

De Geavanceerde uitdrukkingsredacteur kan worden gebruikt om voorwaarden tot stand te brengen om u toe te staan om gebruikers in uw reizen te filtreren. Met deze voorwaarden kunt u zich richten op gebruikers op tijd, datum, locatie, duur of acties zoals het kopen of verlaten van winkelwagentjes, zodat ze tijdens de reis opnieuw op de doelgroep kunnen worden geplaatst.

>[!NOTE]
>
>Gebeurtenissen beginnen met @, gegevensbronnen met #.

## Voorwaarden voor ervaringsgebeurtenissen opbouwen

De geavanceerde uitdrukkingsredacteur is verplicht om vragen op tijdreeksen zoals een lijst van aankopen of voorbij klikken op berichten uit te voeren. Dergelijke vragen kunnen niet worden uitgevoerd gebruikend de eenvoudige redacteur.

De ervaringsgebeurtenissen worden uit Adobe Experience Platform opgehaald als een verzameling in omgekeerde chronologische volgorde, vandaar:

* De eerste functie retourneert de meest recente gebeurtenis
* last function retourneert de oudste functie.

Bijvoorbeeld, laten wij zeggen u klanten met een kartontroeping in de laatste 7 dagen wilt richten om een bericht te verzenden wanneer de klant dichtbij een opslag, met een aanbieding op punten komt die zij gewild hebben die in opslag zijn.

**U moet de volgende voorwaarden bouwen:**

Ten eerste doelklanten die in de online winkel hebben gebladerd maar de bestelling de laatste 7 dagen niet hebben voltooid.

<!--**This expression looks for a specified value in a string value:**

`In (“addToCart”, #{field reference from experience event})`-->

**Deze expressie zoekt naar alle gebeurtenissen voor deze gebruiker die in de laatste 7 dagen zijn opgegeven:**

Vervolgens worden alle addtocart-gebeurtenissen geselecteerd die niet zijn omgezet in een completePurchase.

>[!NOTE]
>
>Als u snel velden in de expressie wilt invoegen, dubbelklikt u op het veld in het linkerdeelvenster van de editor.

De opgegeven tijdstempel fungeert als datumtijdwaarde en de tweede als aantal dagen.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Deze expressie retourneert een Booleaanse waarde.

**Laten we nu een expressie maken die controleert of het product in voorraad is**

* In Inventory, zoekt deze uitdrukking naar kwantitatief gebied van een product en specificeert dat het groter zou moeten zijn dan 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* Bij het recht, worden de noodzakelijke waarden gespecificeerd, hier, moeten wij de plaats van de opslag terugwinnen, die van de plaats van de gebeurtenis &quot;ArriveLumaStudio&quot;in kaart wordt gebracht:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* En specificeer SKU, gebruikend de functie `first` om de meest recente &quot;addToCart&quot;interactie terug te winnen:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

Vanaf dat punt kunt u een ander pad in uw reis toevoegen voor wanneer het product niet in voorraad is en meldingen verzenden met een serviceaanbieding. Vorm dienovereenkomstig berichten en gebruik verpersoonlijkingsgegevens om het berichtdoel te verbeteren.

## Voorbeelden van tekenreeksbewerkingen met de geavanceerde expressie-editor

**In omstandigheden**

Met deze voorwaarde worden alleen de geofence-gebeurtenissen opgehaald die worden geactiveerd in &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Uitleg: dit is een strikte tekenreeksvergelijking (hoofdlettergevoelig), gelijk aan een query in de eenvoudige modus die gebruikmaakt van `equal to` with `Is sensitive` ingeschakeld.

Dezelfde query met `Is sensitive` unselected zal de volgende uitdrukking op geavanceerde wijze produceren:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**In handelingen**

De volgende uitdrukking staat u toe om identiteitskaart van CRM in een gebied van de actieverpersoonlijking te bepalen:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Uitleg: In dit voorbeeld wordt `substr` en `lastIndexOf` functies om accolades te verwijderen die de CRM-id omsluiten die is doorgegeven met een mobiele startgebeurtenis.

Kijk voor meer informatie over het gebruik van de geavanceerde expressieeditor [deze video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html).
