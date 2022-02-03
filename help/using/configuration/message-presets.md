---
title: Voorinstellingen voor berichten maken
description: Leer hoe u berichtvoorinstellingen configureert en controleert
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 1%

---

# Voorinstellingen voor berichten maken {#message-presets-creation}

Met [!DNL Journey Optimizer]kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten: e-mailtype, e-mail en naam van de afzender, mobiele apps en meer.

>[!CAUTION]
>
> * Configuratie van voorinstellingen voor berichten is beperkt tot reisbeheerders. [Meer informatie](../administration/ootb-product-profiles.md#journey-administrator)
>
> * U moet e-mailconfiguratie uitvoeren en [Pushconfiguratie](../push-configuration.md) stappen voordat u berichtvoorinstellingen maakt.


Zodra berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren wanneer u berichten maakt van de **[!UICONTROL Presets]** lijst.

➡️ [Leer hoe u e-mailvoorinstellingen maakt en gebruikt in deze video](#video-presets)

## Een berichtvoorinstelling maken {#create-message-preset}

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Toegang krijgen tot **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor de voorinstelling in en selecteer vervolgens het kanaal of de kanalen die u wilt configureren.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

1. Configureer de **email** instellingen.

   ![](../assets/preset-email.png)

   * Selecteer het type bericht dat wordt verzonden met de voorinstelling: **Transactioneel** of **Marketing**

      >[!CAUTION]
      >
      > **Transactioneel** berichten kunnen worden verzonden naar profielen die zich niet meer hebben geabonneerd op marketingberichten. Deze berichten kunnen alleen worden verzonden in specifieke contexten, zoals het opnieuw instellen van wachtwoorden, de status van de bestelling en leveringsmeldingen.

   * Selecteer het subdomein dat u wilt gebruiken om de e-mails te verzenden. [Meer informatie](about-subdomain-delegation.md)
   * Selecteer de IP-pool die u aan de voorinstelling wilt koppelen. [Meer informatie](ip-pools.md)
   * Voer de headerparameters in voor de e-mails die u met die voorinstelling hebt verzonden.

      >[!CAUTION]
      >
      >E-mailadressen moeten de geselecteerde [gedelegeerd subdomein](about-subdomain-delegation.md).

      <!--CAUTION: Except for the **Reply to (forward email)** field-->

      * **[!UICONTROL Sender name]**: De naam van de afzender, zoals de naam van uw merk.

      * **[!UICONTROL Sender email]**: Het e-mailadres dat u voor uw communicatie wilt gebruiken. Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com* kunt u *contact@marketing.luma.com*.

      * **[!UICONTROL Reply to (name)]**: De naam die wordt gebruikt wanneer de ontvanger op de knop **Reageren** in hun e-mailclientsoftware.

      * **[!UICONTROL Reply to (email)]**: Het e-mailadres dat wordt gebruikt wanneer de ontvanger op de knop **Reageren** in hun e-mailclientsoftware. <!--The emails sent to this address will be forwarded to the **[!UICONTROL Reply to (forward email)]** address provided below. -->U moet een adres gebruiken dat op gedelegeerde subdomein wordt bepaald (bijvoorbeeld *reply@marketing.luma.com*), anders worden de e-mails verwijderd.

      * **[!UICONTROL Error email]**: Alle fouten die door ISPs na een paar dagen van post worden geproduceerd die (asynchrone stuitingen) worden ontvangen op dit adres.

      <!--**[!UICONTROL Reply to (forward email)]**: All emails received by [!DNL Journey Optimizer] for the delegated subdomain will be forwarded to this email address. You can specify any address, except an email address defined on the delegated subdomain. For example, if the delegated subdomain is *marketing.luma.com*, any address like *abc@marketing.luma.com* is prohibited.-->

      >[!NOTE]
      >
      >Met ingang van de release van oktober 2021 is het niet meer mogelijk een e-mailadres voor verzending te definiëren vanaf de [!DNL Journey Optimizer] gebruikersinterface. Als je alle e-mails wilt ontvangen door [!DNL Journey Optimizer] voor het gedelegeerde subdomein dat naar een specifiek e-mailadres moet worden doorgestuurd, neemt u contact op met de [Adobe-team voor klantenondersteuning](https://helpx.adobe.com/nl/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}. <!--move to Deprecated features section when created?-->

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

   * Configureer de **parameters voor e-mailpogingen**. Standaard worden de [periode voor opnieuw uitproberen](retries.md#retry-duration) is ingesteld op 84 uur, maar u kunt deze instelling aanpassen aan uw wensen.

      ![](../assets/preset-retry-paramaters.png)

      U moet een geheel-getalwaarde (in uren of notulen) binnen de volgende waaier ingaan:
      * Voor het e-mailtype voor marketing is de minimale herroepingstermijn 6 uur.
      * Voor transactie-e-mailtype is de minimale herroepingstermijn 10 minuten.
      * Voor beide e-mailtypen is de maximale hergebruiksperiode 84 uur (of 5040 minuten).


1. Configureer de **pushmelding** instellingen.

   ![](../assets/preset-push.png)

   * Selecteer ten minste één platform: **iOS** en/of **Android**

   * Selecteer de mobiele toepassingen die u voor elk platform wilt gebruiken.

      Raadpleeg voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten de [deze sectie](../push-gs.md).

<!--
1. Configure the **SMS** settings.

     ![](../assets/preset-sms.png)

    * Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**
    
    * Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
      For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

    * Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** ter bevestiging. U kunt de berichtvoorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](../assets/preset-submit.png)

1. Nadat de berichtvoorinstelling is gemaakt, wordt deze in de lijst weergegeven met de **[!UICONTROL Processing]** status.

   Tijdens deze stap, zullen verscheidene controles worden uitgevoerd om te verifiëren dat het behoorlijk is gevormd. De verwerkingstijd is ongeveer **48u-72u** en kan **7-10 werkdagen**.

   Deze controles omvatten configuratie en technische tests die door het team van Adobe worden uitgevoerd:

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

1. Als de controles zijn voltooid, wordt met de berichtvoorinstelling het volgende opgehaald **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Voorinstellingen voor monitorberichten {#monitor-message-presets}

Alle voorinstellingen voor berichten worden weergegeven in het dialoogvenster **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** -menu. Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren (kanaaltype, gebruiker, status).

![](../assets/preset-filters.png)

Voorinstellingen voor berichten kunnen de volgende statussen hebben:

* **[!UICONTROL Draft]**: De berichtvoorinstelling is opgeslagen als een concept en is nog niet verzonden. Open het om de configuratie te hervatten.
* **[!UICONTROL Processing]**: De berichtvoorinstelling is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Active]**: De berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de berichtvoorinstelling.
* **[!UICONTROL Deactivated]**: De berichtvoorinstelling is gedeactiveerd. Het kan niet worden gebruikt om nieuwe berichten tot stand te brengen.

Als het maken van een berichtvoorinstelling mislukt, worden de details van elke mogelijke oorzaak van een fout hieronder beschreven.

Als één van deze fouten voorkomt, contacteer [Adobe-team voor klantenondersteuning](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} voor hulp.

* **Validatie van SPF is mislukt**: SPF (het Kader van het Beleid van de Afzender) is een e-mailauthentificatieprotocol dat toestaat om erkende IPs te specificeren die e-mails van een bepaald subdomein kunnen verzenden. De de bevestigingsmislukking van SPF betekent dat de IP adressen in het SPF- verslag niet de IP adressen aanpassen die voor het verzenden van e-mails naar de brievenbusleveranciers worden gebruikt.

* **DKIM-validatie mislukt**: DKIM (DomainKeys Identified Mail) staat de ontvankelijke server toe om te verifiëren dat het ontvangen bericht door de echte afzender van het bijbehorende domein werd verzonden en dat de inhoud van het originele bericht niet op zijn manier werd veranderd. DKIM-validatiefout betekent dat de ontvangende mailservers de authenticiteit van de berichtinhoud en de koppeling met het verzendende domein niet kunnen verifiëren.:

* **Validatie van MX-record mislukt**: MX (Mail eXchange)-fout bij de validatie van records betekent dat de mailservers die verantwoordelijk zijn voor het accepteren van binnenkomende e-mails namens een bepaald subdomein niet correct zijn geconfigureerd.

* **Leverbaarheidsconfiguraties zijn mislukt**: Vanwege een van de volgende redenen kan een fout optreden in de configuraties van de aflevering:
   * Voegend op lijst van gewenste personen van toegewezen IPs
   * Ongeldig `helo` name
   * E-mails die worden verzonden vanuit andere IP&#39;s dan die welke zijn opgegeven in de IP-pool van de corresponderende voorinstelling
   * Kan geen e-mails verzenden naar postvakken van belangrijke ISP&#39;s, zoals Gmail en Yahoo

## Een berichtvoorinstelling bewerken {#edit-message-preset}

Volg onderstaande stappen om een berichtvoorinstelling te bewerken.

>[!NOTE]
>
>U kunt de **[!UICONTROL Push notification settings]**. Als een berichtvoorinstelling alleen is geconfigureerd voor het pushmeldingskanaal, kan dit niet worden bewerkt.

1. Klik in de lijst op de naam van een berichtvoorinstelling om deze te openen.

   ![](../assets/preset-name.png)

1. Bewerk de eigenschappen naar wens.

   >[!NOTE]
   >
   >Als een berichtvoorinstelling de **[!UICONTROL Active]** status, de **[!UICONTROL Name]**, **[!UICONTROL Select channel]** en **[!UICONTROL Subdomain]** velden worden grijs weergegeven en kunnen niet worden bewerkt.

1. Klikken **[!UICONTROL Submit]** om uw wijzigingen te bevestigen.

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >U kunt de berichtvoorinstelling ook opslaan als concept en de update later hervatten.

Nadat de wijzigingen zijn ingediend, doorloopt de berichtvoorinstelling een validatiecyclus die vergelijkbaar is met de validatiecyclus die op dat moment wordt toegepast [een voorinstelling maken](#create-message-preset).

>[!NOTE]
>
>Als u alleen de **[!UICONTROL Description]**, **[!UICONTROL Email type]** en/of **[!UICONTROL Email retry parameters]** in velden, wordt de update onmiddellijk uitgevoerd.

Voor voorinstellingen voor berichten met de **[!UICONTROL Active]** kunt u de details van de update controleren. Dit doet u als volgt:

* Klik op de knop **[!UICONTROL Recent update]** wordt weergegeven naast de naam van de actieve voorinstelling.

   ![](../assets/preset-recent-update-icon.png)

* U kunt de updatedetails van een actieve berichtvooraf ingesteld ook toegang hebben terwijl de update bezig is.

   ![](../assets/preset-view-update-details.png)

Op de **[!UICONTROL Recent update]** scherm, kunt u informatie zoals de updatestatus zien,<!--the approximate remaining time before completion (if validation is in progress)--> en de lijst met gevraagde wijzigingen.

![](../assets/preset-recent-update-screen.png)

### Statussen bijwerken {#update-statuses}

Een update voor een berichtvoorinstelling kan de volgende statussen hebben:

* **[!UICONTROL Processing]**: De berichtvoorinstellingsupdate is verzonden en voert verschillende verificatiestappen uit.
* **[!UICONTROL Success]**: De bijgewerkte berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de update van de berichtvoorinstelling.

Elke status wordt hieronder beschreven.

### Verwerking

Er worden verschillende controles op de leesbaarheid uitgevoerd om te controleren of de voorinstelling correct is bijgewerkt.

>[!NOTE]
>
>Als u alleen de **[!UICONTROL Description]**, **[!UICONTROL Email type]** en/of **[!UICONTROL Email retry parameters]** in velden, wordt de update onmiddellijk uitgevoerd.

De verwerkingstijd is ongeveer **48u-72u** en kan **7-10 werkdagen**. Meer informatie over de controles die zijn uitgevoerd tijdens de validatiecyclus in [deze sectie](#create-message-preset).

Als u een voorinstelling bewerkt die al actief was:

* Zijn status blijft behouden **[!UICONTROL Active]** terwijl het validatieproces bezig is.

* De **[!UICONTROL Recent update]** wordt naast de naam van de voorinstelling in de lijst met voorinstellingen voor berichten weergegeven.

* Tijdens het validatieproces worden de berichten die zijn geconfigureerd met deze voorinstelling, nog steeds gebruikt in de oudere versie van de voorinstelling.

>[!NOTE]
>
>U kunt een berichtvoorinstelling niet wijzigen terwijl de update bezig is. U kunt nog steeds op de naam klikken, maar alle velden worden grijs weergegeven. De wijzigingen worden pas doorgevoerd als de update is gelukt.

### Succes

Zodra het validatieproces is voltooid, wordt de nieuwe versie van de voorinstelling automatisch gebruikt in alle berichten die deze voorinstelling gebruiken. Het kan echter zijn dat u moet wachten:
* een paar minuten voordat het wordt verbruikt door de eenheidspublicaties,
* totdat de volgende batch voor de voorinstelling van kracht is in batchberichten.

<!--Changes made to a message preset with the **[!UICONTROL Active]** status will automatically be applied to all messages currently using this preset.-->

### Mislukt

Als het validatieproces mislukt, wordt de oudere versie van de voorinstelling nog steeds gebruikt.

<!--The possible update error types are as follows:
* **Authorization error**: the bearer token is invalid or not authorized.
* **Illegal modification**: an edit was performed on one or more non-allowed fields.
* **Precondition failed**: some fields can only have specific values and this has not been honored.-->

Meer informatie over mogelijke oorzaken van fouten vindt u in [deze sectie](#monitor-message-presets).

Als het bijwerken mislukt, kan de voorinstelling opnieuw worden bewerkt. U kunt op de naam van de component klikken en de instellingen bijwerken die moeten worden hersteld.

## Een berichtvoorinstelling uitschakelen {#deactivate-preset}

Als u een **[!UICONTROL Active]** bericht niet beschikbaar om nieuwe berichten tot stand te brengen, kunt u het deactiveren. De gepubliceerde berichten die gebruikmaken van deze voorinstelling worden echter niet beïnvloed en blijven werken.

>[!NOTE]
>
>U kunt een berichtvoorinstelling niet deactiveren terwijl een update wordt verwerkt. U moet wachten tot de update is gelukt of mislukt. Meer informatie over [voorinstellingen voor berichten bewerken](#edit-message-preset) en op de [updatestatus](#update-statuses).

1. Open de lijst met voorinstellingen voor berichten.

1. Klik op de knop **[!UICONTROL More actions]** knop.

1. Selecteer **[!UICONTROL Deactivate]**.

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>Gedetailleerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.

U kunt een gedeactiveerde berichtvoorinstelling niet rechtstreeks bewerken. U kunt het bestand echter wel dupliceren en de kopie bewerken om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken. U kunt de toepassing ook opnieuw activeren en wachten tot de update is gelukt om deze te bewerken.

![](../assets/preset-activate.png)

<!--1. Access the message presets list.

1. Deactivate the message preset that you want to edit.

1. Duplicate the deactivated message preset. A copy with the **[!UICONTROL Draft]** status is automatically added to the list.

    ![](../assets/preset-duplicated.png)

1. Open the duplicated message preset, modify it according to your needs, then submit your changes. The message preset will go through the same validation cycle as during the [creation step](#create-message-preset).

1. Once validated, it gets the **[!UICONTROL Active]** status and is ready to be used to create new messages.-->

## Hoe kan ik-video{#video-presets}

Leer hoe te om berichtvoorinstellingen tot stand te brengen, hoe te om hen te gebruiken en hoe te om subdomain te delegeren en een IP pool tot stand te brengen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
