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
source-git-commit: 2a5db6950ac82fd18deb2e4009c9a43247444d6a
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 0%

---

# Machtigingsniveaus {#high-low-permissions}


Elke rol bestaat uit machtigingen waarmee gebruikers toegang hebben tot de verschillende functies.

Zij kunnen in twee types worden verdeeld:

* **toestemming op hoog niveau**: vertegenwoordigt de verschillende toestemmingen die aan **[!UICONTROL Role]**, zoals **[!DNL Publish journeys]** en **[!DNL Manage subdomains delegation]** kunnen worden toegewezen. Rechten op hoog niveau omvatten bevoegdheden op laag niveau. De toestemmingen op hoog niveau zijn gedetailleerd op [ deze pagina ](ootb-permissions.md).

* **laagvlakke toestemming**: vertegenwoordigt de verschillende toestemmingen die uit de toestemming op hoog niveau komen.

De rol **[!DNL Journey administrator]** wordt bijvoorbeeld toegewezen aan de machtiging **[!DNL Manage journeys]** . Uit deze toestemming vloeit het laagniveautoestemmingen voort die de beheerder van de Reis zullen toestaan om reizen te schrijven, te lezen en te schrappen.

![](assets/do-not-localize/permissions.png){width="70%"}


## Reisbron {#journey-capability}

* Met **[!DNL Manage journeys]** machtiging op hoog niveau kunnen gebruikers nieuwe reizen maken en bestaande reizen bewerken, verwijderen, stoppen en pauzeren, en toegang krijgen tot de objecten die op het canvas van de reis worden gebruikt om de reisflow te bouwen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:
      * journeys.publish
      * journeys.read

  +++

* Met **[!DNL View journeys]** -machtiging op hoog niveau kunnen gebruikers door reizen bladeren en deze weergeven.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * journeys.read

   * specifiek voor Adobe Experience Platform:
      * segments.read
      * profiles.read

  +++

* Met machtiging op hoog niveau van **[!DNL Manage journeys events, data sources and actions]** kunnen gebruikers gebeurtenis- en gegevensconfiguraties configureren.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

  +++

* Met machtiging op hoog niveau van **[!DNL View frequency rules]** kunnen gebruikers de frequentieregels weergeven.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * frequency_rules.read

  +++

## Campagnebron {#campaign-capability}

* Met machtiging op hoog niveau van **[!DNL Export suppression list]** kunnen gebruikers de lijst met downloads downloaden als een CSV-bestand.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * suppression_list.export

   * specifiek voor Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

* Met machtiging op hoog niveau kunnen gebruikers nieuwe campagnes maken en deze bewerken/verwijderen **[!DNL Manage campaigns]**

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

  +++

* Met machtiging op hoog niveau van **[!DNL Publish campaigns]** kunnen gebruikers campagnes publiceren.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:

   * specifiek voor Journey Optimizer:

      * door campagne gelezen
      * campagnepublicatie
        <!--* experiments.activate-->

  +++

* Met machtiging op hoog niveau van **[!DNL View campaigns report]** kunnen gebruikers campagnerapport lezen en bewerken.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

  +++

## Hulpbron voor Besluit {#decisions-permissions}

* Met machtiging op hoog niveau van **[!DNL Manage decisions]** kunnen gebruikers nieuwe functies maken en bestaande **[!DNL Activity entities]** bewerken/verwijderen, en de objecten beheren die in deze activiteiten worden gebruikt om de beslissingen te nemen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

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

  +++ This permission includes the following low-level permissions:  

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

  +++

* Met machtiging op hoog niveau van **[!DNL Manage IP pools]** kunnen gebruikers de affiniteitsdefinitie maken, bewerken en verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

  +++

* Met machtiging op hoog niveau van **[!DNL Manage landing page settings]** kunnen gebruikers landingssubdomeinen en vooraf ingestelde instellingen van pagina&#39;s lezen, maken en bewerken.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

  +++

* Met machtiging op hoog niveau van **[!DNL Manage messages general settings]** kunnen gebruikers algemene instellingen op sandboxniveau maken, bewerken en verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * specifiek voor Adobe Experience Platform:
      * schemas.read

  +++

* Met machtiging op hoog niveau van **[!DNL Manage messages presets]** kunnen gebruikers kanaalconfiguraties lezen, maken, bewerken en verwijderen op het niveau van de sandbox.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

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

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomeinen_delegatie.read

  +++

* Met machtiging op hoog niveau van **[!DNL Manage Seedlist]** kunnen gebruikers de zaadlijst lezen, maken, bewerken en verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

  +++

