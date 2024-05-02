---
solution: Journey Optimizer
product: journey optimizer
title: Machtigingsniveaus
description: Meer informatie over machtigingen op hoog en laag niveau waarmee gebruikers toegang krijgen tot de verschillende functies.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: machtiging, hoog niveau, laag niveau, profiel, beheerconsole
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 5d214812b1d7e189fe8a964f445545916d00c0a4
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Elke rol bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.
Zij kunnen in twee types worden verdeeld:

* **Toestemming op hoog niveau**: vertegenwoordigt de verschillende toestemmingen die kunnen worden toegewezen aan **[!UICONTROL Role]**, zoals **[!DNL Publish journeys]** en **[!DNL Manage subdomains delegation]**. Machtigingen op hoog niveau omvatten machtigingen op laag niveau. Machtigingen op hoog niveau worden beschreven in [deze pagina](ootb-permissions.md).

* **Toestemming op laag niveau**: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

Bijvoorbeeld de **[!DNL Journey administrator]** de rol wordt toegewezen aan **[!DNL Manage journeys]** toestemming. Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

## Reisbron {#journey-capability}

* **[!DNL Manage journeys]** Met machtiging op hoog niveau kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken/verwijderen, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow te bouwen.

+++ Dit omvat de volgende laagniveaumachtigingen:

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

+++

* **[!DNL Publish journeys]** met toestemming op hoog niveau kunnen gebruikers reizen publiceren.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** Met toestemming op hoog niveau kunnen gebruikers door reizen bladeren en deze bekijken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * journeys.read

   * specifiek voor Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** Op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevensconfiguraties te vormen.

+++ Dit omvat de volgende laagniveaumachtigingen:

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

+++

* **[!DNL View journeys events, data sources and actions]** op hoog niveau staat de toestemming gebruikers toe om gebeurtenis en gegevens in de reisstroom te gebruiken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * rites_events.read
      * reizen_gegevens_bronnen.read
      * reizen_handelingen.read

   * specifiek voor Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** de toestemming op hoog niveau staat gebruikers toe om read-only reisrapport te lezen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * trajecten_rapport.read
      * messages_report.read

   * specifiek voor Adobe Experience Platform:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Bron voor Journey Optimizer-regels {#journey-rules-capability}

* **[!DNL Manage frequency rules]** Met toestemming op hoog niveau kunnen gebruikers de frequentieregels lezen, maken, bewerken, verwijderen en activeren/deactiveren.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** Op hoog niveau staat de toestemming gebruikers toe om frequentieregels te bekijken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * frequency_rules.read

+++

## Campagnebron {#campaign-capability}

* **[!DNL Export suppression list]** Met machtiging op hoog niveau kunnen gebruikers de lijst met onderdrukking downloaden als een CSV-bestand.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * suppression_list.export

   * specifiek voor Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]** Met machtiging op hoog niveau kunnen gebruikers nieuwe campagnes maken en deze bewerken/verwijderen

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** Met machtiging op hoog niveau kunnen gebruikers campagnes publiceren.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * door campagne gelezen
      * campagnepublicatie
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** op hoog niveau staat de toestemming gebruikers toe om campagnerapport te lezen en uit te geven.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Hulpbron voor Besluit {#decisions-permissions}

* **[!DNL Manage decisions]** met toestemming op hoog niveau kunnen gebruikers nieuwe bestanden maken en bestaande bestanden bewerken/verwijderen **[!DNL Activity entities]** en de objecten beheren die in die activiteiten worden gebruikt om de beslissingen te nemen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * Specifiek beheer van besluiten:
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

+++

* **[!DNL View decisions]** Op hoog niveau staat de toestemming gebruikers toe om een bestaande Activiteit en verwante bedrijfsvoorwerpen te gebruiken om de besluiten te nemen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * Specifiek beheer van besluiten:
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

+++

* **[!DNL Manage offers]** Met toestemming op hoog niveau kunnen gebruikers alle aanbiedingen, componenten, leesbeslissingen en verzamelingen maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * Specifiek beheer van besluiten:
      * aanbiedingen_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * classificeren_strategie.read

   * specifiek voor Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** Met toestemming op hoog niveau kunnen gebruikers classificatiestrategieën lezen, maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * Specifiek beheer van besluiten:
      * classificeren_strategie.read
      * classificeren_strategie.write
      * classificeren_strategie.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Bron voor kanaalconfiguraties {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Experience decisioning entities.

  +++ It includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* **[!DNL Manage file routing]** de toestemming op hoog niveau staat gebruikers toe om dossier te creëren uit te geven en te schrappen dat configuraties verplettert.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* **[!DNL Manage IP pools]** Met machtiging op hoog niveau kunnen gebruikers de affiniteitsdefinitie maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]** Met machtiging op hoog niveau kunnen gebruikers subdomeinen van landingspagina&#39;s en instellingen voor voorinstellingen lezen, maken en bewerken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * specifiek voor Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL Manage messages presets]** Met machtiging op hoog niveau kunnen gebruikers kanaaloppervlakken lezen, maken, bewerken en verwijderen op het niveau van de sandbox.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomeinen_delegatie.read
      * IP_pools.read

   * Specifieke gegevensverzameling:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]** De toestemming op hoog niveau staat gebruikers toe om PTR verslagen te lezen en uit te geven die gebaseerd op subdomain zijn gevormd.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomeinen_delegatie.read

+++

* **[!DNL Manage Seedlist]** Met machtiging op hoog niveau kunnen gebruikers de zaadlijst lezen, maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]** Met toestemming op hoog niveau kunnen gebruikers sms-subdomeinen lezen, maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * sms_subdomeinen.read
      * sms_subdomeinen.write
      * sms_subdomeinen.delete

+++

* **[!DNL Manage subdomains delegations]** Op hoog niveau kunnen gebruikers subdomeindelegaties (waaronder IP-pool) maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * subdomeinen_delegatie.read
      * subdomeinen_delegatie.write
      * subdomeinen_delegatie.delete

+++

* **[!DNL Manage suppression]** Met machtiging op hoog niveau kunnen gebruikers het aantal instanties definiëren voordat een e-mailadres aan de suppressielijst wordt toegevoegd en kunnen ze items toevoegen aan of verwijderen uit de lijst met onderdrukking.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]** de toestemming op hoog niveau staat gebruikers toe om dossier te bekijken dat configuraties verplettert.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * file_routing.read

+++

* **[!DNL View messages general settings]** Met machtiging op hoog niveau kunnen gebruikers algemene instellingen voor berichten weergeven, zoals het uitvoeringsadres.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read

   * specifiek voor Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL View messages presets]** Met machtiging op hoog niveau kunnen gebruikers voorinstellingen voor berichten weergeven.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_presets.read
      * subdomeinen_delegatie.read
      * IP_pools.read

   * Specifieke gegevensverzameling:
      * Mobile_setting.read

+++

* **[!DNL View PTR records]** De toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * PTR_records.read
      * subdomeinen_delegatie.read

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]** Met machtiging op hoog niveau kunnen gebruikers de inhoud en instellingen van de suppressielijst bekijken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * suppression_list.view

   * specifiek voor Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

