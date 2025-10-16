---
solution: Journey Optimizer
product: journey optimizer
title: Het SMS-kanaal configureren
description: Leer hoe u uw omgeving configureert voor het verzenden van tekstberichten met Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Aan de slag met de configuratie SMS / MMS / RCS {#sms-configuration}

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
>abstract="Voordat u tekstberichten (SMS/MMS) kunt verzenden, moet u de providerinstellingen integreren met Journey Optimizer. Zodra gedaan, moet u een configuratie tot stand brengen SMS/MMS. Deze stappen moeten worden uitgevoerd door een Adobe Journey Optimizer System Administrator."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Een SMS-kanaalconfiguratie maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecteer de configuratie van de leverancier van SMS"
>abstract="Selecteer de API geloofsbrieven die voor uw verkoper van SMS worden gevormd."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Fuzzy opt-out"
>abstract="Indien ingeschakeld, detecteert Fuzzy Opt-out binnenkomende berichten die sterk op gedefinieerde opt-out trefwoorden lijken (bijvoorbeeld CANCIL) en verzendt automatisch een bevestigingsantwoord om te controleren of de gebruiker zich niet abonneert. Als de gebruiker via de gedefinieerde prompt bevestigt, wordt het abonnement opgezegd."

Voordat u SMS, MMS of RCS verzendt, moet u de Adobe Journey Optimizer-omgeving configureren. Dit doet u als volgt:

1. Integreer de providerinstellingen met Journey Optimizer.
De stappen zijn afhankelijk van uw SMS-provider. Klik op de onderstaande koppelingen voor gedetailleerde documentatie:
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Aangepaste provider](sms-configuration-custom.md)
1. [Een SMS-configuratie maken](sms-configuration-surface.md)

Deze stappen moeten door een Beheerder van het Systeem van Adobe Journey Optimizer [&#x200B; worden uitgevoerd &#x200B;](../start/path/administrator.md).

## Vereisten{#sms-prerequisites}

Adobe Journey Optimizer is momenteel geïntegreerd met externe providers die services voor tekstberichten aanbieden die onafhankelijk zijn van Adobe Journey Optimizer. De gesteunde leveranciers voor tekstoverseinen en MMS zijn: **Sinch**, **Twilio** en **Infobip**. Merk op dat u extra overseinenleveranciers kunt vormen gebruikend de [&#x200B; configuratie van de douaneleverancier &#x200B;](sms-configuration-custom.md).

Voorafgaand aan het kanaalconfiguratie van SMS, moet u een rekening met één van deze leveranciers tot stand brengen om uw **Symbolische API** en **identiteitskaart van de Dienst** te krijgen, die u de verbinding tussen Adobe Journey Optimizer en de toepasselijke leverancier moet vormen.

Voor uw gebruik van tekstberichten en MMS-services gelden aanvullende voorwaarden van de betreffende provider. Als oplossingen van derden zijn Sinch, Twilio en Infobip via integratie beschikbaar voor Adobe Journey Optimizer-gebruikers. Adobe heeft geen controle en is niet verantwoordelijk voor producten van derden. Neem contact op met uw provider voor problemen met of verzoeken om assistentie met betrekking tot SMS/MMS.

>[!CAUTION]
>
>Als u SMS-subdomeinen wilt openen en bewerken, moet u over de machtiging **[!UICONTROL Manage SMS Subdomains]** in de productiesandbox beschikken. Leer meer over toestemmingen op [&#x200B; deze pagina &#x200B;](../administration/high-low-permissions.md#administration-permissions).
>

