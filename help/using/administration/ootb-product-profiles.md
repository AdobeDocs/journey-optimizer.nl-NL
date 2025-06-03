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
source-git-commit: 49a607e8e4b4cce7bcf41d92abe6b9fa54dfb411
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 5%

---

# Ingebouwde rollen {#ootb-product-profiles}

Ingebouwde rollen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Verwijs naar [ deze pagina ](ootb-permissions.md) voor de lijst van beschikbare toestemmingen om uw rol te bouwen.

## [!DNL Campaign Administrator] {#campaign-administrator}

Met de rol **[!DNL Campaign Administrator]** kunnen de beheermenu&#39;s campagnes en het beheer van beslissingen beheren en publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li> **[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View campaigns report]** : campagnerapport lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li><li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Export suppression list]** : toegang tot de lijst met exportonderdrukking als een CSV-bestand.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en machtigingen in-/uitschakelen.</li><li>**[!DNL Manage landing page settings]**: lees, creeer, geef, en schrap het landen pagina montages uit.</li><li>**[!DNL Manage SMS settings]**: SMS-instellingen lezen, maken, bewerken en verwijderen.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Met de rol **[!DNL Campaign Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Campaigns]** -rapporten.

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]** : publicatiecampagnes.</li><li>**[!DNL View Campaigns report]**: lees, bewerk reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Met de rol **[!DNL Campaign Manager]** kunnen gebruikers **[!UICONTROL Campaigns]** en alle mogelijkheden die aan **[!UICONTROL Campaigns]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View campaigns report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]** : alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Met de rol **[!DNL Campaign Viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Campaigns]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]**: alleen-lezen toegang tot campagnes.</li><li>**[!DNL View campaigns report]**: alleen-lezen toegang tot campagnerapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Met de rol **[!DNL Journey Administrator]** kunnen de beheermenu&#39;s de mogelijkheid hebben om de journalen en het besluitvormingsbeheer te beheren en te publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li> **[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journeys]**: publiceer reizen.</li><li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys report]**: rapport over reizen lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li><li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li>**[!DNL Manage messages presets]**: inhoud, branding lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage Landing page settings]**: subdomeinen van de bestemmingspagina en voorinstellingen van de bestemmingspagina maken, bewerken en verwijderen.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage SMS settings]**: maak, bewerk en verwijder API-referenties en SMS-kanaalconfiguraties die vereist zijn om SMS-kanaal in te schakelen.</li><li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: waarschuwingen voor reizen en aanspraken in-/uitschakelen.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage Library Items]**: voeg opgeslagen expressies toe en verwijder ze naar de [!DNL Journey Optimizer] -bibliotheek.</li></ul> |
| Datagovernance | <ul><li>**[!DNL Manage usage label]**: gebruikslabels lezen, maken en verwijderen.</li><li>**[!DNL Manage data usage policies]**: beleid voor gegevensgebruik lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View data usage policies]**: alleen-lezen toegang tot beleidsregels voor gegevensgebruik.</li><li>**[!DNL View user activity log]**: lees- en exportcontrolelogboeken.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

Met de rol **[!DNL Journey Approver]** kunnen gebruikers leveringen goedkeuren en publiceren. Ze kunnen later het succes van hun leveringen controleren met de **[!DNL Journey]** -rapporten.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journey]**: publiceer reizen.</li><li>**[!DNL View journeys events, data sources and actions]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lees, bewerk reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Met de rol **[!DNL Journey Manager]** kunnen gebruikers **[!UICONTROL Journeys]** en alle mogelijkheden die aan **[!UICONTROL Journeys]** zijn gekoppeld maken en bewerken, maar kunnen ze deze niet publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisgebeurtenissen, aangepaste reisacties en bronnen voor reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel configurations]**: alleen-lezen toegang tot kanaalconfiguraties.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Met de rol **[!DNL Journey viewer]** hebt u alleen-lezen toegang tot de mogelijkheden **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** .

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze machtiging omvat de volgende machtigingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**: alleen-lezen toegang tot reisgebeurtenissen en gegevensbronnen.</li><li>**[!DNL View journeys report]**: alleen-lezen toegang tot reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot entiteiten voor beslissingen.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Met de rol **[!DNL Decisioning manager]** hebt u alleen toegang tot het menu **[!UICONTROL Decision management]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen beslissingen beheren, weergeven en publiceren.

Deze machtiging omvat de volgende machtigingen:

| Capaciteit | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View decisions]**: alleen-lezen toegang tot beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li><li>**[!DNL Publish decisions]**: beslissingsactiviteiten activeren of deactiveren.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Met de rol **[!DNL Content Library Manager]** hebt u alleen toegang tot het menu **[!UICONTROL Content templates]** . Gebruikers die aan deze rol zijn toegewezen, kunnen alleen toegang krijgen tot de sjabloonbibliotheek om inhoud te maken zonder de reizen of campagnes te openen.

Deze machtiging omvat de volgende machtigingen:

| Capaciteit | Machtigingen |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**: lezen, maken, bewerken en verwijderen van Journey Optimizer Library-items, inclusief inhoudssjablonen en fragmenten.</li><li>**[!DNL Manage simulate content]** : toegang tot de optie **[!UICONTROL Simulate content]** voor een voorvertoning en een proefdruk.</li><li>**[!DNL Publish Fragment]**: publiceer inhoudsfragmenten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: besluitvormingsentiteiten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: samenvoegbeleid lezen, maken, bewerken en verwijderen.</li></ul> |