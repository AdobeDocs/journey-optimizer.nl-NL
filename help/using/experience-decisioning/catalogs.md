---
title: Itemcatalogus
description: Leer hoe u met de itemcatalogus werkt
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 2b9261ff0f225a429b9be04db214452736163766
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Itemcatalogus {#catalog}

>[!BEGINSHADEBOX &quot;Wat u vindt in deze documentatiehandleiding&quot;]

* [Aan de slag met Experience Decisition](gs-experience-decisioning.md)
* Je beslissingsobjecten beheren: **[De itemcatalogus configureren](catalogs.md)** - [Beslissingsitems maken](items.md) - [Objectverzamelingen beheren](collections.md)
* Selectie van items configureren: [Beslissingsregels maken](rules.md) - [Classificatiemethoden maken](ranking.md)
* [Selectiestrategieën maken](selection-strategies.md)
* [Beslissingsbeleid maken](create-decision.md)

>[!ENDSHADEBOX]

In het Besluit van de Ervaring, dienen de catalogi als centrale containers voor het organiseren van beslissingspunten. Elke catalogus is gekoppeld aan een Adobe Experience Platform-schema, dat alle kenmerken omvat die aan een beslissingsitem kunnen worden toegewezen.

Vooralsnog worden alle gemaakte beslissingsitems geconsolideerd in één &quot;Aanbiedingscatalogus&quot;, die toegankelijk is via de **[!UICONTROL  Catalogs]** -menu.

![](assets/catalogs-list.png)

Ga als volgt te werk om het schema van de catalogus te openen waarin de kenmerken van de beslissingsitems zijn opgeslagen:

1. Klik in de lijst met items op de knop **[!UICONTROL Edit schema]** naast de knop **[!UICONTROL Create item]** knop.

1. Het schema van de catalogus wordt op een nieuw tabblad geopend, volgens de onderstaande structuur:

   * De **`_experience`** de knoop omvat standaardbeslissingspunten attributen zoals naam, begin en einddatum, en beschrijving.
   * De **`_<imsOrg>`** knooppunt bevat kenmerken voor aangepaste beslissingsitems. Standaard zijn er geen aangepaste kenmerken geconfigureerd, maar u kunt er zo veel toevoegen als nodig is om aan uw vereisten te voldoen. Zodra gedaan, verschijnen de douanekenmerken in het scherm van de verwezenlijking van het besluitpunt naast de standaardattributen.

   ![](assets/catalogs-schema.png)

1. Als u een aangepast kenmerk aan het schema wilt toevoegen, vouwt u het veld **`_<imsOrg>`** en klik op de knop &quot;+&quot; op de gewenste locatie in de structuur.

   ![](assets/catalogs-add.png)

1. Vul de vereiste velden voor het toegevoegde kenmerk in en klik op **[!UICONTROL Apply]**.

   >[!CAUTION]
   >
   >Tot nu toe worden bij Ervaring beslissen alleen de hieronder vermelde gegevenstypen ondersteund. Om het even welk gebied dat buiten deze gegevenstypes valt zal niet beschikbaar voor gebruik zijn wanneer het creëren van een besluitpunt.
   >* String
   >* Boolean
   >* Getal

   Gedetailleerde informatie over het werken met Adobe Experience Platform-schema&#39;s is beschikbaar in het dialoogvenster [XDM System-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html).

1. Sla het schema op wanneer u de gewenste aangepaste kenmerken hebt toegevoegd. Het nieuwe veld is nu beschikbaar in het scherm voor het maken van itembeslissingen, in het dialoogvenster **[!UICONTROL Custom attributes]** sectie.
