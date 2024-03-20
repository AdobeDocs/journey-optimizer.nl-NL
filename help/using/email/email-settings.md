---
solution: Journey Optimizer
product: journey optimizer
title: E-mailinstellingen configureren
description: Leer hoe u e-mailinstellingen op het niveau van het kanaaloppervlak configureert
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '2314'
ht-degree: 0%

---

# E-mailinstellingen configureren {#email-settings}

Als u een e-mailbericht wilt maken, moet u oppervlakken van e-mailkanalen instellen die alle technische parameters definiëren die vereist zijn voor uw berichten. [Leer hoe u oppervlakken maakt](../configuration/channel-surfaces.md)

>[!NOTE]
>
>Als u uw reputatie wilt behouden en de leverbaarheid wilt verbeteren, stelt u de subdomeinen in die u wilt gebruiken voor het verzenden van e-mails voordat u een e-mailoppervlak maakt. [Meer informatie](../configuration/about-subdomain-delegation.md)

Definieer de e-mailinstellingen in de specifieke sectie van de configuratie van het kanaaloppervlak, zoals hieronder wordt beschreven.

![](assets/preset-email-settings.png)

De configuratie van de e-mailoppervlakte wordt opgepikt voor het verzenden van mededelingen die de logica hieronder volgen:

* Voor batchritten is deze code niet van toepassing op batchuitvoering die al was gestart voordat de configuratie van het e-mailoppervlak is gemaakt. De wijzigingen worden opgepikt bij de volgende herhaling of nieuwe uitvoering.

* Voor transactieberichten, wordt de verandering onmiddellijk voor de volgende mededeling (tot vijf minuten vertraging) opgepikt.

>[!NOTE]
>
>De bijgewerkte instellingen van het e-mailoppervlak worden automatisch opgehaald tijdens de reis(en) of campagne(s) waar het oppervlak wordt gebruikt.

## Type e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="De e-mailcategorie definiëren"
>abstract="Selecteer het type e-mailberichten dat wordt verzonden wanneer u dit oppervlak gebruikt: marketing voor speciale e-mails waarvoor toestemming van de gebruiker vereist is of Transactie voor niet-commerciële e-mails die ook in specifieke contexten naar profielen zonder abonnement kunnen worden verzonden."

In de **E-MAILTYPE** selecteert u het type bericht dat met het oppervlak wordt verzonden: **[!UICONTROL Marketing]** of **[!UICONTROL Transactional]**.

* Kies **Marketing** voor speciale e-mails, zoals wekelijkse promoties voor een winkel. Voor deze berichten is toestemming van de gebruiker vereist.

* Kies **Transactioneel** voor niet-commerciële e-mail, zoals bevestiging van de bestelling, wachtwoordherstelmeldingen of leveringsgegevens. Deze e-mails kunnen worden verzonden naar profielen die **geabonneerd** van marketingberichten. Deze berichten kunnen alleen in specifieke contexten worden verzonden.

Wanneer u een bericht maakt, moet u een geldig kanaaloppervlak kiezen dat overeenkomt met de categorie die u voor uw e-mail hebt geselecteerd.

## Subdomein- en IP-pools {#subdomains-and-ip-pools}

In de **Subdomein- en IP-pools** in, vult de vereiste velden in zoals hieronder beschreven.

1. Selecteer het subdomein dat u wilt gebruiken om de e-mails te verzenden.

   Om de reputatie van uw domein te bewaren, versnelt het IP opwarmingsproces en verbetert leverbaarheid, uw verzendende subdomeinen aan Adobe delegeren. [Meer informatie](../configuration/about-subdomain-delegation.md)

1. Selecteer de IP pool om met de oppervlakte te associëren. [Meer informatie](../configuration/ip-pools.md)

   ![](assets/preset-subdomain-ip-pool.png)

   U kunt niet met oppervlakverwezenlijking te werk gaan terwijl de geselecteerde IP pool onder is [editie](../configuration/ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status) en is nooit gekoppeld aan het geselecteerde subdomein. Anders, zal de oudste versie van de IP pool/subdomain vereniging nog worden gebruikt. Als dit het geval is, sparen de oppervlakte als ontwerp en probeer opnieuw zodra de IP pool heeft **[!UICONTROL Success]** status.

   >[!NOTE]
   >
   >Voor niet-productiemilieu&#39;s, leidt de Adobe niet uit-van-de-doos testsubdomeinen noch verleent toegang tot een gedeelde verzendende IP pool. U moet [delegeren uw eigen subdomeinen](../configuration/delegate-subdomain.md) en gebruik IPs van de pool die aan uw organisatie wordt toegewezen.

