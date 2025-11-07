---
solution: Journey Optimizer
product: journey optimizer
title: Problemen met de uitvoering van uw livetraject oplossen
description: Leer hoe u fouten in de uitvoering van live reizen kunt oplossen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: problemen oplossen, problemen oplossen, reis, controle, fouten
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 36%

---

# Problemen met de uitvoering van uw livetraject oplossen {#troubleshooting-execution}

In deze sectie, leer hoe te om reisgebeurtenissen problemen op te lossen, controleer als de profielen uw reis inging, hoe zij door het navigeren, en als de berichten worden verzonden.

U kunt fouten ook oplossen voordat u een reis test of publiceert. Leer hoe [ op deze pagina ](troubleshooting.md).

Als u binnenkomende acties gebruikt, leer hoe te om hen [ op deze pagina ](troubleshooting-inbound.md) problemen op te lossen.

## Controleren of gebeurtenissen correct zijn verzonden {#checking-that-events-are-properly-sent}

Het startpunt van een journey is altijd een gebeurtenis. U kunt tests uitvoeren met tools zoals Postman.

U kunt controleren of de API-aanroep die u via deze tools verzendt, correct is verzonden of niet. Als een fout wordt geretourneerd, betekent dit dat er een probleem is met uw aanroep. Controleer opnieuw de payload, de koptekst (vooral de organisatie-id) en de bestemmings-URL. U kunt de beheerder vragen wat de juiste URL is.

Gebeurtenissen worden niet rechtstreeks van de bron naar de ritten verplaatst. Reizen vertrouwen inderdaad op Adobe Experience Platform-API&#39;s voor streaming-opname. Dientengevolge, in het geval van gebeurtenis verwante kwesties, kunt u naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} voor het Streamen van opname APIs het oplossen van problemen verwijzen.

Als uw reis er niet in slaagt testwijze met fout `ERR_MODEL_RULES_16` toe te laten, zorg ervoor de gebruikte gebeurtenis een [ identiteit namespace ](../audience/get-started-identity.md) omvat wanneer het gebruiken van een kanaalactie.

De naamruimte identity wordt gebruikt om de testprofielen op unieke wijze te identificeren. Bijvoorbeeld, als e-mail wordt gebruikt om de testprofielen te identificeren, zou de identiteit namespace **E-mail** moeten worden geselecteerd. Als het unieke herkenningsteken het telefoonaantal is, dan zou de identiteit namespace **Telefoon** moeten worden geselecteerd.

## Controleren of mensen de reis betreden {#checking-if-people-enter-the-journey}

Reisrapportage meet de toegang van mensen tot een reis in real-time.

Als u het evenement met succes verzendt, maar geen toegang ziet tot de reis, betekent dit dat er iets mis gaat tussen het verzenden van het evenement en de ontvangst van het evenement op de reis.

U kunt het oplossen van problemen met de hieronder vragen beginnen:

* Weet u zeker dat de journey waar u de eerste gebeurtenis verwacht, in de testmodus of live is?
* Hebt u de gebeurtenis opgeslagen voordat u de payload uit de payloadvoorvertoning hebt gekopieerd?
* Bevat de gebeurtenispayload een gebeurtenis-id?
* Hebt u de juiste URL gebruikt?
* Hebt u de payloadstructuur van de streamingopname-API’s gevolgd en de voorvertoning van de payloadstructuur in het deelvenster voor gebeurtenisconfiguratie gebruikt? Zie [deze pagina](../event/about-creating.md#preview-the-payload).
* Gebruikt u de juiste sleutel-waardeparen in de kopbal van uw gebeurtenis?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## Controleren hoe mensen door de reis navigeren {#checking-how-people-navigate-through-the-journey}

De journalistiek meet de voortgang van individuen binnen een reis. Het is gemakkelijk te bepalen waar en waarom een persoon is gestopt.

Controleer bijvoorbeeld het volgende:

* Komt het door een voorwaarde die de persoon uitsluit? De voorwaarde is bijvoorbeeld ‘geslacht = man’ en de persoon is een vrouw. Deze controle kan door een zakelijke gebruiker worden uitgevoerd als de voorwaarde niet te complex is.
* Komt het doordat een aanroep aan een databron niet wordt beantwoord? Wanneer de journey in de testmodus verkeert, is deze informatie in testmoduslogboeken te zien. Wanneer de journey live is, kan een beheerder directe aanroepen aan de databron testen en het ontvangen antwoord controleren. Een beheerder kan de journey ook dupliceren en testen.

## Controleren of berichten zijn verzonden {#checking-that-messages-are-sent-successfully}

Als individuen de juiste manier in de reis stromen maar geen berichten ontvangen zij zouden moeten ontvangen, kunt u controleren of:

* [!DNL Journey Optimizer] heeft correct rekening gehouden met de aanvraag om het bericht te verzenden. Zakelijke gebruikers hebben toegang tot het bericht dat ze geacht worden te zijn verzonden en controleren of de tijd van de meest recente uitvoering overeenkomt met de uitvoeringstijd van uw reis. Ze kunnen ook de meest recente ontvangen API-oproepen/gebeurtenissen controleren.
* [!DNL Journey Optimizer] heeft het bericht verzonden. Controleer de reisrapportering om ervoor te zorgen dat er geen fouten zijn.

In het geval van een bericht dat via een douaneactie wordt verzonden, is het enige wat tijdens reistest kan worden gecontroleerd het feit dat de vraag van het systeem van de douaneactie tot een fout of niet leidt. Als de oproep aan het externe systeem dat aan de douaneactie is gekoppeld niet tot een fout leidt maar niet tot het verzenden van een bericht leidt, zouden sommige onderzoeken aan de kant van het externe systeem moeten worden gedaan.
