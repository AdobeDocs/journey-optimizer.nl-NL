---
title: Aan de slag met op code gebaseerde ervaringen
description: Meer informatie over code-gebaseerde ervaringen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: e3c597f66436e8e0e22d06f1905fc7ca9a9dd570
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 1%

---

# Aan de slag met op code gebaseerd kanaal {#get-sarted-code-based}

Met [!DNL Journey Optimizer] kunt u de ervaringen die u aan uw klanten wilt leveren aanpassen en testen op al uw aanraakpunten, zoals webapps, mobiele apps, bureaubladapps, videoconsoles, apparaten met tv-verbinding, intelligente tv&#39;s, kiosken, geldautomaten, spraakassistenten, IoT-apparaten enzovoort.

Met het **code-gebaseerde ervaring** vermogen, kunt u binnenkomende ervaringen bepalen gebruikend een eenvoudige en intuïtieve niet visuele redacteur. Hiermee kunt u specifieke elementen invoegen en bewerken op afzonderlijke en meer gedetailleerde locaties van uw apps of webpagina&#39;s, ongeacht het type toepassing dat u hebt, in plaats van wijzigingen toe te passen op de gehele inhoud.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>De specifieke begeleiding en de aanbevelingen voor code-gebaseerde ervaringen zijn gedetailleerd in [ deze pagina ](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lood" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong> hoe het </strong> werkt
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validatie" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong> Guardrails en eerste vereisten </strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Onfrequent" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong> creeer een op code-gebaseerde ervaring </strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Validatie" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong> steekproeven van de Implementatie </strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Wanneer moet u op code gebaseerde versus andere kanalen gebruiken? {#code-based-vs-other-channels}

### Codegebaseerde versus andere kanalen

Wanneer moet u het op code gebaseerde kanaal gebruiken in plaats van de andere [!DNL Journey Optimizer] kanalen?

* U kunt het gebruiken van code-gebaseerde ervaringen overwegen wanneer uw digitaal bezit niet door Webbrowser of een mobiele app - gevallen wordt betreden waarin u waarschijnlijk beter het [!DNL Journey Optimizer] [ Webkanaal ](../web/get-started-web.md){target="_blank"} of [!DNL Journey Optimizer] [ in-app overseinen ](../in-app/get-started-in-app.md){target="_blank"} kanaal kunt gebruiken.

* U kunt het op code-gebaseerde kanaal als alternatief voor het [!DNL Journey Optimizer] Webkanaal gebruiken als uw website niet in de [ 2} visuele redacteur van de Webontwerper kan worden geladen {of als u niet de [ browser uitbreiding ](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} kunt gebruiken die visuele auteurskracht voor Webkanaal.](../web/edit-web-content.md#work-with-web-designer){target="_blank"}

* U kunt het op code gebaseerde kanaal ook gebruiken als alternatief voor het [!DNL Journey Optimizer] web of in-app kanalen voor het geval u een API-gebaseerde, headless of server-side implementatie hebt.

### Codegebaseerd versus webkanaal {#code-based-vs-web}

Als u zaken voor webgebruik wilt uitvoeren, kunt u het webkanaal of de ervaring op basis van code gebruiken, maar afhankelijk van uw context is een van beide geschikter. De belangrijkste verschillen worden hieronder vermeld zodat kunt u een weloverwogen besluit nemen over wat te gebruiken wanneer.

**Web**

* Bewerk uw inhoud gebruikend de ](../web/edit-web-content.md#work-with-web-designer){target="_blank"} visuele redacteur van de 0} Webontwerper {.[
* U hebt de ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html) {target="_blank"} implementatie van SDK van het Web van Adobe Experience Platform 0} {en de [ Visuele het Uitgeven Helper van Adobe Experience Cloud ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca) {target="_blank"} uitbreiding nodig die op uw Webbrowser wordt geïnstalleerd. [ [Meer informatie](../web/web-prerequisites.md){target="_blank"}
* Met het webkanaal kunt u alles op de pagina wijzigen en hebt u een vooraf gedefinieerde lijst met handelingen die u kunt gebruiken om wijzigingen aan te brengen. [Meer informatie](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* Het is eenvoudig om in te stellen en snel te gaan.
* Het is gericht op marketer-persona.

**op code-gebaseerde ervaring**

* Bewerk uw inhoud gebruikend de [ verpersoonlijkingsredacteur ](create-code-based.md#edit-code).
* De op code-gebaseerde ervaring vereist vorige ontwikkelingswerk aan uw implementatie om ervoor te zorgen dat uw toepassingen de inhoud kunnen interpreteren en leveren die op de rand door [!DNL Journey Optimizer] voor deze plaatsen wordt gepubliceerd. [Meer informatie](code-based-configuration.md#surface-definition)
* Het vereist meer planning en het kan slechts de dingen veranderen die de ontwikkelaars specificeren. Daarom is het van essentieel belang dat de componenten worden geïdentificeerd (thuisbanner, hoofdafbeelding, menubalk, enz.) op de toepassingen die voor verpersoonlijking of het testen moeten worden gewijzigd, en met uw ontwikkelingsteam samenwerken om de implementatie te bouwen nodig voor de behandeling van deze veranderingen.
* U kunt hiermee JSON-code-inhoud gebruiken.
* Het is gericht op ontwikkelaars-persoonlijkheid.

## Werking {#how-it-works}

>[!CAUTION]
>
>Deze functie is bedoeld voor ontwikkelaars en/of ervaren gebruikers. Het kan door marketers met sommige code-schrijvende vaardigheden worden gebruikt, zolang de kanaalconfiguraties en aanvankelijke opstelling door uw ontwikkelingsteam worden behandeld.

Als u de inhoud wilt bewerken met de ervaringsfunctie van [!DNL Journey Optimizer] op code gebaseerde, pagina&#39;s of apps moeten van instrumenten worden voorzien. Om dit te doen, moet u vóór de specifieke individuele plaatsen (genoemd &quot;[ oppervlakten ](code-based-configuration.md#surface-definition)&quot;verklaren waar u inhoud wilt opnemen of vervangen.

>[!NOTE]
>
>De inhoud die momenteel aan een configuratie is gekoppeld, kan alleen HTML of JSON zijn.

De belangrijkste stappen om een op code-gebaseerde campagne uit te voeren zijn als volgt.

1. Bepaal a [ oppervlakte ](code-based-configuration.md#surface-definition) in uw toepassingsimplementatie, die fundamenteel de plaats is waar u uw op code-gebaseerde ervaring wilt toevoegen, en een code-gebaseerde configuratie van het ervaringskanaal creëren die verwijzingen die plaats. [ leer hoe ](code-based-configuration.md#create-code-based-configuration)

1. Maak een reis of campagne in [!DNL Journey Optimizer] met deze configuratie. [ leer hoe ](create-code-based.md#create-code-based-campaign)

1. Stel een ervaring samen door inhoud voor de geselecteerde configuratie te specificeren gebruikend de [!DNL Journey Optimizer] verpersoonlijkingsredacteur. [ leer hoe ](create-code-based.md#edit-code)

1. Uw app-implementatieteam doet expliciete API- of SDK-aanroepen om inhoud op te halen voor de benoemde oppervlakken, zoals &quot;Banner Text&quot; of &quot;Recommendations Tray 1&quot; of niet-UI gerelateerde beslissingspunten in een toepassing, zoals &quot;zoekalgoritmeparameters&quot;. In dit geval is het implementatieteam verantwoordelijk voor het renderen of anderszins interpreteren en reageren op de geretourneerde inhoud. [Meer informatie](code-based-implementation-samples.md)
