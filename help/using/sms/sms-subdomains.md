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
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '969'
ht-degree: 0%

---

# SMS-subdomeinen configureren {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Een SMS/MMS-subdomein delegeren"
>abstract="Stel uw subdomein in voor tekstberichten (SMS/MMS). U kunt een subdomein gebruiken dat al aan Adobe is gedelegeerd, of een nieuw subdomein vormen."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Een SMS/MMS-subdomein delegeren"
>abstract="U moet een subdomein vormen voor uw tekstberichten te gebruiken, aangezien u dit subdomein nodig hebt om een configuratie van SMS tot stand te brengen. U kunt een subdomein gebruiken dat al aan Adobe is gedelegeerd, of een nieuw subdomein vormen."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Een SMS-configuratie maken"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Een SMS/MMS-subdomein selecteren"
>abstract="Om een configuratie van SMS te kunnen tot stand brengen, zorg ervoor u eerder minstens één subdomain van SMS om van de lijst Subdomain te kiezen hebt gevormd."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Een SMS-configuratie maken"

## Aan de slag met SMS-subdomeinen {#gs-sms-mms-subdomains}

Om URLs te kunnen verkorten die aan uw SMS/MMS- berichten wordt toegevoegd, moet u opstelling subdomain u wanneer [&#x200B; creërend een configuratie van SMS &#x200B;](sms-configuration.md#message-preset-sms) selecteren.

U kunt een subdomein gebruiken dat al is gedelegeerd aan Adobe, of een ander subdomein configureren. Leer meer over het delegeren van subdomeinen aan Adobe in [&#x200B; deze sectie &#x200B;](../configuration/delegate-subdomain.md).

De subdomeinconfiguratie van SMS wordt **gedeeld tussen alle milieu&#39;s**. Daarom heeft elke wijziging van een subdomein van SMS ook invloed op andere productiesandboxen.

Als u SMS-subdomeinen wilt openen en bewerken, moet u over de machtiging **[!UICONTROL Manage SMS Subdomains]** in de productiesandbox beschikken. Leer meer over toestemmingen in [&#x200B; deze sectie &#x200B;](../administration/high-low-permissions.md).

## Een bestaand subdomein gebruiken {#sms-use-existing-subdomain}

Voer de onderstaande stappen uit als u een subdomein wilt gebruiken dat al is gedelegeerd aan Adobe.

1. Blader naar het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer **[!UICONTROL SMS settings]** > **[!UICONTROL SMS subdomains]** .

1. Klik op **[!UICONTROL Set up subdomain]**.

   ![](assets/sms_set-up-subdomain.png)

1. Selecteer **[!UICONTROL Use delegated subdomain]** in de sectie **[!UICONTROL Configuration type]** .

   ![](assets/sms_use-delegated-subdomain.png)

1. Voer het voorvoegsel in dat in je SMS-URL wordt weergegeven.

   Alleen alfanumerieke tekens en afbreekstreepjes zijn toegestaan.

   >[!CAUTION]
   >
   >Gebruik `cdn` of `data` voorvoegsels niet omdat deze zijn gereserveerd voor intern gebruik. Andere beperkte of gereserveerde voorvoegsels zoals `dmarc` of `spf` moeten ook worden vermeden.

1. Selecteer een gedelegeerd subdomein in de lijst.

   U kunt geen subdomein selecteren dat al als subdomein van SMS wordt gebruikt.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Als u een domein selecteert dat aan Adobe gebruikend de [&#x200B; methode van de NAAM &#x200B;](../configuration/delegate-subdomain.md#cname-subdomain-setup) werd afgevaardigd, moet u het DNS verslag op uw het ontvangen platform tot stand brengen. Om het DNS verslag te produceren, is het proces het zelfde als wanneer u een nieuw subdomain van SMS vormt. Leer hoe in [&#x200B; deze sectie &#x200B;](#sms-configure-new-subdomain).

1. Klik op **[!UICONTROL Submit]**.

1. Na verzending wordt het subdomein in de lijst weergegeven met de status **[!UICONTROL Processing]** . Voor meer op de statussen van subdomeinen, verwijs naar [&#x200B; deze sectie &#x200B;](../configuration/delegate-subdomain.md#access-delegated-subdomains).<!--Same statuses?-->

   Alvorens dat subdomain te kunnen gebruiken om berichten te verzenden, moet u wachten tot Adobe de vereiste controles uitvoert, die **tot 4 uren** kan nemen.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Zodra de controles succesvol zijn, krijgt subdomain de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om de kanaalconfiguraties van SMS tot stand te brengen.

## Een nieuw subdomein configureren {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="De overeenkomende DNS-record genereren"
>abstract="Om een nieuw subdomein van SMS te vormen, moet u de Adobe nameserver informatie kopiëren die in de interface van Journey Optimizer wordt getoond en het kleven in uw domein-ontvangende oplossing om het passende DNS verslag te produceren. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om de configuraties van SMS tot stand te brengen."

Volg onderstaande stappen om een nieuw subdomein te configureren.

1. Blader naar het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** en selecteer vervolgens **[!UICONTROL SMS settings]** > **[!UICONTROL SMS subdomains]** .

1. Klik op **[!UICONTROL Set up subdomain]**.

   ![](assets/sms_set-up-subdomain.png)

1. Selecteer **[!UICONTROL Add your own domain]** in de sectie **[!UICONTROL Configuration type]** .

   ![](assets/sms_add-your-own-subdomain.png)

1. Geef het subdomein op dat u wilt delegeren.

   >[!CAUTION]
   >
   >* U kunt geen bestaand subdomein van SMS gebruiken.
   >
   >* Hoofdletters zijn niet toegestaan in subdomeinen.

   Het delegeren van een ongeldig subdomein naar Adobe is niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   Subdomeinen op meerdere niveaus (van hetzelfde bovenliggende domein) worden ondersteund. U kunt bijvoorbeeld &#39;sms.marketing.yourcompany.com&#39; gebruiken.

1. Het verslag dat in uw DNS serververtoningen moet worden geplaatst. Kopieer deze record of download een CSV-bestand en navigeer vervolgens naar de oplossing voor domeinhosting om de overeenkomende DNS-record te genereren.

1. Zorg ervoor dat DNS het verslag in uw domein-ontvangende oplossing is geproduceerd. Als alles correct is geconfigureerd, schakelt u het selectievakje &quot;I confirm...&quot; in en klikt u op **[!UICONTROL Submit]** .

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   Wanneer u een nieuw subdomain van SMS vormt, richt het altijd aan een verslag CNAME.

1. Nadat de subdomeindelegatie is verzonden, wordt het subdomein in de lijst weergegeven met de status **[!UICONTROL Processing]** . Voor meer op de statussen van subdomeinen, verwijs naar [&#x200B; deze sectie &#x200B;](../configuration/delegate-subdomain.md#access-delegated-subdomains).<!--Same statuses?-->

Voordat u SMS-berichten verzendt met een subdomein, moet u wachten tot Adobe de vereiste controles uitvoert. Dit kan maximaal 4 uur in beslag nemen.<!--Learn more in [this section](#subdomain-validation).--> Zodra de controles succesvol zijn, krijgt het subdomein de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om de kanaalconfiguraties van SMS tot stand te brengen.

Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u geen validatierecord maakt voor de hostoplossing.

## Guardrails {#guardrails}

De gebruikersinterface van [!DNL Journey Optimizer] ondersteunt momenteel niet het verwijderen of verwijderen van SMS-subdomeinen nadat deze zijn ingesteld.

Wanneer u echter functies in [!DNL Journey Optimizer] test, kan het nodig zijn een SMS-subdomein te maken. Zodra het testen volledig is, kan dit tot onoverzichtelijke milieu&#39;s met onnodige configuraties leiden aangezien UI niet toestaat voor het verwijderen of het losmaken van subdomeinen van SMS.

Hier volgen enkele aanbevolen stappen en overwegingen:

<!--As an alternative action, create a new SMS subdomain for future use cases and avoid using the existing one if it is no longer needed.-->

* U kunt het beste een testomgeving onderhouden door alleen de benodigde componenten en configuraties te maken.
* Neem in situaties met een impact op het bedrijf contact op met uw Adobe-vertegenwoordiger die u kan helpen bij het verwijderen/verwijderen van het SMS-subdomein. [Meer informatie](#undelegate-subdomain)
* Als verdere hulp wordt vereist, contacteer Adobe voor begeleiding op effectief het beheren van uw geval.

## Een subdomein delegeren ongedaan maken {#undelegate-subdomain}

Als u wenst om subdomain van SMS te delegeren, bereik aan uw vertegenwoordiger van Adobe met subdomain u wilt loskoppelen.

Als subdomain van SMS naar een CNAME-record wijst, kunt u het CNAME DNS-record verwijderen dat u voor het SMS-subdomein hebt gemaakt van uw hostoplossing (maar niet het oorspronkelijke e-mailsubdomein als dat er is).

>[!NOTE]
>
>Een subdomain van SMS kan aan een CNAME- verslag richten omdat het of een [&#x200B; bestaand subdomain &#x200B;](#sms-use-existing-subdomain) aan Adobe werd gedelegeerd gebruikend de [&#x200B; methode CNAME &#x200B;](../configuration/delegate-subdomain.md#cname-subdomain-setup), of a [&#x200B; nieuw subdomain van SMS &#x200B;](#sms-configure-new-subdomain) dat u vormde.

Nadat uw verzoek door Adobe wordt behandeld, wordt het niet-gedelegeerde domein niet meer getoond op de pagina van de subdomeininventaris.
