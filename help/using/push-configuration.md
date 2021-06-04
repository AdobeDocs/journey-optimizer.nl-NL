---
title: Configuratie van pushmeldingen
description: Leer hoe u uw omgeving configureert voor het verzenden van pushmeldingen met Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 03d003682d796906fcf89af02aa98d549b5214a3
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Push-meldingskanaal {#push-notification-configuration} configureren

![](assets/do-not-localize/badge.png)

Voordat u begint met het verzenden van pushberichten met [!DNL Journey Optimizer], moet u instellingen definiëren in zowel [!DNL Adobe Experience Platform] als [!DNL Adobe Experience Platform Launch].

## Adobe Experience Platform-instellingen {#platform-settings}

Voer de volgende stappen uit om uw mobiele app in te stellen in [!DNL Adobe Experience Platform Launch]:

1. [Eigenschap- en bedrijfsrechten toewijzen](#push-rights)
1. [Voeg de pushgegevens van uw mobiele toepassing toe in de Platform launch](#push-credentials-launch).
1. [Maak Edge-](#edge-configuration) configuratie die door de  **[!UICONTROL Edge]** extensie wordt gebruikt om aangepaste gegevens van een mobiel apparaat naar  [!DNL Adobe Experience Platform]te sturen.
1. [Stel een eigenschap](#launch-property) Platform launch in.
1. [Publiceer de eigenschap](#publish-property).
1. [Configureer de ProfileDataSource](#configure-profiledatasource).

### Stap 1: Eigenschap- en bedrijfsrechten {#push-rights} toewijzen

Voordat u een mobiele toepassing maakt, moet u er eerst voor zorgen dat u over de juiste gebruikersmachtigingen beschikt of deze toewijst.

Raadpleeg [documentatie over Platform launches](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions) voor meer informatie over gebruikersbeheer met [!DNL Adobe Experience Platform Launch].

Eigenschap- en bedrijfsrechten toewijzen:

1. Open [!DNL Admin Console].

1. Selecteer op het tabblad **[!UICONTROL Products]** de **[!UICONTROL Adobe Experience Platform Launch]**-kaart.

   ![](assets/push_product_1.png)

1. Selecteer een bestaande **[!UICONTROL Product Profile]** of maak een nieuwe met de **[!UICONTROL New profile]** knoop. Raadpleeg de documentatie [Admin-console](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui) voor meer informatie over het maken van een nieuwe **[!UICONTROL New profile]**.

1. Selecteer **[!UICONTROL Property rights]** op het tabblad **[!UICONTROL Permissions]**.

   ![](assets/push_product_2.png)

1. Klik op **[!UICONTROL Add all]**. Hiermee voegt u de volgende rechten toe aan uw productprofiel:
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. Selecteer vervolgens **[!UICONTROL Company rights]** in het linkermenu.

   ![](assets/push_product_4.png)

1. Voeg de volgende rechten toe:

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. Klik op **[!UICONTROL Save]**.

Dit **[!UICONTROL Product profile]** toewijzen aan gebruikers:

1. Selecteer op [!DNL Admin Console] op het tabblad **[!UICONTROL Products]** de **[!UICONTROL Adobe Experience Platform Launch]**-kaart.

1. Selecteer de eerder geconfigureerde **[!UICONTROL Product profile]**.

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](assets/push_product_6.png)

1. Typ de naam of het e-mailadres van uw gebruiker en selecteer de gebruiker. Klik vervolgens op **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Als de gebruiker niet eerder in de Admin console werd gecreeerd, verwijs naar [gebruikersdocumentatie toevoegen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


U hebt nu de juiste gebruikersmachtigingen om een mobiele toepassing te maken en te configureren in [!DNL Adobe Experience Platform Launch].

### Stap 2: Uw pushgegevens voor mobiele toepassingen toevoegen in Platform launch {#push-credentials-launch}

Nadat u de juiste gebruikersmachtigingen hebt verleend, moet u nu uw pushgegevens voor mobiele toepassingen toevoegen in [!DNL Adobe Experience Platform Launch].

Raadpleeg de stappen in [Adobe Experience Platform Mobile SDK-documentatie](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer#configure-the-journey-optimizer-extension-in-launch) voor meer informatie en procedures over het toevoegen van pushgegevens voor mobiele toepassingen.

<!--
Note that to add push credentials in [!DNL Adobe Experience Platform Launch], the owner of the mobile app should fetch them from APNs/FCM.
1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. Select the **[!UICONTROL App Configurations]** tab in the left-hand panel and click **[!UICONTROL App Configuration]** to create a new configuration.

1. Enter a **[!UICONTROL Name]** for the configuration.

1. From the **[!UICONTROL Messaging Service Type]** drop-down menu, select the **[!UICONTROL Messaging service type]** to be used for these credentials. Here, we selected **[!UICONTROL Apple Push Notification Service]** since we are working with iOS.

1. Enter the mobile app **[!UICONTROL Bundle Id]** in the **[!UICONTROL App ID (iOS Bundle ID)]** field if you are using Apple push notification service or in the **[!UICONTROL App ID (Android package name)]** field if you are using Firebase Cloud Messaging.

    ![](assets/push_launch_app_configuration.png)

1. Drag and drop the .p8 key file or the .json private key file to the **[!UICONTROL Push Credentials]** field.

1. Enter the **[!UICONTROL Key Id]** and **[!UICONTROL Team Id]** if you are using Apple push notification service.

1. Click **[!UICONTROL Save]** to create your app configuration.
-->

### Stap 3: Edge-configuratie {#edge-configuration} maken

**[!UICONTROL Edge configuration]** wordt gebruikt door de  **[!UICONTROL Edge]** extensie om aangepaste gegevens van een mobiel apparaat naar  [!DNL Adobe Experience Platform]te verzenden.
Als u [!DNL Adobe Experience Platform] wilt configureren, moet u de naam **[!UICONTROL Sandbox]** en **[!UICONTROL Event Dataset]** opgeven.

Raadpleeg de stappen in [Adobe Experience Platform Mobile SDK-documentatie](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams) voor meer informatie en procedures over het maken van **[!UICONTROL Edge configuration]**.


<!--
1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)
-->

### Stap 4: Een Platform launch-eigenschap {#launch-property} instellen

Als u een eigenschap [!DNL Adobe Experience Platform Launch] instelt, kan de ontwikkelaar of markator van de mobiele app de kenmerken van de mobiele SDK configureren, zoals Session Timeouts, de [!DNL Adobe Experience Platform]-sandbox die als doel moet worden gebruikt en de **[!UICONTROL Adobe Experience Platform Datasets]** die voor mobiele SDK moet worden gebruikt om gegevens naar te verzenden.

Raadpleeg de stappen in [Adobe Experience Platform Mobile SDK-documentatie](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property) voor meer informatie en procedures over het instellen van een **[!UICONTROL Platform Launch property]**.

Als u de SDK&#39;s die nodig zijn voor pushmeldingen wilt gebruiken, hebt u de volgende SDK-extensies nodig voor zowel Android als iOS:

* **[!UICONTROL Mobile Core]** (automatisch geïnstalleerd)
* **[!UICONTROL Profile]** (automatisch geïnstalleerd)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optioneel, maar aanbevolen voor foutopsporing in de mobiele implementatie.

Raadpleeg [documentatie over Platform launches](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html) voor meer informatie over [!DNL Adobe Experience Platform Launch]-extensies.

<!--

1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

### Stap 5: De eigenschap {#publish-property} publiceren

U moet nu de eigenschap publiceren om uw configuratie te integreren en deze in de mobiele app te gebruiken.

Raadpleeg de stappen in [Adobe Experience Platform Mobile SDK-documentatie](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration) voor het publiceren van de eigenschap

### Stap 6: De ProfileDataSource {#configure-profiledatasource} configureren

Als u de `ProfileDataSource` wilt configureren, gebruikt u `ProfileDCInletURL` vanuit [!DNL Adobe Experience Platform] en voegt u het volgende toe in de mobiele app:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->

### Stap 7: Een berichtvoorinstelling maken {#message-preset}

Als uw mobiele app is ingesteld in [!DNL Adobe Experience Platform Launch], moet u een berichtvoorinstelling maken om pushberichten te kunnen verzenden vanuit **[!DNL Journey Optimizer]**.

Leer hoe u een berichtvoorinstelling maakt en configureert in [deze sectie](configuration/message-presets.md).