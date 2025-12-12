---
solution: Journey Optimizer
product: journey optimizer
title: Rollen en verantwoordelijkheden
description: Meer informatie over de verschillende rollen voor Adobe Journey Optimizer en over hun verantwoordelijkheden
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 0%

---


# Rollen en verantwoordelijkheden

Adobe Journey Optimizer stelt merken in staat om verbonden, contextafhankelijke en persoonlijke ervaringen te leveren gedurende de hele reis van de klant. Journey Optimizer is gebouwd met een complete focus op schaal, snelheid en flexibiliteit en combineert drie belangrijke stuurprogramma&#39;s in een uniforme toepassing:

* **Real-time klanteninzichten en overeenkomst** aangedreven door Adobe in real time klantenprofiel
* **Moderne omnichannel orchestratie** door verenigde canvases voor zowel reizen in real time als partijcampagnes, plus een moderne berichtontwerper
* **Intelligente besluitvorming en verpersoonlijking** door besluitvormingsbeheer en AI/ML mogelijkheden

Journey Optimizer biedt twee orchestratiemethoden om aan verschillende marketingbehoeften te voldoen:

* **Reizen**: Best voor in real time, één-aan-één overeenkomst waar elke klant zich door bij hun eigen tempo beweegt, die door gedrag of gebeurtenissen wordt teweeggebracht
* **Orchestrated Campaigns**: Best voor partij, één-aan-vele campagnes waar het publiek samen door multi-step werkschema&#39;s op programma-ideaal voor seizoensbevorderingen, productlanceringen, en op rekening-gebaseerde mededelingen vooruitgaat

Dankzij deze uniforme ervaring kunt u volledige gebruiksgevallen op één plaats implementeren, van het definiëren van soorten publiek en het ontwerpen van reizen tot het maken van gepersonaliseerde inhoud en het analyseren van resultaten. In deze documentatie wordt uitgelegd wat de belangrijkste functies zijn bij het effectief gebruiken van Journey Optimizer, hun verantwoordelijkheden en hoe u aan de slag kunt gaan.

**Belangrijke Nota:** Adobe Journey Optimizer bepaalt verschillende rollen met specifieke verantwoordelijkheden. Eén individu kan meerdere rollen of alle rollen uitvoeren, afhankelijk van de structuur van uw organisatie.

## Op rollen gebaseerde snelle-starthulplijnen

Om de implementatie te vereenvoudigen, organiseert Adobe Journey Optimizer taken in specifieke rollen die op deskundigheid worden gebaseerd. Elke rol concentreert zich op essentiële taken die worden vereist om een naadloze klantenervaring te leveren.

| Rol | Primaire verantwoordelijkheden | Sleutelvaardigheden | Typische taken |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Beheerder** | Omgeving instellen en toegangsbeheer | Systeemconfiguratie, gebruikersbeheer, beveiliging | Sandboxen instellen, gebruikersmachtigingen beheren, kanalen en voorinstellingen voor berichten configureren |
| **Ingenieur van Gegevens** | Klantprofielgegevens en gegevensbronnen | Gegevensmodellering, XDM-schema&#39;s, bronconnectors | Model profiel en bedrijfsgegevens in schema&#39;s, vormen bronschakelaars, controleren gegevensopname |
| **Ontwikkelaar** | Technische implementatie en integratie | Mobile/Web SDK, API&#39;s, gebeurtenisgestuurde architectuur | SDK&#39;s integreren, gebeurtenissen implementeren, eindpunten van aangepaste handelingen maken |
| **Marketer** | Reisontwerp en persoonlijke ervaringen | Reisorchestratie, content creation, doelgroep | De reizen van de klant van het ontwerp, creeert en personaliseert berichten, beheert aanbiedingen en besluitvormingscomponenten, bepaalt publiek |

Elke rol richt een specifieke fase van de implementatie van Adobe Journey Optimizer en verzekert een gestructureerd en efficiënt plaatsingsproces.

## Implementatievolgorde en Rol-afhankelijkheden

Een geslaagde Journey Optimizer-implementatie volgt doorgaans deze volgorde, die de afhankelijkheden tussen rollen weerspiegelt:

