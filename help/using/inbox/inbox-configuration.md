---
title: Inbox-configuratie
description: Kanaalconfiguratie van Inbox
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# Postvak IN configureren {#inbox-configuration}

Alvorens u de kaartervaringen van de Inhoud door Inbox kunt leveren, moet u een **kanaalconfiguratie van 0} Inbox {in** bepalen. **[!UICONTROL Channel configurations]** Deze configuratie verbindt het oppervlak met toestemming, optionele toegangslabels en de locatie waar de ervaring wordt weergegeven op het web of in uw iOS- of Android-app. Voer de onderstaande stappen uit om een configuratie te maken:

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/inbox-configuration-1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer over de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer **[!UICONTROL Inbox]** kanaal.

   ![](assets/inbox-configuration-2.png)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Selecteer het platform waarop de Postvak IN-ervaring wordt toegepast.

   ![](assets/inbox-configuration-3.png)

1. Voor web:

   * Typ of selecteer in **[!UICONTROL Page URL]** de URL van de pagina waar het Postvak IN moet verschijnen. Gebruik deze optie als de ervaring beperkt is tot één pagina.

   * Definieer in **[!UICONTROL Location on page]** de plaatsing op de pagina, bijvoorbeeld het gebied of de id die uw site gebruikt voor het inbox-oppervlak. [Meer informatie](../web/web-configuration.md)

     ![](assets/inbox-configuration-4.png)

1. Voor iOS en Android:

   * Voer in **[!UICONTROL App id]** de id voor uw app in of selecteer deze, zodat de configuratie van toepassing is op de correcte iOS- of Android-build.

   * Geef in **[!UICONTROL Location or path inside the app]** het scherm, de route of de container op waarin gebruikers het Postvak IN moeten openen.

1. Verzend uw wijzigingen.

U kunt nu uw configuratie selecteren wanneer het creëren van uw Inbox ervaring.

➡️ [ volg de stappen die in deze pagina ](inbox-create.md) worden gedetailleerd
