---
title: Geïntegreerde productprofielen
description: Meer informatie over de ingebouwde productprofielen
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 5087c5a13eda0b9b5894197b393788f82413690b
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 8%

---

# Geïntegreerde productprofielen {#ootb-product-profiles}

Adobe Journey Optimizer geeft een nieuwe functie, Inline authoring, uit waarmee u uw berichten rechtstreeks vanaf een reis kunt maken en schrijven. Raadpleeg deze pagina voor meer informatie over deze nieuwe functie.

>[!WARNING]
>
>Als u gebruikers hebt toegewezen aan **[!DNL Message Manager]** alleen productprofiel, zonder **[!DNL Journey manager]** productprofiel, moet u een nieuw productprofiel toewijzen zodat ze inhoud kunnen blijven bewerken.

Deze functie heeft als volgt invloed op de machtigingen:

| Naam van bevoegdheid | Wordt opgenomen in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Na 25 juli**, zijn de toestemmingen met betrekking tot Berichten nog beschikbaar aangezien de Berichten nog kunnen worden betreden om overgang toe te laten en u kunt hen nog opslaan als malplaatje.

**Vanaf 6 september**, worden de machtigingen voor berichten verwijderd en zijn berichten niet meer toegankelijk.

## [!DNL Journey Administrator] {#journey-administrator}

De **[!DNL Journey Administrator]** Dankzij het productprofiel kunnen de administratiemenu&#39;s de mogelijkheid krijgen om de afhandeling van reizen en besluiten te beheren en te publiceren.

Dit productprofiel bevat de volgende toestemmingen:

| Capaciteit | Machtigingen| |-|-| |Reizen| <ul><li> **[!DNL Manage journeys]**: ritten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journeys]**: ritten publiceren.</li><li>**[!DNL Manage journeys events, data sources and actions]**: gebeurtenissen, bronnen of handelingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys report]**: ritsrapport lezen en bewerken.</li></ul>|
|Beheer|<ul><li>**[!DNL Manage subdomains delegation]**: subdomeindelegatie lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage IP pools]**: lees, creeer, geef, en schrap ip pool uit.</li><li>**[!DNL Manage PTR records]**: PTR-records lezen en bewerken.</li><li>**[!DNL View PTR records]**: alleen-lezen toegang tot PTR-records.</li><li>**[!DNL Manage channel surfaces]**: het lezen, creëren, uitgeven, en schrappen van inhoudbranding.</li><li>**[!DNL Manage Landing page settings]**: subdomeinen van de pagina Landing maken, bewerken en verwijderen, en voorinstellingen van de pagina Landing.</li><li> **[!DNL Manage messages general settings]**: algemene instellingen van berichten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage SMS settings]**: Maak, bewerk en verwijder API-referenties en sms-kanaaloppervlakken die nodig zijn om SMS-kanaal in te schakelen.</li><li>**[!DNL Manage suppression rules]**: toegang hebben lees, creeer, geef en schrap suppressieregels uit.</li><li>**[!DNL View suppression list]**: lokale suppressielijst lezen en exporteren.</li><li>**[!DNL Manage alerts]**: signaleringen voor reizen en aanspraken in- en uitschakelen.</li></ul>|
|Beslissingsbeheer|<ul><li>**[!DNL Manage decisions]**: beslissingen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage ranking strategies]**: waarderingsstrategieën lezen, maken, bewerken en verwijderen.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: toegang verlenen tot sandboxen.</li><li>**[!DNL Manage segments]**: segmenten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Read Identity namespace]**: alleen-lezen toegang tot naamruimte.</li><li>**[!DNL Manage merge policies]**: beleid voor het lezen, maken, bewerken en verwijderen van samenvoegingen.</li></ul>| |Journey Optimizer-bibliotheek|<ul><li>**[!DNL Manage Library Items]**: Opgeslagen expressies toevoegen en verwijderen in het dialoogvenster [!DNL Journey Optimizer] Bibliotheek.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

De **[!DNL Journey Approver]** Met het productprofiel kunnen gebruikers leveringen goedkeuren en publiceren. Zij kunnen later het succes van hun leveringen controleren met de **[!DNL Journey]** rapporten.

