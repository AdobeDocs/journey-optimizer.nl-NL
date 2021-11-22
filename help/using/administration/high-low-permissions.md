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
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: da885bd5e29ff3454fef1c6b362f0e646fe8c39a
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Elk productprofiel bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.
Zij kunnen in twee types worden verdeeld:

* **Toestemming op hoog niveau**: vertegenwoordigt de verschillende toestemmingen die kunnen worden toegewezen aan **[!UICONTROL Product profile]** in de [!DNL Admin console], zoals **[!UICONTROL Publish journeys]** en **[!UICONTROL Manage subdomains delegation]**. Machtigingen op hoog niveau omvatten machtigingen op laag niveau.

* **Toestemming op laag niveau**: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

De **[!UICONTROL Journey administrator]** productprofiel is toegewezen aan **[!UICONTROL Manage journeys]** toestemming. Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

## Reiscapaciteit {#journey-capability}

### Toestemming voor reizen beheren {#manage-journeys}

De **[!UICONTROL Manage journeys]** Met machtiging op hoog niveau kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken/verwijderen, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow te bouwen.

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

De **[!UICONTROL Publish journeys]** met toestemming op hoog niveau kunnen gebruikers reizen publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.publish
   * journeys.read

### Toestemming voor reizen weergeven {#view-journeys}

De **[!UICONTROL View journeys]** Met toestemming op hoog niveau kunnen gebruikers door reizen bladeren en deze bekijken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.read

* specifiek voor Adobe Experience Platform:
   * segments.read
   * profiles.read

### Reisgebeurtenissen, gegevensbronnen en handelingen beheren {#manage-journeys-events}

De **[!UICONTROL Manage journeys events, data sources and actions]** Op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevensconfiguraties te vormen.

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

De **[!UICONTROL View journeys events, data sources and actions]** op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevens in de reisstroom te gebruiken.

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

De **[!UICONTROL View journeys report]** de toestemming op hoog niveau staat gebruikers toe om read-only reisrapport te lezen.

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

De **[!UICONTROL Manage messages]** Met machtiging op hoog niveau kunnen gebruikers berichten maken en bewerken/verwijderen.

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

De **[!UICONTROL Manage messages preview and test]** Met machtiging op hoog niveau kunnen gebruikers persoonlijke berichten voorvertonen.

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

De **[!UICONTROL Publish messages]** Met machtiging op hoog niveau kunnen gebruikers berichten publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.publish

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Toestemming voor berichten weergeven {#view-messages}

De **[!UICONTROL View messages]** Met toestemming op hoog niveau kunnen gebruikers alleen berichten lezen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.read
   * messages_presets.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * segments.read

### Toestemming berichtrapport weergeven {#view-message-reports}

De **[!UICONTROL View messages report]** Met toestemming op hoog niveau kunnen gebruikers alleen lezen via e-mail en pushrapporten.

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

De **[!UICONTROL Manage decisions]** met toestemming op hoog niveau kunnen gebruikers nieuwe bestanden maken en bestaande bestanden bewerken/verwijderen **[!UICONTROL Activity entities]** en de objecten beheren die in die activiteiten worden gebruikt om de beslissingen te nemen.

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

De **[!UICONTROL View decisions]** Op hoog niveau staat de toestemming gebruikers toe om een bestaande Activiteit en verwante bedrijfsvoorwerpen te gebruiken om de besluiten te nemen.

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

De **[!UICONTROL Publish offers decisioning]** Met toestemming op hoog niveau hebben gebruikers toegang tot goedgekeurde/niet-goedgekeurde activiteiten van aanbiedingen.

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

De **[!UICONTROL Manage ranking strategies]** De toestemming op hoog niveau staat gebruikers toe om het rapport van douaneberichten te lezen, tot stand te brengen, uit te geven en te schrappen en actiefuncties te gebruiken.

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

De **[!UICONTROL Manage subdomains delegation]** Op hoog niveau staat de toestemming gebruikers toe om subdomeindelegaties (met inbegrip van IP pool) tot stand te brengen, uit te geven en te schrappen.

Dit omvat de volgende laagniveaumachtigingen:

* subdomeinen_delegatie.read
* subdomeinen_delegatie.write
* subdomeinen_delegatie.delete

### Toestemming voor PTR-records weergeven {#view-ptr}

De **[!UICONTROL View PTR records]** De toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd.

Dit omvat de volgende laagniveaumachtigingen:

* PTR_records.read
* subdomeinen_delegatie.read

### IP-pools beheren, machtiging {#manage-ip-pools}

De **[!UICONTROL Manage IP pools]** Met machtiging op hoog niveau kunnen gebruikers de affiniteitsdefinitie maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Algemene machtigingen voor berichten beheren {#manage-message-settings}

De **[!UICONTROL Manage messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* specifiek voor Adobe Experience Platform:
   * schemas.read

### Algemene instellingen van berichten weergeven {#view-message-settings}

De **[!UICONTROL View messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen voor berichten weergeven, zoals het uitvoeringsadres.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
* specifiek voor Adobe Experience Platform:
   * schemas.read

### Machtigingen voor voorinstellingen voor berichten beheren {#manage-message-presets}

De **[!UICONTROL Manage messages presets]** Met machtiging op hoog niveau kunnen gebruikers berichtvoorinstellingen voor verschillende kanalen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomeinen_delegatie.read
   * IP_pools.read
   * mobile_setting.read (vanuit Adobe Experience Platform Launch)

### Machtigingen voor voorinstellingen voor berichten weergeven {#view-message-presets}

De **[!UICONTROL View messages presets]** Met machtiging op hoog niveau kunnen gebruikers voorinstellingen voor berichten weergeven om te weten welke voorinstellingen voor berichten moeten worden gebruikt bij het maken van een bericht.

Dit omvat de volgende laagniveaumachtigingen:

* messages_presets.read
* subdomeinen_delegatie.read
* IP_pools.read
* mobile_setting.read (vanuit Adobe Experience Platform Launch)

### Machtiging voor onderdrukking beheren {#manage-suppression}

De **[!UICONTROL Manage suppression]** Met machtiging op hoog niveau kunnen gebruikers het aantal instanties definiëren voordat een e-mailadres aan de suppressielijst wordt toegevoegd en kunnen ze items toevoegen aan of verwijderen uit de lijst met onderdrukking.

Dit omvat de volgende laagniveaumachtigingen:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Toestemming voor suppressielijst weergeven {#view-suppresion-list}

De **[!UICONTROL View suppression list]** Met machtiging op hoog niveau kunnen gebruikers de inhoud en instellingen van de suppressielijst bekijken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * suppression_list.view
* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Toestemming voor lijst met exportonderdrukking {#export-suppression-list}

De **[!UICONTROL Export suppression list]** Met machtiging op hoog niveau kunnen gebruikers de lijst met onderdrukking downloaden als een CSV-bestand.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * suppression_list.export
* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read
