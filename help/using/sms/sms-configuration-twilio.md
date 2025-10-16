---
solution: Journey Optimizer
product: journey optimizer
title: Twilio-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 1%

---

# Twilio-provider configureren {#sms-configuration-twilio}

## API-referentie configureren voor SMS/MMS

Als u Twilio wilt configureren met Journey Optimizer, moet u nieuwe API-referenties maken voor Twilio:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Twilio.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: heb toegang tot **Info van de Rekening** ruit van uw pagina van het dashboard van de Console van Twilio om uw geloofsbrieven te vinden.

   * **[!UICONTROL Message SID]**: voer de unieke id in die is toegewezen aan elk bericht dat door de API van Twilio is gemaakt. Leer meer in [ Documentatie van Twilio ](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende aantal toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

1. Klik op **[!UICONTROL Verify SMS connection]** vanuit uw bestaande API-referenties om uw SMS API-referenties te testen en te verifiëren door een voorbeeldbericht naar een opgegeven apparaat te verzenden.

1. Vul de **gebieden van het Aantal** en **Bericht** in en klik **[!UICONTROL Verify connection]**.

   >[!IMPORTANT]
   >
   >Het bericht moet zodanig zijn gestructureerd dat het wordt uitgelijnd met de indeling voor de lading van de provider.

   ![](assets/verify-connection.png)

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS- en MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

## API-referentie configureren voor RCS

Het overseinen RCS wordt gesteund in Adobe Journey Optimizer door Twilio gebruikend de [ eigenschap van de Leverancier van SMS van de Douane ](sms-configuration-custom.md). Dit maakt het mogelijk rijke, interactieve berichten via geverifieerde bedrijfsprofielen te verzenden, met elementen zoals carrousels, knoppen en multimedia-inhoud.

➡️ [ Onderzoek hoe Twilio RCS in de documentatie van Twilio steunt ](https://www.twilio.com/docs/rcs)

Om RCS overseinen met Twilio toe te laten, moeten de nieuwe geloofsbrieven van API via een Leverancier van douaneSMS worden gevormd. De bestaande geloofsbrieven van TwilioSMS zijn niet compatibel, aangezien RCS een verschillend ladingsformaat vereist.

RCS met Twilio configureren:

1. **Register voor het Overseinen RCS in Twilio**

   Voer eerst het RCS-registratieproces in het Twilio-platform uit. Dit omvat het instellen van uw bedrijfsprofiel en het inschakelen van RCS-mogelijkheden voor uw account.

1. **creeer een Webhaak van SMS**

   [ vorm een Webhaak van SMS ](sms-configuration-custom.md#webhook) die inkomende RCS berichtreacties of leveringsupdates kan ontvangen. Deze webhaak moet correct aan uw opstelling van Twilio voor bidirectionele mededeling worden verbonden.

1. **creeer API Verantwoordelijkheid gebruikend Douane als verkoper van SMS**

   In Journey Optimizer, [ bepaal nieuwe API geloofsbrieven ](sms-configuration-custom.md#api-credential) specifiek voor RCS gebruikend &quot;Douane&quot;als verkoper van SMS. Gebruik de aangewezen methode van de RCS eindpuntauthentificatie, basis URL, en kopballen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor uw RCS-berichten maken. [Meer informatie](sms-configuration-surface.md)







