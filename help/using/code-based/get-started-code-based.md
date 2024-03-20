---
title: Aan de slag met op code gebaseerde ervaringen
description: Meer informatie over code-gebaseerde ervaringen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '1205'
ht-degree: 1%

---

# Aan de slag met op code gebaseerd kanaal {#get-sarted-code-based}

>[!AVAILABILITY]
>
>Momenteel is het op code gebaseerde ervaringskanaal niet beschikbaar voor organisaties die de Adobe hebben aangeschaft **Gezondheidsschild** en **Privacy- en beveiligingsschild** add-on aanbiedingen.

[!DNL Journey Optimizer] kunt u de ervaringen die u aan uw klanten wilt leveren aanpassen en testen op al uw aanraakpunten, zoals webapps, mobiele apps, bureaubladapps, bureaubladapps, videoconsoles, apparaten met tv-verbinding, intelligente tv&#39;s, kiosken, geldautomaten, spraakassistenten, IoT-apparaten, enz.

Met de **code-gebaseerde ervaring** kunt u ingebouwde ervaringen definiëren met een eenvoudige en intuïtieve niet-visuele editor. Hiermee kunt u specifieke elementen invoegen en bewerken op afzonderlijke en meer gedetailleerde locaties van uw apps of webpagina&#39;s, ongeacht het type toepassing dat u hebt, in plaats van wijzigingen toe te passen op de gehele inhoud.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!CAUTION]
>
>Momenteel in [!DNL Journey Optimizer] u kunt alleen op code gebaseerde ervaringen maken met **campagnes**.

