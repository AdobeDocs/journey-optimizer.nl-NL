---
solution: Journey Optimizer
product: journey optimizer
title: Aanbevolen procedures voor Journey Optimizer
description: Meer informatie over tips en trucs voor Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 271fb85d-5621-4a12-b3d1-65cf6021b174
source-git-commit: 6c73a1ee024ca61b30d71e77268e51b93576ae62
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 0%

---

# Best practices {#best-practices}

## Gebruiksscenario en omnichannel verpersoonlijkheidsbegeleiding in realtime {#real-time-guidance}

Na de update van Identiteitsdienst 2.0, is het stitching in real time van de identiteit geëvolueerd.

Adobe Journey Optimizer gebruikt de Identity Service om profielen samen te voegen en ervaringen voor de gebruiker aan te passen. Dientengevolge, zijn er sommige belangrijke aspecten aan de dienst om zich van bewust te zijn aangezien u uw gebruiksgevallen bouwt. Als merk wil je iemand een ervaring bieden. De identiteitsgrafiek laat marketers toe om te begrijpen welke apparaten een persoon met over diverse kanalen wordt geassocieerd. De grafiek kan identiteiten bevatten die een persoon (CRMID) of Webbrowser (ECID) vertegenwoordigen. De identiteitsdienst hecht deze informatie samen, die de verwezenlijking van een &quot;360 graadmening&quot;van een persoon, of een samengevoegd profiel toelaat. Betekenis dat wanneer iemand naar uw site bladert en zich vervolgens aanmeldt, alle eerdere gegevens van die sessie aan de aanmeldingsgebruiker kunnen worden gekoppeld. Deze actie vindt in een paar verschillende stappen plaats:

1. Eerste stitching van identiteiten - wanneer een persoon zich aanmeldt, wordt de login-id (CRMID) gekoppeld aan de webbrowser-id (web- of mobiele app-sessie):

   * Dit kan 30 min - 4 uur duren.
   * Gewoonlijk genereert deze aanmeldingsgebeurtenis een identiteitsgrafiek die een koppeling vormt tussen CRMID en ECID.

