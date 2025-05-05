---
solution: Journey Optimizer
product: journey optimizer
title: Twilio-provider configureren
description: Leer hoe u uw omgeving configureert om tekstberichten te verzenden met Journey Optimizer met Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# Twilio-provider configureren {#sms-configuration-twilio}

Als u Twilio wilt configureren met Journey Optimizer, moet u een nieuwe API-referenties maken die worden gebruikt voor Twilio:

1. Blader in het linkerdeelvenster naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw SMS API-referenties, zoals hieronder beschreven:

   * **[!UICONTROL SMS vendor]**: Twilio.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: heb toegang tot de **Info van de Rekening** ruit van uw pagina van het Dashboard van de Console van Twilio om uw geloofsbrieven te vinden.

   * **[!UICONTROL Message SID]**: voer de unieke id in die is toegewezen aan elk bericht dat is gemaakt door de API van Twilio. Leer meer in [ Twilio Documentatie ](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"} .

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende getal toe. Zo kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer.

1. Klik op **[!UICONTROL Submit]** wanneer u klaar bent met de configuratie van uw API-referenties.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u uw API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor sms- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
