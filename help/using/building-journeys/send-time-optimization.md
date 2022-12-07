---
solution: Journey Optimizer
product: journey optimizer
title: Tijdoptimalisatie verzenden
description: Leer hoe te parameter verzendt tijdoptimalisering in uw berichten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Send-Time optimalisatie{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Optimalisatie Verzonden tijd"
>abstract="Met de functie Verzenden via Adobe Journey Optimizer, aangedreven door de AI-services voor optimalisatie van de Adobe, kunt u het beste tijdstip voorspellen waarop een e-mail- of pushbericht wordt verzonden om de betrokkenheid te maximaliseren op basis van een open historie en klikfrequentie."

Met de functie Verzenden via Adobe Journey Optimizer, aangedreven door de AI-services voor optimalisatie van de Adobe, kunt u het beste tijdstip voorspellen waarop een e-mail- of pushbericht wordt verzonden om de betrokkenheid te maximaliseren op basis van een open historie en klikfrequentie. Gebruik ons machine-leert model om gepersonaliseerde verzendtijden voor elke gebruiker te plannen om open te groeien en tarieven van uw berichten te klikken.

Het model van de Optimalisering van de Send-Time neemt uw gegevens van Adobe Journey Optimizer op en kijkt open (voor e-mail en duw) op gebruikersniveau en klikt (voor e-mail) tarieven om te bepalen wanneer uw klanten het meest waarschijnlijk met uw overseinen in dienst zullen nemen. De optimalisering van de Send-Tijd vereist een minimum van één maand van bericht-volgende gegevens om geïnformeerde aanbevelingen te doen. Voor elke gebruiker kiest het systeem automatisch de beste tijd met behulp van de volgende scores:

* Het beste uur van elke dag van de week om de betrokkenheid te maximaliseren
* De beste dag van de week om de betrokkenheid te maximaliseren
* Het beste uur van de beste dag van de week om de betrokkenheid te maximaliseren

Het model varieert, of u over score of opleiding spreekt. De training wordt aanvankelijk wekelijks en vervolgens driemaandelijks gegeven. De score wordt eerst wekelijks en daarna maandelijks vastgesteld.

* Training - de ontwikkeling van het algoritme dat wordt gebruikt om de score te maken
* Scores - de toepassing van een score op individuele profielen die op het getrainde model worden gebaseerd

Deze informatie wordt opgeslagen met het profiel van de gebruiker en wordt bij de uitvoering van de reis gebruikt om Adobe Journey Optimizer te laten weten wanneer je bericht moet worden verzonden.

>[!CAUTION]
>
>Deze functie is niet compatibel met de burst-modus.

## Send-Time optimaliseren activeren{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Send-Time optimaliseren activeren"
>abstract="Kies of u wilt optimaliseren bij het openen van e-mail of door op de e-mail te klikken. Selecteer hiervoor het juiste keuzerondje. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Send-Time optimaliseren activeren"
>abstract="Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

Schakel SendTime Optimization in op een e-mail- of pushbericht door de optie **Send-Time optimalisatie** Schakel over van de activiteitsparameters.

![](../building-journeys/assets/jo-message5.png)

Kies bij e-mailberichten of u wilt optimaliseren bij het openen van een e-mail of door op het juiste keuzerondje te klikken. Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten.

U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt, te accentueren door een waarde in te voeren voor het dialoogvenster **Verzenden binnen de volgende** optie. Als u &quot;zes uur&quot;als waarde kiest, [!DNL Journey Optimizer] zal elk gebruikersprofiel controleren en de optimale verzendtijd kiezen binnen zes uur na de uitvoeringstijd van de reis.
