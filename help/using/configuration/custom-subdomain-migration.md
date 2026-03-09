---
solution: Journey Optimizer
product: journey optimizer
title: Een e-mailsubdomein migreren van CNAME naar aangepaste delegatie
description: Leer hoe u een subdomein van een e-mail- of landingspagina van CNAME-delegatie naar een aangepaste delegatie in Journey Optimizer migreert.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: subdomein, delegatie, migratie, CNAME, aangepaste delegatie
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: f74139cf-640f-4b7b-a0b1-6eae9c75e7e4
source-git-commit: 47c04f6243057ac20fd28a228e4fefb760d7fe26
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# Een e-mailsubdomein migreren van CNAME naar aangepaste delegatie {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>Deze mogelijkheid is beschikbaar in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Als uw subdomain momenteel opstelling met [ CNAMEs ](about-subdomain-delegation.md#cname-subdomain-setup) is, kunt u het aan de **[!UICONTROL Custom delegation]** methode migreren om het veiligheidsbeleid van uw bedrijf te ontmoeten. Dit geeft u volledige eigendom en controle over uw subdomeinen en certificaten binnen [!DNL Journey Optimizer]. [ leer meer op douanesubdomeinen ](delegate-custom-subdomain.md)

In het kader van dit proces moet u:

* [ Schrap de bestaande DNS verslagen ](#delete-dns) van uw het ontvangen oplossing
* [ upload het SSL certificaat ](#upload-ssl-certificate) dat van de Instantie van het Certificaat wordt verkregen
* Voltooi de [ stappen van de Lijn van de Terugkoppeling ](#feedback-loop) door domeineigendom te verifiëren en e-mailadres te melden
* [ creeer een nieuwe reeks DNS verslagen ](#create-dns-records) die door Adobe in uw het ontvangen platform worden geproduceerd

Volg onderstaande stappen om uw subdomein te migreren.

## Voordat u begint {#before-you-begin}

Lees de belangrijke informatie hieronder voordat u het migratieproces start.

>[!IMPORTANT]
>
>U kunt een subdomeinopstelling met de [ methode van de NAAM ](delegate-subdomain.md#cname-subdomain-setup) slechts migreren.

* Zorg ervoor dat de **de delegatiemethode van de Douane** voor uw organisatie wordt toegelaten (dit vermogen is momenteel in Beperkte Beschikbaarheid-contact uw vertegenwoordiger van Adobe om toegang te krijgen). [Meer informatie](delegate-custom-subdomain.md)
* Zorg ervoor dat geen actieve kanaalconfiguraties dit subdomein gebruiken. Het migratieproces zal hun functionaliteit onderbreken.

  >[!NOTE]
  >
  >Als u een kanaalconfiguratie deactiveert voordat u de migratie start, kunt u deze weer terugzetten in de actieve status nadat de migratieworkflow is voltooid.

* Zorg ervoor dat geen actieve campagnes of reizen een kanaalconfiguratie gebruiken verbonden aan dit subdomein aangezien dit leveringsverstoring kan veroorzaken.
* Houd er rekening mee dat de uitvaltijd begint zodra u de migratiestroom betreedt. Het subdomein gaat tijdens het proces naar **[!UICONTROL Draft]** en is niet beschikbaar tot de installatie is voltooid.
* Derhalve wordt het geadviseerd om **de pre-migratiestappen uit te voeren alvorens het migratieproces** te beginnen - om uw SSL certificaat klaar te hebben en onderbreking te verminderen. [Meer informatie](#start-migration)

## De migratie starten {#start-migration}

Voer de onderstaande stappen uit om een bepaald subdomein te migreren.

1. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** .

1. Selecteer een subdomeinset met CNAME&#39;s en open deze.

1. U kunt de sectie **[!UICONTROL Pre-migration CSR Generation]** gebruiken om de CSR te genereren voor het verzenden van de CSR naar de Certificate Authority (certificeringsinstantie) en het SSL-certificaat gereed te hebben wanneer het migratieproces start. [ leer hoe ](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >De stappen vóór de migratie zijn in dit stadium optioneel, maar sterk aanbevolen. Voltooiend hen **alvorens** de aanvang van de migratie vermindert onderbreking en helpt een vlotte overgang verzekeren.

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. Selecteer **[!UICONTROL Migrate now]** in de toegewezen sectie.

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. Herzie de [ getoonde informatie ](#before-you-begin).

   >[!WARNING]
   >
   >De downtime begint zodra u de migratiestroom betreedt, zorg ervoor het uw actieve campagnes en reizen niet beïnvloedt.

1. Klik op **[!UICONTROL Yes]**. Het subdomein krijgt de status **[!UICONTROL Draft]** en is pas beschikbaar als de installatie is voltooid.

## CSR genereren en naar de certificeringsinstantie sturen {#send-csr-to-ca}

Om de migratie te voltooien, hebt u een SSL-certificaat nodig dat door een Certificate Authority (CA) is uitgegeven. Als u dit SSL-certificaat wilt ontvangen, moet u eerst een CSR (Certificate Signing Request) genereren en deze naar de CA verzenden.

Of u al met het migratieproces bent begonnen of niet, volg de onderstaande stappen om uw nieuwe CSR te produceren en te verzenden.

1. Klik op **[!UICONTROL Regenerate CSR]**.

1. Vul het formulier in waarin de CSR (Certificate Signing Request) wordt weergegeven en gegenereerd.

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >De sleutellengte kan alleen 2048 of 4096 bits zijn. Deze kan niet worden gewijzigd nadat het subdomein is verzonden.

1. Klik op **[!UICONTROL Download CSR]** en sla het formulier op uw lokale computer op.

1. Verzend het naar de Instantie van het Certificaat (CA) om uw SSL certificaat te krijgen. Alvorens dit CSR aan uw CA voor ondertekening voor te leggen, zijn er een paar belangrijke punten om te overwegen:

   * De gedownloade CSR van stap 3 is slechts voor data.subdomain.com.

   * Het certificaat moet echter zowel data.subdomain.com als cdn.subdomain.com bestrijken als onderwerpalternatieven (SAN) binnen één certificaat. Als u bijvoorbeeld example.adobe.com delegeert, komt data.subdomain.com overeen met data.example.adobe.com en cdn.subdomain.com met cdn.example.adobe.com.

   * Zowel de subdomeinen Data (data.example.adobe.com) als CDN (cdn.example.adobe.com) moeten als peer ingangen in het zelfde certificaat worden toegevoegd. Er mogen geen aanvullende subdomeinen aan dit certificaat worden toegevoegd.

   * De meeste CA&#39;s staan u toe om extra San&#39;s (zoals CDN subdomain) tijdens het ondertekeningsproces toe te voegen

      * Via het CA-portaal (aanbevolen, indien beschikbaar), of
      * Door dit handmatig bij hun ondersteuningsteam aan te vragen als de poortoptie niet beschikbaar is.

   * Zodra ondertekend, zal CA één enkel certificaat uitgeven dat zowel het domein van Gegevens als subdomain CDN behandelt.

## Bestaande DNS-records verwijderen {#delete-dns}

Na het beginnen van het migratieproces, moet u de bestaande DNS verslagen van uw het ontvangen oplossing schrappen. Voer de onderstaande stappen uit.

1. De lijst van verslagen momenteel gevormd in uw DNS serververtoningen.

1. Navigeer naar uw domein die oplossing ontvangen en schrap de bestaande ingangen van CNAME van uw DNS het ontvangen.

1. Controleer of alle DNS-records zijn verwijderd. Als u klaar bent, schakelt u het vakje &quot;Ik bevestig dat ik de vereiste records van de hostsite heb verwijderd&quot; in.

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## Het SSL-certificaat uploaden {#upload-ssl-certificate}

In de sectie **[!UICONTROL SSL Certificate]** moet u een nieuw SSL-certificaat uploaden naar [!DNL Journey Optimizer] .

Controleer daarvoor het volgende:

* Als u reeds uw CSR naar de Instantie van het Certificaat als deel van [ pre-migratiestappen ](#start-migration) hebt verzonden, zorg ervoor u uw SSL certificaat hebt ontvangen.

* Als u dit nog niet hebt gedaan, volg de stappen aan [ produceren, downloaden en verzenden CSR ](#send-csr-to-ca).

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. Klik op **[!UICONTROL Upload certificate]** als u het SSL-certificaat hebt opgehaald.

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. Upload het SSL-certificaat naar [!DNL Journey Optimizer] in .pem-indeling met de volledige certificaatketen. Hier volgt een voorbeeld van een .pem-bestandsindeling:

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```

1. Schakel het selectievakje &quot;Ik bevestig dat ik het SSL-certificaat heb geüpload&quot; in.

## Feedbacklus voltooien {#feedback-loop}

Voer vervolgens de stappen van de feedbacklus uit om het eigendom van het domein te verifiëren en het e-mailadres te melden.

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

Het proces is hetzelfde als wanneer u een nieuw aangepast subdomein instelt. Volg de stappen die op de [ opstelling worden gedetailleerd een douane subdomain ](delegate-custom-subdomain.md#feedback-loop-steps) pagina.


## Een nieuwe set DNS-records maken {#create-dns-records}

Als u het migratieproces wilt voltooien, maakt u een nieuwe set DNS-records die door Adobe in uw hostplatform worden gegenereerd.

1. Nadat u de stappen van de feedbacklus hebt uitgevoerd, klikt u op de knop **[!UICONTROL Continue]** rechtsboven in het scherm.

   Deze stap controleert of de vorige records zijn verwijderd en of het SSL-certificaat correct is geüpload. Als om het even welke fouten voorkomen, verwijs naar de [ controlelijst van het oplossen van problemen ](#troubleshooting).

1. Als alle validaties zijn gelukt, wordt de sectie **[!UICONTROL Records to be created]** weergegeven.

   ![](assets/subdomain-migrate-records-to-create.png){width="75%"}

1. Maak alle vereiste records in uw hostingplatform.

1. Klik op **[!UICONTROL Submit]** als alle records zijn gemaakt.

   >[!NOTE]
   >
   >Als niet alle vermelde records zijn gemaakt, wordt een fout weergegeven. Zorg ervoor dat u alle vereiste records maakt.

Na het verzenden moet u wachten tot Adobe de vereiste controles uitvoert. Dit kan maximaal 3 uur in beslag nemen. [Meer informatie](delegate-subdomain.md#submit-subdomain)

Zodra subdomain opnieuw actief is, zijn geen veranderingen nodig aan bestaande kanaalconfiguraties die het gebruiken-zij blijven werken zoals vroeger.

## Checklist voor probleemoplossing {#troubleshooting}

Als de fouten terwijl het proberen om uw douanesubdomain voor te leggen voorkomen, voer de hieronder vermelde het oplossen van problemenacties uit.

* _Middel kon niet worden bevestigd. De DNS bestaat nog en moet worden geschrapt._ — Verwijder alle records uit de hostoplossing. [ leer hoe ](#delete-dns)
* _Middel kon niet worden bevestigd. Upload uw SSL-certificaat en probeer het opnieuw._ — Het SSL-certificaat is niet geüpload. Zorg ervoor dat u het bestand uploadt. [ leer hoe ](#upload-ssl-certificate)
* _het certificaat bevat onverwachte domeinen in zijn Onderwerp Alternatieve Namen (San)._ — Zorg ervoor dat u het juiste SSL-certificaat uploadt. [ leer hoe ](#upload-ssl-certificate)
* _het certificaat mist de volgende vereiste domeinen in zijn Onderwerp Alternatieve Namen (San)._ — Zorg ervoor dat u het juiste SSL-certificaat uploadt. [ leer hoe ](#upload-ssl-certificate)

**zie ook**

* [Een aangepast subdomein instellen](delegate-custom-subdomain.md)
* [Methoden voor subdomeindelegatie](about-subdomain-delegation.md#subdomain-delegation-methods)
