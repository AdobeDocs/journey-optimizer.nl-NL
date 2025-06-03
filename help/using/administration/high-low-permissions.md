---
solution: Journey Optimizer
product: journey optimizer
title: Machtigingsniveaus
description: Meer informatie over machtigingen op hoog en laag niveau waarmee gebruikers toegang kunnen krijgen tot de verschillende functies.
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: toestemming, high-level, laag-level, profiel, admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 1a2c6e97fcd30245cff1bf08fd5771ce8bc84ddc
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Elke rol bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.
Zij kunnen in twee types worden verdeeld:

* **toestemming op hoog niveau**: vertegenwoordigt de verschillende toestemmingen die aan **[!UICONTROL Role]**, zoals **[!DNL Publish journeys]** en **[!DNL Manage subdomains delegation]** kunnen worden toegewezen. Rechten op hoog niveau omvatten bevoegdheden op laag niveau. De toestemmingen op hoog niveau zijn gedetailleerd op [ deze pagina ](ootb-permissions.md).

* **laagvlakke toestemming**: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

De rol **[!DNL Journey administrator]** wordt bijvoorbeeld toegewezen aan de machtiging **[!DNL Manage journeys]** . Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

## Reisbron {#journey-capability}

* Met machtiging op hoog niveau van **[!DNL Manage journeys]** kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken/verwijderen, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow op te bouwen.

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

* Met **[!DNL Publish journeys]** -machtiging op hoog niveau kunnen gebruikers reizen publiceren.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* Met **[!DNL View journeys]** -machtiging op hoog niveau kunnen gebruikers door reizen bladeren en deze weergeven.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * journeys.read

   * specifiek voor Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* Met machtiging op hoog niveau van **[!DNL Manage journeys events, data sources and actions]** kunnen gebruikers gebeurtenis- en gegevensconfiguraties configureren.

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

* Met **[!DNL View journeys events, data sources and actions]** machtiging op hoog niveau kunnen gebruikers gebeurtenissen en gegevens gebruiken in de reisflow.

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

* **[!DNL View journeys report]** toestemming op hoog niveau staat gebruikers toe om read-only reisrapport te lezen.

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

* Met machtiging op hoog niveau van **[!DNL Manage frequency rules]** kunnen gebruikers de frequentieregels lezen, maken, bewerken, verwijderen en activeren/deactiveren.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* Met machtiging op hoog niveau van **[!DNL View frequency rules]** kunnen gebruikers de frequentieregels weergeven.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * frequency_rules.read

+++

## Campagnebron {#campaign-capability}

* Met machtiging op hoog niveau van **[!DNL Export suppression list]** kunnen gebruikers de lijst met downloads downloaden als een CSV-bestand.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * suppression_list.export

   * specifiek voor Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* Met machtiging op hoog niveau kunnen gebruikers nieuwe campagnes maken en deze bewerken/verwijderen **[!DNL Manage campaigns]**

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* Met machtiging op hoog niveau van **[!DNL Publish campaigns]** kunnen gebruikers campagnes publiceren.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * door campagne gelezen
      * campagnepublicatie
        <!--* experiments.activate-->

+++

* Met machtiging op hoog niveau van **[!DNL View campaigns report]** kunnen gebruikers campagnerapport lezen en bewerken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## Hulpbron voor Besluit {#decisions-permissions}

* Met machtiging op hoog niveau van **[!DNL Manage decisions]** kunnen gebruikers nieuwe functies maken en bestaande **[!DNL Activity entities]** bewerken/verwijderen, en de objecten beheren die in deze activiteiten worden gebruikt om de beslissingen te nemen.

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

* **[!DNL View decisions]** toestemming op hoog niveau staat gebruikers toe om een bestaande Activiteit en verwante bedrijfsvoorwerpen te gebruiken om de besluiten te nemen.

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

+++

* Met machtiging op hoog niveau van **[!DNL Manage offers]** kunnen gebruikers alle aanbiedingen, componenten, leesbeslissingen en verzamelingen maken, bewerken en verwijderen.

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

