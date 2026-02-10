---
solution: Journey Optimizer
product: journey optimizer
title: Reistypen en selectiehandleiding
description: Vergelijk de verschillende soorten reizen en kies de juiste keuze voor uw gebruiksscenario met beslissingshulplijnen en de compatibiliteitsmatrix voor functies
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: reistypes, unitary, leest publiek, publiekskwalificatie, bedrijfsgebeurtenis, vergelijking, beslissingsgids, kiezen, selectie, real time, gepland, partij, gebeurtenis-teweeggebracht
version: Journey Orchestration
hide: true
hidefromtoc: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# Reistypen en selectiehandleiding {#journey-types-selection}

[!DNL Adobe Journey Optimizer] ondersteunt vier soorten reizen, elk ontworpen voor verschillende toegangsmechanismen en bedrijfsscenario&#39;s. Deze handleiding helpt u de verschillen te begrijpen en het juiste type voor uw gebruikscase te kiezen.

## Overzicht van reistypes {#journey-types}

>[!BEGINTABS]

>[!TAB  Eenheids reizen ]

**wanneer te gebruiken:** Real-time, gebeurtenis-teweeggebrachte ervaringen

**de eenheidstrajecten** worden teweeggebracht individueel wanneer een specifieke actie (aankoop, app login, vormvoorlegging) voorkomt. Profielen worden een voor een ingevoerd in real-time ingevoerd, waardoor dit ideaal is voor directe, op gedrag gebaseerde reacties.

**Perfect voor:** Bevestigingen van de Orde na aankoop, welkome e-mails wanneer iemand zich abonneert, wortelbeëindiging teweeggebracht door het doorbladeren, en wachtwoord terugstellende berichten.

➡️ [ Leer over gebeurtenissen ](../event/about-events.md) | [ Bericht aan abonnees gebruikt geval ](message-to-subscribers-uc.md)

>[!TAB  lees de reizen van het Publiek ]

**wanneer te gebruiken:** Geplande campagnes aan publiekssegmenten

**lees de reizen van het Publiek** beginnen met een [!DNL Adobe Experience Platform] publiek en verzendt berichten in partij naar alle profielen gelijktijdig. Dit type van reis is ideaal voor geplande, grootschalige mededelingen.

**Perfect voor:** Maandelijkse nieuwsbrieven, promotiecampagnes aan doelsegmenten, productaankondigingen, en seizoensgebonden marketing campagnes.

➡️ [ Leer over Gelezen Publiek ](read-audience.md) | [ krijgen begonnen met publiek ](../audience/about-audiences.md)

>[!TAB  reizen van de Kwalificatie van het publiek ]

**wanneer te gebruiken:** Reacties in real time aan de veranderingen van het publiekslidmaatschap

**de reizen van de Kwalificatie van het publiek** teweegbrengen wanneer de profielen voor (of uitgang uit) een specifiek publiek kwalificeren. Profielen worden afzonderlijk ingevoerd als ze in real-time aan de criteria voldoen, zodat ze direct in contact kunnen komen wanneer het gedrag van de klant verandert.

**Perfect voor:** de de rijverbeteringsberichten van VIP, re-engagement wanneer de klanten inactief worden, eerste de berichten van de aankoopviering, en geografisch gericht richten wanneer de klanten zich bewegen.

➡️ [ Leer over de Kwalificatie van het Publiek ](audience-qualification-events.md) | [ Creërend publiek ](../audience/creating-a-segment-definition.md)

>[!TAB  Van bedrijfs gebeurtenisreizen ]

**Wanneer te gebruiken:** Bedrijfs voorwaarden die veelvoudige klanten beïnvloeden

