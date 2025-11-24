---
solution: Journey Optimizer
product: journey optimizer
title: Inhoudsaanwijzing voor AI Assistant
description: Leer hoe u effectieve herinneringen voor het genereren van inhoud door AI maakt met behulp van het CO-STAR-framework voor het maken van marketinginhoud met een hoge conversie en een merkgebonden bestemming.
role: User
level: Intermediate
source-git-commit: bacfe2e04898e8417308e3f1c889214547e3ea02
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 0%

---


# AI Assistant: tips en trucs {#ai-assistant-prompting-guide}

Deze gids helpt u uw verzoeken structureren, intent met duidelijkheid communiceren, en ervoor zorgen AI overseinen produceert die zich op uw merkrichtlijnen, publieksbehoeften, en campagnedoelstellingen richten.
Leer hoe u effectieve herinneringen schrijft waarmee AI Assistant kwalitatief hoogwaardige, on-brand marketinginhoud kan genereren die is afgestemd op uw doelstellingen.

## Het CO-STAR-kader gebruiken {#costar-framework}

U bereikt de beste resultaten met AI Assistant door uw vragen te ordenen met behulp van het CO-STAR-framework. Deze gestructureerde aanpak zorgt ervoor dat AI precies begrijpt wat u nodig hebt.

| Component | Wat het betekent | Waarom het belangrijk is |
|-|-|-|
| **C - Context** | Achtergrond van uw campagne, product of situatie | Helpt AI het grotere beeld te begrijpen |
| **O - Doelstelling** | Uw specifieke marketingdoelstelling | Stuurt wat de inhoud moet bereiken |
| **S - Stijl** | Hoe u wilt communiceren | Hiermee wordt de methode ingesteld |
| **T - Toon** | Emotionele stijl en stem | Vormt hoe uw bericht zich voelt |
| **A - Publiek** | Doelgroep | Zorgt ervoor dat het bericht op de juiste mensen past |
| **R - Vereisten** | Specifieke beperkingen of must-haves | Definieert grenzen en kritieke elementen |

## AI-aanwijzingen {#key-takeaways}


### Doen en niet


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Do</th>
<th>Niet doen</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Gebruik van het CO-STAR-kader voor structuur</p>
<p>Wees expliciet over verse versus bestaande inhoud</p>
<p>Gebruik van Focus-documenten met specifieke extractiehulplijnen</p>
<p>Vervolgkeuzeselecties gebruiken voor toon, strategie en landinstelling</p>
<p>Commerciële doelstellingen afstemmen op inhoudstype-mogelijkheden</p>
<p>Meerdere varianten genereren voor A/B-tests</p>
</td>
<td>
<p>Vragen om structurele wijzigingen, opmaak of beeldbewerking in aanwijzingen</p>
<p>Meningstoon/strategie in aanwijzingen, indien beschikbaar in dropdowns</p>
<p>Gebruik vage doelstellingen als "promoten van ons product"</p>
<p>Selecties voorwaardelijk element aanvragen</p>
<p>Layoutwijzigingen via vragen verwachten</p>
</td>
</tr>
</tbody>
</table>

### Inhoud niet ondersteund in aanwijzingen

>[!TIP]
>
>Gebruik de **e-mailredacteur** of **Adobe Express** voor visuele/beeldwijzigingen.

