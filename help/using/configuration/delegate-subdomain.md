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
source-git-commit: c7c72a74b451759bf99f909bc146897c783f78ed
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 6%

---

# Een subdomein delegeren {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Subdomeindelegatie"
>abstract="Met Journey Optimizer kunt u uw subdomeinen delegeren aan Adobe. U kunt een subdomein volledig delegeren aan Adobe, wat de geadviseerde methode is. U kunt ook een subdomein tot stand brengen gebruikend CNAMEs om aan Adobe-specifieke verslagen te richten, maar deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="Methoden voor subdomeinconfiguratie"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Subdomeindelegatie"
>abstract="Als u e-mailberichten wilt verzenden, delegeert u uw subdomein aan de Adobe. Zodra gedaan, DNS verslagen, inboxes, afzender, antwoord aan en stuitend adressen zullen voor u worden gevormd."

De domeinnaamdelegatie is een methode die de eigenaar van een domeinnaam (technisch: een DNS-zone) toestaat om een onderverdeling van de domeinnaam (technisch: een DNS-zone eronder, die een subzone kan worden genoemd) aan een andere entiteit te delegeren. In feite, als klant, als u de streek &quot;example.com&quot;behandelt, kunt u subzone &quot;marketing.example.com&quot;aan Adobe delegeren. Meer informatie over [subdomeindelegatie](about-subdomain-delegation.md)

>[!NOTE]
>
>Standaard, [!DNL Journey Optimizer] Hiermee kunt u maximaal 10 subdomeinen delegeren. Afhankelijk van uw licentiecontract kunt u echter maximaal 100 subdomeinen delegeren. Bereik uit aan uw contact van de Adobe om meer over het aantal subdomeinen te leren u aan recht hebt.

U kunt een subdomein volledig delegeren, of een subdomein tot stand brengen gebruikend CNAMEs om aan Adobe-specifieke verslagen te richten.

