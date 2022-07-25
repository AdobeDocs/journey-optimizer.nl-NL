---
title: SMS-configuratie
description: Leer hoe u uw omgeving configureert voor het verzenden van SMS-berichten met Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 2%

---

# Sms-kanaal configureren {#sms-configuration}

[!DNL Journey Optimizer] kunt u uw reizen maken en berichten naar het beoogde publiek sturen.

Voordat u SMS verzendt, configureert u uw exemplaar. U moet [providerinstellingen integreren](#create-api) met Journey Optimizer en [een sms-oppervlak maken](#message-preset-sms) (d.w.z. voorinstelling SMS). Deze stappen moeten worden uitgevoerd door een [Adobe Journey Optimizer-systeembeheerder](../start/path/administrator.md).

>[!AVAILABILITY]
>
>Het SMS-kanaal is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

## Nieuwe API-referentie maken {#create-api}

Voer de volgende stappen uit om uw SMS-leverancier te configureren met Journey Optimizer:

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** en klik vervolgens op **[!UICONTROL Create API credential]**.

   ![](assets/sms_4.png)

1. Selecteer uw **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]. Als u uw **[!UICONTROL Service ID]** en **[!UICONTROL API Token]** hebt u toegang tot SMS > API&#39;s via uw Sinch-account.
   * [!DNL Twilio]. Als u uw **[!UICONTROL Service ID]** en **[!UICONTROL API Token]**, opent u het venster Accountinformatie van de pagina Dashboard van de console.

1. Voer een **[!UICONTROL Name]** voor uw API-referentie.

1. Voer uw **[!UICONTROL Service ID]** en **[!UICONTROL API Token]**.

   ![](assets/sms_5.png)

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak (d.w.z. een voorinstelling voor berichten) voor SMS-berichten maken.

## Een kanaaloppervlak maken voor SMS-berichten {#message-preset-sms}

Zodra uw kanaal van SMS is gevormd, moet u een kanaaloppervlakte tot stand brengen om de berichten van SMS van te kunnen verzenden **[!DNL Journey Optimizer]**.

Ga als volgt te werk om een kanaaloppervlak te maken:

1. Toegang krijgen tot **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** en klik vervolgens op **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor het oppervlak in en selecteer vervolgens het SMS-kanaal.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

1. Configureer de **SMS** instellingen.

   ![](assets/preset-sms.png)

   * Selecteer **[!UICONTROL SMS Type]** die samen met het oppervlak worden verzonden: **[!UICONTROL Transactional]** of **[!UICONTROL Marketing]**.

   * Selecteer **[!UICONTROL SMS configuration]** aan het oppervlak te koppelen.

      Voor meer over hoe te om uw milieu te vormen om de berichten van SMS te verzenden, verwijs naar [deze sectie](#create-api).

   * Voer de **[!UICONTROL Sender number]** &#x200B; u voor uw mededelingen wilt gebruiken.

   * Selecteer uw **[!UICONTROL SMS Execution Field]** om de **[!UICONTROL Profile attribute]** aan de telefoonaantallen van de profielen worden geassocieerd.

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** ter bevestiging. U kunt het kanaaloppervlak ook opslaan als concept en de configuratie later hervatten.

   ![](assets/sms_preset_2.png)

1. Nadat het kanaaloppervlak is gemaakt, wordt het in de lijst weergegeven met de **[!UICONTROL Processing]** status.

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [deze sectie](#monitor-message-presets).

1. Als de controles zijn voltooid, krijgt het kanaaloppervlak de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   ![](assets/preset-active.png)

Je kunt nu SMS-berichten verzenden met Journey Optimizer.

**Verwante onderwerpen**

* [Een SMS-bericht maken](../messages/create-sms.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
