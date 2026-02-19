---
solution: Journey Optimizer
product: journey optimizer
title: Subdomain Delegation in  [!DNL Journey Optimizer]
description: Leer hoe u uw subdomeinen kunt delegeren
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, optimaliseren, delegeren
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 17%

---

# Subdomein delegeren in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="De gedelegeerde subdomeinen worden hier weergegeven."
>abstract="Uw eerste subdomein delegeren. Nadat de delegatie is voltooid, worden PTR-records gemaakt en worden e-mailkanalen ingeschakeld."

Door een subdomein voor uw e-mailreizen en -campagnes te maken, kunnen merken verschillende typen verkeer (marketing versus bedrijf bijvoorbeeld) isoleren in specifieke IP-pools en met specifieke domeinen, waardoor het opwarmingsproces van het IP-adres sneller wordt en de leveringsmogelijkheden in het algemeen worden verbeterd.

Als u een domein deelt en het wordt geblokkeerd of aan de lijst van gewezen personen toegevoegd, zou het uw collectieve postlevering kunnen beïnvloeden. Nochtans, zullen de kwesties van de reputatie of de blokken op een domein specifiek voor uw e-mailmarketing mededelingen enkel die stroom van e-mail beïnvloeden. Het gebruiken van uw hoofddomein als afzender of &quot;van&quot;adres voor veelvoudige poststromen kon e-mailauthentificatie ook breken, veroorzakend uw berichten om worden geblokkeerd of in de spamomslag worden geplaatst.

>[!CAUTION]
>
>U kunt niet hetzelfde verzendende domein gebruiken om berichten van [!DNL Adobe Journey Optimizer] en van een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] , te verzenden.

## Waarom instellen van subdomeinen? {#why-set-up-subdomains}

Een subdomein is een afdeling van uw domein dat kan worden gebruikt om uw merken, of diverse soorten verkeer - bijvoorbeeld transactionele berichten en marketing mededelingen te isoleren.

Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

Bij het implementeren van een oplossing zijn er vereisten voor naar buiten gerichte componenten: dit zijn onder andere het instellen van koppelingen en webpagina&#39;s die moeten worden bijgehouden, het weergeven van spiegelpagina&#39;s, enz.

Hoewel deze vereisten worden beheerd via componenten die door zowel Adobe als de klant worden gehost, bevatten deze URL&#39;s die door de ontvangers van de e-mails kunnen worden bekeken. Om te voorkomen dat URL&#39;s de onderliggende technische oplossing of hostingprovider aangeven, kunnen subdomeinen worden ingesteld om dit transparant te maken voor de ontvangers van de e-mails.

**Meer informatie**

* Leer hoe te [ uw subdomeinen ](delegate-subdomain.md) direct van de interface afvaardigen
* Leer hoe te [ om de verslagen van Google TXT ](google-txt.md) aan uw subdomeinen toe te voegen om de succesvolle levering van e-mails aan de adressen van Gmail te verzekeren
* Leer hoe te [ tot de PTR- verslagen ](ptr-records.md) toegang te hebben die voor uw subdomeinen worden geproduceerd, hen toestaat om door postservers te verzenden

## Methoden voor subdomeinconfiguratie {#subdomain-delegation-methods}

De configuratie van subdomain staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Journey Optimizer te vormen.

De beschikbare opstellingsmethodes zijn als volgt.

### Subdomein volledig delegeren aan Adobe (aanbevolen) {#full-subdomain-delegation}

Met [!DNL Journey Optimizer] kunt u de subdomeinen volledig delegeren naar Adobe, rechtstreeks vanuit de productinterface. Door dit te doen, zal Adobe berichten als beheerde dienst kunnen leveren door alle aspecten van DNS te controleren en te handhaven die voor levering, het teruggeven en het volgen worden vereist.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

U kunt op Adobe vertrouwen om de DNS-infrastructuur te onderhouden die nodig is om te voldoen aan de industriestandaard vereisten voor de levering van uw e-mailverzendende domeinen voor marketingdoeleinden, terwijl u DNS voor uw interne e-maildomeinen blijft onderhouden en beheren.

>[!IMPORTANT]
>
>De volledige subdomeindelegatie heeft de voorkeur.

Leer hoe te om een subdomain volledig aan Adobe in [ te delegeren deze sectie ](delegate-subdomain.md#set-up-subdomain).

### Een subdomein instellen met CNAME&#39;s {#cname-subdomain-setup}

Als u domein-specifieke beperkingsbeleid hebt en u Adobe slechts gedeeltelijke controle over DNS wilt hebben, kunt u verkiezen om alle DNS-gerelateerde activiteiten op uw kant uit te voeren.

Met de CNAME-subdomeinset kunt u een subdomein maken en CNAME&#39;s gebruiken om te verwijzen naar Adobe-specifieke records. Met behulp van deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS om een omgeving in te stellen voor het verzenden, renderen en volgen van e-mails.

>[!CAUTION]
>
>De methode CNAME wordt geadviseerd als het beleid van uw organisatie de volledige subdomain delegatiemethode beperkt. Deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren.
>
>Adobe zal niet in het veranderen van, het handhaven van of het beheren van DNS voor subdomain kunnen bijwonen die door de methode CNAME wordt gevormd.

Leer hoe te om subdomain tot stand te brengen gebruikend CNAMEs om aan Adobe-specifieke verslagen in [ te richten deze sectie ](delegate-subdomain.md#cname-subdomain-setup).

### Een aangepast subdomein gebruiken {#custom-subdomain-delegation}

De methode van de douanedelegatie laat u toe om volledig het controleren en het handhaven van alle aspecten van DNS te bezitten die voor het leveren, het teruggeven en het volgen van berichten worden vereist.

In dit geval hebt u volledig eigenaar en beheert u onze eigen subdomeinen en hebt u volledige controle over de certificaten die als onderdeel van dit proces worden gegenereerd.

Leer hoe te [ opstelling een douane subdomain ](delegate-custom-subdomain.md). Als uw subdomain momenteel CNAME gebruikt, kunt u [ van CNAME aan douanedelegatie ](custom-subdomain-migration.md) ook migreren.

## De configuratiemethoden vergelijken

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:
<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Journey Optimizer.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Journey Optimizer DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |-->


| Configuratiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Journey Optimizer zijn vereist.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **methode CNAME** | Maak het subdomein en de naamruimterecord. Adobe zal dan de verslagen verstrekken die in uw DNS servers moeten worden geplaatst en zal de overeenkomstige waarden in de servers van Adobe Journey Optimizer DNS vormen.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |
| **de delegatiemethode van de Douane** | Creeer subdomain en namespace verslag - Adobe zal dan de verslagen verstrekken die in uw DNS servers moeten worden geplaatst. Upload het SSL-certificaat dat u van de Certificate Authority (certificeringsinstantie) hebt gekregen en voltooi de stappen voor het herhalen van feedback door de eigendom van het domein te controleren en het e-mailadres te melden.<br/><br/> In deze opstelling, hebt u volledige verantwoordelijkheid voor het handhaven van DNS. | Zeer hoog |

De extra informatie over domeinconfiguratie is beschikbaar in [ deze documentatie ](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html){target="_blank"}.

Als u een vraag hebt over configuratiemethoden voor subdomeinen, kunt u contact opnemen met Adobe of contact opnemen met de klantenservice om advies in te winnen over de leveringsmogelijkheden.


