---
solution: Journey Optimizer
product: journey optimizer
title: Het SMS-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van SMS met Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 57163faa177a4e8bc90496f7756d7749a4f7e325
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 2%

---

# Sms-kanaal configureren {#sms-configuration}

[!DNL Journey Optimizer] kunt u uw reizen maken en berichten naar het beoogde publiek sturen.

Voordat u SMS verzendt, configureert u uw exemplaar. U moet [de providerinstellingen integreren](#create-api) met Journey Optimizer en [een sms-oppervlak maken](#message-preset-sms) (d.w.z. voorinstelling SMS). Deze stappen moeten worden uitgevoerd door [Adobe Journey Optimizer-systeembeheerder](../start/path/administrator.md).

## Vereisten{#sms-prerequisites}

Adobe Journey Optimizer is momenteel geïntegreerd met externe providers zoals Sinch, Twilio en Infobip, die sms-diensten aanbieden die onafhankelijk zijn van Adobe Journey Optimizer.

Voordat u de SMS-configuratie start, moet u een account maken bij een van deze SMS-providers om de API Token en Service ID te ontvangen waarmee u de verbinding tussen Adobe Journey Optimizer en de betreffende SMS-provider tot stand kunt brengen.

Voor je gebruik van SMS-services gelden aanvullende voorwaarden van de betreffende SMS-provider. Aangezien Sinch en Twilio producten van derden zijn die via integratie beschikbaar zijn voor Adobe Journey Optimizer-gebruikers, zullen gebruikers van Sinch of Twilio voor problemen of vragen in verband met de SMS-diensten contact moeten opnemen met de toepasselijke SMS-provider voor hulp. Adobe heeft geen betrekking op producten van derden en is niet verantwoordelijk voor deze producten.

>[!CAUTION]
>
>Om tot subdomeinen van SMS toegang te hebben en uit te geven, moet u hebben **[!UICONTROL Manage SMS Subdomains]** toestemming voor de productiesandbox.

## Nieuwe API-referentie maken {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Uw SMS-leverancier configureren met Journey Optimizer"
>abstract="Selecteer uw leverancier en vul uw SMS API-referenties in."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Uw SMS-leverancier configureren met Journey Optimizer"
>abstract="Voordat u SMS verzendt, moet u de providerinstellingen integreren met Journey Optimizer. Zodra gedaan, zult u een oppervlakte van SMS moeten tot stand brengen. Deze stappen moeten worden uitgevoerd door een systeembeheerder van Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="Een SMS-kanaaloppervlak maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecteer de configuratie van de leverancier van SMS"
>abstract="Selecteer de API geloofsbrieven die voor uw verkoper van SMS worden gevormd."

Voer de volgende stappen uit om uw SMS-leverancier te configureren met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_6.png)

1. Vorm uw geloofsbrieven van SMS API:

   * Voor **[!DNL Sinch]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL Service ID]** en **[!UICONTROL API Token]**: als u toegang wilt tot de pagina met API&#39;s, vindt u uw referenties onder het tabblad SMS.  [Meer informatie](https://developers.sinch.com/docs/sms/getting-started/)

      * **[!UICONTROL Opt-In Message]**: Typ de aangepaste reactie die automatisch als uw **[!UICONTROL Opt-In Message]**.

      * **[!UICONTROL Help Message]**: Typ de aangepaste reactie die automatisch als uw **[!UICONTROL  Help Message]**.

   * Voor **[!DNL Twilio]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: ga naar het venster Accountinformatie van de pagina Dashboard van de Twilio-console om uw referenties te zoeken.

      * **[!UICONTROL Message SID]**: voer de unieke id in die aan elk bericht is toegewezen dat door de API van Twilio is gemaakt. [Meer informatie](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-)

   * Voor **[!DNL Infobip]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL API base URL]** en **[!UICONTROL API token]**: ga naar de startpagina van uw webinterface of de API-sleutelbeheerpagina om uw referenties te zoeken. [Meer informatie](https://www.infobip.com/docs/api)

   ![](assets/sms_7.png)

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak (d.w.z. een voorinstelling voor berichten) voor SMS-berichten maken.

## Een SMS-oppervlak maken {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="De categorie SMS definiëren"
>abstract="Selecteer het type SMS-berichten op dit oppervlak: Marketing voor promotionele SMS-berichten waarvoor toestemming van de gebruiker vereist is, of Transactie voor niet-commerciële SMS-berichten, zoals het opnieuw instellen van wachtwoorden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Afmelden bij marketing van SMS-berichten"

Zodra uw kanaal van SMS is gevormd, moet u een kanaaloppervlakte tot stand brengen om SMS berichten van te kunnen verzenden **[!DNL Journey Optimizer]**.

Ga als volgt te werk om een kanaaloppervlak te maken:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]**. Klik op de knop **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Voer een naam en beschrijving (optioneel) voor het oppervlak in en selecteer vervolgens het SMS-kanaal.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