1. Na de eerste stitching, zullen om het even welke gegevens die met één van beide identiteiten worden verzonden worden geassocieerd aan het samengevoegde profiel en beschikbaar voor verpersoonlijking in Journey Optimizer in real time. Het bijwerken van het profiel met de meest recente gedragsgegevens kan 1 minuut duren. Verwijs naar deze [&#x200B; pagina &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=nl).

Houd rekening met het volgende wanneer u gebruikszaken maakt:

1. Het merk wil 30 minuten na het verlaten van de site opnieuw een bezoeker van de site inschakelen (bijvoorbeeld verlaten e-mail met winkelwagentje):

   Gebruik de identiteit met de gegevens - ECID. Als u 100% wilt vastleggen van bezoekers die hun e-mailadres/app-installatie in de laatste 30 minuten hebben gegeven, moet u de op cookies gebaseerde identiteit gebruiken om deze reis (ECID) te starten. Hierbij wordt ervan uitgegaan dat uw e-mailadres of pushtoken of ander adres voor de ervaring aan de ECID is gekoppeld.

1. Omnichannel betrokkenheid bij web, e-mail, push, enz.:

   * U moet de adressen voor mededeling beschikbaar op het profiel op tijd van overeenkomst hebben. Om ervoor te zorgen dat dit consistent en tijdig gebeurt, moet u ervoor zorgen dat uw gegevens zijn gekoppeld aan de identiteit die u wilt gebruiken.
   * Als u informatie van een onlangs geïnstalleerde app of browser zitting met bekende of het programma geopende informatie moet gebruiken, moet deze mededeling worden verzonden nadat het verbinden van deze identiteiten is voorgekomen. Dit kan per klant variëren en wij moedigen het wachten aan minstens 30 minuten om hoogste volume van profielen te krijgen.

## Schalen met reisinstructies {#scale}

In deze sectie wordt uitgelegd hoe u kunt schalen met de volgende twee beperkingen:

* Journey Optimizer heeft een grip op 50 activiteiten op een reiscanvas. Deze handleiding is ontworpen om te helpen bij leesbaarheid, kwaliteitscontrole en probleemoplossing. Het aantal activiteiten in een reis zal in de hogere linkersectie van het reiscanvas verschijnen wanneer u binnen 10 activiteiten van deze grens komt.

* Tijdens het publiceren van reizen wordt Journey Optimizer automatisch geschaald en aangepast om een maximale doorvoer en stabiliteit te garanderen. Zoals u bij de mijlpaal van 100 live reizen in één keer in een sandbox, ziet u een oranje overlay en een waarschuwingsteken in de interface over deze prestatie. Als u deze melding ziet en uw reizen moet verlengen tot meer dan 100 rechtstreekse reizen tegelijk, maak dan een ticket voor de klantenservice en wij helpen u uw doelstellingen te bereiken.

<!--DOCAC-10977

* As you publish journeys, Journey Optimizer automatically scales and adjusts to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time in a sandbox, you will see an orange overlay and warning sign appear in the interface on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->


Er zijn een aantal beste praktijken die u kunt aannemen, die u helpen binnen de grenzen blijven en het systeem efficiënt gebruiken.

* Als u uw grens van levende reizen nadert, de eerste stap u kunt nemen is naar het **Overzicht** lusje onder **Reizen** te gaan om te zien hoeveel reizen binnen de laatste 24 uren actief waren die actieve profielen hadden. U kunt het aantal profielen controleren dat de reis in deze sectie binnengaat en weggaat om dat te bepalen.

  ![](assets/journey-guardrails2.png)

* Vervolgens kunt u in het gedeelte Reisinventarisatie alle reizen filteren op Status = &quot;Live&quot; en Type = &quot;Leespubliek&quot;. Sorteer vervolgens op publicatiedatum (oudste naar nieuwste). Klik op de reis en ga naar het schema. Stop alle levende reizen die een programma hadden om **te lopen** of **&lbrace;zo spoedig mogelijk** die ouder zijn dan een dag en slechts één actie hebben.

  ![](assets/journey-guardrails1.png)

* Als uw **leest publiek** reis enkel één actie heeft, wacht geen/besluiten, of verzendt tijdoptimalisering, denk na bewegend hen aan de Campagnes van Journey Optimizer. Campagnes zijn beter geschikt voor eenstapsbetrokkenheid. Een van de belangrijkste verschillen tussen Campagne en Journaal is of u het belangrijk vindt om actief naar de betrokkenheid van de gebruiker te luisteren om de volgende stap te bepalen en met een andere actie in gesprek te gaan.
* Om het aantal activiteiten binnen een reis te verminderen, controleer de voorwaardenstappen. Er zullen vele gevallen zijn waar u de voorwaarden in segmentdefinitie of publiekssamenstelling kunt bewegen.
* Als dezelfde omstandigheden zich bij meerdere reizen herhalen (toestemmingscontroles, onderdrukking), kunt u overwegen deze als onderdeel van de segmentdefinitie te verplaatsen. Als u bijvoorbeeld een voorwaarde hebt om te controleren of het e-mailadres niet leeg is voor meerdere reizen, moet u die voorwaarde opnemen in de segmentdefinitie.
* Als uw reis verscheidene voorwaarden heeft die het publiek verdelen om de aantallen bij elke stap te zien, overweeg het gebruiken van Customer Journey Analytics of een andere rapporteringsoplossing die voor analyse geschikter zijn.
* Als u de limiet van knooppunten op het canvas bijna bereikt, kunt u overwegen om acties te consolideren met dynamische parameters of inhoud om de juiste inhoud te leveren in plaats van expliciete knooppunten.

* Als u de reis van het publiek van het a **Gelezen** met partijsegment (A) hebt en u een inAudience die segment (B) binnen de reis gebruikt om uit te sluiten (d.w.z., A-B) uitvoeren, denk na bewegend die logica aan de segmenteringslogica en gebruik de uitsluiting als deel van de segmenteringslogica zelf.