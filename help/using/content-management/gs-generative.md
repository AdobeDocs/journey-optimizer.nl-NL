---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met de AI Assistant
description: Leer toegang te krijgen tot en te werken met Journey Optimizer AI Assistant
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 267d1850cbe30b1078f3b5b5bd228364bb63edd6
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Aan de slag met de AI Assistant {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI-assistent"
>abstract="Nadat u de levering hebt gemaakt en gepersonaliseerd, kunt u de AI Assistant gebruiken om de inhoud te verbeteren. Deze functie vereenvoudigt het proces van personalisatie en inhoudverbetering door u toe te staan om de inhoud te verfijnen door te beschrijven wat u wilt produceren."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Context definiëren met AI Assistant"
>abstract="Om de geselecteerde inhoud als input voor inhoudsgeneratie te gebruiken, activeer de **originele inhoud van het Gebruik** knevel. U kunt ook uw merkmiddelen uploaden om deze als bron te gebruiken. Als u de geselecteerde inhoud niet gebruikt, zijn het uploaden en selecteren van merkelementen verplicht."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Algemene AI-termen voor Adobe"
>abstract="Voor toegang tot deze functie moet u akkoord gaan met de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen. Controleer de nauwkeurigheid van de uitvoer van deze functie en zorg ervoor dat deze geschikt is voor uw gebruiksscenario."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe Generation AI-gebruikersrichtlijnen"

>[!BEGINSHADEBOX]

**Lijst van inhoud**

* Aan de slag met de AI Assistant
* [E-mailgeneratie met AI Assistant](generative-email.md)
* [SMS genereren met de AI Assistant](generative-sms.md)
* [Push generation met de AI Assistant](generative-push.md)
* [Inhoud experimenteren met de AI Assistant](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>De AI-assistent in Adobe Journey Optimizer is momenteel beschikbaar als een bètaversie om alleen gebruikers te selecteren.

De AI Assistant in Adobe Journey Optimizer, die wordt aangedreven door Azure OpenAI, biedt proactieve suggesties voor wijzigingen in inhoud voor tekst en afbeeldingen. Het is beschikbaar voor e-mail, Push en SMS kanalen. Deze nieuwe functie biedt een snelle, op tekst en afbeeldingen gebaseerde productie. Afbeeldingen genereren wordt beheerd met Adobe Firefly.

Gebruik de AI-assistent in Journey Optimizer om de impact van uw bericht te optimaliseren door te experimenteren met verschillende hoofdtitels en -afbeeldingen. Genereer meerdere varianten en maak een experiment om ze te vergelijken. Als u gebruikmaakt van Journey Optimizer Content Experiment, kunt u meerdere berichtbehandelingen definiëren om te meten welke het beste presteert voor uw doelgroep. U kunt kiezen om de leveringsinhoud, of onderwerp te variëren. Het berichtpubliek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke één het beste in termen van gespecificeerde metrisch werkt. Leer meer over de Experimenteer van de Inhoud in [ deze sectie ](../content-management/content-experiment.md).

## Afvoerkanalen en beperkingen {#generative-guardrails}

De algemene richtlijnen voor het gebruik van de AI Assistant in Journey Optimizer voor het genereren van e-mail worden hieronder weergegeven:

* De kwaliteit van de gegenereerde inhoud wordt sterk beïnvloed door het marketingdoel dat/de marketingprompt die u definieert. Gebruik een duidelijk gedefinieerde prompt voor een juiste interpretatie van het GenAI-model. 
* Upload merkmiddelen voor nauwkeurige informatie over de inhoud van het merk. Anders is de inhoud gebaseerd op algemeen beschikbare informatie. De geüploade inhoud kan de volgende indelingen hebben: PDF, JPEG, PNG- of ZIP-bestanden (met ondersteunde bestandsindelingen).
* De maximale grootte voor geüploade brandmiddelen is 50 MB. Grotere bestanden of veel afbeeldingen kunnen werken, maar de verwerkingstijd neemt toe.
* Gebruik een Adobe Campaign authored e-mailmalplaatjes, bij voorkeur [ ingebouwde e-mailmalplaatjes ](../email/use-email-templates.md), een merkspecifiek malplaatje of douanemalplaatje om uw e-mailinhoud tot stand te brengen. E-mailsjabloon met maximaal 8-10 afbeeldingen wordt aanbevolen.
* Zorg ervoor dat u eventuele problematische uitvoerbestanden meldt met het blokje omhoog, omlaag of de vlagpictogrammen bij het selecteren van varianten.
* Op het gebruik van de AI-assistent zijn de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen van toepassing. [Meer informatie](https://www.adobe.com/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

De volgende beperkingen gelden voor AI Assistant in Journey Optimizer:

* Ondersteunde taal is alleen Engels.
* Alleen beschikbaar voor de e-mail-, push- en SMS-kanalen.
* GenAI-inhoud is mogelijk niet altijd correct: geef uw feedback zodat onze technici de modellen kunnen verfijnen.
* U kunt meerdere merkmiddelen uploaden, maar u kunt slechts één voor een specifieke generatie gebruiken.

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
</tr></table>
