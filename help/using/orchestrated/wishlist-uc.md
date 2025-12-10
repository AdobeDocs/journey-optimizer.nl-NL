---
solution: Journey Optimizer
product: journey optimizer
title: Updates van wenslijstitems verzenden
description: Updates van wenslijstitems verzenden
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Updates van wenslijstitems verzenden {#wishist-uc}

>[!BEGINSHADEBOX]

Terwijl dit voorbeeld het schema van a **Wishlist** gebruikt, is de zelfde methode op om het even welke entiteit met een één-aan-vele verhouding aan **Ontvangers** zoals **Aankopen**, **Abonnementen**, of om het even welk douaneschema van toepassing waarin elke ontvanger veelvoudige bijbehorende verslagen kan hebben.

**Schema&#39;s nodig voor dit gebruiksgeval:**

* **Ontvangers**: gebruikt als het richten dimensie
* **WishlistItems**: met gebieden: `creationDate`, `product`, `Wishlistid`
* **Product**: met gebieden: `description`, `priceref`, `imageurl`
* **AbandonedCarts** (facultatief): met gebied: `lastmodified`

➡️ [ Leer hoe te om model-gebaseerde schema&#39;s ](gs-schemas.md) te vormen

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Deze georkestreerde campagne richt zich op het opnieuw betreden van bezoekers door hen te herinneren aan producten die aan hun Wishlist worden bewaard. Met Campagne Orchestration definieert u het publiek onder voorwaarden die zijn gebaseerd op de activiteiten van het Wishlist-programma. Zo kunt u bezoekers terugzetten en converteren.

1. Begin door een nieuwe campagne te creëren specifiek gericht op Wishlist re-engagement. Dit zal helpen overseinen op klanten concentreren die koopintentie hebben getoond door punten te bewaren.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Vul uw **montages van de Campagne** in.

1. Voeg een **[!UICONTROL Build audience]** activiteit toe om de groep klanten te identificeren die aan doel op Wishlist gedrag wordt gebaseerd.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Stel een beschrijving **[!UICONTROL Label]** in voor dit publiek en kies **[!UICONTROL Recipients]** als **[!UICONTROL Targeting dimension]** . Klik vervolgens op **[!UICONTROL Continue]** om het publiek te configureren.

1. Klik op **[!UICONTROL Add condition]** om het publiek te verfijnen door de volgende voorwaarde te maken:

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
OF
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Dit publiek is gebaseerd op ontvangers met een Wishlist, bevat items met productafbeeldingen of heeft een verlaten winkelwagentje binnen de gedefinieerde tijdsperiode.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Klik op **[!UICONTROL Calculate]** om het aantal profielen weer te geven dat door deze voorwaarden wordt beïnvloed en op **[!UICONTROL View results]** om de details voor elke voorwaarde te inspecteren en te bevestigen dat het publiek overeenkomt met het doelsegment.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Klik op **[!UICONTROL Confirm]**.

1. Voeg een **[!UICONTROL Enrichment]** activiteit toe om de campagne met **Wishlist** en **productinformatie** te personaliseren.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Klik op **[!UICONTROL Add enrichment data]**.

1. Toegang `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Selecteer hoe de gegevens worden verzameld, in dit geval **[!UICONTROL Collect data]** om de details van de Wishlist voor uw publiek te verzamelen.

1. Kies het aantal regels dat u wilt ophalen. Door gebrek, worden drie punten per Wishlist teruggewonnen, maar dit kan afhankelijk van campagnebehoeften worden aangepast meer of minder producten te benadrukken.

1. Klik op **[!UICONTROL Add attribute]** om de volgende drie kenmerken te maken:

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Dit verrijkt het bericht met gedetailleerde productinformatie om omzettingen te drijven.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Voeg een e-mailactiviteit toe om een individueel gepersonaliseerd re-betrokkenheidsbericht voor elke klant te creëren. Klik op **[!UICONTROL Edit content]** om uw inhoud te ontwerpen.

   ➡️ [ Leer meer op e-mailverpersoonlijking ](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Nadat u de e-mail hebt voltooid, slaat u de campagne op en voert u deze uit in de conceptmodus door op **[!UICONTROL Start]** te klikken vanuit de georkestreerde campagne.

1. Nadat u de conceptmodus hebt gestart, geeft u een voorvertoning van de doelgroep weer met details van de lijst met aarzelaars.

   Klik voor meer informatie op een uitvoerresultaat en selecteer **[!UICONTROL Preview results]** .

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Nadat de campagne is gestart, kunnen we onze rapporten verkennen, die ons een robuuste reeks gegevens en KPI&#39;s geven over hoe onze campagne presteert.

➡️ [ Leer meer bij het melden ](../reports/campaign-global-report-cja.md)
