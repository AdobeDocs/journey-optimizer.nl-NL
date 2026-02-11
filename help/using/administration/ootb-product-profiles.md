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
source-git-commit: a91d5c6a22f81411d7a9acbe2bbc8e86c1a4da13
workflow-type: tm+mt
source-wordcount: '2009'
ht-degree: 5%

---

# Ingebouwde rollen {#ootb-product-profiles}

Ingebouwde rollen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Verwijs naar [&#x200B; deze pagina &#x200B;](ootb-permissions.md) voor de lijst van beschikbare toestemmingen om uw rol te bouwen.


## [!DNL Campaign Administrator] {#campaign-administrator}

Met de rol **[!DNL Campaign Administrator]** kunnen de beheermenu&#39;s campagnes en het beheer van beslissingen beheren en publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li> </ul> |
| Campagnes | <ul><li> **[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]** : campagnerapport lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul> <li>**[!DNL Export suppression list]** : toegang tot de lijst met exportonderdrukking als een CSV-bestand.</li> <li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en machtigingen in-/uitschakelen.</li> <li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li> <li>**[!DNL Manage landing page settings]**: lees, creeer, geef, en schrap het landen pagina montages uit.</li> <li>**[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li> <li>**[!DNL Manage SMS settings]**: SMS-instellingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li> <li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Met de rol **[!DNL Campaign Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Campaigns]** -rapporten.

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]**: campagnerapporten lezen, bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

Met de rol **[!DNL Campaign Manager]** kunnen gebruikers **[!UICONTROL Campaigns]** en alle mogelijkheden die aan **[!UICONTROL Campaigns]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View campaigns report]**: lezen, reisrapport bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Met de rol **[!DNL Campaign Viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Campaigns]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]**: alleen-lezen toegang tot campagnes.</li><li>**[!DNL View campaigns report]**: alleen-lezen toegang tot campagnerapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Met de rol **[!DNL Content Library Manager]** hebt u alleen toegang tot het menu **[!UICONTROL Content templates]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen toegang krijgen tot de sjabloonbibliotheek om inhoud te maken zonder de reizen of campagnes te openen.

Deze machtiging omvat de volgende machtigingen:

| Capaciteit | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**: lezen, maken, bewerken en verwijderen van Journey Optimizer Library-items, inclusief inhoudssjablonen en fragmenten.</li><li>**[!DNL Manage simulate content]** : toegang tot de optie **[!UICONTROL Simulate content]** voor een voorvertoning en een proefdruk.</li><li>**[!DNL Publish Fragment]**: publiceer inhoudsfragmenten.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Met de rol **[!DNL Decisioning manager]** hebt u alleen toegang tot het menu **[!UICONTROL Decision management]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen beslissingen beheren, weergeven en publiceren.

Deze machtiging omvat de volgende machtigingen:

