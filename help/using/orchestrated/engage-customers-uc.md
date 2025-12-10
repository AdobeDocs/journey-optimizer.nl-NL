---
solution: Journey Optimizer
product: journey optimizer
title: Klanten inschakelen door te bladeren
description: Klanten inschakelen door te bladeren
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Klanten inschakelen door te bladeren {#engage-customers-uc}

>[!BEGINSHADEBOX]

Merk op dat dit gebruiksgeval met een publiek begint dat reeds in Experience Platform bestaat, specifiek, een publiek in real time van het Webgedrag dat het doorbladeren activiteit verzamelt aangezien het voorkomt. [&#x200B; leer meer in Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Schema&#39;s nodig voor dit gebruiksgeval:**

* **Ontvangers**: gebruikt als het richten afmeting, met gebieden: `email`, `churnprop`
* **Wishlist**: met gebieden: `description`, `priceref`, `imageurl`

➡️ [&#x200B; Leer hoe te om model-gebaseerde schema&#39;s &#x200B;](gs-schemas.md) te vormen

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Deze campagne richt klanten die de categorie van oefenmateriaal hebben doorzocht. Het publiek wordt gededupliceerd en gesegmenteerd door het kernorisico, hoe waarschijnlijk iemand zal stoppen met het aantrekken of kopen.

Klanten met een hoog risico worden verzameld in een afzonderlijk nieuw publiek dat later zal worden gebruikt voor een specifieke communicatie, terwijl klanten met een laag en middelmatig risico een meerstapsreis doormaken met gepersonaliseerde e-mails en follow-ups.

1. Begin door vestiging een nieuwe campagne specifiek gericht op **Wishlist re-engagement**. Dit verzekert uw overseinen zich op klanten concentreren die reeds aankoopintentie door producten aan hun verlanglijst hebben getoond te bewaren.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Vul de **[!UICONTROL Campaign Settings]** -code in, zoals de naam, beschrijving, begin- en einddatum en relevante tags.

1. Voeg een **[!UICONTROL Read audience]** activiteit toe om een vooraf bepaald publiek van Adobe Experience Platform, hier, klanten te selecteren die de categorie van oefenmateriaal op uw website hebben doorzocht.

   Ontvangers worden geïdentificeerd met hun e-mailadressen die in het veld **[!UICONTROL Entity]** zijn geselecteerd.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Voeg een **[!UICONTROL Deduplication]** activiteit toe om dubbele e-mailadressen uit uw publiek te verwijderen, ervoor zorgend dat elke klant slechts één bericht ontvangt.

1. Klik op **[!UICONTROL Add attribute]** en selecteer E-mail als kenmerk voor deduplicatie.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Voeg vervolgens een **[!UICONTROL Split]** -activiteit toe om klanten te segmenteren op basis van de waarschijnlijkheid dat ze naar verwachting zullen klonen, zodat u persoonlijke ervaringen kunt aanbieden die op maat zijn gemaakt voor elke klantengroep.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Klik op **[!UICONTROL Add segment]** om drie groepen te maken:

   * Laag risico

   * Medium-risico

   * Hoge risico

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Klik op **[!UICONTROL Create filter]** om de waarschijnlijkheid van de curve voor elke groep te definiëren.

   Gebruik de **redacteur van de Voorwaarde** om de specifieke waarden te plaatsen die het karnenrisico van elke klant bepalen.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Elk segment wordt verschillend behandeld:

   * [Laag/middelgroot risico](#low-medium-risk)
   * [Hoge risico](#high-risk)

1. Nadat uw campagne is getest en klaar is, klikt u op **[!UICONTROL Publish]** om deze actief te maken.

Nadat de campagne is gestart, verkent u het rapporteringsdashboard om prestatiegegevens en belangrijke inzichten te bekijken.

➡️ [&#x200B; Leer meer bij het melden &#x200B;](../reports/campaign-global-report-cja.md)

## Hoogrisicosegmenten {#high-risk}

Voor klanten die worden geïdentificeerd als met een hoog risico op een hoorn, creeer een specifiek publiekssegment. Dit publiek wordt later gebruikt voor afzonderlijke, gerichte communicatie.

1. Voeg een **[!UICONTROL Save Audience]** toe.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Voeg a **[!UICONTROL Label]** aan uw publiek toe en kies **[!UICONTROL Profile mapping field]**, hier **ontvangers-e-mail**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Dit publiek wordt dan bewaard aan Experience Cloud, waar het later voor een specifieke gerichte campagne kan worden gebruikt.

## Low/medium-risicosegmenten {#low-medium-risk}

Voor klanten met een laag en middelgroot churn-risico, een meerfasencampagne opzetten om de betrokkenheid te versterken:

1. Combineer zowel Laag als Medium risico&#39;s met een **[!UICONTROL Union]** activiteit.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Voeg een **[!UICONTROL Enrichment]** activiteit toe om de campagne met Wishlist en productinformatie te personaliseren.

1. Klik op **[!UICONTROL Add attribute]** om de volgende drie kenmerken te maken:

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Dit verrijkt de boodschap met gedetailleerde informatie over wenslijsten.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Maak een nieuw publiek voor heroriëntering op basis van betrokkenheid bij e-mails.

   Hier maken we een publiek dat is gebaseerd op gebeurtenissen met een klik per e-mail om alle personen die met een eerder verzonden e-mail hebben gewerkt, opnieuw als doel in te stellen. Meer specifiek is het doel van een klik op een koppeling in dat bericht.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Verdeel de betrokkenheid gelijkmatig om een follow-up via SMS of push-berichten te verzenden om conversies aan te moedigen.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Creeer de berichtinhoud voor elk kanaal met inbegrip van profielattributen, zoals de naam van de ontvanger, samen met verrijkingsgegevens zoals de punten van de Wijze lijst, om elk bericht te personaliseren.

   ![](assets/uc-interest-13.png){zoomable="yes"}
