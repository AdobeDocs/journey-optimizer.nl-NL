---
solution: Journey Optimizer
product: journey optimizer
title: Een subdomein delegeren
description: Leer hoe u uw subdomeinen kunt delegeren.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, delegatie, domein, DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 3cc5abdbec27ac9a8009b3b0d125a3b49dc9ed04
workflow-type: tm+mt
source-wordcount: '1968'
ht-degree: 5%

---

# Een subdomein delegeren {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Subdomeindelegatie"
>abstract="Met Journey Optimizer kunt u uw subdomeinen delegeren aan Adobe. U kunt een subdomein volledig delegeren aan Adobe, wat de geadviseerde methode is. U kunt ook een subdomein creëren gebruikend CNAMEs om aan Adobe-specifieke verslagen te richten, maar deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="Methoden voor subdomeinconfiguratie"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Subdomeindelegatie"
>abstract="Als u e-mailberichten wilt verzenden, delegeert u uw subdomein naar Adobe. Zodra gedaan, DNS verslagen, inboxes, afzender, antwoord aan en stuitend adressen zullen voor u worden gevormd."

## Aan de slag met e-mailsubdomeinen {#gs-delegate-subdomain}

De domeinnaamdelegatie is een methode die de eigenaar van een domeinnaam (technisch: een DNS-zone) toestaat om een onderverdeling van de domeinnaam (technisch: een DNS-zone eronder, die een subzone kan worden genoemd) aan een andere entiteit te delegeren. In feite kunt u als klant, als u de zone &quot;example.com&quot; afhandelt, de subzone &quot;marketing.example.com&quot; delegeren aan Adobe. Leer meer over [ subdomain delegatie ](about-subdomain-delegation.md)

Door gebrek, [!DNL Journey Optimizer] staat u toe om **tot 10 subdomeinen** af te vaardigen. Afhankelijk van uw licentiecontract kunt u echter maximaal 100 subdomeinen delegeren. Neem contact op met uw Adobe-contactpersoon voor meer informatie over het aantal subdomeinen waarop u recht hebt.

U kunt een subdomein volledig delegeren, of een subdomein tot stand brengen gebruikend CNAMEs om aan Adobe-specifieke verslagen te richten.

