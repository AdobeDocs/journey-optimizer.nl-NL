---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met campagnes
description: Meer informatie over campagnes in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campagne, hoe, begin, optimaliseer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: cebb21aba29a15236b6810309efc488b578a1ca6
workflow-type: tm+mt
source-wordcount: '1533'
ht-degree: 0%

---

# Aan de slag met campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Campagne"
>abstract="De campagnes beginnen standaard bij handmatige activering en eindigen direct nadat het bericht eenmaal is verzonden. U hebt de flexibiliteit om een specifieke datum en tijd voor het te verzenden bericht te plaatsen. Bovendien kunt u een einddatum voor terugkerende campagnes van de Actie specificeren. In de triggers van Actie kunt u de verzendfrequentie van berichten ook configureren om deze aan te passen aan uw voorkeuren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Start campagne"
>abstract="Geef een datum en tijd op waarop het bericht moet worden verzonden."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Einde campagne"
>abstract="Geef op wanneer een terugkerende campagne moet stoppen met uitvoeren."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="actieftriggers voor campagne"
>abstract="Definieer de frequentie waarmee het campagnebericht moet worden verzonden."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Snelheidbeheersing"
>abstract="Plaats de controle van het Tarief voor uw campagne door de gewenste tariefgrenzen te specificeren. Deze functie is vooral handig om overbelasting op downstreamsystemen, zoals pagina&#39;s voor landingen of platforms voor klantenservice, te voorkomen."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Campagnes maken"
>abstract="Gebruik **Adobe Journey Optimizer** om eenmalige inhoud aan een specifiek publiek te leveren gebruikend diverse kanalen. Wanneer u reizen gebruikt, worden handelingen op volgorde uitgevoerd. Met campagnes, worden de acties uitgevoerd gelijktijdig, of onmiddellijk, of gebaseerd op een gespecificeerd programma."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Maak campagnes om eenmalige inhoud aan een specifiek publiek op verschillende kanalen te leveren. Voordat u uw campagne maakt, moet u ervoor zorgen dat u een kanaalconfiguratie hebt en een Adobe Experience Platform-publiek klaar voor gebruik."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type campagne"
>abstract="Selecteer het type campagne. Welke kanalen beschikbaar zijn, is afhankelijk van het geselecteerde type. <br>**Geplande campagnes** (de campagnes van de Actie) - Ideaal voor eenvoudige, eenmalig partijmededelingen die u kunt plannen om in een specifieke tijd te lopen.<br>**API teweeggebrachte campagnes** - geactiveerd door een API vraag, toelatend geautomatiseerd, op gebeurtenis-gebaseerd overseinen direct van externe systemen.<br>**Geordende campagnes** - verstrek een visueel, belemmering-en-dalingscanvas om complexe, multi-step marketing werkschema&#39;s te ontwerpen en te automatiseren, van publiekssegmentatie aan gepersonaliseerde berichtlevering over kanalen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campagnes"
>abstract="Maak uw segmentatiestroom, maak uw berichten over meerdere kanalen en plan uw campagnes. Ondersteunde kanalen: e-mail, SMS, pushmelding."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campagnes"
>abstract="Lever enige of terugkomende uitgaande leveringen of lopende binnenkomende acties."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campagnes"
>abstract="Lever enige of terugkomende uitgaande transactionele acties."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campagnes"
>abstract="Aangepaste marketingcommunicatie leveren aan doelgroepen. Ondersteunde kanalen: e-mail, sms, pushberichten."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campagnes"
>abstract="Transactiecommunicatie leveren aan afzonderlijke profielen of groepen profielen. Ondersteunde kanalen: e-mail, sms, pushberichten."

Met Adobe Journey Optimizer kunt u doelgerichte, eenmalige inhoud leveren aan specifieke doelgroepen op meerdere kanalen. Met behulp van campagnes kunt u gecoördineerde marketingacties gelijktijdig uitvoeren, zodat u uw publiek op het juiste moment bereikt met de juiste boodschap.

Deze gids verstrekt een duidelijke roadmap om u te helpen campagnegrondbeginselen begrijpen, het juiste campagnetype voor uw gebruiksgeval kiezen, en vertrouwend ontwerpcampagnes die onwrikbare klantenervaringen leveren.

## Wat zijn campagnes?

**campagnes** zijn gecoördineerde marketing acties die inhoud aan een specifiek publiek over één of meerdere kanalen leveren. In tegenstelling tot reizen waar de acties opeenvolgend uitvoeren, voeren de campagnes gelijktijdig-of onmiddellijk of op een bepaald programma uit.

