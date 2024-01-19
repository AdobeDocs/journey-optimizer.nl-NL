---
solution: Journey Optimizer
product: journey optimizer
title: Het SMS-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 1a3a67571ef839bf8e1942e4c9599aa52ea7e2dc
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 1%

---

# Sms-kanaal configureren {#sms-configuration}

Voordat u SMS of MMS verzendt, moet u de Adobe Journey Optimizer-omgeving configureren. U kunt dit als volgt uitvoeren:

* [De providerinstellingen integreren](#create-api) met Journey Optimizer
* [Een SMS-oppervlak maken](#message-preset-sms) (d.w.z. voorinstelling SMS), ook gebruikt voor MMS

Deze stappen moeten worden uitgevoerd door een Adobe Journey Optimizer [Systeembeheerder](../start/path/administrator.md).

## Vereisten{#sms-prerequisites}

Adobe Journey Optimizer is momenteel geïntegreerd met externe providers die services voor tekstberichten aanbieden die onafhankelijk zijn van Adobe Journey Optimizer. Ondersteunde providers voor tekstberichten zijn: **Sinch**, **Twilio** en **Infobip**. MMS wordt alleen ondersteund met **Sinch**.

Voordat u de SMS-kanaalconfiguratie start, moet u een account met een van deze providers maken om uw **API-token** en **Service-id**, die u moet configureren tussen Adobe Journey Optimizer en de toepasselijke provider.

Voor het gebruik van services voor tekstberichten gelden aanvullende voorwaarden van de betreffende provider. Als oplossingen van derden zijn Sinch, Twilio en Infobip via integratie beschikbaar voor Adobe Journey Optimizer-gebruikers. Adobe heeft geen betrekking op producten van derden en is niet verantwoordelijk voor deze producten. Neem contact op met uw provider voor problemen met of verzoeken om assistentie met betrekking tot SMS/MMS.

>[!CAUTION]
>
>Om tot subdomeinen van SMS toegang te hebben en uit te geven, moet u hebben **[!UICONTROL Manage SMS Subdomains]** toestemming voor de productiesandbox. Meer informatie over machtigingen in [deze pagina](../administration/high-low-permissions.md#administration-permissions).
>

## Nieuwe API-referenties maken {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Uw SMS-provider configureren met Journey Optimizer"
>abstract="Adobe Journey Optimizer verzendt tekstberichten via SMS-serviceproviders. Selecteer uw provider en vul uw API-referenties in."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Uw MMS-provider configureren met Journey Optimizer"
>abstract="Adobe Journey Optimizer verzendt media-inhoud via MMS-serviceproviders. Selecteer uw provider en vul uw API-referenties in."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Uw SMS/MMS-provider configureren met Journey Optimizer"
>abstract="Voordat u tekstberichten (SMS/MMS) kunt verzenden, moet u de providerinstellingen integreren met Journey Optimizer. Zodra gedaan, moet u een oppervlakte tot stand brengen SMS/MMS. Deze stappen moeten worden uitgevoerd door een Adobe Journey Optimizer System Administrator."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="Een SMS-kanaaloppervlak maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecteer de configuratie van de leverancier van SMS"
>abstract="Selecteer de API geloofsbrieven die voor uw verkoper van SMS worden gevormd."

Voer de volgende stappen uit om uw SMS/MMS-provider te configureren met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_6.png)

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven.

   ![](assets/sms_7.png)

   * Voor **[!DNL Sinch]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL Service ID]** en **[!UICONTROL API Token]**: als u toegang wilt tot de pagina met API&#39;s, vindt u uw referenties onder het tabblad SMS. Meer informatie in [Sectorale documentatie](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

      * **[!UICONTROL Opt-In Message]**: voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-In Message]**.

      * **[!UICONTROL Help Message]**: voer de aangepaste reactie in die automatisch als uw **Help-bericht**.

   * Voor **[!DNL Sinch MMS]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL Project ID]**, **[!UICONTROL App ID]** en **[!UICONTROL API Token]**: in het menu Conversation API vindt u uw referenties in het menu App. Meer informatie in [Sectorale documentatie](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * Voor **[!DNL Twilio]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]**: ga naar het venster Accountinformatie van de pagina Dashboard van de Twilio-console om uw referenties te zoeken.

      * **[!UICONTROL Message SID]**: voer de unieke id in die aan elk bericht is toegewezen dat door de API van Twilio is gemaakt. Meer informatie in [Twilio-documentatie](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * Voor **[!DNL Infobip]**:

      * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

      * **[!UICONTROL API base URL]** en **[!UICONTROL API token]**: ga naar de startpagina van uw webinterface of de API-sleutelbeheerpagina om uw referenties te zoeken. Meer informatie in [Infobip-documentatie](https://www.infobip.com/docs/api){target="_blank"}.


1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak (d.w.z. een voorinstelling voor berichten) voor SMS-berichten maken.

## Een SMS-oppervlak maken {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="De berichtcategorie definiëren"
>abstract="Selecteer het type tekstberichten die dit oppervlak gebruiken: Marketing voor promotieberichten waarvoor toestemming van de gebruiker vereist is, of Transactie voor niet-commerciële berichten, zoals het opnieuw instellen van wachtwoorden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Afmelden bij marketingberichten"

Zodra uw SMS/MMS kanaal is gevormd, moet u een kanaaloppervlakte tot stand brengen om SMS berichten van te kunnen verzenden **[!DNL Journey Optimizer]**.

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

   * Kies **Marketing** voor promotietekstberichten : voor deze berichten is toestemming van de gebruiker vereist .
   * Kies **Transactioneel** voor niet-commerciële berichten, zoals bevestiging van de bestelling, wachtwoordherstelmeldingen of leveringsgegevens.

   Wanneer u een SMS-/MMS-bericht maakt, moet u een geldig kanaaloppervlak kiezen dat overeenkomt met de categorie die u voor uw bericht hebt geselecteerd.

   >[!CAUTION]
   >
   >**Transactioneel** berichten kunnen worden verzonden naar profielen die zich niet meer hebben geabonneerd op marketingberichten. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

1. Selecteer de **[!UICONTROL SMS configuration]** aan het oppervlak te koppelen.

   Voor meer over hoe te om uw milieu te vormen om de berichten van SMS te verzenden, verwijs naar [deze sectie](#create-api).

1. Voer de **[!UICONTROL Sender number]** &#x200B; u voor uw mededelingen wilt gebruiken.

1. Selecteer uw **[!UICONTROL SMS Execution Field]** om de **[!UICONTROL Profile attribute]** aan de telefoonaantallen van de profielen worden geassocieerd.

1. Als u de functie URL-verkorting wilt gebruiken in uw SMS-berichten, selecteert u een item in het menu **[!UICONTROL Subdomain]** lijst.

   >[!NOTE]
   >
   >Om een subdomein te kunnen selecteren, zorg ervoor u eerder minstens één subdomain SMS/MMS hebt gevormd. [Meer informatie](sms-subdomains.md)

1. Voer de **[!UICONTROL Opt-out number]** U wilt dit oppervlak gebruiken. Wanneer profielen weigeren van dit nummer, kunt u de profielen nog steeds berichten verzenden vanuit andere nummers die u kunt gebruiken om tekstberichten te verzenden met [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >In [!DNL Journey Optimizer]De optie om te weigeren voor tekstberichten wordt niet meer op kanaalniveau beheerd. Het is nu specifiek voor een getal.

1. Zodra alle parameters zijn gevormd, klik **[!UICONTROL Submit]** ter bevestiging. U kunt het kanaaloppervlak ook opslaan als concept en de configuratie later hervatten.

   ![](assets/sms-submit-surface.png)

1. Nadat het kanaaloppervlak is gemaakt, wordt het in de lijst weergegeven met de **[!UICONTROL Processing]** status.

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [deze sectie](#monitor-channel-surfaces).

1. Als de controles zijn voltooid, krijgt het kanaaloppervlak de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   ![](assets/preset-active.png)

U kunt nu tekstberichten verzenden met Journey Optimizer.

**Verwante onderwerpen**

* [Een tekstbericht maken (SMS/MMS)](create-sms.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)

