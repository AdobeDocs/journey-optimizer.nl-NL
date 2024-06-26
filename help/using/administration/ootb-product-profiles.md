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
source-git-commit: fd8835b1f9bffd887758e4015171074c5dfc16c0
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 5%

---

# Ingebouwde rollen {#ootb-product-profiles}

Ingebouwde rollen zijn een reeks eenheidrechten die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. Zie [deze pagina](ootb-permissions.md) voor de lijst van beschikbare toestemmingen om uw rol te bouwen.

## [!DNL Campaign Administrator] {#campaign-administrator}

De **[!DNL Campaign Administrator]** Met deze rol kunnen de bestuursmenu&#39;s campagnes en besluitvormingsbeheer beheren en publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li> **[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]**: publicatiecampagnes.</li><li>**[!DNL View campaigns report]**: lees en bewerk het campagnerapport.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li><li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage messages presets]**: inhoud lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Export suppression list]**: toegang tot lijst met exportonderdrukking als een CSV-bestand.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: waarschuwingen voor campagnes, berichten en aanspraken in- en uitschakelen.</li><li>**[!DNL Manage landing page settings]**: lees, maak, bewerk en verwijder de landingspagina-instellingen.</li><li>**[!DNL Manage SMS settings]**: lees-, maak-, bewerk- en verwijderinstellingen voor SMS.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

De **[!DNL Campaign Approver]** Met de rol kunnen gebruikers leveringen goedkeuren en publiceren. Zij kunnen later het succes van hun leveringen controleren met de **[!DNL Campaigns]** rapporten.

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish campaigns]**: publicatiecampagnes.</li><li>**[!DNL View Campaigns report]**: lezen, reisrapporten bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]**: alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

De **[!DNL Campaign Manager]** rol staat gebruikers toe om tot stand te brengen en uit te geven **[!UICONTROL Campaigns]** en elke capaciteit die verband houdt met **[!UICONTROL Campaigns]** maar kan ze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL Manage campaigns]**: campagnes lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View campaigns report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste berichtrapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View messages presets]**: alleen-lezen toegang tot voorinstellingen voor berichten.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

De **[!DNL Campaign Viewer]** rol verleent read-only toegang tot **[!UICONTROL Campaigns]** en **[!UICONTROL Decision management]** mogelijkheden.

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Campagnes | <ul><li>**[!DNL View campaigns]**: alleen-lezen toegang tot campagnes.</li><li>**[!DNL View campaigns report]**: alleen-lezen toegang tot campagnes.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot besluitvormingsentiteiten.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

De **[!DNL Journey Administrator]** Met deze rol kunnen de administratiemenu&#39;s de mogelijkheid krijgen om hun reis- en beslissingsbeheer te beheren en te publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li> **[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journeys]**: publiceer reizen.</li><li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys report]**: reisrapport lezen en bewerken.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li><li>**[!DNL Manage PTR records]**: lees PTR-records en bewerk deze.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li>**[!DNL Manage messages presets]**: inhoud lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage Landing page settings]**: maak, bewerk en verwijder subdomeinen van de bestemmingspagina en voorinstellingen van de bestemmingspagina.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage SMS settings]**: maak, bewerk en verwijder API-referenties en SMS-kanaaloppervlakken die vereist zijn om SMS-kanaal in te schakelen.</li><li>**[!DNL Manage suppression rules]**: toegang tot suppressieregels lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View suppression list]**: lees en exporteer de lokale suppressielijst.</li><li>**[!DNL Manage alerts]**: signaleringen voor reizen en aanspraken in- en uitschakelen.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: geef toegang tot sandboxen.</li><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte voor identiteiten.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Journey Optimizer Library | <ul><li>**[!DNL Manage Library Items]**: opgeslagen expressies toevoegen en verwijderen in het dialoogvenster [!DNL Journey Optimizer] Bibliotheek.</li></ul> |
| Gegevensbeheer | <ul><li>**[!DNL Manage usage label]**: Gebruikslabels lezen, maken en verwijderen.</li><li>**[!DNL Manage data usage policies]**: beleidsregels voor gegevensgebruik lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View data usage policies]**: alleen-lezen toegang tot beleid voor gegevensgebruik.</li><li>**[!DNL View user activity log]**: lees- en exportauditlogs.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

De **[!DNL Journey Approver]** Met de rol kunnen gebruikers leveringen goedkeuren en publiceren. Zij kunnen later het succes van hun leveringen controleren met de **[!DNL Journey]** rapporten.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journey]**: publiceer reizen.</li><li>**[!DNL View journeys events, data sources and actions]**: alleen-lezen toegang tot reisevenementen, aangepaste reisacties en bronnen van reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapporten bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel surfaces]**: alleen-lezen toegang tot kanaaloppervlakken.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

De **[!DNL Journey Manager]** rol staat gebruikers toe om tot stand te brengen en uit te geven **[!UICONTROL Journeys]** en elke capaciteit die verband houdt met **[!UICONTROL Journeys]** maar kan ze niet publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: reizen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisevenementen, aangepaste reisacties en bronnen van reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |
| Kanaalconfiguraties | <ul><li>**[!DNL View channel surfaces]**: alleen-lezen toegang tot kanaaloppervlakken.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

De **[!DNL Journey viewer]** rol verleent read-only toegang tot **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** mogelijkheden.

Gebruikers die aan deze rol zijn toegewezen, kunnen deze niet bewerken of publiceren.

Deze rol omvat de volgende toestemmingen:

| Bronnen | Machtigingen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**: alleen-lezen toegang tot reizen en gegevensbronnen.</li><li>**[!DNL View journeys report]**: alleen-lezen toegang tot reisrapporten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot besluitvormingsentiteiten.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

De **[!DNL Decisioning manager]** rol verleent slechts toegang tot **[!UICONTROL Decision management]** -menu. Gebruikers die aan deze rol zijn toegewezen, kunnen alleen beslissingen beheren, weergeven en publiceren.

Deze rol omvat de volgende toestemmingen:

| Capaciteit | Machtigingen |
|-|-|
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL View decisions]**: alleen-lezen toegang tot beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li><li>**[!DNL Publish decisions]**: beslissingsactiviteiten activeren of deactiveren.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Experience decisioning entities.</li--></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

De **[!DNL Content Library Manager]** rol verleent slechts toegang tot **[!UICONTROL Content templates]** -menu. Gebruikers die aan deze rol zijn toegewezen, kunnen alleen toegang krijgen tot de sjabloonbibliotheek om inhoud te maken zonder de reizen of campagnes te openen.

Deze rol omvat de volgende toestemmingen:

| Capaciteit | Machtigingen |
|-|-|
| Journey Optimizer Library | <ul><li>**[!DNL Manage library items]**: lees, maak, bewerk en verwijder Journey Optimizer Library-items, inclusief inhoudssjablonen en fragmenten.</li><li>**[!DNL Manage simulate content]**: toegang tot de **[!UICONTROL Simulate content]** voor voorvertoning en proefdruk.</li><li>**[!DNL Publish Fragment]**: publiceer inhoudsfragmenten.</li></ul> |
| Beslissingsbeheer | <ul><li>**[!DNL Manage decisions]**: lees, maak, bewerk en verwijder beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: lees-, maak-, bewerk- en verwijder aangepaste rapporten en gebruik actiefuncties.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: segmentdefinities lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor samenvoegen lezen, maken, bewerken en verwijderen.</li></ul> |