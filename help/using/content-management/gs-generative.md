---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met AI Assistant in Journey Optimizer
description: Leer toegang tot en werk met AI Assistant in Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 5063115c6ac93ef332044bfff43a4df817a1a4e3
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 2%

---

# Aan de slag met AI Assistant {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI Assistant in Journey Optimizer"
>abstract="Zodra u uw levering hebt gemaakt en gepersonaliseerd, kunt u de AI Assistant in Journey Optimizer gebruiken om uw inhoud te verbeteren. Deze functie vereenvoudigt het proces van personalisatie en inhoudverbetering door u toe te staan om de inhoud te verfijnen door te beschrijven wat u wilt produceren."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Brontent uploaden"
>abstract="Met het menu Brontent uploaden kunt u elk merkelement toevoegen dat inhoud bevat die extra context kan bieden voor AI Assistant in Journey Optimizer, of een eerder geüpload element selecteren. Deze optie zorgt ervoor dat AI Assistant toegang heeft tot alle noodzakelijke materialen om de functionaliteit en relevantie ervan te verbeteren."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe Generative AI-termen"
>abstract="Voor toegang tot deze functie moet u akkoord gaan met de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen. Controleer de nauwkeurigheid van de uitvoer van deze functie en zorg ervoor dat deze geschikt is voor uw gebruiksscenario."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe Generative AI-gebruikersrichtlijnen"

