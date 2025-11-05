---
product: journey optimizer
title: Math-functies
description: Meer informatie over wiskundige functies
feature: Journeys
role: Developer
level: Experienced
keywords: wiskunde, functies, uitdrukking, reis, berekening, aantal
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# Math-functies {#math-functions}

De functies van de wiskunde verstrekken essentiële wiskundige verrichtingen voor numerieke berekeningen binnen uw reis uitdrukkingen. Met deze functies kunt u nauwkeurige numerieke berekeningen en transformaties op uw gegevens uitvoeren.

Gebruik wiskundige functies wanneer u wilt:

* Produceer willekeurige waarden voor het testen, het bemonsteren, of randomisatie ([&#x200B; willekeurig &#x200B;](#random))
* Rond decimale aantallen aan het dichtstbijzijnde geheel voor schonere gegevenspresentatie ([&#x200B; rond &#x200B;](#round))
* Wiskundige berekeningen uitvoeren op numerieke velden
* Numerieke waarden transformeren voor bedrijfslogica en besluitvorming

De functies Math behandelen zowel decimale als geheeltypes, automatisch leidend typeomzettingen om nauwkeurige resultaten in uw reis uitdrukkingen te verzekeren.

## random {#random}

Genereert een willekeurig getal tussen 0 en 1.

+++Syntaxis

`random()`

+++

+++Handtekening en type geretourneerd

`random()`

Retourneert een decimaal.

+++

## round {#round}

Retourneert de dichtstbijzijnde gehele-getalwaarde voor het argument met bindingen die worden afgerond naar positief oneindig.

+++Syntaxis

`round(<parameters>)`

+++

+++Parameters

* decimaal
* integer

+++

+++Handtekeningen en type geretourneerd

`round(<decimal>)`

`round(<integer>)`

Retourneer een geheel getal.

+++

+++Voorbeelden

`round(3.14)`

Retourneert 3.

`round(3.54)`

Retourneert 4.

`round(-3.14)`

Retourneert -3.

`round(3)`

Retourneert 3.

+++

