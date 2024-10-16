---
title: Belangrijke stappen om een aanbieding te maken
description: Ontdek de belangrijkste stappen die worden vereist om een aanbieding tot stand te brengen
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 6a416ccbf658d128feb417ac2ab9ac79a0951a5a
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 3%

---

# Belangrijke stappen voor het maken en beheren van aanbiedingen {#key-steps-to-manage-offers}

De belangrijkste stappen om aanbiedingen te creëren, te vormen en te beheren, evenals hen in een besluit te gebruiken, worden hieronder voorgesteld.

![](../assets/offer-create-manage-process.png)

Voor een volledig voorbeeld dat van begin tot eind toont hoe te om aanbiedingen te vormen, gebruik hen in een besluit en hefboomwerking dit besluit in e-mail, controleer [ deze pagina ](../offers-e2e.md).

## Componenten maken {#create-components}

Voordat u aanbiedingen gaat maken, moet u verschillende componenten definiëren die u in uw aanbiedingen wilt gebruiken.

1. [ creeer plaatsingen ](creating-placements.md), die containers zijn die zullen worden gebruikt om uw aanbiedingen te tonen. U kunt bijvoorbeeld een plaatsing maken die alleen in afbeeldingsindeling aan aanbiedingen wordt toegewezen en boven aan uw berichten wordt geplaatst.

1. [ creeer besluitvormingsregels ](creating-decision-rules.md) die de voorwaarden zullen specificeren waaronder de aanbiedingen zullen worden voorgesteld.

1. [ creeer inzamelingsbepalers ](creating-tags.md) (eerder genoemd als &quot;markeringen&quot;) die u aan de aanbiedingen zult associëren, toestaand u om hen gemakkelijk te organiseren en te zoeken in de bibliotheek.

1. Als u regels wilt bepalen die zullen bepalen welke aanbieding eerst voor een bepaalde plaatsing (eerder dan het rekening houden met de prioritaire scores van aanbiedingen) zou moeten worden voorgesteld, kunt u [ tot een rangschikkende formule ](../ranking/create-ranking-formulas.md) leiden.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Aanbiedingen maken en beheren {#create-and-manage-offers}

1. [ creeer aanbiedingen ](creating-personalized-offers.md), en vorm hun inhoud en eigenschappen.

1. [ creeer fallback aanbiedingen ](creating-fallback-offers.md), die de laatste resort aanbiedingen aan vertoning zijn als de klanten niet verkiesbaar voor om het even welke geselecteerde aanbiedingen zijn.

1. [ creeer een inzameling ](creating-collections.md) om de gepersonaliseerde aanbiedingen te omvatten u creeerde en hen in een besluit gebruikt.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Besluiten maken en configureren {#create-and-configure-decisions}

1. [ creeer een besluit ](../offer-activities/create-offer-activities.md) dat plaatsingen met de gepersonaliseerde aanbiedingen en de reserveaanbiedingen zal combineren. Deze combinatie wordt door de beslissingsengine gebruikt om de beste aanbieding voor een specifiek profiel te vinden.

1. [ vorm het besluit ](../offer-activities/create-offer-activities.md#add-decision-scopes). U doet dit door de plaatsen te selecteren en voor elke plaatsing een verzameling en een fallback te selecteren.

1. Indien nodig, kunt u [ een het rangschikken formule ](../offer-activities/configure-offer-selection.md#assign-ranking-formula) of [ AI rangschikken ](../offer-activities/configure-offer-selection.md#use-ranking-strategy) aan een plaatsing toewijzen wanneer het vormen van het besluit.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->