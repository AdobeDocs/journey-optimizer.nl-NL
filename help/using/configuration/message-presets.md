---
title: Voorinstellingen voor berichten maken
description: Leer hoe u voorinstellingen voor e-mail- en pushberichten maakt
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Voorinstellingen voor berichten maken

Met [!DNL Journey Optimizer] kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten (e-mailtype, e-mail en naam van de afzender, mobiele apps, enz.).

Afhankelijk van de verschillende merken waarvoor u moet communiceren, kunt u zoveel voorinstellingen voor berichten instellen als u wilt.

Nadat berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren bij het maken van berichten in de lijst **[!UICONTROL Presets]**.

## Een berichtvoorinstelling maken {#create-message-preset}

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Geef een naam en een beschrijving (optioneel) voor de voorinstelling op en geef vervolgens het kanaal of de kanalen op die u wilt configureren.

   ![](../assets/preset-general.png)

1. Configureer de instellingen voor e-mail- en pushmeldingen:

   Geef voor het e-mailkanaal het volgende op:

   * Het type communicatie dat met de voorinstelling wordt verzonden (transactie- of marketingberichten),
   * Het [subdomein](about-subdomain-delegation.md) om de e-mails te verzenden,
   * De [IP pool](ip-pools.md) om aan vooraf ingesteld te associëren,
   * De headerparameters die moeten worden gebruikt voor de e-mails die worden verzonden met behulp van de voorinstelling.

   ![](../assets/preset-email.png)

   Voor het kanaal van het dupbericht, specificeer IOS en/of mobiele toepassingen Android voor uw berichten te gebruiken. Raadpleeg [deze sectie](../push-configuration.md) voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten.

   ![](../assets/preset-push.png)

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** om te bevestigen. U kunt de berichtvoorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](../assets/preset-submit.png)

1. Nadat de berichtvoorinstelling is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]**.

   Tijdens deze stap, zullen verscheidene controles worden uitgevoerd om te verifiëren dat het behoorlijk is gevormd. De verwerkingstijd is ongeveer 48u-72u, en kan tot 7-10 dagen vergen.

   Deze controles omvatten leverbaarheidstests die door het team van de Adobe worden uitgevoerd:

   * SPF-validatie,
   * DKIM-validatie,
   * MX-recordvalidatie,
   * Controleer de zwarte lijst van IP&#39;s,
   * Helo host check,
   * verificatie van de IP-pool;
   * A/PTR-record, t/m/res-subdomeinverificatie.

1. Als de controles zijn voltooid, krijgt de berichtvoorinstelling de status **[!UICONTROL Active]**. Het is klaar om te worden gebruikt om berichten te leveren.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Voorinstellingen voor monitorberichten

Alle voorinstellingen voor berichten worden weergegeven in het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**. Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren (kanaaltype, gebruiker, status).

![](../assets/preset-filters.png)

Voorinstellingen voor berichten kunnen de volgende statussen hebben:

* **[!UICONTROL Draft]**: De berichtvoorinstelling is opgeslagen als een concept en is nog niet verzonden. Open het om de configuratie te hervatten.
* **[!UICONTROL Processing]**: De berichtvoorinstelling is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Active]**: De berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de berichtvoorinstelling.
* **[!UICONTROL De-activated]**: De berichtvoorinstelling is gedeactiveerd. Het kan niet worden gebruikt om nieuwe berichten tot stand te brengen.

## Voorinstellingen voor berichten bewerken

Als u een berichtvoorinstelling wilt bewerken, moet u deze eerst deactiveren zodat deze niet beschikbaar is voor het maken van nieuwe berichten (gepubliceerde berichten met deze voorinstelling worden niet beïnvloed en blijven werken). Vervolgens moet u de berichtvoorinstelling dupliceren om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken:

1. Open de lijst met voorinstellingen voor berichten en deactiveer vervolgens de berichtvoorinstelling die u wilt bewerken.

   ![](../assets/preset-deactivate.png)

1. Dupliceer de uitgeschakelde berichtvoorinstelling. Er wordt automatisch een kopie met de status **[!UICONTROL Draft]** toegevoegd aan de lijst.

   ![](../assets/preset-duplicated.png)

1. Open de gedupliceerde voorinstelling voor berichten, wijzig deze naar wens en verzend uw wijzigingen. De berichtvoorinstelling doorloopt dezelfde validatiecyclus als tijdens de [aanmaakstap](#create-message-preset).

1. Zodra bevestigd, krijgt het de **[!UICONTROL Active]** status en is klaar om worden gebruikt om nieuwe berichten tot stand te brengen.

   >[!NOTE]
   >
   >De-geactiveerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.