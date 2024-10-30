---
solution: Journey Optimizer
product: journey optimizer
title: Uw aangepaste provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer via een aangepaste provider
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Een aangepaste provider configureren (Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>Aangepaste providers zijn momenteel alleen beschikbaar als bètaversie voor geselecteerde gebruikers. Neem contact op met uw Adobe om deel te nemen aan de Beta.
>
>In deze Beta worden binnenkomende berichten voor het beheer van de opt-in- of opt-out-toestemming en voor de rapportage van de levering niet ondersteund.

Ga als volgt te werk als u berichten in Journey Optimizer wilt verzenden via een aangepaste provider die niet via Adobe uit het vak beschikbaar is (bijv. Sinch, Infobip, Twilio):

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer het menu **[!UICONTROL API Credentials]** .

1. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_byo_1.png)

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Aangepast.

   * **[!UICONTROL Name]**: voer een naam in voor uw API-referentie.

   * **[!UICONTROL Provider AppId]** : voer de toepassings-id in die door uw SMS-provider is opgegeven.

   * **[!UICONTROL Provider Name]** : voer de naam van uw SMS-provider in.

   * **[!UICONTROL Provider URL]** : voer de URL van uw SMS-provider in.

   * **[!UICONTROL Auth Type&#x200B;]**: selecteer het machtigingstype. De gesteunde types van Toestemming zijn **Drager App** of **Basis**.

   * **[!UICONTROL API Token]**: voer de API-token in die door uw SMS-provider is opgegeven.

   * **[!UICONTROL Provider Payload]**: voeg uw providerlading toe, bijvoorbeeld `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}` .

     Zorg ervoor dat de payload `{{toNumber}}`, `{{fromNumber}}`, `{{message}}` bevat.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak voor SMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

Zodra gevormd, kunt u hefboomwerking alle uit-van-de-doos kanaalmogelijkheden zoals bericht creatie, verpersoonlijking, verbinding het volgen, en rapportering.

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
