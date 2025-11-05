---
product: journey optimizer
title: inAudience, functie
description: Meer informatie over de functie Adobe Experience Platform inAudience
feature: Journeys
role: Developer
level: Experienced
keywords: inPubliek, functie, expressie, reis, publiek, segmentatie
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: a866442aa073c648d4455754e9945f0dddfb079d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# inAudience, functie {#inAudience}

De functie `inAudience` is een Adobe Experience Platform-functie waarmee u kunt controleren of een individu op reis tot een bepaald publiek behoort. Deze krachtige functie staat u toe om gepersonaliseerde reiswegen tot stand te brengen die op publiekslidmaatschap worden gebaseerd, toelatend verfijnde segmentatie en het richten binnen uw klantenervaringen.

Gebruik de functie `inAudience` wanneer dat nodig is:

* [Vertakkingstrajecten gebaseerd op het lidmaatschap van het publiek](../condition-activity.md#using-a-segment)
* Voorwaardelijke logica toepassen die afhankelijk is van het feit of een profiel tot een bepaald segment behoort
* Doelspecifieke groepen klanten met persoonlijke ervaringen
* Evalueer de participatie van het publiek in real time binnen reisvoorwaarden
* Combineer veelvoudige publiekscontroles om complexe het richten regels tot stand te brengen

De functie evalueert publiekslidmaatschap in real time en keert een booleaanse waarde terug, die het voor beslissingsknopen en voorwaardelijke uitdrukkingen ideaal maakt. Het publiek wordt bepaald en geleid in [ Adobe Experience Platform ](https://platform.adobe.com/audience/overview){target="_blank"} (leer meer over [ het werken met publiek ](../../audience/about-audiences.md) in Journey Optimizer), en de uitdrukkingsredacteur verstrekt autocomplete suggesties om u te helpen hen nauwkeurig van verwijzingen voorzien.

**Status van het publiek:**

Het publiek kan twee deelnemingsstatussen hebben:

* **Realized**: Het individu kwalificeert voor de publieksdefinitie en is een actief lid
* **Uitgegeven**: Het individu heeft het publiek verlaten en kwalificeert niet meer

Slechts zullen de individuen met de **Geleide** status als actieve publieksleden worden beschouwd. Wanneer de functie `true` retourneert, wordt bevestigd dat de persoon de status heeft gerealiseerd; wanneer `false` wordt geretourneerd, geeft dit de status verlaten. Voor meer informatie over publieksevaluatie, verwijs naar de [ documentatie van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

+++Syntaxis

`inAudience(<parameter>)`

+++

+++Parameters

| Parameter | Beschrijving | Type |
|--- |--- |--- |
| Doelgroep | De publieksnaam | `<string>` |

**Belangrijke beperkingen:**

* De publieksnaam moet een tekenreeksconstante zijn
* Het mag geen veldverwijzing of expressie zijn
* U kunt tot 100 publiek in één enkele reis terugwinnen

+++

+++Handtekening en type geretourneerd

`inAudience(<string>)`

Retourneert een Booleaanse waarde:
* `true`: Het individu is lid van het publiek (gerealiseerde status)

* `false`: De persoon is geen lid van het publiek (verlaten status)

+++

+++Voorbeelden

`inAudience("men over 50")`

Keert **waar** terug als het individu binnen de reisinstantie deel van het publiek van Adobe Experience Platform genoemd &quot;mannen over 50&quot;uitmaakt, **vals** anders.

**Praktische gebruiksgevallen:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Afvoerkanalen en beperkingen {#guardrails}

Wanneer u de functie `inAudience` gebruikt tijdens reizen, dient u rekening te houden met de volgende instructies en beperkingen:

**de herwinningsgrens van het publiek:**
* U kunt tot 100 publiek binnen één enkele reis terugwinnen
* De uitdrukkingsredacteur verstrekt een autocompleted lijst van beschikbare publiek om u te helpen hen correct van verwijzingen voorzien

**beperkingen van de Parameter:**
* De publieksnaam moet een tekenreeksconstante zijn
* Veldverwijzingen en -expressies worden niet ondersteund als parameters

**de naamveranderingen van het publiek:**
* Als u de naam van een bestaand publiek in Adobe Experience Platform wijzigt, worden niet automatisch verwijzingen naar dat publiek in uw reisexpressies bijgewerkt
* Als uw voorwaardenknooppunt `inAudience('oldAudienceName')` gebruikt, moet u de expressie handmatig bewerken om de nieuwe naam te gebruiken
* Als de publieksnaam niet wordt bijgewerkt, wordt de reisconditie verbroken en kan het reisgedrag onjuist zijn

**het beleidsoverwegingen van de Fusie:**
* Wanneer u meerdere soorten publiek gebruikt met de functie `inAudience` , kunnen inconsistenties met het samenvoegbeleid fouten of waarschuwingen veroorzaken
* Verwijs naar [ eigenschappen van de Reis ](../journey-properties.md) voor meer informatie over het gedrag van het fusiebeleid

## Verwante onderwerpen

Meer weten over het gebruik van soorten publiek in Adobe Journey Optimizer?

* **[Ongeveer publiek](../../audience/about-audiences.md)** - begrijp hoe het publiek in Adobe Experience Platform en Journey Optimizer werkt, met inbegrip van hoe te om hen tot stand te brengen en te leiden
* **[las de activiteit van het Publiek](../read-audience.md)** - Gebruik publiek om reisingang teweeg te brengen en alle publieksleden te maken een reis ingaan
* **[de gebeurtenissen van de Kwalificatie van het publiek](../audience-qualification-events.md)** - luister aan profielingangen en uitgang van publiek om reisacties in real time teweeg te brengen
* **[Gebruikend publiek in voorwaarden](../condition-activity.md#using-a-segment)** - creeer voorwaardelijke die reiswegen op publiekslidmaatschap worden gebaseerd gebruikend de activiteit van de Voorwaarde
* **[eigenschappen van de Reis - het beleid van de Fusie](../journey-properties.md)** - begrijp hoe het beleid van de fusie werkt wanneer het gebruiken van veelvoudige publiek met de functie inAudience

