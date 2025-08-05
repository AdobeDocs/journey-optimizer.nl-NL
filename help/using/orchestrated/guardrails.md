---
solution: Journey Optimizer
product: journey optimizer
title: Gangbare campagnes en beperkingen
description: Meer informatie over geordende campagnes, instructies en beperkingen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---


# Afvoerkanalen en beperkingen {#guardrails}

Hieronder vindt u aanvullende instructies en beperkingen wanneer u geordende campagnes gebruikt.

## Beperkingen van gegevensstroom

### Gegevensontwerp en -opslag

* De relationele datastore steunt a **maximum van 200 lijsten** (schema&#39;s).

* Voor Geordende campagnes, moet de totale grootte van om het even welk individueel schema **100 GB** niet overschrijden.

* De dagelijkse updates aan een schema zouden **tot minder dan 20%** van zijn totale verslagtelling moeten worden beperkt om prestaties en stabiliteit te handhaven.

* Relationele gegevens zijn het primaire model dat wordt ondersteund voor inname, gegevensmodellering en segmentatiegebruik.

* De schema&#39;s die voor het richten worden gebruikt moeten minstens **één identiteitsgebied van type`String`** bevatten, die aan een bepaalde identiteitsnaamruimte in kaart wordt gebracht.

### Gegevensopname

* Profiel + relationele gegevensinvoer is vereist.

* Al opname moet via **Gegevens van de Verandering voorkomen vangt** bronnen:

   * Voor **op dossier-Gebaseerd**: `change_type` gebied wordt vereist.

   * Voor **op wolk-Gebaseerde**: Het registreren van de lijst moet worden toegelaten.

* **de directe updates aan Snowflake of datasets worden niet gesteund**. Het systeem is alleen-lezen; alle wijzigingen moeten worden toegepast via Gegevens wijzigen.

* **de processen van ETL worden niet gesteund**. Gegevens moeten vóór inname volledig in de vereiste indeling worden omgezet.

* **Gedeeltelijke updates worden niet toegestaan**, moet elke rij als volledig verslag worden verstrekt.

* De opname van de partij voor de Orchestratie van de Campagne is beperkt tot **eens om de 15 minuten**.

* De latentie van de opsluiting, tijd van opname aan beschikbaarheid in Snowflake, waagt typisch **van 15 minuten aan 2 uren**, afhankelijk van:

   * Gegevensvolume

   * Gelijktijdige installatie van het systeem

   * Type bewerking, bijv. invoegtoepassingen zijn sneller dan updates

### Gegevensmodellering

* Alle schema&#39;s, met inbegrip van feitenlijsten, moeten **een versiedescriptor** omvatten om juiste versiecontrole en traceerbaarheid te verzekeren.

* Elke lijst moet een bepaalde **primaire sleutel** hebben om gegevensintegriteit en stroomafwaartse verrichtingen te steunen.

* `table_name` die tijdens de verwezenlijking van datasets wordt toegewezen is permanent en door segmentatie en verpersoonlijkingseigenschappen wordt gebruikt.

* **de groepen van het Gebied worden niet gesteund** in het huidige gegevens modelleringskader.

## Activiteitsbeperkingen

* Slechts **scalaire attributen worden gesteund** in publieksdefinities; **kaarten en series worden niet toegestaan**.

* **de activiteiten van de Segmentatie baseert zich hoofdzakelijk op relationele gegevens**. Hoewel profielgegevens kunnen worden opgenomen, kan het gebruik van grote profielgegevenssets de prestaties beïnvloeden.

* **De grenzen worden afgedwongen op het aantal profielattributen** die in zowel partij als het stromen publiek kunnen worden gebruikt om systeemefficiency te handhaven.

* **Lijst van Waarden (LOVs)** en **opsommingen** worden volledig gesteund.

* **gelezen Publiek wordt niet in het voorgeheugen ondergebracht**, teweegbrengt elke campagneuitvoering een volledige publieksevaluatie van de onderliggende gegevens teweeg.

* **de Optimalisering wordt sterk geadviseerd** wanneer het werken met grote of complexe publieksdefinities om prestaties te verzekeren.

* **de Bewaarde publieksactiviteiten zijn statisch**, wijzen zij op de gegevens beschikbaar op het tijdstip van campagneuitvoering.

* **het toevoegen aan een Opgeslagen activiteit van het Publiek wordt niet gesteund**. Om het even welke wijzigingen vereisen een volledige beschreven van het publiek.
