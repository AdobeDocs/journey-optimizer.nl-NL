---
solution: Journey Optimizer
product: journey optimizer
title: Reisproblemen oplossen
description: Leer hoe u fouten tijdens reizen kunt oplossen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: problemen oplossen, problemen oplossen, reis, controle, fouten
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 135dd7528e87a6fde7e148745ef2f49104809bc1
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 69%

---

# Uw reis oplossen {#troubleshooting}

Leer in deze sectie hoe u problemen met reizen kunt oplossen voordat u gaat testen of publiceren. Alle hieronder vermelde controles kunnen worden uitgevoerd in de testmodus van de journey of wanneer de journey live is. De aanbeveling is om alle onderstaande controles in de testmodus uit te voeren en vervolgens tot publicatie over te gaan. Zie [deze pagina](../building-journeys/testing-the-journey.md).

## Controleren op fouten voordat wordt getest {#checking-for-errors-before-testing}

Controleer voordat u uw journey gaat testen en publiceren of alle activiteiten correct zijn geconfigureerd. U kunt geen tests of publicaties uitvoeren als het systeem nog steeds fouten detecteert.

Fouten worden weergegeven met een waarschuwingssymbool dat wordt weergegeven op de activiteiten zelf op het canvas. Plaats de cursor op het uitroepteken om het foutbericht weer te geven. Als u op de activiteit klikt, ziet u de regel waarin de fout voorkomt en een waarschuwing. Als een verplicht veld bijvoorbeeld leeg is, wordt een fout weergegeven.

![](assets/journey63.png)

Als op het canvas bijvoorbeeld twee activiteiten zijn losgekoppeld, wordt een waarschuwing weergegeven.

![](assets/canvas-disconnected.png)

Naast de schakeloptie **[!UICONTROL Test]** en de knop **[!UICONTROL Publish]** kan een waarschuwingsteken worden weergegeven. Dit waarschuwingsteken duidt op fouten die door het systeem zijn gedetecteerd en voorkomt activering van de testmodus of publicatie van de journey. Meestal zijn fouten die door het systeem worden gedetecteerd, gekoppeld aan fouten die zichtbaar zijn in de activiteiten, maar soms zijn ze gekoppeld aan andere problemen. In dit geval kunt u de fout weergeven en proberen het probleem te identificeren aan de hand van de foutbeschrijving. Als u de kwestie niet kunt identificeren, kunt u de details kopiëren en hen verzenden naar de beheerder of aan steun. Fouten die tests blokkeren en fouten die publicatie blokkeren, lijken op elkaar.

Het systeem detecteert twee soorten problemen: fouten en waarschuwingen. Fouten blokkeren publicatie en testactivering. Waarschuwingen geven mogelijke problemen aan die testactivering of publicatie niet blokkeren. U ziet een beschrijving van het probleem en een probleemlog-id van het type ERR_XXX_XXX. Dit helpt de technische ondersteuning om het probleem te identificeren.

Er kunnen twee verschillende kleuren worden weergegeven op het teken naast de schakeloptie **[!UICONTROL Test]** en de knop **[!UICONTROL Publish]**. Het teken is rood in geval van fouten. En het is oranje in geval van waarschuwingen.

![](assets/journey75.png)

Fouten en waarschuwingen die globaal zijn voor de journey, worden als eerste in de lijst weergegeven. Fouten en waarschuwingen met betrekking tot specifieke activiteiten worden daarna vermeld, op volgorde van activiteit of weergave in de journey van links naar rechts. Met de knop **[!UICONTROL Copy details]** wordt technische informatie over de journey gekopieerd waarmee het ondersteuningsteam problemen kan oplossen.

Wanneer er een fout in een actie of een voorwaarde optreedt, eindigt de journey van een individu. De enige manier om door te gaan is het selectievakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in te schakelen. Zie [deze sectie](../building-journeys/using-the-journey-designer.md#paths).

## Controleren of gebeurtenissen correct zijn verzonden {#checking-that-events-are-properly-sent}

Het startpunt van een journey is altijd een gebeurtenis. U kunt tests uitvoeren met tools zoals Postman.

U kunt controleren of de API-aanroep die u via deze tools verzendt, correct is verzonden of niet. Als een fout wordt geretourneerd, betekent dit dat er een probleem is met uw aanroep. Controleer opnieuw de payload, de koptekst (vooral de organisatie-id) en de bestemmings-URL. U kunt de beheerder vragen wat de juiste URL is.

Gebeurtenissen worden niet rechtstreeks van de bron naar de ritten verplaatst. Reizen vertrouwen inderdaad op Adobe Experience Platform-API&#39;s voor streaming-opname. Als u problemen hebt met gebeurtenissen, kunt u dus verwijzen naar [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} voor het oplossen van problemen met opname-API&#39;s voor streaming.

## Controleren of mensen de reis betreden {#checking-if-people-enter-the-journey}

Reisrapportage meet de toegang van mensen tot een reis in real-time.

Als u de gebeurtenis zonder problemen verzendt maar geen toegang tot de journey ziet, betekent dit dat er iets misgaat tussen het verzenden van de gebeurtenis en de ontvangst van de gebeurtenis in de journey.

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

Als personen de juiste stroom in de journey volgen, maar geen berichten ontvangen die ze wel zouden moeten ontvangen, kunt u het volgende controleren:

* [!DNL Journey Optimizer] heeft correct rekening gehouden met het verzoek om het bericht te verzenden. Zakelijke gebruikers hebben toegang tot het bericht dat ze geacht worden te zijn verzonden en controleren of de tijd van de meest recente uitvoering overeenkomt met de uitvoeringstijd van uw reis. Ze kunnen ook de meest recente ontvangen API-oproepen/gebeurtenissen controleren.
* [!DNL Journey Optimizer] heeft het bericht verzonden. Controleer de reisrapportering om ervoor te zorgen dat er geen fouten zijn.

In het geval van een bericht dat via een douaneactie wordt verzonden, is het enige wat tijdens reistest kan worden gecontroleerd het feit dat de vraag van het systeem van de douaneactie tot een fout of niet leidt. Als de oproep aan het externe systeem dat aan de douaneactie is gekoppeld niet tot een fout leidt maar niet tot het verzenden van een bericht leidt, zouden sommige onderzoeken aan de kant van het externe systeem moeten worden gedaan.
