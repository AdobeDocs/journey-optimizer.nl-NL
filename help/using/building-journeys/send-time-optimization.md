---
solution: Journey Optimizer
product: journey optimizer
title: Tijdoptimalisatie verzenden
description: Leer hoe te parameter verzendt tijdoptimalisering in uw berichten
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: send-time, send, message, optimization, trip, AI, Intelligent
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Send-Time optimalisatie{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Optimalisatie van verzonden tijd"
>abstract="De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door Adobe AI-services, kan de beste tijd voorspellen om een e-mail- of pushbericht te verzenden om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden."

De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door Adobe AI-services, kan de beste tijd voorspellen om een e-mail- of pushbericht te verzenden om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden. Gebruik ons machine-leert model om gepersonaliseerde verzendtijden voor elke gebruiker te plannen om open te groeien en tarieven van uw berichten te klikken.

Het model van de Optimalisering van de Send-Time neemt uw gegevens van Adobe Journey Optimizer op en kijkt open (voor e-mail en duw) op gebruikersniveau en klikt (voor e-mail) tarieven om te bepalen wanneer uw klanten het meest waarschijnlijk met uw overseinen in dienst zullen nemen. De optimalisering van de Send-Tijd vereist een minimum van één maand van bericht-volgende gegevens om geïnformeerde aanbevelingen te doen. Voor elke gebruiker kiest het systeem automatisch de beste tijd met behulp van de volgende scores:

* Het beste uur van elke dag van de week om de betrokkenheid te maximaliseren
* De beste dag van de week om de betrokkenheid te maximaliseren
* Het beste uur van de beste dag van de week om de betrokkenheid te maximaliseren

Het model varieert, of u over score of opleiding spreekt. De training wordt aanvankelijk wekelijks en vervolgens driemaandelijks gegeven. De score wordt eerst wekelijks en daarna maandelijks vastgesteld.

* Training - de ontwikkeling van het algoritme waarmee de score wordt gemaakt
* Scores - de toepassing van een score op individuele profielen die op het getrainde model worden gebaseerd

Deze informatie wordt opgeslagen met het profiel van de gebruiker en wordt bij de uitvoering van de reis gebruikt om Adobe Journey Optimizer te laten weten wanneer je bericht moet worden verzonden.

## Send-Time optimaliseren activeren{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Send-Time optimaliseren activeren"
>abstract="Kies of u wilt optimaliseren bij het openen van e-mail of door op de e-mail te klikken. Selecteer hiervoor het juiste keuzerondje. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Send-Time optimaliseren activeren"
>abstract="Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten. U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt te accentueren door een waarde voor Verzenden in te voeren binnen de volgende optie."

Laat Send-Time Optimalisering op een e-mail of duw bericht toe door de **schakelaar van de Optimalisering van de Send-Time** van de activiteitenparameters te selecteren.

![](../building-journeys/assets/jo-message5.png)

Kies bij e-mailberichten of u wilt optimaliseren bij het openen van een e-mail of door op het juiste keuzerondje te klikken. Pushberichten worden standaard ingesteld op de optie Openen, omdat klikken niet van toepassing zijn op pushberichten.

U kunt ook verkiezen om de verzendtijden te steunen die door het systeem worden gebruikt door een waarde voor **in te gaan verzendt binnen de volgende** optie. Als u &quot;zes uur&quot; als waarde kiest, controleert [!DNL Journey Optimizer] elk gebruikersprofiel en kiest u de optimale verzendtijd binnen zes uur na de uitvoeringstijd van de reis.
