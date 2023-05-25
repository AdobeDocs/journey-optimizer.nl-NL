---
title: Een melding in de app maken in een reis
description: Leer hoe u een bericht in de app maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, bericht, maken, starten
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informatief"
source-git-commit: 50afe137c618153278c596f1553216c20637e40b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 1%

---

# Een bericht in de app maken in een reis {#create-in-app-journey}

1. Open uw reis en sleep vervolgens een **[!UICONTROL In-app]** van de **[!UICONTROL Actions]** in het palet.

   Wanneer een profiel het einde van de rit bereikt, verlopen alle berichten in de app die aan hen worden weergegeven, automatisch. Daarom wordt er automatisch een wachtbewerking toegevoegd na uw activiteiten in de app om de juiste timing te garanderen.

   ![](assets/in_app_journey_1.png)

1. Voer een **[!UICONTROL Label]** en **[!UICONTROL Description]** voor uw bericht.

1. Kies de optie [In-app oppervlak](inapp-configuration.md) te gebruiken.

   ![](assets/in_app_journey_2.png)

1. U kunt nu beginnen met het ontwerpen van uw inhoud met de **[!UICONTROL Edit content]** knop. [Meer informatie](design-in-app.md)

1. Klikken **[!UICONTROL Edit trigger]** om de trigger te configureren.

   ![](assets/in_app_journey_4.png)

1. Kies de frequentie van de trigger wanneer het bericht in de app actief is:

   * **[!UICONTROL Show every time]**: Toon altijd het bericht wanneer de gebeurtenissen die in **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Show once]**: Alleen dit bericht weergeven als de gebeurtenissen die voor de eerste keer zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** vervolgkeuzelijst.
   * **[!UICONTROL Show until click through]**: Dit bericht weergeven wanneer de gebeurtenissen zijn geselecteerd in het dialoogvenster **[!UICONTROL Mobile app trigger]** drop-down komt voor tot een interactie gebeurtenis door SDK met een actie van &quot;geklikt&quot;wordt verzonden.

1. Van de **[!UICONTROL Mobile app trigger]** -dropdown(s), kies de gebeurtenis(sen) en de criteria die uw bericht zullen activeren:

   1. Selecteer in de linkervervolgkeuzelijst de gebeurtenis die nodig is om het bericht te activeren.
   1. Selecteer in de rechtervervolgkeuzelijst de vereiste validatie voor de geselecteerde gebeurtenis.
   1. Klik op de knop **[!UICONTROL Add]** als u wilt dat de trigger rekening houdt met meerdere gebeurtenissen of criteria. Herhaal vervolgens de bovenstaande stappen.
   1. Selecteer hoe uw gebeurtenissen worden gekoppeld. Kies bijvoorbeeld **[!UICONTROL And]** als u **beide** triggers moeten waar zijn om een bericht weer te geven of **[!UICONTROL Or]** als u wilt dat het bericht wordt getoond als **ofwel** van de triggers zijn waar.
   1. Klikken **[!UICONTROL Save]** wanneer uw triggers zijn geconfigureerd.

   ![](assets/in_app_journey_3.png)

1. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

1. Zodra uw bericht in de app klaar is, voltooit u de configuratie en publiceert u uw reis om het te activeren.

Voor meer informatie over hoe te om een reis te vormen, verwijs naar [deze pagina](../building-journeys/journey-gs.md).

## Beperkingen van activiteiten in de app {#in-app-activity-limitations}

* Deze functie is momenteel niet beschikbaar voor klanten in de gezondheidszorg.

* Personalisatie kan alleen profielkenmerken bevatten.

* De weergave in de app is gekoppeld aan de duur van de rit. Dit houdt in dat wanneer de reis voor een profiel afloopt, alle in-app-berichten binnen die reis niet meer worden weergegeven voor dat profiel.  Het is daarom niet mogelijk om een bericht in de app rechtstreeks te stoppen van een reisactiviteit. In plaats daarvan moet u de volledige reis beëindigen om te voorkomen dat de berichten in de app naar het profiel worden weergegeven.

* In de testmodus is de weergave in de app afhankelijk van de levensduur van de rit. Om te voorkomen dat de reis te vroeg eindigt tijdens de test, past u de **[!UICONTROL Wait time]** waarde voor uw **[!UICONTROL Wait]** activiteiten.

* **[!UICONTROL Reaction]** activiteiten kunnen niet worden gebruikt om te reageren op een geopende In-app of klik.

* Er treedt een activeringsvertraging op tussen het moment dat een gebruikersprofiel een in-app-activiteit op het canvas bereikt en het moment waarop het bericht in de app wordt weergegeven. Deze vertraging kan variëren van 15 minuten tot 1 uur.

**Verwante onderwerpen:**

* [In-app-bericht ontwerpen](design-in-app.md)
* [Uw In-app-bericht testen en verzenden](send-in-app.md)
* [Rapport in app](../reports/campaign-global-report.md#inapp-report)
* [Configuratie in de app](inapp-configuration.md)
