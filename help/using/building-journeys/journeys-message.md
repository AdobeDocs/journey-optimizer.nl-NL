---
solution: Journey Optimizer
product: journey optimizer
title: Een bericht toevoegen in een journey
description: Leer hoe u een bericht tijdens een rit kunt toevoegen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: reis, bericht, push, sms, email, in app
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 055b735308cc6f0f942c165541d87dfdb74f557c
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# E-mail, In-app, Push, SMS{#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Berichtactiviteit"
>abstract="Journey Optimizer wordt geleverd met ingebouwde berichtmogelijkheden. U kunt gewoon tijdens uw reis een push-, SMS-, In-app- of e-mailberichtactiviteit toevoegen en instellingen en inhoud definiëren. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis."

[!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden. U kunt gewoon tijdens uw reis een push-, SMS-, In-app- of e-mailberichtactiviteit toevoegen en instellingen en inhoud definiëren. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis.

U kunt ook specifieke acties instellen om u berichten te sturen:

* Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. Meer informatie in deze [sectie](../action/action.md).

* Raadpleeg de volgende secties als u werkt met Campagne en Journey Optimizer:

   * [[!DNL Journey Optimizer] en Campaign Classic v7/Campagne v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] en Campaign Standard](../action/acs-action.md)

Volg onderstaande stappen om een bericht toe te voegen aan een rit:

1. Begin uw reis met een [Gebeurtenis](general-events.md) of [Publiek lezen](read-audience.md) activiteit.

1. Van de **Handelingen** van het palet, slepen en neerzetten en **email**, en **In-app**, en **SMS** of **Push** op het canvas.

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
   <a href="../in-app/create-in-app.md">
   <img alt="Lood" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>In-app-berichten maken</strong>
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

U kunt de inhoud van een bericht (e-mail, In-app, Push, SMS) tijdens een live reis bijwerken.

Om dit te doen, open uw levende reis, selecteer de berichtactiviteit en klik **Inhoud bewerken**.

![](assets/add-a-message2.png)

U kunt de kenmerken die worden gebruikt in personalisatie echter niet wijzigen, ongeacht of het profielkenmerken of contextafhankelijke gegevens (van gebeurtenis- of reiseigenschappen) zijn.

Als u contextuele gegevens hebt gewijzigd, wordt het volgende foutbericht weergegeven: ERR_AUTHORING_JOURNEYVERSION_201

Als u profielkenmerken hebt gewijzigd, wordt het volgende foutbericht weergegeven: ERR_AUTHORING_JOURNEYVERSION_202

Voor de activiteit in de app kunnen wijzigingen in de inhoud worden aangebracht terwijl de reis live is, maar triggers in de app kunnen niet worden gewijzigd.

## Send-Time optimalisatie{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Optimalisatie van verzonden tijd"
>abstract="De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door de AI-services van de Adobe, kan de beste tijd voorspellen om een e-mail- of pushbericht te verzenden om de betrokkenheid te maximaliseren op basis van een open historie en klikfrequentie."

### Over Send-Time optimalisatie {#about-send-time}

De functie voor Send-Time optimalisatie van Adobe Journey Optimizer, aangedreven door de AI-services van de Adobe, kan de beste tijd voorspellen om een e-mail- of pushbericht te verzenden om de betrokkenheid te maximaliseren op basis van een open historie en klikfrequentie. Gebruik ons machine-leert model om gepersonaliseerde verzendtijden voor elke gebruiker te plannen om open te groeien en tarieven van uw berichten te klikken.

Het model van de Optimalisering van de Send-Time neemt uw gegevens van Adobe Journey Optimizer op en kijkt open (voor e-mail en duw) op gebruikersniveau en klikt (voor e-mail) tarieven om te bepalen wanneer uw klanten het meest waarschijnlijk met uw overseinen in dienst zullen nemen. De optimalisering van de Send-Tijd vereist een minimum van één maand van bericht-volgende gegevens om geïnformeerde aanbevelingen te doen. Voor elke gebruiker kiest het systeem automatisch de beste tijd met behulp van de volgende scores:

