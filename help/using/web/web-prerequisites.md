---
title: Voorwaarden voor webkanalen
description: Volg de voorwaarden op deze pagina om webpagina's te kunnen openen en schrijven in de Journey Optimizer-gebruikersinterface
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 2%

---

# Vereisten en geleiders {#web-prerequisites}

Webpagina&#39;s openen en ontwerpen in het dialoogvenster [!DNL Journey Optimizer] gebruikersinterface, volg de volgende voorwaarden:

* Als u wijzigingen aan uw website wilt toevoegen, moet u over een specifieke implementatie beschikken. [Meer informatie](#implementation-prerequisites)

* Als u toegang wilt krijgen tot [!DNL Journey Optimizer] webontwerper heeft een specifieke Google Chrome-browserextensie geïnstalleerd. [Meer informatie](#visual-authoring-prerequesites)

* Zorg ervoor dat u de gedetailleerde Adobe Experience Platform-instellingen definieert voor een correcte webervaring [hier](#delivery-prerequisites).

## Let op: {#caution-notes-web}

* Momenteel in [!DNL Journey Optimizer] u kunt alleen webervaringen maken in **campagnes**. [Meer informatie](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] webcampagnes zijn gericht op nieuwe profielen die nog niet eerder zijn ingeschakeld op andere kanalen. Hierdoor wordt het totale aantal aanspreekbare profielen verhoogd. Dit kan kosten met zich meebrengen als het contractuele aantal aanschafbare profielen dat u hebt aangeschaft, wordt overschreden. De licentiemetriek voor elk pakket wordt vermeld op het tabblad [Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html) pagina.


>[!AVAILABILITY]
>
>Het webkanaal is momenteel niet beschikbaar voor organisaties die de add-on Adobe Healthcare Shield-aanbieding hebben aangeschaft.
>

## Voorwaarden voor implementatie {#implementation-prerequisites}

Momenteel worden twee typen implementaties ondersteund om het ontwerpen en leveren van webkanaalcampagnes op uw wegeigenschappen mogelijk te maken:

* Alleen client - Als u wijzigingen aan uw website wilt toevoegen, moet u het [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} op uw website.

* Hybride modus - U kunt de opdracht [AEP Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>De implementatie van alleen de server wordt momenteel niet ondersteund.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Visuele ontwerpvereisten {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Als u uw webpagina&#39;s op betrouwbare wijze wilt openen, ontwerpen en voorvertonen in het dialoogvenster [!DNL Journey Optimizer] webontwerper moet de [Helper voor Adobe Experience Cloud Visual Editing](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensie van de browser geïnstalleerd op uw webbrowser.

>[!CAUTION]
>
>Google Chrome en Microsoft Edge zijn momenteel de enige browsers die ontwerpwebpagina&#39;s ondersteunen in [!DNL Journey Optimizer].

### De extensie Visuele bewerkingshulp installeren {#install-visual-editing-helper}

Voer de onderstaande stappen uit om de extensie van de browser van de Visual Editing Helper te downloaden en installeren.

1. Open een nieuw tabblad in uw browser (Google Chrome of Microsoft Edge).

1. Ga naar de [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Als u Microsoft Edge gebruikt, selecteert u **[!UICONTROL Allow extensions from other stores]** op de bovenste banner. Zo kunt u extensies van de Chrome Web Store toevoegen aan Microsoft Edge.

1. Zoeken en naar de [Helper voor Adobe Experience Cloud Visual Editing](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} browserextensie.

1. Klik op **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.

   >[!NOTE]
   >
   >Als u Microsoft Edge gebruikt, wordt de extensie toegevoegd aan Edge, ook al is het label van de knop **[!UICONTROL Add to Chrome]**.

1. Zorg ervoor de Visuele het Uitgeven Helper browser uitbreiding correct in de toolbar van uw browser wordt toegelaten.

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

De Adobe Experience Cloud Visual Editing Helper wordt nu automatisch ingeschakeld wanneer een website wordt geopend in het dialoogvenster [!DNL Journey Optimizer] webontwerper wil creatieve functies uitoefenen.

De extensie heeft geen voorwaardelijke instellingen en verwerkt alle instellingen automatisch, inclusief de instellingen voor Cookies van SameSite.

>[!NOTE]
>
>Sommige websites kunnen niet betrouwbaar worden geopend in de [!DNL Journey Optimizer] webontwerper heeft een van de volgende redenen:
>
> * De website heeft een strikt beveiligingsbeleid.
> * De website bevindt zich in een iframe.
> * De QA- of werkgebiedsite van de klant is niet beschikbaar voor de buitenwereld (de site is intern).

### Problemen met laden van website oplossen {#troubleshooting}

Bij gebruik van de Adobe [!DNL Journey Optimizer] webontwerper, als u probeert een website te laden die niet kan worden geladen, wordt een bericht weergegeven waarin wordt gesuggereerd dat u de [Visuele bewerkingshulpprogramma voor browsers](#install-visual-editing-helper).

Als de Visual Editing Helper browser uitbreiding correct geïnstalleerd is, maar de website nog niet laadt of zich onverwacht gedraagt, is een potentiële moeilijke situatie om uw website in browser te openen en koekjes goed te keuren alvorens het in te proberen te laden in browser [!DNL Journey Optimizer] webontwerper.

Voor pagina&#39;s onder verificatie, als de aanmeldingspagina niet kan worden geladen of als u na het aanmelden nog steeds niet bent aangemeld:

* Probeer u eerst aan te melden op een nieuw browsertabblad en navigeer naar de gewenste pagina. Kopieer vervolgens de URL en open deze in het dialoogvenster [!DNL Journey Optimizer] webontwerper.

* Als u uw website nog steeds niet kunt laden in het dialoogvenster [!DNL Journey Optimizer] Webontwerper, contacteer de Zorg van de Klant van Adobe om het probleem te melden, ervoor zorgt u het falende URL specificeert.

## Leveringsvoorwaarden {#delivery-prerequisites}

De webervaring kan alleen correct worden geleverd als de volgende instellingen zijn gedefinieerd:

* In de [Adobe Experience Platform-gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}moet u ervoor zorgen dat er een gegevensstroom is gedefinieerd, zoals onder de **[!UICONTROL Adobe Experience Platform]** de dienst u hebt **[!UICONTROL Adobe Journey Optimizer]** optie ingeschakeld.

  Dit zorgt ervoor dat de inkomende Journey Optimizer-gebeurtenissen correct worden afgehandeld door de Adobe Experience Platform Edge. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Dit samenvoegbeleid wordt gebruikt door [!DNL Journey Optimizer] binnenkomende kanalen om binnenkomende campagnes op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## Gemarkeerde domeinen voor elementen {#branded-domains-for-assets}

Als u tijdens het ontwerpen van een webversie inhoud toevoegt die afkomstig is van de [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) moet u het subdomein instellen dat wordt gebruikt om deze inhoud te publiceren. [Meer informatie](web-delegated-subdomains.md)
