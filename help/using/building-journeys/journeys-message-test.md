---
title: Een bericht toevoegen in een journey
description: Een bericht toevoegen in een journey
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3530a600a4c842ff99bc23354b2d158c6d41f902
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Een bericht toevoegen in een journey

[!DNL Journey Optimizer] berichtmogelijkheden zijn ingebouwd. U hoeft alleen uw inhoud te ontwerpen en uw bericht te publiceren. Zie [deze sectie](../get-started-content.md). Vervolgens voegt u eenvoudig een push- of e-mailbericht toe dat is ontworpen met Journey Optimizer.

Als u een systeem van derden gebruikt om uw berichten te verzenden, kunt u een douaneactie tot stand brengen. Meer informatie vindt u in deze [sectie](../action/action.md).

## Een berichtactiviteit toevoegen

1. Zoals altijd, begin uw reis met een gebeurtenis of een **Read Segment** activiteit.

   ![](../assets/jo-message0.png)

1. Sleep in de sectie **Handelingen** van het palet een **Bericht**-activiteit naar het canvas.

   ![](../assets/jo-message1.png)

1. Voeg een label en beschrijving toe.

   ![](../assets/jo-message2.png)

1. Klik in het veld **Bericht**. De lijst met beschikbare berichten die in Journey Optimizer zijn ontworpen, wordt weergegeven. U kunt de lijst filteren op status.

   ![](../assets/jo-message3.png)

1. Kies een bericht en klik **Select**. U kunt een nieuw bericht direct van dit scherm tot stand brengen door **Create bericht** te klikken.

   ![](../assets/jo-message4-ter.png)

   Als u uw bericht wilt controleren, kunt u **Open het bericht** pictogram in het **Bericht** gebied klikken. Het bericht wordt geopend op een nieuw tabblad.

   ![](../assets/jo-message4-bis.png)

1. Voeg de volgende stappen aan uw reis toe.

## E-mailparameters en push-parameters

In de secties **[!UICONTROL Email parameters]** en **[!UICONTROL Push parameters]** worden alleen-lezen velden weergegeven. U voert typisch deze configuratie uit wanneer het creëren van het bericht. Zie [deze sectie](../get-started-content.md).

![](../assets/jo-message4.png)

Als u een specifieke waarde wilt forceren, kunt u het pictogram **Inschakelen van parameteroverschrijving** rechts van het veld gebruiken. Deze optie kan nuttig zijn voor testdoeleinden. Voor een e-mailbericht kunt u bijvoorbeeld uw e-mailadres toevoegen. Nadat u de reis hebt gepubliceerd, wordt het e-mailbericht naar u verzonden.

## Tijdoptimalisatie verzenden{#send-time-optimization}

### Optimalisatie Verzonden tijd{#about-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Optimalisatie Verzonden tijd"
>abstract="De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door de AI-services van Adobe, kan de beste tijd voorspellen voor het verzenden van een e-mail- of pushbericht om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden."

De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door de AI-services van Adobe, kan de beste tijd voorspellen voor het verzenden van een e-mail- of pushbericht om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden. Gebruik ons machine-leert model om gepersonaliseerde verzendtijden voor elke gebruiker te plannen om open te groeien en tarieven van uw berichten te klikken.

Het model van de Optimalisering van de Send-Time neemt uw gegevens van Adobe Journey Optimizer op en kijkt open (voor e-mail en duw) op gebruikersniveau en klikt (voor e-mail) tarieven om te bepalen wanneer uw klanten het meest waarschijnlijk met uw overseinen in dienst zullen nemen. De optimalisering van de Send-Tijd vereist een minimum van één maand van bericht-volgende gegevens om geïnformeerde aanbevelingen te doen. Voor elke gebruiker, output het model de volgende vooruitlopende gegevens:

* Het beste uur van elke dag van de week om de betrokkenheid te maximaliseren
* De beste dag van de week om de betrokkenheid te maximaliseren
* Het beste uur van de beste dag van de week om de betrokkenheid te maximaliseren

Het model varieert, of u over score of opleiding spreekt. De training wordt aanvankelijk wekelijks en vervolgens driemaandelijks gegeven. De score wordt eerst wekelijks en daarna maandelijks vastgesteld.

* Training - de ontwikkeling van het algoritme dat wordt gebruikt om de score te maken
* Scores - de toepassing van een score op individuele profielen die op het getrainde model worden gebaseerd

Deze informatie wordt opgeslagen met het profiel van de gebruiker en wordt bij de uitvoering van de reis gebruikt om Adobe Journey Optimizer te laten weten wanneer je bericht moet worden verzonden.

## Belangrijke opmerkingen{#send-time-optimization-notes}

* Deze functie is alleen beschikbaar voor monokanaalberichten via e-mail en push met de functie voor bijhouden ingeschakeld.
* Het bericht moet worden gepubliceerd.
* Deze functie is niet compatibel met de burst-modus.

## Optimalisatie Verzonden tijd activeren{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Optimalisatie Verzonden tijd activeren"
>abstract="Kies of u wilt optimaliseren bij het openen van e-mail of door op de e-mail te klikken. Selecteer hiervoor het juiste keuzerondje. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Optimalisatie Verzonden tijd activeren"
>abstract="Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

Schakel Send-Time Optimization in op een e-mail- of pushbericht door de schakelaar **Send-Time Optimization** te selecteren uit de parameters voor berichtactiviteit.

![](../assets/jo-message5.png)

Kies bij e-mailberichten of u wilt optimaliseren bij het openen van een e-mail of door op het juiste keuzerondje te klikken. Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten.

U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde in te voeren voor de optie **Verzenden binnen de volgende optie**. Als u &quot;zes uur&quot;als waarde kiest, zal Adobe Journey Optimizer elk gebruikersprofiel controleren om te zien of komt de optimale verzendtijd binnen zes uur na de tijd van de reisuitvoering voor en selecteert de Send-Time Optimization-bepaalde tijd. Als die tijd niet binnen de volgende zes uur is, zal Adobe Journey Optimizer standaard het bericht verzenden op het tijdstip van uitvoering van de reis.
