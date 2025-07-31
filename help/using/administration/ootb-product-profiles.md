---
solution: Journey Optimizer
product: journey optimizer
title: ingebouwde Journey Optimizer-rollen
description: Meer informatie over de ingebouwde rollen
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: machtigingen, schrijven, berichten
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ee2e07353762a81aadd3d63580c528f617599623
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 5%

---

# Ingebouwde rollen {#ootb-product-profiles}

Ingebouwde rollen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Verwijs naar [ deze pagina ](ootb-permissions.md) voor de lijst van beschikbare toestemmingen om uw rol te bouwen.

## [!DNL Content Library Manager] {#content-library-manager}

Met de rol **[!DNL Content Library Manager]** hebt u alleen toegang tot het menu **[!UICONTROL Content templates]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen toegang krijgen tot de sjabloonbibliotheek om inhoud te maken zonder de reizen of campagnes te openen.

Deze rol omvat de volgende toestemmingen:

| Capaciteit | Machtigingen |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**: lezen, maken, bewerken en verwijderen van Journey Optimizer Library-items, inclusief inhoudssjablonen en fragmenten.</li><li>**[!DNL Manage simulate content]** : toegang tot de optie **[!UICONTROL Simulate content]** voor een voorvertoning en een proefdruk.</li><li>**[!DNL Publish Fragment]**: publiceer inhoudsfragmenten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Met de rol **[!DNL Decisioning manager]** hebt u alleen toegang tot het menu **[!UICONTROL Decision management]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen beslissingen beheren, weergeven en publiceren.

Deze rol omvat de volgende toestemmingen:

| Capaciteit | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li><li>**[!DNL View decisions]**: alleen-lezen toegang tot beslissingsentiteiten.</li><li>**[!DNL Publish decisions]**: beslissingsactiviteiten activeren of deactiveren.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

Met de rol **[!DNL Campaign Administrator]** kunnen de beheermenu&#39;s campagnes en het beheer van beslissingen beheren en publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li> **[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]** : campagnerapport lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul> <li>**[!DNL Export suppression list]** : toegang tot de lijst met exportonderdrukking als een CSV-bestand.</li> <li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en machtigingen in-/uitschakelen.</li> <li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li> <li>**[!DNL Manage landing page settings]**: lees, creeer, geef, en schrap het landen pagina montages uit.</li> <li>**[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li> <li>**[!DNL Manage SMS settings]**: SMS-instellingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li> <li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Met de rol **[!DNL Campaign Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Campaigns]** -rapporten.

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]**: campagnerapporten lezen, bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Met de rol **[!DNL Campaign Manager]** kunnen gebruikers **[!UICONTROL Campaigns]** en alle mogelijkheden die aan **[!UICONTROL Campaigns]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View campaigns report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Met de rol **[!DNL Campaign Viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Campaigns]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]**: alleen-lezen toegang tot campagnes.</li><li>**[!DNL View campaigns report]**: alleen-lezen toegang tot campagnerapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Met de rol **[!DNL Journey Administrator]** kunnen de beheermenu&#39;s de mogelijkheid hebben om de journalen en het besluitvormingsbeheer te beheren en te publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul> <li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Publish journeys]**: publiceer reizen.</li> <li>**[!DNL View journeys report]**: rapport over reizen lezen en bewerken.</li> </ul> |
| Kanaalconfiguraties | <ul> <li>**[!DNL Manage alerts]**: waarschuwingen voor reizen en aanspraken in-/uitschakelen.</li> <li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li> <li>**[!DNL Manage Landing page settings]**: subdomeinen van de bestemmingspagina en voorinstellingen van de bestemmingspagina maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li> <li>**[!DNL Manage SMS settings]**: maak, bewerk en verwijder API-referenties en SMS-kanaalconfiguraties die vereist zijn om SMS-kanaal in te schakelen.</li> <li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li> <li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li> </ul> |
| Beslissingsbeheer | <ul> <li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li> </ul> |
| Journey Optimizer Library | <ul> <li>**[!DNL Manage Library Items]**: voeg opgeslagen expressies toe en verwijder ze naar de [!DNL Journey Optimizer] -bibliotheek.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL Manage data usage policies]**: beleid voor gegevensgebruik lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage usage label]**: gebruikslabels lezen, maken en verwijderen.</li> <li>**[!DNL View data usage policies]**: alleen-lezen toegang tot beleidsregels voor gegevensgebruik.</li> <li>**[!DNL View user activity log]**: lees- en exportcontrolelogboeken.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Met de rol **[!DNL Journey Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Journey]** -rapporten.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journey]**: publiceer reizen.</li><li>**[!DNL View journeys events, data sources and actions]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lees, bewerk reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Met de rol **[!DNL Journey Manager]** kunnen gebruikers **[!UICONTROL Journeys]** en alle mogelijkheden die aan **[!UICONTROL Journeys]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Met de rol **[!DNL Journey viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**: alleen-lezen toegang tot reisgebeurtenissen en gegevensbronnen.</li><li>**[!DNL View journeys report]**: alleen-lezen toegang tot reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Orchestrated Campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: read, create, edit, and delete custom dashboards.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: Read, create, edit and delete links and reconciliations between Adobe Experience Platform Profiles and Relational store entities.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL View sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to publish Orchestrated campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaign reports.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li> </ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Orchestrated campaigns]** and every capability linked to **[!UICONTROL Orchestrated campaigns]** but will not be able to publish them.

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Orchestrated campaigns]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Messages|<ul><li>**[!DNL View messages]**: view messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

-->