* Met machtiging op hoog niveau van **[!DNL Manage SMS subdomains]** kunnen gebruikers sms-subdomeinen lezen, maken, bewerken en verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * sms_subdomeinen.read
      * sms_subdomeinen.write
      * sms_subdomeinen.delete

  +++

* Met **[!DNL Manage subdomains delegations]** -machtiging op hoog niveau kunnen gebruikers subdomeindelegaties (waaronder IP-pool) maken, bewerken en verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:

      * subdomeinen_delegatie.read
      * subdomeinen_delegatie.write
      * subdomeinen_delegatie.delete

  +++

* Met machtiging op hoog niveau van **[!DNL Manage suppression]** kunnen gebruikers het aantal instanties definiëren voordat een e-mailadres aan de lijst met onderdrukking wordt toegevoegd en kunt u items toevoegen aan of verwijderen uit de lijst met onderdrukking.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

  +++

* **[!DNL View file routing]** toestemming op hoog niveau staat gebruikers toe om dossier te bekijken die configuraties verpletteren.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  
   * specifiek voor Journey Optimizer:

      * file_routing.read

  +++

* Met machtiging op hoog niveau van **[!DNL View messages general settings]** kunnen gebruikers berichten weergeven met algemene instellingen, zoals het uitvoeringsadres.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * messages_general_settings.read

   * specifiek voor Adobe Experience Platform:
      * schemas.read

  +++

* Met machtiging op hoog niveau van **[!DNL View messages presets]** kunnen gebruikers voorinstellingen voor berichten weergeven.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 

   * specifiek voor Journey Optimizer:
      * messages_presets.read
      * subdomeinen_delegatie.read
      * IP_pools.read

   * Specifieke gegevensverzameling:
      * Mobile_setting.read

  +++

* **[!DNL View PTR records]** toestemming op hoog niveau staat gebruikers toe om PTR verslagen te bekijken die gebaseerd op subdomain zijn gevormd.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen: 
   * specifiek voor Journey Optimizer:

      * PTR_records.read
      * subdomeinen_delegatie.read

  +++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* Met machtiging op hoog niveau van **[!DNL View suppression list]** kunnen gebruikers de inhoud en instellingen van de suppressielijst bekijken.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:
      * suppression_list.view

   * specifiek voor Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ This permission includes the following low-level permissions: 
-->

## Hulpbron voor AI {#ai-permissions}

* Met machtiging op hoog niveau van **[!DNL Generate content]** hebben gebruikers toegang tot AI Assistant in Journey Optimizer.

  +++ Dit omvat de volgende laagactieve machtigingen:  

   * specifiek voor Journey Optimizer:
      * ai-assistant-generated-content.generate

  +++

## Geordende campagnebron {#ai-orchestrated-campaign}

* Met machtiging op hoog niveau van **[!DNL Manage orchestrated campaigns]** kunnen gebruikers nieuwe campagnes maken en geordende campagnes bewerken/verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * orchestrated_campagnes.read
      * orchestrated_campagnes.write
      * orchestrated_campagnes.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * specifiek voor Adobe Experience Platform:

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

  +++

* Met machtiging op hoog niveau van **[!DNL Manage orchestrated campaigns admin]** kunnen gebruikers nieuwe koppelingen en verbindingen en verbindingen tussen Adobe Experience Platform-profielen en relationele opslagentiteiten maken en bewerken/verwijderen.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

  +++

* Met **[!DNL Publish orchestrated campaigns]** machtiging op hoog niveau kunnen gebruikers geordende campagnes publiceren.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:

   * specifiek voor Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * specifiek voor Adobe Experience Platform:

      * sandboxes.view

  +++

* Met **[!DNL View orchestrated campaigns]** machtiging op hoog niveau kunnen gebruikers de geordende campagne en de inhoud ervan bekijken.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * specifiek voor Adobe Experience Platform:

      * sandboxes.view
      * segments.read
      * profiles.read

  +++

* Met machtiging op hoog niveau van **[!DNL View orchestrated campaigns admin]** kunnen gebruikers de beheerinstellingen weergeven, maar kunnen instellingen niet worden bewerkt.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read

  +++

* **[!DNL View orchestrated campaigns report]** toestemming op hoog niveau staat gebruikers toe om georkestreerde campagneprestaties in zowel levend als bedrijfsrapport te bekijken.

  +++ Deze toestemming omvat de volgende laagvlakke toestemmingen:  

   * specifiek voor Journey Optimizer:

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * specifiek voor Adobe Experience Platform:

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++
