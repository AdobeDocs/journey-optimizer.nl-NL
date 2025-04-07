---
solution: Journey Optimizer
product: journey optimizer
title: Over ExperienceEvent-schema's voor reisgebeurtenissen
description: Meer informatie over ExperienceEvent-schema's voor reisgebeurtenissen
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: schema's, XDM, platform, streaming, opname, reis
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---

# Over ExperienceEvent-schema&#39;s voor [!DNL Journey Optimizer] -gebeurtenissen {#about-experienceevent-schemas}

[!DNL Journey Optimizer] -gebeurtenissen zijn XDM Experience Events die via Streaming Ingestie naar Adobe Experience Platform worden verzonden.

Daarom is een belangrijke voorwaarde voor het instellen van gebeurtenissen voor [!DNL Journey Optimizer] dat u bekend bent met het Adobe Experience Platform Experience Data Model (of XDM) en hoe u XDM Experience Event-schema&#39;s kunt samenstellen en hoe u XDM-gegevens kunt streamen naar Adobe Experience Platform.

## Schemavereisten voor [!DNL Journey Optimizer] gebeurtenissen  {#schema-requirements}

De eerste stap bij het instellen van een gebeurtenis voor [!DNL Journey Optimizer] is ervoor te zorgen dat u een XDM-schema hebt gedefinieerd om de gebeurtenis te vertegenwoordigen, en een dataset die is gemaakt om instanties van de gebeurtenis op Adobe Experience Platform op te nemen. Het hebben van een dataset voor uw gebeurtenissen is niet strikt noodzakelijk, maar het verzenden van de gebeurtenissen naar een specifieke dataset zal u toestaan om de de gebeurtenisgeschiedenis van gebruikers voor toekomstige verwijzing en analyse te handhaven, zodat is het altijd een goed idee. Als u nog geen geschikt schema en een geschikte dataset voor uw gebeurtenis hebt, kunnen beide taken in de Webinterface van Adobe Experience Platform worden gedaan.

![](assets/schema1.png)

Elk XDM-schema dat voor [!DNL Journey Optimizer] -gebeurtenissen wordt gebruikt, moet aan de volgende vereisten voldoen:

* Het schema moet van de klasse XDM ExperienceEvent zijn.

  ![](assets/schema2.png)

* Voor systeem-geproduceerde gebeurtenissen, moet het schema de Orchestration eventID gebiedsgroep omvatten. [!DNL Journey Optimizer] gebruikt dit veld om gebeurtenissen te identificeren die tijdens reizen worden gebruikt.

  ![](assets/schema3.png)

* Declareer een identiteitsveld voor het identificeren van afzonderlijke profielen in de gebeurtenis. Als er geen identiteit is opgegeven, kan een identiteitskaart worden gebruikt. Dit wordt niet aanbevolen.

  ![](assets/schema4.png)

* Als u deze gegevens voor raadpleging later in een Reis beschikbaar zou willen zijn, merk het schema en de dataset voor profiel.

  ![](assets/schema5.png)

  ![](assets/schema6.png)

* U kunt gegevensvelden vrij gebruiken om andere contextgegevens vast te leggen die u met de gebeurtenis wilt opnemen, zoals informatie over de gebruiker, het apparaat waaruit de gebeurtenis is gegenereerd, de locatie of andere betekenisvolle omstandigheden die met de gebeurtenis verband houden.

  ![](assets/schema7.png)

  ![](assets/schema8.png)

## Schema-relaties benutten{#leverage_schema_relationships}

Adobe Experience Platform staat u toe om verhoudingen tussen schema&#39;s te bepalen om één dataset als raadplegingslijst voor een andere te gebruiken.

Laten we zeggen dat uw model met merkgegevens een schema heeft voor het vastleggen van aankopen. U hebt ook een schema voor de productcatalogus. U kunt de product-id vastleggen in het aankoopschema en een relatie gebruiken om de volledige productdetails uit de productcatalogus op te zoeken. Hierdoor kunt u een publiek maken voor alle klanten die bijvoorbeeld een laptop hebben gekocht, zonder dat u expliciet alle laptop-id&#39;s hoeft op te geven of alle productdetails in transactiesystemen hoeft vast te leggen.

