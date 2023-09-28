---
solution: Journey Optimizer
product: journey optimizer
title: Websubdomeinen configureren
description: Leer hoe u websubdomeinen instelt met Journey Optimizer
role: Admin
level: Intermediate
keywords: web, subdomeinen, configuratie
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: e26f45c1c08e1e5c88daf72cafdcd979753cc692
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Websubdomeinen configureren {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Een websubdomein delegeren"
>abstract="U stelt het subdomein in voor gebruik met een webkanaal. U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd of een ander subdomein vormen."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Een websubdomein delegeren"
>abstract="Als u inhoud van de Adobe Experience Manager Assets Essentials toevoegt aan uw webervaringen, moet u het subdomein instellen dat wordt gebruikt om deze inhoud te publiceren. Selecteer een subdomein dat al is gedelegeerd aan de Adobe of configureer een nieuw subdomein."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Een websubdomein instellen"
>abstract="Selecteer een subdomein in de lijst met subdomeinen die zijn gedelegeerd aan de Adobe. U kunt dit websubdomein instellen als het standaardsubdomein, maar er kan slechts één standaardsubdomein tegelijk worden gebruikt."

Als u tijdens het ontwerpen van een webversie inhoud toevoegt die afkomstig is van de [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) moet u het subdomein instellen dat wordt gebruikt om deze inhoud te publiceren.

U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of u kunt een ander subdomein vormen. Meer informatie over het delegeren van subdomeinen naar Adobe in [deze sectie](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>De subdomeinconfiguratie van het Web is gemeenschappelijk voor alle milieu&#39;s. Daarom geldt het volgende:
>
>* Als u websubdomeinen wilt openen en bewerken, moet u beschikken over **[!UICONTROL Manage Web Subdomains]** toestemming voor de productiesandbox.
>
> * Elke wijziging aan een websubdomein heeft ook invloed op de productiesandboxen.

U kunt meerdere subdomeinen voor het web maken, maar alleen de subdomeinen **default** subdomein wordt gebruikt. U kunt het standaardwebsubdomein wijzigen, maar u kunt slechts één subdomein tegelijk gebruiken.

## Websubdomeinen openen en beheren {#access-web-subdomains}

1. Ga naar de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Web configuration]** > **[!UICONTROL Web subdomains]**. Alle subdomeinen die zijn ingesteld met de huidige sandbox worden weergegeven.

   ![](assets/web-access-subdomains.png)

1. U kunt filteren op de gebruiker die elk subdomein of één van de delegatiestatus (**[!UICONTROL Draft]**, **[!UICONTROL Processing]**, **[!UICONTROL Success]** of **[!UICONTROL Failed]**).

   ![](assets/web-filter-subdomains.png)

1. De **[!UICONTROL Default]** badge wordt weergegeven naast het subdomein dat momenteel als standaard wordt gebruikt. Als u het standaardsubdomein wilt wijzigen, selecteert u **[!UICONTROL Set as default]** van de **[!UICONTROL More actions]** naast het gewenste subdomein.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >U kunt het standaardwebsubdomein wijzigen, maar u kunt slechts één subdomein tegelijk gebruiken.

## Een bestaand subdomein gebruiken {#web-use-existing-subdomain}

Volg onderstaande stappen om een subdomein te gebruiken dat al is gedelegeerd aan Adobe.

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Web configuration]** > **[!UICONTROL Web subdomains]**.

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteer de **[!UICONTROL Use delegated subdomain]** van de **[!UICONTROL Configuration type]** en kiest u een gedelegeerd subdomein in de lijst.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >U kunt geen subdomein selecteren dat al als websubdomein wordt gebruikt.

1. Het voorvoegsel dat wordt weergegeven in de URL wordt automatisch toegevoegd. U kunt dit niet wijzigen.

1. Als u dit subdomein als standaard wilt instellen, selecteert u de bijbehorende optie.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Alleen de **default** subdomein wordt gebruikt.

1. Klik op **[!UICONTROL Submit]**. Het subdomein krijgt de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt voor uw webervaringen.

   >[!NOTE]
   >
   >In zeer zeldzame gevallen, kon een subdomain opstelling ontbreken. In dit geval kunt u de opdracht **[!UICONTROL Failed]** subdomein om de lijst op te schonen met de opdracht **[!UICONTROL Delete]** van de knop **[!UICONTROL More actions]** pictogram.

## Een nieuw subdomein configureren {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="De overeenkomende DNS-record genereren"
>abstract="Om een nieuw Web subdomain te vormen, moet u de Adobe nameserverinformatie kopiëren die in de interface van Journey Optimizer wordt getoond en het kleven in uw domein-ontvangende oplossing om het passende DNS verslag te produceren. Wanneer de controles zijn voltooid, kan het subdomein worden gebruikt om inhoud te publiceren die afkomstig is uit de Experience Manager Assets Essentials-bibliotheek."

Volg onderstaande stappen om een nieuw subdomein te configureren.

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL web configuration]** > **[!UICONTROL web subdomains]**.

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteren **[!UICONTROL Add your own domain]** van de **[!UICONTROL Configuration type]** sectie.

1. Geef het subdomein op dat u wilt delegeren.

   >[!CAUTION]
   >
   >U kunt geen bestaand websubdomein gebruiken.
   >
   >Hoofdletters zijn niet toegestaan in subdomeinen.

   ![](assets/web-add-your-own-domain.png)

   Het delegeren van een ongeldig subdomein aan Adobe wordt niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   >[!NOTE]
   >
   >Subdomeinen op meerdere niveaus (van hetzelfde bovenliggende domein) worden ondersteund. U kunt bijvoorbeeld &#39;web.marketing.yourcompany.com&#39; gebruiken.

1. Als u dit subdomein als standaard wilt instellen, selecteert u de bijbehorende optie.

   >[!NOTE]
   >
   >Alleen de **default** subdomein wordt gebruikt.

1. Het verslag dat in uw DNS serververtoningen moet worden geplaatst. Kopieer deze record of download een CSV-bestand en navigeer vervolgens naar de oplossing voor domeinhosting om de overeenkomende DNS-record te genereren.

1. Zorg ervoor dat DNS het verslag in uw domein-ontvangende oplossing is geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;, dan klik **[!UICONTROL Submit]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   >[!NOTE]
   >
   >Wanneer u een nieuw Web subdomain vormt, zal het altijd aan een verslag van de NAAM richten.

1. Nadat de subdomeindelegatie is verzonden, wordt het subdomein weergegeven in de lijst met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Voordat u dat subdomein kunt gebruiken om webberichten te verzenden, moet u wachten tot de Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.

1. Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. U kunt deze functie gebruiken om webkanaaloppervlakken te maken.

   Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.


<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->