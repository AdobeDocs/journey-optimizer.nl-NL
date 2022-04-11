---
title: Configuratie bestemmingspagina
description: Leer hoe u uw omgeving configureert voor het maken en gebruiken van bestemmingspagina's met Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 62d8f4b0caa4ed74991e92475392c3278bdf5317
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# Landingspagina’s configureren {#lp-configuration}

## Subdomeinen van bestemmingspagina configureren {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Een voorinstelling voor een openingspagina maken"
>abstract="Als u een voorinstelling voor een bestemmingspagina wilt maken, moet u ervoor zorgen dat u eerder ten minste één subdomein van de bestemmingspagina hebt geconfigureerd om te kiezen uit de lijst met subdomeinnamen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="Voorinstellingen voor openingspagina&#39;s maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Een subdomein van een bestemmingspagina delegeren"
>abstract="U moet een subdomein configureren om te gebruiken voor uw bestemmingspagina&#39;s, aangezien u dit subdomein nodig hebt om een voorinstelling voor een bestemmingspagina te maken. U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd of een nieuw subdomein vormen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="Voorinstellingen voor openingspagina&#39;s maken"

Om in staat te zijn [voorinstellingen voor openingspagina&#39;s maken](#lp-create-preset), moet u de subdomeinen instellen die u voor de bestemmingspagina&#39;s wilt gebruiken.

U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of u kunt een ander subdomein vormen. Meer informatie over het delegeren van subdomeinen naar Adobe in [deze sectie](delegate-subdomain.md).

### Een bestaand subdomein gebruiken {#lp-use-existing-subdomain}

Voer de onderstaande stappen uit om een subdomein te gebruiken dat al is gedelegeerd aan Adobe.

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

   ![](assets/lp_access-subdomains.png)

1. Klik op **[!UICONTROL Set up subdomain]**.

   ![](assets/lp_set-up-subdomain.png)

1. Selecteren **[!UICONTROL Use delegated domain]** van de **[!UICONTROL Configuration type]** sectie.

   ![](assets/lp_use-delegated-subdomain.png)

1. Voer het voorvoegsel in dat wordt weergegeven in de URL van de bestemmingspagina.

   >[!NOTE]
   >
   >Alleen alfanumerieke tekens en afbreekstreepjes zijn toegestaan.

1. Selecteer een gedelegeerd subdomein in de lijst.

   >[!NOTE]
   >
   >U kunt geen subdomein selecteren dat al wordt gebruikt als subdomein van de bestemmingspagina.

   ![](assets/lp_prefix-and-subdomain.png)

   >[!CAUTION]
   >
   >Als u een domein selecteert dat aan Adobe werd gedelegeerd gebruikend [CNAME, methode](delegate-subdomain.md#cname-subdomain-delegation), moet u het DNS-record op uw hostingplatform maken. Om het DNS verslag te produceren, is het proces het zelfde als wanneer u een nieuw landend paginasubdomain vormt. Meer informatie over [deze sectie](#lp-configure-new-subdomain).

1. Klik op **[!UICONTROL Submit]**.

1. Na verzending wordt het subdomein in de lijst weergegeven met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Voordat u dat subdomein kunt gebruiken om berichten te verzenden, moet u wachten tot Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. Deze kan worden gebruikt om voorinstellingen voor openingspagina&#39;s te maken.

### Een nieuw subdomein configureren {#lp-configure-new-subdomain}

Volg onderstaande stappen om een nieuw subdomein te configureren.

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteren **[!UICONTROL Add your own domain]** van de **[!UICONTROL Configuration type]** sectie.

   ![](assets/lp_add-your-own-subdomain.png)

1. Geef het subdomein op dat u wilt delegeren.

   >[!CAUTION]
   >
   >U kunt geen bestaand subdomein van een bestemmingspagina gebruiken.

   Het delegeren van een ongeldig subdomein aan Adobe is niet toegestaan. Zorg ervoor u een geldig subdomein ingaat dat door uw organisatie, zoals marketing.yourcompany.com wordt bezeten.

   Subdomeinen op meerdere niveaus, zoals &#39;email.marketing.yourcompany.com&#39;, worden momenteel niet ondersteund.

1. Het verslag dat in uw DNS serververtoningen moet worden geplaatst. Kopieer deze record of download een CSV-bestand en navigeer vervolgens naar de oplossing voor domeinhosting om de overeenkomende DNS-record te genereren.

1. Zorg ervoor dat DNS het verslag in uw domein-ontvangende oplossing is geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;, dan klik **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Wanneer u een nieuw het landen paginasubdomain vormt, zal het altijd aan een verslag van de NAAM richten.

1. Nadat de subdomeindelegatie is verzonden, wordt het subdomein weergegeven in de lijst met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Voordat u dat subdomein kunt gebruiken om berichten te verzenden, moet u wachten tot Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.<!--Learn more in [this section](#subdomain-validation).-->

1. Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. Deze kan worden gebruikt om voorinstellingen voor openingspagina&#39;s te maken.

   Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.

## Voorinstellingen voor openingspagina definiëren {#lp-define-preset}

Wanneer [een openingspagina maken](../landing-pages/create-lp.md#create-a-lp), moet u een voorinstelling voor een bestemmingspagina selecteren om de bestemmingspagina te kunnen samenstellen en er doorheen te kunnen gaan **[!DNL Journey Optimizer]**.

### Voorinstellingen voor openingspagina&#39;s openen {#lp-presets}

Volg onderstaande stappen om voorinstellingen voor openingspagina&#39;s te openen.

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** -menu.

1. Selecteer **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Klik op een vooraf ingesteld label voor toegang tot de details van de voorinstelling voor de openingspagina.

   ![](assets/lp_preset-details.png)

### Een voorinstelling voor een openingspagina maken {#lp-create-preset}

Volg onderstaande stappen om een voorinstelling voor een openingspagina te maken.

>[!NOTE]
>
>Als u een voorinstelling wilt maken, moet u ervoor zorgen dat u eerder ten minste één subdomein van de bestemmingspagina hebt geconfigureerd. [Meer informatie](#lp-subdomains)

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Selecteer **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Voer een naam en een beschrijving in voor de voorinstelling.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

1. Selecteer een subdomein van een bestemmingspagina in de vervolgkeuzelijst.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Om een subdomein te kunnen selecteren, zorg ervoor u eerder minstens één het landen paginasubdomain hebt gevormd. [Meer informatie](#lp-subdomains)

   De instellingen die overeenkomen met de geselecteerde subdomeinweergave.

1. Als u het subdomein van de bestemmingspagina als volgende URL wilt selecteren, controleer **[!UICONTROL Same as landing page subdomain]** optie. [Meer informatie over bijhouden](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Als de bestemmingspagina-URL bijvoorbeeld &#39;pages.mail.luma.com&#39; is en de URL voor bijhouden &#39;data.mail.luma.com&#39;, kunt u &#39;pages.mail.luma.com&#39; kiezen die u wilt gebruiken als subdomein voor bijhouden.

1. Klikken **[!UICONTROL Submit]** om het maken van de voorinstelling voor de bestemmingspagina te bevestigen. U kunt de voorinstelling ook opslaan als concept en de configuratie ervan later hervatten.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Nadat de voorinstelling voor de openingspagina is gemaakt, wordt deze in de lijst weergegeven met de **[!UICONTROL Active]** status. U kunt deze nu gebruiken voor uw bestemmingspagina&#39;s.

   ![](assets/lp-preset-active-temp.png)

U kunt nu [bestemmingspagina&#39;s maken](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].

>[!NOTE]
>
>Leer hoe u berichtvoorinstellingen voor pushmeldingen en e-mailberichten kunt maken in [deze sectie](message-presets.md).

**Verwante onderwerpen**:

* [Aan de slag met bestemmingspagina&#39;s](../landing-pages/get-started-lp.md)
* [Een landingspagina maken](../landing-pages/create-lp.md#create-a-lp)
