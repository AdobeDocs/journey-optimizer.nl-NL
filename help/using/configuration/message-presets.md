---
title: Voorinstellingen voor berichten maken
description: Leer hoe u berichtvoorinstellingen configureert en controleert
feature: Applicatie-instellingen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: 705aa4c238eb1d6d6ce46b68f8690f639124a090
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 1%

---


# Voorinstellingen voor berichten maken

Met [!DNL Journey Optimizer] kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten: e-mailtype, e-mail en naam van de afzender, mobiele apps en meer.

>[!CAUTION]
>
> * Configuratie van voorinstellingen voor berichten is beperkt tot reisbeheerders. [Meer informatie](../administration/ootb-product-profiles.md#journey-administrator)
   >
   > 
* U moet de configuratiestappen E-mail en van de Duw uitvoeren alvorens berichtvoorinstellingen te creëren.


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

      >[!CAUTION]
      >
      >Met uitzondering van het veld **Reageren op (e-mail doorsturen)** moet het domein voor e-mailadressen het geselecteerde [gedelegeerde subdomein](about-subdomain-delegation.md) gebruiken.

      * **[!UICONTROL Sender name]**: Naam van de afzender, zoals de naam van uw merk.

      * **[!UICONTROL Sender email]**: Het e-mailadres dat u voor uw communicatie wilt gebruiken. Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com* is, kunt u *contact@marketing.luma.com* gebruiken.

      * **[!UICONTROL Reply to (name)]**: De naam die wordt gebruikt wanneer de ontvanger op de  **** knop Replay-out klikt in zijn e-mailclientsoftware.

      * **[!UICONTROL Reply to (email)]**: Het e-mailadres dat wordt gebruikt wanneer de ontvanger op de  **** knop Replay-out klikt in de software van zijn e-mailclient. De e-mails die naar dit adres worden verzonden, worden doorgestuurd naar het onderstaande **[!UICONTROL Reply to (forward email)]**-adres. U moet een adres gebruiken dat op gedelegeerde subdomain (bijvoorbeeld *reply@marketing.luma.com*) wordt bepaald, anders zullen de e-mails worden gelaten vallen.

      * **[!UICONTROL Reply to (forward email)]**: Alle e-mails die zijn ontvangen door  [!DNL Journey Optimizer] voor het gedelegeerde subdomein worden doorgestuurd naar dit e-mailadres. U kunt elk adres opgeven, behalve een e-mailadres dat is gedefinieerd in het gedelegeerde subdomein. Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com* is, is elk adres zoals *abc@marketing.luma.com* niet toegestaan.

      * **[!UICONTROL Error email]**: Alle fouten die door ISPs na een paar dagen van post worden geproduceerd die (asynchrone stuitingen) worden ontvangen op dit adres.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook liggend `_`, punt`.` en afbreekstreepje `-` tekens gebruiken.


1. Configureer **pushmelding**-instellingen.

   ![](../assets/preset-push.png)

   * Selecteer ten minste één platform: **iOS** en/of **Android**

   * Selecteer de mobiele toepassingen die u voor elk platform wilt gebruiken.

      Raadpleeg [deze sectie](../push-gs.md) voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten.

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

