---
title: Aan de slag met op code gebaseerde ervaringen
description: Meer informatie over code-gebaseerde ervaringen in Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 1%

---

# Aan de slag met op code gebaseerd kanaal {#get-sarted-code-based}

Met [!DNL Journey Optimizer] kunt u de ervaringen die u aan uw klanten wilt leveren aanpassen en testen op al uw aanraakpunten, zoals webapps, mobiele apps, bureaubladapps, videoconsoles, apparaten met tv-verbinding, intelligente tv&#39;s, kiosken, geldautomaten, spraakassistenten, IoT-apparaten enzovoort.

Met het **code-gebaseerde ervaring** vermogen, kunt u binnenkomende ervaringen bepalen gebruikend een eenvoudige en intuïtieve niet visuele redacteur. Hiermee kunt u specifieke elementen invoegen en bewerken op afzonderlijke en meer gedetailleerde locaties van uw apps of webpagina&#39;s, ongeacht het type toepassing dat u hebt, in plaats van wijzigingen toe te passen op de gehele inhoud.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>De specifieke aanbevelingen voor code-gebaseerde ervaringen zijn gedetailleerd op [ deze pagina ](code-based-prerequisites.md).


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
<a href="code-based-configuration.md">
<img alt="Validatie" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong> op code-Gebaseerde kanaalconfiguratie </strong></a>
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
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ een gebruiksgeval van begin tot eind dat toont hoe te om inhoudsexperimenten te gebruiken om besluiten met het op code-gebaseerde ervaringskanaal te vergelijken is presentend in [ deze sectie ](../experience-decisioning/experience-decisioning-uc.md).

## Wanneer moet u op code gebaseerde versus andere kanalen gebruiken? {#code-based-vs-other-channels}

### Codegebaseerde versus andere kanalen

Wanneer moet u het op code gebaseerde kanaal gebruiken in plaats van de andere [!DNL Journey Optimizer] kanalen?

* U kunt het gebruiken van code-gebaseerde ervaringen overwegen wanneer uw digitaal bezit niet door Webbrowser of een mobiele app - gevallen wordt betreden waarin u waarschijnlijk beter het [!DNL Journey Optimizer] [ Webkanaal ](../web/get-started-web.md){target="_blank"} of [!DNL Journey Optimizer] [ in-app overseinen ](../in-app/get-started-in-app.md){target="_blank"} kanaal kunt gebruiken.

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* U kunt het op code gebaseerde kanaal als alternatief voor het [!DNL Journey Optimizer] web of in-app kanalen gebruiken voor het geval u een API-gebaseerde, headless of server-side implementatie hebt.

* U kunt het op code gebaseerde kanaal ook gebruiken op native mobiele toepassingen als alternatief voor het kanaal in de app als u de inhoud in uw native app wilt wijzigen in plaats van modellen, popups of overlays weer te geven.

### Codegebaseerd versus webkanaal {#code-based-vs-web}

Als u zaken voor webgebruik wilt uitvoeren, kunt u het webkanaal of de ervaring op basis van code gebruiken, maar afhankelijk van uw context is een van beide geschikter. De belangrijkste verschillen worden hieronder vermeld zodat kunt u een weloverwogen besluit nemen over wat te gebruiken, en wanneer.

**Web**

