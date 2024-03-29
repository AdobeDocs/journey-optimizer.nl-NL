---
title: Dataset met plaatsingen
description: Deze sectie maakt een lijst van alle gebieden die in de uitgevoerde dataset voor plaatsingen worden gebruikt
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# Dataset met plaatsingen {#placements-dataset}

Telkens als een aanbieding wordt gewijzigd, wordt de autogenerated dataset voor plaatsingen bijgewerkt.

![](../assets/dataset-placements.png)

De meest recente succesvolle partij in de dataset wordt getoond op het recht. De hiërarchische mening van het schema voor de dataset toont op de linkerruit.

>[!NOTE]
>
>Leer hoe te om tot de uitgevoerde datasets voor elk voorwerp van uw Bibliotheek van de Aanbieding in toegang te hebben [deze sectie](../export-catalog/access-dataset.md).

Hier volgt een lijst met alle velden die kunnen worden gebruikt in het dialoogvenster **[!UICONTROL Decision Object Repository - Placements]** dataset.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ Id

**Veld:** _id
**Titel:** Id
**Omschrijving:** Een unieke id voor de record.
**Type:** string

+++

+++ _experience

**Veld:** _experience
**Type:** object

+++

+++ _experience > decisions

**Veld:** beslissing
**Type:** object

+++

+++ _experience > decisions > Placement&#39;s Channel Identifier

**Veld:** channelID
**Titel:** Kanaalid van plaatsing
**Omschrijving:** Het kanaal waarin het voorstel is gedaan. De waarde is een geldige kanaal-URI. Zie https://ns.adobe.com/xdm/channels/channel.
**Type:** string

+++

+++ _experience > decisions > Content Component Type

**Veld:** componentType
**Titel:** Type inhoudcomponent
**Omschrijving:** Een opsomming van URI&#39;s waarbij elke waarde wordt toegewezen aan een type dat aan de inhoudcomponent wordt gegeven. Sommige consumenten van de inhoudrepresentaties verwachten dat de @type-waarde een verwijzing naar een schema is dat aanvullende eigenschappen van de inhoudcomponent beschrijft.
**Type:** string

+++

+++ _experience > decisions > contentTypes

**Veld:** contentTypes
**Type:** array

+++

+++_experience > decisions > contentTypes > MIME Media Type

**Titel:** MIME-mediatype
**Omschrijving:** Een beperking voor het mediatype van de componenten die in die plaatsing worden verwacht. Er kunnen meerdere mediatypen mogelijk zijn voor één component, zoals een andere afbeeldingsindeling.
**Type:** string

+++

+++ _experience > decisions > Placement Description

**Veld:** beschrijving
**Titel:** Plaatsingsbeschrijving
**Omschrijving:** Het wordt gebruikt om menselijke leesbare intenties over te brengen over hoe de dynamische inhoud in de algemene berichtlevering wordt gebruikt. Dat een bepaalde ruimte een \&quot;banner\&quot; in een webpagina is, wordt vaak weergegeven via de beschrijving en niet via een formele methode.
**Type:** string

+++

+++ _experience > decisions > Placement Name

**Veld:** name
**Titel:** Plaatsingsnaam
**Omschrijving:** Een toegewezen naam voor de plaatsing om naar het in menselijke interactie te verwijzen.
**Type:** string

+++

+++ _repo

**Veld:** _repo
**Type:** object

+++

+++ _repo > Placement ETag

**Veld:** etel
**Titel:** Plaatsing ETag
**Omschrijving:** De revisie die het object voor de beslissingsoptie had toen de momentopname werd gemaakt.
**Type:** string

+++
