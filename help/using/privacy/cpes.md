---
solution: Journey Optimizer
product: journey optimizer
title: Weigeren beheren
description: Meer informatie over het beheren van opt-out en privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Goedkeuring van opt-out voor personalisatie implementeren {#cpes-opt-out}


## Expressieeditor

De Redacteur van uitdrukkingen terwijl het personaliseren van beelden, tekst, onderwerpregel (Segment in Campaigns) - UI en Zwaartepunt

De redacteur van de Personalisatie zelf voert geen toestemmingscontroles of handhaving uit aangezien het niet betrokken is bij de levering van berichtacties. De redacteur van de verpersoonlijking houdt zich aan rechten gebaseerde de etiketten van de toegangscontrole die door de verenigde profieldienst worden verstrekt om verschillende gebieden toe te staan/toe te staan om voor verpersoonlijking worden gebruikt. De voorproef van het bericht en geeft dienst terug zal geïdentificeerde gebieden met gevoelige informatie maskeren.

In AJO-campagnes kan de handhaving van het toestemmingsbeleid op twee plaatsen plaatsvinden. Klanten kunnen definities van het toestemmingsbeleid opnemen als onderdeel van het publiek of de segmentcreatie om ervoor te zorgen dat het publiek dat voor de campagne is geselecteerd reeds profielen heeft uitgefilterd die niet aan de toestemmingscriteria voldoen. Ten tweede zal de dienst van berichtruntime een algemene toestemmingscontrole op het kanaalniveau uitvoeren om ervoor te zorgen dat de profielen hebben gekozen-binnen om marketingmededelingen op het specifieke kanaal te ontvangen. Het voorwerp van de Campagne AJO zelf voert momenteel geen extra controles van het toestemmingsbeleid uit.

AJO-campagne en persoonlijke stappen voor het handmatig afdwingen van toestemming:

De status van een gebruiker die zich aanmeldt en voorkeuren voor personalisatie moeten onderdeel zijn van de publieksregels en -definitie voordat deze worden geactiveerd in een Journey Optimizer-campagne. Een op de markt brengende gebruiker in Adobe Experience Platform kan een toestemmingscontrole aan hun publiek toevoegen door een nieuwe publiekssamenstelling te creëren of door een nieuw segment te bepalen gebruikend regelbouwer.

Als u composer voor het publiek gebruikt, kunt u het publiek splitsen met behulp van profielkenmerken. Als u eenmaal de juiste toestemmingskenmerken hebt geselecteerd die u wilt controleren, kunt u het resulterende publiek voor activering opslaan in een campagne. Houd er rekening mee dat als u een publiek maakt dat geen toestemming heeft gegeven voor personalisatie en u vervolgens dit publiek selecteert voor activering in een campagne, de personalisatiehulpmiddelen beschikbaar blijven. Het is aan de marketing gebruiker om te begrijpen dat als zij met een publiek werken dat geen verpersoonlijking zou moeten ontvangen, dat zij geen verpersoonlijkingshulpmiddelen zouden moeten gebruiken.

Ga als volgt te werk om een gesplitst publiek in de publiekscompositie te maken:

1. Selecteer uw beginnende publiek.

1. Klik op het pluspictogram om een gesplitst publiek te maken.

1. Kies in de eigenschappen Splitsen de optie &#39;splitsen van kenmerken&#39; als type.

1. Klik in het veld Kenmerk op het potloodpictogram om het venster Kenmerkselectie weer te geven.

1. Type in Keuze waarde om naar het attribuut van de verpersoonlijkingstoestemming te zoeken (merk op dit het attribuut path profile.consents.personalize.content.val zal zijn

1. Selecteer dit kenmerk.

1. In Weg 1 - kies een etiket om u te helpen het niet-gepersonaliseerde publiek bepalen.

1. Kies de gewenste waarde in deze lijst: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values

   In dit geval gebruiken we een &#39;n&#39; om NO aan te duiden als de opt-out voor personalisatie

   U kunt een afzonderlijk pad maken voor andere keuzevelden of u kunt de resterende paden verwijderen en &quot;andere profielen&quot; inschakelen. Dit zijn alle andere profielen waarvoor de waarde &quot;n&quot; niet is gekozen.

1. Als u klaar bent, klikt u in het vak met de tekst &#39;Publiek opslaan&#39;. Er wordt een nieuw eigenschappenvenster geopend waarin u kunt kiezen welke naam u wilt gebruiken voor het afgeleide publiek.

1. Publiceer de publiekscompositie nadat u klaar bent.

Als het gebruiken van de bouwer van de segmentregel om uw publiek tot stand te brengen kunt u verpersoonlijking en toestemmingswaardekeuzen als uitsluitingsparameters in de publieksdefinitie selecteren. Door in de uitsluitingsparameters toe te voegen, kunt u één publiekssegment van profielen maken waarin personen die geen toestemming hebben gegeven, worden uitgefilterd.