1. Definieer de **SMS-instellingen**.

   ![](assets/sms-surface-settings.png)

   Begin door te selecteren **[!UICONTROL SMS Type]** die samen met het oppervlak worden verzonden: **[!UICONTROL Transactional]** of **[!UICONTROL Marketing]**.

   * Kies **Marketing** voor promotionele SMS: voor deze berichten is toestemming van de gebruiker vereist.
   * Kies **Transactioneel** voor niet-commerciële berichten, zoals bevestiging van de bestelling, wachtwoordherstelmeldingen of leveringsgegevens.

   Wanneer u een SMS-bericht maakt, moet u een geldig kanaaloppervlak kiezen dat overeenkomt met de categorie die u voor uw bericht hebt geselecteerd.

   >[!CAUTION]
   >
   >**Transactioneel** SMS-berichten kunnen worden verzonden naar profielen die zich niet meer hebben geabonneerd op marketingberichten. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

1. Selecteer de **[!UICONTROL SMS configuration]** aan het oppervlak te koppelen.

   Voor meer over hoe te om uw milieu te vormen om de berichten van SMS te verzenden, verwijs naar [deze sectie](#create-api).

1. Voer de **[!UICONTROL Sender number]** &#x200B; u voor uw mededelingen wilt gebruiken.

1. Selecteer uw **[!UICONTROL SMS Execution Field]** om de **[!UICONTROL Profile attribute]** aan de telefoonaantallen van de profielen worden geassocieerd.

1. Als u de functie URL-verkorting wilt gebruiken in uw SMS-berichten, selecteert u een item in het menu **[!UICONTROL Subdomain]** lijst.

   >[!NOTE]
   >
   >Om subdomain te kunnen selecteren, zorg ervoor u eerder minstens één subdomain van SMS hebt gevormd. [Meer informatie](sms-subdomains.md)

1. Voer de **[!UICONTROL Opt-out number]** U wilt dit oppervlak gebruiken. Wanneer profielen weigeren van dit nummer, kunt u de profielen nog steeds berichten verzenden van andere nummers die u kunt gebruiken om SMS-berichten te verzenden met [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >In [!DNL Journey Optimizer], SMS-optie-optie wordt niet meer op kanaalniveau beheerd. Het is nu specifiek voor een getal.

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** ter bevestiging. U kunt het kanaaloppervlak ook opslaan als concept en de configuratie later hervatten.

   ![](assets/sms-submit-surface.png)

1. Nadat het kanaaloppervlak is gemaakt, wordt het in de lijst weergegeven met de **[!UICONTROL Processing]** status.

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [deze sectie](#monitor-channel-surfaces).

1. Als de controles zijn voltooid, krijgt het kanaaloppervlak de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   ![](assets/preset-active.png)

Je bent nu klaar om SMS-berichten te verzenden met Journey Optimizer.

**Verwante onderwerpen**

* [Een SMS-bericht maken](create-sms.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)