{de ritten van de Bedrijfs gebeurtenis **worden teweeggebracht door zaken-vlakke gebeurtenissen (voorraadupdates, weeralarm, prijsveranderingen) die veelvoudige profielen gelijktijdig beïnvloeden.** Deze maatregelen zijn eerder gericht op bredere bedrijfsomstandigheden dan op individuele acties.

**Perfect voor:** Lage inventarisalarm aan geïnteresseerde klanten, de aankondigingen van de flitsverkoop, op weer-gebaseerde bevorderingen, de berichten van de prijsdaling, en product achterstandsalarm.

➡️ [ Leer over bedrijfsgebeurtenissen ](../event/about-creating-business.md) | [ Invoerbeheer ](entry-management.md)

>[!ENDTABS]

## Beslissingsgids: Het kiezen van uw reistype {#decision-guide}

Volg deze beslisboom om het juiste reistype voor uw gebruiksgeval te selecteren:

### Stap 1: Wat zet de reis in gang?

* **de Klant voert specifieke actie** uit (aankoop, klik, login) → Ga naar Stap 2
* **Tijd/programma** (verzend in specifieke tijd of terugkomend) → **Reis van het publiek van het Gebruik Gelezen**
* **de statusveranderingen van de Klant** (sluit zich aan bij/verlaat een segment) → Ga naar Stap 3
* **Bedrijfs voorwaarde** (voorraadniveau, prijsverandering, weer) → **Van het Bedrijfs gebruik gebeurtenisreis**

### Stap 2: De individuele trekkers van de klantenactie

* **is directe, real-time reactie nodig?**
   * Ja → **Eenheid van het Gebruik reis**
   * No → Consider Read Audience trip with scheduled executing

### Stap 3: wijzigingen in de status van de klant

* **moet antwoorden wanneer de klanten een segment ingaan OF weggaan?**
   * Ja → **reis van de Kwalificatie van het publiek van het Gebruik**
   * Nee, alleen bij het binnenvaren → Denk na over een eenheidstraject met evenement of lees het publiek met het filter

### Snelle selectie in gebruik

| Uw doel | Aanbevolen transporttype | Waarom |
|-----------|------------------------|-----|
| Bevestiging van bestelling verzenden na aankoop | Unitair | Onmiddellijke respons op individuele actie |
| Maandelijkse nieuwsbrief naar abonnees sturen | Publiek lezen | Geplande batchcommunicatie |
| Klanten op de hoogte stellen wanneer ze de VIP-status bereiken | Poortkwalificatie | Realtime reactie op statuswijziging |
| Klanten waarschuwen voor lage voorraad van gevolgde objecten | Zakelijke gebeurtenis | De bedrijfsomstandigheden beïnvloeden veelvoudige klanten |
| Welkom nieuwe gebruikers van apps | Unitair | Wordt geactiveerd door een inschrijvingsgebeurtenis |
| Inactieve klanten opnieuw betrekken | Poortkwalificatie | Reageert op inactiviteitssegmentitem |
| Seizoensgebonden bevordering naar doelsegment | Publiek lezen | Geplande campagne voor publiek |
| Aankondiging van Flash-verkoop | Zakelijke gebeurtenis | Het besluit van de zaken beïnvloedt veelvoudige klanten |

>[!NOTE]
>
>Weet u niet zeker welk type u wilt kiezen? Begin met **Eenvoudige reizen** voor op gebeurtenis-gebaseerde ervaringen of **Gelezen de reizen van het Publiek** voor geplande campagnes-deze behandelen gemeenschappelijkste gebruiksgevallen.

## Gedetailleerde vergelijking van reistypes {#journey-types-comparison}

In deze tabel kunt u snel de verschillende soorten reizen vergelijken en de juiste keuze maken voor uw gebruiksscenario:

| Verhouding | Eenheidstreizen | Reizen publiek lezen | Publiek gekwalificeerde reizen | Zakelijke gebeurtenissenreizen |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **mechanisme van de Ingang** | Afzonderlijke gebeurtenistrigger | Geplande partij | Wijziging van het Real-Time publiekslidmaatschap | Gebeurtenis op bedrijfsniveau |
| **timing van de Ingang** | In real time, wanneer gebeurtenissen voorkomen | Gepland (eenmalig of terugkerend) | In real time, aangezien de kwalificatie voorkomt | In real time, wanneer de bedrijfsgebeurtenis brandt |
| **ingang van het Profiel** | Eén voor één | Alles tegelijk (batch) | Eén voor één | Meerdere profielen tegelijk |
| **Trigger bron** | Actie van de klant (aankoop, klik, login) | Tijdschema | Publiek lidmaatschap (entry/exit) | Bedrijfsomstandigheden (voorraad, weer, prijs) |
| **Best voor** | Transactieberichten, gedragsreacties | Marketingcampagnes, nieuwsbrieven | Loyaliteitsprogramma&#39;s, levenscyclusfasen | Voorraadwaarschuwingen, promoties, bedrijfsomstandigheden |
| **Gebruik wanneer** | Directe reactie op de afzonderlijke acties die nodig zijn | Grote publiekssegmenten op schema bereiken | Reageren op wijzigingen in de klantstatus | Bedrijfs gebeurtenissen beïnvloeden veelvoudige klanten |
| **Voorbeelden** | Bevestigen van bestelling, wachtwoord opnieuw instellen | Maandelijkse nieuwsbrief, seizoenscampagne | VIP-upgrade, inactiviteitswaarschuwing | Waarschuwing voor lage voorraad, flash-verkoop, prijsdaling |
| **re-entry** | Configureerbaar (meerdere items per profiel toestaan) | Elk profiel wordt één keer per uitvoering ingevoerd | Configureerbaar per kwalificatiegebeurtenis | Dezelfde gebeurtenis kan van invloed zijn op meerdere profielen |
| **Vereisten van Gegevens** | Gebeurtenisschema met triggergegevens | [!DNL Adobe Experience Platform] publiek | Streaming- of batchpubliek | Schema voor zakelijke gebeurtenissen |

## Compatibiliteit van kenmerken per type transport {#feature-compatibility}

Niet alle functies zijn beschikbaar voor alle soorten reizen. Gebruik deze matrix om te begrijpen welke mogelijkheden werken met welke transporttypen:

| Functie/mogelijkheid | Unitair | Publiek lezen | Poortkwalificatie | Zakelijke gebeurtenis |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **mechanismen van de Ingang** |
| Gebeurtenisgestuurde vermelding | ✅ | ❌ | ❌ | ✅ |
| Gepland item | ❌ | ✅ | ❌ | ❌ |
| Publiek-gebaseerd item | ❌ | ✅ | ✅ | ❌ |
| **de eigenschappen van 0} Orchestration** |
| Wachten op activiteiten | ✅ | ✅ | ✅ | ✅ |
| Conditioneringsactiviteiten | ✅ | ✅ | ✅ | ✅ |
| Aangepaste acties | ✅ | ✅ | ✅ | ✅ |
| Lees de publieksactiviteit (binnenreis) | ✅ | ✅ | ✅ | ✅ |
| Kwalificatieactiviteit van het publiek | ✅ | ✅ | ✅ | ✅ |
| Snelheid | ✅ | ✅ | ✅ | ✅ |
| **het beheer van het Profiel** |
| Opnieuw openen van profiel | ✅ Configureerbaar | ❌ Eenmaal per uitvoering | ✅ Configureerbaar | ✅ Per gebeurtenis |
| Naamruimteconfiguratie | ✅ Vereist | ✅ Optioneel | ✅ Vereist | ✅ Vereist |
| Profiel uiteinde | ✅ | ✅ | ✅ | ✅ |
| **het Testen &amp; optimalisering** |
| Testmodus | ✅ | ✅ | ✅ | ✅ |
| Droge run | ✅ | ✅ | ✅ | ✅ |
| Padexperimenten (A/B-tests) | ✅ | ✅ | ✅ | ❌ |
| Optimalisatie bij verzending | ✅ | ✅ | ✅ | ✅ |
| **Kanalen** |
| Email | ✅ | ✅ | ✅ | ✅ |
| Pushmeldingen | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| In-app berichten | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Inhoudskaarten | ✅ | ✅ | ✅ | ✅ |
| **Geavanceerde mogelijkheden** |
| Incrementeel lezen | ❌ | ✅ | ❌ | ❌ |
| Exportpubliek | ✅ | ✅ | ✅ | ✅ |
| Tijdzonebeheer | ✅ | ✅ | ✅ | ✅ |
| Reactiegebeurtenissen | ✅ | ✅ | ✅ | ✅ |
| Externe databronnen | ✅ | ✅ | ✅ | ✅ |
| Throtting/Capping | ✅ | ✅ | ✅ | ✅ |

**Legend:** ✅ = Gesteund | ❌ = Niet ondersteund

## Volgende stappen {#next-steps}

Nu je reistypes begrijpt, ben je klaar om:

* **[creeer uw eerste reis](journey-gs.md)** - Step-by-step gids
* **[leer over de reisontwerper](using-the-journey-designer.md)** - Ontwerp uw wegcanvas
* **[verken reismogelijkheden](journey.md#capabilities)** - ontdek geavanceerde eigenschappen
* **[de reis FAQ van de Mening](journey-faq.md)** - Gemeenschappelijke beantwoorde vragen

**Behoefte met campagnes te vergelijken?**

* [ Reizen vs Campagnes vergelijkingsgids ](../start/journeys-vs-campaigns.md) - kies tussen reizen, acties/API campagnes, en Geordende campagnes