De volledige subdomeindelegatie is de geadviseerde methode. Leer meer over de verschillen tussen beide [ methodes van de subdomeinconfiguratie ](about-subdomain-delegation.md#subdomain-delegation-methods).

Subdomeinconfiguratie is **gemeenschappelijk aan alle milieu&#39;s**. Daarom heeft elke wijziging van een subdomein ook invloed op de productiesandboxen.

>[!CAUTION]
>
>Parallelle verzending van subdomeinen wordt niet ondersteund in [!DNL Journey Optimizer] . Als u een subdomein probeert te verzenden voor delegatie wanneer een ander subdomein de **[!UICONTROL Processing]** status heeft, wordt een foutbericht weergegeven.

## Subdomein volledig delegeren aan Adobe {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="De overeenkomende DNS-records genereren"
>abstract="Als u een nieuw subdomein volledig wilt delegeren aan Adobe, moet u de Adobe-gegevens van de nameserver die in de Journey Optimizer-interface worden weergegeven kopiëren en plakken in uw domein-ontvangende oplossing om de overeenkomende DNS-records te genereren. Als u een subdomein wilt delegeren met gebruik van CNAME&#39;s, moet u ook de SSL CDN URL-validatierecord kopiëren en plakken. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om berichten te leveren."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain#cname-subdomain-delegation" text="CNAME-subdomeindelegatie"

Met [!DNL Journey Optimizer] kunt u de subdomeinen volledig delegeren naar Adobe, rechtstreeks vanuit de productinterface. Door dit te doen, zal Adobe berichten als beheerde dienst kunnen leveren door alle aspecten van DNS te controleren en te handhaven die voor het leveren, het teruggeven en het volgen van e-mailcampagnes worden vereist.

U kunt op Adobe vertrouwen om de DNS-infrastructuur te onderhouden die nodig is om te voldoen aan de industriestandaard vereisten voor de levering van uw e-mailverzendende domeinen voor marketingdoeleinden, terwijl u DNS voor uw interne e-maildomeinen blijft onderhouden en beheren.

Voer de volgende stappen uit om een nieuw subdomein volledig te delegeren aan Adobe:

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** en klik op **[!UICONTROL Set up subdomain]** .

   ![](assets/subdomain-delegate.png)

1. Selecteer **[!UICONTROL Fully delegated]** in de sectie **[!UICONTROL Set up method]** .

   ![](assets/subdomain-method-full.png)

1. Geef de naam op van het subdomein dat u wilt delegeren.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Het delegeren van een ongeldig subdomein naar Adobe is niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

1. Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;.

   ![](assets/subdomain-submit.png)

1. DMARC-record instellen. Als het subdomein een bestaande DMARC-record heeft en deze wordt opgehaald door [!DNL Journey Optimizer] , kunt u dezelfde waarden gebruiken of wijzigen als nodig is. Als u geen waarden toevoegt, worden de standaardwaarden gebruikt. [Meer informatie](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Klik op **[!UICONTROL Submit]**.

   U kunt de records maken en de subdomeinconfiguratie later verzenden met de knop **[!UICONTROL Save as draft]** . Vervolgens kunt u de subdomeindelegatie hervatten door deze te openen vanuit de lijst met subdomeinen.

1. Het subdomein wordt in de lijst weergegeven met de status **[!UICONTROL Processing]** . Voor meer op de statussen van subdomeinen, verwijs naar [ deze sectie ](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Voordat u dat subdomein kunt gebruiken voor het verzenden van berichten, moet u wachten tot Adobe de vereiste controles uitvoert. Dit kan maximaal 3 uur in beslag nemen. Lees meer in [deze sectie](#subdomain-validation).

   >[!NOTE]
   >
   >Ontbrekende records (de records die nog niet op de hostingoplossing zijn gemaakt) worden weergegeven.

1. Zodra de controles succesvol zijn, krijgt subdomain de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.

Wanneer een subdomein in [!DNL Journey Optimizer] is gedelegeerd aan Adobe, wordt automatisch een PTR-record gemaakt en gekoppeld aan dit subdomein. [Meer informatie](ptr-records.md)


## Een subdomein instellen met CNAME&#39;s {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="De overeenkomende DNS- en validatierecords genereren"
>abstract="Als u een subdomein wilt delegeren met gebruik van CNAME&#39;s, moet u de Adobe-informatie voor de naamserver en de URL-validatierecord van de SSL CDN kopiëren en plakken die in de Journey Optimizer-interface in uw hostplatform worden weergegeven. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om berichten te leveren."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="De validatierecord kopiëren"
>abstract="Adobe genereert een validatierecord. U moet de corresponderende record op uw hostplatform maken voor CDN URL-validatie."

Als u domein-specifieke beperkingsbeleid hebt en u Adobe slechts gedeeltelijke controle over DNS wilt hebben, kunt u verkiezen om alle DNS-gerelateerde activiteiten op uw kant uit te voeren.

Met de CNAME-subdomeinset kunt u een subdomein maken en CNAME&#39;s gebruiken om te verwijzen naar Adobe-specifieke records. Met behulp van deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS om een omgeving in te stellen voor het verzenden, renderen en volgen van e-mails.

>[!CAUTION]
>
>De methode CNAME wordt geadviseerd als het beleid van uw organisatie de volledige subdomain delegatiemethode beperkt. Deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren. Adobe zal niet in het veranderen van, het handhaven van of het beheren van DNS voor subdomain kunnen bijwonen die door de methode CNAME wordt gevormd.

➡️ [ Leer hoe te om subdomain tot stand te brengen die CNAME gebruiken om aan Adobe-Specifieke verslagen in deze video te richten ](#video)

Volg onderstaande stappen om een subdomein in te stellen met gebruik van CNAME&#39;s:

1. Open het menu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** en klik op **[!UICONTROL Set up subdomain]** .

1. Selecteer de methode **[!UICONTROL CNAME set up]** .

   ![](assets/subdomain-method-cname.png)

1. Geef de naam op van het subdomein dat u wilt delegeren.

   >[!CAUTION]
   >
   >U mag een ongeldig subdomein niet delegeren aan Adobe. Zorg ervoor om een geldig subdomein in te gaan dat **door uw organisatie** wordt bezeten, zoals marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

1. Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

1. Stel het DMARC-record in. Als het subdomein een bestaande DMARC-record heeft en deze wordt opgehaald door [!DNL Journey Optimizer] , kunt u dezelfde waarden gebruiken of wijzigen als nodig is. Als u geen waarden toevoegt, worden de standaardwaarden gebruikt. [Meer informatie](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Klik op **[!UICONTROL Continue]**.

   U kunt de records later maken met de knop **[!UICONTROL Save as draft]** . Vervolgens kunt u de subdomeindelegatie in dit stadium hervatten door deze vanuit de lijst met subdomeinen te openen.

1. Wacht tot Adobe controleert of de records zonder fouten op de hostingoplossing zijn gegenereerd. Dit proces kan tot 2 minuten duren.

   >[!NOTE]
   >
   >Ontbrekende records (de records die nog niet op de hostingoplossing zijn gemaakt) worden weergegeven.

1. Adobe genereert een SSL CDN URL-validatierecord. Kopieer deze validatierecord naar het hostplatform. Als u deze record op de hostingoplossing juist hebt gemaakt, schakelt u het selectievakje &quot;I confirm...&quot; in en klikt u op **[!UICONTROL Submit]** .

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. Nadat de CNAME-subdomeindelegatie is verzonden, wordt het subdomein in de lijst weergegeven met de status **[!UICONTROL Processing]** . Voor meer op de statussen van subdomeinen, verwijs naar [ deze sectie ](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   Voordat u dat subdomein kunt gebruiken voor het verzenden van berichten, moet u wachten tot Adobe de vereiste controles uitvoert. Dit duurt meestal 2 tot 3 uur. Lees meer in [deze sectie](#subdomain-validation).

1. Zodra de controles succesvol <!--i.e Adobe validates the record you created and installs it--> zijn, subdomain krijgt de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.

Na het valideren van de record en het installeren van het certificaat maakt Adobe automatisch de PTR-record voor het CNAME-subdomein. [Meer informatie](ptr-records.md)


## Subdomeinvalidatie {#subdomain-validation}

De onderstaande controles en acties worden uitgevoerd totdat het subdomein is geverifieerd en kunnen worden gebruikt om berichten te verzenden.

Deze stappen worden uitgevoerd door Adobe en kunnen **tot 3 uren** nemen.

1. **pre-validate**: Adobe controleert of subdomain aan Adobe DNS (NS- verslag, verslag SOA, de opstelling van de Zone, eigendomsverslag) is gedelegeerd. Als de pre-validatiestap mislukt, wordt een fout geretourneerd samen met de bijbehorende reden, anders gaat Adobe naar de volgende stap.

1. **vorm DNS voor het domein**:

   * **MX verslag**: Het verslag van eXchange van de post - het serververslag van de Post dat binnenkomende e-mails verwerkt die naar subdomain worden verzonden.
   * **SPF verslag**: Het verslag van het Kader van het Beleid van de afzender - maakt een lijst van IPs van de postservers die e-mails van subdomain kunnen verzenden.
   * **het verslag van DKIM**: DomainKeys Identified Mail standaardverslag - gebruikt publiek-private zeer belangrijke encryptie om het bericht voor authentiek te verklaren om voor de gek houden te vermijden.
   * **A**: StandaardIP afbeelding.
   * **CNAME**: Een Canonical Naam of CNAME verslag is een type van DNS verslag dat een alias naam aan een ware of canonieke domeinnaam in kaart brengt.

1. **creeer het volgen en spiegel URLs**: als het domein email.example.com is, zal het volgen/spiegeldomein data.email.example.com zijn. Het wordt beveiligd door het SSL-certificaat te installeren.

1. **Levering CDN CloudFront**: als CDN niet opstelling reeds is, voorziet Adobe het voor identiteitskaart van uw organisatie.

1. **creeer CDN domein**: als het domein email.example.com is, zal het CDN domein cdn.email.example.com zijn.

1. **creeer en maak SSL CDN certificaat** vast: Adobe leidt tot het CDN certificaat voor het CDN domein en verbindt het certificaat aan het CDN domein.

1. **creeer voorwaartse DNS**: als dit eerste subdomain is dat u delegeert, zal Adobe voorwaartse DNS creëren die wordt vereist om PTR verslagen - voor elk van uw IPs tot stand te brengen.

1. **creeer PTR verslag**: Het verslag van PTR, dat ook als omgekeerd DNS verslag wordt bekend, wordt vereist door ISPs zodat zij niet de e-mails als spam merken. Gmail adviseert ook hebbend PTR verslagen voor elk IP. Adobe leidt PTR verslagen slechts tot wanneer u subdomain voor het eerst, voor elk IP, één voor alle IP&#39;s delegeert die dat subdomain richten. Bijvoorbeeld, als IP *192.1.2.1* is en subdomain *email.example.com* is, zal het PTR verslag zijn: *192.1.2.1PTR r1.email.example.com*. U kunt de PTR-record achteraf bijwerken en naar het nieuwe gedelegeerde domein verwijzen. [ leer meer over PTR verslagen ](ptr-records.md)

## Een subdomein delegeren ongedaan maken {#undelegate-subdomain}

Neem contact op met uw Adobe-vertegenwoordiger als u een subdomein wilt dedelegeren.

U moet echter verschillende stappen uitvoeren in de gebruikersinterface voordat u Adobe bereikt.

>[!NOTE]
>
>U kunt alleen subdomeinen met de status **[!UICONTROL Success]** dedelegeren. Subdomeinen met de statussen **[!UICONTROL Draft]** en **[!UICONTROL Failed]** kunnen eenvoudig uit de gebruikersinterface worden verwijderd.

Voer eerst de volgende stappen uit in [!DNL Journey Optimizer] :

1. Deactiveer alle kanaalconfiguraties verbonden aan subdomain. [ leer hoe ](../configuration/channel-surfaces.md#deactivate-a-surface)

1. U kunt elke landingspagina-subdomeinen, SMS-subdomeinen en websubdomeinen die aan dit subdomein zijn gekoppeld, verwijderen.

   U moet een specifiek verzoek voor elke [ het landen pagina ](../landing-pages/lp-subdomains.md#undelegate-subdomain), [ SMS ](../sms/sms-subdomains.md#undelegate-subdomain), of [ Web subdomain ](../web/web-delegated-subdomains.md#undelegate-subdomain) opheffen.

1. Stop de actieve campagnes verbonden aan subdomeinen. [ leer hoe ](../campaigns/modify-stop-campaign.md#stop)

1. Stop de actieve reizen verbonden aan subdomeinen. [ leer hoe ](../building-journeys/end-journey.md#stop-journey)

1. Punt de [ PTR verslagen ](ptr-records.md#edit-ptr-record) verbonden aan subdomain aan een ander subdomain.

   Als dit het enige gedelegeerde subdomein is, kunt u deze stap overslaan.

Als u klaar bent, neemt u contact op met uw Adobe-vertegenwoordiger met het subdomein dat u wilt uitschakelen.

Nadat uw verzoek door Adobe wordt behandeld, wordt het niet-gedelegeerde domein niet meer getoond op de pagina van de subdomeininventaris.

>[!CAUTION]
>
>Wanneer een subdomein niet is gedelegeerd, geldt het volgende:
>
>* U kunt de kanaalconfiguraties die dat subdomein gebruikten, niet opnieuw activeren.
>* U kunt hetzelfde subdomein niet opnieuw delegeren via de gebruikersinterface. Neem desgewenst contact op met uw Adobe-vertegenwoordiger.

## Hoe kan ik-video{#video}

Leer hoe u een subdomein maakt met CNAME om naar Adobe-specifieke records te verwijzen.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
