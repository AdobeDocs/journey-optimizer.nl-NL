---
solution: Journey Optimizer
product: journey optimizer
title: Een aangepast subdomein delegeren
description: Leer hoe u aangepaste subdomeinen kunt delegeren.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, delegatie, domein, DNS
hide: true
hidefromtoc: true
exl-id: 34af1329-f0c8-4fcd-a284-f8f4214611d4
source-git-commit: 64ff860167439e1b098918cd913f2361f7365a50
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---

# Een aangepast subdomein instellen {#delegate-custom-subdomain}

Als alternatief aan [ volledig gemachtigde ](about-subdomain-delegation.md#full-subdomain-delegation) en [ CNAME opstelling ](about-subdomain-delegation.md#cname-subdomain-delegation) methodes, staat de **delegatie van de Douane** methode u toe om de eigendom van uw subdomeinen binnen Journey Optimizer te nemen om volledige controle over de geproduceerde certificaten te hebben.

Als onderdeel van dit proces moet Adobe ervoor zorgen dat uw DNS dienovereenkomstig is geconfigureerd voor het leveren, renderen en bijhouden van berichten. Dit is waarom u [ het SSL certificaat ](#upload-ssl-certificate) moet uploaden dat van de Autoriteit van het Certificaat wordt verkregen en de [ stappen van de Lijn van de Terugkoppeling ](#feedback-loop-steps) door domeineigendom te verifiëren en e-mailadres te melden voltooit.

Volg onderstaande stappen om een aangepast subdomein in te stellen.

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** .

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteer in de sectie **[!UICONTROL Set up method]** de optie **[!UICONTROL Custom delegation]**.

   ![](assets/subdomain-method-custom.png){width=90%}

1. Geef de naam op van het subdomein dat u wilt delegeren.

   >[!CAUTION]
   >
   >U kunt niet hetzelfde verzendende domein gebruiken om berichten van [!DNL Adobe Journey Optimizer] en van een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] , te verzenden.

## De DNS-records maken {#create-dns-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_dns"
>title="De overeenkomende DNS-records genereren"
>abstract="Als u een aangepast subdomein wilt delegeren aan Adobe, moet u de informatie van de nameserver die in de interface van Journey Optimizer wordt weergegeven kopiëren en plakken in uw domein-ontvangende oplossing om de overeenkomende DNS-records te genereren."

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records, één voor één, of door een CSV-bestand te downloaden.

1. Navigeer naar de hostingoplossing voor uw domein om de overeenkomende DNS-records te genereren.

1. Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd.

1. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;.

   ![](assets/subdomain-custom-submit.png){width="75%"}

## Het SSL-certificaat uploaden {#upload-ssl-certificate}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom-ssl"
>title="Aanvraag voor certificaatondertekening genereren"
>abstract="Wanneer u een nieuw aangepast subdomein instelt, moet u de CSR (Certificate Signing Request) genereren, dit invullen en naar de Certificate Authority verzenden om het SSL-certificaat te verkrijgen dat u naar Journey Optimizer moet uploaden."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_key_length"
>title="xxx"
>abstract=""

1. Klik in de sectie **[!UICONTROL SSL Certificate]** op **[!UICONTROL Generate CSR]** .

   ![](assets/subdomain-custom-ssl-certificate.png){width="85%"}

   >[!NOTE]
   >
   >De vervaldatum van uw SSL-certificaat wordt weergegeven. Wanneer de datum is bereikt, moet u een nieuw certificaat uploaden.

1. Vul het formulier in dat de CSR (Certificate Signing Request) weergeeft en genereert.

   ![](assets/subdomain-custom-generate-csr.png){width="70%"}

   >[!NOTE]
   >
   >De sleutellengte kan alleen 2048 of 4096 bits zijn. Deze kan niet worden gewijzigd nadat het subdomein is verzonden.

1. Klik op **[!UICONTROL Download CSR]** en sla het formulier op uw lokale computer op. Verzend het naar de Autoriteit van het Certificaat om uw SSL certificaat te krijgen.

1. Nadat u het certificaat hebt opgehaald, klikt u op **[!UICONTROL Upload SSL certificate]** en uploadt u het naar [!DNL Journey Optimizer] in .pem-indeling.

## De stappen voor het herhalen van feedback voltooien {#feedback-loop-steps}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_feedback-loop"
>title="De stappen voor het herhalen van feedback voltooien"
>abstract="Ga naar Yahoo! De Hub van de afzender en vult het formulier in om domeineigendom te verifiëren. Voer het FBL-rapportadres hieronder in en gebruik de OTP die wordt ontvangen om het eigendom op de Yahoo te verifiëren! Afzender Hub."

1. Ga naar de [ Yahoo! De Hub van de afzender ](https://senders.yahooinc.com/) website en vult de vereiste vorm in om uw domeinbezit te verifiëren.

1. Yahoo verifieert de domeineigendom! De Hub van de afzender zal vereisen dat u een e-mailadres verstrekt. Voer het FBL-rapportadres in dat onder **[!UICONTROL Value]** wordt vermeld. Dit is een e-mailadres dat eigendom is van Adobe.

1. Als Yahoo! De Hub van de afzender produceert een Eenmalig Wachtwoord (OTP), zal het naar dit adres van Adobe worden verzonden.

1. Ga naar het Adobe Deliverability Team dat u dit OTP zal voorzien. <!--Specify how to reach out + any information that customer should share in the request to deliverability team to get access to the right OTP-->

   >[!CAUTION]
   >
   >OTP is geldig slechts voor 24 uren, zodat zorg u aan Adobe bereikt zodra OTP wordt geproduceerd. <!--TBC?-->
   >
   >Het OTP- verzoek kan slechts op weekdagen worden gemaakt. Er is geen ondersteuning voor weekends. <!--Add times + timezone-->

1. Ga OTP op Yahoo in! Afzender Hub.

1. Controleer of je alle stappen voor het herhalen van feedback hebt uitgevoerd.

1. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik heb voltooid...&quot;.

   ![](assets/subdomain-custom-feedback-loop.png){width="85%"}

1. Klik op **[!UICONTROL Continue]** en wacht tot Adobe controleert of de records zonder fouten op de hostoplossing zijn gegenereerd. Dit proces kan tot 2 minuten duren.

   >[!NOTE]
   >
   >Ontbrekende records (de records die nog niet op de hostingoplossing zijn gemaakt) worden weergegeven.

   Adobe genereert een SSL CDN URL-validatierecord. Kopieer deze validatierecord naar het hostplatform. Als u deze record op de hostingoplossing juist hebt gemaakt, schakelt u het selectievakje &quot;I confirm...&quot; in.

1. Klik op **[!UICONTROL Submit]** om de vereiste controles door Adobe uit te voeren. [Meer informatie](#submit-subdomain)


## Controlelijst voor problemen oplossen {#check-list}

Als de fouten terwijl het proberen om uw douanesubdomain voor te leggen voorkomen, voer de hieronder vermelde het oplossen van problemenacties uit.

* Controleer of alle DNS-records correct zijn doorgegeven met DNS-opzoekgereedschappen.

* Controleer of uw certificaat aan alle technische vereisten voldoet voordat u het uploadt.

* Controleer of het certificaat in de juiste indeling is geüpload.