* Het beste uur van elke dag van de week om de betrokkenheid te maximaliseren
* De beste dag van de week om de betrokkenheid te maximaliseren
* Het beste uur van de beste dag van de week om de betrokkenheid te maximaliseren

Het model varieert, of u over score of opleiding spreekt. De training wordt aanvankelijk wekelijks en vervolgens driemaandelijks gegeven. De score wordt eerst wekelijks en daarna maandelijks vastgesteld.

* Training - de ontwikkeling van het algoritme waarmee de score wordt gemaakt
* Scores - de toepassing van een score op individuele profielen die op het getrainde model worden gebaseerd

Deze informatie wordt opgeslagen met het profiel van de gebruiker en wordt bij de uitvoering van de reis gebruikt om Adobe Journey Optimizer te laten weten wanneer je bericht moet worden verzonden.

>[!CAUTION]
>
>Deze functie is niet compatibel met de burst-modus.

### Veelgestelde vragen {#faq-send-time}

Wat kan de Optimalisering van de Verzendtijd doen? Hoe worden nieuwe profielen verwerkt? Spreidt het over een periode van 6/12/24 uur?

Optimalisatie van verzendtijd probeert de beste tijd te voorspellen om met klanten in contact te komen en open-/kliksnelheden voor e-mails te optimaliseren. De score heeft een indeling van `3*7*24` kenmerken voor elk profiel. De `7*24` kenmerken beschrijven de volgorde van de te verwachten beste tijd voor het verzenden van e-mails naar de ontvanger en 3 is voor het optimaliseren van de e-mailopeningsfrequentie, het klikken op snelheid via e-mail en het open tarief via push.

Waar kan ik de verwachte verzendtijd voor elk profiel zien?

U kunt de algemene score zien in het dialoogvenster **Profielen** interface. Voor elk van de drie sets van 168 scores lopen de ranks van -83 tot 84. Hoe hoger de rangorde, hoe beter de tijd is om met de ontvanger te communiceren. Aangezien u het begin en de duur van een reis kunt bepalen, kan de beste rang (84) niet in dat tijdvenster vallen. In dit geval raden we u aan een uur met de hoogste rangorde te kiezen.

Welke rapportage is beschikbaar?

Open uw reis, klik **Rapport weergeven** in de rechterbovenhoek en selecteert u de **Reis** links. [Meer informatie](../reports/journey-global-report.md)

Hoe beïnvloeden de gegevens van de Optimalisering van de Send-Time profielrijkdom?

De optimalisering van de Send-Tijd voegt de score/de attributen aan elk profiel toe maar geen nieuw profiel wordt gecreeerd.

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

U kunt er ook voor kiezen om de verzendtijden die door het systeem worden gebruikt, te accentueren door een waarde in te voeren voor de **Verzenden binnen de volgende** -optie. Als u &quot;zes uur&quot;als waarde kiest, [!DNL Journey Optimizer] zal elk gebruikersprofiel controleren en de optimale verzendtijd kiezen binnen zes uur na de uitvoeringstijd van de reis.

**Wat gebeurt er als de optimale tijd zich buiten het venster bevindt?**

Neem een voorbeeld met de volgende opstelling:

* Optimaliseren bij klikken
* Actie moet om 10 uur beginnen
* Venster is 3 uur

Een profiel kan een optimale open tijd hebben die buiten het venster is. De optimale open functie van John bij klikken is bijvoorbeeld 17.00 uur.

Op profielniveau zijn er scores voor elk uur van de week. In dit voorbeeld wordt de e-mail altijd verzonden binnen het venster. Tijdens runtime, controleert het systeem de lijst van scores binnen dat venster (3 uurvenster dat bij 10 AM begint). Vervolgens vergelijkt het systeem de scores voor 10, 11 en 12 uur &#39;s middags en wordt het hoogste geselecteerd. Het e-mailbericht wordt op dat moment verzonden.
