---
title: Voorinstellingen voor berichten maken
description: Leer hoe u berichtvoorinstellingen configureert en controleert
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: b2eedebb42f878cec0e7747e015693fad4667cff
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---


# Voorinstellingen voor berichten maken

Met [!DNL Journey Optimizer] kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten: e-mailtype, e-mail en naam van de afzender, mobiele apps en meer.

>[!CAUTION]
>
> * Configuratie van voorinstellingen voor berichten is beperkt tot reisbeheerders. [Meer informatie](../administration/ootb-product-profiles.md#journey-administrator)
>
> * U moet de configuratiestappen E-mail en van de Duw uitvoeren alvorens berichtvoorinstellingen te creëren.


Nadat berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren bij het maken van berichten in de lijst **[!UICONTROL Presets]**.

➡️ [Meer informatie over het maken en gebruiken van e-mailvoorinstellingen in deze video](#video-presets)

## Een berichtvoorinstelling maken {#create-message-preset}

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor de voorinstelling in en selecteer vervolgens het kanaal of de kanalen die u wilt configureren.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook liggend `_`, punt`.` en afbreekstreepje `-` tekens gebruiken.

1. Configureer de **e-mail**-instellingen.

   ![](../assets/preset-email.png)

   * Selecteer het type bericht dat wordt verzonden met de voorinstelling: **Transactioneel** of **Marketing**

      >[!CAUTION]
      >
      > **De berichten van de** Transactionalans kunnen worden verzonden naar profielen die van marketing mededelingen afzien. Deze berichten kunnen alleen worden verzonden in specifieke contexten, zoals het opnieuw instellen van wachtwoorden, de status van de bestelling en leveringsmeldingen.

   * Selecteer het subdomein dat u wilt gebruiken om de e-mails te verzenden. [Meer informatie](about-subdomain-delegation.md)
   * Selecteer de IP-pool die u aan de voorinstelling wilt koppelen. [Meer informatie](ip-pools.md)
   * Voer de headerparameters in voor de e-mails die u met die voorinstelling hebt verzonden.

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

   * Configureer de **e-mailparameters opnieuw proberen**. Standaard is de [retry time period](retries.md#retry-duration) ingesteld op 84 uur, maar u kunt deze instelling aanpassen aan uw wensen.

      ![](../assets/preset-retry-paramaters.png)

      U moet een geheel-getalwaarde (in uren of notulen) binnen de volgende waaier ingaan:
      * Voor het e-mailtype voor marketing is de minimale herroepingstermijn 6 uur.
      * Voor transactie-e-mailtype is de minimale herroepingstermijn 10 minuten.
      * Voor beide e-mailtypen is de maximale hergebruiksperiode 84 uur (of 5040 minuten).


1. Configureer de **instellingen voor pushmeldingen**.

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

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [deze sectie](#monitor-message-presets).

1. Als de controles zijn voltooid, krijgt de berichtvoorinstelling de status **[!UICONTROL Active]**. Het is klaar om te worden gebruikt om berichten te leveren.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Voorinstellingen voor monitorberichten {#monitor-message-presets}

Alle voorinstellingen voor berichten worden weergegeven in het menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**. Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren (kanaaltype, gebruiker, status).

![](../assets/preset-filters.png)

Voorinstellingen voor berichten kunnen de volgende statussen hebben:

* **[!UICONTROL Draft]**: De berichtvoorinstelling is opgeslagen als een concept en is nog niet verzonden. Open het om de configuratie te hervatten.
* **[!UICONTROL Processing]**: De berichtvoorinstelling is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Active]**: De berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de berichtvoorinstelling.
* **[!UICONTROL De-activated]**: De berichtvoorinstelling is gedeactiveerd. Het kan niet worden gebruikt om nieuwe berichten tot stand te brengen.

Als het maken van een berichtvoorinstelling mislukt, worden de details van elke mogelijke oorzaak van een fout hieronder beschreven.

Als één van deze fouten voorkomt, contacteer [Adobe het Team van de Steun van de Zorg van de Klant ](https://helpx.adobe.com/nl/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} om hulp te krijgen.

* **Validatie van SPF is mislukt**: SPF (het Kader van het Beleid van de Afzender) is een e-mailauthentificatieprotocol dat toestaat om erkende IPs te specificeren die e-mails van een bepaald subdomein kunnen verzenden. De de bevestigingsmislukking van SPF betekent dat de IP adressen in het SPF- verslag niet de IP adressen aanpassen die voor het verzenden van e-mails naar de brievenbusleveranciers worden gebruikt.

* **DKIM-validatie mislukt**: DKIM (DomainKeys Identified Mail) staat de ontvankelijke server toe om te verifiëren dat het ontvangen bericht door de echte afzender van het bijbehorende domein werd verzonden en dat de inhoud van het originele bericht niet op zijn manier werd veranderd. DKIM-validatiefout betekent dat de ontvangende mailservers de authenticiteit van de berichtinhoud en de koppeling met het verzendende domein niet kunnen verifiëren.:

* **Validatie van MX-record mislukt**: MX (Mail eXchange)-fout bij de validatie van records betekent dat de mailservers die verantwoordelijk zijn voor het accepteren van binnenkomende e-mails namens een bepaald subdomein niet correct zijn geconfigureerd.

* **Leverbaarheidsconfiguraties zijn mislukt**: Vanwege een van de volgende redenen kan een fout optreden in de configuraties van de aflevering:
   * Voegend op lijst van gewenste personen van toegewezen IPs
   * Ongeldige naam `helo`
   * E-mails die worden verzonden vanuit andere IP&#39;s dan die welke zijn opgegeven in de IP-pool van de corresponderende voorinstelling
   * Kan geen e-mails verzenden naar postvakken van belangrijke ISP&#39;s, zoals Gmail en Yahoo

## Voorinstellingen voor berichten bewerken

Als u een berichtvoorinstelling wilt bewerken, moet u deze eerst deactiveren zodat deze niet beschikbaar is voor het maken van nieuwe berichten (gepubliceerde berichten met deze voorinstelling worden niet beïnvloed en blijven werken). Vervolgens moet u de berichtvoorinstelling dupliceren om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken:

1. Open de lijst met voorinstellingen voor berichten en activeer vervolgens de berichtvoorinstelling die u wilt bewerken.

   ![](../assets/preset-deactivate.png)

1. Dupliceer de uitgeschakelde berichtvoorinstelling. Er wordt automatisch een kopie met de status **[!UICONTROL Draft]** toegevoegd aan de lijst.

   ![](../assets/preset-duplicated.png)

1. Open de gedupliceerde voorinstelling voor berichten, wijzig deze naar wens en verzend uw wijzigingen. De berichtvoorinstelling doorloopt dezelfde validatiecyclus als tijdens de [aanmaakstap](#create-message-preset).

1. Zodra bevestigd, krijgt het de **[!UICONTROL Active]** status en is klaar om worden gebruikt om nieuwe berichten tot stand te brengen.

   >[!NOTE]
   >
   >De-geactiveerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.

## Hoe kan ik-video{#video-presets}

Leer hoe te om berichtvoorinstellingen tot stand te brengen, hoe te om hen te gebruiken en hoe te om subdomain te delegeren en een IP pool tot stand te brengen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
