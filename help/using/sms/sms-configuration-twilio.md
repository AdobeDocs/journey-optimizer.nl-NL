---
solution: Journey Optimizer
product: journey optimizer
title: Twilio-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# Twilio-provider configureren {#sms-configuration-twilio}

Als u Twilio met Journey Optimizer wilt configureren, moet u een nieuwe API-referenties maken die voor Twilio worden gebruikt:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_6.png)

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: toegang tot de **Accountgegevens** van de pagina Twilio Console Dashboard om uw referenties te zoeken.

   * **[!UICONTROL Message SID]**: voer de unieke id in die aan elk bericht is toegewezen dat door de API van Twilio is gemaakt. Meer informatie in [Twilio-documentatie](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