1. **Beheerder**: Plaatst omhoog het milieu\
   De beheerder vestigt de stichting door zandbakken te vormen, de controles van de opstellingstoegang, en kanaalconfiguraties voor te bereiden. Dit moet eerst gebeuren om andere teams in staat te stellen te werken.
   * Ontwikkeling-, staging- en productiesandboxen configureren
   * De rollen van de opstelling, toestemmingen, en voorwerp-vlakke toegangsbeheer (OLAC)
   * Kanaalconfiguraties configureren (e-mail, SMS, push, in-app, web, inhoudskaarten)
   * Subdomeinen delegeren en IP-pools instellen
   * Onderdrukkingslijsten en toestemmingsbeleid configureren

2. **Ingenieur van Gegevens**: Creeert de gegevensstichting\
   De Ingenieurs van gegevens bouwen de gegevensinfrastructuur die verpersoonlijking macht, bepalend hoe de klantengegevens in en door het systeem stromen.
   * Identiteitsnaamruimten maken voor klantidentificatie
   * XDM-schema&#39;s ontwerpen (profiel, ervaringsgebeurtenissen, relationeel)
   * De datasets van de opstelling en laat hen voor het Profiel van de Klant in real time toe
   * Gegevensinvoer configureren (batch en streaming)
   * Berekende kenmerken maken voor complexe berekeningen
   * Gebeurtenissen en gegevensbronnen configureren voor reizen

3. **Ontwikkelaar**: Implementeert technische integratie\
   Ontwikkelaars verbinden toepassingen met Journey Optimizer door SDK&#39;s te integreren, gebeurtenissen te verzenden en API-eindpunten te maken. Met deze implementaties kunnen reizen worden gestart en uitgevoerd.
   * Mobiele SDK (iOS/Android) integreren met instellingen voor pushmeldingen
   * Web SDK voor webervaringen implementeren
   * Gebeurtenissen verzenden vanuit toepassingen om reizen te activeren
   * Eindpunten voor aangepaste handelingen maken voor externe systeemintegratie
   * Implementaties testen met Adobe Experience Platform Assurance

4. **Marketer**: Ontwerpen en voeren klantenervaringen uit\
   Marketers gebruiken al het basiswerk om reizen te maken, inhoud te maken en de ervaringen van klanten op alle kanalen te optimaliseren.
   * Bouw publiek met behulp van segmentatie, CSV-upload of publiekscompositie
   * Aangepaste inhoud ontwerpen met AI Assistant en sjablonen
   * Multikanaalreizen maken met gebeurtenis- en publiektriggers
   * Testen met goedkeuringswerkstromen vóór starten
   * Prestaties bewaken en optimaliseren op basis van rapportageinzichten

**Nota:** Terwijl deze opeenvolging typisch is, kunnen sommige activiteiten parallel voorkomen. Ontwikkelaars kunnen bijvoorbeeld aan toepassingsintegratie werken terwijl Data Engineers schema&#39;s configureren.

## Aan de slag met Rol

Elke rol begint met specifieke taken die aan zijn nadruk worden aangepast. Als u deze eerste stappen uitvoert, verloopt het instappen soepeler en wordt het proces beter afgestemd op het gehele implementatieproces:

### Voor Marktdeelnemers {#for-marketers}

Als Markteur of Bedrijfs Praktijk, ontwerpt u klantenreizen om persoonlijke, contextuele ervaringen over alle aanraakpunten te leveren. U zult in een verenigde interface werken om volledige gebruiksgevallen van begin tot eind uit te voeren.

**Zeer belangrijke mogelijkheden u zult gebruiken:**

