---
solution: Journey Optimizer
product: journey optimizer
title: Subdomeinen configureren voor tekstberichten (SMS/MMS)
description: Leer hoe u SMS-subdomeinen configureert met Journey Optimizer
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: SMS, subdomeinen, configuratie
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: 227cdb77b0db40c59fa089789c444c2364fd062e
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# SMS-subdomeinen configureren {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Een SMS/MMS-subdomein delegeren"
>abstract="Stel uw subdomein in voor tekstberichten (SMS/MMS). U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of een nieuw subdomein vormen."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Een SMS/MMS-subdomein delegeren"
>abstract="U moet een subdomein vormen voor uw tekstberichten te gebruiken, aangezien u dit subdomein nodig hebt om een oppervlakte van SMS tot stand te brengen. U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of een nieuw subdomein vormen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="SMS-oppervlakken maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Een SMS/MMS-subdomein selecteren"
>abstract="Om een oppervlakte van SMS te kunnen tot stand brengen, zorg ervoor u eerder minstens één subdomain van SMS om van de Subdomain naamlijst hebt gevormd te plukken."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="SMS-oppervlakken maken"

Als u URL&#39;s die aan uw SMS/MMS-berichten zijn toegevoegd, wilt verkorten, moet u het subdomein instellen dat u selecteert wanneer [het creëren van een oppervlakte van SMS](sms-configuration.md#message-preset-sms).

U kunt een subdomein gebruiken dat reeds aan Adobe wordt gedelegeerd, of u kunt een ander subdomein vormen. Meer informatie over het delegeren van subdomeinen naar Adobe in [deze sectie](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>* De subdomeinconfiguratie van SMS wordt gedeeld tussen alle milieu&#39;s. Daarom heeft elke wijziging van een subdomein van SMS ook invloed op andere productiesandboxen.
>
>* Om tot subdomeinen van SMS toegang te hebben en uit te geven, moet u hebben **[!UICONTROL Manage SMS Subdomains]** toestemming voor de productiesandbox. Meer informatie over machtigingen in [deze sectie](../administration/high-low-permissions.md).
>

## Een bestaand subdomein gebruiken {#sms-use-existing-subdomain}

Volg onderstaande stappen om een subdomein te gebruiken dat al is gedelegeerd aan Adobe.

1. Bladeren naar de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteert u **[!UICONTROL SMS configuration]** > **[!UICONTROL SMS subdomains]**.

   ![](assets/sms_access-subdomains.png)

1. Klik op **[!UICONTROL Set up subdomain]**.

   ![](assets/sms_set-up-subdomain.png)

1. Selecteren **[!UICONTROL Use delegated subdomain]** van de **[!UICONTROL Configuration type]** sectie.

   ![](assets/sms_use-delegated-subdomain.png)

1. Voer het voorvoegsel in dat in je SMS-URL wordt weergegeven.

   >[!NOTE]
   >
   >Alleen alfanumerieke tekens en afbreekstreepjes zijn toegestaan.

1. Selecteer een gedelegeerd subdomein in de lijst.

   >[!NOTE]
   >
   >U kunt geen subdomein selecteren dat al als subdomein van SMS wordt gebruikt.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Als u een domein selecteert dat aan Adobe werd gedelegeerd gebruikend [CNAME, methode](../configuration/delegate-subdomain.md#cname-subdomain-delegation), moet u het DNS-record op uw hostingplatform maken. Om het DNS verslag te produceren, is het proces het zelfde als wanneer u een nieuw subdomain van SMS vormt. Meer informatie over [deze sectie](#sms-configure-new-subdomain).

1. Klik op **[!UICONTROL Submit]**.

1. Na verzending wordt het subdomein in de lijst weergegeven met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Voordat u dat subdomein kunt gebruiken om berichten te verzenden, moet u wachten tot de Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om de kanaaloppervlakten van SMS te creëren.

## Een nieuw subdomein configureren {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="De overeenkomende DNS-record genereren"
>abstract="Om een nieuw subdomain van SMS te vormen, moet u de Adobe nameserver informatie kopiëren die in de interface van Journey Optimizer wordt getoond en het kleven in uw domein-ontvangende oplossing om het passende DNS verslag te produceren. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om de oppervlakken van SMS tot stand te brengen."

Volg onderstaande stappen om een nieuw subdomein te configureren.

1. Bladeren naar de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL SMS configuration]** > **[!UICONTROL SMS subdomains]**.

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteren **[!UICONTROL Add your own domain]** van de **[!UICONTROL Configuration type]** sectie.

   ![](assets/sms_add-your-own-subdomain.png)

1. Geef het subdomein op dat u wilt delegeren.

   >[!CAUTION]
   >
   >* U kunt geen bestaand subdomein van SMS gebruiken.
   >
   >* Hoofdletters zijn niet toegestaan in subdomeinen.

   Het delegeren van een ongeldig subdomein aan Adobe wordt niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   >[!NOTE]
   >
   >Subdomeinen op meerdere niveaus (van hetzelfde bovenliggende domein) worden ondersteund. U kunt bijvoorbeeld &#39;sms.marketing.yourcompany.com&#39; gebruiken.

1. Het verslag dat in uw DNS serververtoningen moet worden geplaatst. Kopieer deze record of download een CSV-bestand en navigeer vervolgens naar de oplossing voor domeinhosting om de overeenkomende DNS-record te genereren.

1. Zorg ervoor dat DNS het verslag in uw domein-ontvangende oplossing is geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;, dan klik **[!UICONTROL Submit]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Wanneer u een nieuw subdomain van SMS vormt, zal het altijd aan een verslag van de NAAM richten.

1. Nadat de subdomeindelegatie is verzonden, wordt het subdomein weergegeven in de lijst met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

Voordat u een subdomein kunt gebruiken om SMS-berichten te verzenden, moet u wachten totdat de Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.<!--Learn more in [this section](#subdomain-validation).--> Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om de kanaaloppervlakten van SMS te creëren.

Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.
