---
solution: Journey Optimizer
product: journey optimizer
title: Het actieve activiteitenkanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van Live-activiteiten met Journey Optimizer
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 2%

---

# Aan de slag met Live activity-configuratie {#mobile-live-config}

>[!BEGINSHADEBOX]

* [Aan de slag met Live-activiteiten](get-started-mobile-live.md)
* **[Levende activiteitenconfiguratie](mobile-live-configuration.md)**
* [Integratie van live-activiteiten met Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* [Live-activiteiten maken](create-mobile-live.md)
* [Veelgestelde vragen](mobile-live-faq.md)
* [Rapport voor live-activiteitencampagne](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Voordat u uw Live-activiteit kunt verzenden, moet u de Adobe Journey Optimizer-omgeving configureren. Dit doet u als volgt:

## Stap 1: Voeg uw pushreferenties voor de app toe in Journey Optimizer (optioneel){#push-credentials-launch}

De registratie van de pushreferenties voor de mobiele app is vereist om Adobe te machtigen pushberichten namens u te verzenden.

Stap 1 is optioneel als uw pushgegevens al zijn geconfigureerd, omdat deze opnieuw kunnen worden gebruikt voor de configuratie van het kanaal Live activiteit. Als er geen referenties zijn gedefinieerd, moet u nieuwe pushreferenties voor uw app maken. Raadpleeg de onderstaande stappen:

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL Push settings]** > **[!UICONTROL Push credentials]**.

1. Klik op **[!UICONTROL Create push credential]**.

   ![](assets/credential-1.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Platform]** het besturingssysteem:

1. Voer de mobiele app **[!UICONTROL App ID]** in.

   ![](assets/credential-2.png)

1. Schakel de optie **[!UICONTROL Apply to all sandboxes]** in om deze pushgegevens beschikbaar te maken voor alle sandboxen. Als een specifieke zandbak zijn eigen geloofsbrieven voor het zelfde Platform en toepassings identiteitskaart paar heeft, zullen die zandbakspecifieke geloofsbrieven belangrijkheid nemen.

1. Schakel de knop **[!UICONTROL Manually enter push Credentials]** in om uw referenties toe te voegen.

1. Sleep het .p8 Apple Push Notification Authentication Key-bestand naar het bestand. Deze sleutel kan van de **Certificaten** worden verkregen, **herkenningstekens** en **Profielen** pagina.

1. Verstrek **Zeer belangrijke identiteitskaart**. Dit is een tekenreeks van 10 tekens die wordt toegewezen tijdens het maken van de p8-auttoets. Het kan onder **Sleutels** lusje in **Certificaten**, **Herkenningstekens** en **pagina van Profielen** worden gevonden.

1. Verstrek **identiteitskaart van het Team**. Dit is een tekenreekswaarde die u vindt op het tabblad Lidmaatschap.

1. Klik op **[!UICONTROL Submit]** om uw toepassingsconfiguratie te maken.

## Stap 2: Maak uw Live-activiteitsconfiguratie {#config-live-activity}

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** . Klik op de knop **[!UICONTROL Create channel configuration]**.

   ![](assets/config-1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in en selecteer vervolgens het WhatsApp-kanaal.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Selecteer **[!DNL Live activity]** als kanaal.

   ![](assets/config-2.png)

1. Selecteer **[!UICONTROL Marketing action(s)]** om toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. Meer informatie

1. Kies iOS als uw **[!UICONTROL Platform]** .

1. Selecteer van drop-down het zelfde **[!UICONTROL App id]** zoals voor uw [ hierboven gevormde duw credentie ](#push-credentials-launch) of kies bestaande.

   ![](assets/config-3.png)

1. Nadat alle parameters zijn geconfigureerd, klikt u op **[!UICONTROL Submit]** om te bevestigen. U kunt de kanaalconfiguratie als ontwerp ook bewaren en zijn configuratie later hervatten.

1. Nadat de kanaalconfiguratie is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]** .

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [ deze sectie ](../configuration/channel-surfaces.md).

1. Wanneer de controles succesvol zijn, krijgt de kanaalconfiguratie de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

U kunt nu de integratie starten met Adobe Experience Platform Mobile SDK om real-time, dynamische updates op het Lock Screen en Dynamic Island in te schakelen.

➡️ [ Leer meer op de integratie van Adobe Experience Platform Mobile SDK ](mobile-live-configuration-sdk.md)
