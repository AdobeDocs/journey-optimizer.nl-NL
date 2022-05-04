---
title: API's voor besluitvorming en Edge-besluitvorming
description: Het Beheer van het besluit is een inzameling van de diensten en programma's UI die marketers toelaat om de gepersonaliseerde aanbiedingservaringen van de eindgebruiker over kanalen en toepassingen tot stand te brengen en te leveren gebruikend bedrijfslogica en besluitvormingsregels.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: dc56f2dc461a11c9706b3572ccd4b9e0feb6f055
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# API&#39;s voor besluitvorming en Edge-besluitvorming {#about-decisioning-apis}

U kunt voorstellen leveren gebruikend of **Beslissing** of de **Randbeslissing** API.

Op deze pagina vindt u informatie over specifieke functies die beschikbaar zijn voor elke API. Terwijl beide u toestaan om aanbiedingen aan uw klanten te leveren, adviseren wij gebruikend **Randbeslissing** API waar mogelijk voor binnenkomende gebruiksgevallen en voor betere latentie en doorvoer op uw platform.

|  | Verzoeken/sec | Latentie |
|---|---|---|
| API voor besluitvorming | 2000 | &lt;500 ms |
| Edge-API voor besluitvorming | 5000 | &lt;250 ms |

Raadpleeg de volgende secties voor meer informatie over het werken met de API&#39;s:
* [API voor besluitvorming](decisioning-api.md)
* [Edge-API voor besluitvorming](edge-decisioning-api.md)

## Edge-API-mogelijkheden voor besluitvorming {#edge}

**Unieke aanvraag voor ervaringsgebeurtenissen en beslissingsverzoeken**

Met de Edge Decisioning-API kunt u in één aanvraag de ervaringsgebeurtenis zelf verzenden samen met de beslissingsaanvraag, in plaats van twee verschillende aanvragen te hebben.

Als een klant bijvoorbeeld uw website bezoekt, bevat de aanvraag de ervaringsgebeurtenis (het bezoek van de klant aan de pagina) en wordt een aanbieding teruggestuurd om de bezochte pagina te vullen.

**Opslag van contextgegevens in Adobe Experience Platform**

Contextgegevens verwijzen naar gegevens die u alleen kent op het moment dat u een aanbieding wilt terugsturen. Bijvoorbeeld de kleur van het aangekochte artikel, het weer op het moment van de aankoop, enz.

Wanneer contextgegevens worden doorgegeven met een Edge-API-aanvraag voor besluitvorming, worden gegevens opgeslagen in het Adobe Experience Platform-profiel, zodat ze later opnieuw kunnen worden gebruikt.

>[!NOTE]
>
>Opdat de contextgegevens worden opgeslagen, moet u een specifiek geconfigureerd XDM-schema hebben.

## API-mogelijkheden voor besluitvorming {#decisioning}

De hieronder vermelde functies zijn alleen beschikbaar met de API voor besluitvorming. Gebruik de API voor besluitvorming als u een van deze toepassingen wilt gebruiken om aan uw vereisten te voldoen. Anders raden we u aan de Edge-API&#39;s voor besluitvorming te gebruiken.

* **Gebeurtenissen van Experience**: hefboomwerkingservaringsgebeurtenissen om uw beslissingsregels te bouwen.
* **Inhoud en kenmerken van aanbiedingen**: u kunt ervoor kiezen om de inhoud en kenmerken van een aanbieding niet te retourneren met een speciale optie.
* **Metagegevens aanbieden**: een optie inschakelen om de metagegevens van een aanbieding te retourneren.
* **Samenvoegbeleid**: in uw aanvraag een ander samenvoegbeleid gebruiken dan het beleid dat aan uw sandbox is gekoppeld.
* **Decisitiegebeurtenissen en frequentiecapping**: blokbeslissingsgebeurtenissen worden niet geteld door een willekeurige frequentiecapping die plaatsvindt.
* **Proposities dupliceren**: Schakel een optie in om voorstellingen niet te dedupliceren.
