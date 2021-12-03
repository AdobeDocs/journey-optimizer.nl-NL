---
title: Een abonnementenlijst maken
description: Meer informatie over het instellen van een abonnementenlijst in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Een abonnementenlijst maken {#create-subscription-list}

## Wat is een abonnementenlijst?

Een abonnementsdienst heeft betrekking op marketinggoederen en -diensten die worden geleverd aan klanten die ervoor hebben gekozen communicatie over een specifiek onderwerp/evenement/belang/enz. te ontvangen. doorlopend. In [!DNL Journey Optimizer], worden deze opted-in klanten verzameld in een abonnementenlijst.

Een abonnementenservice kan:

* een nieuwsbrief, bijvoorbeeld &quot;Running series&quot;
* een evenement, bijvoorbeeld &quot;Top 2021&quot;
* een webinar, bijvoorbeeld &quot;Meer weten over crypto&quot;
* een belang bij een bepaald product/een bepaalde sport/dienst/enz., bijvoorbeeld &quot;interesse om in de komende twaalf maanden een huis te kopen&quot;
* een voorkeur voor het melden van nieuwe nummers, bijvoorbeeld &quot;Ontvang meldingen over nieuwe nummers via e-mail&quot;

De profielen kunnen aan een abonnementenlijst door worden toegevoegd [landingspagina](create-lp.md). Een voorbeeld wordt weergegeven in [deze sectie](get-started-lp.md#subscription-to-a-service).

## Een abonnementenlijst definiëren {#define-subscription-list}

Voer de onderstaande stappen uit om een abonnementenlijst te maken.

1. Selecteer **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. Klik in de abonnementenlijst op **[!UICONTROL Create subscription]** lijst.

   ![](../assets/lp_create-subscription-list.png)

1. Voeg een naam en een beschrijving toe. Deze velden zijn verplicht.

1. U kunt een begin- en einddatum definiëren.

   ![](../assets/lp_subscription-list-dates.png)

1. Klik op **[!UICONTROL Save]**.

In de lijst worden alle gemaakte abonnementenlijsten weergegeven. U kunt ze filteren op basis van de aanmaakdatum of wijzigingsdatum.

![](../assets/lp_subscription-filters.png)

De mogelijke status is als volgt:

* **[!UICONTROL Not started]**: U hebt een begindatum gedefinieerd die later is dan de huidige dag. De profielen die op deze lijst zijn geabonneerd, ontvangen nog geen mededelingen met betrekking tot deze abonnementenlijst.
* **[!UICONTROL Live]**: De huidige dag bestaat uit de begindatum en einddatum van de abonnementenlijst, of u hebt geen begin-/einddatum gedefinieerd, wat betekent dat de abonnementenlijst altijd live is.
* **[!UICONTROL Expired]**: De einddatum wordt doorgegeven. De abonnementenlijst is niet meer geldig. Profielen die op deze lijst zijn geabonneerd, ontvangen geen andere berichten over deze abonnementenlijst.

Nadat u de abonnementenlijst hebt gemaakt, kunt u deze in een bestemmingspagina gebruiken, zodat de profielen zich via een formulier kunnen aanmelden en aan de lijst kunnen worden toegevoegd. [Meer informatie](design-lp.md)

U kunt abonnementenlijsten als segmenten ook gebruiken wanneer het bouwen van reizen en verpersoonlijking.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->