---
title: Aan de slag met Experience Decisition
description: Ervaar meer over het beslissen van ervaring
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 1%

---

# Aan de slag met Experience Decisition {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* **[Aan de slag met Experience Decisition](gs-experience-decisioning.md)**
* Je beslissingsobjecten beheren
   * [De itemcatalogus configureren](catalogs.md)
   * [Beslissingsitems maken](items.md)
   * [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren
   * [Beslissingsregels maken](rules.md)
   * [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

## Wat is Experience Decisition {#about}

>[!AVAILABILITY]
>
>De ervaringsbeslissingsfunctie is momenteel beschikbaar als een bètafunctie om alleen gebruikers te selecteren. Neem contact op met de klantenservice van de Adobe om deel te nemen aan het bètaprogramma.

Ervaring Beslissen vereenvoudigt personalisatie door een gecentraliseerde catalogus van marketingaanbiedingen aan te bieden, die bekend staan als &#39;beslissingspunten&#39; en een geavanceerde beslissingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.

Deze beslissingsitems worden naadloos geïntegreerd in een breed scala aan binnenkomende oppervlakken via het nieuwe op code gebaseerde ervaringskanaal, dat nu toegankelijk is in Journey Optimizer-campagnes.

**Beperkingen:**

* Beslissingsbeleid is alleen beschikbaar voor gebruik in op code gebaseerde ervaringscampagnes.
* Vooralsnog is geen functie voor het aftoppen van frequenties beschikbaar in Experience Decisioning.

## Belangrijkste stappen bij het nemen van beslissingen {#steps}

De belangrijkste stappen om met de Beslissing van de Ervaring te werken zijn als volgt:

1. **Aangepaste kenmerken configureren**: U kunt de catalogus met beslissingsitems afstemmen op uw specifieke vereisten door aangepaste kenmerken in te stellen in het schema van de catalogus.

1. **Beslissingsitems maken** om aan uw doelpubliek te tonen.

1. **Organiseren met verzamelingen**: De inzamelingen van het gebruik om besluitpunten te categoriseren die op op attribuut-gebaseerde regels worden gebaseerd. Neem inzamelingen in uw selectiestrategieën op om te bepalen welke inzameling van besluitvormingspunten zou moeten worden overwogen.

1. **Beslissingsregels maken**: Beslissingsregels worden gebruikt in besluitvormingspunten en/of selectiestrategieën om te bepalen aan wie een beslissingselement kan worden getoond.

1. **Classificatiemethoden implementeren**: Maak rangschikkingsmethoden en pas deze toe binnen besluitvormingsstrategieën om de prioriteitsvolgorde voor het selecteren van besluitvormingsitems te bepalen.

1. **Selectiestrategieën maken**: Bouw selectiestrategieën die hefboomwerkingen inzamelingen, besluitvormingsregels, en rangschikkende methodes om de besluitvormingspunten te identificeren geschikt voor vertoning aan profielen.

1. **Een beslissingsbeleid insluiten in uw op code gebaseerde campagne**: In het besluitvormingsbeleid worden meerdere selectiestrategieën gecombineerd om te bepalen welke in aanmerking komende beslissingsitems aan het beoogde publiek moeten worden getoond.