* Met machtiging op hoog niveau van **[!DNL Manage ranking strategies]** kunnen gebruikers classificatiestrategieën lezen, maken, bewerken en verwijderen.

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
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

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

* **[!DNL Manage file routing]** toestemming op hoog niveau staat gebruikers toe om dossier tot stand te brengen uit te geven en te schrappen die configuraties verpletteren.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* Met machtiging op hoog niveau van **[!DNL Manage IP pools]** kunnen gebruikers de affiniteitsdefinitie maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* Met machtiging op hoog niveau van **[!DNL Manage landing page settings]** kunnen gebruikers landingssubdomeinen en vooraf ingestelde instellingen van pagina&#39;s lezen, maken en bewerken.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* Met machtiging op hoog niveau van **[!DNL Manage messages general settings]** kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * specifiek voor Adobe Experience Platform:
      * schemas.read

+++

* Met machtiging op hoog niveau van **[!DNL Manage messages presets]** kunnen gebruikers kanaalconfiguraties lezen, maken, bewerken en verwijderen op het niveau van de sandbox.

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

* Met machtiging op hoog niveau van **[!DNL Manage PTR records]** kunnen gebruikers PTR-records lezen en bewerken die zijn geconfigureerd op basis van het subdomein.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomeinen_delegatie.read

+++

* Met machtiging op hoog niveau van **[!DNL Manage Seedlist]** kunnen gebruikers de zaadlijst lezen, maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* Met machtiging op hoog niveau van **[!DNL Manage SMS subdomains]** kunnen gebruikers sms-subdomeinen lezen, maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * sms_subdomeinen.read
      * sms_subdomeinen.write
      * sms_subdomeinen.delete

+++

* Met **[!DNL Manage subdomains delegations]** -machtiging op hoog niveau kunnen gebruikers subdomeindelegaties (waaronder IP-pool) maken, bewerken en verwijderen.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * subdomeinen_delegatie.read
      * subdomeinen_delegatie.write
      * subdomeinen_delegatie.delete

+++

* Met machtiging op hoog niveau van **[!DNL Manage suppression]** kunnen gebruikers het aantal instanties definiëren voordat een e-mailadres aan de lijst met onderdrukking wordt toegevoegd en kunt u items toevoegen aan of verwijderen uit de lijst met onderdrukking.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]** toestemming op hoog niveau staat gebruikers toe om dossier te bekijken die configuraties verpletteren.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * file_routing.read

+++

* Met machtiging op hoog niveau van **[!DNL View messages general settings]** kunnen gebruikers berichten weergeven met algemene instellingen, zoals het uitvoeringsadres.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read

   * specifiek voor Adobe Experience Platform:
      * schemas.read

+++

* Met machtiging op hoog niveau van **[!DNL View messages presets]** kunnen gebruikers voorinstellingen voor berichten weergeven.

+++ Dit omvat de volgende laagniveaumachtigingen:

   * specifiek voor Journey Optimizer:
      * messages_presets.read
      * subdomeinen_delegatie.read
      * IP_pools.read

   * Specifieke gegevensverzameling:
      * Mobile_setting.read

+++

* **[!DNL View PTR records]** toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd.

+++ Dit omvat de volgende laagniveaumachtigingen:
   * specifiek voor Journey Optimizer:

      * PTR_records.read
      * subdomeinen_delegatie.read

+++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* Met machtiging op hoog niveau van **[!DNL View suppression list]** kunnen gebruikers de inhoud en instellingen van de suppressielijst bekijken.

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

## Hulpbron voor AI {#ai-permissions}

* Met machtiging op hoog niveau van **[!DNL Generate content]** hebben gebruikers toegang tot AI Assistant in Journey Optimizer.

+++ Dit omvat de volgende laagactieve machtigingen:

   * specifiek voor Journey Optimizer:
      * ai-assistant-generated-content.generate

+++
