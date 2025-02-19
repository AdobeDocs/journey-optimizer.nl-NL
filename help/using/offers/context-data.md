---
product: experience platform
solution: Experience Platform
title: Aan de slag met contextgegevens
description: Leer hoe u contextgegevens kunt gebruiken in besluitvormingsbeheer.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Aan de slag met contextgegevens {#context-data}

Gegevens die als onderdeel van het beslissingsverzoek worden verzonden, worden beschouwd als contextgegevens. U kunt contextgegevens in de beslissingsengine gebruiken, bijvoorbeeld om een beslissingsregel te ontwerpen waarvoor het huidige weer op het moment dat het beslissingsverzoek wordt ingediend, op het tijdstip waarop het wordt gedaan, op 80 graden moet zijn ingesteld.

De gegevens van de context worden bepaald verschillend tussen **Beslissing** en **Edge Beslissende** API verzoeken. Voor beide soorten verzoeken kunnen contextgegevens worden gebruikt in geschiktheidsregels of in rangschikkingsformules, maar alleen Edge-API-aanvragen voor besluitvorming kunnen contextgegevens gebruiken om inhoud aan te passen.

Controleer voordat u begint de volgende instructies en beperkingen:

* Wegens verschillende manier om context tussen Beslissende en Edge te overgaan vraag, zijn de op context-gebaseerde toelatingsregels en rangschikkingsformules niet onderling verwisselbaar tussen Beslissing en Edge Beslissende vraag.
* Het testen met de parameter `dryrun` is alleen mogelijk met de API voor besluitvorming. Deze is niet beschikbaar met de Edge-API voor besluitvorming. Het instellen van deze parameter op `true` met de API voor besluitvorming heeft geen invloed op de uiteinden en het aantal bepalingen.

Zie de volgende secties voor gedetailleerde informatie over het gebruik van contextgegevens in elke API:

* [Contextgegevens gebruiken in Edge-beslissingsverzoeken](context-data-edge.md)
* [Contextgegevens gebruiken in beslissingsverzoeken](context-data-decisioning.md)