* Bewerk uw inhoud gebruikend de [&#128279;](../web/web-visual-editor.md){target="_blank"} visuele redacteur van de 0&rbrace; Webontwerper &lbrace;of de Web [ niet-visuele redacteur ](../web/web-non-visual-editor.md).
* U hebt het [ Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}  nodig - een cliënt-zijimplementatie.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* Met het webkanaal kunt u alles op de pagina wijzigen en hebt u een vooraf gedefinieerde lijst met handelingen die u kunt gebruiken om wijzigingen aan te brengen. [Meer informatie](../web/web-visual-editor.md){target="_blank"}
* Het is eenvoudig om in te stellen en snel te gaan.
* Het is gericht op marketer-persona.

**op code-gebaseerde ervaring**

* Bewerk uw inhoud gebruikend de [ verpersoonlijkingsredacteur ](create-code-based.md#edit-code).
* U hebt of het [ Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}  nodig - cliënt-zijimplementatie, of de [ Server API van Edge Network van AEP ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"}  - server-zijimplementatie.
* De op code-gebaseerde ervaring vereist vorige ontwikkelingswerk aan uw implementatie om ervoor te zorgen dat uw toepassingen de inhoud kunnen interpreteren en leveren die op de rand door [!DNL Journey Optimizer] voor deze plaatsen wordt gepubliceerd. [Meer informatie](code-based-surface.md)
* Het vereist meer planning en het kan slechts de dingen veranderen die de ontwikkelaars specificeren. Daarom is het essentieel om de componenten (huisbanner, heldenbeeld, menubalk, enz.) op de toepassingen te identificeren die voor verpersoonlijking of het testen moeten worden gewijzigd, en met uw ontwikkelingsteam te werken om de implementatie te bouwen nodig voor het behandelen van deze veranderingen.
* U kunt hiermee JSON-code-inhoud gebruiken.
* Het is gericht op ontwikkelaars-persoonlijkheid.

## Werking {#how-it-works}

>[!CAUTION]
>
>Deze functie is bedoeld voor ontwikkelaars en/of ervaren gebruikers. Het kan door marketers met sommige code-schrijvende vaardigheden worden gebruikt, zolang de kanaalconfiguraties en aanvankelijke opstelling door uw ontwikkelingsteam worden behandeld.

Als u de inhoud wilt bewerken met de ervaringsfunctie van [!DNL Journey Optimizer] op code gebaseerde, pagina&#39;s of apps moeten van instrumenten worden voorzien. Om dit te doen, moet u vóór de specifieke individuele plaatsen (genoemd &quot;[ oppervlakten ](code-based-surface.md)&quot;verklaren waar u inhoud wilt opnemen of vervangen.

>[!NOTE]
>
>Momenteel kan de inhoud die aan een configuratie is gekoppeld, alleen HTML of JSON zijn.

De belangrijkste stappen om een op code-gebaseerde ervaring tot stand te brengen en te leveren zijn als volgt.

1. Zorg ervoor dat u de kanaalspecifieke voorwaarden volgt. [Meer informatie](code-based-prerequisites.md)

1. Bepaal a [ oppervlakte ](code-based-surface.md#surface-definition) in uw toepassingsimplementatie, die fundamenteel de plaats is waar u uw ervaring wilt toevoegen.

1. Maak een op code gebaseerde kanaalconfiguratie die naar die locatie verwijst. [ leer hoe ](code-based-configuration.md#create-code-based-configuration)

1. Maak een reis of campagne in [!DNL Journey Optimizer] met deze configuratie. [ leer hoe ](create-code-based.md#create-code-based-campaign)

1. Stel een ervaring samen door inhoud voor de geselecteerde configuratie te specificeren gebruikend de [!DNL Journey Optimizer] verpersoonlijkingsredacteur. [ leer hoe ](create-code-based.md#edit-code)

1. Test uw op code gebaseerde ervaring. [ leer hoe ](test-code-based.md)

1. Publiceer het. [ leer hoe ](publish-code-based.md)

1. Als uw op code gebaseerde ervaringstraject of -campagne live is, moet de app- of paginaimplementatie die om inhoud voor het oppervlak vraagt, aanwezig zijn om de inhoud op te halen en weer te geven.

   >[!INFO]
   >
   >Om dit te verzekeren, maakt uw app implementatieteam expliciete API of SDK vraag om inhoud voor de oppervlakte te halen die in de op code-gebaseerde configuratie wordt bepaald, zoals &quot;Banner Tekst&quot;of &quot;het Lijn van Aanbevelingen 1&quot;, of niet-UI-verwante besluitvormingspunten in een toepassing, zoals &quot;onderzoeksalgoritmeparameters&quot;. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Meer informatie](code-based-implementation-samples.md)

