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
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '658'
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
>abstract="Als u de geselecteerde inhoud wilt gebruiken als invoer voor het genereren van inhoud, activeert u de optie **Originele inhoud gebruiken** schakelen. U kunt ook uw merkmiddelen uploaden om deze als bron te gebruiken. Als u de geselecteerde inhoud niet gebruikt, zijn het uploaden en selecteren van merkelementen verplicht."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Algemene AI-termen voor Adobe"
>abstract="Voor toegang tot deze functie moet u akkoord gaan met de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen. Alle aanwijzingen, contextgegevens of aanvullende informatie of andere gegevens die u aan deze functie verstrekt, moeten zijn gekoppeld aan een specifieke context, die uw brandingmaterialen, website-inhoud, gegevens, schema&#39;s voor dergelijke gegevens, sjablonen of andere vertrouwde documenten kan bevatten en geen persoonlijke gegevens mag bevatten (persoonlijke gegevens omvatten alles wat u terug kunt koppelen naar een specifiek individu). U moet de nauwkeurigheid van de uitvoer van deze functie controleren en controleren of deze geschikt is voor uw gebruiksgeval"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe Generation AI-gebruikersrichtlijnen"

>[!BEGINSHADEBOX]

**Inhoudsopgave**

* Aan de slag met de AI Assistant
* [E-mailgeneratie met AI Assistant](generative-email.md)
* [SMS genereren met de AI Assistant](generative-sms.md)
* [Push generation met de AI Assistant](generative-push.md)
* [Inhoud experimenteren met de AI Assistant](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>De AI-assistent in Adobe Journey Optimizer is momenteel beschikbaar als een bètaversie om alleen gebruikers te selecteren.

De AI-assistent in Adobe Journey Optimizer biedt proactieve suggesties voor inhoudvariatie voor tekst en afbeeldingen. Het is beschikbaar voor e-mail, Push en SMS kanalen. Deze nieuwe functie biedt een snelle, op tekst en afbeeldingen gebaseerde productie. Afbeeldingen genereren wordt beheerd met Adobe Firefly.

Gebruik de AI-assistent in Journey Optimizer om de impact van uw bericht te optimaliseren door te experimenteren met verschillende hoofdtitels en -afbeeldingen. Genereer meerdere varianten en maak een experiment om ze te vergelijken. Als u gebruikmaakt van Journey Optimizer Content Experiment, kunt u meerdere berichtbehandelingen definiëren om te meten welke het beste presteert voor uw doelgroep. U kunt kiezen om de leveringsinhoud, of onderwerp te variëren. Het berichtpubliek wordt willekeurig toegewezen aan elke behandeling om te bepalen welke één het beste in termen van gespecificeerde metrisch werkt. Meer informatie over Inhoud experimenteren in [deze sectie](../content-management/content-experiment.md).

## Afvoerkanalen en beperkingen {#generative-guardrails}

De algemene richtlijnen voor het gebruik van de AI Assistant in Journey Optimizer voor het genereren van e-mail worden hieronder weergegeven:

* De kwaliteit van de gegenereerde inhoud wordt sterk beïnvloed door het marketingdoel dat/de marketingprompt die u definieert. Gebruik een duidelijk gedefinieerde prompt voor een juiste interpretatie van het GenAI-model. 
* Upload merkmiddelen voor nauwkeurige informatie over de inhoud van het merk. Anders is de inhoud gebaseerd op algemeen beschikbare informatie. De geüploade inhoud kan de volgende indelingen hebben: PDF, JPEG, PNG- of ZIP-bestanden (met ondersteunde bestandsindelingen).
* De maximale grootte voor geüploade brandmiddelen is 50 MB. Grotere bestanden of veel afbeeldingen kunnen werken, maar de verwerkingstijd neemt toe.
* Gebruik bij voorkeur een door Adobe Campaign geschreven e-mailsjabloon [ingebouwde e-mailsjablonen](../email/use-email-templates.md), een merkspecifieke sjabloon of aangepaste sjabloon om uw e-mailinhoud te maken. E-mailsjabloon met maximaal 8-10 afbeeldingen wordt aanbevolen.
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
<a href="generative-email.md"><strong>E-mailgeneratie</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="SMS-generatie" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>SMS-generatie</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Push generation" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Pushmelding genereren</strong></a>
</div>
<p></td>
</tr></table>
