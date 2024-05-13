---
solution: Journey Optimizer
product: journey optimizer
title: Het SMS-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a08a28d7bfe912ff545ca559bd04b70642fe2ab5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Ga aan de slag met de configuratie van SMS {#sms-configuration}

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
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="Een SMS-kanaaloppervlak maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecteer de configuratie van de leverancier van SMS"
>abstract="Selecteer de API geloofsbrieven die voor uw verkoper van SMS worden gevormd."

Voordat u SMS of MMS verzendt, moet u de Adobe Journey Optimizer-omgeving configureren. Dit doet u als volgt:

1. De providerinstellingen integreren met Journey Optimizer:
   * [Met Sinch](sms-configuration-sinch.md)
   * [Met Infobip](sms-configuration-infobip.md)
   * [Met Twilio](sms-configuration-twilio.md)
1. [Een SMS-oppervlak maken](sms-configuration-surface.md)

Deze stappen moeten worden uitgevoerd door een Adobe Journey Optimizer [Systeembeheerder](../start/path/administrator.md).

## Vereisten{#sms-prerequisites}

Adobe Journey Optimizer is momenteel geïntegreerd met externe providers die services voor tekstberichten aanbieden die onafhankelijk zijn van Adobe Journey Optimizer. Ondersteunde providers voor tekstberichten en MMS zijn: **Sinch**, **Twilio** en **Infobip**.

Voordat u de SMS-kanaalconfiguratie start, moet u een account met een van deze providers maken om uw **API-token** en **Service-id**, die u moet configureren tussen Adobe Journey Optimizer en de toepasselijke provider.

Voor uw gebruik van tekstberichten en MMS-services gelden aanvullende voorwaarden van de betreffende provider. Als oplossingen van derden zijn Sinch, Twilio en Infobip via integratie beschikbaar voor Adobe Journey Optimizer-gebruikers. Adobe heeft geen betrekking op producten van derden en is niet verantwoordelijk voor deze producten. Neem contact op met uw provider voor problemen met of verzoeken om assistentie met betrekking tot SMS/MMS.

>[!CAUTION]
>
>Om tot subdomeinen van SMS toegang te hebben en uit te geven, moet u hebben **[!UICONTROL Manage SMS Subdomains]** toestemming voor de productiesandbox. Meer informatie over machtigingen in [deze pagina](../administration/high-low-permissions.md#administration-permissions).
>