>[!CAUTION]
>
>De volledige subdomeindelegatie is de geadviseerde methode. Meer informatie over de verschillen tussen beide [subdomeinconfiguratiemethoden](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>Subdomeinconfiguratie is algemeen voor alle omgevingen. Daarom zal elke wijziging aan een subdomein ook invloed hebben op de productiesandboxen.

## Volledige subdomeindelegatie {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="De overeenkomende DNS-records genereren"
>abstract="Om een nieuw subdomein volledig aan Adobe te delegeren, moet u kopiëren-kleven de Adobe nameserverinformatie die in de interface van Journey Optimizer in uw domein-ontvangende oplossing wordt getoond om de passende DNS verslagen te produceren. Als u een subdomein wilt delegeren met gebruik van CNAME&#39;s, moet u ook de SSL CDN URL-validatierecord kopiëren en plakken. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om berichten te leveren."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html#cname-subdomain-delegation" text="CNAME-subdomeindelegatie"

[!DNL Journey Optimizer] staat u toe om uw subdomeinen aan Adobe direct van de productinterface volledig te delegeren. Door dit, zal de Adobe berichten als beheerde dienst kunnen leveren door alle aspecten van DNS te controleren en te handhaven die voor het leveren, het teruggeven en het volgen van e-mailcampagnes worden vereist.

U kunt op Adobe vertrouwen om de DNS infrastructuur te handhaven die wordt vereist om aan industrie-standaardleveringsvereisten voor uw e-mail marketing verzendende domeinen te voldoen, terwijl het blijven DNS voor uw interne e-maildomeinen handhaven en controleren.

Volg de onderstaande stappen om een nieuw subdomein volledig te delegeren aan Adobe:

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** en klik vervolgens op **[!UICONTROL Set up subdomain]**.

   ![](assets/subdomain-delegate.png)

1. Selecteren **[!UICONTROL Fully delegated]** van de **[!UICONTROL Set up method]** sectie.

   ![](assets/subdomain-method-full.png)

1. Geef de naam op van het subdomein dat u wilt delegeren.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Het delegeren van een ongeldig subdomein aan Adobe wordt niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

1. Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;.

   ![](assets/subdomain-submit.png)

1. DMARC-record instellen. Als het subdomein een bestaand DMARC-record heeft en als het wordt opgehaald door [!DNL Journey Optimizer]kunt u dezelfde waarden gebruiken of wijzigen als u wilt. Als u geen waarden toevoegt, worden de standaardwaarden gebruikt. [Meer informatie](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Klik op **[!UICONTROL Submit]**.

   >[!NOTE]
   >
   >U kunt de records maken en de subdomeinconfiguratie later verzenden met de opdracht **[!UICONTROL Save as draft]** knop. Vervolgens kunt u de subdomeindelegatie hervatten door deze te openen vanuit de lijst met subdomeinen.

1. Het subdomein wordt in de lijst weergegeven met de **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Voordat u dat subdomein kunt gebruiken om berichten te verzenden, moet u wachten tot de Adobe de vereiste controles uitvoert. Dit kan maximaal 3 uur in beslag nemen. Lees meer in [deze sectie](#subdomain-validation).

   >[!NOTE]
   >
   >Ontbrekende records (de records die nog niet op de hostingoplossing zijn gemaakt) worden weergegeven.

1. Wanneer de controles zijn voltooid, haalt het subdomein het subdomein **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   >[!NOTE]
   >
   >Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.

Zodra een subdomein aan Adobe binnen wordt gedelegeerd [!DNL Journey Optimizer], wordt automatisch een PTR-record gemaakt en gekoppeld aan dit subdomein. [Meer informatie](ptr-records.md)

>[!CAUTION]
>
>Parallelle uitvoering van subdomeinen wordt momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een subdomein probeert in te dienen voor delegatie wanneer een ander subdomein het **[!UICONTROL Processing]** status, krijgt u een foutbericht.

## CNAME-subdomeininstelling {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="De overeenkomende DNS- en validatierecords genereren"
>abstract="Als u een subdomein wilt delegeren met gebruik van CNAME&#39;s, moet u de gegevens van de Adobe-nameserver en de URL-validatierecord van de SSL CDN kopiëren en plakken die in de Journey Optimizer-interface in uw hostplatform worden weergegeven. Zodra de controles succesvol zijn, is subdomain klaar om worden gebruikt om berichten te leveren."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="De validatierecord kopiëren"
>abstract="Adobe genereert een validatierecord. U moet de corresponderende record op uw hostplatform maken voor CDN URL-validatie."

Als u domein-specifieke beperkingsbeleid hebt en u Adobe slechts gedeeltelijke controle over DNS wilt hebben, kunt u verkiezen om alle DNS-gerelateerde activiteiten op uw kant uit te voeren.

De subdomeinopstelling van CNAME laat u toe om subdomain tot stand te brengen en CNAMEs te gebruiken om aan Adobe-specifieke verslagen te richten. Met deze configuratie delen u en de Adobe de verantwoordelijkheid voor het onderhoud van DNS in de omgeving voor het verzenden, renderen en volgen van e-mails.

>[!CAUTION]
>
>De methode CNAME wordt geadviseerd als het beleid van uw organisatie de volledige subdomain delegatiemethode beperkt. Deze benadering vereist u om DNS verslagen op uw te handhaven en te beheren. De Adobe zal niet in het veranderen van, het handhaven van of het beheren van DNS voor subdomain kunnen bijwonen die door de methode CNAME wordt gevormd.

➡️ [Leer hoe te om subdomain tot stand te brengen gebruikend CNAME om aan Adobe-specifieke verslagen in deze video te richten](#video)

Volg onderstaande stappen om een subdomein in te stellen met gebruik van CNAME&#39;s:

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** en klik vervolgens op **[!UICONTROL Set up subdomain]**.

1. Selecteer de **[!UICONTROL CNAME set up]** methode.

   ![](assets/subdomain-method-cname.png)

1. Geef de naam op van het subdomein dat u wilt delegeren.

   >[!CAUTION]
   >
   >Het delegeren van een ongeldig subdomein aan Adobe wordt niet toegestaan. Zorg ervoor dat u een geldig subdomein invoert dat eigendom is van uw organisatie, zoals marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

1. Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;ik bevestig...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

1. Stel het in op DMARC-record. Als het subdomein een bestaand DMARC-record heeft en als het wordt opgehaald door [!DNL Journey Optimizer]kunt u dezelfde waarden gebruiken of wijzigen als u wilt. Als u geen waarden toevoegt, worden de standaardwaarden gebruikt. [Meer informatie](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Klik op **[!UICONTROL Continue]**.

   >[!NOTE]
   >
   >U kunt de records later maken met de opdracht **[!UICONTROL Save as draft]** knop. Vervolgens kunt u de subdomeindelegatie in dit stadium hervatten door deze vanuit de lijst met subdomeinen te openen.

1. Wacht tot de Adobe controleert dat de verslagen zonder fouten op uw het ontvangen oplossing worden geproduceerd. Dit proces kan tot 2 minuten duren.

   >[!NOTE]
   >
   >Ontbrekende records (de records die nog niet op de hostingoplossing zijn gemaakt) worden weergegeven.

1. Adobe genereert een SSL CDN URL-validatierecord. Kopieer deze validatierecord naar het hostplatform. Als u deze record op de hostingoplossing juist hebt gemaakt, schakelt u het selectievakje &quot;I confirm...&quot; in en klikt u op **[!UICONTROL Submit]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. Zodra de subdomeindelegatie van CNAME is voorgelegd, toont subdomain in de lijst met **[!UICONTROL Processing]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   Voordat u dat subdomein kunt gebruiken om berichten te verzenden, moet u wachten tot de Adobe de vereiste controles uitvoert. Dit duurt meestal 2 tot 3 uur. Lees meer in [deze sectie](#subdomain-validation).

1. Zodra de controles succesvol zijn<!--i.e Adobe validates the record you created and installs it-->, wordt het subdomein de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   >[!NOTE]
   >
   >Het subdomein wordt gemarkeerd als **[!UICONTROL Failed]** als u er niet in slaagt de validatierecord voor uw hostoplossing te maken.

Na het valideren van de record en het installeren van het certificaat wordt door Adobe automatisch de PTR-record voor het subdomein CNAME gemaakt. [Meer informatie](ptr-records.md)

>[!CAUTION]
>
>Parallelle uitvoering van subdomeinen wordt momenteel niet ondersteund in [!DNL Journey Optimizer]. Als u een subdomein probeert in te dienen voor delegatie wanneer een ander subdomein het **[!UICONTROL Processing]** status, krijgt u een foutbericht.

## Subdomeinvalidatie {#subdomain-validation}

De onderstaande controles en acties worden uitgevoerd totdat het subdomein is geverifieerd en kunnen worden gebruikt om berichten te verzenden.

>[!NOTE]
>
>Deze stappen worden uitgevoerd door Adobe en kunnen tot 3 uur duren.

1. **Pre-validate**: Adobe controleert of het subdomein is gedelegeerd aan Adobe DNS (NS-record, SOA-record, Zone-instelling, eigendomsrecord). Als de pre-bevestigingsstap ontbreekt, is een fout teruggekeerd samen met de overeenkomstige reden, anders gaat de Adobe aan de volgende stap.

1. **DNS voor het domein configureren**:

   * **MX-record**: E-mailuitwisselingsrecord - E-mailserverrecord dat binnenkomende e-mails verwerkt die naar het subdomein zijn verzonden.
   * **SPF-record**: Het verslag van het Kader van het Beleid van de afzender - maakt een lijst van IPs van de postservers die e-mails van subdomain kunnen verzenden.
   * **DKIM-record**: DomainKeys Identified Mail standard record - Gebruikt versleuteling met een openbare en persoonlijke sleutel om het bericht te verifiëren zodat spoofing wordt voorkomen.
   * **A**: Standaard IP-toewijzing.
   * **CNAME**: Een Canonical Name- of CNAME-record is een type DNS-record dat een aliasnaam toewijst aan een echte of canonieke domeinnaam.

1. **URL&#39;s voor bijhouden en spiegelen maken**: als het domein email.example.com is, wordt het tracking/mirror-domein data.email.example.com. Het wordt beveiligd door het SSL-certificaat te installeren.

1. **CDN CloudFront instellen**: als CDN nog niet is ingesteld, bepaalt de Adobe het voor identiteitskaart van uw organisatie.

1. **CDN-domein maken**: als het domein email.example.com is, wordt het CDN-domein cdn.email.example.com.

1. **CDN SSL-certificaat maken en koppelen**: Adobe maakt het CDN-certificaat voor het CDN-domein en koppelt het certificaat aan het CDN-domein.

1. **forward DNS maken**: als dit het eerste subdomein is dat u delegeert, zal de Adobe voorwaartse DNS tot stand brengen die wordt vereist om PTR verslagen - voor elk van uw IPs tot stand te brengen.

1. **PTR-record maken**: PTR-record, ook wel omgekeerd DNS-record genoemd, wordt vereist door de ISP&#39;s, zodat deze de e-mails niet als spam markeren. Gmail adviseert ook hebbend PTR verslagen voor elk IP. Adobe leidt tot PTR verslagen slechts wanneer u subdomain voor het eerst, één voor elk IP delegeert, alle IPs die dat subdomain richten. Als het IP-bestand bijvoorbeeld *192.1.2.1* en het subdomein is *email.example.com* De PTR-record is: *192.1.2.1 PTR r1.email.example.com*. U kunt de PTR-record achteraf bijwerken en naar het nieuwe gedelegeerde domein verwijzen. [Meer informatie over PTR-records](ptr-records.md)

## Hoe kan ik-video{#video}

Leer hoe u een subdomein maakt met CNAME om naar Adobe-specifieke records te verwijzen.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
