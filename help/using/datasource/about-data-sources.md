---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevensbronnen
description: Leer hoe u aan de slag kunt met gegevensbronnen
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: gegevens, bron, reis, platform
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 8521e59022c221c0ca4e5b69b5b3aefe6304b417
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 32%

---

# Aan de slag met gegevensbronnen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informatie over databronnen"
>abstract="De databronconfiguratie wordt altijd uitgevoerd door een technische gebruiker. Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor parameter- en personalisatiedata in acties en het definiëren van voorwaarden, tijdzones en aangepaste wachttijden."

>[!TIP]
>Nieuw bij gegevensbeheer in Journey Optimizer? Begin met [ worden begonnen met gegevensbeheer ](../data/gs-data.md) overzicht om schema&#39;s, datasets, identiteiten te begrijpen, en hoe de gegevensstromen alvorens gegevensbronnen te vormen.

Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor:

* [conditiedefinitie](../building-journeys/conditions.md)
* parameter- en personalisatiedata in [acties](../action/action.md)
* [aangepaste wachtdefinitie](../building-journeys/wait-activity.md#custom)
* [tijdzonedefinitie](../building-journeys/timezone-management.md)

➡️ [Ontdek deze functie in video](#video)

Deze configuratie is niet vereist als uw journey’s alleen lokale data uit een gebeurtenispayload gebruiken. Bijvoorbeeld, als uw reis uit een gebeurtenis bestaat die door een activiteit van de kanaalactie wordt gevolgd die slechts gegevens van de gebeurtenis gebruikt, is er geen behoefte om een gegevensbron te vormen.

Er zijn twee soorten databronnen:

* De **pre-gevormde** gegevensbron van Adobe Experience Platform die de verbinding aan de Dienst van het Profiel van de Klant in real time bepaalt. Dit is een ingebouwde databron. Zie [deze pagina](../datasource/adobe-experience-platform-data-source.md).
* De **externe** gegevensbronnen die u toestaan om een verbinding aan externe systemen te bepalen. Dit zijn databronnen die u kunt maken. Zie [deze pagina](../datasource/external-data-sources.md).

>[!NOTE]
>
>Aangezien de reacties nu worden gesteund, zou u douaneacties in plaats van gegevensbronnen voor externe gegevensbronnen moeten gebruiken-gevallen. Voor meer informatie over reacties, zie deze [ sectie ](../action/action-response.md)

Voor elke databron definieert u de informatie die u wilt ophalen met behulp van veldengroepen. Veldengroepen zijn reeksen velden die uit een databron kunnen worden opgehaald. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Schemarelaties worden niet ondersteund voor gegevensbronnen.

## Kies uw strategie voor gegevenstoegang {#data-access-strategy}

Alvorens een gegevensbron te vormen, overweeg welke benadering beste uw gebruiksgeval past. Er zijn drie opties beschikbaar, elk met verschillende compromissen wat betreft persistentie, profielverrijking en herbruikbaarheid. Voor een gedetailleerde bespreking van deze opties, zie [ Beste praktijken voor geavanceerde reizen in Journey Optimizer ](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Optie 1 — Toegang externe gegevens via de Acties van de Douane (geen het Leer van Gegevens)**

Sluit tijdens de reis rechtstreeks een externe API aan zonder permanente gegevens in het Experience Platform Data Lake. Meest geschikt wanneer:

* De gegevens zijn alleen nuttig binnen de reiscontext en niet elders nodig.
* Het externe systeem is toegankelijk door een API eindpunt dat de vereiste attributen terugkeert.

Leer meer over [ douaneacties ](../action/action.md) en [ reacties van de douaneactie ](../action/action-response.md).

**Optie 2 — Dataset in het Leer van Gegevens, niet toegelaten voor Profiel**

Gegevens in een gegevensset opnemen om reizen te activeren en te personaliseren op basis van contextuele gebeurtenisgegevens, zonder bij te dragen aan het realtime-klantprofiel. Meest geschikt wanneer:

* Records bevatten een identiteitsveld dat kan worden gebruikt voor toegangsprofielen die al in Experience Platform zijn opgeslagen.
* De gegevens zijn niet nodig voor het maken van publiek of het stikken van identiteiten buiten Journey Optimizer.

**Optie 3 — Profiel-Toegelaten dataset in het meer van Gegevens**

De samenvattingsgegevens in a [ profiel-toegelaten dataset ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} om publiek tot stand te brengen, verrijken identiteitsgrafieken, en hefboomwerkingsgegevens over veelvoudige reizen en rt-CDP bestemmingen. Meest geschikt wanneer:

* De gegevens zijn handig voor publieksdefinities die worden gebruikt in kanalen buiten Journey Optimizer.
* De gegevens bevatten meerdere identiteiten die bijdragen tot rijkere, gestikte profielfragmenten.

| | Gegevens in Data Lake | Gegevensset ingeschakeld voor profiel |
| --- | --- | --- |
| **Optie 1** — Externe gegevens via de Acties van de Douane | Nee | Nee |
| **Optie 2** — Dataset niet toegelaten voor Profiel | Ja | Nee |
| **Optie 3** — Profiel-Toegelaten dataset | Ja | Ja |

Voor meer informatie over het configureren van een Adobe Experience Platform-databron en een externe databron en hoe u gegevens in een journey kunt vinden en gebruiken, bekijkt u deze [zelfstudievideo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Hoe kan ik-video {#video}

Begrijp wat een databron is en leer hoe u Experience Platform en externe databronnen kunt configureren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

