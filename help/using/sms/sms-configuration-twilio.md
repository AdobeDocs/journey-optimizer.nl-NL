---
solution: Journey Optimizer
product: journey optimizer
title: Twilio-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# Twilio-provider configureren {#sms-configuration-twilio}

Als u Twilio met Journey Optimizer wilt configureren, moet u een nieuwe API-referenties maken die voor Twilio worden gebruikt:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Twilio.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: heb toegang tot **Info van de Rekening** ruit van uw pagina van het dashboard van de Console van Twilio om uw geloofsbrieven te vinden.

   * **[!UICONTROL Message SID]**: voer de unieke id in die is toegewezen aan elk bericht dat door de API van Twilio is gemaakt. Leer meer in [ Documentatie van Twilio ](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-) {target="_blank"}.

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende aantal toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
