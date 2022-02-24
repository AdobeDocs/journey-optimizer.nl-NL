---
title: Machtigingsniveaus
description: Meer informatie over machtigingen op hoog en laag niveau
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: b1c4fb836d34cc6263f804c7a0f700571281b31a
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

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

## Berichtmogelijkheden {#message-capability}

### [!DNL Manage messages] machtiging {#manage-messages}

De **[!DNL Manage messages]** Met machtiging op hoog niveau kunnen gebruikers berichten maken en bewerken/verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* specifiek voor Adobe Experience Platform:
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] machtiging {#mange-messages-preview}

De **[!DNL Manage messages preview and test]** Met machtiging op hoog niveau kunnen gebruikers persoonlijke berichten voorvertonen.

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

### [!DNL Publish messages] machtiging {#publish-messages}

De **[!DNL Publish messages]** Met machtiging op hoog niveau kunnen gebruikers berichten publiceren.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.publish

* specifiek voor Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] machtiging {#view-messages}

De **[!DNL View messages]** Met toestemming op hoog niveau kunnen gebruikers alleen berichten lezen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages.read
   * messages_presets.read

* specifiek voor Adobe Experience Platform:
   * schemas.read
   * segments.read

### [!DNL View messages report] machtiging {#view-message-reports}

De **[!DNL View messages report]** Met toestemming op hoog niveau kunnen gebruikers alleen lezen via e-mail en pushrapporten.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

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

### [!DNL Manage ranking strategies] machtiging {#manage-decisions}

De **[!DNL Manage ranking strategies]** De toestemming op hoog niveau staat gebruikers toe om het rapport van douaneberichten te lezen, tot stand te brengen, uit te geven en te schrappen en actiefuncties te gebruiken.

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

### [!DNL Manage messages general settings] machtiging {#manage-message-settings}

De **[!DNL Manage messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* specifiek voor Adobe Experience Platform:
   * schemas.read

### [!DNL View messages general settings] machtiging {#view-message-settings}

De **[!DNL View messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen voor berichten weergeven, zoals het uitvoeringsadres.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_general_settings.read
* specifiek voor Adobe Experience Platform:
   * schemas.read

### [!DNL Manage messages presets] machtiging {#manage-message-presets}

De **[!DNL Manage messages presets]** Met machtiging op hoog niveau kunnen gebruikers berichtvoorinstellingen voor verschillende kanalen op sandboxniveau maken, bewerken en verwijderen.

Dit omvat de volgende laagniveaumachtigingen:

* specifiek voor Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomeinen_delegatie.read
   * IP_pools.read
   * mobile_setting.read (vanuit Adobe Experience Platform Launch)

### [!DNL View messages presets] machtiging {#view-message-presets}

De **[!DNL View messages presets]** Met machtiging op hoog niveau kunnen gebruikers voorinstellingen voor berichten weergeven om te weten welke voorinstellingen voor berichten moeten worden gebruikt bij het maken van een bericht.

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

## Journey Optimizer Library-mogelijkheid {library-permissions}

### Bibliotheekitems beheren {#library-items}

De **[!DNL Manage Library Items]** Met machtiging op hoog niveau kunnen gebruikers opgeslagen expressies toevoegen en verwijderen in het dialoogvenster [!DNL Journey Optimizer] Bibliotheek.

Dit omvat de volgende laagniveaumachtigingen:

* library_item.create
* library_item.delete
