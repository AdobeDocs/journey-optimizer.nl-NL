---
solution: Journey Optimizer
product: journey optimizer
title: Over de wijzigingen in de tijd tot leven (TTL) en streaming segmentatie
description: Wijzigingen in tijd tot live en streaming segmentatie in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform, data Lake, create, Lake, datasets, profile
source-git-commit: 1be920fb8b3ea825e38084f459523ccde0ad979b
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---


# Wijzigingen in tijd tot live en streaming segmentatie {#ttl-guardrail}

## Tijd-aan-levende (TTL) guardrail {#ttl}

Beginnend 1 November, 2024, zal een tijd-aan-levende (TTL) guardrail aan systeem-geproduceerde datasets van Journey Optimizer in **nieuwe zandbakken en nieuwe organisaties** als volgt worden uitgerold:

* 90 dagen voor gegevens in de profielopslag
* 13 maanden voor gegevens in het data Lake

Deze verandering zal uit aan **bestaande klantenzandbakken** later in een recentere fase worden opgerold.

**vaak Gestelde Vragen**

+++ Zal deze wijziging alleen van toepassing zijn op productiesandboxen of zal deze ook van toepassing zijn op dev-sandboxen?

Deze wijziging is van toepassing op alle sandboxtypen.

+++


+++ Worden profielen zelf beïnvloed voor de 90 dagen-TTL in de profielopslag?

De door het systeem gegenereerde gegevenssetgegevens in het profiel worden na 90 dagen verwijderd, niet de profielen zelf.

+++

+++ Als een systeem-geproduceerde datasetgegevens aan Customer Journey Analytics (CJA) worden geduwd, zullen de gegevens in CJA ook door TTL worden beïnvloed?

Gegevens in CJA worden gesynchroniseerd met Experience Platform. Daarom zal een verwijdering van gegevens door een TTL op systeem-geproduceerde datasetgegevens ook de gegevens in CJA beïnvloeden.

+++

## Streaming segmentatie-updates {#segmentation-update}

Bovendien, op 1 november, zal het stromen segmentatie niet meer het gebruik van verzenden en terugkoppelen gebeurtenissen van het volgen en terugkoppelen datasets steunen.  De informatie over waarom deze praktijk in het verleden ontmoedigd is kan [ hier ](../audience/about-audiences.md#streaming-segmentation-events-guardrails) worden gevonden.


**vaak Gestelde Vragen**

+++ Zullen deze veranderingen het gebruik van kliks of andere het volgen gebeurtenissen beïnvloeden?

Deze wijziging is alleen van invloed op het gebruik van open- en verzendgebeurtenissen. Kliks en andere volggebeurtenissen kunnen nog steeds worden gebruikt in een streaming segment.

+++

+++ Zal batchsegmentatie door deze wijziging worden beïnvloed?

Deze wijziging is alleen van invloed op streamingsegmentatie. Verstuur- en open-gebeurtenissen kunnen nog steeds worden gebruikt in een batchsegment. Als ze in een streaming segment worden gebruikt, worden ze op batchwijze geëvalueerd.

+++

+++ Zal deze wijziging gevolgen hebben voor het verzamelen van trackinggegevens?

Deze wijziging heeft geen invloed op de verzameling van gegevens over het bijhouden van gegevens. Verstuur- en open gebeurtenissen blijven verzameld.

+++


+++ Heeft deze wijziging gevolgen voor de reacties?

Reactievoorvallen in de Reizen worden niet beïnvloed door deze wijziging.

+++


+++ Zal deze wijziging alleen van toepassing zijn op productiesandboxen of zal deze ook van toepassing zijn op dev-sandboxen?

Deze wijziging is van toepassing op alle sandboxtypen.

+++