---
title: Oppervlak op basis van code
description: Leer wat een op code-gebaseerde ervaringsoppervlakte is
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# Op code gebaseerde ervaringsoppervlakken {#code-based-surface}

## Wat is een oppervlak? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="De oppervlak-URI voor de component toevoegen"
>abstract="Als uw implementatie niet voor Web, iOS, of Android is, of als u specifieke URIs moet richten, ga een oppervlakte URI in, die een unieke herkenningsteken richtend aan de entiteit is waar u uw ervaring wilt leveren. Zorg ervoor u een oppervlakte URI ingaat die in uw eigen implementatie wordt gebruikt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Creeer een code-gebaseerde ervaringsconfiguratie voor Andere platforms"

Een op code-gebaseerde ervaring **oppervlakte** is om het even welke entiteit die voor gebruiker of systeeminteractie wordt ontworpen, uniek door een [&#x200B; URI &#x200B;](#surface-uri) wordt geïdentificeerd. Het oppervlak wordt gespecificeerd in de [&#x200B; toepassing implementatie &#x200B;](code-based-prerequisites.md#implementation-prerequisites) en moet de oppervlakte aanpassen die in uw [&#x200B; code-gebaseerde configuratie van het ervaringskanaal &#x200B;](code-based-configuration.md) wordt van verwijzingen voorzien.

Een oppervlak kan worden beschouwd als een container op elk hiërarchisch niveau met een bestaande entiteit (aanraakpunt).

* Dit kan een webpagina, een mobiele app, een bureaubladtoepassing, een specifieke inhoudslocatie binnen een grotere entiteit (bijvoorbeeld a `div` ) of een niet-standaard weergavepatroon (bijvoorbeeld een kiosk of een bureaubladtoepassingsbanner) zijn. <!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Het kan zich ook uitstrekken tot specifieke stukken inhoudscontainers voor niet-display of abstracted-display doeleinden (bijvoorbeeld JSON-lobs die aan services worden geleverd).

* Dit kan ook een jokeroppervlak zijn dat overeenkomt met verschillende definities van het clientoppervlak (zo kan een locatie van een hoofdafbeelding op elke pagina van uw website bijvoorbeeld worden vertaald in een oppervlak-URI, zoals: web://mydomain.com/*#hero_image).

>[!NOTE]
>
>Wanneer u meerdere op code gebaseerde ervaringsacties uitvoert op hetzelfde oppervlak, bepaalt de campagne of de rit **[!UICONTROL Priority score]** wat aan de eindgebruiker wordt geleverd als deze in aanmerking komt voor meer dan één actie. [&#x200B; leer meer op prioritaire scores &#x200B;](../conflict-prioritization/priority-scores.md)

## Identificatiecode oppervlak {#surface-uri}

A **oppervlakte URI** dient als nauwkeurige herkenningsteken richtend aan verschillende gebruikersinterface elementen of componenten binnen een toepassing. Een oppervlak-URI bestaat uit meerdere secties:

1. **Type**: Web, mobileapp, atm, kiosk, tvcd, de dienst, enz.
1. **Bezit**: pagina URL of app bundel
1. **Container**: plaats op de pagina/app activiteit

In de onderstaande tabellen staan enkele voorbeelden van de oppervlakte-URI-definitie voor verschillende apparaten.

**Web en mobiel**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Vertegenwoordigt een individueel element binnen een specifieke pagina van een specifiek domein, waar een element een etiket zoals in de volgende voorbeelden kan zijn: hero_banner, top_nav, menu, footer, enz. |
| iOS-app | `mobileapp://com.vendor.bundle/activity#element` | Vertegenwoordigt een specifiek element binnen een inheemse toepassingsactiviteit, zoals een knoop of ander meningselement. |
| Android-app | `mobileapp://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een native app. |

**Andere apparatentypen**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Desktop | `desktop://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een toepassing, zoals een knoop, een menu, een heldenbanner, enz. |
| TV-app | `tvcd://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een apparaat dat op een slimme tv of tv is aangesloten - bundel-id. |
| Service | `service://servicename/#element` | Vertegenwoordigt een server-zijproces of andere handentiteit. |
| Kiosk | `kiosk://location/screen#element` | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |
| ATM | `atm://location/screen#element` | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |

**de oppervlakken van de Vervanging**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Jokertekenweb | `wildcard:web://domain.com/*#element` | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder een specifiek domein. |
| Jokertekenweb | `wildcard:web://*domain.com/*#element` | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder alle domeinen die eindigen met &quot;domain.com&quot;. |

## URI-compositie {#uri-composition}

In [!DNL Journey Optimizer], steunt het op code-gebaseerde ervaringskanaal twee types van klantenimplementaties:

* Gebaseerd op [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} voor uw websites, of op [&#x200B; Mobiele SDK van Adobe Experience Platform &#x200B;](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} voor u mobiele apps;
* Server-kant of hybride gebruikend [&#x200B; de Server APIs van AEP Edge Network &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"}.

>[!NOTE]
>
>Leer meer over de implementatievereisten in [&#x200B; deze sectie &#x200B;](code-based-prerequisites.md#implementation-prerequisites).

Gebruikend op code-gebaseerde ervaringen, kunt u inhoud op korrelplaatsen <!--(such as a specific location on a page, or inside a mobile native app)--> wijzigen die uniek door [!DNL Journey Optimizer] gebruikend [&#x200B; oppervlakte URIs &#x200B;](#surface-uri) worden geïdentificeerd.

Deze oppervlakte-URIs wordt samengesteld en behandeld afhankelijk van de implementatiemethode:

* **Web/Mobiele SDK**: Uw web/mobiele ontwikkelaar moet deze korrelige plaatsen als eenvoudige koorden bepalen, omdat het Web/Mobile SDK geschikt is om de oppervlakte-URI automatisch samen te stellen die op huidige URL/app identiteitskaart en het plaatstekenreeks wordt gebaseerd.

* **Edge Network APIs**: De app/paginaontwikkelaar moet volledige oppervlakte URIs bepalen die de volledige weg en de plaats omvatten waar de inhoud zal worden verbruikt, omdat volledige URIs in dit type van implementatie wordt vereist.

Dit is waarom, wanneer het creëren van a [&#x200B; code-Gebaseerde configuratie van het ervaringskanaal &#x200B;](code-based-configuration.md), u twee manieren hebt om de oppervlakte volgens het geselecteerde platform te specificeren:

* Voor **[!UICONTROL Web]**, **[!UICONTROL iOS]** en **[!UICONTROL Android]** platforms, moet u **URL/app identiteitskaart** en a **plaats of weg** ingaan om de oppervlakte samen te stellen. Leer meer over het vormen van code-gebaseerde ervaringen voor [&#x200B; Web &#x200B;](code-based-configuration.md#web) en [&#x200B; mobiele &#x200B;](code-based-configuration.md#mobile) platforms

* Als het platform **[!UICONTROL Other]** is, moet u de volledige **oppervlakte URI** ingaan, als in de voorbeelden [&#x200B; hierboven &#x200B;](#surface-uri). Leer meer over het vormen op code-gebaseerde ervaringen voor [&#x200B; andere &#x200B;](code-based-configuration.md#other) platforms
