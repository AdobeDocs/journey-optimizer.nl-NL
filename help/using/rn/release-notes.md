---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Aanvullende informatie voor Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f1a8305d0f9cc93ae5dc93d73c8ed9513733d1a2
workflow-type: tm+mt
source-wordcount: '4189'
ht-degree: 9%

---

# Aanvullende informatie {#release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd in de laatste week van elke maand in deze releaseopmerkingen.

Opmerkingen bij vorige release zijn beschikbaar in [deze pagina](release-notes-2022.md). U kunt ook de [meest recente documentatie-updates](documentation-updates.md) pagina voor meer wijzigingen.

[!DNL Adobe Journey Optimizer] is native [!DNL Adobe Experience Platform] en erft van de meest recente innovaties en verbeteringen. Meer informatie over deze wijzigingen vindt u in [Opmerkingen bij de release van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Nieuwsbrief](../assets/do-not-localize/nl-icon.png) Meld u aan voor de [Adobe Journey Optimizer driemaandelijkse nieuwsbrief](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} vandaag, en ontvang de recentste productupdates, opwindende verhalen, gebruiksgevallen, uiteinden en meer die direct aan uw Postbus worden geleverd elk kwartaal.


## Opmerkingen bij de release september 2023 {#sept-rn-2023}

### Nieuwe functies{#sept-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>Berekende kenmerken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met berekende kenmerken kunt u gebeurtenisgegevens eenvoudig samenvatten in profielkenmerken via een intuïtieve gebruikersinterface voor verbeterde op gedrag gebaseerde segmentatie, personalisatie en activering. Met deze functie kunt u berekende kenmerken op een zelfservermanier maken, deze beheren en ze in segmentatie gebruiken, in realtime klantprofielbestemmingen of Journey Optimizer.<br/><br/>
Bovendien vereenvoudigt de berekende attributen segmentatie en reisworkflows om u te helpen relevante ervaringen naadloos te leveren. Meer informatie in het dialoogvenster <a href="../audience/computed-attributes.md">gedetailleerde documentatie</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Geconsolideerde Kanaalrapporten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De functie Kanaalrapport biedt analisten en marketers een uitgebreid overzicht van verkeers- en betrokkenheidsgegevens op kanaalniveau.</p>
<p>Als u toegang wilt krijgen tot <b>Rapport</b> menu, moet u de <b>Kanaalrapporten weergeven</b> toestemming.</p>
<img src="assets/channel-reports.png"/>
<p>Raadpleeg voor meer informatie de <a href="../reports/channel-report.md">gedetailleerde documentatie</a>, en <a href="../reports/channel-report.md#channel-report-video">hoe kan ik-video</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dataset-exportdoelen (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer-gegevenssets die naar Cloud Storage-doelen worden geëxporteerd, zijn nu over het algemeen beschikbaar. Met deze functie kunt u een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren.</p>
<img src="../data/assets/dataset-export-setup.png">
<p>Raadpleeg de <a href="../data/export-datasets.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Opslag van gebruikersgegevens voor mobiele toepassingen per sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met deze nieuwe functie kunt u pushgegevens eenvoudig beheren en koppelen aan een specifieke sandbox in App Surfaces.</p>
<p>Raadpleeg de <a href="../in-app/inapp-configuration.md#channel-prerequisites">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

### Verbeteringen {#sept-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Personalisatie**

* Naast visuele fragmenten is het nu mogelijk om expressiefragmenten te maken, op te slaan en opnieuw te gebruiken vanuit de Journey Optimizer-interface via de Expressieeditor. Expressiefragmenten vervangen de eerder opgeslagen expressies. [Meer informatie](../personalization/use-expression-fragments.md)

**Waarschuwing**

* Er is een nieuw type systeemwaarschuwing geïntroduceerd. U kunt nu een melding krijgen wanneer een **Publiek lezen** activiteit mislukt. [Meer informatie](../reports/alerts.md).

**Webkanaal**

* Toepassingen van één pagina (SPA) kunnen nu worden ontworpen in de visuele editor van het web, zodat u kunt selecteren op welke specifieke weergaven u de wijzigingen van uw webpagina wilt toepassen. Een weergave kan worden gedefinieerd als een hele site of een groep visuele elementen op een site, zoals de startpagina, de hele productsite of het voorkeurenframe voor levering op alle afrekenpagina&#39;s. Eenmalige ontwikkelaarsopstelling is nodig om de meningen in de implementatie van SDK van het Web van Adobe Experience Platform te bepalen; dit laat marketers toe om de Webcampagnes van Adobe Journey Optimizer op SPA tot stand te brengen en in werking te stellen. [Meer informatie](../web/web-spa.md)

* Wanneer u een pagina bewerkt met de webontwerper, kunt u nu rechtstreeks vanuit het deelvenster Wijzigingen nieuwe wijzigingen aan uw inhoud toevoegen, zonder dat u een component hoeft te selecteren en te bewerken vanuit de ontwerpinterface. [Meer informatie](../web/manage-web-modifications.md#add-modifications)

* Wanneer u websubdomeinen instelt, kunt u nu ook uw eigen subdomein toevoegen, naast het gebruik van een subdomein dat al is gedelegeerd aan de Adobe. [Meer informatie](../web/web-delegated-subdomains.md#web-configure-new-subdomain)

**Journeys**

* Wanneer u een reis dupliceert, kunt u nu de naam van de reiskopie definiëren. [Meer informatie](../building-journeys/journey-gs.md#uplicate-a-journey)



* Ondersteuning voor aangepaste acties is nu GA. Met deze mogelijkheid kunt u API-oproepreacties gebruiken in aangepaste acties en uw reis ordenen op basis van deze reacties. Bovendien is een nieuwe guardrail toegevoegd om alle douaneacties tot 15.000 vraag over 30 seconden per eindpunt te beperken. [Meer informatie](../action/action-response.md)
<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**E-mailkanaal**

* Met een nieuwe optie in de configuratie van het e-mailoppervlak kunt u ervoor kiezen om transactieberichten naar profielen te verzenden, zelfs als hun e-mailadres zich op de Adobe bevindt [!DNL Journey Optimizer] suppressielijst. [Meer informatie](../email/email-settings.md#send-to-suppressed-email-addresses)

**Sms-kanaal**

* Twee nieuwe velden, **Bericht bij aanmelden** en **Help-bericht**, zijn toegevoegd aan het API-configuratiescherm, zodat gebruikers reacties voor binnenkomende trefwoorden kunnen aanpassen. Merk op dat dit slechts voor de leverancier van SMS van Sinch beschikbaar is. [Meer informatie](../sms/sms-configuration.md#create-api)

* De opt-out van SMS wordt niet meer beheerd op kanaalniveau. Het is nu numeriek-specifiek, wat betekent dat als sommige profielen van een bepaald aantal of korte code opteren, u hen nog berichten van andere aantallen kunt verzenden u kunt gebruiken om SMS berichten te verzenden. Met een nieuwe optie kunt u de optie **Uitschakelen-nummer** u wilt gebruiken voor een bepaald oppervlak. [Meer informatie](../sms/sms-configuration.md#message-preset-sms)

**Direct mailkanaal**

* U kunt nu bestanden versleutelen die zijn bedoeld voor uw direct-mailproviders wanneer deze worden overgebracht naar een server. Om dit te doen, is een nieuw gebied beschikbaar in het dossier dat configuratiescherm verplettert, toestaand u om uw encryptiesleutel te kopiëren-kleven. [Meer informatie](../direct-mail/direct-mail-configuration.md)

**Rapportage**

* U kunt nu Journey Optimizer-rapporten exporteren als CSV-bestand. Meer informatie in het dialoogvenster [gedetailleerde documentatie](../reports/global-report.md#export-reports) en de [hoe kan ik-video](../reports/global-report.md#video-csv).

**Assets**

* Met een nieuwe optie voor Middelen kunt u de repository voor uw Middelen in Journey Optimizer kiezen. U kunt kiezen voor een opslagplaats voor Assets Essentials of een as a Cloud Service opslagplaats voor middelen, op voorwaarde dat u eigenaar bent van deze oplossing. [Meer informatie](../content-management/assets-essentials.md)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->

## Opmerkingen bij de release augustus 2023 {#aug-rn-2023}

### Nieuwe functies{#aug-2023-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.

<table>
<thead>
<tr>
<th><strong>In-app berichten verzenden tijdens uw reizen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu persoonlijke In-app-berichten naar uw app-gebruikers verzenden voor een reis. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<img src="assets/do-not-localize/in-app-jo.gif"/>
<p>Raadpleeg de <a href="../in-app/create-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>E-mails met lijsten met zaden valideren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu zaadlijsten maken en beheren in Journey Optimizer. Een zaadlijst bestaat uit interne adressen die aan uw daadwerkelijke publiek kunnen worden toegevoegd en het nauwkeurige zelfde bericht zoals de gerichte profielen bij de tijd van de leveringsuitvoering ontvangen. Gebruik deze mogelijkheid om de verzonden communicatie te controleren en ervoor te zorgen dat alle weergave-indelingen, URL's, afbeeldingen en koppelingen correct zijn.</p>
<img src="../configuration/assets/seed-list-details.png">
<p>Raadpleeg de <a href="../configuration/seed-lists.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Generate text and images with the Content assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the Content assistant. You can now use the Content assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
<p>This capability is currently available as a private beta.</p>
<img src="assets/gen-ai-image-2.png"/>
<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->



### Verbeteringen {#aug-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

<!--
**APIs**

A new API to create and manage Content Fragments is now available. [Learn more](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.-->

<!--**Email channel**

A new option is available in the email surface settings to include email addresses suppressed due to spam complaint in your transactional messages audiences. Even if they marked marketing messages as spam, these profiles can then receive transactional messages, such as password reset or account statements. This option is disabled by default.-->

**Journeys**

* U kunt nu API vraagreacties in douaneacties gebruiken en uw reis structureren die op deze reacties wordt gebaseerd. Deze functie is momenteel beschikbaar als een persoonlijke bètaversie. [Meer informatie](../action/action-response.md).
* Er is een nieuw type systeemwaarschuwing geïntroduceerd. U kunt nu een melding krijgen wanneer een aangepaste handeling mislukt. [Meer informatie](../reports/alerts.md).
  <!--* When duplicating a journey, you can now define the name of the journey copy.-->


**Direct mail**

* Azure kan nu als servertype in het dossier worden geselecteerd dat configuratie verplettert. [Meer informatie](../direct-mail/direct-mail-configuration.md#file-routing-configuration)
* Ampersand is nu beschikbaar als veld voor kolomscheidingen in de instellingen voor het oppervlak voor directe e-mail. [Meer informatie](../direct-mail/direct-mail-configuration.md#direct-mail-surface)




## Opmerkingen bij de release juli 2023 {#july-rn-2023}

### Nieuwe functies{#july-2023-features}

<table>
<thead>
<tr>
<th><strong>Samenstelling publiek</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu compositieworkflows maken om bestaande Adobe Experience Platform-soorten publiek te combineren tot een visueel canvas en verschillende activiteiten (splitsen, verrijken...) gebruiken om nieuwe soorten publiek te maken. Nieuw gecreëerd publiek wordt samen met het bestaande publiek weer in Adobe Experience Platform opgeslagen en kan in Journey Optimizer-campagnes worden gebruikt om klanten te bereiken.</p>
<img src="assets/do-not-localize/gif-ao.gif"/>
<p>Raadpleeg de <a href="../audience/get-started-audience-orchestration.md">gedetailleerde documentatie</a> voor meer informatie.</p>
<p>De samenstelling van het publiek is volledig geïntegreerd met het nieuwe Adobe Experience Platform-menu "Soorten publiek", dat als een gecentraliseerd portaal voor het publiek fungeert. U kunt nu een bladerpagina gebruiken die een nieuw dashboard met segmenttendensen en overlappingen omvat om nieuwe inzichten te vinden en organisatorische hulpmiddelen voor het folderen en het etiketteren te onderzoeken. Binnen deze ervaring zijn beheerbesturingselementen ingebouwd voor gestandaardiseerde publiekslabels en mogelijkheden voor levenscyclusbeheer van het publiek om activeringsworkflows te beheren. Met deze nieuwe beheerervaring kunt u het publiek nu gemakkelijk en veilig beheren vanaf één locatie. Raadpleeg voor meer informatie <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html" target="_blank">Adobe Experience Platform-documentatie</a>.</p></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mailkanaal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu direct-mailberichten toevoegen aan uw campagnes. Directe post is een off-line kanaal dat u toestaat om de dossiers te personaliseren en te produceren die door directe postleveranciers worden vereist om post naar uw klanten te verzenden.</p>
<p>Wanneer u een directe postbestelling voorbereidt, genereert Journey Optimizer een bestand met alle doelprofielen en de gekozen contactgegevens (bijvoorbeeld postadres). U kunt dit bestand dan naar uw direct-mailprovider sturen, die voor de werkelijke verzending zorgt.</p>
<p>Direct mail channel is momenteel niet beschikbaar voor organisaties die de Adobe Healthcare Shield Add-on-aanbieding hebben aangeschaft.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>Raadpleeg de <a href="../direct-mail/get-started-direct-mail.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uw HTML-inhoud converteren voor de e-mailontwerper</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu alle HTML-inhoud importeren en converteren in de e-maileditor van Journey Optimizer. Inhoudsblokken worden automatisch geïdentificeerd en zijn beschikbaar in de e-mailontwerper: gebruik zijn krachtige ontwerpmogelijkheden om de inhoud bij te werken en aan te passen!</p>
<img src="assets/html-convert.png">
<p>Raadpleeg de <a href="../email/existing-content.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Tags gebruiken in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Naast campagnes en reizen kunt u nu Adobe Experience Platform Unified Tags toewijzen aan uw bestemmingspagina's, inhoudssjablonen, fragmenten en abonnementenlijsten. Op deze manier kunt u ze gemakkelijk classificeren en kunt u zoeken en navigeren in alle lijsten verbeteren. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Raadpleeg de <a href="../start/search-filter-categorize.md#tags">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Inhoudssjablonen, API's</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu Adobe Journey Optimizer-inhoudssjablonen maken en beheren met behulp van speciale API's, zodat u uw bestaande inhoudssysteem naadloos kunt integreren.</p>
<p>Raadpleeg de <a href="https://developer.adobe.com/journey-optimizer-apis/references/content/">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#july-2023-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.


**Campagnes**

Contextuele gebeurtenissen met betrekking tot campagnes zijn nu beschikbaar voor gebruik in het menu Contextafhankelijke kenmerken van de verpersoonlijkingseditor.


**Doelgroepen**

Er zijn verbeteringen aangebracht in de publiekekiezer tijdens reizen of campagnes, met toevoeging van nieuwe kolommen waarin de oorsprong en de actualiseringsfrequentie van het publiek worden weergegeven. Met de release van de portal Publiek compositie hebben Adobe Experience Platform en Adobe Journey Optimizer het gebruik van &quot;publiek&quot; en &quot;segment&quot; binnen het systeem en de documentatie bijgewerkt.

* Publiek: Een reeks personen, accounts, huishoudens of andere entiteiten die gemeenschappelijke kenmerken en gedragingen delen.
* Segmentdefinitie: in Adobe Experience Platform worden de regels gebruikt om sleutelkenmerken of gedrag van een doelgroep te beschrijven. Deze term werd voorheen &quot;segment&quot; genoemd.

Als gevolg hiervan worden in Adobe Journey Optimizer en de gebruikersinterface van Adobe Experience Platform &quot;Segmenten&quot; vervangen door &quot;Soorten publiek&quot; om deze nieuwe weg van publieksvorming en -beheer weer te geven.

**API&#39;s**

De JWT-methode voor het genereren van toegangstokens voor Adobe Journey Optimizer API-verificatie is afgekeurd. Alle nieuwe integraties moeten worden gecreeerd gebruikend de server-aan-Server authentificatiemethode OAuth. De Adobe adviseert ook dat u uw bestaande integraties aan de methode OAuth migreert. [Meer informatie](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.


**Andere wijzigingen**

Journey Optimizer-gegevenssets die naar Cloud Storage-doelen worden geëxporteerd, zijn nu beschikbaar voor alle klanten als een openbare bètaversie. Met deze functie kunt u een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren. [Meer informatie](../data/export-datasets.md)





## Opmerkingen bij de release van juni 2023 {#june-rn-2023}

<table>
<thead>
<tr>
<th><strong>API-getriggerde campagnes voor het op de markt brengen van gebruiksgevallen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu API's gebruiken om marketingcampagnes in Adobe Journey Optimizer te starten vanaf een extern systeem.</p>
<p>Tot deze versie, beantwoordde API-teweeggebrachte campagnecapaciteit diverse operationele en transactionele overseinenbehoeften zoals wachtwoordterugstellen of teken OTP, maar kon niet worden gebruikt om marketing campagnes tot stand te brengen. Beschikbare kanalen voor API-getriggerde campagnes zijn: E-mail, SMS en Push berichten.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Raadpleeg de <a href="../campaigns/api-triggered-campaigns.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<!--
### Improvements {#june-2023-improvements}


**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.

**Journeys**

You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

<!--
## June 2023 early release notes {#june-rn-2023}

Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    


**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.     

* A new type of system alert has been introduced. You can now get notified when a custom action fails.
-->

## Opmerkingen bij de release van mei 2023 {#may-rn-2023}

### Nieuwe functies{#may-2023-features}



<table>
<thead>
<tr>
<th><strong>Inhoud experimenteren in campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer steunt nu experimenten in campagnes. Experimenten zijn gerandomiseerde onderzoeken, die in de context van online tests betekenen dat u sommige willekeurig geselecteerde gebruikers aan een bepaalde variatie van een bericht blootstelt, en een andere willekeurig geselecteerde reeks gebruikers aan één of andere andere variatie of behandeling. Na blootstelling, kunt u de resultaatmetriek meten u in geinteresseerd bent, zoals opent van e-mail, abonnementen, of aankopen.</p>
<img src="assets/do-not-localize/experiment.gif"/>
<p>Raadpleeg de <a href="../campaigns/content-experiment.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Objective reporting and performance measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports.</p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../reports/campaign-global-report.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Fragmenten maken en gebruiken in uw e-mailinhoud</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu fragmenten ontwerpen, gebruiken en beheren om uw e-mails en inhoudssjablonen snel samen te stellen. Een fragment is een vooraf gebouwde herbruikbare component waarnaar in meerdere e-mails van Journey Optimizer-campagnes en -reizen kan worden verwezen voor een verbeterd en versneld ontwerpproces.</p>
<img src="assets/do-not-localize/fragments.gif"/>
<p>Raadpleeg de <a href="../content-management/fragments.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Tags gebruiken in uw campagnes (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu Adobe Experience Platform Unified Tags toewijzen aan uw campagnes. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. Merk op dat de Verenigde markeringseigenschap momenteel in bèta is.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Raadpleeg de <a href="../start/search-filter-categorize.md#tags">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Persoonlijk beoordelingsmodel voor optimalisatie voor AI (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De gepersonaliseerde Optimalisering AI rangschikkingsmodellen zijn nu algemeen beschikbaar in Beslissingsbeheer. Met dit nieuwe type model kunt u aanbiedingen optimaliseren en aanpassen op basis van publiek en prestaties.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Raadpleeg de <a href="../offers/ranking/personalized-optimization-model.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>



### Verbeteringen {#may-2023-improvements}

**Doelgroepen**

* Ter voorbereiding op de algemene beschikbaarheid van de Poortfunctie Publiek werkt Adobe Experience Platform het gebruik van &quot;publiek&quot; en &quot;segment&quot; binnen het systeem en de documentatie bij.

   * Publiek: Een reeks personen, accounts, huishoudens of andere entiteiten die gemeenschappelijke kenmerken en gedragingen delen.
   * Segmentdefinitie: in Adobe Experience Platform worden de regels gebruikt om sleutelkenmerken of gedrag van een doelgroep te beschrijven. Deze term werd voorheen &quot;segment&quot; genoemd.

  Dientengevolge, binnen Adobe Journey Optimizer en Adobe Experience Platform UI, zult u &quot;Segmenten&quot;vervangen door &quot;Publiek&quot;zien om deze nieuwe weg van publieksverwezenlijking en beheer te weerspiegelen.

  De vertalingen van de term &quot;publiek&quot; voor een groep profielen die bedoeld zijn om een bericht te ontvangen, zijn voor sommige talen geharmoniseerd voor alle Digital Experience-producten:

   * Duits: Zielgruppe
   * Braziliaans Portugees: público-alvo
   * Spaans: público destinatario

<!--* Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.-->

**Sms-kanaal**

* Infobip is toegevoegd als leverancier wanneer het vormen van uw het kanaaloppervlakten van SMS. [Meer informatie](../sms/sms-configuration.md)
* Twillio - De API credentieopstelling omvat nu de capaciteit om de dienst SID van het Overseinen voor naadloze integratie met uw rekening van Twilio toe te voegen. [Meer informatie](../sms/sms-configuration.md)

**Kanaal in app**

* Toegevoegde nieuwe regels van de berichttrekker voor de Dienst van Plaatsen van de Adobe. [Meer informatie](../in-app/inapp-configuration.md)
* Nieuwe Adobe Experience Platform Assurance-mogelijkheden toegevoegd om apparaatgebeurtenissen vast te leggen die moeten worden toegevoegd als triggerregels.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

**Campagnes**

* Het is nu mogelijk een campagne te dupliceren vanuit het inventarisscherm met behulp van het actiemenu voor ovaal. [Meer informatie](../campaigns/modify-stop-campaign.md#duplicate)
* U kunt nu ontwerpwijzigingen in een live campagne verwijderen.
* De stappen voor het activeren van een campagne zijn nu gestroomlijnd. [Meer informatie](../campaigns/modify-stop-campaign.md)

**Beslissingsbeheer**

* U kunt nu de frequentietoewijzing bewerken als de aanbieding de optie **[!UICONTROL Draft]** status en nooit eerder gepubliceerd met ingeschakelde frequentiecapping. [Meer informatie](../offers/offer-library/add-constraints.md#frequency-capping)

**Personalisatie**

* U kunt activa verwijzingen van de Redacteur van de Personalisatie nu selecteren en direct opnemen wanneer het werken in HTML inhoud.

### Oplossingen{#may-2023-fixes}

* In-app Berichten - Probleem verholpen waarbij het plannen van de campagne conflicteerde met de instellingen voor berichtfrequentie.


## Opmerkingen bij de release van april 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nieuwe functies{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Webkanaal (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer breidt zijn mogelijkheden over de kanalen uit door steun voor Webkanaal toe te voegen. U kunt nu net als elk ander kanaal een webeleving ontwerpen, wijzigen en voorvertonen via een slimme en intuïtieve visuele interface om uw ervaring voor eindgebruikers aan te passen. Op dit moment kunt u in Journey Optimizer alleen webervaringen maken in campagnes.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Raadpleeg de <a href="../web/get-started-web.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Snelstartworkflow voor mobiel aan boord (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nieuwe workflow voor snel starten op het instapmodel voor mobiele apparaten is nu beschikbaar. Met deze nieuwe productfunctie kunt u de Mobile SDK snel configureren om gegevens van mobiele gebeurtenissen te verzamelen en te valideren en om mobiele pushberichten te verzenden met Adobe Journey Optimizer. Dit vermogen is toegankelijk via de homepage van de Inzameling van Gegevens als openbare bèta.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Raadpleeg de <a href="../push/mobile-onboarding-wf.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nieuw journaal (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> Het dashboard Journey is nu gesplitst in twee tabbladen:</p>
<ul><li>Gebruik de <strong>Overzicht</strong> om toegang te krijgen tot een nieuw dashboard dat belangrijke metriek met betrekking tot uw reizen toont.</li>
<li>Gebruik de <strong>Bladeren</strong> voor toegang tot de lijst van alle reizen.</li></ul>
<p>Deze mogelijkheid is toegankelijk voor alle reizen als een openbare bètaversie.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Raadpleeg de <a href="../building-journeys/journey-gs.md#journey-access">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#april-2023-improvements}

**Journeys**

* Het reiscanvas geeft nu de activiteit-id weer op berichtactiviteiten en eindtags. Dit verbetert rapportage en heroriëntering.
* De indeling van het configuratievenster, dat wordt weergegeven in handelingen, gegevensbronnen, gebeurtenissen en reizen, is verbeterd.
* Nieuw inzicht in het aantal knooppunten op het canvas met beveiligingen om mee te groeien: maak reizen gemakkelijk te lezen, QA en los problemen op met een maximum aantal knooppunten per reis bij 50. [Meer informatie](../start/guardrails.md#journeys-guardrails-journeys)
* Wanneer u een [E-mail](../email/create-email.md), [SMS](../sms/create-sms.md) of [Push](../push/create-push.md) tijdens een reis wordt het oppervlak standaard voorgevuld met het laatst gebruikte oppervlak voor dat kanaal, in de huidige reis.
* U kunt nu statische of dynamische queryparameters definiëren in uw aangepaste handelingen. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)

**Rapportage**

* U kunt nu Journey Optimizer-rapporten exporteren als PDF. [Meer informatie](../reports/global-report.md#export-reports)

**Content Designer**

* De Adobe Journey Optimizer Content Designer is bijgewerkt en de toegang tot ontwerpstijlen en -componenten is nu eenvoudiger. Deze nieuwe versie biedt een verbeterde gebruikerservaring en wordt geleverd met verbeterde prestaties, gedeeltelijke compatibiliteit met donkere modi en ondersteuning voor nieuwe toegankelijkheidsstandaarden.



## Opmerkingen bij de release maart 2023 {#mar-2023}

### Nieuwe functies{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Kanaal in de app (algemene beschikbaarheid)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu binnen een campagne persoonlijke In-app-berichten naar gebruikers van de app sturen. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Raadpleeg de <a href="../in-app/get-started-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS-klik bijhouden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met SMS klikt het volgen, kunt u de prestaties van uw verkorte URLs controleren, identificeren wie op hen klikte, en deze gegevens gebruiken om die klanten met verdere campagnes opnieuw te richten.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Raadpleeg de <a href="../sms/create-sms.md#sms-content">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tags gebruiken in uw reizen (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Journey Optimizer-expert kunt u uw zakelijke objecten nu organiseren met tags. Met tags kunt u objecten snel en eenvoudig classificeren om zoekopdrachten te verbeteren. Deze functie is momenteel beschikbaar in bèta en alleen voor reizen.</p>
<p>Raadpleeg de <a href="../start/search-filter-categorize.md#tags">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#mar-2023-improvements}

**Journeys**

* De nieuwe **Throttling API** Hiermee kunt u een limiet instellen voor het aantal gebeurtenissen dat per seconde wordt verzonden, zodat overweldigende verkeersspikes op uw externe systemen of API worden voorkomen. Wanneer de ingestelde limiet is bereikt, worden alle volgende API-aanroepen zo snel mogelijk in de wachtrij geplaatst en verwerkt in de volgorde waarin ze zijn ontvangen. Houd er rekening mee dat deze functie slechts ondersteuning biedt voor één configuratie met vertraagde verwerking van al uw sandboxen. [Meer informatie](../configuration/external-systems.md)
* Het canvas Journey is verbeterd voor een eenvoudigere en verbeterde gebruikerservaring. Aan het einde van elk pad op het canvas zijn de lege plaatsaanduidingen verwijderd. U kunt nu gewoon uw activiteiten toevoegen door deze aan het einde van een pad te slepen.
* In het reiscanvas, het etiket van **Einde** -tag wordt niet meer automatisch ingesteld met de naam van de vorige activiteit. Gebruikers kunnen desgewenst handmatig een aangepast label toevoegen.
* De standaardonderbreking en foutenduur in reiseigenschappen zijn veranderd van 5 aan 30 seconden. [Meer informatie](../configuration/external-systems.md#timeout)
* De standaardsnelheid voor het wijzigen van het aantal berichten voor het publiek is gewijzigd van 20.000 in 5.000 berichten per seconde. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Er is een hulplijn toegevoegd aan de testmodus om alleen te luisteren naar gebeurtenissen die via de interface worden verzonden. Er wordt geen rekening gehouden met gebeurtenissen die via een extern gereedschap worden verzonden. [Meer informatie](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Beslissingsbeheer**

* Om mogelijke verwarring met de recente versie van tags in Adobe Experience Platform te voorkomen, zijn de namen van Beslissingsbeheertags gewijzigd in &quot;Verzamelingsaanduidingen&quot;.

  Hoewel de term &quot;tag&quot; niet meer wordt gebruikt in de gebruikersinterface van het besluitvormingsbeheer, wordt deze nog steeds gebruikt in back-endservices zoals API&#39;s en datasets.

* U kunt de teller van de aanbieding nu op een dagelijkse, wekelijkse of maandelijkse basis terugstellen. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

* U kunt ook kiezen naar welke Adobe Experience Platform-gebeurtenis moet worden gezocht om de offer decisioning te beperken. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

* Er zijn aanvullende parameters toegevoegd aan het scherm Plaatsingsontwerp. Hiermee kunt u bepalen of een aanbieding op meerdere plaatsen kan worden gedupliceerd en kunt u opgeven of de inhoud en metagegevens van de aanbieding moeten worden opgenomen in de API-reactie. [Meer informatie](../offers/offer-library/creating-placements.md)

**Personalisatie**

* U kunt nu standaardterugvaltekst voor op tekenreeks gebaseerde profielkenmerken opnemen in de Expressieeditor. Deze waarden worden weergegeven als de geselecteerde kenmerken geen resultaat opleveren. [Meer informatie](../personalization/personalization-build-expressions.md#add)

**Rapportage**

* De functionaliteit van de widget voor rapportage is verbeterd en het is nu mogelijk om aan te passen hoe gebruikers hun gegevens bekijken. Met deze verbetering kunnen gebruikers nu kiezen tussen meerdere visualisatieopties, zoals grafiek, tabel en donutgrafieken.

  Als u toegang wilt hebben tot de meest recente widgets, moet u de verschillende rapportdashboards opnieuw instellen. Raadpleeg voor meer informatie over het aanpassen van het dashboard de [gedetailleerde documentatie](../reports/global-report.md#modify-dashboard).

## Opmerkingen bij de release van februari 2023 {#feb-2023}

### Nieuwe functies{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Kanaal in app (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu binnen een campagne persoonlijke In-app-berichten naar gebruikers van de app sturen. Met Journey Optimizer kunt u meldingen ontwerpen en de lay-out, weergave, tekst en knoppen van berichten aanpassen voor een naadloze ervaring.</p>
<p><strong>Waarschuwing</strong> - Deze functie is momenteel in bètaversie beschikbaar voor bètaklanten. Neem contact op met de klantenservice van de Adobe om deel te nemen aan het bètaprogramma.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Raadpleeg de <a href="../in-app/get-started-in-app.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer-gegevenssets exporteren naar cloudopslagdoelen (bèta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren. Beschikbare bestemmingen zijn: Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP.</p>
<p><strong>Waarschuwing</strong> - Deze functie is momenteel in bèta beschikbaar voor alle Adobe Journey Optimizer-gebruikers. Werk samen met uw Adobe als u nog geen toegang hebt tot Doelen.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Raadpleeg de <a href="../data/export-datasets.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Verbeteringen {#feb-2023-improvements}

**Journeys**

* De **Wachttijd bij terugkeer** het veld is toegevoegd aan de eigenschappen van de reis . In dit veld kunt u de tijd definiëren die u moet wachten voordat u een profiel toestaat om de reis opnieuw te betreden tijdens een enkele reis (te beginnen met een evenement of een publiekskwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. [Meer informatie](../building-journeys/journey-gs.md#entrance)

* Er zijn verbeteringen doorgevoerd voor **begin- en einddatum van de reis**. Als u geen begindatum hebt opgegeven, wordt deze nu automatisch toegevoegd op het moment van publicatie. Voor **Lees publiek** voor reizen kunt u nu een einddatum toevoegen. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt. [Meer informatie](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Beheer**

* **Lijst van gewenste personen** - U kunt de lijst van gewenste personen nu downloaden als een CSV-bestand. [Meer informatie](../configuration/allow-list.md#download-allowed-list)

* **E-mailoppervlak** - Er is een extra controle toegevoegd aan de instellingen van het e-mailoppervlak: als de MX-record voor het subdomein dat wordt gebruikt in het dialoogvenster **Reageren op (e-mailadres)** of in de **BCC-e-mailadres** is niet behoorlijk gevormd, kan de e-mailoppervlakte niet meer worden gecreeerd. U moet het gevormd hebben of een andere gebruiken. [Meer informatie](../email/email-settings.md#reply-to-email)

* **E-mailoppervlak** - In de **Parameters voor URL-tracking** sectie van de instellingen van het e-mailoppervlak, de limiet voor elke **Waarde** Het veld is bijgewerkt van 255 tekens naar 5 kB ten behoeve van compatibiliteit met Adobe Analytics-tracking. [Meer informatie](../email/email-settings.md#url-tracking)

**Beslissingsbeheer**

* **Plaatsen** - Er zijn aanvullende parameters toegevoegd aan het scherm voor het maken van plaatsingen. Hiermee kunt u bepalen of een aanbieding op meerdere plaatsen kan worden gedupliceerd en kunt u opgeven of de inhoud en metagegevens van de aanbieding moeten worden opgenomen in de API-reactie. [Meer informatie](../offers/offer-library/creating-placements.md)

* **URL-personalisatie** - Wanneer u URL&#39;s als inhoud toevoegt aan de representaties van uw aanbiedingen, kunt u deze URL&#39;s nu aanpassen met de Expressieeditor. [Meer informatie](../offers/offer-library/add-representations.md)

## Opmerkingen bij de release januari 2023{#jan-2023-release}

### Nieuwe functies{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Gegevenshygiëne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform biedt een reeks mogelijkheden voor gegevenshygiëne waarmee u uw opgeslagen gegevens kunt beheren via programmatische verwijderingen van consumentengegevens en gegevenssets. Deze mogelijkheid is nu beschikbaar voor Adobe Journey Optimizer. </p>
<p>U kunt uw gegevensopslag beheren om ervoor te zorgen dat de informatie wordt gebruikt zoals verwacht, wordt bijgewerkt wanneer onjuiste gegevens het bevestigen vereisen, en wordt geschrapt wanneer het organisatorische beleid het noodzakelijk acht.</p>
<p><strong>Waarschuwing</strong> - Gegevenshygiëne-mogelijkheden zijn momenteel alleen beschikbaar voor organisaties die de <strong>Gezondheidsschild</strong> en <strong>Privacy- en beveiligingsschild</strong> add-on aanbiedingen.</p><p>Raadpleeg de <a href="../privacy/data-hygiene.md">gedetailleerde documentatie</a> voor meer informatie.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-mailinhoudssjablonen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu zelfstandige inhoudssjablonen maken die u kunt gebruiken voor reizen en campagnes voor snel hergebruik.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Leer hoe u inhoudssjablonen kunt maken, bewerken en gebruiken in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">deze video</a>. Raadpleeg de <a href="../content-management/content-templates.md">gedetailleerde documentatie</a> voor meer informatie.
</p>
</td>
</tr>
</tbody>
</table>

### Verbeteringen {#jan-2023-improvements}

**Journeys**

* Wanneer u een **kwalificatie publiek** of **Lees publiek** in een reis, wordt namespace nu vooraf gevuld, door gebrek, met het laatst gebruikte namespace. Zie de [kwalificatie publiek](../building-journeys/audience-qualification-events.md#about-segment-qualification) en [Lees publiek](../building-journeys/read-audience.md#configuring-segment-trigger-activity) secties.

* Op het reiscanvas is er een nieuwe knop beschikbaar op de werkbalk waarmee u een schermafbeelding van uw reis kunt downloaden.

**Email Designer**

* U kunt de e-mailinhoud nu exporteren vanuit de **HTML exporteren** -menu. Geëxporteerde bestanden zijn beschikbaar in een ZIP-bestand (archiefbestand).

**Beheer**

* Een nieuwe subsectie bevat aanbevelingen voor het opbouwen van de **Reageren op (e-mail)** het adresseren en waarborgen van een adequaat antwoordbeheer. [Meer informatie](../email/email-settings.md#reply-to-email)

* Bij het maken of bewerken **IP-pools**, worden de bijbehorende PTR- verslagen nu getoond in de IP lijst en wanneer het hangen over de geselecteerde IP adressen. [Meer informatie](../configuration/ip-pools.md#create-ip-pool)

* Nadat een IP pool in een kanaaloppervlakte is geselecteerd, is PTR- verslaginformatie nu zichtbaar wanneer het bedekken over de IP adressen. [Meer informatie](../email/email-settings.md#subdomains-and-ip-pools)

* De gebruikersinterface voor bewerken [PTR-records](../configuration/ptr-records.md#edit-ptr-record) en [uitvoeringsvelden](../configuration/primary-email-addresses.md) is bijgewerkt.

* De gebruikersinterface voor het maken en bewerken van subdomeinen is verbeterd. [Meer informatie](../configuration/delegate-subdomain.md)

* De onderdrukkingslijst **Recente uploads** scherm is bijgewerkt. [Meer informatie](../configuration/manage-suppression-list.md#recent-uploads)

**Campagnes**

* Er wordt nu automatisch een voorbeeld van een cURL-aanvraag gegenereerd die uitvoering van door de API geïnitieerde campagnes toestaat, en beschikbaar gesteld in het campagnescherm. [Meer informatie](../campaigns/api-triggered-campaigns.md)


**Personalisatie**

* Er zijn nieuwe hulpfuncties beschikbaar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber en toHexString. Bovendien accepteert de functie toDateTimeOnly nu tekenreekstypen, datumvelden, lange en int-veldtypen. [Meer informatie](../personalization/functions/functions.md)
