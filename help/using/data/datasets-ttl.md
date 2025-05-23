---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over datasets Tijd-aan-levende (TTL) gidsen
description: Datasets Time-to-live guardrails in  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform, data Lake, create, Lake, datasets, profile
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: b27ddcc88ca4b4209c9d29974a0b0d0dbe98cc94
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 2%

---

# Datasets Time-to-live (TTL)-instructies {#ttl-guardrail}

Vanaf Februari 2025, wordt een tijd-aan-levende (TTL) guardrail opgesteld uit aan systeem-geproduceerde datasets van Journey Optimizer in **nieuwe zandbakken en nieuwe organisaties** als volgt:

* 90 dagen voor gegevens in de profielopslag,
* 13 maanden voor gegevens in het data Lake.

Deze verandering wordt uitgerold aan **bestaande klantenzandbakken** in een verdere fase.

## Betrokken gegevenssets {#datasets}

De onderstaande tabel bevat een lijst met alle beïnvloede gegevenssets en hun respectievelijke time-to-live-gegevens in het gegevensmeer en de profielopslag.

| Gegevensset | Data Lake TTL | Profielwinkel TTL |
|------|-----|-----|
| Dataset voor AJO-feedbackgebeurtenis | 13 maanden | 90 dagen |
| AJO Email Tracking Experience Event Dataset | 13 maanden | 90 dagen |
| Dataset voor AJO Push Tracking Experience | 13 maanden | 90 dagen |
| Gegevensset AJO Entiteit | 13 maanden | 90 dagen |
| Gegevensset AJO-oppervlakken | 13 maanden | nvt |
| Gegevensset van gebeurtenis Inbound Activity van AJO | 13 maanden | 90 dagen |
| AJO Classification-gegevensset | 13 maanden | nvt |
| Gegevensset AJO-e-mailBCC-feedbackgebeurtenis | 13 maanden | nvt |
| acpEntiteit-gebeurtenisgegevensset | 13 maanden | nvt |
| Journeys | 13 maanden | nvt |
| Gebeurtenissen reisstap | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Aangepaste aanbiedingen | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Alternatieve aanbiedingen | 13 maanden | nvt |
| Beslissingsobjectrepository - Plaatsingen | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Activiteiten | 13 maanden | nvt |
| ODE-beslissingsgebeurtenissen - prodbeslissing | 13 maanden | nvt |

## Veelgestelde vragen {#faq}

Hieronder volgt een lijst met antwoorden op veelgestelde vragen over TLL-gegevenssets.

+++Is deze wijziging alleen van toepassing op productiestanddozen of is deze ook van toepassing op dev-sandboxen?

Deze wijziging is van toepassing op alle sandboxtypen.

+++

+++Worden profielen zelf beïnvloed voor de 90 dagen-TTL in de profielopslag?

De door het systeem gegenereerde gegevenssetgegevens in het profiel worden na 90 dagen verwijderd, niet de profielen zelf.

+++

+++Als een door het systeem gegenereerde gegevensset naar [!DNL Customer Journey Analytics] (CJA) wordt geduwd, zullen de gegevens in CJA ook door de TTL worden beïnvloed?

Gegevens in [!DNL Customer Journey Analytics] blijven gesynchroniseerd met Experience Platform. Daarom zal een verwijdering van gegevens toe te schrijven aan een TTL op systeem-geproduceerde datasetgegevens ook de gegevens in [!DNL Customer Journey Analytics] beïnvloeden.

+++

+++ Kunnen klanten TTL voor [!DNL Journey Optimizer] gegevens van de systeemdataset in profielopslag verhogen?

De uitbreidingen van TTLs worden momenteel niet gesteund. Het is echter de bedoeling dat het TTL-proces wordt geoptimaliseerd zodat deze verlengingsverzoeken soms vanaf de tweede helft van 2025 kunnen worden ingediend.

>[!NOTE]
>
>Voor gegevens die in het profiel zijn opgeslagen, geldt de machtiging Totaal gegevensvolume. Elke toename van de gegevensopslag op het profiel als gevolg van een uitbreiding van de TTL zou daarom in mindering worden gebracht op de machtiging Totaal gegevensvolume. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=nl-NL){target=_blank}

+++

+++Kunnen klanten TTL voor [!DNL Journey Optimizer] gegevens van de systeemdataset in gegevens verhogen?

De uitbreidingen van TTLs worden momenteel niet gesteund. De klanten kunnen gegevens door Doelen uitvoeren om gegevens langer te behouden. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=nl-NL){target=_blank} . Bovendien kunnen klanten met een machtiging **[!DNL Data Distiller]** afgeleide gegevenssets maken om de gegevens in het gegevensmeer op te slaan zonder een TTL. [ leer meer ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++Zullen de volgende mogelijkheden door TTLs worden beïnvloed?

* **Opzoeken opslag**: Nr
* **Afbakening van de Reis**: Nr
* **Aanbieding die** begrenzen: Nr
* **verzendt de Optimalisering van de Tijd (STO)**: Nr
* **het frequentietoewijzing van het Bericht** (d.w.z., Bedrijfs regels): Nr
* **Meldend**: Nr

  >[!NOTE]
  >
  >Een TTL wordt reeds uitgevoerd op de [!DNL Customer Journey Analytics] (CJA) verbinding, die effectieve maximum terugblik periode van beïnvloede datasetgegevens tot 13 maanden vermindert.

* **de gegevensbron van Experience Platform**: Ja - de de gebeurtenisherwinning van de Ervaring is onderworpen aan 90 dag TTL.
* **Berekende attributen**: Ja - de aanvankelijke backfill berekening zal tot laatste 90 dagen van gegevens worden beperkt; gegevens verwerkte attributen zullen op stijgende gebeurtenissen voor verdere updates worden bijgewerkt. Zodra de volgende updates de terugkijkperiode (maximum 6 maanden) bereiken, beïnvloedt TTL hoofdzakelijk niet meer het gegevens verwerkte attribuut. Meer weten?
* **Segmentatie en het opnieuw richten**: Ja - de segmentatie is afhankelijk van gegevens in de profielopslag; daarom, is terugblik beperkt tot 90 dagen op beïnvloede datasetgegevens.
* **het Volgen**: Ja - vermindert effectieve maximum terugblik periode van beïnvloede datasetgegevens tot 90 dagen. Gegevens uit beïnvloede datasets blijven 13 maanden in data Lake.

+++

+++Welke timestamp wordt gebruikt voor handhaving TTL (b.v., voor backfill gebruiksgevallen)?

De tijdstempel van de gebeurtenis wordt gebruikt (dus niet de innamedatum).

+++
