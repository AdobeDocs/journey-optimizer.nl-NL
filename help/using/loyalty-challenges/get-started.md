---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met Loyalty Challenges
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen kunt maken en beheren om aansprekende loyaliteitsprogramma's op te bouwen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
source-git-commit: 17d7cf7ae18ff987b7a9c9bebdec44b354ed11da
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Aan de slag met Loyalty Challenges {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* **wordt begonnen met de Uitdagingen van de Loyalty** {2 }︎ ◀ u hier **bent**
* [Toegang tot en beheer uitdagingen en taken](access-loyalty-challenges.md)
* [Uitdagingen maken](create-challenges.md)
* [Taken maken](create-tasks.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta**. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Overzicht {#overview}

De Uitdagingen van de Loyalty laten u toe om het in dienst nemen, gokken loyaliteitsprogramma&#39;s tot stand te brengen die klantengedrag drijven en merkverhoudingen te verdiepen. Bouw uitdagingen die klanten voor specifieke acties belonen—van het maken van aankopen en het schrijven van revisies tot het engageren op sociale media en het verwijzen van vrienden.

Met Loyalty Uitdagingen, kunt u:

* **flexibele de uitdagingstypes van het Ontwerp**: Creeer Standaard, Streak, of Opeenvolgende uitdagingen om uw bedrijfsdoelstellingen aan te passen
* **vorm strategisch beloningen**: Lever punten bij taakmijlpalen of op volledige voltooiing om overeenkomst te handhaven
* **personaliseer de ervaring**: De inhoudskaarten van het gebruik en multi-kanaaloverseinen om onderdompelde, brandde ervaringen tot stand te brengen
* **integreer foutloos**: verbind met uw bestaande loyaliteitsleveranciers en hefboomwerkingExperience Platform gegevens
* **Spoor automatisch**: De vooruitgang van de klant door auto-geproduceerde reizen zonder douaneontwikkeling

![](assets/challenges-gs.png)

U kunt drie soorten uitdagingservaringen tot stand brengen:

* **Standaard uitdagingen**: De klanten voltooien om het even welk gespecificeerd aantal taken in om het even welke orde. Gebruik dit type als u de flexibiliteit en meerdere paden wilt voltooien.\
  *Voorbeeld: &quot;De Uitdaging van de Wellness van de Zomer&quot;- Voltooi 3 van 5 taken: koop gezondheidsproducten, aandeel op sociale media, verwijs een vriend, schrijf een overzicht, of ben een virtuele gebeurtenis* bij

* **de uitdagingen van de Streak**: De klanten voltooien achtereenvolgens de zelfde taak veelvoudige tijden. Gebruik dit type om consistent, herhaald gedrag in de loop van de tijd aan te moedigen.\
  *Voorbeeld: &quot;Week van Koffie Lover&quot;- Koop koffieproducten voor 7 opeenvolgende dagen om een vrije drankenbeloning te ontgrendelen*

* **Opeenvolgende uitdagingen**: De klanten voltooien taken in een bepaalde orde. Gebruik dit type om klanten door een specifieke reis of een onboarding proces te begeleiden.\
  *Voorbeeld: &quot;Nieuwe Reis van het Lid&quot; - meld u aan voor e-mails → Maak uw eerste aankoop → Schrijf een productoverzicht → vernieuw een vriend (volledig in deze nauwkeurige orde)*

## Werking {#how-it-works}

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **creeer een uitdaging** - bepaal de basisuitdagingseigenschappen, met inbegrip van naam, type (Norm, Streak, of Opeenvolgend), en datumwaaier.

1. **voegt taken** toe - bepaal de specifieke acties klanten moeten voltooien, met inbegrip van taaktypes (aankoop, uitgeven), hoeveelheden, productfilters, en beloningen.

1. **de inhoudskaarten van het Ontwerp** - creeer de visuele vertegenwoordiging van uw uitdaging gebruikend de inhoudskaarten van Journey Optimizer die op klantenapparaten tonen. De kaarten van de inhoud tonen uitdagingsinformatie, vooruitgang, en beloningen.

1. **vorm overseinen** (facultatief) - opstelling multi-kanaalberichten (in-app, e-mail, duw) voor zeer belangrijke levenscyclusstadia: lancering, in-lopend, en voltooiing.

1. **Uitgezochte doelpubliek** - bepaal welke klanten aan uw uitdaging kunnen deelnemen door een publiek van Adobe Experience Platform te selecteren.

1. **Lancering de uitdaging** - publiceer de uitdaging, dan produceer een reis. Journey Optimizer maakt automatisch de reis voor je uitdaging. Publiceer de auto-geproduceerde reis om de uitdaging voor klanten ter beschikking te stellen.

Voor gedetailleerde geleidelijke instructies, zie [&#x200B; uitdagingen &#x200B;](create-challenges.md) creëren.

## Vereisten {#prerequisites}

Voordat u Loyalty Challenges gaat gebruiken, moet u controleren of u beschikt over:

+++Vereiste machtigingen

Als u Loyalty Challenges wilt gebruiken, hebt u de juiste machtigingen nodig in Journey Optimizer en Adobe Experience Platform.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Neem contact op met de beheerder als u geen toegang hebt tot de functie of aanvullende machtigingen nodig hebt.

+++

+++Doelgroep

Zorg ervoor dat het doelpubliek dat u nodig hebt, bestaat in Adobe Experience Platform voordat u de uitdaging aanbrengt. Tijdens uitdagingsconfiguratie, zult u het publiek selecteren dat bepaalt welke klanten verkiesbaar zijn om deel te nemen. [&#x200B; Leer hoe te met publiek &#x200B;](../audience/about-audiences.md) te werken.

+++

## Laten we dieper duiken {#lets-dive-deeper}

Nu je weet wat Loyalty Challenges zijn en hoe ze werken, is het tijd om in de details te duiken. Onderzoek de volgende onderwerpen om tot de interface toegang te hebben, creeer uw eerste uitdaging, en bepaal de taken uw klanten zullen voltooien.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Toegang" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong> toegang &amp; beheer uitdagingen en taken </strong></a>
    </div>
    <p>
    <em> Leer hoe te om tot de inventaris toegang te hebben en uitdagingen en taken te beheren </em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Maken" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong> creeer uitdagingen </strong></a>
    </div>
    <p>
    <em> Leer hoe te om uw eerste loyaliteitsuitdaging te bouwen en te vormen </em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="Taken" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong> creeer taken </strong></a>
    </div>
    <p>
    <em> Leer hoe te om taken te bepalen die de klanten voor uitdagingen </em> voltooien
    </p>
  </td>
</tr>
</table>
