---
solution: Journey Optimizer
product: journey optimizer
title: Het WhatsApp-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van WhatsApp-berichten met Journey Optimizer
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 1%

---

# Aan de slag met WhatsApp-configuratie {#whatsapp-config}

Voordat u het WhatsApp-bericht verzendt, moet u uw Adobe Journey Optimizer-omgeving configureren en koppelen aan uw WhatsApp-account. Dit doet u als volgt:

1. [Uw WhatsApp API-referenties maken](#WhatsApp-credentials)
1. [Maak uw whatsApp-webhooks](#WhatsApp-webhook)
1. [De whatsApp-configuratie maken](#WhatsApp-configuration)

Deze stappen moeten door een Beheerder van het Systeem van Adobe Journey Optimizer [&#x200B; worden uitgevoerd &#x200B;](../start/path/administrator.md).

## WhatsApp API-referenties maken {#whatsapp-credentials}

1. Blader in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw API-referenties, zoals hieronder wordt beschreven:

   * **API Token**: Ga uw API teken in. Leer meer in [&#x200B; Documentatie van Meta &#x200B;](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
   * **identiteitskaart Bedrijfs van de Rekening**: Ga het unieke aantal met betrekking tot uw bedrijfsportefeuille in. Leer meer in [&#x200B; Documentatie van Meta &#x200B;](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Klik op **[!UICONTROL Continue]**.

1. Kies de **WhatsApp BedrijfsRekening** u met uw whatsApp API geloofsbrieven wilt verbinden.

   ![](assets/whatsapp-api-2.png)

1. Selecteer de **naam van de Afzender** wordt gebruikt om uw WhatsApp- berichten te verzenden die.

1. De instellingen voor het telefoonnummer worden automatisch ingevuld:

   * **Classificatie van de Kwaliteit**: wijst op klant terugkoppelt op berichten die in de afgelopen 24 uren worden verzonden.
      * Groen: Hoge kwaliteit
      * Geel: Medium-kwaliteit
      * Rood: lage kwaliteit

     Leer meer over [&#x200B; de classificatie van de Kwaliteit &#x200B;](https://www.facebook.com/business/help/766346674749731#)

   * **Output**: wijst op het tarief waaraan uw telefoonaantal berichten kan verzenden.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu uw Webhaak voor WhatsApp-berichten maken. [Meer informatie](#whatsapp-webhook)

## Webhaak maken {#WhatsApp-webhook}

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword_category"
>title="Binnenkomende trefwoordcategorie"
>abstract="<b> Opt-binnen </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker intekent. <br/><b> Opt-uit </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker afmeldt. <br/><b> Hulp </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker om hulp of steun verzoekt. <br/><b> Gebrek </b>: verzendt uw fallback auto-reactie wanneer geen sleutelwoorden aanpassen."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword"
>title="Trefwoorden invoeren"
>abstract="U kunt trefwoorden definiëren om specifieke automatische reacties te activeren op basis van de gebruikerstekst. Trefwoorden zijn niet hoofdlettergevoelig, dus stop en STOP worden bijvoorbeeld op dezelfde manier behandeld."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_webhook_url"
>title="URL voor terugbellen"
>abstract="De validatieaanvraag en webhaakmeldingen voor dit object worden naar de opgegeven URL verzonden."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_verify_token"
>title="Token verifiëren"
>abstract="Het token dat Meta terugweergeeft om de callback-URL tijdens het verificatieproces te bevestigen en te verifiëren."

>[!NOTE]
>
>Zonder opgegeven opt-in- of opt-out-trefwoorden zijn standaardtoestemmingsberichten niet ingeschakeld.

Nadat de whatsApp API-referenties zijn gemaakt, kunt u nu Webhooks configureren om binnenkomende reacties vast te leggen voor het beheer van de toestemming om zich aan te melden en te weigeren, en om leveringsrapporten te ontvangen, zoals leesontvangstbewijzen indien beschikbaar.

1. Navigeer in de linkertrack naar **[!UICONTROL Administration]** `>` **[!UICONTROL Channels]** , selecteer het menu **[!UICONTROL WhatsApp Webhooks]** onder **[!UICONTROL WhatsApp settings]** en klik op de knop **[!UICONTROL Create Webhook]** .

   ![](assets/webhook-1.png)

1. Voer een **[!UICONTROL Name]** in voor uw webhaak.

1. Van **[!UICONTROL Select configuration]** drop-down, selecteer [&#x200B; API Geloofsbrieven &#x200B;](#whatsapp-credentials) u eerder creeerde.

   ![](assets/webhook-2.png)

1. Kies uw **[!UICONTROL Inbound keyword category]** , zoals:

   * **[!UICONTROL Opt-in Keywords]**
   * **[!UICONTROL Opt-out Keywords]**
   * **[!UICONTROL Help Keywords]**

1. Ga uw **[!UICONTROL Keywords]** in en klik ![&#x200B; toevoegen &#x200B;](assets/do-not-localize/Smock_AddCircle_18_N.svg).

   ![](assets/webhook-3.png)

1. Voer in het veld **[!UICONTROL Reply Message]** het bericht in dat wordt verzonden wanneer een geconfigureerd trefwoord wordt ontvangen of selecteer een vooraf gedefinieerde optie in het vervolgkeuzemenu.

   ![](assets/webhook-4.png)

<!--
1. Click **[!UICONTROL View payload editor]** to validate and customize your request payloads. 
    
    You can dynamically personalize your payload using profile attributes, and ensure accurate data is sent for processing and response generation with the help of built-in helper functions.
-->
1. Klik ![&#x200B; toevoegen &#x200B;](assets/do-not-localize/Smock_AddCircle_18_N.svg) om extra **[!UICONTROL Inbound keyword]** toe te voegen.

1. Klik **[!UICONTROL Submit]** wanneer u de configuratie van uw WhatsApp Webhaak beëindigde.

1. In het **[!UICONTROL Webhooks]** menu, klik het ![&#x200B; bakpictogram &#x200B;](assets/do-not-localize/Smock_Delete_18_N.svg) om uw WebHaak te schrappen WhatsApp.

   ![](assets/webhook-5.png)

1. Als u de bestaande configuratie wilt wijzigen en toegang wilt krijgen tot uw **[!UICONTROL Webhook URL]** of **[!UICONTROL Webhook Verify toker]** , zoekt u de gewenste Webhaak en klikt u op de optie **[!UICONTROL Edit]** om de gewenste wijzigingen aan te brengen.

1. Kopieer de **[!UICONTROL Webhook Verify toker]** die u hier hebt gegenereerd en plak deze in de Meta-interface als onderdeel van uw WebHaak-instelling.

   Voor gedetailleerde instructies op hoe en waar om dit verificatietoken toe te voegen, verwijs naar [&#x200B; documentatie van Meta &#x200B;](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#configure-webhooks-product).

1. Open en kopieer uw nieuwe **[!UICONTROL Webhook URL]** vanuit uw eerder verzonden **[!UICONTROL WhatsApp Webhook]** .

   ![](assets/webhook-6.png)

Nu uw Webhaak wordt gevormd, kunt u uw configuratie tot stand brengen WhatsApp.

## WhatsApp-configuratie maken {#whatsapp-configuration}

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** . Klik op de knop **[!UICONTROL Create channel configuration]**.

   ![](assets/whatsapp-config-1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in en selecteer vervolgens het WhatsApp-kanaal.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Selecteer **[!DNL WhatsApp]** als kanaal.

   ![](assets/whatsapp-config-2.png)

1. Selecteer **[!UICONTROL Marketing action(s)]** om toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. Meer informatie

1. Selecteer het eerder gemaakte bestand **[!UICONTROL WhatsApp API configuration]** .

   ![](assets/whatsapp-config-3.png)

1. Ga **[!UICONTROL Sender name]** in &#x200B; u voor uw mededelingen wilt gebruiken.

1. Nadat alle parameters zijn geconfigureerd, klikt u op **[!UICONTROL Submit]** om te bevestigen. U kunt de kanaalconfiguratie als ontwerp ook bewaren en zijn configuratie later hervatten.

1. Nadat de kanaalconfiguratie is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Processing]** .

   >[!NOTE]
   >
   >Als de controles niet succesvol zijn, leer meer over de mogelijke mislukkingsredenen in [&#x200B; deze sectie &#x200B;](../configuration/channel-surfaces.md).

1. Wanneer de controles succesvol zijn, krijgt de kanaalconfiguratie de **[!UICONTROL Active]** status. Het is klaar om te worden gebruikt om berichten te leveren.

Zodra gevormd, kunt u hefboomwerking alle uit-van-de-doos kanaalmogelijkheden zoals bericht creatie, verpersoonlijking, verbinding het volgen, en rapportering.

U kunt nu WhatsApp-berichten verzenden met Journey Optimizer.


## Hoe kan ik-video {#video}

In de onderstaande video ziet u hoe u het WhatsApp-kanaal instelt in Adobe Journey Optimizer.

+++ Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3470274/?captions=dut&learn=on)

+++
