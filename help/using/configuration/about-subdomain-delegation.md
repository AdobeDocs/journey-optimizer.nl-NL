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
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 24%

---

# Subdomein delegeren in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="De gedelegeerde subdomeinen worden hier weergegeven."
>abstract="Uw eerste subdomein delegeren. Nadat de delegatie is voltooid, worden PTR-records gemaakt en worden e-mailkanalen ingeschakeld."

Het creëren van subdomain voor e-mailcampagnes staat merken toe om verschillende types van verkeer (marketing versus collectief bijvoorbeeld) in specifieke IP groepen en met specifieke domeinen te isoleren, die het IP opwarmingsproces zullen versnellen en leveringscapaciteit over het algemeen zullen verbeteren.

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

De configuratie van subdomain staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Campaign te vormen.

De beschikbare opstellingsmethodes zijn als volgt.

### Subdomein volledig delegeren aan Adobe (aanbevolen) {#full-subdomain-delegation}

Met [!DNL Journey Optimizer] kunt u de subdomeinen volledig delegeren naar Adobe, rechtstreeks vanuit de productinterface. Door dit te doen, zal Adobe berichten als beheerde dienst kunnen leveren door alle aspecten van DNS te controleren en te handhaven die voor het leveren, het teruggeven en het volgen van e-mailcampagnes worden vereist.

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

## De configuratiemethoden vergelijken

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:

| Configuratiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign nodig zijn.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **methode CNAME** | Maak het subdomein en de naamruimterecord. Adobe verstrekt dan de records die in uw DNS servers moeten worden geplaatst en configureert de overeenkomstige waarden in de DNS-servers van Adobe Campaign.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |
| **Custom delegation method** |  Create the subdomain and namespace record - Adobe will then provide the records to be placed in your DNS servers. Upload the SSL Certificate obtained from the Certificate Authority and complete the Feedback Loop steps by verifying domain ownership and reporting email address.<br/><br/>In this setup, you have full responsibility for maintaining DNS. | Very high |-->

De extra informatie over domeinconfiguratie is beschikbaar in [ deze documentatie ](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=nl-NL){target="_blank"}.

Als u een vraag hebt over configuratiemethoden voor subdomeinen, kunt u contact opnemen met Adobe of contact opnemen met de klantenservice om advies in te winnen over de leveringsmogelijkheden.


