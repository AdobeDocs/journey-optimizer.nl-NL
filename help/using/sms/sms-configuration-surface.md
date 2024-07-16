---
solution: Journey Optimizer
product: journey optimizer
title: Vorm de oppervlakte van SMS
description: Leer hoe u uw SMS/MMS-oppervlak configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 080928d14a9d6ec116286386748b77a6a25e76f8
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Een SMS/MMS-oppervlak maken {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="De berichtcategorie definiëren"
>abstract="Selecteer het type tekstberichten die dit oppervlak gebruiken: Marketing voor promotieberichten waarvoor toestemming van de gebruiker vereist is, of Transactie voor niet-commerciële berichten, zoals het opnieuw instellen van wachtwoorden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Afmelden bij marketingberichten"

Zodra uw SMS/MMS-kanaal is geconfigureerd, moet u een kanaaloppervlak maken om SMS- en MMS-berichten van **[!DNL Journey Optimizer]** te kunnen verzenden.

Ga als volgt te werk om een kanaaloppervlak te maken:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** . Klik op de knop **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor het oppervlak in en selecteer vervolgens het SMS-kanaal.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Bepaal de **montages van SMS**.

   ![](assets/sms-surface-settings.png)

   Selecteer eerst de **[!UICONTROL SMS Type]** die met het oppervlak wordt verzonden: **[!UICONTROL Transactional]** of **[!UICONTROL Marketing]** .

   * Kies **Marketing** voor promotietekstberichten: deze berichten vereisen gebruikerstoestemming.
   * Kies **Transactie** voor niet-commerciële berichten zoals ordesbevestiging, wachtwoord terugstellende berichten, of leveringsinformatie bijvoorbeeld.

   Wanneer u een SMS/MMS maakt, moet u een geldig kanaaloppervlak kiezen dat overeenkomt met de categorie die u voor uw bericht hebt geselecteerd.

   >[!CAUTION]
   >
   >**Transactionele** berichten kunnen naar profielen worden verzonden die van marketing mededelingen afmelden. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

1. Selecteer de **[!UICONTROL SMS configuration]** die u aan het oppervlak wilt koppelen.

   Voor meer op hoe te om uw milieu te vormen om de berichten van SMS te verzenden, verwijs naar [ deze sectie ](#create-api).

1. Ga **[!UICONTROL Sender number]** in &#x200B; u voor uw mededelingen wilt gebruiken.

1. Selecteer de **[!UICONTROL SMS Execution Field]** om de **[!UICONTROL Profile attribute]** te selecteren die aan de telefoonnummers van de profielen is gekoppeld.

1. Als u de functie voor het verkorten van URL&#39;s wilt gebruiken in uw SMS-berichten, selecteert u een item in de lijst **[!UICONTROL Subdomain]** .

   >[!NOTE]
   >
   >Om een subdomein te kunnen selecteren, zorg ervoor u eerder minstens één subdomain SMS/MMS hebt gevormd. [ leer hoe ](sms-subdomains.md)

1. Nadat alle parameters zijn geconfigureerd, klikt u op **[!UICONTROL Submit]** om te bevestigen. U kunt het kanaaloppervlak ook opslaan als concept en de configuratie later hervatten.

   ![](assets/sms-submit-surface.png)

1. Nadat het kanaaloppervlak is gemaakt, wordt het in de lijst weergegeven met de status **[!UICONTROL Processing]** .

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [ deze sectie ](#monitor-channel-surfaces).

1. Wanneer de controles succesvol zijn, krijgt het kanaaloppervlak de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   ![](assets/preset-active.png)

U kunt nu tekstberichten verzenden met Journey Optimizer.
