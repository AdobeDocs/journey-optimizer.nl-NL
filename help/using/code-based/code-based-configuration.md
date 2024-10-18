---
title: Configuratie op basis van code
description: Codegebaseerde configuratie maken
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: b057d198d3c5b12121ee50d7a97ff4b33b8209b4
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 1%

---

# Uw op code gebaseerde ervaring configureren {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definieer een op code gebaseerde ervaringsconfiguratie"
>abstract="Een op code-gebaseerde configuratie bepaalt de weg en de plaats binnen uw toepassing, uniek geïdentificeerd door URI in de toepassingsimplementatie, waar de inhoud zal worden geleverd en worden verbruikt."

Alvorens [ bouwend uw ervaring ](create-code-based.md), moet u een op code-gebaseerde ervaringsconfiguratie tot stand brengen waarin u bepaalt waar de inhoud binnen uw toepassing zal worden geleverd en worden verbruikt.

Een op code-gebaseerde ervaringsconfiguratie moet naar de oppervlakte verwijzen, die fundamenteel de plaats is waar u uw veranderingen wilt teruggeven. Volgens het geselecteerde platform moet u een locatie/pad of de volledige oppervlakte-URI invoeren. [Meer informatie](#surface-definition)

## Een op code gebaseerde ervaringsconfiguratie maken {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Geef de specifieke locatie op uw pagina of app aan"
>abstract="In dit veld wordt de exacte bestemming aangegeven binnen een pagina of in de app waartoe gebruikers toegang moeten hebben. Het kan een bepaalde sectie binnen een webpagina zijn, of een pagina diep binnen de navigatiestructuur van de app."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="Een URL definiëren voor het maken en voorvertonen van inhoud"
>abstract="Met dit veld zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een opgegeven URL hebben die essentieel is voor een effectieve weergave van inhoud en voor een voorvertoning."

Ga als volgt te werk om een op code gebaseerde configuratie van het ervaringskanaal te maken:

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/code_config_1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer op het Toegangsbeheer van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md)

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Selecteer het **op code-Gebaseerde ervarings** kanaal.

   ![](assets/code_config_2.png)