>[!INFO]
>
>Ga in een hands-on ervaring met [&#x200B; binnen onze levende eigenschapvoorproef &#x200B;](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, die wordt ontworpen om u zijn eigenschappen te laten onderzoeken en volledig zijn mogelijkheden te begrijpen.


De AI Assistant in Adobe Journey Optimizer, die wordt aangedreven door Microsoft Azure OpenAI en Adobe Firefly, biedt proactieve suggesties voor wijzigingen in inhoud voor tekst en afbeeldingen. Dit nieuwe vermogen verstrekt a **herinnering gebaseerde tekst en beeldgeneratie**. Het genereren van afbeeldingen wordt beheerd met Adobe Firefly.

De Medewerker van AI steunt generatie **in veelvoudige talen** toelatend u om diverse globale publiek te bereiken en in dienst te nemen. AI Assistant is beschikbaar in de volgende talen:

<table style="table-layout:fixed; margin-top: 0px; margin-bottom: 0px;">
  <tbody>
    <tr style="border: 0;background-color: #FFFFFF;">
      <td>
        <ul>
          <li>Frans</li>
          <li>Spaans</li>
          <li>Duits</li>
          <li>Italiaans</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Japans</li>
          <li>Zweeds</li>
          <li>Nederlands</li>
          <li>Noors</li>
        </ul>
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

Met AI Assistant in Adobe Journey Optimizer optimaliseert u de impact van uw bericht door te experimenteren met verschillende hoofdtitels en -afbeeldingen. Genereer meerdere varianten en maak een experiment om ze te vergelijken. De hefboomwerkende **Experimenteer van de Inhoud van Journey Optimizer**, kunt u veelvoudige berichtbehandelingen bepalen om te meten welke het beste voor uw doelpubliek presteert. U kunt kiezen om de leveringsinhoud, of onderwerp te variëren. Het berichtpubliek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke één het beste in termen van gespecificeerde metrisch werkt. Leer meer over de Experimenteer van de Inhoud in [&#x200B; deze sectie &#x200B;](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Alvorens te beginnen gebruikend dit vermogen, lees verwante [&#x200B; Grafieken en Beperkingen &#x200B;](#generative-guardrails).
>
>
>* U moet met a [&#x200B; gebruikersovereenkomst &#x200B;](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} akkoord gaan alvorens u AI Medewerker in Adobe Journey Optimizer kunt gebruiken. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

## AI-assistent openen {#generative-access}

Om tot AI Medewerker in de eigenschap van Adobe Journey Optimizer toegang te hebben, moeten de gebruikers worden verleend **produceert de toestemming van de Inhoud**. [Meer informatie](../administration/permissions.md)

+++  Leer hoe u machtigingen voor het genereren van inhoud toewijst

1. In het **product van Toestemmingen**, ga naar het **lusje van Rollen** en selecteer de gewenste **Rol**.

1. Klik **uitgeven** om de toestemmingen te wijzigen.

1. Voeg het **AI Medewerker** middel toe, dan uitgezocht **produceer Inhoud** van het drop-down menu.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Klik **sparen** om veranderingen toe te passen.

   Voor alle gebruikers die al zijn toegewezen aan deze rol, worden hun machtigingen automatisch bijgewerkt.

1. Om deze rol aan nieuwe gebruikers toe te wijzen, navigeer aan het **lusje van Gebruikers** binnen het **dashboard van Rollen** en klik **toevoegen Gebruiker**.

1. Ga de naam van de gebruiker, e-mailadres in, of kies van de lijst, dan klik **sparen**.

1. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [&#x200B; deze documentatie &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

De gebruiker ontvangt een e-mail met instructies om toegang te krijgen tot uw exemplaar.

+++

## Afvoerkanalen en beperkingen {#generative-guardrails}

De algemene richtlijnen voor het gebruik van AI Assistant in Adobe Journey Optimizer voor het genereren van e-mail worden hieronder weergegeven:

* De kwaliteit van de gegenereerde inhoud wordt sterk beïnvloed door het marketingdoel dat/de marketingprompt die u definieert. Gebruik een duidelijk gedefinieerde prompt voor een juiste interpretatie van het GenAI-model. 
* Upload merkmiddelen voor nauwkeurige informatie over de inhoud van het merk. Anders is de inhoud gebaseerd op algemeen beschikbare informatie. De geüploade inhoud kan de volgende indelingen hebben: PDF-, JPEG-, PNG- of ZIP-bestanden (met ondersteunde bestandsindelingen).
* De maximale grootte voor geüploade brandmiddelen is 50 MB. Grotere bestanden of veel afbeeldingen kunnen werken, maar de verwerkingstijd neemt toe.
* Gebruik een merkspecifieke of aangepaste sjabloon om uw e-mailinhoud te maken met AI Assistant in Adobe Journey Optimizer. E-mailsjablonen met maximaal 8-10 afbeeldingen worden aanbevolen.
* Zorg ervoor dat u eventuele problematische uitvoerbestanden meldt met het blokje omhoog, omlaag of de vlagpictogrammen bij het selecteren van varianten.
* Op uw gebruik van AI Assistant zijn de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen van toepassing. [Meer informatie](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Als onderdeel van de toezegging van Adobe om de transparantie bij het gebruik van generatieve AI-tools bij het maken van media te bevorderen, zal Adobe Content Credentials toepassen wanneer inhoud of een project dat een door Firefly gegenereerd element bevat, wordt gedownload of geëxporteerd. [Meer informatie](https://helpx.adobe.com/firefly/using/content-credentials.html)

De volgende beperkingen gelden voor AI Assistant in Adobe Journey Optimizer:

* Alleen beschikbaar voor de e-mail-, push-, web- en sms-kanalen.
* GenAI-inhoud is mogelijk niet altijd correct: geef uw feedback zodat onze technici de modellen kunnen verfijnen.
* U kunt meerdere merkmiddelen uploaden, maar u kunt slechts één voor een specifieke generatie gebruiken.


## Mogelijkheden voor het genereren van inhoud voor AI Assistant {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="E-mailgeneratie" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong> E-mailgeneratie </strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="SMS-generatie" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong> generatie van SMS </strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Push generation" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong> de generatie van het pushbericht </strong></a>
</div>
<p></td>
<td>
<a href="generative-web.md">
<img alt="Webgeneratie" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong> Web-pagina generatie </strong>
</div>
<p>
</td>
</tr></table>

## Aanvullende bronnen

* **[AI Medewerker voor e-mail](generative-email.md)** - Leer hoe te om de Medewerker van AI te gebruiken om e-mailinhoudvariaties te produceren en te optimaliseren.
* **[AI Medewerker voor dupberichten](generative-push.md)** - ontdek hoe te om het dwingen inhoud van het pushbericht met AI hulp tot stand te brengen.
* **[AI Medewerker voor SMS](generative-sms.md)** - produceer efficiënte het berichtvariaties van SMS gebruikend AI-Aangedreven inhoudsverwezenlijking.
* **[AI Medewerker voor Webervaringen](generative-web.md)** - Leer hoe te om Webinhoud met AI Medewerker tot stand te brengen en te optimaliseren.
* **[Generatieve experimentatie](generative-experimentation.md)** - begrijp hoe te om AI-Gegenereerde inhoud met experimenteren te combineren.
* **[&#128279;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/ai-assistant){target="_blank"} de Hulpleerprogramma&#39;s van 1&rbrace; AI** - Onderzoek geleidelijke videoleerprogramma&#39;s op AI Hulpeigenschappen en beste praktijken.
