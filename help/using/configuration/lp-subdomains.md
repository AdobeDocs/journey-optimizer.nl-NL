---
title: Subdomeinen van bestemmingspagina configureren
description: Leer hoe u subdomeinen van landingspagina's configureert met Journey Optimizer
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Subdomeinen van bestemmingspagina configureren {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Een voorinstelling voor een openingspagina maken"
>abstract="Als u een voorinstelling voor een bestemmingspagina wilt maken, moet u ervoor zorgen dat u eerder ten minste één subdomein van de bestemmingspagina hebt geconfigureerd om te kiezen uit de lijst met subdomeinnamen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Voorinstellingen voor openingspagina&#39;s maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Een subdomein van een bestemmingspagina delegeren"
>abstract="U moet een subdomein configureren om te gebruiken voor uw bestemmingspagina&#39;s, aangezien u dit subdomein nodig hebt om een voorinstelling voor een bestemmingspagina te maken. U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd of een nieuw subdomein vormen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Voorinstellingen voor openingspagina&#39;s maken"

Om in staat te zijn [voorinstellingen voor openingspagina&#39;s maken](lp-presets.md), moet u de subdomeinen instellen die u voor de bestemmingspagina&#39;s wilt gebruiken.

U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of u kunt een ander subdomein vormen. Meer informatie over het delegeren van subdomeinen naar Adobe in [deze sectie](delegate-subdomain.md).

## Een bestaand subdomein gebruiken {#lp-use-existing-subdomain}

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

   U kunt niet meerdere gedelegeerde subdomeinen van hetzelfde bovenliggende domein gebruiken. Als &#39;marketing1.yourcompany.com&#39; bijvoorbeeld al is gedelegeerd aan Adobe voor uw bestemmingspagina&#39;s, kunt u &#39;marketing2.yourcompany.com&#39; niet gebruiken. Maar subdomeinen met meerdere niveaus die worden ondersteund voor bestemmingspagina&#39;s, kunt u doorgaan met het gebruik van een subdomein van &#39;marketing1.yourcompany.com&#39; (zoals &#39;email.marketing1.yourcompany.com&#39;) of een ander bovenliggende domein.

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

## Een nieuw subdomein configureren {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="De overeenkomende DNS-record genereren"
>abstract="Als u een nieuw subdomein van een bestemmingspagina wilt configureren, moet u de gegevens van de Adobe nameserver kopiëren die in de Journey Optimizer-interface worden weergegeven en deze plakken in uw domein-ontvangende oplossing om het overeenkomende DNS-record te genereren. Als de controles zijn voltooid, kan het subdomein worden gebruikt om voorinstellingen voor bestemmingspagina&#39;s te maken."

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

   >[!NOTE]
   >
   >Voor bestemmingspagina&#39;s worden subdomeinen met meerdere niveaus ondersteund. U kunt bijvoorbeeld &#39;email.marketing.yourcompany.com&#39; gebruiken.

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
