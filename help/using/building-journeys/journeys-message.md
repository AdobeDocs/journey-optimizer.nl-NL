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
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 2%

---

# Ingebouwde kanaalhandelingen gebruiken {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Ingebouwde kanaalactie"
>abstract="Journey Optimizer wordt geleverd met ingebouwde kanaalactiemogelijkheden. U kunt eenvoudig aan uw reis een bericht (e-mail, tekstbericht (SMS/MMS), duw, direct mail) of een binnenkomende ervaring (In-app, Web, code-gebaseerde ervaring, inhoudskaart) activiteit toevoegen, en montages en inhoud bepalen. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis."

[!DNL Journey Optimizer] wordt geleverd met ingebouwde kanaalactiemogelijkheden die worden gebruikt om berichten te verzenden: wanneer een profiel deze activiteit ingaat, wordt een bericht naar hen verzonden.

Als u een ingebouwde kanaalactie aan uw reis wilt toevoegen, sleept u een kanaalactiviteit en zet u de instellingen en inhoud van de activiteit neer. Het wordt vervolgens uitgevoerd en verzonden in het kader van de reis.

>[!NOTE]
>
>U kunt ook aangepaste handelingen instellen om uw berichten te verzenden in [!DNL Journey Optimizer] . [Meer informatie](#recommendation)

## Een bericht toevoegen tijdens een rit  {#add-msg-in-journey}

Met ingebouwde kanaalacties, kunt u uitgaande of binnenkomende berichten vormen. Voor meer informatie over de kanalen beschikbaar in reizen, verwijs naar de lijst in deze sectie: [&#x200B; Kanalen in reizen &amp; campagnes &#x200B;](../channels/gs-channels.md#channels).

Volg onderstaande stappen om een ingebouwde kanaalactie aan een reis toe te voegen.

1. Begin uw reis met een [&#x200B; Gebeurtenis &#x200B;](general-events.md) of a [&#x200B; gelezen activiteit van het publiek &#x200B;](read-audience.md).

1. Van de **sectie van Acties** van het palet, sleep en laat vallen een kanaalactiviteit in het canvas.

   ![&#x200B; de actiesactiviteit van het kanaal van het Web in wegcanvas &#x200B;](assets/journey-web-activity.png)

1. U kunt ook de **[!UICONTROL Action]** -activiteit selecteren, zodat u meerdere binnenkomende acties kunt selecteren. [Meer informatie](journey-action.md)

1. Configureer uw activiteit. De gedetailleerde configuratierichtlijnen zijn beschikbaar in de hieronder verbindingen.

   * Leer de gedetailleerde stappen om uw uitgaande actie tot stand te brengen als volgt:

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
      <td>
      <a href="../direct-mail/create-direct-mail.md">
      <img alt="Validatie" src="../assets/do-not-localize/direct-mail.jpg">
      </a>
      <div>
      <a href="../direct-mail/create-direct-mail.md"><strong> creeer direct-mailberichten </strong></a>
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
   >* Elke binnenkomende ervaringsactiviteit komt met een 3 dagen **wachten** activiteit. [Meer informatie](wait-activity.md#auto-wait-node)
   >
   >* Voor e-mails en pushmeldingen kunt u Send-Time optimaliseren inschakelen. [Meer informatie](send-time-optimization.md)

1. Afhankelijk van de activiteit, kunt u geavanceerde parameters tonen specifiek voor het geselecteerde kanaal, en sommige standaardwaarden zoals het uitvoeringsadres met voeten treden. [Meer informatie](about-journey-activities.md#advanced-parameters)

   >[!NOTE]
   >
   >Als de geavanceerde parameters verborgen zijn, klikt u op de knop **[!UICONTROL Show read-only fields]** boven in het rechterdeelvenster.

## Live-inhoud bijwerken {#update-live-content}

U kunt de inhoud van een ingebouwde kanaalactie tijdens een live reis bijwerken.

Om dit te doen, open uw levende reis, selecteer de kanaalactiviteit en klik **geef inhoud** uit.

![&#x200B; voeg dropdown actieactiviteit toe die beschikbare kanaalopties tonen &#x200B;](assets/add-a-message2.png)

U kunt de kenmerken die worden gebruikt in personalisatie echter niet wijzigen, ongeacht of het profielkenmerken of contextafhankelijke gegevens (van gebeurtenis- of reiseigenschappen) zijn.

Als u contextafhankelijke gegevens hebt gewijzigd, wordt het volgende foutbericht weergegeven: `ERR_AUTHORING_JOURNEYVERSION_201`

Als u profielkenmerken hebt gewijzigd, wordt het volgende foutbericht weergegeven: `ERR_AUTHORING_JOURNEYVERSION_202`

Voor de activiteit in de app kunnen wijzigingen in de inhoud worden aangebracht terwijl de reis live is, maar triggers in de app kunnen niet worden gewijzigd.

## Verzenden met aangepaste handelingen {#recommendation}

In plaats van de ingebouwde berichtmogelijkheden te gebruiken, kunt u douaneacties gebruiken om verbinding van een derdesysteem te vormen om berichten of API vraag te verzenden.

* Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. [Meer informatie](../action/action.md)

* Raadpleeg de volgende secties als u met [!DNL Adobe Campaign] werkt:

   * [[!DNL Journey Optimizer] en Campagne v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] en Campaign Standard](../action/acs-action.md)