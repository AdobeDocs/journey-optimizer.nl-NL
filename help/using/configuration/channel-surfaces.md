---
title: Kanaaloppervlakken instellen
description: Leer hoe u kanaaloppervlakken configureert en controleert
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Kanaaloppervlakken instellen {#set-up-channel-surfaces}

Met [!DNL Journey Optimizer]kunt u kanaaloppervlakken instellen (dus voorinstellingen voor berichten) die alle technische parameters definiëren die nodig zijn voor uw berichten: e-mailtype, e-mail en naam van de afzender, mobiele apps, configuratie van SMS en meer.

>[!CAUTION]
>
> * Als u kanaaloppervlakken wilt maken, bewerken en verwijderen, moet u beschikken over de [Kanaaloppervlak beheren](../administration/high-low-permissions.md#manage-channel-surface) toestemming.
>
> * U moet de opdracht [E-mailconfiguratie](#configure-email-settings), [Pushconfiguratie](../configuration/push-configuration.md) en [SMS-configuratie](../configuration/sms-configuration.md) stappen voordat u kanaaloppervlakken maakt.


Zodra de kanaaloppervlakten zijn gevormd, zult u hen kunnen selecteren wanneer het creëren van berichten van een reis.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Een kanaaloppervlak maken {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Instellingen voor kanaaloppervlak"
>abstract="Wanneer u een kanaaloppervlak instelt, selecteert u het kanaal waarop het van toepassing is en definieert u alle technische parameters die voor uw berichten vereist zijn, zoals het e-mailtype, subdomein, de naam van de afzender, mobiele apps, de configuratie van SMS en meer."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Instellingen voor kanaaloppervlak"
>abstract="Wanneer u een kanaaloppervlak instelt, selecteert u het kanaal waarop het van toepassing is en definieert u alle technische parameters die voor uw berichten vereist zijn, zoals het e-mailtype, de naam van de afzender, mobiele apps, de configuratie van SMS en meer."

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

Op de **[!UICONTROL Recent update]** op het scherm, kunt u informatie zoals de updatestatus, en de lijst van gevraagde veranderingen zien.

<!--![](assets/preset-recent-update-screen.png)-->

### Statussen bijwerken {#update-statuses}

Een update van een kanaaloppervlak kan de volgende statussen hebben:

* **[!UICONTROL Processing]**: De update van het kanaaloppervlak is verzonden en wordt door verschillende verificatiestappen uitgevoerd.
* **[!UICONTROL Success]**: Het bijgewerkte kanaaloppervlak is geverifieerd en kan worden geselecteerd om berichten te maken.
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt tijdens de update-verificatie van het kanaaloppervlak.

Elke status wordt hieronder beschreven.

#### Verwerking {#surface-processing}

Er zullen verschillende controles op de aflevering worden uitgevoerd om na te gaan of de oppervlakte correct is bijgewerkt.

>[!NOTE]
>
>Als u alleen de **[!UICONTROL Description]**, **[!UICONTROL Email type]** en/of **[!UICONTROL Email retry parameters]** in velden, wordt de update onmiddellijk uitgevoerd.

De verwerkingstijd kan maximaal **3 uur**. Meer informatie over de controles die zijn uitgevoerd tijdens de validatiecyclus in [deze sectie](#create-channel-surface).

Als u een oppervlak bewerkt dat al actief was:

* Zijn status blijft behouden **[!UICONTROL Active]** terwijl het validatieproces bezig is.

* De **[!UICONTROL Recent update]** wordt naast de naam van het oppervlak in de lijst met kanaaloppervlakken weergegeven.

* Tijdens het bevestigingsproces, gebruiken de berichten die gebruikend dit oppervlak worden gevormd nog de oudere versie van de oppervlakte.

>[!NOTE]
>
>U kunt een kanaaloppervlak niet wijzigen terwijl de update wordt uitgevoerd. U kunt nog steeds op de naam klikken, maar alle velden worden grijs weergegeven. De wijzigingen worden pas doorgevoerd als de update is gelukt.

#### Succes {#success}

Zodra het validatieproces is voltooid, wordt de nieuwe versie van het oppervlak automatisch gebruikt in alle berichten die dit oppervlak gebruiken. Het kan echter zijn dat u moet wachten:
* een paar minuten voordat het wordt verbruikt door de eenheidspublicaties,
* tot de volgende batch voor het oppervlak effectief is in batchberichten.

#### Mislukt {#failed}

Als het validatieproces mislukt, wordt de oudere versie van het oppervlak nog steeds gebruikt.

Meer informatie over mogelijke oorzaken van fouten vindt u in [deze sectie](#monitor-channel-surfaces).

Als de update mislukt, wordt het oppervlak opnieuw bewerkbaar. U kunt op de naam van de component klikken en de instellingen bijwerken die moeten worden hersteld.

## Een kanaaloppervlak deactiveren {#deactivate-a-surface}

Als u een **[!UICONTROL Active]** kanaaloppervlak niet beschikbaar om nieuwe berichten te maken, kunt u het deactiveren. De berichten over reizen die momenteel op dit oppervlak worden gebruikt, zullen echter niet worden beïnvloed en blijven werken.

>[!NOTE]
>
>U kunt een kanaaloppervlak niet deactiveren terwijl een update wordt verwerkt. U moet wachten tot de update is gelukt of mislukt. Meer informatie over [kanaaloppervlakken bewerken](#edit-channel-surface) en op de [updatestatus](#update-statuses).

1. Open de lijst met kanaaloppervlakken.

1. Voor het actieve oppervlak van uw keuze klikt u op de knop **[!UICONTROL More actions]** knop.

1. Selecteer **[!UICONTROL Deactivate]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Gedeactiveerde kanaaloppervlakken kunnen niet worden verwijderd om problemen te voorkomen tijdens reizen waarbij deze oppervlakken worden gebruikt om berichten te verzenden.

U kunt een gedeactiveerd kanaaloppervlak niet rechtstreeks bewerken. U kunt het bestand echter wel dupliceren en de kopie bewerken om een nieuwe versie te maken waarmee u nieuwe berichten kunt maken. U kunt de toepassing ook opnieuw activeren en wachten tot de update is gelukt om deze te bewerken.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
