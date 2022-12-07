---
solution: Journey Optimizer
product: journey optimizer
title: Een bericht toevoegen in een journey
description: Leer hoe u een bericht tijdens een rit kunt toevoegen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 1%

---

# E-mail, SMS, Push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden. U kunt gewoon tijdens uw reis een push-, SMS- of e-mailberichtactiviteit toevoegen en instellingen en inhoud definiëren. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis.

U kunt ook specifieke acties instellen om u berichten te sturen:

* Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. Meer informatie in deze [sectie](../action/action.md).

* Raadpleeg de volgende secties als u werkt met Campagne en Journey Optimizer:

   * [[!DNL Journey Optimizer] en Campaign Classic v7/Campagne v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] en Campaign Standard](../action/acs-action.md)

Volg onderstaande stappen om een bericht toe te voegen aan een rit:

1. Begin uw reis met een [Gebeurtenis](general-events.md) of [Segment lezen](read-segment.md) activiteit.

1. Van de **Handelingen** van het palet, slepen en neerzetten en **email**, en **SMS** of **Push** op het canvas.

1. Configureer uw activiteit. Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Lood" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>E-mails maken</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Onfrequent" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>Pushberichten maken<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="Validatie" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>SMS-berichten maken</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Actieve inhoud bijwerken{#update-live-content}

U kunt de inhoud van een bericht (e-mail, sms, push) tijdens een live reis bijwerken.

Om dit te doen, open uw levende reis, selecteer de berichtactiviteit en klik **Inhoud bewerken**.

![](assets/add-a-message2.png)

U kunt de kenmerken die worden gebruikt in personalisatie echter niet wijzigen, ongeacht of het profielkenmerken of contextafhankelijke gegevens (van gebeurtenis- of reiseigenschappen) zijn.

## Send-Time optimalisatie{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Optimalisatie Verzonden tijd"
>abstract="Met de functie Verzenden via Adobe Journey Optimizer, aangedreven door de AI-services voor optimalisatie van de Adobe, kunt u het beste tijdstip voorspellen waarop een e-mail- of pushbericht wordt verzonden om de betrokkenheid te maximaliseren op basis van een open historie en klikfrequentie."

### Over Send-Time optimalisatie {#about-send-time}

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

### Send-Time optimaliseren activeren{#activate-send-time-optimization}

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
