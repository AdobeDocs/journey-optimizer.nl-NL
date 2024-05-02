---
solution: Journey Optimizer
product: journey optimizer
title: Sinch-provider configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer met Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%

---

# Sinch-provider configureren {#sms-configuration-sinch}

Wanneer u de Sinch-provider gebruikt met Journey Optimizer, kunt u twee verschillende opties vinden:

* **SMS-configuratie**: Stel uw Sinch API-referenties in om SMS-berichten naadloos te verzenden.

* **MMS-configuratie**: Voor multimediaberichten (MMS) configureert u uw aanmeldgegevens voor Sinch MMS API. Merk op dat het volgen en het antwoorden aan binnenkomende berichten, door de configuratie van SMS worden behandeld. De opstelling MMS is slechts voor uitgaande levering van het MMS bericht.

## Inloggegevens van de API{#create-api}

Voer de volgende stappen uit om uw Sinch-provider te configureren voor het verzenden van SMS-berichten en MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_6.png)

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Service ID]** en **[!UICONTROL API Token]**: als u toegang wilt tot de pagina met API&#39;s, vindt u uw referenties onder het tabblad SMS. Meer informatie in [Sectorale documentatie](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Opt-In Keywords]**: voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-In Message]**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-In Message]**: voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-In Message]**.

   * **[!UICONTROL Opt-Out Keywords]**: voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **[!UICONTROL Opt-Out Message]**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Opt-Out Message]**: voer de aangepaste reactie in die automatisch als uw **[!UICONTROL Opt-Out Message]**.

   * **[!UICONTROL Help Keywords]**: voer de standaardtrefwoorden of aangepaste trefwoorden in die automatisch uw **Help-bericht**. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden.

   * **[!UICONTROL Help Message]**: voer de aangepaste reactie in die automatisch als uw **Help-bericht**.

   * **[!UICONTROL Double Opt-In Keywords]**: voer de trefwoorden in die het dubbele aanmeldingsproces activeren. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging. Gebruik voor meerdere trefwoorden door komma&#39;s gescheiden waarden. [Meer informatie over de dubbele aanmelding voor SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Double Opt-In Message]**: voer de aangepaste reactie in die automatisch wordt verzonden als reactie op de dubbele aanmeldingsbevestiging.

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak voor SMS-berichten maken. [Meer informatie](sms-configuration-surface.md)

## Referenties voor MMS API instellen {#sinch-mms}

>[!IMPORTANT]
>
> Samen met de opstelling MMS, moet u ook de geloofsbrieven van Sinch API tot stand brengen specifiek voor het volgen van binnenkomende berichten en het beheren van toestemmingsverzoeken.

Voer de volgende stappen uit om Sinch MMS te configureren voor het verzenden van MMS met Journey Optimizer:

1. Blader in de linkertrack naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u de **[!UICONTROL API Credentials]** -menu. Klik op de knop **[!UICONTROL Create new API credentials]**.

   ![](assets/sms_6.png)

1. Configureer uw SMS API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]**: kies een naam voor uw API-referentie.

   * **[!UICONTROL Project ID]**, **[!UICONTROL App ID]** en **[!UICONTROL API Token]**: in het menu Conversation API vindt u uw referenties in het menu App. Meer informatie in [Sectorale documentatie](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * **[!UICONTROL Service Plan ID]** en **[!UICONTROL SMS API Token]**: Uw **[!UICONTROL Service Plan ID]** en **[!UICONTROL SMS API Token]** bevinden zich op het tabblad SMS van de pagina met API&#39;s.

1. Klikken **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Nadat u de API-referentie hebt gemaakt en geconfigureerd, moet u nu een kanaaloppervlak voor MMS-berichten maken. [Meer informatie](sms-configuration-surface.md)