1. Nadat een IP pool is geselecteerd, is de informatie PTR zichtbaar wanneer het hangen over de IP adressen onder de IP pool drop-down lijst wordt getoond. [Meer informatie over PTR-records](../configuration/ptr-records.md)

   ![](assets/email-surface-ptr-record.png)

   >[!NOTE]
   >
   >Als een PTR-record niet is geconfigureerd, neemt u contact op met uw Adobe.

## List-Unsubscribe {#list-unsubscribe}

Aan [selecteren, subdomein](#subdomains-and-ip-pools) in de lijst **[!UICONTROL Enable List-Unsubscribe]** weergegeven.

![](assets/preset-list-unsubscribe.png)

Deze optie is standaard ingeschakeld.

Als u deze optie ingeschakeld laat, wordt automatisch een afmeldingskoppeling opgenomen in de e-mailkoptekst, zoals:

![](assets/preset-list-unsubscribe-header.png)

Als u deze optie uitschakelt, wordt er geen koppeling voor afmelden weergegeven in de e-mailkoptekst.

De unsubscribe-koppeling bestaat uit twee elementen:

* An **e-mailadres opzeggen**, waarnaar alle afmeldingsverzoeken worden verzonden.

  In [!DNL Journey Optimizer], is het e-mailadres voor opzeggen het standaardadres **[!UICONTROL Mailto (unsubscribe)]** adres dat in de kanaaloppervlakte wordt getoond, die op [geselecteerd subdomein](#subdomains-and-ip-pools).

  ![](assets/preset-list-unsubscribe-mailto.png)

* De **abonnement-URL opzeggen**, dit is de URL van de bestemmingspagina waarop de gebruiker wordt omgeleid wanneer deze het abonnement opzegt.

  Als u een [one-click opt-out link](../privacy/opt-out.md#one-click-opt-out) voor een bericht dat is gemaakt met dit oppervlak, is de URL voor het afmelden van een abonnement de URL die is gedefinieerd voor de koppeling om één muisklik uit te schakelen.

  ![](assets/preset-list-unsubscribe-opt-out-url.png)

  >[!NOTE]
  >
  >Als u geen koppeling om te weigeren met één klik toevoegt aan uw berichtinhoud, wordt er geen bestemmingspagina weergegeven voor de gebruiker.

Meer informatie over het toevoegen van een link voor opzeggen van koptekst aan je berichten in [deze sectie](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parameters koptekst {#email-header}

In de **[!UICONTROL Header parameters]** in, voert u de namen en e-mailadressen van de afzender in die zijn gekoppeld aan het type e-mail dat met dat oppervlak is verzonden.

* **[!UICONTROL Sender name]**: De naam van de afzender, zoals de naam van uw merk.

* **[!UICONTROL Sender email]**: Het e-mailadres dat u voor uw communicatie wilt gebruiken.

* **[!UICONTROL Reply to (name)]**: De naam die wordt gebruikt wanneer de ontvanger op de knop **Antwoord** in hun e-mailclientsoftware.

* **[!UICONTROL Reply to (email)]**: Het e-mailadres dat wordt gebruikt wanneer de ontvanger op de knop **Antwoord** in hun e-mailclientsoftware. [Meer informatie](#reply-to-email)

* **[!UICONTROL Error email]**: Alle fouten die door ISPs na een paar dagen van post worden geproduceerd die (asynchrone stuitingen) worden ontvangen op dit adres. De out-of-office berichten en de uitdagingsreacties worden ook ontvangen op dit adres.

  Als u de meldingen buiten het kantoor wilt ontvangen en reacties wilt uitdagen op een specifiek e-mailadres dat niet is gedelegeerd aan de Adobe, moet u een [voorwaarts proces](#forward-email). Zorg er in dat geval voor dat u een handmatige of geautomatiseerde oplossing hebt waarmee de e-mailberichten die in deze Postvak IN worden geplaatst, kunnen worden verwerkt.

>[!CAUTION]
>
>De **[!UICONTROL Sender email]** en **[!UICONTROL Error email]** adressen moeten de huidige geselecteerde gebruiken [gedelegeerd subdomein](../configuration/about-subdomain-delegation.md). Als het gedelegeerde subdomein bijvoorbeeld *marketing.luma.com* kunt u *contact@marketing.luma.com* en *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>Adressen moeten beginnen met een letter (A-Z) en mogen alleen alfanumerieke tekens bevatten. U kunt ook het onderstrepingsteken gebruiken `_`, punt`.` en afbreekstreepje `-` tekens.

### E-mail beantwoorden {#reply-to-email}

Bij het definiëren van de **[!UICONTROL Reply to (email)]** adres, kunt u om het even welk e-mailadres specificeren op voorwaarde dat het een geldig adres, in correct formaat en zonder enige typefout is.

Het inbox dat voor antwoorden wordt gebruikt, ontvangt alle e-mails met reacties, behalve meldingen buiten het kantoor en antwoorden op de vraag, die worden ontvangen op de **[!UICONTROL Error email]** adres.

Volg onderstaande aanbevelingen om te zorgen voor een goed antwoordbeheer:

* Zorg ervoor dat de toegewezen Postvak IN voldoende ontvangstcapaciteit heeft om alle e-mails met reacties te ontvangen die via het e-mailoppervlak worden verzonden. Als het postvak &#39;Bounces&#39; retourneert, worden sommige reacties van uw klanten mogelijk niet ontvangen.

* De reacties moeten worden verwerkt met inachtneming van de verplichtingen inzake privacy en naleving, aangezien zij persoonlijk identificeerbare informatie (PII) kunnen bevatten.

* Merk geen berichten als spam in antwoordinbox, aangezien het alle andere reacties zal beïnvloeden die naar dit adres worden verzonden.

Bovendien, wanneer het bepalen van **[!UICONTROL Reply to (email)]** adres, zorg ervoor om subdomain te gebruiken die een geldige MX verslagconfiguratie heeft, anders zal de verwerking van de e-mailoppervlakte ontbreken.

Als u een fout bij het voorleggen van de e-mailoppervlakte krijgt, betekent het dat het MX- verslag niet voor subdomain van het adres wordt gevormd u inging. Contacteer uw beheerder voor het vormen van het overeenkomstige MX verslag of gebruik een ander adres met een geldige MX verslagconfiguratie.

>[!NOTE]
>
>Als het subdomein van het adres u inging een domein is dat [volledig gedelegeerd](../configuration/delegate-subdomain.md#full-subdomain-delegation) als u Adobe wilt, neemt u contact op met de accountmanager van uw Adobe.

### E-mail doorsturen {#forward-email}

Alle e-mails ontvangen door doorsturen naar een specifiek e-mailadres [!DNL Journey Optimizer] voor het gedelegeerde subdomein, contacteer de Zorg van de Klant van de Adobe.

>[!NOTE]
>
>Als het subdomein wordt gebruikt voor de **[!UICONTROL Reply to (email)]** Het adres wordt niet gedelegeerd aan Adobe, door:sturen kan niet voor dit adres werken.

U moet het volgende opgeven:

* Het e-mailadres van uw keuze. Merk op dat het voorwaartse domein van het e-mailadres geen subdomein kan aanpassen dat aan Adobe wordt gedelegeerd.
* De naam van uw sandbox.
* De oppervlaknaam of subdomein waarvoor het voorwaartse e-mailadres zal worden gebruikt.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel surface level.-->

>[!NOTE]
>
>Per subdomein kan slechts één voorwaarts e-mailadres aanwezig zijn. Als meerdere oppervlakken hetzelfde subdomein gebruiken, moet voor alle oppervlakken hetzelfde e-mailadres worden gebruikt.

Het e-mailadres voor verzending wordt ingesteld door Adobe. Dit kan 3 tot 4 dagen duren.

Zodra gedaan, alle berichten die op worden ontvangen **[!UICONTROL Reply to (email)]** en **[!UICONTROL Error email]** adressen worden doorgestuurd naar het specifieke e-mailadres dat u hebt opgegeven.

## BCC-e-mail {#bcc-email}

U kunt een identieke kopie (of blinde koolstofkopie) van e-mails verzenden die zijn verzonden door [!DNL Journey Optimizer] naar een BCC-postvak waar ze worden opgeslagen voor compatibiliteits- of archiefdoeleinden.

Om dit te doen, laat toe **[!UICONTROL BCC email]** optionele functie op het niveau van het kanaaloppervlak. [Meer informatie](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Bovendien, wanneer het bepalen van **[!UICONTROL Bcc email]** adres, zorg ervoor om subdomain te gebruiken die een geldige MX verslagconfiguratie heeft, anders zal de verwerking van de e-mailoppervlakte ontbreken.

Als u een fout bij het voorleggen van de e-mailoppervlakte krijgt, betekent het dat het MX- verslag niet voor subdomain van het adres wordt gevormd u inging. Contacteer uw beheerder voor het vormen van het overeenkomstige MX verslag of gebruik een ander adres met een geldige MX verslagconfiguratie.

## Verzenden naar onderdrukt e-mailadressen {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="Prioriteit suppressielijst overschrijven"
>abstract="U kunt ook transactiemeldingen verzenden naar profielen, zelfs als hun e-mailadres op de suppressielijst voor Adobe Journey Optimizer staat vanwege een spamklacht. Deze optie is standaard uitgeschakeld."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html" text="De vervolgkeuzelijst beheren"

>[!IMPORTANT]
>
>Deze optie is alleen beschikbaar als u **[!UICONTROL Transactional]** e-mailtype. [Meer informatie](#email-type)

In [!DNL Journey Optimizer], worden alle e-mailadressen die zijn gemarkeerd als harde stuiteringen, zachte stuiteringen en spamklachten, automatisch verzameld in de [onderdrukkingslijst](../configuration/manage-suppression-list.md) en van een reis of een campagne zijn uitgesloten.

U kunt echter besluiten door te gaan met het verzenden van berichten van de **transactie** typen naar profielen, zelfs als hun e-mailadressen op de suppressielijst staan vanwege een spamklacht van de gebruiker.

Transactieberichten bevatten over het algemeen nuttige en verwachte informatie, zoals een orderbevestiging of een wachtwoordherstelmelding. Daarom zelfs als zij één van uw marketing berichten als spam hebben gemeld, het grootste deel van de tijd wilt u uw klanten dit type van niet-commerciële e-mail ontvangen.

Als u e-mailadressen wilt opnemen die zijn onderdrukt als gevolg van een spamklacht in het publiek van het transactiebericht, selecteert u de desbetreffende optie in het menu **[!UICONTROL Send to suppressed email addresses]** sectie.

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>Deze optie is standaard uitgeschakeld.

Deze optie is standaard uitgeschakeld als best practice voor de te leveren items. Zo weet u zeker dat er geen contact wordt opgenomen met uw klanten die ervoor hebben gekozen dit niet te doen. Nochtans, kunt u deze standaardoptie veranderen, die u dan toestaat om transactieberichten naar uw klanten te verzenden.

Zodra deze optie wordt toegelaten, hoewel een klant uw marketing e-mail als spam merkte, zal die klant uw transactiemeldingen kunnen ontvangen gebruikend de huidige oppervlakte. Zorg er altijd voor dat de voorkeuren voor weigeren worden beheerd in overeenstemming met de best practices voor prestaties.

## Zaadlijst {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Een zaadlijst toevoegen"
>abstract="Selecteer de zaadlijst van uw keus om specifieke interne adressen aan uw publiek automatisch toe te voegen. Deze zaadadressen zullen op de tijd van de leveringsuitvoering worden omvat en zullen een nauwkeurige kopie van het bericht voor betrouwbaarheidsdoeleinden ontvangen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="Wat zijn zaadlijsten?"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#create-seed-list" text="Een zaadlijst maken"


Een zaadlijst in [!DNL Journey Optimizer] kunt u automatisch specifieke e-mailadressen toevoegen aan uw leveringen. [Meer informatie](../configuration/seed-lists.md)

>[!CAUTION]
>
>Deze functie is momenteel alleen van toepassing op het e-mailkanaal.

Selecteer de lijst die voor u relevant is in het dialoogvenster **[!UICONTROL Seed list]** sectie. Leer hoe u een zaadlijst maakt in [deze sectie](../configuration/seed-lists.md#create-seed-list).

![](../configuration/assets/seed-list-surface.png)

>[!NOTE]
>
>Er kan slechts één zaadlijst tegelijk worden geselecteerd.

Wanneer de huidige oppervlakte in een campagne of reis wordt gebruikt, zijn de e-mailadressen op de geselecteerde zaadlijst inbegrepen bij de leveringstijd, die zij een exemplaar van de levering voor verzekeringsdoeleinden zullen ontvangen.

Leer hoe u de lijst met voorvertoningen gebruikt in een campagne of een reis in [deze sectie](../configuration/seed-lists.md#use-seed-list).

## Parameters opnieuw proberen {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="De periode voor het opnieuw proberen aanpassen"
>abstract="Retries worden 3,5 dagen (84 uur) uitgevoerd wanneer een e-maillevering mislukt als gevolg van een tijdelijke soft bounce-fout. U kunt deze standaardperiode voor opnieuw proberen aanpassen aan uw wensen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html" text="Opnieuw proberen"

U kunt de **Parameters opnieuw proberen**.

![](assets/preset-retry-parameters.png)

Standaard worden de [periode voor opnieuw uitproberen](../configuration/retries.md#retry-duration) is ingesteld op 84 uur, maar u kunt deze instelling aanpassen aan uw wensen.

U moet een geheel-getalwaarde (in uren of notulen) binnen de volgende waaier ingaan:

* Voor het in de handel brengen van e-mails is de minimale herroepingstermijn 6 uur.
* Voor transactie-e-mailberichten is de minimale herroepingstermijn 10 minuten.
* Voor beide e-mailtypen is de maximale hergebruiksperiode 84 uur (of 5040 minuten).

Meer informatie over nieuwe pogingen in [deze sectie](../configuration/retries.md).

## URL-tracking {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parameters voor URL-tracking definiëren"
>abstract="Met deze sectie kunt u automatisch parameters voor bijhouden toevoegen aan de URL&#39;s in uw e-mailinhoud. Deze functie is optioneel."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Voorvertoning van parameters voor URL bijhouden"
>abstract="Bekijk hoe u parameters voor bijhouden toevoegt aan de URL&#39;s in uw e-mailinhoud."

U kunt **[!UICONTROL URL tracking parameters]** om de doeltreffendheid van uw marketing inspanningen over kanalen te meten. Deze functie is optioneel.

De parameters die in deze sectie worden gedefinieerd, worden toegevoegd aan het einde van de URL&#39;s die in de inhoud van uw e-mailbericht zijn opgenomen. Vervolgens kunt u deze parameters vastleggen in hulpprogramma&#39;s voor webanalyse, zoals Adobe Analytics of Googles Analytics, en verschillende prestatierapporten maken.

U kunt maximaal 10 volgparameters toevoegen met de functie **[!UICONTROL Add new parameter]** knop.

![](assets/preset-url-tracking.png)

Als u een URL-volgparameter wilt configureren, kunt u rechtstreeks de gewenste waarden invoeren in het dialoogvenster **[!UICONTROL Name]** en **[!UICONTROL Value]** velden.

U kunt ook elke **[!UICONTROL Value]** veld met de [Expressieeditor](../personalization/personalization-build-expressions.md). Klik op het pictogram van de editie om de editor te openen. Vervolgens kunt u de beschikbare contextafhankelijke kenmerken selecteren en/of de tekst rechtstreeks bewerken.

![](assets/preset-url-tracking-editor.png)

De volgende vooraf gedefinieerde waarden zijn beschikbaar via de Expressieeditor:

* **Id van handeling Bron**: ID van de e-mailactie die aan de reis of campagne is toegevoegd.

* **Naam van bronhandeling**: naam van de e-mailactie die aan de reis of campagne is toegevoegd.

* **Bron-id**: ID van de reis of campagne waarnaar de e-mail is verzonden.

* **Bronnaam**: naam van de reis of campagne waarnaar de e-mail is verzonden.

* **Id van bronversie**: ID van de reis- of campagneversie waarmee de e-mail is verzonden.

* **Offerte-id**: ID van het voorstel dat in de e-mail wordt gebruikt.

>[!NOTE]
>
>U kunt tekstwaarden typen en contextafhankelijke kenmerken gebruiken in de Expressieeditor. Elk **[!UICONTROL Value]** mag een aantal tekens bevatten tot maximaal 5 kB.

<!--You can drag and drop the parameters to reorder them.-->

Hieronder staan voorbeelden van URL&#39;s die compatibel zijn met Adobe Analytics en Googles Analytics.

* URL die compatibel is met Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Compatibele URL voor Googles Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

U kunt de resulterende URL voor bijhouden dynamisch voorvertonen. Elke keer dat u een parameter toevoegt, bewerkt of verwijdert, wordt de voorvertoning automatisch bijgewerkt.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>U kunt ook dynamische parameters voor gepersonaliseerde reeksspatiëring toevoegen aan de koppelingen in uw e-mailinhoud, maar dit is niet mogelijk op oppervlakteneniveau. Dit moet u doen wanneer u uw bericht ontwerpt met de e-mailontwerper. [Meer informatie](message-tracking.md#url-tracking)