Gebruik [!DNL Journey Optimizer] om:

* Lever **eenmalig of terugkomende inhoud** aan gerichte publiekssegmenten
* Voer **gecoördineerde multi-kanaalmededelingen** over e-mail uit, duw, SMS, in-app, Web, en meer
* Trigger **geautomatiseerde reacties** via API vraag naar real time, gebeurtenis-gedreven overseinen
* Het ontwerp **complexe marketing werkschema&#39;s** met visuele orchestratiehulpmiddelen

![](assets/gs-campaigns.png)

➡️ **Klaar om te beginnen met bouwen?** [&#x200B; creeer uw eerste campagne &#x200B;](create-campaign.md) in notulen.

## Kies het type campagne {#campaign-types}

**alvorens u begint te bouwen**, is het belangrijk om te begrijpen welk type van campagne uw gebruiksgeval past. Adobe Journey Optimizer ondersteunt drie soorten campagnes, elk ontworpen voor verschillende scenario&#39;s en activeringsmechanismen:

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB  campagnes van de Actie (Gepland) ]

**wanneer te gebruiken:** Eenvoudige, geplande partijmededelingen

**campagnes van de Actie** (die ook als Geplande campagnes worden bekend) zijn ideaal voor ongecompliceerde, eenmalige of terugkomende partijmededelingen die in een specifieke tijd lopen.

**Twee categorieën:**

* **Marketing** - de aanbiedingen van de bevordering, betrokkenheidscampagnes, aankondigingen, wettelijke berichten, of beleidsupdates. Ontvangers moeten worden ingeschakeld.
* **Transactionele** - Verstoringen, noodgevallen, annuleringen. Geen opt-in vereist.

**Perfect voor:**

* Maandelijkse nieuwsbrieven naar klantsegmenten
* Tijdgevoelige promotieaankondigingen
* Seizoensgebonden marketingcampagnes
* Productlanceringen
* Meldingen over verstoring van de service

