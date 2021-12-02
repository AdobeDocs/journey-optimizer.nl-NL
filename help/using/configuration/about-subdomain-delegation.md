---
title: Subdomeinen delegeren
description: Leer hoe u uw subdomeinen kunt delegeren
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 203f8545200d4a6c20a748807e20ba7aba1ab5f3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 36%

---

# Subdomeindelegatie in [!DNL Journey Optimizer]

Het creëren van subdomain voor e-mailcampagnes staat merken toe om verschillende types van verkeer (marketing versus collectief bijvoorbeeld) in specifieke IP groepen en met specifieke domeinen te isoleren, die het IP opwarmingsproces zullen versnellen en leveringscapaciteit over het algemeen zullen verbeteren. Als u een domein deelt en het wordt geblokkeerd of aan de lijst van gewezen personen toegevoegd, zou het uw collectieve postlevering kunnen beïnvloeden. Nochtans, zullen de kwesties van de reputatie of de blokken op een domein specifiek voor uw e-mailmarketing mededelingen enkel die stroom van e-mail beïnvloeden. Als u uw hoofddomein als afzender of het adres &#39;Van&#39; voor meerdere e-mailstreams gebruikt, kan de e-mailverificatie ook worden verbroken, waardoor uw berichten worden geblokkeerd of in de spammap worden geplaatst.

## Waarom zou ik subdomeinen instellen? {#why-setting-up-subdomains}

Een subdomein is een afdeling van uw domein dat kan worden gebruikt om uw merken, of diverse soorten verkeer - bijvoorbeeld transactionele berichten en marketing mededelingen te isoleren.

Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

Bij het implementeren van een oplossing gelden er vereisten voor naar buiten gerichte onderdelen: het gaat hierbij onder andere om het instellen van koppelingen en webpagina&#39;s die moeten worden bijgehouden, het weergeven van spiegelpagina&#39;s, enz.

Hoewel deze vereisten worden beheerd via componenten die door zowel Adobe als de klant worden gehost, bevatten ze URL&#39;s die door de ontvangers van de e-mails kunnen worden bekeken. Om te voorkomen dat URL&#39;s de onderliggende technische oplossing of hostingprovider aangeven, kunnen subdomeinen worden ingesteld om dit transparant te maken voor de ontvangers van de e-mails.

**Meer informatie**

* Leer hoe u [delegeren van subdomeinen](delegate-subdomain.md) rechtstreeks vanuit de interface
* Leer hoe u [Google TXT-records toevoegen](google-txt.md) naar uw subdomeinen om ervoor te zorgen dat e-mails naar Gmail-adressen succesvol worden verzonden
* Leer hoe u [toegang tot de PTR-records](ptr-records.md) gegenereerd voor uw subdomeinen, zodat deze kunnen worden geverifieerd door e-mailservers te verzenden

## Methoden voor subdomeinconfiguratie {#subdomain-delegation-methods}

De configuratie van subdomain staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Campaign te vormen. Beschikbare instelmethoden zijn:

* **Volledige subdomeindelegatie aan Adobe** (aanbevolen): Het subdomein wordt volledig gedelegeerd aan Adobe. Adobe kan alle aspecten van DNS beheren en handhaven die voor het leveren, het teruggeven en het volgen van berichten worden vereist. [Meer informatie over volledige subdomeindelegatie](delegate-subdomain.md#full-subdomain-delegation)

* **Gebruik van CNAME&#39;s**: Creeer subdomain en gebruik CNAMEs om aan Adobe-specifieke verslagen te richten. Gebruikend deze opstelling, zowel u als Adobe ashare verantwoordelijkheid voor het handhaven van DNS. [Meer informatie over CNAME-subdomeindelegatie](delegate-subdomain.md#cname-subdomain-delegation)

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:

| Configuratiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign nodig zijn.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **CNAME, aangepaste methode** | Maak het subdomein en de naamruimterecord. Adobe verstrekt dan de records die in uw DNS servers moeten worden geplaatst en configureert de overeenkomstige waarden in de DNS-servers van Adobe Campaign.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

Aanvullende informatie over domeinconfiguratie is beschikbaar in [deze documentatie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Als u om het even welke vraag betreffende de methodes van de subdomeinconfiguratie hebt, bereik uit aan Adobe, of uiteindelijk contacteer de Zorg van de Klant om het raadplegen van de Leverbaarheid te verzoeken.