1. Selecteer het platform waarop de basiscode wordt toegepast:

   * [Web](#web)
   * [iOS en/of Android](#mobile)
   * [Overige](#other)

   >[!NOTE]
   >
   >U kunt verschillende platforms selecteren. Wanneer u meerdere platforms kiest, wordt de inhoud geleverd aan alle geselecteerde pagina&#39;s of apps.

1. Kies de indeling die de toepassing voor deze specifieke locatie verwacht. Dit wordt gebruikt wanneer het ontwerpen van de code-gebaseerde ervaring in campagnes en reizen.

   ![](assets/code_config_4.png)

1. Klik op **[!UICONTROL Submit]** om de wijzigingen op te slaan.

U kunt deze configuratie nu selecteren wanneer [ creërend een code-gebaseerde ervaring ](create-code-based.md) in uw campagnes en reizen.

>[!NOTE]
>
>Het implementatieteam van uw app is verantwoordelijk voor het uitvoeren van expliciete API- of SDK-aanroepen om inhoud op te halen voor de oppervlakken die zijn gedefinieerd in de geselecteerde op code gebaseerde ervaringsconfiguratie. Leer meer op de verschillende klantenimplementaties in [ deze sectie ](code-based-implementation-samples.md).

### Webplatforms {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="Een URL definiëren voor het ontwerpen en voorvertonen van inhoud"
>abstract="Met dit veld zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een opgegeven URL hebben die essentieel is voor een effectieve weergave van inhoud en voor een voorvertoning."

Volg onderstaande stappen om de op code gebaseerde instellingen voor ervaringsconfiguratie voor webplatforms te definiëren.

1. Selecteer een van de volgende opties:

   * **[!UICONTROL Single page]** - Als u de wijzigingen uitsluitend op één pagina wilt toepassen, voert u een **[!UICONTROL Page URL]** in.

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL Pages matching rule]** - Als u meerdere URL&#39;s met dezelfde regel als doel wilt instellen, maakt u een of meer regels. [Meer informatie](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     Als u bijvoorbeeld elementen wilt bewerken die op alle pagina&#39;s met vrouwenproducten van uw Luma-website worden weergegeven, selecteert u **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` en **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women` .

     ![](assets/code_config_matching_rules.png)

1. Het volgende is van toepassing op de voorbeeld-URL:

   * Als er één pagina-URL wordt ingevoerd, wordt die URL gebruikt voor de voorvertoning. U hoeft geen andere URL in te voeren.
   * Als a [ pagina&#39;s passende regel ](../web/web-configuration.md#web-page-matching-rule) wordt geselecteerd, moet u a **[!UICONTROL Default authoring and preview URL]** ingaan die aan voorproef de ervaring in browser zal worden gebruikt. [Meer informatie](../code-based/create-code-based.md#preview-on-device)

     ![](assets/code_config_matching_rules_preview.png)

1. In het veld **[!UICONTROL Location on page]** wordt de exacte bestemming opgegeven binnen de pagina waartoe gebruikers toegang moeten krijgen. Het kan een bepaalde sectie op een pagina binnen de navigatie-structuur van de plaats, zoals &quot;held-banner&quot; of &quot;product-rail&quot; zijn.

   ![](assets/code_config_location_on_page.png)

### Mobiele platforms (iOS en Android) {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="Geef uw toepassings-id op"
>abstract="Voer de toepassings-id in voor nauwkeurige identificatie en configuratie binnen de operationele omgeving van de toepassing, zodat u verzekerd bent van naadloze integratie en functionaliteit."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="Geef de URL voor het voorvertonen van inhoud op"
>abstract="Dit veld is essentieel voor het inschakelen van de simulatie en voorvertoning van uw inhoud rechtstreeks op uw apparaat in de toepassing."

Volg onderstaande stappen om de op code gebaseerde instellingen voor ervaringsconfiguratie voor mobiele platforms te definiëren.

1. Voer uw **[!UICONTROL App id]** in. Dit zorgt voor een nauwkeurige identificatie en configuratie binnen de operationele omgeving van de app en voor naadloze integratie en functionaliteit.

1. Geef de **[!UICONTROL Location or path inside the app]** op. In dit veld wordt de exacte bestemming aangegeven in de app waartoe gebruikers toegang moeten krijgen. Het kan een bepaalde sectie of pagina diep binnen de navigatiestructuur van de app zijn, zoals &#39;hero-banner&#39; of &#39;product-rail&#39;.

   ![](assets/code_config_3.png)

1. Vul het veld **[!UICONTROL Preview URL]** in om voorvertoningen op het apparaat in te schakelen. Deze URL informeert de voorbeeldservice over de specifieke URL die moet worden gebruikt wanneer voorvertoning op apparaat wordt geactiveerd. [Meer informatie](../code-based/create-code-based.md#preview-on-device)

   De URL van de voorvertoning is een diepe koppeling die door de ontwikkelaar van de app in uw app is geconfigureerd. Zo zorgt u ervoor dat alle URL&#39;s die overeenkomen met het deep link-schema, in de app worden geopend in plaats van in een mobiele webbrowser. Neem contact op met de ontwikkelaar van de app om het deep link-schema voor uw app te verkrijgen.

+++  De volgende bronnen kunnen u helpen bij het configureren van diepe koppelingen voor uw app-implementatie

   * Voor Android:

      * [ creeer Diepe Verbindingen aan de Context van de Toepassing ](https://developer.android.com/training/app-links/deep-linking)

   * Voor iOS:

      * [ het bepalen van een Regeling van Douane URL voor Uw app ](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

      * [ ondersteunend Universele Verbindingen in Uw app ](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >Als u kwesties terwijl het previewing van de ervaring ontmoet, gelieve te verwijzen naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link).

### Andere platforms {#other}

Volg de onderstaande stappen om de op code gebaseerde instellingen voor ervaringsconfiguratie voor andere platforms te definiëren (zoals videoconsoles, met tv verbonden apparaten, slimme tv&#39;s, kiosken, ATM&#39;s, spraakassistenten, IoT-apparaten, enz.).

1. Selecteer **[!UICONTROL Other]** als het platform als uw implementatie niet voor Web, iOS of Android is, of als u specifieke URI&#39;s moet instellen.

1. Voer de **[!UICONTROL Surface URI]** in. Een oppervlakte-URI is een unieke identificatie die correspondeert met de entiteit waar u uw ervaring wilt leveren. [Meer informatie](#surface-definition)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >Zorg ervoor u een oppervlakte URI ingaat die in uw eigen implementatie wordt gebruikt. Anders kunnen de wijzigingen niet worden uitgevoerd.

1. **[!UICONTROL Add another surface URI]** indien nodig. U kunt maximaal 10 URI&#39;s toevoegen.

   >[!NOTE]
   >
   >Wanneer u meerdere URI&#39;s toevoegt, wordt de inhoud aan alle vermelde componenten geleverd.

## Wat is een oppervlak? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="De oppervlak-URI voor de component toevoegen"
>abstract="Als uw implementatie niet voor Web, iOS, of Android is, of als u specifieke URIs moet richten, ga een oppervlakte URI in, die een unieke herkenningsteken richtend aan de entiteit is waar u uw ervaring wilt leveren. Zorg ervoor u een oppervlakte URI ingaat die in uw eigen implementatie wordt gebruikt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/code-based-configuration#other" text="Creeer een code-gebaseerde ervaringsconfiguratie voor Andere platforms"

Een op code-gebaseerde ervaring **oppervlakte** is om het even welke entiteit die voor gebruiker of systeeminteractie wordt ontworpen, die uniek door een **URI** wordt geïdentificeerd. Het oppervlak wordt opgegeven in de implementatie van de toepassing en moet overeenkomen met het oppervlak waarnaar wordt verwezen in uw op code gebaseerde configuratie van het ervaringskanaal.

Een oppervlak kan worden beschouwd als een container op elk hiërarchisch niveau met een bestaande entiteit (aanraakpunt).

* Dit kan een webpagina, een mobiele app, een bureaubladtoepassing, een specifieke inhoudslocatie binnen een grotere entiteit (bijvoorbeeld a `div` ) of een niet-standaard weergavepatroon (bijvoorbeeld een kiosk of een bureaubladtoepassingsbanner) zijn. <!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Het kan zich ook uitstrekken tot specifieke stukken inhoudscontainers voor niet-display of abstracted-display doeleinden (bijvoorbeeld JSON-lobs die aan services worden geleverd).

* Dit kan ook een jokeroppervlak zijn dat overeenkomt met verschillende definities van het clientoppervlak (zo kan een locatie van een hoofdafbeelding op elke pagina van uw website bijvoorbeeld worden vertaald in een oppervlak-URI, zoals: web://mydomain.com/*#hero_image).

Wanneer u een op code gebaseerde configuratie van het ervaringskanaal maakt, hebt u twee manieren om het oppervlak op te geven op basis van het geselecteerde platform:

* Voor **[!UICONTROL Web]**, **[!UICONTROL iOS]** en **[!UICONTROL Android]** platforms, moet u a **plaats of weg** ingaan om de oppervlakte samen te stellen.

* Als het platform **[!UICONTROL Other]** is, moet u de volledige **oppervlakte URI** ingaan, zoals in de hieronder voorbeelden.

Een oppervlakte-URI fungeert als een nauwkeurige identificatie die naar verschillende elementen of componenten van de gebruikersinterface binnen een toepassing wordt geleid. Een oppervlak-URI bestaat uit meerdere secties:

1. **Type**: Web, mobileapp, atm, kiosk, tvcd, de dienst, enz.
1. **Bezit**: pagina URL of app bundel
1. **Container**: plaats op de pagina/app activiteit

In de onderstaande tabellen staan enkele voorbeelden van de oppervlakte-URI-definitie voor verschillende apparaten.

**Web en mobiel**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Vertegenwoordigt een individueel element binnen een specifieke pagina van een specifiek domein, waar een element een etiket zoals in de volgende voorbeelden kan zijn: hero_banner, top_nav, menu, footer, enz. |
| iOS-app | `mobileapp://com.vendor.bundle/activity#element` | Vertegenwoordigt een specifiek element binnen een inheemse toepassingsactiviteit, zoals een knoop of ander meningselement. |
| Android-app | `mobileapp://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een native app. |

**Andere apparatentypen**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Desktop | `desktop://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een toepassing, zoals een knoop, een menu, een heldenbanner, enz. |
| TV-app | `tvcd://com.vendor.bundle/#element` | Vertegenwoordigt een specifiek element binnen een apparaat dat op een slimme tv of tv is aangesloten - bundel-id. |
| Service | `service://servicename/#element` | Vertegenwoordigt een server-zijproces of andere handentiteit. |
| Kiosk | `kiosk://location/screen#element` | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |
| ATM | `atm://location/screen#element` | Voorbeeld van mogelijke extra oppervlaktetypen die gemakkelijk kunnen worden toegevoegd. |

**de oppervlakken van de Vervanging**

| Type | URI | Beschrijving |
| --------- | ----------- | ------- | 
| Jokertekenweb | `wildcard:web://domain.com/*#element` | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder een specifiek domein. |
| Jokertekenweb | `wildcard:web://*domain.com/*#element` | Jokeroppervlak - vertegenwoordigt een afzonderlijk element op elke pagina onder alle domeinen die eindigen met &quot;domain.com&quot;. |