| Capaciteit | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li><li>**[!DNL View decisions]**: alleen-lezen toegang tot beslissingsentiteiten.</li><li>**[!DNL Publish decisions]**: beslissingsactiviteiten activeren of deactiveren.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Met de rol **[!DNL Journey Administrator]** kunnen de beheermenu&#39;s de mogelijkheid hebben om de journalen en het besluitvormingsbeheer te beheren en te publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li> </ul> |
| Kanaalconfiguraties | <ul> <li>**[!DNL Manage alerts]**: waarschuwingen voor reizen en aanspraken in-/uitschakelen.</li> <li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li> <li>**[!DNL Manage Landing page settings]**: subdomeinen van de bestemmingspagina en voorinstellingen van de bestemmingspagina maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li> <li>**[!DNL Manage SMS settings]**: maak, bewerk en verwijder API-referenties en SMS-kanaalconfiguraties die vereist zijn om SMS-kanaal in te schakelen.</li> <li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li> <li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL Manage data usage policies]**: beleid voor gegevensgebruik lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage usage label]**: gebruikslabels lezen, maken en verwijderen.</li> <li>**[!DNL View data usage policies]**: alleen-lezen toegang tot beleidsregels voor gegevensgebruik.</li> <li>**[!DNL View user activity log]**: alleen-lezen toegang tot opgenomen auditlogs van Experience Platform-activiteiten.</li> </ul> |
| Beslissingsbeheer | <ul> <li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li> </ul> |
| Journeys | <ul> <li>**[!DNL Manage journeys]**: lees-, maak-, bewerk-, stop- (live, testmodus en droge run) en verwijder reizen. </li> <li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Publish journeys]**: publiceren, testmodus starten, droge run starten, reizen onderbreken en hervatten. </li> <li>**[!DNL View journeys report]**: rapport over reizen lezen en bewerken.</li> </ul> |
| Journey Optimizer Library | <ul> <li>**[!DNL Manage Library Items]**: voeg opgeslagen expressies toe en verwijder ze naar de [!DNL Journey Optimizer] -bibliotheek.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Met de rol **[!DNL Journey Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Journey]** -rapporten.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Journeys | <ul><li>**[!DNL Manage journeys]**: lees-, maak-, bewerk-, stop- (live, testmodus en droge run) en verwijder reizen. </li><li>**[!DNL Publish journey]**: publiceren, testmodus starten, droge run starten, reizen onderbreken en hervatten. </li><li>**[!DNL View journeys events, data sources and actions]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lees, bewerk reisrapporten.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Met de rol **[!DNL Journey Manager]** kunnen gebruikers **[!UICONTROL Journeys]** en alle mogelijkheden die aan **[!UICONTROL Journeys]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Journeys | <ul><li>**[!DNL Manage journeys]**: lees-, maak-, bewerk-, stop- (live, testmodus en droge run) en verwijder reizen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Met de rol **[!DNL Journey viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |
| Journeys | <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**: alleen-lezen toegang tot reisgebeurtenissen en gegevensbronnen.</li><li>**[!DNL View journeys report]**: alleen-lezen toegang tot reisrapporten.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

Met de rol **[!DNL Orchestrated Campaign Administrator]** kunnen de beheermenu&#39;s geordende campagnes beheren en publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**: schakel de door AI aangedreven campagne- en publieksfuncties in of open.</li> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li> <li>**[!DNL View operational insights]**: alleen-lezen toegang tot inzichten op systeemniveau en dashboards controleren.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Export suppression list]** : toegang tot de lijst met exportonderdrukking als een CSV-bestand.</li> <li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en machtigingen in-/uitschakelen.</li> <li>**[!DNL Manage custom dashboards]**: aangepaste dashboards lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li> <li>**[!DNL Manage landing page settings]**: lees, creeer, geef, en schrap het landen pagina montages uit.</li> <li>**[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li> <li>**[!DNL Manage SMS settings]**: SMS-instellingen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li> <li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li> </ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: lees, maak, bewerk en verwijder aangepaste widgets en widgetschema via de Widgetbibliotheek.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL View user activity log]**: alleen-lezen toegang tot opgenomen controlelogboeken van Experience Platform-activiteiten. </li> </ul> |
| Gegevensinvoer | <ul> <li>**[!DNL Manage sources]**: bronnen lezen, maken, bewerken en uitschakelen.</li> </ul> |
| Data management | <ul> <li>**[!DNL Manage datasets]**: datasets lezen, maken, bewerken en verwijderen.</li> </ul> |
| Gegevensmodellering | <ul> <li>**[!DNL Manage schemas]**: schema&#39;s en gerelateerde bronnen lezen, maken, bewerken en verwijderen.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Journey Optimizer-regels | <ul> <li>**[!DNL View frequency rules]**: alleen-lezen toegang tot frequentieregels.</li><li>**[!DNL Manage frequency rules]**: frequentieregels lezen, maken, bewerken of verwijderen.</li> </ul> |
| Berichten | <ul><li> **[!DNL Manage Messages]**: berichten lezen, maken, bewerken en verwijderen. </li> **[!DNL Manage Messages Preview and Test]** : geef uw goedkeuring en publiceer berichten wanneer een beleid wordt toegepast.</li><li>**[!DNL Publish Messages]** : publicatieberichten. </li><li>**[!DNL View Messages Report]**: berichtrapporten lezen en bewerken. <li></ul> |
| Geordende campagnes | <ul><li> **[!DNL Manage orchestrated campaigns]**: geordende campagnes lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: koppelingen en aansluitingen tussen Adobe Experience Platform Profiles en Relational Store-entiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish orchestrated campaigns]**: geordende campagnes publiceren.</li><li>**[!DNL View orchestrated campaigns report]**: lees en bewerk het geordende campagnerapport.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

