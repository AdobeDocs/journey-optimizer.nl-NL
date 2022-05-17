---
title: Voorinstellingen voor berichten instellen
description: Leer hoe u berichtvoorinstellingen configureert en controleert
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '1490'
ht-degree: 1%

---

# Voorinstellingen voor berichten instellen {#message-presets-creation}

Met [!DNL Journey Optimizer]kunt u voorinstellingen voor berichten instellen die alle technische parameters definiëren die vereist zijn voor e-mail- en pushberichten: e-mailtype, e-mail en naam van de afzender, mobiele apps en meer.

>[!CAUTION]
>
> * Als u berichtvoorinstellingen wilt maken, bewerken en verwijderen, moet u beschikken over de [Voorinstellingen voor berichten beheren](../administration/high-low-permissions.md#manage-message-presets).
>
> * U moet [E-mailconfiguratie](#configure-email-settings) en [Pushconfiguratie](../configuration/push-configuration.md) stappen voordat u berichtvoorinstellingen maakt.


Zodra berichtvoorinstellingen zijn geconfigureerd, kunt u deze selecteren wanneer u berichten maakt van de **[!UICONTROL Presets]** lijst.

➡️ [Leer hoe u e-mailvoorinstellingen maakt en gebruikt in deze video](#video-presets)

## Een berichtvoorinstelling maken {#create-message-preset}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Gegevens en instellingen voor voorinstellingen voor berichten"
>abstract="Door een berichtvoorinstelling in te stellen, kunt u het kanaal selecteren waarop het van toepassing is en alle technische parameters definiëren die nodig zijn voor uw berichten, zoals het e-mailtype, het te gebruiken subdomein, de naam van de afzender, mobiele apps, enzovoort."

Ga als volgt te werk om een berichtvoorinstelling te maken:

1. Toegang krijgen tot **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** en klik vervolgens op **[!UICONTROL Create Message preset]**.

   ![](assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor de voorinstelling in en selecteer vervolgens het kanaal of de kanalen die u wilt configureren.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

1. Configureer de **email** instellingen. [Meer informatie](#configure-email-settings)

1. Configureer de **pushmelding** instellingen. [Meer informatie](#configure-push-settings)

   <!--Configure SMS settings. [Learn more](#configure-sms-settings) -->

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** ter bevestiging. U kunt de berichtvoorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >U kunt niet doorgaan met het maken van de voorinstelling terwijl de geselecteerde IP-pool zich onder [editie](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status) en is nooit gekoppeld aan het geselecteerde subdomein. [Meer informatie](#subdomains-and-ip-pools)
   >
   >Sla de voorinstelling op als concept en wacht tot de IP-pool de **[!UICONTROL Success]** status om het maken van de voorinstelling te hervatten.

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

   ![](assets/preset-active.png)

## E-mailinstellingen configureren {#configure-email-settings}

E-mailinstellingen worden gedefinieerd in een specifieke sectie van de configuratie van de berichtvoorinstelling.

![](assets/preset-email.png)

Uw instellingen configureren zoals beschreven in [deze sectie](email-settings.md).

## Pushinstellingen configureren {#configure-push-settings}

De duw montages worden bepaald in een specifiek gedeelte van de bericht vooraf ingestelde configuratie.

Voer de onderstaande stappen uit om de pushinstellingen te definiëren die zijn gekoppeld aan de berichtvoorinstelling:

1. Selecteer ten minste één platform: **iOS** en/of **Android**.

1. Selecteer de mobiele toepassingen die u voor elk platform wilt gebruiken.

![](assets/preset-push.png)

Raadpleeg voor meer informatie over het configureren van uw omgeving voor het verzenden van pushberichten de [deze sectie](../configuration/push-gs.md).

<!--
## Configure SMS settings {#configure-sms-settings}

1. Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**.

    ![](assets/preset-sms.png)
    
1. Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
    For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

## Voorinstellingen voor monitorberichten {#monitor-message-presets}

Alle voorinstellingen voor berichten worden weergegeven in het dialoogvenster **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** -menu. Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren (kanaaltype, gebruiker, status).

![](assets/preset-filters.png)

Zodra gecreeerd, kunnen de berichtvoorinstellingen de volgende statussen hebben:

* **[!UICONTROL Draft]**: De berichtvoorinstelling is opgeslagen als een concept en is nog niet verzonden. Open het om de configuratie te hervatten.
* **[!UICONTROL Processing]**: De berichtvoorinstelling is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Active]**: De berichtvoorinstelling is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de verificatie van de berichtvoorinstelling.
* **[!UICONTROL Deactivated]**: De berichtvoorinstelling is gedeactiveerd. Het kan niet worden gebruikt om nieuwe berichten tot stand te brengen.

Als het maken van een berichtvoorinstelling mislukt, worden de details van elke mogelijke oorzaak van een fout hieronder beschreven.

Als een van deze fouten optreedt, neemt u contact op met [Adobe Klantenservice](https://helpx.adobe.com/nl/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} voor hulp.

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

   ![](assets/preset-name.png)

1. Bewerk de eigenschappen naar wens.

   >[!NOTE]
   >
   >Als een berichtvoorinstelling de **[!UICONTROL Active]** status, de **[!UICONTROL Name]**, **[!UICONTROL Select channel]** en **[!UICONTROL Subdomain]** velden worden grijs weergegeven en kunnen niet worden bewerkt.

1. Klikken **[!UICONTROL Submit]** om uw wijzigingen te bevestigen.

   ![](assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >U kunt de berichtvoorinstelling ook opslaan als concept en de update later hervatten.

Nadat de wijzigingen zijn ingediend, doorloopt de berichtvoorinstelling een validatiecyclus die vergelijkbaar is met de validatiecyclus die op dat moment wordt toegepast [een voorinstelling maken](#create-message-preset).

>[!NOTE]
>
>Als u alleen de **[!UICONTROL Description]**, **[!UICONTROL Email type]** en/of **[!UICONTROL Email retry parameters]** in velden, wordt de update onmiddellijk uitgevoerd.

Voor voorinstellingen voor berichten met de **[!UICONTROL Active]** kunt u de details van de update controleren. Dit doet u als volgt:

* Klik op de knop **[!UICONTROL Recent update]** wordt weergegeven naast de naam van de actieve voorinstelling.

   ![](assets/preset-recent-update-icon.png)

* U kunt de updatedetails van een actieve berichtvooraf ingesteld ook toegang hebben terwijl de update bezig is.

   ![](assets/preset-view-update-details.png)

Op de **[!UICONTROL Recent update]** op het scherm, kunt u informatie zoals de updatestatus, en de lijst van gevraagde veranderingen zien.

![](assets/preset-recent-update-screen.png)

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

### Succes {#success}

Zodra het validatieproces is voltooid, wordt de nieuwe versie van de voorinstelling automatisch gebruikt in alle berichten die deze voorinstelling gebruiken. Het kan echter zijn dat u moet wachten:
* een paar minuten voordat het wordt verbruikt door de eenheidspublicaties,
* totdat de volgende batch voor de voorinstelling van kracht is in batchberichten.

### Mislukt {#failed}

Als het validatieproces mislukt, wordt de oudere versie van de voorinstelling nog steeds gebruikt.

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

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Gedetailleerde berichtvoorinstellingen kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze voorinstellingen worden gebruikt om berichten te verzenden.

U kunt een gedeactiveerde berichtvoorinstelling niet rechtstreeks bewerken. U kunt het bestand echter wel dupliceren en de kopie bewerken om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken. U kunt de toepassing ook opnieuw activeren en wachten tot de update is gelukt om deze te bewerken.

![](assets/preset-activate.png)

## Hoe kan ik-video{#video-presets}

Leer hoe te om berichtvoorinstellingen tot stand te brengen, hoe te om hen te gebruiken en hoe te om subdomain te delegeren en een IP pool tot stand te brengen.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