Deze verzoeken worden niet ondersteund en moeten via andere tools worden afgehandeld:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>Wijzigingen in e-mailstructuur ✕</th>
<th>Wijzigingen in visuele opmaak ✕</th>
<th>Beeldbewerkingen ✕</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Te wijzigen specifieke secties selecteren</li>
<li>Elementen verwijderen of klonen</li>
<li>Voorwaardelijke selecties</li>
<li>Schermindelingssecties toevoegen of verwijderen</li>
</ul>
</td>
<td>
<ul>
<li>Tekstopmaak (vet, cursief, lettergrootte)</li>
<li>Kleurwijzigingen</li>
<li>Indelingsstijl (randen, opvulling, marges)</li>
<li>Visuele effecten (schaduwen)</li>
</ul>
</td>
<td>
<ul>
<li>Wijzigingen in achtergrond</li>
<li>Tekstbedekkingen of logo's toevoegen</li>
<li>Afbeeldingen uitsnijden of vergroten/verkleinen</li>
<li>Kleuraanpassingen</li>
<li>Vervanging afbeelding</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Kwaliteitscontrolelijst {#quality-checklist}

Controleer voordat u inhoud genereert het volgende:

&controle; **Duidelijke doelstelling**: verklaart duidelijk de actie, het product/de dienst, de waarde, en de context.

&controle; **Gedefinieerd doelpubliek**: Specificeert de demografisch, de rol, of het segment.

&controle; **het type van Inhoud groepering**: De doelstelling past het geselecteerde kanaal of het formaat aan.

&controle; **gevormde Dropdown selecties**: De toon, de strategie, en de scène worden gekozen, omvatten hen niet in de herinnering.

&controle; **gespecificeerde nadruk van het Document**: benadrukt welke inhoud of secties aan verwijzing.

&controle; **toegepaste Merk**: De aangewezen merkrichtlijnen worden geselecteerd.

&controle; **Realistisch werkingsgebied**: Vermijd verzoeken om lay-outveranderingen, het stileren, of structurele geeft uit.

## Effectieve marketingdoelstellingen schrijven {#marketing-objectives}

### Wees specifiek en actiegericht

Zorg er bij het ontwerpen van marketingdoelstellingen voor dat deze duidelijk, handelbaar en meetbaar zijn. Vermijd vage of algemene verklaringen.

**Voorbeelden van goede doelstellingen:**

&check; &quot;Drive sign-ups voor onze gratis proefversie van 30 dagen van het nieuwe AI-dashboard voor analysemogelijkheden&quot;

&check; &quot;Genereer leads voor ons B2B-webinar over &#39;Reducing Cloud Costs by 40%&#39; dat op 15 maart plaatsvindt&quot;

&check; &quot;Onze beperkte vakantiekorting voor 25% verhogen op premieabonnementen, die 25 december eindigt&quot;

**Voorbeelden om te vermijden:**

✕ &quot;Ons product promoten&quot; (te vaag)

✕ &quot;Zorg dat mensen dingen kopen&quot; (onduidelijke waarde)

✕ &quot;E-mail over nieuwe functies&quot; (heeft geen doel)

### Uw doel structureren

Geef altijd context en waardevoorstel op, zodat AI relevante inhoud kan genereren.
Gebruik deze formule om u te helpen efficiënte doelstellingen schrijven: **Actie + Product/Dienst + Waarde/Voordeel + Urgentie/Context**

**Voorbeelden van goede doelstellingen:**

&check; &quot;Aanmoedig downloads van onze nieuwe mobiele app die gebruikers helpt bij het volgen van duurzame leefgewoonten met gepersonaliseerde eco-vriendelijke aanbevelingen&quot;

&check; &quot;Registratie bevorderen voor onze exclusieve workshop over geavanceerde technieken voor gegevensvisualisatie voor marketingprofessionals&quot;

&check; &quot;Aanwezigheid op station voor de introductie van ons product toont de revolutionaire AI-schrijfassistent die meer dan 5 uur per week bespaart&quot;

**Voorbeelden om te vermijden:**

✕ &quot;Nieuwe app bekendmaken&quot; (waardevoorstel en context ontbreken)

✕ &quot;Laat mensen zich aanmelden voor een workshop&quot; (heeft geen specifieke kenmerken van publiek en voordeel)

✕ &quot;Gebeurtenis bevorderen&quot; (geen duidelijke actie, waarde of urgentie)

## Nieuwe inhoud maken versus bestaande inhoud wijzigen {#new-vs-modify}

Geef duidelijk aan of uw verzoek betrekking heeft op het genereren van nieuwe inhoud of het bijwerken van bestaand materiaal. Dit onderscheid is belangrijk omdat het de AI begeleidt bij het kiezen van de juiste aanpak en een nauwkeuriger en bruikbaarder resultaat garandeert.

### Nieuwe inhoud maken

Deze strategie toepassen wanneer u marketingcampagnes start, nieuwe producten onthult of een bijgewerkte of vernieuwde communicatie start. Het zorgt ervoor dat uw boodschap sterk begint en op uw doelen wordt afgestemd.

**hoe te om** te veroorzaken ➤ wanneer het creëren van nieuwe inhoud, nadruk op uw marketing doelstelling zonder bestaande inhoud van verwijzingen te voorzien.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **Proefversie SaaS**: &quot;lanceer onze nieuwe software van CRM aan kleine bedrijfseigenaars, die 50% tijdbesparingen, 90% snellere loodkwalificatie benadrukken, en het aanbieden van een 30 dagen vrije proef met gepersonaliseerd onboarding&quot;
* **de aankondiging van de Eigenschap**: &quot;kondig nieuwe API integratiemogelijkheden aan die ontwikkelingstijd door 60% voor ondernemingsklanten verminderen, richtend technische besluitvormers&quot;
* **Bevordering van de Gebeurtenis**: &quot;De registraties van de aandrijving voor ons webinar op &quot;Digitale Marketing Trends 2024&quot;kenmerkend deskundigen van Google, Meta, en Adobe, benadrukkend actionable inzichten en beperkte plaatsen (maximum 500)&quot;

>[!ENDSHADEBOX]

### Bestaande inhoud wijzigen

>[!TIP]
>
>Voor standaardwijzigingen zoals uitwerken, vatten samen, of vereenvoudigen, gebruik **verfijnen** eigenschap in plaats van douaneherinneringen te schrijven. [Meer informatie](generative-uc.md##refine)

Pas dit toe wanneer u uw huidige marketingcampagnes moet bijwerken, vernieuwen of aanpassen. Deze methode steunt stijgende verbeteringen, die uw overseinen verzekeren relevant blijft zonder van kras te beginnen.

**hoe te om** te veroorzaken ➤ wanneer het wijzigen van bestaande inhoud, specificeer duidelijk wat u en hoe te het veranderen wilt.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **de Campagne verfrist zich**: &quot;wijzig de productlancering e-mail om zich op de eigenschappen van de ondernemingsveiligheid in plaats van algemene productiviteitsvoordelen te concentreren, richtend de besluitvormers van IT met nalevingscertificatie&quot;
* **Pieksprivot van het publiek**: &quot;Pas onze uitnodiging van de softwaredemo aan om gezondheidszorg specifiek te richten, die generische voorbeelden met de gevallen van het gezondheidszorggebruik en de nalevingsvoordelen van HIPAA vervangen&quot;
* **seizoensgebonden update**: &quot;Werk onze promotiecampagne Q3 voor Q4 vakantiewinkelen bij, veranderend nadruk van terug aan school aan vakantiecadeau die met snelle het verschepen nadruk geeft&quot;

>[!ENDSHADEBOX]

## Verbeter uw vraag met geavanceerde montages {#personalize-prompt}

### Typen communicatiestrategie

>[!TIP]
>
>Gebruik het vervolgkeuzemenu Communicatiestrategie in het menu Tekstinstellingen in plaats van deze te vermelden in de vraag naar gespecialiseerde verwerking.

Uw communicatiestrategie bepaalt hoe u uw boodschap presenteert om de impact te maximaliseren. De verschillende strategieën werken beter voor verschillende doelstellingen, of u urgentie bouwt, vertrouwen vestigt, of drijft directe actie. Kies de strategie die het beste aansluit bij uw campagnedoelstellingen en doelgerichtheid.

| **Strategie** | **Best voor** | **de Stijl van het Overseinen** | **Voorbeelden** |
|--------------|--------------|------------------------|--------------|
| **Dringend** | Tijdgevoelige aanbiedingen, termijnen, onmiddellijke actie | Creeert directe druk met op tijd-gebaseerde taal | &quot;Nu handelen: de aanbieding verloopt om middernacht&quot; <br> &quot;Nu registreren voordat steunkleuren worden gevuld&quot; <br> &quot;48-uurs Flash-verkoop begint nu&quot; |
| **FOMO (Angst om uit te ontbreken)** | Beperkte aanbiedingen, evenementen, exclusieve toegang | Gebruikt aanwijzingen voor urgentie, schaarste en tijdsdruk | &quot;Nog maar 24 uur over! Beperkte voorraad van 40% korting <br> &quot;Last choice: Early vogel pricing ends future&quot; <br> &quot;Only 100 beta spots remaining&quot; |
| **Sociale Bewijs** | Betrouwbaarheidsopbouw, getuigenissen, populaire producten | Gebruikt ervaringen en validatie van anderen | &quot;Word 50.000+ tevreden klanten&quot; <br> &quot;Rated 4.9/5 stars by Industry professional&quot; <br> &quot;Trusted by Fortune 500 companies&quot; |
| **Scarcity** | Beperkte voorraad, exclusieve releases, producten van hoge vraag | Benadrukt beperkte beschikbaarheid en exclusiviteit | &quot;Slechts 5 items in voorraad&quot; <br> &quot;Beperkte editie: 100 eenheden beschikbaar&quot; <br> &quot;Exclusieve release: First come, first serving&quot; |
| **Stimulerend** | Promoties, beloningsprogramma&#39;s, speciale aanbiedingen | Belangrijkste tastbare voordelen en beloningen | &quot;Maak 20% korting op uw eerste bestelling&quot; <br> &quot;Verdien dit weekend dubbele punten&quot; <br> &quot;Gratis verzending voor bestellingen van meer dan $50&quot; |
| **Exclusiviteit** | Premium producten, VIP-ervaringen, alleen voor leden | Gebruikt premiumpositionering en taal voor speciale toegang | &quot;Exclusieve uitnodiging voor onze persoonlijke voorvertoning&quot; <br> &quot;Elite-lidmaatschap ontgrendelt geavanceerde analysemogelijkheden&quot; <br> &quot;Sluit u aan bij geselecteerde Fortune 500-bedrijven die ons al gebruiken&quot; |
| **Gamification** | Betrokkenheidscampagnes, loyaliteitsprogramma&#39;s, interactieve inhoud | Gebruikt spelmechanica en prestatietaal | &quot;Ontgrendel je volgende bonusniveau&quot; <br> &quot;Volledige uitdagingen om badges te verdienen&quot; <br> &quot;Beklimm het spelersbord voor exclusieve prijzen&quot; |
| **Informatief** | Onderwijs, onderzoek, complexe producten, gedachteleiding | Gebruikt feiten, gegevens, inzichten en uitleg | &quot;5 inzichten van het analyseren van 10.000+ interacties&quot; <br> &quot;Nieuw onderzoek onthult 3 doorbraakbenaderingen&quot; <br> &quot;Volledige gids voor het implementeren van AI in marketing&quot; |
| **Onderwijs &amp; Inzichten** | Leerinhoud, trends in de branche, beste praktijken | Biedt waardevolle kennis en activeerbare taken | &quot;Geniet van geavanceerde technieken met onze handleiding voor experts&quot; <br> &quot;Ontdek 7 strategieën die veel marketeers gebruiken&quot; <br> &quot;Leer hoe u uw workflow in 5 stappen kunt optimaliseren&quot; |

### De juiste toon instellen {#tone}

>[!TIP]
>
>Gebruik het keuzemenu Kleurtint in het menu Tekstinstellingen in plaats van deze op te geven in de vraag.

Tint bepaalt hoe de doelgroep uw boodschap waarneemt en reageert. Selecteer altijd een tint die is afgestemd op uw stem van het merk en het werkgebied van de profielreis.

Gebruik de onderstaande tabel om elke toon in detail te bekijken, inclusief wanneer deze het beste werkt en voorbeelden van inhoud die in elke stijl past.

| Tonaliteit | Best voor | Voorbeeld van inhoud |
|-|-|-|
| Professional | B2B-communicatie, formele aankondigingen | &quot;We zijn blij om ons strategisch partnerschap aan te kondigen...&quot; |
| Empathetisch | Klantenondersteuning, gevoelige onderwerpen | &quot;Wij begrijpen hoe frustrerend dit voor u moet zijn...&quot; |
| Enorm | Campagnes, verlichte inhoud | &quot;Waarschuwing: kan tot aanzienlijke productiviteitswinst leiden!&quot; |
| Opwindend | Productlanceringen, gebeurtenispromoties | &quot;Dit is het moment waarop je hebt gewacht!&quot; |
| Inspiratie | Motiviteitscampagnes, merkdoel | &quot;Samen kunnen we een verschil maken in de wereld...&quot; |
| Persuasiet | Verkoopcampagnes, conversies | &quot;Mis deze beperkte kans niet aan...&quot; |
| vriendelijk | Klantenservice, welkomstberichten | &quot;We zijn zo blij dat je hier bij ons bent!&quot; |
| Formeel | Juridische mededelingen, officiële aankondigingen | &quot;Hierbij stellen wij u in kennis van de volgende wijzigingen...&quot; |
| Apologetisch | Serviceterugwinning, probleemoplossing | &quot;Onze excuses voor het ongemak...&quot; |
| Assertief | Leaderinhoud, gezaghebbende overseinen | &quot;Dit is wat je nu moet doen...&quot; |
| Verteller | Merkverhalen, emotionele verbindingen | &quot;Het begon allemaal met een simpele vraag...&quot; |
| Gesprek | Nuratiecampagnes, relatieopbouw | &quot;Laten we praten over hoe dit je kan helpen...&quot; |

### De middelen van uw merk optimaliseren {#brand-assets}

>[!TIP]
>
>Als u reeds een merkactiva door het **Merk Assets** menu hebt geüpload, te hoeven u niet om het in uw herinnering van verwijzingen te voorzien. Het systeem gebruikt automatisch geselecteerde documenten.

Brand-elementen bieden feitelijke informatie die uw gegenereerde inhoud verrijkt met specifieke, nauwkeurige details.
Wanneer u brede documenten zoals productbrochures uploadt, voeg aan uw herinnering toe welke delen om zich op te concentreren:

* **in plaats van** _&quot;Gebruik de productbrochure&quot;_ **u** _&quot;concentreert zich op de geavanceerde veiligheidseigenschappen en nalevingscertificatie, specifiek SOC 2 naleving en gegevensencryptie&quot;zou moeten gebruiken_

* **in plaats van** _&quot;Verwijzing de casestudies&quot;_ **u** _zou moeten gebruiken &quot;de resultaten van ROI van het Hoogtepunt van gezondheidszorgcliënten, specifiek de 40% kostenvermindering bij Regionaal Medisch Centrum&quot;_

* **in plaats van** _&quot;omvat technische details&quot;_ **zou u** _moeten gebruiken &quot;Benadruk API integratiemogelijkheden en ontwikkelaarsvoordelen, zich het concentreren op REST API eindpunten en 99.9% uptime SLA&quot;_

### Inhoud verfijnen

>[!TIP]
>
>Gebruik de functie Verfijnen in plaats van te vragen wanneer u bestaande inhoud wilt uitwerken, samenvatten, vereenvoudigen, de toon wijzigen of vertalen. [Meer informatie](generative-uc.md#refine)

Zodra de inhoud wordt geproduceerd, gebruik **verfijnen** eigenschap om het met de volgende opties te herhalen en te verbeteren:

| **Actie** | **Geval van het Gebruik** | **Vragen Voorbeeld** |
|-|-|-|
| **Uitwerken** | Voeg diepte en detail toe aan korte inhoud | &quot;Uitwerken van de technische voordelen van onze beveiligingsfuncties&quot; |
| **vat** samen | Condente lange inhoud voor verschillende indelingen | &quot;Overzicht van dit product weergeven voor een bericht op sociale media&quot; |
| **vereenvoudigt** | Complexe inhoud toegankelijker maken | &quot;Vereenvoudig deze technische uitleg voor een algemeen publiek&quot; |
| **Toon van de Verandering** | Inhoud aanpassen voor verschillende soorten publiek | &quot;De toon van de verandering in casual voor jongere demografie&quot; |
| **transcreate** | Culturele aanpassing na vertaling | &quot;Deze campagne doorlichten voor de Japanse markt&quot; |

## Promptvoorbeelden op basis van scenario&#39;s

### Gebaseerd op inhoudstype {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Kanaal</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Email</strong></td>
<td>"De vooruitzichten van de onderneming van de genezing door drie klanten succesverhalen met gedetailleerde ROI metriek te tonen (IBM: 45% kostenvermindering, Accenture: 200% loodverhoging, Microsoft: 60% tijdbesparingen), richtend de directeuren van IT bij bedrijven met 1000+ werknemers."</td>
</tr>
<tr>
<td><strong>Sms</strong></td>
<td>"VIP-klanten waarschuwen voor een 4-uurs flash-verkoop op premiumelektronica met een korting van 40%, beperkt tot de eerste 100 klanten"</td>
</tr>
<tr>
<td><strong>Pushmeldingen</strong></td>
<td>"Neem opnieuw contact op met gebruikers die de app in 7 dagen nog niet hebben geopend met aanbevelingen voor persoonlijke inhoud op basis van hun leesgeschiedenis."</td>
</tr>
<tr>
<td><strong>Landingspagina's</strong></td>
<td>"Zet B2B-bezoekers om in gekwalificeerde leads door aan te tonen hoe onze oplossing voor bedrijfsbeveiliging 99,9% van de cyberaanvallen voorkomt, met Fortune 500-getuigenissen en gratis veiligheidscontrole"</td>
</tr>
</tbody>
</table>

### Gebaseerd op sectorspecifieke benaderingen {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industrie</th>
<th>Voorbeeld vragen</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B-technologie</strong></td>
<td>"Toon ROI en technische specificaties aan terwijl het richten van veiligheidszorgen voor de besluitvormers van IT die onze oplossing van de wolkeninfrastructuur evalueren, benadrukkend 99.9% uptime SLA, SOC 2 naleving, en 40% kostenbesparingen."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Maak urgentie rond vakantieproducten met beperkte voorraad en benadruk gratis verzending en eenvoudige retourzendingen voor kopers op het laatste moment, waarbij de nadruk ligt op beperkte hoeveelheden (minder dan 50 resterende) en verzendkosten van 24 uur."</td>
</tr>
<tr>
<td><strong>Financiële diensten</strong></td>
<td>"Voorlichten van klanten over strategieën voor de diversificatie van hun beleggingsportefeuille met behoud van de naleving van de regelgeving, met daarin kennis van gecertificeerde financiële adviseurs en risicodisclaimers."</td>
</tr>
<tr>
<td><strong>Gezondheidszorg en Wellness</strong></td>
<td>"Bevorderen van de voordelen van preventieve zorg en jaarlijkse gezondheidsonderzoeken met behoud van de medische nauwkeurigheid, met aanbevelingen voor door het moederbord gecertificeerde artsen en waarborgen voor de privacy van patiënten."</td>
</tr>
<tr>
<td><strong>Onderwijs en training</strong></td>
<td>"Benadruk de resultaten van loopbaanvooruitgang en de industriecertificeringen terwijl het tonen van instructeursdeskundigheid, benadrukkend 92% baanplaatsingstarief en op project-gebaseerd leerplan."</td>
</tr>
<tr>
<td><strong>SaaS-platforms</strong></td>
<td>"Benadruk tijdbesparingen en automatiseringsvoordelen met specifieke metriek terwijl het richten van integratiezorgen, die gemiddelde wekelijkse tijdbesparingen van 25 uur en integratie met 200+ populaire hulpmiddelen voorzien."</td>
</tr>
</tbody>
</table>
