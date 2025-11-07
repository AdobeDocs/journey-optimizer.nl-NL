---
solution: Journey Optimizer
product: journey optimizer
title: Het LINE-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van LINE-berichten met Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
source-git-commit: bc734ed1249b1ec186eb5f479d605bafee8a1d06
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Regelkanaal configureren in Journey Optimizer {#line-configuration}

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/line-config-1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in en selecteer vervolgens het kanaal dat u wilt configureren.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer **LIJN** kanaal.

   ![](assets/line-config-2.png)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Selecteer het type bericht voor de configuratie:

   * **Marketing**: Voor promotionele berichten, zoals wekelijkse promoties voor een detailhandel. Deze berichten vereisen gebruikerstoestemming en zouden het beleid van de LIJN betreffende gebruiker moeten naleven opt-ins.
   * **Transactional**: Voor niet-commerciële berichten, zoals orderbevestigingen, wachtwoord terugstellende berichten, of leveringsupdates. Deze berichten kunnen zelfs worden verzonden naar gebruikers die zich niet meer hebben geabonneerd op marketingberichten, maar zijn strikt beperkt tot specifieke transactiecontext.

1. Selecteer de **[!UICONTROL Channel settings]** .

   Vraag uw Adobe-medewerker om uw **[!UICONTROL Channel settings]** in te stellen.

   ![](assets/line-config-2.png)

1. Selecteer de **[!UICONTROL LINE user ID]** die u wilt toewijzen. Dit is het herkenningsteken wordt gebruikt om berichten aan individuele gebruikers binnen uw kanaal van de LIJN te verbinden dat.

1. Typ uw **[!UICONTROL Sender Name]** , zoals de naam van uw merk.

1. Verzend uw wijzigingen.

U kunt nu uw configuratie selecteren wanneer u uw LIJNbericht creeert.

## De API voor lijnkanaalinstellingen configureren {#line-api}

Deze API plaatst omhoog kanaalmontages die de noodzakelijke vergunning en configuratiedetails voor het verbinden met de API van het Overseinen van de LIJN opslaan. Met deze instellingen kan Adobe Journey Optimizer berichten via LINE verifiëren en verzenden met behulp van de opgegeven referenties.

**Eindpunt**

```
POST https://platform.adobe.io/journey/imp/config/channel-settings
```

| Naam koptekst | Beschrijving |
|-|-|
| Toestemming | Gebruikerstoken van uw technische account |
| x-api-key | Client-id van Adobe Developer Console |
| x-gw-ims-org-id | Uw IMS-organisatie-id |
| x-sandbox-name | Naam van sandbox, bijvoorbeeld prod |
| Inhoudstype | Moet application/json zijn |


**Lichaam van het Verzoek**

```json
{
    "name": "your_defined_name",
    "channelRegistryId": "line",
    "channel": "line",
    "channelSettings": {
        "channelId": "your_line_channel_id",
        "channelSecret": "your_line_channel_secret"
    }
}
```

**Reactie van de Montages van het Kanaal**

```json
{
"id": "3603ed66-ae86-42b8-8a90-d4b4e54e7c3b",
"name": "your_defined_name",
"channelRegistryId": "line",
"channel": "line",
"channelSettings": {
    "channelId": "your_line_channel_id",
    "channelSecret": "your_line_channel_secret"
    },
    "channelPublicationId": "v1_line",
    "createdAt": "2025-07-30T12:00:00.000Z",
    "modifiedAt": "2025-07-30T12:00:00.000Z",
    "isFromLatestVersion": true,
    "_etag": "\"eab98d24-18af-48ae-90f9-e59d4f8cfb2b\""
}
```
