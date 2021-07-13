---
title: Machtigingsniveaus
description: Meer informatie over machtigingen op hoog en laag niveau
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Controlegroepen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Elk productprofiel bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.
Zij kunnen in twee types worden verdeeld:

* **Toestemming** op hoog niveau: vertegenwoordigt de verschillende toestemmingen die aan  **[!UICONTROL Product profile]** in  [!DNL Admin console], zoals  **[!UICONTROL Publish journeys]** en kunnen worden toegewezen  **[!UICONTROL Manage subdomains delegation]**. Machtigingen op hoog niveau omvatten machtigingen op laag niveau.

* **Toestemming** op laag niveau: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

Het productprofiel **[!UICONTROL Journey administrator]** wordt bijvoorbeeld toegewezen aan de machtiging **[!UICONTROL Manage journeys]**. Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

## Reiscapaciteit {#journey-capability}

### Toestemming voor reizen beheren {#manage-journeys}

Met de machtiging op hoog niveau **[!UICONTROL Manage journeys]** kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken/verwijderen, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow op te bouwen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* specifiek voor Adobe Experience Platform:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### Licentie voor reizen publiceren {#publish-journeys}

Met de machtiging op hoog niveau **[!UICONTROL Publish journeys]** kunnen gebruikers reizen publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.publish
   * journeys.read

### Toestemming voor reizen weergeven {#view-journeys}

Met de machtiging op hoog niveau **[!UICONTROL View journeys]** kunnen gebruikers door reizen bladeren en deze weergeven.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.read

* specifiek voor Adobe Experience Platform:
   * segments.read
   * profiles.read

### Reisgebeurtenissen, gegevensbronnen en handelingen beheren {#manage-journeys-events}

Met de machtiging op hoog niveau **[!UICONTROL Manage journeys events, data sources and actions]** kunnen gebruikers gebeurtenis- en gegevensconfiguraties configureren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * rites_events.read
   * trip_events.write
   * reizen_gebeurtenissen.delete
   * reizen_gegevens_bronnen.read
   * reizen_gegevens_bronnen.write
   * reizen_gegevens_bronnen.delete
   * reizen_handelingen.read
   * trajecten_handelingen.write
   * reizen_handelingen.delete
