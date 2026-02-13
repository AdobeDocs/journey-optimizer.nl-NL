---
solution: Journey Optimizer
product: journey optimizer
title: Configuratie van pushmeldingen
description: Leer hoe u uw omgeving configureert voor het verzenden van pushmeldingen met Journey Optimizer
feature: Push, Channel Configuration
role: Admin
level: Intermediate
exl-id: d8de1524-9d71-4978-86f5-1cd46f2e265c
source-git-commit: bd1bb6156427fc9539a60119f909b67c505d5a1c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 2%

---

# Meldingskanaal voor webpushmeldingen configureren {#push-notification-configuration}

Met [!DNL Journey Optimizer] kunt u uw reizen maken en berichten verzenden naar een doelgroep. Voordat u webpushmeldingen begint te verzenden met [!DNL Journey Optimizer] , moet u ervoor zorgen dat er configuraties en integratie zijn in Adobe Experience Platform. Om de de gegevensstroom van de Berichten van de Duw in [!DNL Adobe Journey Optimizer] te begrijpen gelieve te verwijzen naar [&#x200B; deze pagina &#x200B;](push-gs.md).

>[!AVAILABILITY]
>
>Het nieuwe **Mobiele onboarding snelle beginwerkschema** is nu beschikbaar. Met deze nieuwe productfunctie kunt u de Mobile SDK snel configureren om gegevens van mobiele gebeurtenissen te verzamelen en te valideren en om mobiele pushberichten te verzenden. Dit vermogen is toegankelijk via de homepage van de Inzameling van Gegevens als openbare bèta. [Meer informatie](mobile-onboarding-wf.md)
>

## Voordat u begint {#start-push}

### Machtigingen instellen {#setup-permissions}

Voordat u een mobiele toepassing maakt, moet u er eerst voor zorgen dat u over de juiste gebruikersmachtigingen voor tags in Adobe Experience Platform beschikt of deze toewijst. Leer meer in [&#x200B; documentatie van Markeringen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=nl-NL){target="_blank"}.

>[!CAUTION]
>
>De duimconfiguratie moet door een deskundige gebruiker worden uitgevoerd. Afhankelijk van uw implementatiemodel en persona&#39;s betrokken bij deze implementatie, zou u de volledige reeks toestemmingen aan één enkel productprofiel kunnen moeten toewijzen of toestemmingen tussen de app ontwikkelaar en **Adobe Journey Optimizer** beheerder delen. Leer meer over **toestemmingen van Markeringen** in [&#x200B; deze documentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=nl-NL){target="_blank"}.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

Om **Bezit** en **bedrijf** rechten toe te wijzen, volg hieronder de stappen:

1. Open de lus **[!DNL Admin Console]** .

1. Selecteer op het tabblad **[!UICONTROL Products]** de **[!UICONTROL Adobe Experience Platform Data Collection]** -kaart.

   ![](assets/push_product_1.png)

1. Selecteer een bestaande **[!UICONTROL Product Profile]** of maak een nieuwe **[!UICONTROL New profile]** met de knop. Leer hoe te om een nieuw **[!UICONTROL New profile]** in de [&#x200B; Admin consoledocumentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html?lang=nl-NL#ui){target="_blank"} tot stand te brengen.

1. Selecteer op het tabblad **[!UICONTROL Permissions]** de optie **[!UICONTROL Property rights]**.

   ![](assets/push_product_2.png)

1. Klik op **[!UICONTROL Add all]**. Hiermee voegt u het volgende recht toe aan uw productprofiel:
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   Deze machtigingen zijn vereist voor het installeren en publiceren van de Adobe Journey Optimizer-extensie en het publiceren van de app-eigenschap in Adobe Experience Platform Mobile SDK.

1. Selecteer vervolgens **[!UICONTROL Company rights]** in het linkermenu.

   ![](assets/push_product_4.png)

1. Voeg de volgende rechten toe:

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   Deze toestemmingen worden vereist voor de mobiele toepassingsontwikkelaar aan opstellings dupgeloofsbrieven in **de Inzameling van Gegevens van Adobe Experience Platform** en bepalen de het kanaalconfiguraties van het Duwbericht (d.w.z. berichtvoorinstellingen) in **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. Klik op **[!UICONTROL Save]**.

Volg onderstaande stappen om deze **[!UICONTROL Product profile]** aan gebruikers toe te wijzen:

1. Open de lus **[!DNL Admin Console]** .

1. Selecteer op het tabblad **[!UICONTROL Products]** de **[!UICONTROL Adobe Experience Platform Data Collection]** -kaart.

1. Selecteer de eerder geconfigureerde **[!UICONTROL Product profile]**.

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](assets/push_product_6.png)

1. Typ de naam of het e-mailadres van uw gebruiker en selecteer de gebruiker. Klik vervolgens op **[!UICONTROL Save]** .

   >[!NOTE]
   >
   >Als de gebruiker niet eerder in de console Admin werd gecreeerd, verwijs naar [&#x200B; gebruikersdocumentatie &#x200B;](https://helpx.adobe.com/nl/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users) toevoegen.

   ![](assets/push_product_7.png)


### Controleer uw gegevenssets {#push-datasets}

De volgende schema&#39;s en datasets zijn beschikbaar met het kanaal van de dupmelding:

| Schema <br> Dataset | Groep velden | Bewerking |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM het Schema van het Profiel van de Duw <br> Dataset van het Profiel van CJM | De Details van het Push- Bericht <br> Adobe CJM ExperienceEvent - de Details van het Profiel van het Bericht <br> Adobe CJM ExperienceEvent - de Details van de Uitvoering van het Bericht <br> de Details van de Toepassing <br> Milieu Details | Push Token registreren |
| CJM het Schema van de Gebeurtenis van de Ervaring van het Push Volgen CJM <br> CJM de Dataset van de Gebeurtenis van de Draagervaring | Push Notification Tracking | Interacties bijhouden en gegevens verstrekken voor de rapportageinterface |


>[!NOTE]
>
>Wanneer gebeurtenissen voor het bijhouden van push-gegevens worden opgenomen in de CJM-gegevensset voor het bijhouden van push-ervaringen, kunnen er fouten optreden, ook al worden gegevens gedeeltelijk met succes opgenomen. Dit kan voorkomen als sommige gebieden in uw afbeelding niet in inkomende gebeurtenissen bestaan: het systeem registreert waarschuwingen maar verhindert niet inname van geldige gedeelten van de gegevens. Deze waarschuwingen worden in batch-status weergegeven als &#39;mislukt&#39;, maar geven gedeeltelijk succes bij inname aan.
>
>Om de volledige lijst van gebieden en attributen voor elk schema te bekijken, raadpleeg het [&#x200B; het schemawoordenboek van Journey Optimizer &#x200B;](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL){target="_blank"}.

### De eigenschap pushNotification configureren {#push-property}

Om **Push berichten van het Web** toe te laten, moet u eerst ervoor zorgen dat het [&#x200B; pushNotifications bezit &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/js/commands/configure/pushnotifications) behoorlijk binnen het Web SDK wordt gevormd. Deze eigenschap bepaalt hoe pushmeldingen worden verwerkt door uw webtoepassing.

Bovendien, moet u sleutels produceren VAPID, die worden vereist om [&#x200B; uw geloofsbrieven van de toepassingsduw &#x200B;](#push-credentials-launch) in Journey Optimizer te vormen.

## Stap 1: Voeg uw pushreferenties voor de app toe in Journey Optimizer {#push-credentials-launch}

Nadat u de juiste gebruikersmachtigingen hebt verleend, moet u nu uw pushgegevens voor mobiele toepassingen toevoegen in Journey Optimizer.

De registratie van de pushreferenties voor de mobiele app is vereist om Adobe te machtigen pushberichten namens u te verzenden. Raadpleeg de onderstaande stappen:

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL Push settings]** > **[!UICONTROL Push credentials]**.

1. Klik op **[!UICONTROL Create push credential]**.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Platform]** de optie **[!UICONTROL Web]** .

   ![](assets/add-app-config-web.png)

1. Geef de **[!UICONTROL App ID]** op.

1. Voer de **[!UICONTROL VAPID public key]** en **[!UICONTROL private key]** in.

1. Klik op **[!UICONTROL Submit]** om uw toepassingsconfiguratie te maken.

## Stap 2: Creeer een kanaalconfiguratie voor duw{#message-preset}

Wanneer u uw pushreferenties hebt gemaakt, moet u een configuratie maken om pushmeldingen te kunnen verzenden vanuit **[!DNL Journey Optimizer]** .

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/push-config-9.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.


1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [&#x200B; leer meer over de Controle van de Toegang van het Niveau van Objecten (OLAC) &#x200B;](../administration/object-based-access.md).

1. Selecteer **kanaal van de Duw**.

   ![](assets/push-config-10.png)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Kies uw **[!UICONTROL Platform]**: Android, iOS en/of Web.

1. Selecteer het zelfde **[!UICONTROL App id]** zoals voor uw [&#x200B; hierboven gevormde dupreferentie &#x200B;](#push-credentials-launch).

1. Sla uw wijzigingen op.

U kunt nu uw configuratie selecteren wanneer u pushmeldingen maakt.

## Stap 3: Vorm het sendPushSubscription bezit {#sendPushSubscription-property}

Zodra uw pushgeloofsbrieven en kanaalconfiguratie opstelling zijn, moet u [&#x200B; het sendPushSubscription bevel &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/js/commands/sendpushsubscription) in uw Webtoepassing uitvoeren. Met deze opdracht registreert u pushabonnementen van gebruikers bij Adobe Experience Platform, zodat het systeem kan bijhouden welke gebruikers zich hebben aangemeld voor het ontvangen van pushberichten en hun abonnementsstatus kunnen behouden. Deze registratie is essentieel voor Journey Optimizer om gerichte pushberichten naar uw gebruikers te sturen.

## Stap 4: Test uw mobiele app met een gebeurtenis {#mobile-app-test}

Nadat u de webpushconfiguratie in zowel Adobe Experience Platform als [!DNL Adobe Experience Platform Data Collection] hebt voltooid, kunt u uw implementatie testen voordat u pushberichten naar uw profielen verzendt. Door te testen zorgt u ervoor dat abonnementen correct zijn geregistreerd en dat meldingen correct worden verzonden naar de browsers van uw gebruikers.

Voor gedetailleerde instructies bij het creëren van een testreis met gebeurtenissen om uw opstelling van de Webduw te bevestigen, verwijs naar de [&#x200B; mobiele documentatie van de het berichtconfiguratie van de app duw &#x200B;](push-configuration.md), die een uitvoerige testende werkschema toepasselijk op zowel mobiele als Webdrukkanalen verstrekt.
