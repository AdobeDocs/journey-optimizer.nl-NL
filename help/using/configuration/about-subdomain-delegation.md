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
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 23%

---

# Subdomein delegeren in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="De gedelegeerde subdomeinen worden hier weergegeven."
>abstract="Uw eerste subdomein delegeren. Nadat de delegatie is voltooid, worden PTR-records gemaakt en worden e-mailkanalen ingeschakeld."

Het creëren van subdomain voor e-mailcampagnes staat merken toe om verschillende types van verkeer (marketing versus collectief bijvoorbeeld) in specifieke IP groepen en met specifieke domeinen te isoleren, die het IP opwarmingsproces zullen versnellen en leveringscapaciteit over het algemeen zullen verbeteren.

Als u een domein deelt en het wordt geblokkeerd of aan de lijst van gewezen personen toegevoegd, zou het uw collectieve postlevering kunnen beïnvloeden. Nochtans, zullen de kwesties van de reputatie of de blokken op een domein specifiek voor uw e-mailmarketing mededelingen enkel die stroom van e-mail beïnvloeden. Het gebruiken van uw hoofddomein als afzender of &quot;van&quot;adres voor veelvoudige poststromen kon e-mailauthentificatie ook breken, veroorzakend uw berichten om worden geblokkeerd of in de spamomslag worden geplaatst.

>[!NOTE]
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

De configuratie van subdomain staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Campaign te vormen. Beschikbare instelmethoden zijn:

* **Volledige subdomain delegatie aan Adobe** (geadviseerd): Subdomain wordt volledig gedelegeerd aan Adobe. Adobe kan alle aspecten van DNS beheren en handhaven die voor het leveren, het teruggeven en het volgen van berichten worden vereist. [ leer meer over volledige subdomain delegatie ](delegate-subdomain.md#full-subdomain-delegation)

* **Gebruik van CNAMEs**: Creeer subdomain en gebruik CNAMEs om aan Adobe-specifieke verslagen te richten. Met deze instelling delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. [ Leer meer over subdomain van de NAAM delegatie ](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* De volledige subdomeindelegatie heeft de voorkeur.
>
>* De methode CNAME wordt geadviseerd als het beleid van uw organisatie de volledige subdomain delegatiemethode beperkt. Deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren. Adobe zal niet in het veranderen van, het handhaven van of het beheren van DNS voor subdomain kunnen bijwonen die door de methode CNAME wordt gevormd.

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:

| Configuratiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign nodig zijn.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **CNAME, aangepaste methode** | Maak het subdomein en de naamruimterecord. Adobe verstrekt dan de records die in uw DNS servers moeten worden geplaatst en configureert de overeenkomstige waarden in de DNS-servers van Adobe Campaign.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

De extra informatie over domeinconfiguratie is beschikbaar in [ deze documentatie ](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Als u om het even welke vraag betreffende subdomain configuratiemethodes hebt, contacteer aan Adobe, of uiteindelijk de Zorg van de Klant om het raadplegen van de Leverbaarheid te verzoeken.

## Gedelegeerde subdomeinen benaderen {#access-delegated-subdomains}

Alle gedelegeerde subdomeinen worden weergegeven in het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** . Er zijn filters beschikbaar waarmee u de lijst (datum van delegatie, gebruiker of status) kunt verfijnen.

![](assets/subdomain-list.png)

De kolom **[!UICONTROL Status]** bevat informatie over het delegatieproces van subdomeinen:

* **[!UICONTROL Draft]**: de subdomeindelegatie is opgeslagen als concept. Klik op de subdomeinnaam om het delegatieproces te hervatten.
* **[!UICONTROL Processing]**: het subdomein controleert verschillende configuraties voordat het kan worden gebruikt,
* **[!UICONTROL Success]**: het subdomein heeft de controles met succes doorlopen en kan worden gebruikt om berichten te leveren,
* **[!UICONTROL Failed]**: een of meer controles zijn mislukt nadat de subdomeindelegatie is verzonden.

Als u toegang wilt tot gedetailleerde informatie over een subdomein met de status **[!UICONTROL Success]** , opent u het subdomein in de lijst.

![](assets/subdomain-delegated.png)

U kunt:

* Haal de subdomeinnaam (read-only) op die tijdens het delegatieproces wordt gevormd, evenals geproduceerde URLs (middelen, spiegelpagina&#39;s, het volgen URLs),

* Voeg een van de plaatsverificatie TXT- verslag van Google aan uw subdomain toe om ervoor te zorgen dat het wordt geverifieerd (zie [ een van Google TXT- verslag aan subdomain ](google-txt.md) toevoegen).


>[!CAUTION]
>
>Subdomeinconfiguratie is algemeen voor alle omgevingen. Daarom zal elke wijziging aan een subdomein ook invloed hebben op de productiesandboxen.
