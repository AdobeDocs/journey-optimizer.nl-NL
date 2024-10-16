---
solution: Journey Optimizer
product: journey optimizer
title: Voeg een ingebouwde kanaalactie aan een reis toe
description: Leer hoe u een ingebouwde kanaalactie aan een reis toevoegt
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: reis, bericht, push, sms, e-mail, in-app, web, inhoudskaart, op code gebaseerde ervaring
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Ingebouwde kanaalhandelingen gebruiken {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Ingebouwde kanaalactie"
>abstract="Journey Optimizer wordt geleverd met ingebouwde kanaalactiemogelijkheden. U kunt aan uw reis eenvoudig een uitgaande (e-mail, tekstbericht (SMS/MMS), duw) of binnenkomende (in-app, Web, code-gebaseerde ervaring, inhoudskaart) activiteit toevoegen, en montages en inhoud bepalen. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis."

[!DNL Journey Optimizer] wordt geleverd met ingebouwde kanaalactiemogelijkheden. U kunt aan uw reis eenvoudig een uitgaande (e-mail, tekstbericht (SMS/MMS), duw) of binnenkomende (in-app, Web, code-gebaseerde ervaring, inhoudskaart) activiteit toevoegen, en montages en inhoud bepalen. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis.

>[!NOTE]
>
>U kunt ook specifieke acties instellen om u berichten te sturen. [Meer informatie](#recommendation)

Volg onderstaande stappen om een ingebouwde kanaalactie aan een reis toe te voegen.

1. Begin uw reis met een [ Gebeurtenis ](general-events.md) of a [ gelezen activiteit van het publiek ](read-audience.md).

1. Van de **Acties** sectie van het palet, sleep en laat vallen uitgaand (**e-mail**, **duw**, **SMS**) of binnenkomend (**In-app**, **Web**, **code-gebaseerde ervaring**, **inhoudskaart**) op het canvas.

   ![](assets/journey-web-activity.png)

1. Configureer uw activiteit.

   * Leer de gedetailleerde stappen om uw berichtinhoud tot stand te brengen als volgt:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="Lood" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong> creeer e-mails </strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="Onfrequent" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong> creeer dupberichten <strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="Validatie" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong> creeer tekstberichten (SMS/MMS) </strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * Leer de gedetailleerde stappen om uw binnenkomende actie tot stand te brengen als volgt:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Lood" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong> creeer in-app berichten </strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Lood" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong> creeer Webervaringen </strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Lood" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong> creeer inhoudskaarten </strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Onfrequent" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong> creeer op code-gebaseerde ervaringen <strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >Elke binnenkomende berichtactiviteit komt met een 3 dagen **wachten** activiteit. [Meer informatie](../building-journeys/wait-activity.md#auto-wait-node)

## Aanbeveling {#recommendation}

[!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheid. Met aangepaste handelingen kunt u echter de verbinding van een systeem van derden configureren om berichten of API-aanroepen te verzenden.

* Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. [Meer informatie](../action/action.md)

* Raadpleeg de volgende secties als u werkt met Campagne en Journey Optimizer:

   * [[!DNL Journey Optimizer] en Campagne v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] en Campaign Standard](../action/acs-action.md)

## Actieve inhoud bijwerken{#update-live-content}

U kunt de inhoud van een ingebouwde kanaalactie tijdens een live reis bijwerken.

Om dit te doen, open uw levende reis, selecteer de kanaalactiviteit en klik **geef inhoud** uit.

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

>[!NOTE]
>
>Deze functie is niet standaard ingeschakeld. U kunt contact opnemen met uw Adobe om de pen te activeren.
>
>De functie Send-Time optimalisatie is alleen van toepassing op e-mail- en pushkanalen.

### Over Send-Time optimalisatie {#about-send-time}

De functie van de Optimalisatie van de Send-Time van Adobe Journey Optimizer, die door de diensten van AI van de Adobe wordt aangedreven, kan de beste tijd voorspellen om een **e-mail** of **duw bericht** te verzenden om overeenkomst te maximaliseren die op historisch open wordt gebaseerd en tarieven klikt. Gebruik ons machine-leert model om gepersonaliseerde verzendtijden voor elke gebruiker te plannen om open te groeien en tarieven van uw berichten te klikken.

Het model van de Optimalisering van de Send-Time neemt uw gegevens van Adobe Journey Optimizer op en kijkt open (voor e-mail en duw) op gebruikersniveau en klikt (voor e-mail) tarieven om te bepalen wanneer uw klanten het meest waarschijnlijk met uw overseinen in dienst zullen nemen. De optimalisering van de Send-Tijd vereist een minimum van één maand van bericht-volgende gegevens om geïnformeerde aanbevelingen te doen. Voor elke gebruiker kiest het systeem automatisch de beste tijd met behulp van de volgende scores:

* Het beste uur van elke dag van de week om de betrokkenheid te maximaliseren
* De beste dag van de week om de betrokkenheid te maximaliseren
* Het beste uur van de beste dag van de week om de betrokkenheid te maximaliseren

Het model varieert, of u over score of opleiding spreekt. De training wordt aanvankelijk wekelijks en vervolgens driemaandelijks gegeven. De score wordt eerst wekelijks en daarna maandelijks vastgesteld.

* Training - de ontwikkeling van het algoritme waarmee de score wordt gemaakt
* Scores - de toepassing van een score op individuele profielen die op het getrainde model worden gebaseerd

Deze informatie wordt opgeslagen met het profiel van de gebruiker en wordt bij de uitvoering van de reis gebruikt om Adobe Journey Optimizer te laten weten wanneer je bericht moet worden verzonden.

### Veelgestelde vragen {#faq-send-time}

+++ Wat kan de Optimalisering van de Verzendtijd doen? Hoe worden nieuwe profielen verwerkt? Spreidt het over een periode van 6/12/24 uur?

Optimalisatie van verzendtijd probeert de beste tijd te voorspellen om met klanten in contact te komen en open-/kliksnelheden voor e-mails te optimaliseren. De score heeft een indeling van `3*7*24` -kenmerken voor elk profiel. De `7*24` -kenmerken beschrijven de volgorde van de voorspelde beste tijd voor het verzenden van e-mails naar de ontvanger en 3 is bedoeld voor het optimaliseren van de openingsfrequentie van e-mail, het klikken op snelheid per e-mail en het uitvoeren van een push-snelheid.

+++

+++Waar kan ik de verwachte verzendtijd voor elk profiel zien?

U kunt de algemene score in de **Profielen** interface zien. Voor elk van de drie sets van 168 scores lopen de ranks van -83 tot 84. Hoe hoger de rangorde, hoe beter de tijd is om met de ontvanger te communiceren. Aangezien u het begin en de duur van een reis kunt bepalen, kan de beste rang (84) niet in dat tijdvenster vallen. In dit geval raden we u aan een uur met de hoogste rangorde te kiezen.

+++


+++Welke rapportering is beschikbaar?

Heb toegang tot uw reis, klik het **rapport van de Mening** knoop in het hoogste recht en selecteer het **** lusje van de Reis op de linkerzijde. [Meer informatie](../reports/journey-global-report-cja.md)

+++

+++Hoe beïnvloeden de gegevens van de Optimalisatie van de Send-Time profielrijkdom?

De optimalisering van de Send-Tijd voegt de score/de attributen aan elk profiel toe maar geen nieuw profiel wordt gecreeerd.

+++

### Send-Time optimaliseren activeren{#activate-send-time-optimization}

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

**wat gebeurt als de optimale tijd buiten het venster is?**

Neem een voorbeeld met de volgende opstelling:

* Optimaliseren bij klikken
* Actie moet om 10 uur beginnen
* Venster is 3 uur

Een profiel kan een optimale open tijd hebben die buiten het venster is. De optimale open functie van John bij klikken is bijvoorbeeld 17.00 uur.

Op profielniveau zijn er scores voor elk uur van de week. In dit voorbeeld wordt de e-mail altijd verzonden binnen het venster. Tijdens runtime, controleert het systeem de lijst van scores binnen dat venster (3 uurvenster dat bij 10 AM begint). Vervolgens vergelijkt het systeem de scores voor 10, 11 en 12 uur &#39;s middags en wordt het hoogste geselecteerd. Het e-mailbericht wordt op dat moment verzonden.