➡️ [&#x200B; Leer over de campagnes van de Actie &#x200B;](create-campaign.md)

>[!TAB  API teweeggebrachte campagnes ]

**wanneer te gebruiken:** Real-time, gebeurtenis-gedreven overseinen met externe systemen

**API-teweeggebrachte campagnes** activeren door API vraag, toelatend geautomatiseerd overseinen direct van externe systemen. Deze campagnes steunen verpersoonlijking gebruikend zowel profielattributen als contextgegevens in real time van de API lading.

**Twee categorieën:**

* **Marketing** - Gepersonaliseerde marketing mededelingen aan gericht publiek
* **Transactie** - Berichten die individuele acties volgen (wachtwoordterugstelt, kartaankopen, enz.)

**Perfect voor:**

* Bevestigingen voor opnieuw instellen van wachtwoord
* Terugwinning van winkelwagentjes
* Bevestigingen van bestellingen en verzendupdates
* Meldingen over accountactiviteiten
* Persoonlijke aanbevelingen in realtime

➡️ [&#x200B; Leer over API-teweeggebrachte campagnes &#x200B;](api-triggered-campaigns.md)

>[!TAB  Geordende campagnes ]

**wanneer te gebruiken:** Complexe, multi-step marketing werkschema&#39;s

**Geordende campagnes** verstrekken een visueel, belemmering-en-dalingscanvas om verfijnde marketing werkschema&#39;s te ontwerpen en te automatiseren. Van publiekssegmentatie tot gepersonaliseerde berichtlevering over kanalen, gebeurt alles in één intuïtieve die milieu voor snelheid en controle wordt gebouwd.

**Perfect voor:**

* Meerdere uitstapprogramma&#39;s voor klantenservice
* Complexe segmentering en gerichte strategieën
* Kanaaloverschrijdende campagneorchestratie
* Door het merk geïnitieerde marketing op schaal
* Geavanceerde workflowautomatisering met meerdere beslissingspunten

➡️ [&#x200B; Leer over Geordende campagnes &#x200B;](../orchestrated/gs-orchestrated-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>Weet u niet zeker welk type u wilt kiezen? Begin met **campagnes van de Actie** voor geplande partijmededelingen of **API-teweeggebrachte campagnes** voor overseinen-deze behandelen gemeenschappelijkste gebruiksgevallen in real time.

## Uw workflow voor het maken van campagnes {#workflow}

De bouw van succesvolle campagnes volgt een duidelijk, herhaalbaar proces. Dit is uw stapsgewijze workflow:

**1. Plan** → **2. Vorm** → **3. Ontwerp** → **4. Overzicht** → **5. Activeer** → **6. Monitor**

### &#x200B;1. **Plan uw campagne** {#plan}

Geef voordat u begint aan welke doelen u wilt bereiken:

* **wat is het doel?** (bijvoorbeeld schijfconversies, betrokkenheid vergroten, klanten op de hoogte stellen)
* **Wie is het publiek?** (bv. bouwen of selecteren vanuit Adobe Experience Platform)
* **Welk campagnetype past?** (Zie [&#x200B; campagneretypes &#x200B;](#campaign-types) hierboven)
* **Welke kanalen zult u gebruiken?** (e-mail, duw, SMS, in-app, Web, enz.) → [&#x200B; zie gesteunde kanalen door campagnetype &#x200B;](../channels/gs-channels.md#channels)
* **wanneer zou het moeten uitvoeren?** (direct, gepland of API-geactiveerd)

### &#x200B;2. **vorm campagneeigenschappen** {#configure}

Stel de basis voor uw campagne in:

1. **Naam en beschrijf** uw campagne voor gemakkelijke identificatie
2. **Uitgezochte campagnetype** (Handeling, API-teweeggebracht, of Geordend)
3. **kies uw publiek**
4. **Vastgestelde prioriteit** als het gebruiken van conflictbeheer
5. **vorm programma** (voor campagnes van de Actie) of API details (voor API-teweeggebracht)

**Type-Specifieke gidsen:**
* [Eigenschappen van handelscampagne →](campaign-properties.md)
* [API-gestuurde campagneeigenschappen →](api-triggered-campaign-properties.md)
* [Instellingen geordende campagne →](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;3. **Ontwerp uw inhoud** {#design}

Maak aansprekende berichten voor uw publiek:

* Gebruik **E-mail Designer** voor rijke e-mailervaringen
* Vorm **duw berichten** met beelden en diepe verbindingen
* Ontwerp **SMS/MMS berichten** met verpersoonlijking
* Creeer **in-app** en **Web** ervaringen
* Voeg **verpersoonlijking** toe gebruikend profielattributen en contextuele gegevens

**Type-Specifieke gidsen:**
* [Inhoud van de campagne →](campaign-content.md)
* [API-activering van campagne-inhoud →](api-triggered-campaign-content.md)
* [Geordende campagneinhoud →](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;4. **Overzicht en test** {#review}

Controleer altijd uw campagne voordat u de activering uitvoert:

* **inhoud van de Voorproef** met testprofielen
* **Controle richtend** om het juiste publiek te verzekeren
* **verifieer programma** en activeringsmontages
* **Goedkeuring van het Verzoek** als het gebruiken van het goedkeuringswerkschema
* **leverbaarheid van de Test** met zaadlijsten

**Type-Specifieke gidsen:**
* [Actiecampagnes redigeren →](review-activate-campaign.md)
* [API-gestuurde campagnes controleren →](review-activate-api-triggered-campaign.md)
* [Geordende campagnes controleren →](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;5. **activeer uw campagne** {#activate}

Activeer uw campagne als de revisie is voltooid:

* **Handmatige activering** - activeer onmiddellijk of op geplande tijd
* **API activering** - voor API-teweeggebrachte campagnes, gebruik het activeringseindpunt
* **proces van de Goedkeuring** - indien vereist, wacht op goedkeuring van de belanghebbende
* Opmerking: actieve campagnes kunnen niet worden bewerkt (u moet dupliceren om wijzigingen aan te brengen)

**Type-Specifieke gidsen:**
* [Actiecampagnes activeren →](review-activate-campaign.md)
* [API-gestuurde campagnes activeren →](review-activate-api-triggered-campaign.md)
* [Geordende campagnes activeren →](../orchestrated/create-orchestrated-campaign.md)

### &#x200B;6. **Monitor en analyseer** {#monitor}

Houd bij hoe uw campagne presteert:

* Campagnerapporten en analyses weergeven
* Bewaking van de leverings- en betrokkenheidscijfers
* Fouten en grenzen bijhouden
* Conversie en ROI analyseren
* Inzichten gebruiken voor optimalisatie

**Type-Specifieke gidsen:**
* [Campagnerapporten van acties →](../reports/campaign-global-report-cja.md)
* [API-activering van campagnerebewaking →](api-triggered-campaigns.md#monitor)
* [Geordende campagneanalytica →](../orchestrated/create-orchestrated-campaign.md)

➡️ **Klaar om te beginnen?** Kies het type campagne:
* [Handelingscampagne →](create-campaign.md)
* [API-gestuurde campagne maken →](api-triggered-campaigns.md)
* [Geordende campagne maken →](../orchestrated/gs-orchestrated-campaigns.md)

## Vereisten {#prerequisites}

Voordat u met campagnes gaat werken, moet u het volgende controleren:

### Vereiste installatie

* **Soorten publiek** - de Soorten van het publiek moeten in Adobe Experience Platform beschikbaar zijn alvorens campagnes te creëren. [&#x200B; worden begonnen met publiek → &#x200B;](../audience/about-audiences.md)

* **configuraties van het Kanaal** - de configuraties van het Kanaal (vooraf instelt) moeten worden gecreeerd en beschikbaar voor de kanalen u wilt gebruiken. [&#x200B; de configuraties van het het kanaal van de opstelling →](../configuration/channel-surfaces.md)

* **Toestemmingen** - u hebt aangewezen toestemmingen nodig die op het campagnetype worden gebaseerd. Neem contact op met de beheerder als u geen toegang hebt tot campagnefuncties. [&#x200B; leer over ingebouwde rollen → &#x200B;](../administration/ootb-product-profiles.md)

| Type campagne | Machtigingen |
|----------------------------|----------------------------------------------------------------------------|
| **campagnes van de Actie** | De beheerder van de campagne <br> Campagne goedkeurde &lbrace;<br> Manager van de Campagne <br> de kijker van de Campagne |
| **API teweeggebrachte campagnes** | De beheerder van de campagne <br> Campagne goedkeurde &lbrace;<br> Manager van de Campagne <br> de kijker van de Campagne |
| **Geordende campagnes** | De geordende Beheerder van de Campagne <br> Geordende Begeleidende fiatteur van de Campagne &lbrace;<br> Geordende Manager van de Campagne <br> Geordende Kijker van de Campagne |

+++Campagnemachtigingen toewijzen

1. Navigeer naar het tabblad **[!UICONTROL Roles]** in het [!DNL Permissions] -product en selecteer een van de ingebouwde campagnebestanden **[!UICONTROL Roles]** .

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

   Als de gebruiker niet eerder werd gecreeerd, verwijs naar [&#x200B; gebruikersdocumentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/users){target="_blank"} toevoegen.

Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

+++

## Campagne-mogelijkheden {#capabilities}

Terwijl u comfortabeler bent met campagnes, verkent u de volgende krachtige mogelijkheden:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=nl-NL)

**Plannend &amp; timing**

Plan campagnes voor specifieke datums/tijden, stel terugkerende leveringen in en optimaliseer verzendtijden voor maximale impact.

[Meer informatie over plannen](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=nl-NL)

**de controle van het Tarief**

Beperk berichtendoorvoer om overbelasting op downstreamsystemen zoals het landen van pagina&#39;s of platforms voor de klantenservice te voorkomen.

[Grenswaarden voor regeltarieven](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=nl-NL)

**Publiek richtend**

Doelspecifiek Adobe Experience Platform-publiek nauwkeurig instellen en de publiekskwalificaties dynamisch beheren.

[Campagnepubliek selecteren](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=nl-NL)

**de werkschema&#39;s van de Goedkeuring**

Evaluatie- en goedkeuringsprocessen uitvoeren voordat campagnes live gaan, zodat kwaliteit en naleving gewaarborgd zijn.

[Controleren en activeren](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=nl-NL)

**stille uren**

Eerbiedig klantenvoorkeur door berichtlevering tijdens gespecificeerde tijdvensters te vermijden.

[Stille uren configureren](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=nl-NL)

**Send-time optimalisering**

Gebruik AI om de beste tijd te bepalen om berichten voor maximumovereenkomst met elke individu te verzenden.

[Verzendtijd optimaliseren](campaigns-message-optimization.md)
:::

::::

## Aan de slag met campagneretypen {#get-started-types}

Nu u campagnes begrijpt in [!DNL Journey Optimizer] , kiest u het type campagne dat u wilt starten:

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="actieplannen" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Actiecampagnes</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API-actiecampagnes</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="duwen" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Geordende campagnes</a></td>
</tr></table>
