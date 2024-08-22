---
title: Configuratie op basis van code
description: Codegebaseerde configuratie maken
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 1%

---

# Uw op code gebaseerde ervaring configureren {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="Toepassings-id"
>abstract="Geef de toepassings-id op voor nauwkeurige identificatie en configuratie binnen de operationele omgeving van de app, zodat u verzekerd bent van naadloze integratie en functionaliteit."

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Locatie op pagina"
>abstract="De locatie of het pad in het toepassingsveld geeft exact de bestemming aan in de app waartoe gebruikers toegang moeten hebben. Dit kan een bepaalde sectie of pagina diep zijn binnen de navigatiestructuur van de app."

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="OppervlakteURI"
>abstract="Een oppervlakte-URI fungeert als een nauwkeurige identificatie die naar verschillende elementen of componenten van de gebruikersinterface in een toepassing wordt geleid."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="Standaard URL voor ontwerpen en voorvertonen"
>abstract="Met dit veld zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een opgegeven URL hebben die essentieel is voor een effectieve weergave van inhoud en voor een voorvertoning."

## Een kanaalconfiguratie maken {#reatte-code-based-configuration}

Ga als volgt te werk om een kanaalconfiguratie te maken:

1. Open het menu **[!UICONTROL Channels]** > **[!UICONTROL General settings]** > **[!UICONTROL Channel configurations]** en klik op **[!UICONTROL Create channel configuration]** .

   ![](assets/code_config_1.png)

1. Voer een naam en beschrijving (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   > Namen moeten beginnen met een letter (A-Z). Het mag alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

1. Als u aangepaste of basislabels voor gegevensgebruik aan de configuratie wilt toewijzen, kunt u **[!UICONTROL Manage access]** selecteren. [ leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC) ](../administration/object-based-access.md).

1. Selecteer **[!UICONTROL Marketing action]**(s) om het toestemmingsbeleid aan de berichten te associëren gebruikend deze configuratie. Alle toestemmingsbeleid verbonden aan de marketing actie wordt gebruikt om de voorkeur van uw klanten te respecteren. [Meer informatie](../action/consent.md#surface-marketing-actions)

1. Selecteer **op code-Gebaseerd ervarings** kanaal.

   ![](assets/code_config_2.png)

1. Selecteer het platform waarvoor de code-basiservaring zal worden toegepast.

1. Voor web:

   * Geef een **[!UICONTROL Page URL]** op om wijzigingen alleen toe te passen op één pagina.

   * U kunt ook een **[!UICONTROL Pages matching rule]** maken om meerdere URL&#39;s als doel in te stellen die overeenkomen met de opgegeven regel. Dit kan bijvoorbeeld worden gebruikt om wijzigingen overal op een website toe te passen, zoals het bijwerken van een hoofdbanner op alle pagina&#39;s of het toevoegen van een bovenste afbeelding aan weergave op elke productpagina. [Meer informatie](../web/web-configuration.md)

1. Voor iOS en Android:

   * Voer de **[!UICONTROL App id]** en **[!UICONTROL Location or path inside the app]** in.

1. Selecteer Overige als platform als uw implementatie niet voor Web, iOS of Android is of als u specifieke URI&#39;s moet opgeven. Wanneer u meerdere platforms kiest of meerdere URI&#39;s toevoegt, wordt de inhoud geleverd aan alle geselecteerde pagina&#39;s of toepassingen.

   * Voer de **[!UICONTROL Surface URI]** in.

   >[!CAUTION]
   >
   >Zorg ervoor dat het oppervlak-URI dat in uw op code gebaseerde campagne wordt gebruikt, overeenkomt met het oppervlak dat in uw eigen implementatie wordt gebruikt. Anders worden de wijzigingen niet doorgevoerd.

1. Kies de indeling die de toepassing op die specifieke locatie verwacht. Dit wordt gebruikt wanneer het ontwerpen van de code-gebaseerde ervaring in campagnes en reizen.

1. Verzend uw wijzigingen.

U kunt nu uw configuratie selecteren wanneer u uw op code-gebaseerde ervaring creeert.


## Wat is een oppervlak? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definieer een op code gebaseerde ervaringsconfiguratie"
>abstract="Een op code-gebaseerde configuratie bepaalt de weg en de plaats binnen uw toepassing, uniek geïdentificeerd door URI in de toepassingsimplementatie, waar de inhoud zal worden geleverd en worden verbruikt."

A **code-based ervaringsoppervlakte** is om het even welke entiteit die voor gebruiker of systeeminteractie wordt ontworpen, die uniek door URI wordt geïdentificeerd. Het oppervlak wordt opgegeven in de implementatie van de toepassing en moet overeenkomen met het oppervlak dat is samengesteld in de configuratie van het ervaringskanaal op basis van code.

Wanneer het creëren van een code-gebaseerde configuratie van het ervaringskanaal - voor de platforms van het Web, iOS en Android, moet u een weg en een plaats ingaan om de oppervlakte samen te stellen, terwijl als het platform Andere is u volledige URI, zoals in de voorbeelden hieronder zult moeten ingaan.

Met andere woorden, kan een oppervlakte als container op om het even welk niveau van hiërarchie met een entiteit (touchpoint) worden gezien die bestaat.<!--good idea to illustrate how it can be seen, but to clarify-->

* Dit kan een webpagina, een mobiele app, een bureaubladtoepassing, een specifieke inhoudslocatie binnen een grotere entiteit (bijvoorbeeld a `div` ) of een niet-standaard weergavepatroon (bijvoorbeeld een kiosk of een bureaubladtoepassingsbanner) zijn. <!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Het kan zich ook uitstrekken tot specifieke stukken inhoudscontainers voor niet-display of abstracted-display doeleinden (bijvoorbeeld JSON-lobs die aan services worden geleverd).

* Dit kan ook een jokeroppervlak zijn dat overeenkomt met verschillende definities van het clientoppervlak (zo kan een locatie van een hoofdafbeelding op elke pagina van uw website bijvoorbeeld worden vertaald in een oppervlak-URI, zoals: web://mydomain.com/*#hero_image).

Een oppervlak-URI bestaat in principe uit meerdere secties:
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

