---
solution: Journey Optimizer
product: journey optimizer
title: Loyalty-uitdagingen openen en beheren
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen en -taken kunt openen, beheren en organiseren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Loyalty-uitdagingen openen en beheren {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* **de Uitdagingen van de Loyalty van de Toegang** {2 }︎ ◀ u bent hier **- Overzicht, uitdagingen en taakbeheer**
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* [&#x200B; creeer taken &#x200B;](create-tasks.md) - bepaal uitdagingstaken

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## Access Loyal Challenges

Navigeer naar Journey Optimizer en selecteer **[!UICONTROL Loyalty Challenge (Beta)]** onder de sectie **[!UICONTROL Journey management]** om Loyalty Challenges te openen.

De interface van de Uitdagingen van de Loyalty verstrekt een gecentraliseerde plaats om, al uw uitdagingen en taken te bekijken te beheren en te organiseren. U hebt toegang tot twee belangrijke inventarissen:

* **Uitdagingen inventariseren**: Bekijk en beheer alle loyaliteitsuitdagingen, controleer hun status, en voer snelle acties uit
* **inventaris van Taken**: Blader herbruikbare taken die over veelvoudige uitdagingen kunnen worden gebruikt

## Uitdagingen inventariseren {#challenges-tab}

Op het tabblad **[!UICONTROL Challenges]** worden alle uitdagingen weergegeven die zijn gesorteerd op de datum die als laatste is gewijzigd, waarbij de laatst gewijzigde uitdagingen als eerste worden weergegeven.

![](assets/challenges-inventory.png)

Belangrijkste weergegeven informatie:

* **[!UICONTROL Challenge]**: Uitdagingsnaam
* **[!UICONTROL State]**: Huidige status van de challenge (concept of gepubliceerd)
* **[!UICONTROL Tasks]**: Aantal taken gevormd in de uitdaging
* **[!UICONTROL Journey]**: Koppeling naar de automatisch gegenereerde reis die verband houdt met de uitdaging
* **[!UICONTROL Status]**: Huidige status van de bijbehorende reis (Laag, Actief, Gestopt, enz.)
* **[!UICONTROL Start/End Date (UTC)]**: Wanneer de uitdaging actief wordt en vervalt

Van het lusje van Uitdagingen, kunt u acties op uitdagingen uitvoeren:

* **uitdaging van de Mening**: Selecteer de uitdagingsnaam om zijn detailspagina te openen
* **dupliceer een uitdaging**: Selecteer het ![](assets/do-not-localize/Smock_More_18_N.svg) pictogram en kies **[!UICONTROL Duplicate]**. Er wordt een kopie gemaakt met alle taken, inhoud en berichten intact.
* **Schrap een uitdaging**: Selecteer het ![](assets/do-not-localize/Smock_More_18_N.svg) pictogram en kies **[!UICONTROL Delete]**
* **geef een uitdaging** uit: Selecteer de uitdagingsnaam om zijn detailspagina te openen en het uit te geven.

  Wanneer u een gepubliceerde uitdaging voor het uitgeven opent, moet u het eerst aan de status van het Ontwerp terugkeren:

   * Alle aanpassingen die rechtstreeks op de automatisch gegenereerde reis worden aangebracht, gaan verloren
   * De uitdaging keert terug naar de status van het Ontwerp
   * Nadat u de wijzigingen hebt aangebracht, moet u de uitdaging opnieuw opslaan en publiceren
   * U moet de bijbehorende reis opnieuw publiceren om de bijgewerkte uitdaging aan klanten ter beschikking te stellen

  >[!IMPORTANT]
  >
  >Het omkeren van een gepubliceerde controle naar een concept kan niet ongedaan worden gemaakt. Overweeg de impact op uw actieve reis alvorens te werk te gaan.

## Overzicht van taken {#tasks-tab}

Op het tabblad **[!UICONTROL Tasks]** worden alle herbruikbare taken weergegeven die voor meerdere uitdagingen kunnen worden gebruikt. Taken die u hier maakt, kunnen worden geselecteerd wanneer u een uitdaging maakt of bewerkt.

![](assets/tasks-inventory.png)

Belangrijkste weergegeven informatie:

* **[!UICONTROL Task Name]**: De naam die u aan de taak hebt toegewezen
* **[!UICONTROL Description]**: korte beschrijving van wat de taak vereist
* **[!UICONTROL Task Activity]**: Type activiteit (aankoop, uitgaven)
* **[!UICONTROL SKU]**: In aanmerking komende en/of uitgesloten items
* **[!UICONTROL Used in challenges]**: Aantal uitdagingen die momenteel deze taak gebruiken

Via het tabblad Taken kunt u handelingen uitvoeren op taken:

* **Mening/geef taak** uit: Selecteer de taaknaam om volledige configuratie te bekijken en de taak uit te geven
* **dupliceer een taak**: Selecteer het ![](assets/do-not-localize/Smock_More_18_N.svg) pictogram en kies **[!UICONTROL Duplicate]**
* **schrap een taak**: Selecteer het ![](assets/do-not-localize/Smock_More_18_N.svg) pictogram en kies **[!UICONTROL Delete]**