* **Journey Orchestration**: Creeer in real time, één-aan-één klantenovereenkomst waar elke persoon zich bij hun eigen tempo beweegt, die door gedrag of gebeurtenissen over kanalen wordt teweeggebracht
* **Organiseren van de Campagne**: Ontwerp en automatiseer complexe, multi-step partijcampagnes bij schaal gebruikend een visueel canvas. Ideaal voor campagnes met een merk, zoals seizoensgebonden promoties, productlanceringen en communicatie op basis van account. Gebruik segmentering van meerdere entiteiten om een exact publiek te maken door klantgegevens aan te sluiten bij verwante entiteiten (accounts, aankopen, boekingen)
* **Moderne Designer van het Bericht**: Ontwerp en verpersoonseer e-mail en mobiele berichten met een belemmering-en-dalingsinterface. Buiten-de-doosmalplaatjes uitgeven om tijd aan markt te versnellen
* **Beheer van het Besluit**: Creeer en beheer aanbiedingen, toelatingsregels, en andere componenten in een gecentraliseerde bibliotheek die in e-mail en klantenaanraakpunten kunnen worden ingebed
* **Beheer van Activa**: De Hoofdzaak van de Activa van de Manager van de Ervaring van de Toegang volledig ingebed in Journey Optimizer voor gestroomlijnde elemententoegang en levering
* **Definitie van het publiek**: Bouw op bestelling publiek met onmiddellijke verfijning gebruikend relationele vragen, met pre-send zicht voor nauwkeurige publiekscijfers
* **AI/ML de Diensten**: De optimalisering van de gebruiks verzendt-tijd en voorspelbare betrokkenheidsscores om high-value klanten te richten en kanaliseert kanonrisico

**Begin met:** de gevalmalplaatjes en tovenaars van het Gebruik om nieuwe klantenreizen gemakkelijk tot stand te brengen en op te stellen.

[Aan de slag als een marketeter →](path/marketer.md)

### Voor gegevensengineers {#for-data-engineers}

Als Data Architect of engineer stelt u de gegevens van het klantprofiel en andere gegevensbronnen in en onderhoudt deze die de ervaringen van Journey Optimizer kracht maken.

**Zeer belangrijke verantwoordelijkheden:**

* **Gegevens van het Profiel van de Klant**: De gegevens van het modelklantenprofiel en bedrijfsgegevens in schema&#39;s om een verenigde 360 graadmening van de klant te creëren
* **Relationele Gegevens Modeling**: Voor Geordende campagnes, ontwerp relationele schema&#39;s om multi-entiteitssegmentatie-verbindende klantengegevens met verwante entiteiten zoals rekeningen, aankopen, abonnementen, en het boeken voor flexibele publieksverwezenlijking toe te laten
* **de Verbindingen van Source**: Vorm bronschakelaars om gegevens van Web, CRM, off-line gegevens, en andere bronnen in Adobe Experience Platform in te voeren
* **Resolutie van de Identiteit**: De naamruimten van de opstelling om profielen onophoudelijk bij te werken en klanten binnen en uit segmenten en reizen in real time te bewegen
* **Gegevensbronnen**: Vorm gegevensbronnen om in real time aan externe signalen over de klantenreis te luisteren
* **Beheer van het Profiel**: Laat datasets voor het Profiel van de Klant in real time aan macht gepersonaliseerde ervaringen toe
* **Kwaliteit van Gegevens**: De gegevens van de monitor opnemen om alles te verzekeren vloeiend in Journey Optimizer stroomt

**Begin met:** Model uw eerste schema van het klantenprofiel en vorm een bronschakelaar beginnen het opnemen van gegevens.

[Aan de slag als Data Engineer →](path/data-engineer.md)

### Voor beheerders {#for-administrators}

Als beheerder stelt u de Journey Optimizer-omgeving zo in dat uw teams efficiënt en veilig kunnen werken.

**Zeer belangrijke verantwoordelijkheden:**

* **Sandboxes**: Creeer en beheer zandbakken aan verdelingsgegevens en reizen voor verschillende gebruikersgroepen (ontwikkeling, het testen, productie)
* **Beheer van de Gebruiker**: De groepen van de opstelling gebruikersgroepen en toestemmingen om toegang tot verschillende functionaliteit te controleren
* **Opstelling van het Kanaal**: Vorm leveringskanalen en berichtvoorinstellingen om verenigbare branding over berichten en activa te verzekeren die door Journey Optimizer worden geleverd
* **Veiligheid &amp; Governance**: Pas objecten-vlakke toegangscontrole (OLAC) toe, vorm toestemmingsbeleid, en voer gegevensbeleid uit
* **Leverbaarheid**: De subdomeinen van de Delegatie, creeer IP pools, en beheer suppressielijsten en lijsten van gewenste personen
* **Configuratie van de Reis**: De elementen en de configuraties van de opstellingstraject voor uw teams

