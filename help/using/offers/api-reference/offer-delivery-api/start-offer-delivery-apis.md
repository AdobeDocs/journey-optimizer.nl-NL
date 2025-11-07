---
title: Aan de slag met API's voor levering van aanbiedingen
description: Meer informatie over de beschikbare API's voor het aanbieden van persoonlijke aanbiedingen.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Aan de slag met API&#39;s voor levering van aanbiedingen {#about-decisioning-apis}

U kunt aanbiedingen leveren gebruikend of **Beslissing** of **Edge Beslissing** API. Bovendien, staat de **Beslissing van de Partij** API u toe om aanbiedingen aan alle profielen in een bepaald publiek in één vraag te leveren. De aanbiedingsinhoud voor elke profielen in het publiek wordt geplaatst in een dataset van Adobe Experience Platform waar het voor de werkschema&#39;s van de douanepartij beschikbaar is.

In deze pagina, zult u informatie over specifieke functionaliteit vinden die met **Beslissing** en **Edge Decisioning** APIs beschikbaar is. Terwijl beide u toestaan om aanbiedingen aan uw klanten te leveren, adviseren wij het gebruiken van **Edge Decisioning** API wanneer mogelijk voor binnenkomende gebruiksgevallen en om betere latentie en productie op uw platform te verzekeren.

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:

* [API voor besluitvorming](decisioning-api.md)
* [Edge-API voor besluitvorming](edge-decisioning-api.md)
* [Batchbeslissing-API](batch-decisioning-api.md)

## Edge-API-mogelijkheden voor besluitvorming {#edge}

**Unieke verzoek om ervaringsgebeurtenissen en beslissingsverzoeken**

Met de Edge-API voor besluitvorming kunt u in één aanvraag de ervaringsgebeurtenis zelf en de beslissingsaanvraag verzenden in plaats van twee verschillende aanvragen te hebben.

Als een klant bijvoorbeeld uw website bezoekt, bevat de aanvraag de ervaringsgebeurtenis (het bezoek van de klant aan de pagina) en wordt een aanbieding teruggestuurd om de bezochte pagina te vullen.

**de gegevensopslag van de context in Adobe Experience Platform**

Contextgegevens verwijzen naar gegevens die u alleen kent op het moment dat u een aanbieding wilt terugsturen. Bijvoorbeeld de kleur van het aangekochte artikel, het weer op het moment van de aankoop, enz.

Wanneer contextgegevens worden doorgegeven met een Edge-API-aanvraag voor besluitvorming, worden gegevens opgeslagen in het Adobe Experience Platform-profiel, zodat ze later opnieuw kunnen worden gebruikt.

>[!NOTE]
>
>Opdat de contextgegevens worden opgeslagen, moet u een specifiek geconfigureerd XDM-schema hebben.

**de Teller update van de het afschilderen van de Frequentie**

Als voor sommige van uw aanbiedingen de functie voor het toewijzen van frequenties is ingeschakeld om te bepalen hoe vaak het aantal bijschriften wordt teruggezet, wordt de teller binnen 3 seconden bijgewerkt en beschikbaar in een Edge-beslissing voor de API voor besluitvorming. [ Leer hoe te om beperkingen aan een aanbieding toe te voegen ](../../offer-library/add-constraints.md)

## API-mogelijkheden voor besluitvorming {#decisioning}

De hieronder vermelde functies zijn alleen beschikbaar met de API voor besluitvorming. Gebruik de API voor besluitvorming als u een van deze toepassingen wilt gebruiken om aan uw vereisten te voldoen. Anders raden we u aan de Edge-API&#39;s voor besluitvorming te gebruiken.

* **inhoud en kenmerken van de Aanbieding**: u kunt verkiezen om de inhoud en de kenmerken van een aanbieding niet terug te keren gebruikend een specifieke optie.
* **meta-gegevens van de Aanbieding**: laat een optie toe om de meta-gegevens van een aanbieding terug te keren.
* **beleid van de Fusie**: gebruik in uw verzoek een verschillend samenvoegbeleid van verbonden aan uw zandbak.
* **het Beslissen gebeurtenissen en frequentie het in kaart brengen**: de gebeurtenissen van de blokbeslissing van worden geteld door om het even welke frequentie het in kaart brengen die gebeurt.
* **dupliceer voorstellingen**: laat een optie toe om geen voorstellingen te dedupliceren.
