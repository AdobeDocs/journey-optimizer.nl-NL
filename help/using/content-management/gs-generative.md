---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met de AI Assistant in Journey Optimizer
description: Leer toegang tot en werk met AI Assistant in Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 5cfae89416219fac54d310d9fa3f40fdfdd8878e
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 1%

---

# Aan de slag met de AI Assistant {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI Assistant in Journey Optimizer"
>abstract="Zodra u uw levering hebt gemaakt en gepersonaliseerd, kunt u de AI Assistant in Journey Optimizer gebruiken om uw inhoud te verbeteren. Deze functie vereenvoudigt het proces van personalisatie en inhoudverbetering door u toe te staan om de inhoud te verfijnen door te beschrijven wat u wilt produceren."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Brontent uploaden"
>abstract="Met het menu Brand-element uploaden kunt u elk merkelement toevoegen dat inhoud bevat die extra context kan bieden voor de AI Assistant in Journey Optimizer, of een eerder geüpload element selecteren. Deze optie zorgt ervoor dat de AI Assistant toegang heeft tot alle noodzakelijke materialen om de functionaliteit en relevantie ervan te verbeteren."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe Generative AI-termen"
>abstract="Voor toegang tot deze functie moet u akkoord gaan met de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen. Controleer de nauwkeurigheid van de uitvoer van deze functie en zorg ervoor dat deze geschikt is voor uw gebruiksscenario."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe Generative AI-gebruikersrichtlijnen"

>[!INFO]
>
>Ga zelf in een hands-on ervaring met [ binnen onze levende eigenschapvoorproef ](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator) {target="_blank"}, die wordt ontworpen om u zijn eigenschappen te laten onderzoeken en volledig zijn mogelijkheden te begrijpen.


De AI Assistant in Adobe Journey Optimizer, die wordt aangedreven door Microsoft Azure OpenAI en Adobe Firefly, biedt proactieve suggesties voor wijzigingen in inhoud voor tekst en afbeeldingen. Het is beschikbaar voor e-mail, Push en SMS kanalen. Deze nieuwe functie biedt een snelle, op tekst en afbeeldingen gebaseerde productie. Het genereren van afbeeldingen wordt beheerd met Adobe Firefly.

Gebruik de AI-assistent in Adobe Journey Optimizer om de impact van uw bericht te optimaliseren door te experimenteren met verschillende hoofdtitels en -afbeeldingen. Genereer meerdere varianten en maak een experiment om ze te vergelijken. Als u gebruikmaakt van Journey Optimizer Content Experiment, kunt u meerdere berichtbehandelingen definiëren om te meten welke het beste presteert voor uw doelgroep. U kunt kiezen om de leveringsinhoud, of onderwerp te variëren. Het berichtpubliek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke één het beste in termen van gespecificeerde metrisch werkt. Leer meer over de Experimenteer van de Inhoud in [ deze sectie ](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Alvorens te beginnen gebruikend dit vermogen, lees uit verwante [ Grafieken en Beperkingen ](#generative-guardrails).
>
>
>* U moet met a [ gebruikersovereenkomst ](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) {target="_blank"} akkoord gaan alvorens u de Medewerker AI in Adobe Journey Optimizer kunt gebruiken. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

## De AI-assistent openen {#generative-access}

Om tot de AI Medewerker in de eigenschap van Adobe Journey Optimizer toegang te hebben, moeten de gebruikers **worden verleend produceert de toestemming van de Inhoud**. [Meer informatie](../administration/permissions.md)

+++  Leer hoe u machtigingen voor het genereren van inhoud toewijst

1. In het **product van Toestemmingen**, ga naar het **lusje van Rollen** en selecteer de gewenste **Rol**.

1. Klik **uitgeven** om de toestemmingen te wijzigen.

1. Voeg het **AI Medewerker** middel toe, dan uitgezocht **produceer Inhoud** van het drop-down menu.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Klik **sparen** om veranderingen toe te passen.

   Voor alle gebruikers die al zijn toegewezen aan deze rol, worden hun machtigingen automatisch bijgewerkt.

1. Om deze rol aan nieuwe gebruikers toe te wijzen, navigeer aan het **lusje van Gebruikers** binnen het **dashboard van Rollen** en klik **toevoegen Gebruiker**.

1. Ga de naam van de gebruiker, e-mailadres in, of kies van de lijst, dan klik **sparen**.

1. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

De gebruiker ontvangt een e-mail met instructies om toegang te krijgen tot uw exemplaar.

+++

## Afvoerkanalen en beperkingen {#generative-guardrails}

De algemene richtlijnen voor het gebruik van de AI Assistant in Adobe Journey Optimizer voor het genereren van e-mail worden hieronder weergegeven:

* De kwaliteit van de gegenereerde inhoud wordt sterk beïnvloed door het marketingdoel dat/de marketingprompt die u definieert. Gebruik een duidelijk gedefinieerde prompt voor een juiste interpretatie van het GenAI-model. 
* Upload merkmiddelen voor nauwkeurige informatie over de inhoud van het merk. Anders is de inhoud gebaseerd op algemeen beschikbare informatie. De geüploade inhoud kan de volgende indelingen hebben: PDF-, JPEG-, PNG- of ZIP-bestanden (met ondersteunde bestandsindelingen).
* De maximale grootte voor geüploade brandmiddelen is 50 MB. Grotere bestanden of veel afbeeldingen kunnen werken, maar de verwerkingstijd neemt toe.
* Gebruik een merkspecifieke of aangepaste sjabloon om uw e-mailinhoud te maken met AI Assistant in Adobe Journey Optimizer. E-mailsjablonen met maximaal 8-10 afbeeldingen worden aanbevolen.
* Zorg ervoor dat u eventuele problematische uitvoerbestanden meldt met het blokje omhoog, omlaag of de vlagpictogrammen bij het selecteren van varianten.
* Op uw gebruik van de AI Assistant zijn de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen van toepassing. [Meer informatie](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Als onderdeel van de toezegging van Adobe om de transparantie bij het gebruik van generatieve AI-tools bij het maken van media te bevorderen, zal Adobe Content Credentials toepassen wanneer inhoud of een project dat een door Firefly gegenereerd element bevat, wordt gedownload of geëxporteerd. [Meer informatie](https://helpx.adobe.com/firefly/using/content-credentials.html)

De volgende beperkingen gelden voor AI Assistant in Adobe Journey Optimizer:

* Ondersteunde taal is alleen Engels. Niet-Engelse invoer kan leiden tot inconsistente of onjuiste resultaten. Problemen die voortvloeien uit niet-Engelse antwoorden worden momenteel niet behandeld of verbeterd.
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