Wanneer u [een campagne opzetten](../campaigns/create-campaign.md#configure), selecteert u **Ervaring op basis van code** als uw handeling en basisinstellingen definiëren.

>[!NOTE]
>
>Als dit de eerste keer is dat u een op code gebaseerde ervaring maakt, moet u ervoor zorgen dat u de in [deze sectie](code-based-prerequisites.md).

<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lood" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Hoe werkt het</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validatie" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Vereisten</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Onfrequent" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Een op code gebaseerde ervaring maken</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Validatie" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Uitvoeringsvoorbeelden</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Wanneer moet u op code gebaseerde versus andere kanalen gebruiken? {#code-based-vs-other-channels}

### Codegebaseerde versus andere kanalen

Wanneer moet u het op code gebaseerde kanaal gebruiken in plaats van het andere? [!DNL Journey Optimizer] kanalen?

* U kunt overwegen om op code-gebaseerde ervaringen te gebruiken wanneer uw digitale bezit niet door Webbrowser of een mobiele app wordt betreden - gevallen waarin u waarschijnlijk beter kunt gebruiken [!DNL Journey Optimizer] [webkanaal](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} kanaal.

* U kunt het op code gebaseerde kanaal gebruiken als alternatief voor het [!DNL Journey Optimizer] webkanaal als uw website niet in de [webontwerper](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} dat visuele authoring voor het webkanaal mogelijk maakt.

* U kunt het op code gebaseerde kanaal ook gebruiken als alternatief voor het [!DNL Journey Optimizer] web- of in-app-kanalen voor het geval u een API-gebaseerde, headless- of server-side implementatie hebt.

### Codegebaseerd versus webkanaal

Als u zaken voor webgebruik wilt uitvoeren, kunt u het webkanaal of de ervaring op basis van code gebruiken, maar afhankelijk van uw context is een van beide geschikter. De belangrijkste verschillen worden hieronder vermeld zodat kunt u een weloverwogen besluit nemen over wat te gebruiken wanneer.

**Web**
* Uw inhoud bewerken met de opdracht [webontwerper](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visuele editor.
* U hebt de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Met het webkanaal kunt u alles op de pagina wijzigen en hebt u een vooraf gedefinieerde lijst met handelingen die u kunt gebruiken om wijzigingen aan te brengen. [Meer informatie](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* Het is eenvoudig om in te stellen en snel te gaan.
* Het is gericht op marketer-persona.

**Ervaring op basis van code**
* Uw inhoud bewerken met de opdracht [Expression-editor](create-code-based.md#edit-code).
* De op code-gebaseerde ervaring vereist vorige ontwikkelingswerk aan uw implementatie om ervoor te zorgen dat uw oppervlakten de inhoud kunnen interpreteren en leveren die op de rand wordt gepubliceerd door [!DNL Journey Optimizer] voor deze oppervlakken. [Meer informatie](#surface-definition)
* Het vereist meer planning en het kan slechts de dingen veranderen die de ontwikkelaars specificeren. Daarom is het van essentieel belang dat de componenten worden geïdentificeerd (thuisbanner, hoofdafbeelding, menubalk, enz.) op de oppervlakken die moeten worden aangepast voor personalisatie of testen, en samenwerken met uw ontwikkelingsteam om de implementatie te bouwen die nodig is voor het verwerken van deze wijzigingen.
* U kunt hiermee JSON-code-inhoud gebruiken.
* Het is gericht op ontwikkelaars-persoonlijkheid.

## Werking {#how-it-works}

>[!CAUTION]
>
>Deze functie is bedoeld voor ontwikkelaars en/of ervaren gebruikers. Het kan door marketers met sommige code-schrijvende vaardigheden worden gebruikt, zolang de oppervlakimplementaties en aanvankelijke opstelling door uw ontwikkelingsteam worden behandeld.

Als u de inhoud wilt bewerken met de [!DNL Journey Optimizer] uw pagina&#39;s of apps moeten zijn voorzien van instrumenten voor de op code gebaseerde ervaringsfunctie. Hiervoor moet u vóór de specifieke individuele locaties declareren (aangeduid als &quot;[oppervlakken](#surface-definition)&quot;) waar u inhoud wilt invoegen of vervangen<!--HOW??-->.

>[!NOTE]
>
>Momenteel kan de inhoud die aan een oppervlak is gekoppeld, alleen HTML of JSON zijn. <!--WILL COME LATER: text, image or another format depending on the application-->

De belangrijkste stappen om een op code-gebaseerde campagne uit te voeren zijn als volgt.

1. Een [oppervlak](#surface-definition), wat eigenlijk de plaats is waar u uw code-gebaseerde ervaring wilt toevoegen, en een campagne in [!DNL Journey Optimizer] met dit oppervlak. [Meer informatie](create-code-based.md#create-code-based-campaign)

1. Stel een ervaring samen door inhoud voor het geselecteerde oppervlak te specificeren gebruikend [!DNL Journey Optimizer] Expressieeditor. [Meer informatie](create-code-based.md#edit-code)

1. Uw app-implementatieteam doet expliciete API- of SDK-aanroepen om inhoud op te halen voor de benoemde oppervlakken, zoals &quot;Banner Text&quot; of &quot;Recommendations Tray 1&quot; of niet-UI gerelateerde beslissingspunten in een toepassing, zoals &quot;zoekalgoritmeparameters&quot;. In dit geval is het implementatieteam verantwoordelijk voor het renderen of anderszins interpreteren en reageren op de geretourneerde inhoud.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Wat is een oppervlak? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Een op code gebaseerd ervaringsoppervlak definiëren"
>abstract="Een op code gebaseerd oppervlak is een entiteit die is ontworpen voor interactie van gebruiker of systeem, en die uniek wordt geïdentificeerd door een URI."

A **code-gebaseerd ervaringsoppervlak** is een entiteit die is ontworpen voor interactie van gebruiker of systeem<!--ask Robert to explain further-->, die op unieke wijze wordt geïdentificeerd door een **URI**.

Met andere woorden, een oppervlak kan worden beschouwd als een container op elk hiërarchisch niveau met een bestaande entiteit (aanraakpunt).<!--good idea to illustrate how it can be seen, but to clarify-->

* Het kan een webpagina, een mobiele app, een bureaubladtoepassing of een specifieke inhoudlocatie binnen een grotere entiteit zijn (bijvoorbeeld een `div`) of een niet-standaard weergavepatroon (bijvoorbeeld een kiosk of een banner van een bureaubladtoepassing).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Het kan zich ook uitstrekken tot specifieke stukken inhoudscontainers voor niet-display of abstracted-display doeleinden (bijvoorbeeld JSON-lobs die aan services worden geleverd).

* Dit kan ook een jokeroppervlak zijn dat overeenkomt met verschillende definities van het clientoppervlak (zo kan een locatie van een hoofdafbeelding op elke pagina van uw website bijvoorbeeld worden vertaald in een oppervlak-URI, zoals: web://mydomain.com/*#hero_image).

Een oppervlak-URI bestaat in principe uit meerdere secties:
1. **Type**: web, ios, android, atm, kiosk, tvcd, service, enz.
1. **Eigenschap**: pagina-URL of app-bundel
1. **Container**: locatie op de pagina/app-activiteit

In de onderstaande tabellen staan enkele voorbeelden van de oppervlakte-URI-definitie voor verschillende apparaten.

**Web en mobiel**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Web | web://domain.com/path/page.html | Vertegenwoordigt een afzonderlijk pad en een afzonderlijke pagina van een website. |
| Web | web://domain.com/path/page.html#element | Vertegenwoordigt een individueel element binnen een specifieke pagina van een specifiek domein. |
| Web | web://domain.com/*#element | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder een specifiek domein. |
| iOS-app | mobileapp://com.vendor.bundle | Vertegenwoordigt een specifieke mobiele toepassing voor één platform - in dit geval iOS-app. |
| iOS-app | mobileapp://com.vendor.bundle/activity | Vertegenwoordigt een specifieke activiteit (mening) binnen een mobiele toepassing. |
| iOS-app | mobileapp://com.vendor.bundle/activity#element | Vertegenwoordigt een specifiek element binnen een activiteit, zoals een knoop of ander meningselement. |
| Android-app | mobileapp://com.vendor.bundle | Vertegenwoordigt een specifieke mobiele toepassing voor één platform - in dit geval Android-app. |

**Andere apparaattypen**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Desktop | desktop://com.vendor.bundle | Vertegenwoordigt een specifieke bureaubladtoepassing. |
| Desktop | desktop://com.vendor.bundle#element | Vertegenwoordigt een specifiek element binnen een toepassing, zoals een knoop, een menu, een heldenbanner, enz. |
| tvOS-app | tvos://com.vendor.bundle | Vertegenwoordigt een specifieke tvOS-app. |
| TV-app | tvcd://com.vendor.bundle | Vertegenwoordigt een specifieke apparaat-app voor Smart TV of met tv verbonden apparaten - bundle ID. |
| Service | service://servicename | Vertegenwoordigt een server-zijproces of andere handentiteit. |
| Kiosk | kiosk://location/screen | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |
| ATM | atm://location/screen | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |

**Jokeroppervlakken**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Jokertekenweb | jokerteken:web:/domain.com/`*`#element | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder een specifiek domein. |
| Jokertekenweb | jokerteken:web://`*`domain.com/`*`#element | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder alle domeinen die eindigen met &quot;domain.com&quot;. |



