---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer built-in Roles
description: Learn about the built-in Roles
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: permissions, authoring, messages
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 5%

---

# Built-in roles {#ootb-product-profiles}

Built-in roles are a set of unitary rights which allows users access to certain functionalities or objects in the interface. [](ootb-permissions.md)

## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]**

This role includes the following permissions:

| Bronnen | Permissions |
|-|-|
| Campagnes | <ul><li> **[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]** : campagnerapport lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, maak, bewerk en verwijder ip-pool.</li><li>**[!DNL Manage PTR records]**: lees en bewerk PTR-records.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li> **[!DNL Manage messages general settings]**: algemene berichtinstellingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage messages presets]**: lees, creëer, bewerk en verwijder contentbranding.</li><li>**[!DNL Manage suppression rules]**: lees-, creëer-, bewerk- en verwijderingsregels voor toegang tot suppressieregels.</li><li>**[!DNL Export suppression list]** : toegang tot de lijst met exportonderdrukking als een CSV-bestand.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en machtigingen in-/uitschakelen.</li><li>**[!DNL Manage landing page settings]**: lees, creeer, geef, en schrap het landen pagina montages uit.</li><li>**[!DNL Manage SMS settings]**: SMS-instellingen lezen, maken, bewerken en verwijderen.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**</li><li>**[!DNL Read datasets]**</li><li>**[!DNL Read schemas]**</li><li>**[!DNL Read Identity namespace]**</li><li>**[!DNL Manage merge policies]**</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Met de rol **[!DNL Campaign Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Campaigns]** -rapporten.

| Bronnen | Permissions |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**</li><li>**[!DNL Publish campaigns]**</li><li>**[!DNL View Campaigns report]**</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**</li><li>**[!DNL Read datasets]**</li><li>**[!DNL Read schemas]**</li><li>**[!DNL Manage merge policies]**</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Met de rol **[!DNL Campaign Manager]** kunnen gebruikers **[!UICONTROL Campaigns]** en alle mogelijkheden die aan **[!UICONTROL Campaigns]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

This role includes the following permissions:

| Bronnen | Permissions |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**</li><li>**[!DNL View campaigns report]**</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL Manage ranking strategies]**</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**</li><li>**[!DNL Read datasets]**</li><li>**[!DNL Read schemas]**</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Met de rol **[!DNL Campaign Viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Campaigns]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol bevat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]**: alleen-lezen toegang tot campagnes.</li><li>**[!DNL View campaigns report]**: alleen-lezen toegang tot campagnerapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Met de rol **[!DNL Journey Administrator]** kunnen de beheermenu&#39;s de mogelijkheid hebben om de journalen en het besluitvormingsbeheer te beheren en te publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li> **[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journeys]**: publiceer reizen.</li><li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys report]**: rapport over reizen lezen en bewerken.</li></ul> |
| Channel configurations | <ul><li>**[!DNL Manage subdomains delegation]**</li><li>**[!DNL Manage IP pools]**</li><li>**[!DNL Manage PTR records]**</li><li>**[!DNL View PTR records]**</li><li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage Landing page settings]**: subdomeinen van de bestemmingspagina en voorinstellingen van de bestemmingspagina maken, bewerken en verwijderen.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage SMS settings]**: maak, bewerk en verwijder API-referenties en SMS-kanaalconfiguraties die vereist zijn om SMS-kanaal in te schakelen.</li><li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: waarschuwingen voor reizen en aanspraken in-/uitschakelen.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**</li><li>**[!DNL Manage segments]**</li><li>**[!DNL Manage profiles]**</li><li>**[!DNL Read datasets]**</li><li>**[!DNL Read schemas]**</li><li>**[!DNL Read Identity namespace]**</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage Library Items]**: voeg opgeslagen expressies toe en verwijder ze naar de [!DNL Journey Optimizer] -bibliotheek.</li></ul> |
| Datagovernance | <ul><li>**[!DNL Manage usage label]**</li><li>**[!DNL Manage data usage policies]**</li><li>**[!DNL View data usage policies]**</li><li>**[!DNL View user activity log]**</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]** **[!DNL Journey]**

Deze rol bevat de volgende machtigingen:

| Bronnen | Permissions |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**</li><li>**[!DNL Publish journey]**</li><li>**[!DNL View journeys events, data sources and actions]**</li><li>**[!DNL View journeys report]**: lees, bewerk reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Met de rol **[!DNL Journey Manager]** kunnen gebruikers **[!UICONTROL Journeys]** en alle mogelijkheden die aan **[!UICONTROL Journeys]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Met de rol **[!DNL Journey viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**</li><li>**[!DNL View journeys report]**</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]****[!UICONTROL Decision management]** Users assigned to this role will only be able to manage, view and publish decisions.

Deze rol omvat de volgende toestemmingen:

| Capaciteit | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**</li><li>**[!DNL View decisions]**</li><li>**[!DNL Manage ranking strategies]**</li><li>**[!DNL Publish decisions]**</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]****[!UICONTROL Content templates]** Users assigned to this role will only be able to access the template library to create content without accessing the journeys or campaigns.

This role includes the following permissions:

| Capability | Permissions |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**</li><li>**[!DNL Manage simulate content]****[!UICONTROL Simulate content]**</li><li>**[!DNL Publish Fragment]**</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**</li></ul> |