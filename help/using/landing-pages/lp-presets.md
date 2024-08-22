---
solution: Journey Optimizer
product: journey optimizer
title: Voorinstellingen voor openingspagina definiëren
description: Leer hoe u uw omgeving configureert voor het maken en gebruiken van bestemmingspagina's met Journey Optimizer
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: landen, landen pagina, vormen, milieu, subdomein, vooraf instelt
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 2%

---

# Voorinstellingen voor openingspagina definiëren {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Een voorinstelling voor een openingspagina maken"
>abstract="Als u een bestemmingspagina wilt maken en deze via Journey Optimizer wilt gebruiken, moet u een voorinstelling voor een bestemmingspagina maken die het te gebruiken subdomein bevat."

Wanneer [ creërend een het landen pagina ](../landing-pages/create-lp.md#create-a-lp), moet u een het landen vooraf ingestelde pagina selecteren om de het landen pagina en hefboomwerking het door **[!DNL Journey Optimizer]** te kunnen bouwen.

## Voorinstellingen voor openingspagina&#39;s openen {#access-lp-presets}

Volg onderstaande stappen om voorinstellingen voor openingspagina&#39;s te openen.

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** .

1. Selecteer **[!UICONTROL Landing page settings]** > **[!UICONTROL Landing page presets]** .

   ![](assets/lp_presets-access.png)

1. Klik op een vooraf ingesteld label voor toegang tot de details van de voorinstelling voor de openingspagina.

   ![](assets/lp_preset-details.png)

## Een voorinstelling voor een openingspagina maken {#lp-create-preset}

Voer de onderstaande stappen uit om een voorinstelling voor een openingspagina te maken.

>[!NOTE]
>
>Als u een voorinstelling wilt maken, moet u ervoor zorgen dat u eerder ten minste één subdomein van de bestemmingspagina hebt geconfigureerd. [ leer hoe ](lp-subdomains.md)

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer vervolgens **[!UICONTROL Landing page settings]** > **[!UICONTROL Landing page presets]** .

1. Selecteer **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Voer een naam en een beschrijving in voor de voorinstelling.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Selecteer een subdomein van een bestemmingspagina in de vervolgkeuzelijst.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Om een subdomein te kunnen selecteren, zorg ervoor u eerder minstens één het landen paginasubdomain hebt gevormd. [ leer hoe ](#lp-subdomains)

   De instellingen die overeenkomen met de geselecteerde subdomeinweergave.

1. Als u het subdomein van de bestemmingspagina voor het volgen URL wilt selecteren, controleer de **[!UICONTROL Same as landing page subdomain]** optie. [ Leer meer bij het volgen ](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Als de bestemmingspagina-URL bijvoorbeeld &#39;pages.mail.luma.com&#39; is en de URL voor bijhouden &#39;data.mail.luma.com&#39;, kunt u &#39;pages.mail.luma.com&#39; kiezen die u wilt gebruiken als subdomein voor bijhouden.

1. Klik op **[!UICONTROL Submit]** om het maken van de voorinstelling voor de openingspagina te bevestigen. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Nadat de voorinstelling voor de openingspagina is gemaakt, wordt deze in de lijst weergegeven met de status **[!UICONTROL Active]** . U kunt deze nu gebruiken voor uw bestemmingspagina&#39;s.

U bent nu klaar om landende pagina&#39;s ](../landing-pages/create-lp.md) in [!DNL Journey Optimizer] te creëren.[
<!--
>[!NOTE]
>
>Learn how to create channel configurations for push notifications and emails in [this section](channel-surfaces.md).-->

**Verwante onderwerpen**:

* [Aan de slag met bestemmingspagina&#39;s](../landing-pages/get-started-lp.md)
* [Een landingspagina maken](../landing-pages/create-lp.md#create-a-lp)
