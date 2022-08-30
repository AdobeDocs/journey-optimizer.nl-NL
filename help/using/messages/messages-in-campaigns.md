---
title: Berichten toevoegen aan campagnes
description: Leer hoe u berichten in een campagne kunt toevoegen
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 2%

---


# Berichten toevoegen aan campagnes{#messages-in- campaigns}

In uw campagnes, selecteer het kanaal om het bericht te ontwerpen en te personaliseren u naar uw publiek wilt verzenden. Wanneer u een e-mail, een SMS-bericht of een pushbericht aan uw campagne toevoegt, kunt u deze direct verzenden of het bericht plannen.

>[!NOTE]
>U kunt ook reizen maken om geactiveerde berichten te verzenden. Meer informatie [in deze sectie](messages-in-journeys.md).

Leer hoe te om berichten in een campagne toe te voegen en te vormen [in deze sectie](../campaigns/create-campaign.md)

Leer gedetailleerde stappen om uw berichtinhoud tot stand te brengen op de volgende pagina:

* [Een e-mail maken](create-email.md)
* [Pushberichten maken](create-push.md)
* [Een SMS-bericht maken](create-sms.md)

## Optimalisatie bij verzenden inschakelen{#sto-in-journeys}

Voor e-mail- en pushberichten kunt u **[!UICONTROL Send-time optimization]**.

Gebruiken **[!UICONTROL Send-time optimization]** om gepersonaliseerd te plannen verzend tijden voor elke gebruiker om open te groeien en tarieven van uw berichten te klikken. [Meer informatie](../messages/send-time-optimization.md).

## Geavanceerde parameters{#adv-settings}

Geavanceerde parameters zijn standaard alleen-lezen en verborgen.

Klik op de knop **[!UICONTROL Show read-only fields]** boven aan het berichtvenster.

![](assets/show-read-only.png)

De geavanceerde parameters worden getoond bij de bodem van de berichtruit. Deze parameters worden gedefinieerd door de [systeembeheerder](../start/path/administrator.md) in de [kanaaloppervlak](../configuration/channel-surfaces.md) (d.w.z. voorinstelling bericht) die aan het bericht is gekoppeld.

Voor pushberichten kunt u de volgende parameters weergeven: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Voor e-mail kunt u het primaire e-mailadres weergeven.

Voor specifiek gebruik, kunt u deze waarden in specifieke contexten met voeten treden. Als u een waarde wilt afdwingen, klikt u op de knop **Parameteroverschrijving inschakelen** rechts van het veld. Deze optie is bijvoorbeeld handig voor:

* Test een e-mailadres. U kunt uw e-mailadres toevoegen. Nadat u de reis hebt gepubliceerd, wordt het e-mailbericht naar u verzonden.
* Raadpleeg het e-mailadres van de abonnees van een lijst. Meer informatie in [dit geval gebruiken](../building-journeys/message-to-subscribers-uc.md).

Klik op hetzelfde pictogram om geavanceerde instellingen te verbergen.

## Bladeren door berichten{#browse-message}

Wanneer de veelvoudige berichten in een reis worden gebruikt, kunt u van één aan een andere van **Inhoud bewerken** scherm.

![](assets/inline-messages-multi-content.png)

U kunt vervolgens [waarschuwingen controleren](alerts.md) en [simuleren](../design/preview.md) elke inhoud uit één weergave.

## Een bericht dupliceren {#duplicate-message}

U kunt een bestaand bericht kopiëren vanaf het canvas van de reis.

Volg onderstaande stappen om dit te doen:

1. Selecteer het bericht dat u wilt kopiëren.

1. Gebruik de **[!UICONTROL Copy]** van de knop **[!UICONTROL Action]** venster.

   ![](assets/message-duplicate.png)

1. Enter **crtl+V** om het bericht te plakken.

   Het bericht wordt toegevoegd aan de reiscanvas. Alle montages en configuratie zullen aan het nieuwe bericht worden gekopieerd.

   ![](assets/message-duplicated.png)

1. Wijzig de naam van het bericht om het oorspronkelijke bericht te kunnen onderscheiden van de kopie, bijvoorbeeld bij het bewerken van berichten, zoals hieronder:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Voor e-mailberichten kunt u ook een bestaand bericht naar een sjabloon sturen. [Meer informatie](../design/email-templates.md).

## Een bericht verwijderen{#delete-message}

Als u een bericht wilt verwijderen, gebruikt u het prullenbakpictogram boven aan het deelvenster Handeling Kanaal.

![](assets/delete-message.png)

Gebruik de **[!UICONTROL Confirm]** te valideren.