Dit productprofiel bevat de volgende toestemmingen:

| Capaciteit | Machtigingen| |-|-| |Reizen| <ul><li>**[!DNL Manage journeys]**: ritten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Publish journey]**: ritten publiceren.</li><li>**[!DNL View journeys events, data sources and actions]**: alleen-lezen toegang tot reisevenementen, aangepaste reisacties en bronnen van reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapporten bewerken.</li></ul>|
|Beslissingsbeheer| <ul><li>**[!DNL Manage decisions]**: lezen, maken, bewerken en verwijderen van beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: U kunt aangepaste rapporten lezen, maken, bewerken en verwijderen en actiefuncties gebruiken.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: segmenten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor het lezen, maken, bewerken en verwijderen van samenvoegingen.</li></ul>|
|Beheer| <ul><li>**[!DNL View channel surfaces]**: alleen-lezen toegang tot kanaaloppervlakken.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

De **[!DNL Journey Manager]** Met het productprofiel kunnen gebruikers het bestand maken en bewerken **[!UICONTROL Journeys]** en elke capaciteit die verband houdt met **[!UICONTROL Journeys]** maar kan ze niet publiceren.

Dit productprofiel bevat de volgende toestemmingen:

| Capaciteit | Machtigingen| |-|-| |Reizen| <ul><li>**[!DNL Manage journeys]**: ritten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL View journeys events]**: alleen-lezen toegang tot reisevenementen, aangepaste reisacties en bronnen van reisgegevens.</li><li>**[!DNL View journeys report]**: lezen, reisrapport bewerken.</li></ul>|
|Beslissingsbeheer| <ul><li>**[!DNL Manage decisions]**: lezen, maken, bewerken en verwijderen van beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: U kunt aangepaste rapporten lezen, maken, bewerken en verwijderen en actiefuncties gebruiken.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: segmenten lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Manage profiles]**: profielen lezen, maken, bewerken en verwijderen.</li><li>**[!DNL Read datasets]**: alleen-lezen toegang tot gegevenssets.</li><li>**[!DNL Read schemas]**: alleen-lezen toegang tot schema&#39;s.</li><li>**[!DNL Manage merge policies]**: beleid voor het lezen, maken, bewerken en verwijderen van samenvoegingen.</li></ul>|
|Beheer| <ul><li>**[!DNL View channel surfaces]**: alleen-lezen toegang tot kanaaloppervlakken.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

De **[!DNL Journey viewer]** het productprofiel staat read-only toegang tot toe **[!UICONTROL Journeys]** en **[!UICONTROL Decision management]** mogelijkheden.

Gebruikers die aan dit productprofiel zijn toegewezen, kunnen dit profiel niet bewerken of publiceren.

Dit productprofiel bevat de volgende toestemmingen:

| Capaciteit | Machtigingen| |-|-| |Reizen| <ul><li>**[!DNL View journeys]**: alleen-lezen toegang tot reizen.</li><li>**[!DNL View journeys event, data sources, actions]**: alleen-lezen toegang tot reizen en gegevensbronnen.</li><li>**[!DNL View journeys report]**: alleen-lezen toegang tot reisrapporten.</li></ul>|
|Beslissingsbeheer| <ul><li>**[!DNL View decisions]**: alleen-lezen toegang tot besluitvormingsentiteiten.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

De **[!DNL Decisioning manager]** het productprofiel staat alleen de **[!UICONTROL Decision management]** -menu. Gebruikers die aan dit productprofiel zijn toegewezen, kunnen alleen beslissingen beheren, weergeven en publiceren.

Dit productprofiel bevat de volgende toestemmingen:

| Capaciteit | Machtigingen| |-|-| |Beheer van besluiten | <ul><li>**[!DNL Manage decisions]**: lezen, maken, bewerken en verwijderen van beslissingsentiteiten.</li><li>**[!DNL View decisions]**: alleen-lezen toegang tot beslissingsentiteiten.</li><li>**[!DNL Manage ranking strategies]**: U kunt aangepaste rapporten lezen, maken, bewerken en verwijderen en actiefuncties gebruiken.</li><li>**[!DNL Publish decisions]**: beslissingsactiviteiten activeren of deactiveren.</li></ul>|
