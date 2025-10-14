---
title: Voorwaarden voor webkanalen
description: Volg de voorwaarden op deze pagina om webpagina's te kunnen openen en schrijven in de Journey Optimizer-gebruikersinterface
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 7bb8f1dfa6a1538017ac9632bf96a2f7e7b01085
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 1%

---

# Vereisten en geleiders {#web-prerequisites}

Als u webpagina&#39;s wilt openen en schrijven in de gebruikersinterface van [!DNL Journey Optimizer] , moet u aan de volgende voorwaarden voldoen:

* Als u wijzigingen aan uw website wilt toevoegen, moet u over een specifieke implementatie beschikken. [Meer informatie](#implementation-prerequisites)

* Als u toegang wilt tot de [!DNL Journey Optimizer] -webontwerper, moet een specifieke Google Chrome-browserextensie zijn geïnstalleerd. [Meer informatie](#visual-authoring-prerequisites)

* Voor de Webervaring die correct moet worden geleverd, zorg ervoor u de hier gedetailleerde montages van Adobe Experience Platform [&#128279;](#delivery-prerequisites) bepaalt.

* Om rapportering voor het Webkanaal toe te laten, moet u ervoor zorgen de dataset die in uw gegevensstroom van de Webimplementatie wordt gebruikt ook in uw rapporteringsconfiguratie wordt omvat. [Meer informatie](#experiment-prerequisites)

>[!IMPORTANT]
>
>[!DNL Journey Optimizer] webcampagnes zijn gericht op nieuwe profielen die nog niet eerder zijn ingeschakeld op andere kanalen. Hierdoor neemt het totale aantal aanspreekbare profielen toe. Dit kan kosten met zich meebrengen als het contractueel aantal aangeschafte profielen wordt overschreden. De metriek van de vergunning voor elk pakket is vermeld op de [&#x200B; pagina van de Beschrijving van het Product van Journey Optimizer &#x200B;](https://helpx.adobe.com/nl/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. U kunt het aantal in dienst komende profielen in het [&#x200B; dashboard van het vergunningsgebruik &#x200B;](../audience/license-usage.md) controleren.
>

## Voorwaarden voor implementatie {#implementation-prerequisites}

Er worden twee typen implementaties ondersteund waarmee u webkanaalcampagnes kunt ontwerpen en leveren op uw westeigenschappen:

* Cliënt-kant slechts - om wijzigingen aan uw website toe te voegen, moet u [&#x200B; Adobe Experience Platform Web SDK &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=nl-NL){target="_blank"} op uw website uitvoeren.

  >[!NOTE]
  >
  >Zorg ervoor uw [&#x200B; versie van SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/release-notes){target="_blank"} 2.16 of hierboven is.

* Hybride wijze - u kunt de [&#x200B; Server API van AEP Edge Network gebruiken API &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=nl-NL){target="_blank"} om voor verpersoonlijkingsserver-kant te verzoeken; de reactie wordt verstrekt aan SDK van het Web van Adobe Experience Platform om de wijzigingen cliënt-kant terug te geven. Leer meer in de Adobe Experience Platform [&#x200B; API documentatie van de Server van Edge Network &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=nl-NL){target="_blank"}. U kunt meer over de hybride wijze te weten komen en sommige implementatiemonsters in [&#x200B; controleren dit blogpost &#x200B;](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>De server-kant slechts implementatie wordt momenteel niet gesteund met het kanaal van het Web. Als u een server-zij slechts implementatie voor uw Web-pagina&#39;s hebt, kunt u het [&#x200B; op code-gebaseerde ervaringskanaal &#x200B;](../code-based/get-started-code-based.md) in plaats daarvan gebruiken.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=nl-NL){target="_blank"}.-->

## Visuele ontwerpvereisten {#visual-authoring-prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_web_browser_extension"
>title="Een overeenkomende regel voor pagina&#39;s maken"
>abstract="Als u toegang wilt tot de webontwerper van [!DNL Journey Optimizer] , moet u een specifieke browserextensie hebben geïnstalleerd: de Adobe Experience Cloud Visual Editing Helper, die alleen beschikbaar is op Google Chrome of Microsoft Edge."

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Om uw Web-pagina&#39;s betrouwbaar in de [!DNL Journey Optimizer] Webontwerper te kunnen openen, auteur en voorproef, moet u de [&#x200B; Adobe Experience Cloud Visual Editing Helper &#x200B;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} browser uitbreiding hebben die op uw Webbrowser wordt geïnstalleerd.

>[!CAUTION]
>
>Google Chrome en Microsoft Edge zijn momenteel de enige browsers die ontwerpwebpagina&#39;s in [!DNL Journey Optimizer] ondersteunen.

### De extensie Visuele bewerkingshulp installeren {#install-visual-editing-helper}

Voer de onderstaande stappen uit om de extensie van de browser van de Visual Editing Helper te downloaden en installeren.

1. Open een nieuw tabblad in uw browser (Google Chrome of Microsoft Edge).

1. Ga naar de [&#x200B; Opslag van het Web van Google Chrome &#x200B;](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Als u Microsoft Edge gebruikt, selecteert u **[!UICONTROL Allow extensions from other stores]** op de bovenste banner. Zo kunt u extensies van de Chrome-webwinkel toevoegen aan Microsoft Edge.

1. Onderzoek en navigeer aan [&#x200B; Adobe Experience Cloud Visuele het Uitgeven Helper &#x200B;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} browser uitbreiding.

1. Klik op **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]** .

   >[!NOTE]
   >
   >Als u Microsoft Edge gebruikt, wordt de extensie toegevoegd aan Edge, ook al is het label voor de knop **[!UICONTROL Add to Chrome]** .

1. Zorg ervoor de Visuele het Uitgeven Helper browser uitbreiding correct in de toolbar van uw browser wordt toegelaten.

   ![](assets/web-visual-editing-extension-edge.png)

De visuele het Uitgeven van Adobe Experience Cloud Helper wordt nu automatisch toegelaten wanneer een website in [!DNL Journey Optimizer] [&#x200B; Webontwerper &#x200B;](web-visual-editor.md) aan macht authoring wordt geopend.

De extensie heeft geen voorwaardelijke instellingen en verwerkt alle instellingen automatisch, inclusief de instellingen voor Cookies van SameSite.

>[!NOTE]
>
>Sommige websites kunnen om een van de volgende redenen mogelijk niet betrouwbaar worden geopend in de [!DNL Journey Optimizer] -webontwerper:
>
> * De website heeft een strikt beveiligingsbeleid.
> * De website bevindt zich in een iframe.
> * De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).

### Problemen met laden van website oplossen {#troubleshooting}

Wanneer het gebruiken van de het Webontwerper van Adobe [!DNL Journey Optimizer], als u probeert om een website te laden die er niet in slaagt te laden, toont een bericht voorstellend dat u de [&#x200B; Visuele het Uitgeven Browser van de Helper browser uitbreiding &#x200B;](#install-visual-editing-helper) installeert.

1. Zorg ervoor de Visuele het Uitgeven Helper browser uitbreiding correct geïnstalleerd is.

1. Als de website zich nog steeds onverwacht gedraagt, moet u ervoor zorgen dat cookies van andere leveranciers zijn toegestaan in uw browser. Als dit niet het geval is, kan de webpagina niet worden geladen in de webontwerper van [!DNL Journey Optimizer] .

Voor pagina&#39;s onder verificatie, als de aanmeldingspagina niet kan worden geladen of als u na het aanmelden nog steeds niet bent aangemeld:

1. Meld u eerst aan op een nieuw browsertabblad en navigeer naar de gewenste pagina. Kopieer vervolgens de URL en open deze in de webontwerper van [!DNL Journey Optimizer] .

2. Als u uw website nog steeds niet kunt laden in de [!DNL Journey Optimizer] -webontwerper, neemt u contact op met de klantenservice van Adobe om het probleem te melden. Controleer of u de falende URL opgeeft.

## Leveringsvoorwaarden {#delivery-prerequisites}

De webervaring kan alleen correct worden geleverd als de volgende instellingen zijn gedefinieerd:

* In de [&#x200B; Gegevensverzameling van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=nl-NL){target="_blank"}, zorg ervoor u een gegevensstroom hebt die zoals onder de **[!UICONTROL Adobe Experience Platform]** dienst wordt bepaald u de **[!UICONTROL Adobe Journey Optimizer]** toegelaten optie hebt.

  Dit zorgt ervoor dat de binnenkomende gebeurtenissen van Journey Optimizer correct worden afgehandeld door de Adobe Experience Platform Edge. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=nl-NL){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* In [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}, zorg ervoor u één toegelaten fusiebeleid met de **[!UICONTROL Active-On-Edge Merge Policy]** optie hebt. Selecteer hiertoe een beleid in het menu **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=nl-NL#configure){target="_blank"}

  Dit samenvoegbeleid wordt door [!DNL Journey Optimizer] binnenkomende kanalen gebruikt om binnenkomende campagnes op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=nl-NL){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Om de levering van de ervaringen van het Web van Journey Optimizer problemen op te lossen, kunt u de **Edge Delivery** mening binnen **Adobe Experience Platform Assurance** gebruiken. Deze plugin laat u toe om verzoekvraag in detail te inspecteren, te verifiëren of de verwachte randvraag zoals voorzien voorkomt, en profielgegevens, met inbegrip van identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages te onderzoeken. Daarnaast kunt u de activiteiten bekijken waarvoor het verzoek is gekwalificeerd en vaststellen voor welke activiteiten het niet heeft uitgevoerd.

  Het gebruiken van de **insteekmodule van Edge Delivery** helpt u de inzichten verkrijgen nodig om uw binnenkomende implementaties effectief te begrijpen en problemen op te lossen.

  [&#x200B; leer meer over de mening van Edge Delivery &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/assurance/view/edge-delivery)

## Voorwaarden voor rapportage {#experiment-prerequisites}

Om rapportering voor het Webkanaal toe te laten, moet u ervoor zorgen de [&#x200B; dataset &#x200B;](../data/get-started-datasets.md) wordt gebruikt in uw Webimplementatie [&#x200B; datastream &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=nl-NL){target="_blank"} is ook inbegrepen in uw rapporteringsconfiguratie.

Met andere woorden, wanneer het vormen van rapportering, als u een dataset toevoegt die niet in uw Webgegevensstroom aanwezig is, zullen de Webgegevens niet in uw rapporten tonen.

Leer hoe te om datasets voor het melden in [&#x200B; toe te voegen deze sectie &#x200B;](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>De dataset wordt gebruikt read-only door het [!DNL Journey Optimizer] rapporteringssysteem en beïnvloedt gegevensinzameling of gegevensopname niet.

Als u **niet** gebruikend de volgende vooraf bepaalde [&#x200B; gebiedsgroepen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=nl-NL#field-group){target="_blank"} voor uw datasetschema bent: `AEP Web SDK ExperienceEvent` en `Consumer Experience Event` (zoals bepaald op [&#x200B; deze pagina &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html?lang=nl-NL#add-field-groups){target="_blank"}), zorg ervoor om de volgende gebiedsgroepen toe te voegen: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, en `Web Details`. Deze zijn nodig door [!DNL Journey Optimizer] -rapporten, omdat ze bijhouden aan welke campagnes en reizen elk profiel deelneemt.

[Meer informatie over rapportconfiguratie](../reports/reporting-configuration.md)

>[!NOTE]
>
>Het toevoegen van deze veldgroepen heeft geen invloed op de normale gegevensverzameling. Het is alleen additief voor de pagina&#39;s waar een campagne of reis wordt uitgevoerd, waarbij alle andere trackingmogelijkheden ongewijzigd blijven.

## Gemarkeerde domeinen voor elementen {#branded-domains-for-assets}

Wanneer het ontwerpen van Webervaringen, als u inhoud toevoegt die uit de [&#x200B; Adobe Experience Manager Assets &#x200B;](../integrations/assets.md) bibliotheek komt, moet u opstelling subdomain die zal worden gebruikt om deze inhoud te publiceren. [Meer informatie](web-delegated-subdomains.md)
