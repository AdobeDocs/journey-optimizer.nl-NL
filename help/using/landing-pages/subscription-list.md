---
solution: Journey Optimizer
product: journey optimizer
title: Een lidmaatschapslijst maken
description: Meer informatie over het instellen van een abonnementenlijst in Journey Optimizer
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: landen, landingspagina, lijst, abonnement, service
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 1aa2ac109cdbf0ba6af58204926f1cd5add334b0
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 3%

---

# Abonnementenlijsten {#create-subscription-list}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Een abonnementenlijst instellen"
>abstract="Een abonnementenlijst maken om profielen te verzamelen die zich hebben aangemeld voor het ontvangen van communicatie over een specifiek onderwerp of een specifieke gebeurtenis. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/subscription-list.html#define-subscription-list" text="Een lidmaatschapslijst maken"

Een abonnementsdienst heeft betrekking op marketinggoederen en -diensten die worden geleverd aan klanten die ervoor hebben gekozen communicatie over een specifiek onderwerp/evenement/belang/enz. te ontvangen. doorlopend. In [!DNL Journey Optimizer] worden deze gekozen klanten verzameld in een abonnementenlijst.

U kunt een abonnementenservice gebruiken voor:

* een nieuwsbrief, bijvoorbeeld: &quot;Running series&quot;
* een evenement , bijvoorbeeld : &quot; top 2021 &quot;
* een webinar, bijvoorbeeld: &quot;Meer informatie over crypto&quot;
* een belang bij een bepaald product/een bepaalde sport/dienst/enz., bijvoorbeeld: &quot;Interessant om in de komende twaalf maanden een huis te kopen&quot;
* een voorkeur voor het melden van nieuwe nummers, bijvoorbeeld: &quot;Ontvang nieuwe berichten over nummers via e-mail&quot;

De profielen kunnen aan een abonnementenlijst door a [&#x200B; worden toegevoegd landend pagina &#x200B;](create-lp.md). Een voorbeeld wordt voorgesteld in [&#x200B; deze sectie &#x200B;](lp-use-cases.md#subscription-to-a-service).

## Een lidmaatschapslijst maken {#define-subscription-list}

Voer de onderstaande stappen uit om een abonnementenlijst te maken.

1. Selecteer **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]** om de abonnementenlijsten te openen.

   ![](assets/lp_subscription-lists.png)

1. Selecteer de knop **[!UICONTROL Create subscription list]**.

   ![](assets/lp_create-subscription-list.png)

1. Voeg een titel en een beschrijving toe. Deze velden zijn verplicht.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >U kunt momenteel geen spatiëring gebruiken of een naam invoeren die al bestaat voor een andere abonnementenlijst in het veld **[!UICONTROL Title]** .

1. U kunt een begin- en einddatum definiëren.

   ![](assets/lp_subscription-list-dates.png)

1. Selecteer of maak Adobe Experience Platform-tags in het veld **[!UICONTROL Tags]** om uw openingspagina te categoriseren voor een betere zoekopdracht. [Meer informatie](../start/search-filter-categorize.md#tags)

1. Klik op **[!UICONTROL Save]**.

## Abonnementenlijst gebruiken {#use-subscription-lists}

Zodra de abonnementenlijst wordt gecreeerd, kunt u:

* Profielen toevoegen aan de abonnementenlijst

  U kunt personen tot **uitnodigen om zich bij de lijst** aan te sluiten, door aan een nieuwsbrief in te tekenen, of het registreren aan een gebeurtenis. U kunt ook **gepersonaliseerde berichten** naar de abonnees verzenden.

  Als u bijvoorbeeld een publiek wilt uitnodigen om zich te registreren voor een gebeurtenis of u wilt zich abonneren op een nieuwsbrief, kunt u hem een bericht met een koppeling naar een bestemmingspagina sturen zodat hij of zij zich bij de gebeurtenis kan aansluiten of zich kan abonneren. Profielen die zich aanmelden via het formulier op de bestemmingspagina worden toegevoegd aan de abonnementenlijst die u hiervoor hebt gemaakt.

* Berichten verzenden naar abonnees

  U kunt abonnementenlijsten als publiek ook gebruiken wanneer het bouwen van reizen, en het toevoegen van verpersoonlijking.

  Wanneer een klant zich bijvoorbeeld abonneert op een streamingservice, kan deze de directe verzending van een welkomste-mailreeks activeren, zodat deze zich voor het eerst bij de app kan aanmelden en zijn weergavevoorkeuren kan instellen.

Leer hoe te om uw abonnementenlijst in [&#x200B; te gebruiken dit gebruiksgeval &#x200B;](lp-use-cases.md#subscription-to-a-service).


## Door uw abonnementenlijsten bladeren {#browse-subscription-lists}

In de lijst worden alle gemaakte abonnementenlijsten weergegeven. U kunt ze filteren op basis van de aanmaakdatum of wijzigingsdatum en hun status.

![](assets/lp_subscription-filters.png)

De mogelijke statussen zijn als volgt:

* **[!UICONTROL Not started]**: U hebt een begindatum gedefinieerd die later is dan de huidige dag. De geabonneerde profielen ontvangen nog geen communicatie met betrekking tot deze abonnementenlijst.
* **[!UICONTROL Live]**: De huidige dag bestaat uit de begindatum en einddatum van de abonnementenlijst, of u hebt geen begin- en einddatum gedefinieerd, wat betekent dat de abonnementenlijst altijd actief is.
* **[!UICONTROL Expired]**: De einddatum wordt doorgegeven, zodat de abonnementenlijst niet meer geldig is. Voor elk geabonneerd profiel worden geen berichten meer ontvangen die betrekking hebben op deze abonnementenlijst.


## Abonnementenlijsten controleren {#monitor-subscription-lists}

U kunt de gevolgen van uw abonnementenlijst controleren door specifieke rapporten. U hebt toegang tot twee typen rapporten:

* Abonnementenlijst Live-rapport

  Live rapporten, die toegankelijk zijn vanaf het tabblad Laatste 24 uur, geven gebeurtenissen weer die in de afgelopen 24 uur hebben plaatsgevonden, met een minimale tijdsinterval van twee minuten vanaf de gebeurtenis. [Meer informatie](../reports/subscription-report-live.md)

* Abonnementenlijst Alle tijdrapporten, met Customer Journey Analytics

  Deze rapporten richten zich op gebeurtenissen die minstens twee uur geleden hebben plaatsgevonden en behandelen gebeurtenissen over een geselecteerde tijdspanne. Het **rapport van het Abonnement** biedt essentiële inzichten in de abonnementen van profielen en abonnementen verbonden aan bijzondere lijsten aan, die u helpen de doeltreffendheid van verschillende abonnementscampagnes en initiatieven in het drijven van overeenkomst en omzettingen begrijpen. [Meer informatie](../reports/subscription-report-global-cja.md)