* specifiek voor Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Reisgebeurtenissen, gegevensbronnen en actietoestemming weergeven {#view-journeys-event}

Met de machtiging op hoog niveau **[!UICONTROL View journeys events, data sources and actions]** kunnen gebruikers gebeurtenissen en gegevens gebruiken in de reisflow.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * rites_events.read
   * reizen_gegevens_bronnen.read
   * reizen_handelingen.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Toestemming voor reisrapporten weergeven {#view-journeys-report}

Met de machtiging op hoog niveau **[!UICONTROL View journeys report]** kunnen gebruikers alleen-lezenreisrapporten maken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * trajecten_rapport.read
   * messages_report.read

* specifiek voor Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Berichtmogelijkheden {#message-capability}

### Machtiging voor berichten beheren {#manage-messages}

Met de machtiging op hoog niveau **[!UICONTROL Manage messages]** kunnen gebruikers een bericht maken en bewerken/verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* specifiek voor Adobe Experience Platform:
   * segments.read
   * schemas.read

### Voorvertoning van berichten beheren en machtigingen testen {#mange-messages-preview}

Met de machtiging op hoog niveau **[!UICONTROL Manage messages preview and test]** kunnen gebruikers een voorvertoning van gepersonaliseerde berichten weergeven.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### Machtiging voor berichten publiceren {#publish-messages}

Met de machtiging op hoog niveau **[!UICONTROL Publish messages]** kunnen gebruikers berichten publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.publish

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Toestemming voor berichten weergeven {#view-messages}

Met de machtiging op hoog niveau **[!UICONTROL View messages]** kunnen gebruikers alleen berichten lezen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.read
   * messages_presets.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * segments.read

### Toestemming berichtrapport weergeven {#view-message-reports}

Met de machtiging op hoog niveau **[!UICONTROL View messages report]** kunnen gebruikers alleen-lezen e-mail- en pushrapporten verzenden.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Beslissingsvermogen {#decisions-permissions}

### Machtiging voor beslissingen beheren {#manage-decisioning}

Met de **[!UICONTROL Manage decisions]**-machtiging op hoog niveau kunnen gebruikers nieuwe **[!UICONTROL Activity entities]** maken en bestaande  bewerken/verwijderen en de objecten beheren die in die activiteiten worden gebruikt om de beslissingen te nemen.

Dit omvat de volgende laagniveaumachtigingen:

* Specifieke aspecten van het besluitvormingsbeheer:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * classificeren_strategie.read

* specifiek voor Adobe Experience Platform:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### Toestemming voor beslissingen weergeven {#view-decisions}

De **[!UICONTROL View decisions]** toestemming op hoog niveau staat gebruikers toe om een bestaande Activiteit en verwante bedrijfsvoorwerpen te gebruiken om de besluiten te nemen.

Dit omvat de volgende laagniveaumachtigingen:

* Specifieke aspecten van het besluitvormingsbeheer:
   * activities.read
   * offers.read
   * placements.read
   * classificeren_strategie.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Publiceren biedt beslissingsbevoegdheid {#publish-decisions}

De **[!UICONTROL Publish offers decisioning]** toestemming op hoog niveau staat gebruikers toe om tot goed te keuren/unapproval de activiteiten van de Aanbieding goed te keuren.

Dit omvat de volgende laagniveaumachtigingen:

* Specifieke aspecten van het besluitvormingsbeheer:
   * aanbiedingen_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * classificeren_strategie.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Machtiging voor waarderingsstrategieën beheren {#manage-decisions}

Met de machtiging op hoog niveau **[!UICONTROL Manage ranking strategies]** kunnen gebruikers het rapport met aangepaste berichten lezen, maken, bewerken en verwijderen en actiefuncties gebruiken.

Dit omvat de volgende laagniveaumachtigingen:

* Specifieke aspecten van het besluitvormingsbeheer:
   * classificeren_strategie.read
   * classificeren_strategie.write
   * classificeren_strategie.delete
   * activities.read
   * offers.read
   * placements.read

## Beheercapaciteit {#administration-permissions}

### Machtiging voor subdomeinen delegeren beheren {#manage-subdomain}

Met de machtiging op hoog niveau **[!UICONTROL Manage subdomains delegation]** kunnen gebruikers subdomeindelegatie (inclusief IP-pool) maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* subdomeinen_delegatie.read
* subdomeinen_delegatie.write
* subdomeinen_delegatie.delete

### Toestemming voor PTR-records weergeven {#view-ptr}

De **[!UICONTROL View PTR records]** toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd en de volgende laag-vlakke toestemmingen omvat:

* PTR_records.read
* subdomeinen_delegatie.read

### IP-pools beheren, machtiging {#manage-ip-pools}

Met de machtiging op hoog niveau **[!UICONTROL Manage IP pools]** kunnen gebruikers affiniteitsdefinitie maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Algemene machtigingen voor berichten beheren {#manage-message-settings}

Met de machtiging op hoog niveau **[!UICONTROL Manage messages general settings]** kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* specifiek voor Adobe Experience Platform:
   * schemas.read

### Algemene instellingen van berichten weergeven {#view-message-settings}

Met de machtiging op hoog niveau **[!UICONTROL View messages general settings]** kunnen gebruikers berichten weergeven met algemene instellingen, zoals suppressieregels of uitvoeringsadres.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
* specifiek voor Adobe Experience Platform:
   * schemas.read

### Machtigingen voor voorinstellingen voor berichten beheren {#manage-message-presets}

Met de machtiging op hoog niveau **[!UICONTROL Manage messages presets]** kunnen gebruikers berichtvoorinstellingen voor kanalen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomeinen_delegatie.read
   * IP_pools.read
   * mobile_setting.read (vanuit Adobe Experience Platform Launch)

### Machtigingen voor voorinstellingen voor berichten weergeven {#view-message-presets}

Met de machtiging op hoog niveau **[!UICONTROL View messages presets]** kunnen gebruikers voorinstellingen voor berichten weergeven om te weten welke voorinstellingen voor berichten moeten worden gebruikt bij het maken van een bericht.

Dit omvat de volgende laagniveaumachtigingen:

* messages_presets.read
* subdomeinen_delegatie.read
* IP_pools.read
* mobile_setting.read (vanuit Adobe Experience Platform Launch)

### Machtiging voor suppressieregels beheren {#manage-suppression-rules}

Met de machtiging op hoog niveau **[!UICONTROL Manage suppression rules]** kunnen gebruikers het aantal instanties definiëren voordat het e-mailadres van de gebruiker aan de onderdrukkingslijst wordt toegevoegd.

Dit omvat de volgende laagniveaumachtigingen:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete

### Toestemming voor suppressielijst weergeven {#view-suppresion-list}

Met de machtiging op hoog niveau **[!UICONTROL View suppression list]** kunnen gebruikers berichtconfiguraties weergeven, waaronder voorinstellingen voor berichten en algemene berichtinstellingen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * suppression_list.view
* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Toestemming voor lijst met exportonderdrukking {#export-suppression-list}

Met de machtiging op hoog niveau **[!UICONTROL Export suppression list]** kunnen gebruikers berichtconfiguraties configureren, waaronder voorinstellingen voor berichten en algemene berichtinstellingen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read
