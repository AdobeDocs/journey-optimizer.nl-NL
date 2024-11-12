---
solution: Journey Optimizer
product: journey optimizer
title: Sinch-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: a196a27fd22a03915838ab4a9bb6139f85242f6b
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 1%

---

# Sinch-provider configureren {#sms-configuration-sinch}

Wanneer u de Sinch-provider gebruikt met Journey Optimizer, kunt u twee verschillende opties vinden:

* **Configuratie van SMS**: Opstelling uw geloofsbrieven van Sinch API om de berichten van SMS foutloos te verzenden.

* **Configuratie MMS**: Voor het overseinen van verschillende media (MMS), vorm uw Inch MMS API geloofsbrieven. Merk op dat het volgen en het antwoorden aan binnenkomende berichten, door de configuratie van SMS worden behandeld. De opstelling MMS is slechts voor uitgaande levering van het MMS bericht.

## Inloggegevens van de API{#create-api}

Voer de volgende stappen uit om uw Sinch-provider te configureren voor het verzenden van SMS-berichten en MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Sinch.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Service ID]** en **[!UICONTROL API Token]** : als u toegang wilt tot de pagina met API&#39;s, vindt u uw referenties onder het tabblad SMS. Leer meer in [ de Documentatie van de Sinch ](https://developers.sinch.com/docs/sms/getting-started/) {target="_blank"}.

   * **[!UICONTROL Opt-In Keywords]** : voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-In Message]** activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-In Message]** : voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-In Message]** wordt verzonden.

   * **[!UICONTROL Opt-Out Keywords]** : voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-Out Message]** activeren. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-Out Message]** : voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-Out Message]** wordt verzonden.

   * **[!UICONTROL Help Keywords]**: ga het gebrek of douanesleutelwoorden in die uw **Bericht van de Hulp** automatisch zullen teweegbrengen. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Help Message]**: ga de douanereactie in die automatisch als uw **Bericht van de Hulp** wordt verzonden.

   * **[!UICONTROL Double Opt-In Keywords]** : voer de trefwoorden in die het dubbele aanmeldingsproces activeren. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. [ Leer meer op SMS Dubbelopt-binnen ](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Double Opt-In Message]**: voer de aangepaste reactie in die automatisch wordt verzonden als reactie op de dubbele aanmeldingsbevestiging.

   * **[!UICONTROL Inbound Number]**: voeg uw unieke binnenkomende aantal of korte code toe. Hierdoor kunt u dezelfde API-referenties gebruiken in verschillende sandboxen, elk met een eigen binnenkomend nummer of korte code.

   * **[!UICONTROL Custom Inbound Keywords]**: definieer unieke trefwoorden voor specifieke acties, zoals KORTING, AANBIEDINGEN, ENROLL. Deze trefwoorden worden vastgelegd en opgeslagen als kenmerken in het profiel, zodat u een kwalificatie voor een streaming segment op de reis kunt activeren en een aangepaste reactie of actie kunt leveren.

   * **[!UICONTROL Default Inbound Reply Message]**: voer het standaardantwoord in dat wordt verzonden wanneer een eindgebruiker een binnenkomend SMS-bericht verzendt dat niet overeenkomt met een van de gedefinieerde trefwoorden.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor SMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

## Referenties voor MMS API instellen {#sinch-mms}

>[!IMPORTANT]
>
> Samen met de opstelling MMS, moet u ook de geloofsbrieven van Sinch API tot stand brengen specifiek voor het volgen van binnenkomende berichten en het beheren van toestemmingsverzoeken.

Voer de volgende stappen uit om Sinch MMS te configureren voor het verzenden van MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** `>` **[!UICONTROL SMS Settings]** en selecteer het menu **[!UICONTROL API Credentials]** . Klik op de knop **[!UICONTROL Create new API credentials]**.

1. Configureer uw MMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL SMS vendor]**: Sinch MMS.

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Project ID]** , **[!UICONTROL App ID]** en **[!UICONTROL API Token]** : volg de onderstaande stappen om uw MMS API-referenties te verzamelen.

      * Voor **[!UICONTROL Project ID]** en **[!UICONTROL App ID]**: Heb toegang tot de [ API van de Gesprek - overzicht ](https://dashboard.sinch.com/convapi/overview) pagina van uw project van Sinch op uw Staaldashboard.
      * Voor **[!UICONTROL API Token]**: Verkrijg de [ sleutels van de Toegang ](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) voor uw Project van de Sinch en produceer a **Base64 API Symbolisch** uit uw Duidelijke Sleutels van de Toegang van het Project ****.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

1. Klik in het menu **[!UICONTROL API Credentials]** op het binpictogram om uw API-referenties te verwijderen.

1. Als u bestaande referenties wilt wijzigen, zoekt u de gewenste API-referenties en klikt u op de optie **[!UICONTROL Edit]** om de benodigde wijzigingen aan te brengen.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaalconfiguratie voor MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
