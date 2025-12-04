---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over datasets Tijd-aan-levende (TTL) gidsen
description: Datasets Time-to-live guardrails in  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: platform, data Lake, create, Lake, datasets, profile
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: 6233fcb466e741fd7eb912e6c59c8daf030f71a0
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 1%

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
| Dataset voor entiteitsgebeurtenis | 13 maanden | nvt |
| Journeys | 13 maanden | nvt |
| Gebeurtenissen reisstap | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Aangepaste aanbiedingen | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Alternatieve aanbiedingen | 13 maanden | nvt |
| Beslissingsobjectrepository - Plaatsingen | 13 maanden | nvt |
| Beslissingsobjectopslagplaats - Activiteiten | 13 maanden | nvt |
| Ervaar het Beslissen van de Bewaarplaats van Objecten - De Persoonlijke Punten van de Aanbieding | 13 maanden | nvt |
| ODE-beslissingsgebeurtenissen - prodbeslissing | 13 maanden | nvt |

## Veelgestelde vragen {#faq}

U zult onder Veelgestelde Vragen over datasets tijd-aan-levende (TTL) vinden.

Wilt u meer details? Gebruik terugkoppelen opties bij de bodem van deze pagina om uw vraag op te roepen, of met [&#x200B; gemeenschap van Adobe Journey Optimizer &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"} te verbinden.

+++Zal deze wijziging alleen van toepassing zijn op productiesandboxen of zal deze ook van toepassing zijn op dev-sandboxen?

Deze wijziging is van toepassing op alle sandboxtypen.

+++

+++Worden profielen zelf beïnvloed voor de 90 dagen-TTL in de profielopslag?

De door het systeem gegenereerde gegevenssetgegevens in het profiel worden na 90 dagen verwijderd, niet de profielen zelf.

+++

+++Als een door het systeem gegenereerde gegevensset wordt doorgegeven aan [!DNL Customer Journey Analytics] (CJA), zullen de gegevens in CJA ook door de TTL worden beïnvloed?

Gegevens in [!DNL Customer Journey Analytics] blijven gesynchroniseerd met Experience Platform. Daarom zal een verwijdering van gegevens toe te schrijven aan een TTL op systeem-geproduceerde datasetgegevens ook de gegevens in [!DNL Customer Journey Analytics] beïnvloeden.

+++

+++ Kunnen klanten TTL voor [!DNL Journey Optimizer] gegevens van de systeemdataset in profielopslag verhogen? 

De uitbreidingen van TTLs worden momenteel niet gesteund. Het is echter de bedoeling dat het TTL-proces wordt geoptimaliseerd zodat deze verlengingsverzoeken soms vanaf de tweede helft van 2025 kunnen worden ingediend.

>[!NOTE]
>
>Voor gegevens die in het profiel zijn opgeslagen, geldt de machtiging Totaal gegevensvolume. Elke toename van de gegevensopslag op het profiel als gevolg van een uitbreiding van de TTL zou daarom in mindering worden gebracht op de machtiging Totaal gegevensvolume. [&#x200B; leer meer &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=nl-NL){target=_blank}

+++

+++Kunnen klanten TTL voor [!DNL Journey Optimizer] de gegevens van de systeemdataset in gegevenshoop verhogen? 

De uitbreidingen van TTLs worden momenteel niet gesteund. De klanten kunnen gegevens door Doelen uitvoeren om gegevens langer te behouden. [&#x200B; leer meer &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=nl-NL){target=_blank} . Bovendien kunnen klanten met een machtiging **[!DNL Data Distiller]** afgeleide gegevenssets maken om de gegevens in het gegevensmeer op te slaan zonder een TTL. [&#x200B; leer meer &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++Zullen de TTL&#39;s invloed hebben op de volgende mogelijkheden? 

* **Opzoeken opslag**: Nr
* **Afbakening van de Reis**: Nr
* **Aanbieding die** begrenzen: Nr
* **verzendt de Optimalisering van de Tijd (STO)**: Nr
* **het frequentietoewijzing van het Bericht** (d.w.z., Bedrijfs regels): Nr
* **Meldend**: Nr

  >[!NOTE]
  >
  >Een TTL wordt reeds uitgevoerd op de [!DNL Customer Journey Analytics] (CJA) verbinding, die effectieve maximum terugblik periode van beïnvloede datasetgegevens tot 13 maanden vermindert.

* **Experience Platform gegevensbron**: Niet van toepassing - de gebeurtenisherwinning van de Ervaring wordt niet gesteund via gegevensbronnen.
* **Berekende attributen**: Ja - de aanvankelijke backfill berekening zal tot laatste 90 dagen van gegevens worden beperkt; gegevens verwerkte attributen zullen op stijgende gebeurtenissen voor verdere updates worden bijgewerkt. Zodra de volgende updates de terugkijkperiode (maximum 6 maanden) bereiken, beïnvloedt TTL hoofdzakelijk niet meer het gegevens verwerkte attribuut. Meer weten?
* **Segmentatie en het opnieuw richten**: Ja - de segmentatie is afhankelijk van gegevens in de profielopslag; daarom, is terugblik beperkt tot 90 dagen op beïnvloede datasetgegevens.
* **het Volgen**: Ja - vermindert effectieve maximum terugblik periode van beïnvloede datasetgegevens tot 90 dagen. Gegevens uit beïnvloede datasets blijven 13 maanden in data Lake.

+++

+++Welke timestamp wordt gebruikt voor de handhaving van TTL (b.v., voor backfill gebruiksgevallen)? 

De tijdstempel van de gebeurtenis wordt gebruikt (dus niet de innamedatum).

+++

+++Hoe beïnvloedt de nieuwe TTL gebruiksgevallen die langere gegevensbewaring vereisen (bijvoorbeeld, exclusief profielen die een e-mail in de afgelopen 120 dagen hebben ontvangen, of het begrenzen van e-mails over een jaar)?

Het nieuwe beleid van TTL zal de terugblik periode voor systeem-geproduceerde datasetgegevens in de profielopslag beperken tot 90 dagen en in het gegevens meer tot 13 maanden. De gevallen van het gebruik die toegang tot gegevens na deze periodes vereisen zullen beïnvloed worden. Bijvoorbeeld, zal de publiekssegmentatie of de frequentie die op gebeurtenissen worden gebaseerd ouder dan 90 dagen in de profielopslag niet meer mogelijk zijn gebruikend systeemdatasets.

+++

+++Welke alternatieven zijn beschikbaar om gegevens langer te bewaren dan de GVTO?

Klanten die langer moeten worden bewaard, moeten overwegen relevante gegevens van AJO-gegevenssets naar externe opslag te exporteren voordat de GVTO-vervaldatum verloopt. Adobe Journey Optimizer ondersteunt het exporteren van gegevenssets naar verschillende cloudopslagbestemmingen (Amazon S3, Azure Blob, Google Cloud Storage, enz.). [&#x200B; leer meer &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=nl-NL){target=_blank}

+++

+++Wat moeten klanten doen om zich voor te bereiden op de verandering van TTL?

* Herzie uw gebruiksgevallen en identificeer om het even welke die gegevensbehoud voorbij nieuwe TTLs vereisen.
* Opstelling geautomatiseerde vragen om kritieke gegevens naar afgeleide datasets te kopiëren alvorens het gegeven wordt geschrapt.
* Werk samen met uw Adobe-vertegenwoordiger om eventuele extra behoeften of mogelijke TTL-uitbreidingen (gepland voor toekomstige versies) te bespreken.

+++

+++Zullen klanten worden geïnformeerd alvorens TTL op bestaande zandbakken wordt afgedwongen?

Ja, betrokken klanten zullen vooraf op de hoogte worden gesteld, en het productteam zal met hen samenwerken om een vlotte overgang te verzekeren.

+++Kan ik door het Journey Optimizer-systeem gegenereerde gegevenssets verwijderen?

Door het Journey Optimizer-systeem gegenereerde gegevenssets zijn beveiligd en kunnen niet worden verwijderd via de standaard Adobe Experience Platform-gebruikersinterface. Deze datasets zijn essentieel voor de functionaliteit van Journey Optimizer en worden beheerd door het systeem.

Als u een gegevensset van een Journey Optimizer-systeem permanent moet verwijderen (bijvoorbeeld voor QA-omgevingen, opschonen van sandboxen of specifieke vereisten voor gegevenshygiëne), neemt u contact op met Adobe Engineering of Adobe Customer Care. Deze datasets vereisen gespecialiseerde backendprocedures om volledige en veilige verwijdering te verzekeren.

>[!NOTE]
>
>Voor routinematige gegevensopruiming binnen deze systeemdatasets, gebruik **[!UICONTROL Data Lifecycle]** verrichtingen beschikbaar door Privacy Service om specifieke verslagen of identiteiten te schrappen. [Meer informatie](../privacy/data-hygiene.md)


+++
