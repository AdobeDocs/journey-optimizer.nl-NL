---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met Bronconnectors in Journey Optimizer
description: Leer hoe u gegevens uit externe bronnen in Adobe Journey Optimizer kunt opnemen
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 52b58d18cdbbff79f4dcb7af2817b178a4a0b429
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 3%

---

# Aan de slag met Bronconnectors {#sources-gs}

## Wat is een bron? {#what-is-source}

A **bron** is een schakelaar die externe gegevens in Adobe Journey Optimizer brengt. De bronnen staan u toe om klanteninformatie van systemen in te voeren u reeds gebruikt, zoals de platforms van CRM, wolkenopslag, of gegevensbestanden, en die gegevens ter beschikking te stellen voor het creëren van gepersonaliseerde klantenreizen.

Beschouw bronnen als bruggen tussen Journey Optimizer en uw externe gegevenssystemen. Ze synchroniseren automatisch gegevens, zodat u altijd up-to-date klantgegevens hebt om uw marketingcampagnes aan te sturen.

## Waarom bronnen belangrijk zijn {#why-sources-matter}

De bronnen zijn essentieel voor het creëren van gepersonaliseerde, data-gedreven klantenervaringen in Journey Optimizer. Dit is de reden waarom:

* **Verenigde klantenmening** - combineer gegevens van veelvoudige systemen om het volledige beeld van elke klant te zien
* **Realtime verpersoonlijking** - Gebruik verse gegevens om geschikte, relevante berichten in uw reizen te leveren
* **Geautomatiseerde gegevenssynchronisatie** - houd klanteninformatie huidig zonder handgegevensimporten
* **Efficiënte werkschema&#39;s** - verbind eens, dan gegevensstromen automatisch in uw reizen

Bijvoorbeeld, kunt u bronnen gebruiken om aankoopgeschiedenis van uw e-commerceplatform in te voeren, dan reizen tot stand te brengen die gepersonaliseerde productaanbevelingen verzenden die op wat klanten hebben gekocht.

## Wat u met bronnen kunt doen {#sources-use-cases}

Veelvoorkomende gevallen van gebruik voor bronnen in Journey Optimizer zijn:

* **de klantgegevens van de Invoer van de systemen van CRM** - de contactinformatie van de synchronisatie, voorkeur, en betrokkenheidsgeschiedenis van platforms zoals Salesforce of Microsoft Dynamics
* **verbindt aankoopgegevens** - breng in orde geschiedenis en productvoorkeur van e-commerceplatforms om aanbiedingen te personaliseren
* **integreer de gegevens van het loyaliteitsprogramma** - de puntsaldi van de toegang en rijinformatie om uw meest betrokken klanten te belonen
* **gedragsgegevens van de Synchronisatie** - de interacties van de website en de patronen van het toepassingsgebruik van de Invoer om relevante reizen teweeg te brengen
* **de profielattributen van de Update** - houd klantenprofielen huidig met gegevens van wolkenopslag of gegevensbestanden

## Algemene brontypen {#source-types}

Journey Optimizer biedt ondersteuning voor verschillende typen bronnen die verbinding kunnen maken met uw bestaande systemen:

**de toepassingen van Adobe:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**opslag van de Wolk:**
* Amazon S3
* Azure Blob Storage
* Google Cloud Storage
* SFTP

**Gegevensbestanden:**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**CRM en marketing automatisering:**
* Microsoft Dynamics
* Salesforce
* Salesforce Marketing Cloud

➡️ zie de volledige lijst in de [ Experience Platform broncatalogus ](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"}

## Voordat u begint {#prerequisites}

Voordat u bronnen configureert, moet u ervoor zorgen dat:

* **Passende toestemmingen** - Toegang om bronnen in Adobe Experience Platform te beheren
* **het systeemgeloofsbrieven van Source** - de details van de Authentificatie voor het externe systeem u wilt verbinden
* **Begrip van uw gegevens** - weet welke gegevensgebieden u nodig hebt en hoe zij aan de profielen van Journey Optimizer in kaart brengen

➡️ Leer over [ toegangsbeheer en toestemmingen ](../../administration/permissions.md)

## Hoe bronnen werken {#how-sources-work}

Adobe Journey Optimizer gebruikt het sourceframework van Adobe Experience Platform. Hier volgt de basisworkflow:

1. **verbindt** - de authentificatie van de opstelling aan uw extern gegevenssysteem
2. **Uitgezochte gegevens** - kies welke gegevens om in te voeren en hoe vaak te synchroniseren
3. **de gebieden van de Kaart** - bepalen hoe de externe gegevensgebieden aan de profielattributen van Journey Optimizer beantwoorden
4. **Programma** - de Opstelling automatische gegevens verfrist intervallen
5. **Monitor** - de gegevensstroom van het spoor en lost om het even welke synchronisatiekwesties op

Zodra gevormd, lopen de bronnen automatisch op de achtergrond, die uw klantengegevens vers houden en klaar voor gebruik in reizen houden.

## Meer informatie {#learn-more}

![](assets/sources-home.png)

Bekijk deze video om bronschakelaars te begrijpen en hoe te om hen in Journey Optimizer te vormen:

>[!VIDEO](https://video.tv.adobe.com/v/335919?quality=12)

Voor gedetailleerde informatie over het vormen en het leiden van bronnen, verwijs naar de [ de brondocumentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=nl){target="_blank"}.

## Volgende stappen {#next-steps}

Nu je begrijpt welke bronnen er zijn en waarom ze belangrijk zijn:

* Onderzoek de [ broncatalogus ](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"} om schakelaars voor uw systemen te vinden
* Leer hoe te [ een bronverbinding ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html){target="_blank"} tot stand brengen
* Begrijp [ gegevenstoewijzing en transformatie ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html){target="_blank"}
* Zie hoe te [ gebruik ingevoerde gegevens in reizen ](../building-journeys/journey-gs.md)
