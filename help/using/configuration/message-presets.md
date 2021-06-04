---
title: Voorinstellingen voor berichten maken
description: Leer hoe u berichtvoorinstellingen configureert en controleert
source-git-commit: 6cabe17f67d0207fc72d3c61498fae0affe5a785
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# Voorinstellingen voor berichten maken

Met [!DNL Journey Optimizer] kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten: e-mailtype, e-mail en naam van de afzender, mobiele apps en meer.

>[!CAUTION]
>
> Configuratie van voorinstellingen voor berichten is beperkt tot reisbeheerders. [Meer informatie](../administration/ootb-product-profiles.md#journey-administrator)


Nadat berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren bij het maken van berichten in de lijst **[!UICONTROL Presets]**.

## Een berichtvoorinstelling maken {#create-message-preset}

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor de voorinstelling in en selecteer vervolgens het kanaal of de kanalen die u wilt configureren.

   ![](../assets/preset-general.png)


   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook liggend `_`, punt`.` en afbreekstreepje `-` tekens gebruiken.

1. Configureer **e-mail**-instellingen.

   ![](../assets/preset-email.png)

   * Selecteer het type bericht dat wordt verzonden met de voorinstelling: **Transactioneel** of **Marketing**

      >[!CAUTION]
      >
      > **De berichten van de** Transactionalans kunnen worden verzonden naar profielen die van marketing mededelingen afzien. Deze berichten kunnen alleen worden verzonden in specifieke contexten, zoals het opnieuw instellen van wachtwoorden, de status van de bestelling en leveringsmeldingen.

   * Selecteer het subdomein dat u wilt gebruiken om de e-mails te verzenden. [Meer informatie](about-subdomain-delegation.md)
   * Selecteer de IP-pool die u aan de voorinstelling wilt koppelen. [Meer informatie](ip-pools.md)
   * Voer de headerparameters in voor de e-mails die u verzendt met de voorinstelling.

      >[!NOTE]
      >
      > * Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook liggend `_`, punt`.` en afbreekstreepje `-` tekens gebruiken.
         > 
         > 
      * Met uitzondering van het **Reageren op (e-mail door:sturen)**, moet het domein van e-mailadressen het huidige geselecteerde subdomein gebruiken.



1. Configureer **pushmelding**-instellingen.

   ![](../assets/preset-push.png)

   * Selecteer ten minste één platform: **iOS** en/of **Android**

   * Selecteer de mobiele toepassingen die u voor elk platform wilt gebruiken.

      Raadpleeg [deze sectie](../push-configuration.md) voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten.

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** om te bevestigen. U kunt de berichtvoorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](../assets/preset-submit.png)

1. Nadat de berichtvoorinstelling is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]**.

   Tijdens deze stap, zullen verscheidene controles worden uitgevoerd om te verifiëren dat het behoorlijk is gevormd. De verwerkingstijd is ongeveer **48h-72h**, en kan tot **7-10 dagen** duren.

   Deze controles omvatten leverbaarheidstests die door het team van de Adobe worden uitgevoerd:

   * SPF-validatie
   * DKIM-validatie
   * MX-recordvalidatie
   * Controle IPs voegend op lijst van gewenste personen
   * Helo host check
   * Verificatie van IP-pool
   * A/PTR-record, t/m/res-subdomeinverificatie

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
   >Gedetailleerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.

