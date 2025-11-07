---
solution: Journey Optimizer
product: journey optimizer
title: De configuratie van SMS configureren
description: Leer hoe u uw SMS/MMS-configuratie configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: fc12ee65fc773c70b88504a951e5f5c5b2b3b0e6
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 1%

---

# Een SMS/MMS/RCS-configuratie maken {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="De berichtcategorie definiëren"
>abstract="Selecteer het type tekstberichten die deze configuratie gebruiken: Marketing voor promotieberichten, waarvoor toestemming van de gebruiker vereist is, of Transactie voor niet-commerciële berichten, zoals het terugstellen van wachtwoorden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Afmelden bij marketingberichten"

Nadat u het SMS/MMS/RCS-kanaal hebt geconfigureerd, moet u een kanaalconfiguratie maken om SMS-, RCS- en MMS-berichten van **[!DNL Journey Optimizer]** te kunnen verzenden.

Ga als volgt te werk om een kanaalconfiguratie te maken:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** . Klik op de knop **[!UICONTROL Create channel configuration]**.

   ![](assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in en selecteer vervolgens het SMS-kanaal.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Bepaal de **montages van SMS**.

   ![](assets/sms-surface-settings.png){width=80%}

   Selecteer eerst de **[!UICONTROL SMS Type]** die met de configuratie wordt verzonden: **[!UICONTROL Transactional]** of **[!UICONTROL Marketing]** .

   * Kies **Marketing** voor promotietekstberichten: deze berichten vereisen gebruikerstoestemming.
   * Kies **Transactie** voor niet-commerciële berichten zoals ordesbevestiging, wachtwoord terugstellende berichten, of leveringsinformatie bijvoorbeeld.

   Wanneer u een SMS/MMS maakt, moet u een geldige kanaalconfiguratie kiezen die overeenkomt met de categorie die u voor uw bericht hebt geselecteerd.

   >[!CAUTION]
   >
   >**Transactionele** berichten kunnen naar profielen worden verzonden die van marketing mededelingen afmelden. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

1. Selecteer de **[!UICONTROL SMS configuration]** die u aan de configuratie wilt koppelen.

   Voor meer op hoe te om uw milieu te vormen om de berichten van SMS te verzenden, verwijs naar [&#x200B; deze sectie &#x200B;](#create-api).

1. Ga **[!UICONTROL Sender number]** in &#x200B; u voor uw mededelingen wilt gebruiken.

1. Als u de functie voor het verkorten van URL&#39;s wilt gebruiken in uw SMS-berichten, selecteert u een item in de lijst **[!UICONTROL Subdomain]** .

   >[!NOTE]
   >
   >Om een subdomein te kunnen selecteren, zorg ervoor u eerder minstens één subdomain SMS/MMS hebt gevormd. [&#x200B; leer hoe &#x200B;](sms-subdomains.md)

1. In de sectie **[!UICONTROL Execution dimension]** gebruikt u **[!UICONTROL SMS Execution Field]** om onder de profielkenmerken het telefoonnummer te selecteren dat u met prioriteit wilt gebruiken als er meerdere nummers beschikbaar zijn in de database. [Meer informatie](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >Door gebrek, [!DNL Journey Optimizer] gebruikt het telefoonaantal dat in de [&#x200B; wordt gespecificeerd algemene montages &#x200B;](../configuration/primary-email-addresses.md) op het zandbakniveau. Wanneer u dit veld bijwerkt, wordt de standaardwaarde voor de ritten en campagnes met deze configuratie genegeerd.

1. Nadat alle parameters zijn geconfigureerd, klikt u op **[!UICONTROL Submit]** om te bevestigen. U kunt de kanaalconfiguratie als ontwerp ook bewaren en zijn configuratie later hervatten.

   ![](assets/sms-submit-surface.png)

1. Nadat de kanaalconfiguratie is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]** .

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [&#x200B; deze sectie &#x200B;](../configuration/channel-surfaces.md).

1. Wanneer de controles succesvol zijn, krijgt de kanaalconfiguratie de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   ![](assets/preset-active.png)

U kunt nu tekstberichten verzenden met Journey Optimizer.
