---
solution: Journey Optimizer
product: journey optimizer
title: Machtigingsniveaus
description: Meer informatie over machtigingen op hoog en laag niveau
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Elk productprofiel bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.
Zij kunnen in twee types worden verdeeld:

* **Toestemming op hoog niveau**: vertegenwoordigt de verschillende toestemmingen die kunnen worden toegewezen aan **[!UICONTROL Product profile]** in de [!DNL Admin console], zoals **[!DNL Publish journeys]** en **[!DNL Manage subdomains delegation]**. Machtigingen op hoog niveau omvatten machtigingen op laag niveau.

* **Toestemming op laag niveau**: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

De **[!DNL Journey administrator]** productprofiel is toegewezen aan **[!DNL Manage journeys]** toestemming. Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

## Reiscapaciteit {#journey-capability}

### [!DNL Manage journeys] machtiging {#manage-journeys}

De **[!DNL Manage journeys]** Met machtiging op hoog niveau kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken/verwijderen, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow te bouwen.

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

### [!DNL Publish journeys] machtiging {#publish-journeys}

De **[!DNL Publish journeys]** met toestemming op hoog niveau kunnen gebruikers reizen publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] machtiging {#view-journeys}

De **[!DNL View journeys]** Met toestemming op hoog niveau kunnen gebruikers door reizen bladeren en deze bekijken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * journeys.read

* specifiek voor Adobe Experience Platform:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] machtiging {#manage-journeys-events}

De **[!DNL Manage journeys events, data sources and actions]** Op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevensconfiguraties te vormen.

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

### [!DNL View journeys events, data sources and actions] machtiging {#view-journeys-event}

De **[!DNL View journeys events, data sources and actions]** op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevens in de reisstroom te gebruiken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * rites_events.read
   * reizen_gegevens_bronnen.read
   * reizen_handelingen.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] machtiging {#view-journeys-report}

De **[!DNL View journeys report]** de toestemming op hoog niveau staat gebruikers toe om read-only reisrapport te lezen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * trajecten_rapport.read
   * messages_report.read

* specifiek voor Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Beslissingsvermogen {#decisions-permissions}

### [!DNL Manage decisions] machtiging {#manage-decisioning}

De **[!DNL Manage decisions]** met toestemming op hoog niveau kunnen gebruikers nieuwe bestanden maken en bestaande bestanden bewerken/verwijderen **[!DNL Activity entities]** en de objecten beheren die in die activiteiten worden gebruikt om de beslissingen te nemen.

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

### [!DNL View decisions] machtiging {#view-decisions}

De **[!DNL View decisions]** Op hoog niveau staat de toestemming gebruikers toe om een bestaande Activiteit en verwante bedrijfsvoorwerpen te gebruiken om de besluiten te nemen.

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

### [!DNL Publish offers decisioning] machtiging {#publish-decisions}

De **[!DNL Publish offers decisioning]** Met toestemming op hoog niveau hebben gebruikers toegang tot goedgekeurde/niet-goedgekeurde activiteiten van aanbiedingen.

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

### [!DNL Manage ranking strategies] machtiging {#manage-ranking-strategies}

De **[!DNL Manage ranking strategies]** Met toestemming op hoog niveau kunnen gebruikers classificatiestrategieën lezen, maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* Specifieke aspecten van het besluitvormingsbeheer:
   * classificeren_strategie.read
   * classificeren_strategie.write
   * classificeren_strategie.delete
   * activities.read
   * offers.read
   * placements.read

## Beheercapaciteit {#administration-permissions}

### [!DNL Manage subdomains delegation] machtiging {#manage-subdomain}

De **[!DNL Manage subdomains delegation]** Op hoog niveau staat de toestemming gebruikers toe om subdomeindelegaties (met inbegrip van IP pool) tot stand te brengen, uit te geven en te schrappen.

Dit omvat de volgende laagniveaumachtigingen:

* subdomeinen_delegatie.read
* subdomeinen_delegatie.write
* subdomeinen_delegatie.delete

### [!DNL Manage PTR records] machtiging {#manage-ptr}

De **[!DNL Manage PTR records]** De toestemming op hoog niveau staat gebruikers toe om PTR verslagen te lezen en uit te geven die gebaseerd op subdomain zijn gevormd.

Dit omvat de volgende laagniveaumachtigingen:

* PTR_records.read
* PTR_records.write
* subdomeinen_delegatie.read

### [!DNL View PTR records] machtiging {#view-ptr}

De **[!DNL View PTR records]** De toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd.

Dit omvat de volgende laagniveaumachtigingen:

* PTR_records.read
* subdomeinen_delegatie.read

### [!DNL Manage IP pools] machtiging {#manage-ip-pools}

De **[!DNL Manage IP pools]** Met machtiging op hoog niveau kunnen gebruikers de affiniteitsdefinitie maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->
### [!DNL Manage channel surface] machtiging {#manage-channel-surface}

De **[!DNL Manage channel surface]** Met machtiging op hoog niveau kunnen gebruikers kanaaloppervlakken maken, bewerken en verwijderen via kanalen op sandboxniveau.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomeinen_delegatie.read
   * IP_pools.read
   * mobile_setting.read (vanuit Adobe Experience Platform Launch)

### [!DNL View channel surface] machtiging {#view-channel-surface}

De **[!DNL View channel surface]** Met machtiging op hoog niveau kunnen gebruikers kanaaloppervlakken weergeven om te weten welke kanaaloppervlakken moeten worden gebruikt.

Dit omvat de volgende laagniveaumachtigingen:

* messages_presets.read
* subdomeinen_delegatie.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)

### [!DNL Manage suppression] machtiging {#manage-suppression}

De **[!DNL Manage suppression]** Met machtiging op hoog niveau kunnen gebruikers het aantal instanties definiëren voordat een e-mailadres aan de suppressielijst wordt toegevoegd en kunnen ze items toevoegen aan of verwijderen uit de lijst met onderdrukking.

Dit omvat de volgende laagniveaumachtigingen:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] machtiging {#view-suppression-list}

De **[!DNL View suppression list]** Met machtiging op hoog niveau kunnen gebruikers de inhoud en instellingen van de suppressielijst bekijken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * suppression_list.view

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] machtiging {#export-suppression-list}

De **[!DNL Export suppression list]** Met machtiging op hoog niveau kunnen gebruikers de lijst met onderdrukking downloaden als een CSV-bestand.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * suppression_list.export

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] machtiging {#manage-landing-page-settings}

De **[!DNL Manage landing page settings]** Met machtiging op hoog niveau kunnen gebruikers subdomeinen van landingspagina&#39;s en instellingen voor voorinstellingen lezen, maken en bewerken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] machtiging {#manage-frequency-rules}

De **[!DNL Manage frequency rules]** Met toestemming op hoog niveau kunnen gebruikers de frequentieregels lezen, maken, bewerken, verwijderen en activeren/deactiveren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] machtiging {#view-frequency-rules}

De **[!DNL View frequency rules]** Op hoog niveau staat de toestemming gebruikers toe om frequentieregels te bekijken.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * frequency_rules.read