Met de rol **[!DNL Orchestrated Campaign Approver]** kunnen gebruikers geordende campagnes publiceren.

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li> <li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li> <li>**[!DNL Enable AI Assistant]**: schakel de door AI aangedreven campagne- en publieksfuncties in of open.</li>  <li>**[!DNL View operational insights]**: alleen-lezen toegang tot inzichten op systeemniveau en dashboards controleren.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li> <li>**[!DNL Manage custom dashboards]**: maak, bewerk en verwijder aangepaste dashboards.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: lees, maak, bewerk en verwijder aangepaste widgets en widgetschema via de Widgetbibliotheek.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL View user activity log]**: alleen-lezen toegang tot opgenomen controlelogboeken van Experience Platform-activiteiten.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Journey Optimizer-regels | <ul> <li>**[!DNL View frequency rules]**: alleen-lezen toegang tot frequentieregels.</li></ul> |
| Berichten | <ul><li> **[!DNL Manage Messages]**: berichten lezen, maken, bewerken en verwijderen. </li> **[!DNL Manage Messages Preview and Test]** : geef uw goedkeuring en publiceer berichten wanneer een beleid wordt toegepast.</li><li>**[!DNL Publish Messages]** : publicatieberichten. </li><li>**[!DNL View Messages Report]**: berichtrapporten lezen en bewerken. <li></ul> |
| Geordende campagnes | <ul><li>**[!DNL Manage orchestrated campaigns]**: geordende campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish orchestrated campaigns]**: geordende campagnes publiceren.</li><li>**[!DNL View orchestrated campaigns admin]**: alleen-lezen toegang tot koppelingen en aansluitingen tussen Adobe Experience Platform Profiles en Relational Store-entiteiten.</li><li>**[!DNL View orchestrated campaigns report]**: lees geordende campagnerapporten, bewerk deze.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

Met de rol **[!DNL Orchestrated Campaign Manager]** kunnen gebruikers **[!UICONTROL Orchestrated campaigns]** en alle mogelijkheden die aan **[!UICONTROL Orchestrated campaigns]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: schakel de door AI aangedreven campagne- en publieksfuncties in of open.</li> <li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View datasets]**: alleen-lezen toegang tot gegevenssets.</li>  <li>**[!DNL View operational insights]**: alleen-lezen toegang tot inzichten op systeemniveau en dashboards controleren.</li><li>**[!DNL View schemas]**: alleen-lezen toegang tot schema&#39;s.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage custom dashboards]**: maak, bewerk en verwijder aangepaste dashboards.</li><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: lees, maak, bewerk en verwijder aangepaste widgets en widgetschema via de Widgetbibliotheek.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL View user activity log]**: alleen-lezen toegang tot opgenomen controlelogboeken van Experience Platform-activiteiten.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Journey Optimizer-regels | <ul> <li>**[!DNL View frequency rules]**: alleen-lezen toegang tot frequentieregels. </li></ul> |
| Berichten | <ul><li> **[!DNL Manage Messages]**: berichten lezen, maken, bewerken en verwijderen. </li> **[!DNL Manage Messages Preview and Test]** : geef uw goedkeuring en publiceer berichten wanneer een beleid wordt toegepast.</li><li>**[!DNL View Messages Report]**: berichtrapporten lezen en bewerken. </li></ul> |
| Geordende campagnes | <ul><li>**[!DNL Manage orchestrated campaigns]**: geordende campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View orchestrated campaigns report]**: geordende campagnes lezen, bewerken.</li><li>**[!DNL View orchestrated campaigns admin]**: alleen-lezen toegang tot koppelingen en aansluitingen tussen Adobe Experience Platform Profiles en Relational Store-entiteiten.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

Met de rol **[!DNL Campaign Viewer]** hebt u alleen-lezen toegang tot de mogelijkheden van **[!UICONTROL Orchestrated campaigns]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: schakel de door AI aangedreven campagne- en publieksfuncties in of open.</li> <li>**[!DNL View operational insights]**: alleen-lezen toegang tot inzichten op systeemniveau en dashboards controleren.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage custom dashboards]**: maak, bewerk en verwijder aangepaste dashboards.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: lees, maak, bewerk en verwijder aangepaste widgets en widgetschema via de Widgetbibliotheek.</li> </ul> |
| Datagovernance | <ul> <li>**[!DNL View user activity log]**: alleen-lezen toegang tot opgenomen controlelogboeken van Experience Platform-activiteiten.</li> </ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |
| Journey Optimizer-regels | <ul> <li>**[!DNL View frequency rules]**: alleen-lezen toegang tot frequentieregels.</li></ul> |
| Geordende campagnes | <ul><li>**[!DNL View orchestrated campaigns]**: alleen-lezen toegang tot geordende campagnes.</li><li>**[!DNL View orchestrated campaigns report]**: alleen-lezen toegang tot geordende campagnes.</li></ul> |




