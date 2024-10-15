---
title: Voorwaarden voor webkanalen
description: Volg de voorwaarden op deze pagina om webpagina's te kunnen openen en schrijven in de Journey Optimizer-gebruikersinterface
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: c5308cfdb237fcf563886db1dfca257d23bb4449
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 0%

---

# Vereisten en geleiders {#web-prerequisites}

Als u webpagina&#39;s wilt openen en schrijven in de gebruikersinterface van [!DNL Journey Optimizer] , moet u aan de volgende voorwaarden voldoen:

* Als u wijzigingen aan uw website wilt toevoegen, moet u over een specifieke implementatie beschikken. [Meer informatie](#implementation-prerequisites)

* Als u toegang wilt tot de [!DNL Journey Optimizer] -webontwerper, moet een specifieke Google Chrome-browserextensie zijn geïnstalleerd. [Meer informatie](#visual-authoring-prerequisites)

* Voor de Webervaring die correct moet worden geleverd, zorg ervoor u de hier gedetailleerde montages van Adobe Experience Platform [ ](#delivery-prerequisites) bepaalt.

>[!IMPORTANT]
>
>[!DNL Journey Optimizer] webcampagnes zijn gericht op nieuwe profielen die nog niet eerder zijn ingeschakeld op andere kanalen. Hierdoor neemt het totale aantal aanspreekbare profielen toe. Dit kan kosten met zich meebrengen als het contractueel aantal aangeschafte profielen wordt overschreden. De metriek van de vergunning voor elk pakket is vermeld op de [ de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html) {target="_blank"} pagina. U kunt het aantal in dienst komende profielen in het [ dashboard van het vergunningsgebruik ](../audience/license-usage.md) controleren.
>

## Voorwaarden voor implementatie {#implementation-prerequisites}

Er worden twee typen implementaties ondersteund waarmee u webkanaalcampagnes kunt ontwerpen en leveren op uw westeigenschappen:

* Cliënt-kant slechts - om wijzigingen aan uw website toe te voegen, moet u [ SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html) uitvoeren {target="_blank"} op uw website.

  >[!NOTE]
  >
  >Zorg ervoor uw [ versie van SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/release-notes) {target="_blank"} 2.16 of hierboven is.

* Hybride wijze - u kunt de [ API van de Server van de Edge Network AEP ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) gebruiken {target="_blank"} om voor verpersoonlijkings server-kant te verzoeken; de reactie wordt verstrekt aan het Web SDK van Adobe Experience Platform om de wijzigingen cliënt-kant terug te geven. Leer meer in de documentatie van de Server API van de Edge Network van Adobe Experience Platform [ ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html) {target="_blank"}. U kunt meer over de hybride wijze te weten komen en sommige implementatiemonsters in [ controleren dit blogpost ](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41) {target="_blank"}.

>[!NOTE]
>
>De server-kant slechts implementatie wordt momenteel niet gesteund met het kanaal van het Web. Als u een server-zij slechts implementatie voor uw Web-pagina&#39;s hebt, kunt u het [ op code-gebaseerde ervaringskanaal ](../code-based/get-started-code-based.md) in plaats daarvan gebruiken.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Visuele ontwerpvereisten {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Om uw Web-pagina&#39;s betrouwbaar in de [!DNL Journey Optimizer] Webontwerper te kunnen openen, auteur en voorproef, moet u de [ Adobe Experience Cloud Visual Editing Helper ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca) {target="_blank"} browser uitbreiding hebben die op uw Webbrowser wordt geïnstalleerd.

>[!CAUTION]
>
>Google Chrome en Microsoft Edge zijn momenteel de enige browsers die ontwerpwebpagina&#39;s in [!DNL Journey Optimizer] ondersteunen.

### De extensie Visuele bewerkingshulp installeren {#install-visual-editing-helper}

Voer de onderstaande stappen uit om de extensie van de browser van de Visual Editing Helper te downloaden en installeren.

1. Open een nieuw tabblad in uw browser (Google Chrome of Microsoft Edge).

1. Ga naar de [ Opslag van het Web van Google Chrome ](https://chrome.google.com/webstore/category/extensions) {target="_blank"}.

1. Als u Microsoft Edge gebruikt, selecteert u **[!UICONTROL Allow extensions from other stores]** op de bovenste banner. Zo kunt u extensies van de Chrome-webwinkel toevoegen aan Microsoft Edge.

1. Onderzoek en navigeer aan [ Adobe Experience Cloud Visuele het Uitgeven Helper ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca) {target="_blank"} browser uitbreiding.

1. Klik op **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]** .

   >[!NOTE]
   >
   >Als u Microsoft Edge gebruikt, wordt de extensie toegevoegd aan Edge, ook al is het label voor de knop **[!UICONTROL Add to Chrome]** .

1. Zorg ervoor de Visuele het Uitgeven Helper browser uitbreiding correct in de toolbar van uw browser wordt toegelaten.

   ![](assets/web-visual-editing-extension-edge.png)

De visuele het Uitgeven van Adobe Experience Cloud Helper wordt nu automatisch toegelaten wanneer een website in [!DNL Journey Optimizer] [ Webontwerper ](edit-web-content.md#work-with-web-designer) aan macht authoring wordt geopend.

De extensie heeft geen voorwaardelijke instellingen en verwerkt alle instellingen automatisch, inclusief de instellingen voor Cookies van SameSite.

>[!NOTE]
>
>Sommige websites kunnen om een van de volgende redenen mogelijk niet betrouwbaar worden geopend in de [!DNL Journey Optimizer] -webontwerper:
>
> * De website heeft een strikt beveiligingsbeleid.
> * De website bevindt zich in een iframe.
> * De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).

### Problemen met laden van website oplossen {#troubleshooting}

Wanneer het gebruiken van de Adobe [!DNL Journey Optimizer] Webontwerper, als u probeert om een website te laden die er niet in slaagt te laden, een berichtvertoningen die erop wijzen dat u de [ Visuele het Uitgeven Browser van de Helper browser uitbreiding ](#install-visual-editing-helper) installeert.

1. Zorg ervoor de Visuele het Uitgeven Helper browser uitbreiding correct geïnstalleerd is.

1. Als de website zich nog steeds onverwacht gedraagt, moet u ervoor zorgen dat cookies van andere leveranciers zijn toegestaan in uw browser. Als dit niet het geval is, kan de webpagina niet worden geladen in de webontwerper van [!DNL Journey Optimizer] .

Voor pagina&#39;s onder verificatie, als de aanmeldingspagina niet kan worden geladen of als u na het aanmelden nog steeds niet bent aangemeld:

1. Meld u eerst aan op een nieuw browsertabblad en navigeer naar de gewenste pagina. Kopieer vervolgens de URL en open deze in de webontwerper van [!DNL Journey Optimizer] .

2. Als u uw website nog steeds niet kunt laden in de [!DNL Journey Optimizer] webontwerper, neemt u contact op met de klantenservice van de Adobe om het probleem te melden. Controleer of u de falende URL opgeeft.

## Leveringsvoorwaarden {#delivery-prerequisites}

De webervaring kan alleen correct worden geleverd als de volgende instellingen zijn gedefinieerd:

* In de [ Gegevensverzameling van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html) {target="_blank"}, zorg ervoor u een gegevensstroom hebt die zoals onder de **[!UICONTROL Adobe Experience Platform]** dienst wordt bepaald u de **[!UICONTROL Adobe Journey Optimizer]** toegelaten optie hebt.

  Dit zorgt ervoor dat de binnenkomende gebeurtenissen van Journey Optimizer correct worden afgehandeld door de Adobe Experience Platform Edge. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) {target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* In [ Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl) {target="_blank"}, zorg ervoor u één toegelaten fusiebeleid met de **[!UICONTROL Active-On-Edge Merge Policy]** optie hebt. Selecteer hiertoe een beleid in het menu Experience Platform **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** . [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure) {target="_blank"}

  Dit samenvoegbeleid wordt door [!DNL Journey Optimizer] binnenkomende kanalen gebruikt om binnenkomende campagnes op de rand correct te activeren en te publiceren. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html) {target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Om de levering van de ervaringen van het Web van Journey Optimizer problemen op te lossen, kunt u de **Edge Delivery** mening binnen **de Verzekering van Adobe Experience Platform** gebruiken. Deze plugin laat u toe om verzoekvraag in detail te inspecteren, te verifiëren of de verwachte randvraag zoals voorzien voorkomt, en profielgegevens, met inbegrip van identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages te onderzoeken. Daarnaast kunt u de activiteiten bekijken waarvoor het verzoek is gekwalificeerd en vaststellen voor welke activiteiten het niet heeft uitgevoerd.

  Het gebruiken van de **insteekmodule van Edge Delivery** helpt u de inzichten verkrijgen nodig om uw binnenkomende implementaties effectief te begrijpen en problemen op te lossen.

  [ Leer meer op de mening van Edge Delivery ](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## Voorwaarden voor rapportage {#experiment-prerequisites}

Om rapportering voor het Webkanaal toe te laten, moet u ervoor zorgen de [ dataset ](../data/get-started-datasets.md) wordt gebruikt in uw Webimplementatie [ datastream ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html) {target="_blank"} is ook inbegrepen in uw rapporteringsconfiguratie die.

Met andere woorden, wanneer het vormen van rapportering, als u een dataset toevoegt die niet in uw Webgegevensstroom aanwezig is, zullen de Webgegevens niet in uw rapporten tonen.

Leer hoe te om datasets voor het melden in [ toe te voegen deze sectie ](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>De dataset wordt gebruikt read-only door het [!DNL Journey Optimizer] rapporteringssysteem en beïnvloedt gegevensinzameling of gegevensopname niet.

Als u **niet** gebruikend de volgende vooraf bepaalde [ gebiedsgroepen ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group) {target="_blank"} voor uw datasetschema bent: `AEP Web SDK ExperienceEvent` en `Consumer Experience Event` (zoals bepaald in [ deze pagina ](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups) {target="_blank"}), zorg ervoor om de volgende gebiedsgroepen toe te voegen: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, en `Web Details`. Deze zijn nodig voor het [!DNL Journey Optimizer] -inhoudexperiment. Tijdens het bijhouden van de experimenten en behandelingen waaraan elk profiel deelneemt.

[Meer informatie over rapportconfiguratie](../reports/reporting-configuration.md)

>[!NOTE]
>
>Het toevoegen van deze veldgroepen heeft geen invloed op de normale gegevensverzameling. Het is alleen additief voor de pagina&#39;s waarop een experiment wordt uitgevoerd, waarbij alle andere tracking ongewijzigd blijft.

## Gemarkeerde domeinen voor elementen {#branded-domains-for-assets}

Wanneer het ontwerpen van Webervaringen, als u inhoud toevoegt die uit de [ Adobe Experience Manager Assets ](../content-management/assets.md) bibliotheek komt, moet u opstelling subdomain die zal worden gebruikt om deze inhoud te publiceren. [Meer informatie](web-delegated-subdomains.md)
