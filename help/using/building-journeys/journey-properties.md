---
solution: Journey Optimizer
product: journey optimizer
title: De eigenschappen van uw reis definiëren
description: Leer hoe u eigenschappen van uw reis met Adobe Journey Optimizer instelt
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, configuratie, eigenschappen
source-git-commit: 67032a4bcbfd56552d783f3ef78593375bfcc378
workflow-type: tm+mt
source-wordcount: '1560'
ht-degree: 0%

---

# De eigenschappen van uw reis instellen {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journeyeigenschappen"
>abstract="In dit gedeelte worden de eigenschappen van de reis weergegeven. Standaard zijn alleen-lezen parameters verborgen. Welke instellingen beschikbaar zijn, is afhankelijk van de status van de rit, van uw machtigingen en de productconfiguratie."

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Criteria voor het verlaten van de reis"
>abstract="In dit gedeelte worden de opties voor afsluitcriteria weergegeven. U kunt één of veelvoudige regels van de uitgangscriteria voor uw reis tot stand brengen."

Reiseigenschappen zijn gecentraliseerd in de rechtertrein van de reis. Deze sectie wordt standaard weergegeven wanneer u een nieuwe reis maakt. Voor bestaande reizen klikt u op het potloodpictogram naast de naam van de reis om de eigenschappen ervan te openen.


Gebruik deze sectie om de naam van de reis in te stellen, een beschrijving toe te voegen en:

