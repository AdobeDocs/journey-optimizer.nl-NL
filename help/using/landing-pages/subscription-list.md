---
solution: Journey Optimizer
product: journey optimizer
title: Een lidmaatschapslijst maken
description: Meer informatie over het instellen van een abonnementenlijst in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: landen, landingspagina, lijst, abonnement, service
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: b7685798cec415c8a97992ddacf8f0ebcb393107
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 5%

---

# Abonnementenlijsten {#create-subscription-list}

## Wat is een abonnementenlijst? {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Een abonnementenlijst instellen"
>abstract="Een abonnementenlijst maken om profielen te verzamelen die zich hebben aangemeld voor het ontvangen van communicatie over een specifiek onderwerp of een specifieke gebeurtenis. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html#define-subscription-list" text="Een lidmaatschapslijst maken"

Een abonnementsdienst heeft betrekking op marketinggoederen en -diensten die worden geleverd aan klanten die ervoor hebben gekozen communicatie over een specifiek onderwerp/evenement/belang/enz. te ontvangen. doorlopend. In [!DNL Journey Optimizer], worden deze opted-in klanten verzameld in een abonnementenlijst.

Een abonnementenservice kan:

* een nieuwsbrief, bijvoorbeeld: &quot;Running series&quot;
* een evenement , bijvoorbeeld : &quot; top 2021 &quot;
* een webinar, bijvoorbeeld: &quot;Meer informatie over crypto&quot;
* een belang bij een bepaald product/een bepaalde sport/dienst/enz., bijvoorbeeld: &quot;Interessant om in de komende twaalf maanden een huis te kopen&quot;
* een voorkeur voor het melden van nieuwe nummers, bijvoorbeeld: &quot;Ontvang nieuwe berichten over nummers via e-mail&quot;

De profielen kunnen aan een abonnementenlijst door worden toegevoegd [landingspagina](create-lp.md). Een voorbeeld wordt weergegeven in [deze sectie](lp-use-cases.md#subscription-to-a-service).

## Een lidmaatschapslijst maken {#define-subscription-list}

Voer de onderstaande stappen uit om een abonnementenlijst te maken.

1. Als u de abonnementenlijsten wilt openen, selecteert u **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](assets/lp_subscription-lists.png)

1. Selecteer de knop **[!UICONTROL Create subscription list]**.

   ![](assets/lp_create-subscription-list.png)

1. Voeg een titel en een beschrijving toe. Deze velden zijn verplicht.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >U kunt momenteel geen spatiëring gebruiken of een naam invoeren die al bestaat voor een andere abonnementenlijst in het dialoogvenster **[!UICONTROL Title]** veld.

1. U kunt een begin- en einddatum definiëren.

   ![](assets/lp_subscription-list-dates.png)

1. Adobe Experience Platform-tags selecteren of maken vanuit het menu **[!UICONTROL Tags]** veld om uw landingspagina te categoriseren voor een betere zoekopdracht. [Meer informatie](../start/search-filter-categorize.md#tags)

1. Klik op **[!UICONTROL Save]**.

In de lijst worden alle gemaakte abonnementenlijsten weergegeven. U kunt ze filteren op basis van de aanmaakdatum of wijzigingsdatum en hun status.

![](assets/lp_subscription-filters.png)

De mogelijke statussen zijn als volgt:

* **[!UICONTROL Not started]**: U hebt een begindatum gedefinieerd die later is dan de huidige dag. De geabonneerde profielen ontvangen nog geen communicatie met betrekking tot deze abonnementenlijst.
* **[!UICONTROL Live]**: De huidige dag bestaat uit de begindatum en einddatum van de abonnementenlijst, of u hebt geen begin-/einddatum gedefinieerd, wat betekent dat de abonnementenlijst altijd live is.
* **[!UICONTROL Expired]**: De einddatum wordt doorgegeven, zodat de abonnementenlijst niet meer geldig is. Voor elk geabonneerd profiel worden geen berichten meer ontvangen die betrekking hebben op deze abonnementenlijst.

Zodra de abonnementenlijst wordt gecreeerd, kunt u het in een het landen pagina gebruiken. De profielen die zich aanmelden via het formulier voor de landingspagina worden toegevoegd aan de lijst. [Meer informatie](design-lp.md)

U kunt abonnementenlijsten ook als publiek gebruiken wanneer [trajecten](../building-journeys/journey-gs.md#jo-build) en personalisatie toevoegen.

>[!NOTE]
>
>U kunt de gevolgen van uw abonnementenlijst controleren door specifieke rapporten. [Meer informatie](../reports/subscription-report-live.md)
