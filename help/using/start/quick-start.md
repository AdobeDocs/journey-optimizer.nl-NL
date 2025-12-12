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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 1%

---


# Rollen en verantwoordelijkheden

Adobe Journey Optimizer stelt merken in staat om verbonden en gecontextualiseerde klantreizen te leveren gedurende de gehele levenscyclus van de klant. Het staat teams toe om interactie bij schaal te personaliseren en klantenverwachtingen met bedrijfsdoelstellingen te richten. In deze documentatie wordt uitgelegd wat de belangrijkste functies zijn bij het effectief gebruiken van Journey Optimizer, hun verantwoordelijkheden en hoe u aan de slag kunt gaan.

**Belangrijke Nota:** Adobe Journey Optimizer bepaalt verschillende rollen met specifieke verantwoordelijkheden. Eén individu kan meerdere rollen of alle rollen uitvoeren, afhankelijk van de structuur van uw organisatie.

## Op rollen gebaseerde snelle-starthulplijnen

Om de implementatie te vereenvoudigen, organiseert Adobe Journey Optimizer taken in specifieke rollen die op deskundigheid worden gebaseerd. Elke rol concentreert zich op essentiële taken die worden vereist om een naadloze klantenervaring te leveren.

| Rol | Primaire verantwoordelijkheden | Sleutelvaardigheden | Typische taken |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Beheerder** | Omgeving instellen en toegangsbeheer | Systeemconfiguratie, gebruikersbeheer, beveiliging | Sandboxen configureren, machtigingen beheren, kanaalconfiguraties instellen |
| **Ingenieur van Gegevens** | Grondslag en architectuur van gegevens | Gegevensmodellering, XDM-schema&#39;s, gegevenskwaliteit | Creeer schema&#39;s en datasets, vorm gegevensopname, beheer gegevenslevenscyclus |
| **Ontwikkelaar** | Technische implementatie en integratie | Mobile/Web SDK, API&#39;s, gebeurtenisgestuurde architectuur | SDK&#39;s integreren, gebeurtenissen implementeren, eindpunten van aangepaste handelingen maken |
| **Marketer** | Ontwerp en uitvoering door de klant | Reisontwerp, maken van inhoud, gegevensanalyse | Reizen samenstellen, persoonlijke inhoud maken, campagnes optimaliseren |

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

Focus op het creëren van persoonlijke klantenervaringen over alle kanalen.

**Zeer belangrijke mogelijkheden u zult gebruiken:**

* Creeer publiek en bouwt segmenten met veelvoudige methodes (segmentdefinities, Csv uploadt, publiekssamenstelling)
* Inhoud ontwerpen met AI Assistant voor het genereren van tekst en afbeeldingen
* Bouw multi-kanaals klantenreizen met belemmering-en-dalingsontwerper
* Optimalisatie van verzendtijd en conflictbeheer gebruiken om de betrokkenheid te maximaliseren
* Inhoud testen en goedkeuringswerkstromen gebruiken voordat ze worden gepubliceerd
* Prestaties bewaken met geïntegreerde rapporteringsdashboards

**Begin met:** creeer een eenvoudige welkome reis of verlaten campagne van de wortelterugwinning gebruikend vooraf gebouwde malplaatjes.

[Aan de slag als een marketeter →](path/marketer.md)

### Voor gegevensengineers {#for-data-engineers}

Vestig de gegevensstichting die individuele ervaringen toelaat.

**Zeer belangrijke verantwoordelijkheden:**

* Naamruimten maken en identiteitsresolutie configureren
* XDM-schema&#39;s ontwerpen voor profiel- en gebeurtenisgegevens (standaard en relationeel)
* De datasets van de opstelling en laat hen voor het Profiel van de Klant in real time toe
* Bronconnectors voor batch- en streaming gegevensinvoer configureren
* Berekende kenmerken maken om segmentatie te vereenvoudigen
* Gebeurtenissen en gegevensbronnen configureren voor uitvoering van de reis
* Gegevenskwaliteit, beheer en levenscyclus beheren

**Begin met:** de identiteitsnamespaces van de opstelling en creeer uw eerste profielschema met de vereiste gebiedsgroepen.

[Aan de slag als Data Engineer →](path/data-engineer.md)

### Voor beheerders {#for-administrators}

Stel de Journey Optimizer-omgeving voor uw organisatie in en beheer deze.

**Zeer belangrijke verantwoordelijkheden:**

* Sandboxen maken en beheren voor ontwikkeling, testen en productie
* Rollen en machtigingen configureren met behulp van externe of aangepaste rollen
* Pas voorwerp-vlakke toegangsbeheer (OLAC) toe om middelen te beveiligen
* Kanaalconfiguraties instellen voor e-mail-, SMS-, push-, in-app-, web- en inhoudskaarten
* Subdomeinen delegeren en IP-pools maken voor e-maillevering
* Onderdrukkingslijsten en -lijsten van gewenste personen beheren
* Beleid voor machtigingen en gegevensbeheer configureren (met gezondheidszorg/privacyschild)

**Begin met:** vorm zandbakken, opstelling basisrollen en toestemmingen, dan werk met uw team op kanaalconfiguraties.

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

* [&#x200B; Video&#39;s van het Leerprogramma &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html){target="_blank"} - geleidelijke videoleerprogramma&#39;s voor alle rollen
* [&#x200B; de Gevallen van het Gebruik van de Reis Bibliotheek &#x200B;](../building-journeys/jo-use-cases.md) - Praktische voorbeelden en implementatiepatronen
* [&#x200B; AI &amp; Intelligente Eigenschappen &#x200B;](ai-features.md) - leer over Medewerker AI, send-time optimalisering, en inhoudsgeneratie
* [&#x200B; Gids van het Gebruikersinterface &#x200B;](user-interface.md) - navigeer effectief Journey Optimizer

**blijven bijgewerkt:**

* [&#x200B; Nota&#39;s van de Versie &#x200B;](../rn/release-notes.md) - de Meest recente eigenschappen, de verbeteringen, en moeilijke situaties
* [&#x200B; Updates van de Documentatie &#x200B;](../rn/documentation-updates.md) - de recente documentatieveranderingen van het spoor
* **Berichten van het Product** - laat alarm in uw [&#x200B; profiel van Adobe Experience Cloud &#x200B;](https://experience.adobe.com/preferences){target="_blank"} toe om berichten over nieuwe versies, onderhoudsvensters, en belangrijke aankondigingen te ontvangen. Klik op het profielpictogram > Voorkeuren > Meldingen om te configureren.

**Gemeenschap &amp; Steun:**

* [&#x200B; Gemeenschap van Experience League &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - verbind met andere gebruikers en deskundigen
* [&#x200B; Forum van het Product &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - stel vragen en deel kennis
