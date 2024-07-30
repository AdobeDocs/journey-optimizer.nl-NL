---
solution: Journey Optimizer
product: journey optimizer
title: Het SMS-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '342'
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
   * [Met een aangepaste provider](sms-configuration-custom.md)
1. [Een SMS-oppervlak maken](sms-configuration-surface.md)

Deze stappen moeten door een Beheerder van het Systeem van Adobe Journey Optimizer [ worden uitgevoerd ](../start/path/administrator.md).

## Vereisten{#sms-prerequisites}

Adobe Journey Optimizer is momenteel geïntegreerd met externe providers die services voor tekstberichten aanbieden die onafhankelijk zijn van Adobe Journey Optimizer. De gesteunde leveranciers voor tekstoverseinen en MMS zijn: **Sinch**, **Twilio** en **Infobip**.

Voorafgaand aan het kanaalconfiguratie van SMS, moet u een rekening met één van deze leveranciers tot stand brengen om uw **Symbolische API** en **identiteitskaart van de Dienst** te krijgen, die u de verbinding tussen Adobe Journey Optimizer en de toepasselijke leverancier moet vormen.

Voor uw gebruik van tekstberichten en MMS-services gelden aanvullende voorwaarden van de betreffende provider. Als oplossingen van derden zijn Sinch, Twilio en Infobip via integratie beschikbaar voor Adobe Journey Optimizer-gebruikers. Adobe heeft geen betrekking op producten van derden en is niet verantwoordelijk voor deze producten. Neem contact op met uw provider voor problemen met of verzoeken om assistentie met betrekking tot SMS/MMS.

>[!CAUTION]
>
>Als u SMS-subdomeinen wilt openen en bewerken, moet u over de machtiging **[!UICONTROL Manage SMS Subdomains]** in de productiesandbox beschikken. Leer meer over toestemmingen in [ deze pagina ](../administration/high-low-permissions.md#administration-permissions).
>

