---
solution: Journey Optimizer
product: journey optimizer
title: Het LINE-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van LINE-berichten met Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6820f57ca4f8734eb746d1bdb2eae8829f37d520
workflow-type: tm+mt
source-wordcount: '248'
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