* beheren [binnenkomst en wedertoetreding](#entrance),
* begin en einde kiezen [datums](#dates),
* beheren [toegang tot gegevens](#manage-access),
* een [tijdsduur time-out](#timeout) bij reisactiviteiten (alleen voor Admin-gebruikers);
* de reis en het profiel selecteren [tijdzones](#timezone)
* Wijs Adobe Experience Platform Verenigde Markeringen aan uw reis toe, om hen gemakkelijk te classificeren en onderzoek van de campagnemelijst te verbeteren. [Leer hoe u met tags kunt werken](../start/search-filter-categorize.md#tags)

![](assets/journey32.png)

>[!NOTE]
>
>Voor live reizen worden in dit scherm alleen de publicatiedatum en de naam van de gebruiker weergegeven die de reis heeft gepubliceerd.

De **Technische details kopiëren** staat u toe om technische informatie over de reis te kopiëren die het steunteam kan gebruiken om problemen op te lossen. De volgende informatie wordt gekopieerd: `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt`.


## Entrance en re-entry {#entrance}

Nieuwe reizen zijn standaard geschikt voor herbinnenkomst. U kunt de controle van **Hernieuwde toegang toestaan** optie voor &quot;één enkele schot&quot;reizen, bijvoorbeeld als u een eenmalig geschenk wilt aanbieden wanneer een persoon een winkel ingaat.

Wanneer de **Hernieuwde toegang toestaan** -optie is geactiveerd, de **Wachttijd bij terugkeer** wordt weergegeven. In dit veld kunt u de tijd definiëren die u moet wachten voordat u een profiel toestaat om de reis opnieuw te betreden tijdens een enkele reis (te beginnen met een evenement of een publiekskwalificatie). Hierdoor wordt voorkomen dat ritten meerdere keren ten onrechte worden geactiveerd voor dezelfde gebeurtenis. Het veld wordt standaard ingesteld op 5 minuten. De maximale duur is 29 dagen.

Meer informatie over toegang tot profielen en beheer van nieuwe toegang, in [deze sectie](entry-management.md).

## Toegang beheren {#manage-access}

Als u aangepaste of basislabels voor gegevensgebruik aan de reis wilt toewijzen, klikt u op de knop **[!UICONTROL Manage access]** knop. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## Tijdzones voor reizen en profielen {#timezone}

De tijdzone wordt gedefinieerd op het niveau van de reis. U kunt een vaste tijdzone invoeren of Adobe Experience Platform-profielen gebruiken om de tijdzone van de reis te definiëren. Als een tijdzone in Adobe Experience Platform-profiel is gedefinieerd, kan deze tijdens de reis worden opgehaald.

Zie voor meer informatie over tijdzonebeheer [deze pagina](../building-journeys/timezone-management.md).

## Begin- en einddatum {#dates}

U kunt een **Begindatum**. Als u er geen hebt opgegeven, wordt deze automatisch gedefinieerd op het moment van publicatie.

U kunt ook een **Einddatum**. Hiermee kunnen profielen automatisch worden afgesloten wanneer de datum wordt bereikt. Als er geen einddatum is opgegeven, kunnen profielen blijven tot de [algemene time-out](#global_timeout) (over het algemeen 91 dagen, en met de toevoeging aan het gezondheidsschild tot 7 dagen teruggebracht). De enige uitzondering is terugkerende publiekstrajecten met **Herkomst forceren bij herhaling** geactiveerd, die eindigt op de begindatum van het volgende exemplaar.

## Time-out {#timeout}

### Time-out of fout bij reisactiviteiten {#timeout_and_error}

Wanneer u een actie of voorwaardenactiviteit bewerkt, kunt u een alternatief pad definiëren in het geval van een fout of time-out. Als de verwerking van de activiteit die een derdensysteem ondervraagt de tijdsduur overschrijdt die in **[!UICONTROL Timeout or error]** op het terrein van de eigenschappen van de reis zal het tweede pad worden gekozen om een mogelijke terugvalactie uit te voeren .

Toegestane waarden liggen tussen 1 en 30 seconden.

We raden u aan om een zeer korte definitie te geven **[!UICONTROL Timeout or error]** waarde als uw reis tijdgevoelig is (bijvoorbeeld: het reageren op de plaats in real time van een persoon) omdat u uw actie niet meer dan een paar seconden kunt vertragen. Als uw reis minder tijdgevoelig is, kunt u een langere waarde gebruiken om meer tijd aan het geroepen systeem te geven om een geldige reactie te verzenden.

Reizen gebruiken ook een wereldwijde time-out, zoals hieronder wordt beschreven.

### Globale time-out voor transport {#global_timeout}

Naast de [timeout](#timeout_and_error) wordt gebruikt in reisactiviteiten, wordt een globale reis timeout toegepast. Het wordt niet getoond in de interface en kan niet worden veranderd.

Door deze wereldwijde time-out wordt de voortgang van individuen tijdens de reis gestopt **91 dagen** nadat ze zijn binnengekomen. Deze time-out wordt beperkt tot **7 dagen** met de toevoeging aan het gezondheidsschild. Dit betekent dat de reis van een individu niet langer mag duren dan 91 dagen (of 7 dagen). Na deze time-outperiode worden de gegevens van de persoon verwijderd. Personen die aan het einde van de time-outperiode nog onderweg zijn, worden gestopt en er wordt geen rekening mee gehouden bij de rapportage. Je zou dus meer mensen op de reis zien komen dan vertrekken.

>[!NOTE]
>
>De reizen reageren niet direct op privacy opt-out, toegang of schrappingsverzoeken. De wereldwijde time-out zorgt er echter voor dat individuen nooit langer dan 91 dagen op een reis blijven.

Vanwege de reistijd van 91 dagen, wanneer het niet is toegestaan om de reis opnieuw te betreden, kunnen we er niet voor zorgen dat het blokkeren van de terugkeer meer dan 91 dagen zal duren. Aangezien we alle informatie over personen die 91 dagen na hun binnenkomst de reis hebben betreden, verwijderen, kunnen we niet weten dat de persoon eerder, meer dan 91 dagen geleden, is binnengekomen.

Een individu kan alleen een wachtdienst doen als hij of zij genoeg tijd in de reis heeft om de wachttijd vóór de reisonderbreking van 91 dagen te voltooien. Zie [deze pagina](../building-journeys/wait-activity.md).


#### Time-to-live (TTL) en veelgestelde vragen over gegevensinvoer {#timeout-faq}

Vanaf de release van Adobe Journey Optimizer juni 2024 is de wereldwijde time-out van de reis van 30 naar 91 dagen gestegen. De gevolgen worden vermeld in de FAQ hieronder:

**Voor eenheidsreizen**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met de reis die wordt gepubliceerd na de introductie van de TTL-uitbreiding?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan, hebben automatisch een TTL van 91 dagen.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat een reis ingaat die vóór de lancering van de uitbreiding van TTL werd gepubliceerd?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) hebben, in overeenstemming met de tijd dat de reis oorspronkelijk werd gepubliceerd.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat al een reis is begonnen toen de uitbreiding van de TTL wordt gestart?</p>
    </td>
    <td>
      <p>Het profiel behoudt een TTL van 91 dagen (7 dagen voor HIPAA), volgens de oorspronkelijke publicatietijd van de reis.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel in een vorige reisversie dat opnieuw wordt gepubliceerd na de lancering van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) handhaven, die met de de publicatietijd van de originele reisversie wordt gericht.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een nieuw profiel dat een opnieuw gepubliceerde reisversie invoert na de introductie van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen hebben, die TTL van de onlangs opnieuw gepubliceerde reisversie aanpassen.</p>
    </td>
  </tr>
</table>

**Voor segmenttriggerreizen**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe eenmalige reizen die na de uitbreiding van de TTL worden gepubliceerd?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan zullen een TTL van 91 dagen automatisch hebben.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe terugkerende reizen zonder gedwongen terugkeer die na de uitbreiding van de GVTO worden gepubliceerd?</p>
    </td>
    <td>
      <p>Profielen die de nieuwe reis ingaan zullen een TTL van 91 dagen automatisch hebben.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met nieuwe terugkerende reizen met gedwongen terugkeer die na de uitbreiding van de GVTO worden gepubliceerd?</p>
    </td>
    <td>
      <p>De profielen die de nieuwe reis ingaan zullen een TTL gelijk aan de herhalingsperiode hebben. Bijvoorbeeld, als de reis dagelijks loopt, zal TTL 1 dag zijn.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat een reis ingaat die vóór de lancering van de uitbreiding van TTL werd gepubliceerd?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPAA) hebben, verenigbaar met de originele publicatietijd. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een profiel dat door een reis loopt wanneer de uitbreiding van TTL wordt gelanceerd?</p>
    </td>
    <td>
      <p>Het profiel behoudt een TTL van 91 dagen (7 dagen voor HIPAA), volgens de oorspronkelijke publicatietijd van de reis. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een lopend profiel in een vorige reisversie die opnieuw wordt gepubliceerd na de lancering van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen (7 dagen voor HIPPA) handhaven, die aan de originele de publicatietijd van de reisversie wordt aangepast. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Wat gebeurt er met een nieuw profiel dat een opnieuw gepubliceerde reisversie invoert na de introductie van de uitbreiding van TTL?</p>
    </td>
    <td>
      <p>Het profiel zal een TTL van 91 dagen hebben, die TTL van de onlangs opnieuw gepubliceerde reisversie aanpassen. Voor terugkerende ritten met gedwongen terugkeer zal de TTL overeenkomen met de herhalingsperiode.</p>
    </td>
  </tr>
</table>

## Beleid samenvoegen {#merge-policies}

Reis gebruikt samenvoegbeleid terwijl het terugwinnen van profielgegevens van Adobe Experience Platform. Afhankelijk van het type van reis, worden de verschillende samenvoegingsbeleidsvormen gebruikt:

* In kwalificatiereizen voor het publiek of het publiek lezen: het samenvoegbeleid van het publiek wordt gebruikt
* Bij Eenheidstijdvluchten wordt het standaard samenvoegbeleid gebruikt
* Bij zakenreizen: het samenvoegbeleid van het doelpubliek in de volgende Lees-publieksactiviteit wordt gebruikt

De reis zal het fusieprincipe respecteren dat door de volledige reis wordt gebruikt. Als er daarom meerdere soorten publiek worden gebruikt op een reis (bijvoorbeeld in &quot;inAudience&quot;-functies), waardoor inconsistenties ontstaan met het fusiebeleid dat door de reis wordt gebruikt, wordt een fout opgeworpen en wordt de publicatie geblokkeerd. Nochtans, als een inconsistent publiek in berichtverpersoonlijking wordt gebruikt, wordt een alarm niet opgeheven, ondanks de inconsistentie. Om deze reden, wordt het hoogst geadviseerd om het samenvoegbeleid te controleren verbonden aan uw publiek, wanneer dit publiek in berichtverpersoonlijking wordt gebruikt.

Raadpleeg voor meer informatie over samenvoegingsbeleid [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