**Begin met:** vorm zandbakken en gebruikerstoestemmingen, dan opstelling uw eerste kanaalconfiguraties en berichtvoorinstellingen.

[Aan de slag als beheerder →](path/administrator.md)

### Voor ontwikkelaars {#for-developers}

Implementeer technische integratie die Journey Optimizer verbindt met uw toepassingen.

**Zeer belangrijke verantwoordelijkheden:**

* Adobe Experience Platform Mobile SDK integreren (iOS/Android)
* Web SDK voor webervaringen en webpushmeldingen implementeren
* Referenties en certificaten voor pushmeldingen configureren
* Gebeurtenissen verzenden vanuit toepassingen om reizen te activeren
* Bouw API eindpunten die Journey Optimizer via douaneacties roept
* Codegebaseerde ervaringen implementeren voor het web, mobiele apparaten en andere oppervlakken
* Implementaties testen en fouten opsporen met Adobe Experience Platform Assurance
* Werken met Journey Optimizer API&#39;s voor programmatische toegang

**Begin met:** integreer Mobiele of SDK van het Web, dan voer uw eerste gebeurtenis uit om een reis teweeg te brengen.

[&#x200B; krijgen Begonnen als Ontwikkelaar → &#x200B;](path/developer.md)

## Cross-Role Collaboration

Succesvolle Journey Optimizer-implementaties vereisen samenwerking voor alle rollen:

* **de Beheerders** laten andere rollen door opstellings zandbakken, toestemmingen, en kanaalconfiguraties toe
* **Ingenieurs van Gegevens** verstrekken de gegevensstichting die de Ontwikkelaars en de Marketers voortbouwen op
* **Ontwikkelaars** voeren de technische integratie uit die de Marketers gebruiken om reizen teweeg te brengen
* **de Keters** verstrekken terugkoppelen aan alle teams over gegevenskwaliteit, eigenschapverzoeken, en gebruikerservaring

**Beste praktijken:** Greep regelmatige interfunctionele vergaderingen om op prioriteiten te richten, vooruitgang te delen, en blockers over teams te richten.

## Hoe kan ik-video {#video}

Bekijk de inleidende video voor meer informatie over sleutelmogelijkheden en persona&#39;s van Journey Optimizer. De video doorloopt de gebruikersinterface en markeert belangrijke eigenschappen die op rol-specifieke workflows worden gebaseerd.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Aanvullende bronnen

Verken de volgende bronnen voor diepgaander leren en updates:

**het Leren &amp; Documentatie:**

* [&#x200B; Video&#39;s van het Leerprogramma &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=nl-NL){target="_blank"} - geleidelijke videoleerprogramma&#39;s voor alle rollen
* [&#x200B; de Gevallen van het Gebruik van de Reis Bibliotheek &#x200B;](../building-journeys/jo-use-cases.md) - Praktische voorbeelden en implementatiepatronen
* [&#x200B; AI &amp; Intelligente Eigenschappen &#x200B;](ai-features.md) - leer over Medewerker AI, send-time optimalisering, en inhoudsgeneratie
* [&#x200B; Gids van het Gebruikersinterface &#x200B;](user-interface.md) - navigeer effectief Journey Optimizer

**blijven bijgewerkt:**

* [&#x200B; Nota&#39;s van de Versie &#x200B;](../rn/release-notes.md) - de Meest recente eigenschappen, de verbeteringen, en moeilijke situaties
* [&#x200B; Updates van de Documentatie &#x200B;](../rn/documentation-updates.md) - de recente documentatieveranderingen van het spoor
* [&#x200B; Berichten van het Product &#x200B;](../rn/releases.md#staying-informed) - Leer hoe te aan e-mail en in-productalarm voor de updates van Journey Optimizer in te schrijven

**Gemeenschap &amp; Steun:**

* [&#x200B; Gemeenschap van Experience League &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - verbind met andere gebruikers en deskundigen
* [&#x200B; Forum van het Product &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - stel vragen en deel kennis
