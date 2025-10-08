---
solution: Journey Optimizer
product: journey optimizer
title: Gangbare campagnes en beperkingen
description: Meer informatie over geordende campagnes, instructies en beperkingen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: a9b790bc833b5819862bf2f3284968d81f595f28
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---


# Afvoerkanalen en beperkingen {#guardrails}

Hieronder vindt u instructies en beperkingen wanneer u geordende campagnes gebruikt.

## Beperkingen van gegevensstroom

### Gegevensontwerp en -opslag

* De relationele datastore steunt a **maximum van 200 lijsten** (schema&#39;s).

* Voor Geordende campagnes, moet de totale grootte van om het even welk individueel schema **100 GB** niet overschrijden.

* De dagelijkse updates aan een schema zouden **tot minder dan 20%** van zijn totale verslagtelling moeten worden beperkt om prestaties en stabiliteit te handhaven.

* Relationele gegevens zijn het primaire model dat wordt ondersteund voor inname, gegevensmodellering en segmentatiegebruik.

* De schema&#39;s die voor het richten worden gebruikt moeten minstens **één identiteitsgebied van type`String`** bevatten, die aan een bepaalde identiteitsnaamruimte in kaart wordt gebracht.

* Het gemiddelde aantal attributen per schema **zou 50 kolommen** niet moeten overschrijden om manageability en prestaties te handhaven.

* Model-gebaseerde schema&#39;s kunnen niet voor Adobe Experience Platform **Profielen** worden toegelaten. Slechts worden de Standaard schema&#39;s XDM gesteund voor Adobe Experience Platform **Profielen**. Modelgebaseerde schema&#39;s kunnen worden ingeschakeld voor geordende campagnes of actiecampagnes. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Data-opname

* Profiel + relationele gegevensinvoer is vereist.

* Al opname moet via **Gegevens van de Verandering voorkomen vangt** bronnen:

   * Voor **op dossier-Gebaseerd**: `_change_request_type` gebied wordt vereist. Ondersteunde waarden zijn `U` (upsert) of `D` (delete).

   * Voor **op wolk-Gebaseerde**: Het registreren van de lijst moet worden toegelaten.

* **Gedeeltelijke verslagupdates worden niet toegestaan**, moet elke rij als volledig verslag worden verstrekt.

* De opname van de partij voor de Orchestratie van de Campagne is beperkt tot **eens om de 15 minuten**.

* De latentie van de congestie, in relationele opslag, waagt typisch **van 15 minuten aan 2 uren**, afhankelijk van:

   * Gegevensvolume

   * Gelijktijdige installatie van het systeem

   * Type bewerking, bijv. invoegtoepassingen zijn sneller dan updates

* **Dataflow aan datasetverhouding is 1-1**. Dit betekent dat slechts één bron één dataset tegelijk kan voeden. Om de bron te schakelen, moet bestaande dataflow worden geschrapt en een nieuwe dataflow worden gecreeerd met de nieuwe bron.

### Gegevensmodellering

* Alle schema&#39;s, met inbegrip van feitenlijsten, moeten **een versiedescriptor** omvatten om juiste versiecontrole en traceerbaarheid te verzekeren.

* Elke lijst moet een bepaalde **primaire sleutel** hebben om gegevensintegriteit en stroomafwaartse verrichtingen te steunen.

* `table_name` die tijdens de verwezenlijking van datasets wordt toegewezen is permanent en door segmentatie en verpersoonlijkingseigenschappen wordt gebruikt.

* **de groepen van het Gebied worden niet gesteund** in het huidige gegevens modelleringskader.

* Ondersteuning voor samengestelde primaire sleutels met stromen voor het uploaden van bestanden is momenteel niet beschikbaar.

## Activiteitsbeperkingen

* Slechts **scalaire attributen worden gesteund** in publieksdefinities; **kaarten en series worden niet toegestaan**.

* **de activiteiten van de Segmentatie baseert zich hoofdzakelijk op relationele gegevens**. Hoewel profielgegevens kunnen worden opgenomen, kan het gebruik van grote profielgegevenssets de prestaties beïnvloeden.

* **De grenzen worden afgedwongen op het aantal profielattributen** die in zowel partij als het stromen publiek kunnen worden gebruikt om systeemefficiency te handhaven.

* **Opsommingen** worden volledig gesteund.

* **gelezen Publiek wordt niet in het voorgeheugen ondergebracht**, teweegbrengt elke campagneuitvoering een volledige publieksevaluatie van de onderliggende gegevens teweeg.

* **de Optimalisering wordt sterk geadviseerd** wanneer het werken met grote of complexe publieksdefinities om prestaties te verzekeren.

* **de Bewaarde publieksactiviteiten zijn statisch**, wijzen zij op de gegevens beschikbaar op het tijdstip van campagneuitvoering.

* **het toevoegen aan een Opgeslagen activiteit van het Publiek wordt niet gesteund**. Om het even welke wijzigingen vereisen een volledige beschreven van het publiek.

## Kanaalbeperkingen

Alleen SMS-, push- en e-mailkanalen worden ondersteund in geordende campagnes.
