---
title: Een abonnementenlijst maken
description: Meer informatie over het instellen van een abonnementenlijst in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 4609b071e6011bb2c28156b9638f40b7d6f29249
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 2%

---

# Abonnementenlijsten {#create-subscription-list}

## Wat is een abonnementenlijst? {#subscription-list-definition}

Een abonnementsdienst heeft betrekking op marketinggoederen en -diensten die worden geleverd aan klanten die ervoor hebben gekozen communicatie over een specifiek onderwerp/evenement/belang/enz. te ontvangen. doorlopend. In [!DNL Journey Optimizer], worden deze opted-in klanten verzameld in een abonnementenlijst.

Een abonnementenservice kan:

* een nieuwsbrief , bijvoorbeeld : &quot;Running series&quot;
* een gebeurtenis, bijvoorbeeld: &quot;Top 2021&quot;
* een webinar, bijvoorbeeld: &quot;Meer informatie over crypto&quot;
* een belang bij een bepaald product/sport/dienst/enz., bijvoorbeeld: &quot;Wil in de komende 12 maanden een huis kopen&quot;
* een voorkeur voor de wijze van kennisgeving, bijvoorbeeld: &quot;Ontvang nieuwe berichten over nummers op e-mail&quot;

De profielen kunnen aan een abonnementenlijst door worden toegevoegd [landingspagina](create-lp.md). Een voorbeeld wordt weergegeven in [deze sectie](lp-use-cases.md#subscription-to-a-service).

## Een abonnementenlijst definiëren {#define-subscription-list}

Voer de onderstaande stappen uit om een abonnementenlijst te maken.

1. Selecteer **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Selecteer de knop **[!UICONTROL Create subscription list]**.

   ![](../assets/lp_create-subscription-list.png)

1. Voeg een naam en een beschrijving toe. Deze velden zijn verplicht.

1. U kunt een begin- en einddatum definiëren.

   ![](../assets/lp_subscription-list-dates.png)

1. Klik op **[!UICONTROL Save]**.

In de lijst worden alle gemaakte abonnementenlijsten weergegeven. U kunt ze filteren op basis van de aanmaakdatum of wijzigingsdatum en hun status.

![](../assets/lp_subscription-filters.png)

De mogelijke status is als volgt:

* **[!UICONTROL Not started]**: U hebt een begindatum gedefinieerd die later is dan de huidige dag. De geabonneerde profielen ontvangen nog geen communicatie met betrekking tot deze abonnementenlijst.
* **[!UICONTROL Live]**: De huidige dag bestaat uit de begindatum en einddatum van de abonnementenlijst, of u hebt geen begin-/einddatum gedefinieerd, wat betekent dat de abonnementenlijst altijd live is.
* **[!UICONTROL Expired]**: De einddatum wordt overgegaan, zodat is de abonnementenlijst niet meer geldig. Voor elk geabonneerd profiel worden geen berichten meer ontvangen die betrekking hebben op deze abonnementenlijst.

Zodra de abonnementenlijst wordt gecreeerd, kunt u het in een het landen pagina gebruiken. De profielen die zich aanmelden via het formulier voor de landingspagina worden toegevoegd aan de lijst. [Meer informatie](design-lp.md)

U kunt abonnementlijsten ook als segmenten gebruiken wanneer [trajecten](../building-journeys/journey-gs.md#jo-build) en personalisatie toevoegen.

>[!NOTE]
>
>U kunt de gevolgen van uw abonnementenlijst controleren door specifieke rapporten. [Meer informatie](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