Als u een relatie wilt definiëren, moet u een speciaal veld in het bronschema hebben, in dit geval het veld product-id in het aankoopschema. Dit gebied moet het gebied van productID in het bestemmingsschema van verwijzingen voorzien. De bron en bestemmingstabellen moeten voor profielen worden toegelaten en het bestemmingsschema moet dat gemeenschappelijke gebied hebben dat als zijn primaire identiteit wordt bepaald.

Hier volgt het productcatalogusschema dat is ingeschakeld voor profiel met de product-id die is gedefinieerd als de primaire identiteit.

![](assets/schema9.png)

Hier volgt het aankoopschema met de relatie die is gedefinieerd in het veld product-id.

![](assets/schema10.png)

>[!NOTE]
>
>Leer meer over schemaverhoudingen in de [ documentatie van Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html).

In Journey Optimizer kunt u vervolgens alle velden uit de gekoppelde tabellen benutten:

* wanneer het vormen van een zaken of eenheidsgebeurtenis, [ las meer ](../event/experience-event-schema.md#unitary_event_configuration)
* wanneer het gebruiken van voorwaarden in een reis, [ las meer ](../event/experience-event-schema.md#journey_conditions_using_event_context)
* in berichtverpersoonlijking, [ las meer ](../event/experience-event-schema.md#message_personalization)
* in de verpersoonlijking van de douaneactie, [ las meer ](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### Arrays{#relationships_limitations}

U kunt een schemaverhouding op een serie van koorden, bijvoorbeeld, een lijst van product IDs bepalen.

![](assets/schema15.png)

U kunt ook een schema-relatie definiëren met een kenmerk binnen een array van objecten, bijvoorbeeld een lijst met aankoopgegevens (product-id, productnaam, prijs, korting). De opgezochte waarden zullen in reizen (voorwaarden, douaneacties, enz.) en berichtverpersoonlijking beschikbaar zijn.

![](assets/schema16.png)

### Gebeurtenisconfiguratie{#unitary_event_configuration}

De gekoppelde schemavelden zijn beschikbaar in de configuratie van een eenheidsgebeurtenis en bedrijfsgebeurtenis:

* wanneer het doorbladeren door de gebieden van het gebeurtenisschema in het scherm van de gebeurtenisconfiguratie.
* wanneer het bepalen van een voorwaarde voor systeem-geproduceerde gebeurtenissen.

![](assets/schema11.png)

De gekoppelde velden zijn niet beschikbaar:

* in de sleutelformule voor gebeurtenissen
* in event id condition (op regel gebaseerde gebeurtenissen)

Leren hoe te om een eenheidsgebeurtenis te vormen, verwijs naar deze [ pagina ](../event/about-creating.md).

### Reisomstandigheden met gebeurteniscontext{#journey_conditions_using_event_context}

U kunt gegevens van een raadplegingslijst gebruiken verbonden met een gebeurtenis die in een reis voor voorwaardenbouw (uitdrukkingsredacteur) wordt gebruikt.

Voeg een voorwaarde toe in een reis, geef de uitdrukking uit en ontvouw de gebeurtenisknoop in de uitdrukkingsredacteur.

![](assets/schema12.png)

Leren hoe te om reisvoorwaarden te bepalen, verwijs naar deze [ pagina ](../building-journeys/condition-activity.md).

### Berichtenpersonalisatie{#message_personalization}

De gekoppelde velden zijn beschikbaar wanneer u een bericht personaliseert. De verwante gebieden worden getoond in de context die van de reis tot het bericht wordt overgegaan.

![](assets/schema14.png)

Leren hoe te om een bericht met contextuele reisinformatie te personaliseren, verwijs naar deze [ pagina ](../personalization/personalization-use-case.md).

### Aangepaste actie-personalisatie met context van reisgebeurtenis{#custom_action_personalization_with_journey_event_context}

De verbonden gebieden zijn beschikbaar wanneer het vormen van de actieparameters van een actie van de reisdouane.

![](assets/schema13.png)

Leren hoe te om douaneacties te gebruiken, verwijs naar deze [ pagina ](../building-journeys/using-custom-actions.md).
