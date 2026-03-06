---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische media
description: Dynamische media gebruiken met Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4c1d39c4-3154-4bec-ac3c-c2ead7164d69
source-git-commit: f212a2178e83283d4755da5483d7c11ba4df183f
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Afteltimer invoegen {#countdown}

Creeer urgentie en maximaliseer omzettingen met de Dynamische tijdopnemers van Media die in real time bijwerken wanneer de ontvangers uw e-mails openen. Deze functie is ideaal voor Flash-verkoop, aanbiedingen met beperkte tijd en tijdgevoelige aanbiedingen.

Bijvoorbeeld, als markator voor een handelsmerk, runt u een flitsverkoop 48 uur. Door de afteltimer te gebruiken in je speciale e-mails:

* Ontvangers die onmiddellijk openen, zien &quot;47 uur resterend&quot;
* Ontvangers die 24 uur later openen, zien &quot;23 uur resterend&quot;
* Ontvangers die na afloop van de verkoop openen, zien &quot;Tijd is op!&quot;

Voor meer informatie over hoe te om tellertijdopnemers aan uw Dynamische malplaatje van Media in Adobe Experience Manager toe te voegen, verwijs [&#x200B; naar dit document &#x200B;](assets/do-not-localize/countdown.pdf).


1. Maak in **[!DNL Adobe Experience Manager]** een sjabloon voor dynamische media en voeg er een component voor afteltimer aan toe.

   ![](assets/timer-1.png)

1. Maak in **[!DNL Journey Optimizer]** een nieuwe campagne of open een bestaande campagne en open vervolgens de e-mail-Designer.

1. De belemmering en laat vallen een **HTML** of **3&rbrace; component van Activa &lbrace;in uw e-mailinhoud.**

1. Houd de muisaanwijzer boven de component en klik op **[!UICONTROL Show the source code]** (voor HTML-componenten) of **[!UICONTROL Browse]** (voor Asset-componenten).

   ![](assets/timer-2.png)

1. Navigeer in het menu **[!UICONTROL Edit HTML]** naar **[!UICONTROL Assets]** en klik op **[!UICONTROL Open asset selector]** om door de gepubliceerde sjabloon voor dynamische media te bladeren en deze te selecteren.

   ![](assets/timer-3.png)

1. Schakel de optie voor het ophalen van vullingen in door naar Aan te gaan. Hierdoor wordt de leesbaarheid verbeterd doordat lange kenmerkpaden worden verborgen.

   ![](assets/timer-6.png)

1. Configureer in het menu **[!UICONTROL Custom attributes]** de eventuele aanpasbare URL-parameters die nodig zijn voor de sjabloon.

   Klik op **[!UICONTROL Save]** als u klaar bent.

   ![](assets/timer-4.png)

1. U kunt ook toegang krijgen tot de parameters van de sjabloon Dynamische media door het element te selecteren in de e-mail-Designer en vervolgens het menu **[!UICONTROL Settings]** te openen.

   Configureer het volgende:

   * **tekst van de Banner**: De tekst die met uw tijdopnemer wordt getoond
   * **Eind tijd**: De datum en de tijd wanneer aftellen verloopt. Voer de tijd alleen in GMT (Greenwich Mean Time) in. Het systeem accepteert geen andere tijdzones.
   * **Tekst van de Fallback**: Het bericht dat na tijdopnemereinden wordt getoond

   ![](assets/timer-5.png)

1. Klik **[!UICONTROL Preview]** om de tijdopnemer met tellerupdates in real time te bekijken en uw configuratie te verifiëren.

Wanneer ontvangers het e-mailbericht openen, zien ze de juiste tijd die nog over is voor de Flash-verkoop. Als ze het e-mailbericht later opnieuw openen, wordt de aftelling automatisch bijgewerkt om de resterende tijd te weerspiegelen. Na de einddatum wordt het standaardbericht automatisch weergegeven.
