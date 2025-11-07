---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud in e-mailsjablonen vergrendelen
description: Leer hoe u inhoud in uw e-mailsjablonen kunt vergrendelen.
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: f64fe1c4-3e30-4b74-80f8-b801a5f1d4c4
source-git-commit: dcbb83e72377838281e1762bb99230e7fe52ab4c
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Inhoud in e-mailsjablonen vergrendelen {#lock-content-email-templates}

>[!CONTEXTUALHELP]
>id="ajo_locking_governance"
>title="Bestuur"
>abstract="Schakel governance in of uit om de inhoud van de sjabloon te vergrendelen door de gehele sjabloon of specifieke structuren en componenten te vergrendelen. Hierdoor kunt u onbedoelde bewerkingen of verwijderingen voorkomen, waardoor u meer controle hebt over de aanpassing van de sjabloon en de efficiëntie en betrouwbaarheid van uw e-mailcampagnes verbetert."

>[!CONTEXTUALHELP]
>id="ajo_locking_mode"
>title="Modus"
>abstract="Selecteer de gewenste vergrendelingsmodus voor de sjabloon. **het sluiten van de Inhoud** staat u toe om specifieke secties van inhoud binnen het malplaatje te sluiten. **las slechts** laat u de volledige inhoud van het malplaatje sluiten, verhinderend om het even welke wijzigingen."

>[!CONTEXTUALHELP]
>id="ajo_locking_content_addition"
>title="Inhoud toevoegen inschakelen"
>abstract="Schakel deze optie in en uit om nader te bepalen hoe gebruikers met de sjabloon kunnen werken. Selecteer **structuur &amp; inhoudsuitbreiding** toestaan om gebruikers toe te staan om structuren tussen bestaande degenen toe te voegen en inhoudscomponenten of fragmenten binnen editable structuren toe te voegen. **staat inhoudoptelling slechts** toe gebruikers om inhoudcomponenten of fragmenten binnen editable structuren toe te voegen zonder structuren toe te voegen of te dupliceren."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_activated"
>title="Bestuur ingeschakeld"
>abstract="De inhoudvergrendeling wordt geactiveerd en voorkomt wijzigingen."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_read_only"
>title="Alleen-lezen"
>abstract="Deze inhoud bevindt zich in de modus Alleen-lezen en kan niet worden gewijzigd."

Met Journey Optimizer kunt u inhoud in e-mailsjablonen vergrendelen door de volledige sjabloon of specifieke structuren en componenten te vergrendelen. Zo voorkomt u onbedoelde bewerkingen of verwijderingen, waardoor u meer controle hebt over de aanpassing van sjablonen en de efficiëntie en betrouwbaarheid van uw e-mailcampagnes verbetert.

>[!IMPORTANT]
>
>Inhoudsvergrendeling is een functie op editorniveau voor auteurs en garandeert niet dat de inhoud onbewerkt blijft wanneer deze wordt geïmporteerd of gemaakt via de API.

Het sluiten van de inhoud kan of op het **structuur** niveau of op het **component** niveau worden toegepast. Hieronder vindt u de belangrijkste beginselen die van toepassing zijn op het niveau van structuur en component wanneer u de inhoud van de sjabloon vergrendelt:

* Wanneer een structuur is vergrendeld:

   * Alle inhoud binnen die structuur is standaard ook vergrendeld.
   * Er kan geen inhoud worden toegevoegd aan de structuur.
   * Standaard kunt u de structuur niet verwijderen. U kunt deze beperking negeren door de optie Verwijderen toestaan in te schakelen.
   * Afzonderlijke inhoudcomponenten binnen de vergrendelde structuur kunnen worden ingesteld als bewerkbaar.

* Wanneer een structuur bewerkbaar is (structuur niet vergrendeld):

   * Afzonderlijke inhoudcomponenten kunnen binnen die structuur worden vergrendeld.
   * Een component kan standaard niet worden verwijderd als deze is vergrendeld of als de optie Alleen bewerkbare inhoud vergrendelen is geselecteerd. U kunt deze beperking negeren door de optie Verwijderen toestaan in te schakelen.

>[!AVAILABILITY]
>
>Gebruikers met machtigingen om inhoudssjablonen te maken, kunnen de vergrendeling van inhoud inschakelen.

➡️ [Ontdek deze functie in video](#video)

## Een e-mailsjabloon vergrendelen {#define}

### Inhoud vergrendelen inschakelen {#enable}

U kunt contentvergrendeling voor een e-mailsjabloon rechtstreeks inschakelen in de e-mailsjabloon van de Designer. Dit is zowel het geval als het gaat om het maken van een nieuwe sjabloon of het bewerken van een bestaande sjabloon. Voer de volgende stappen uit:

1. Open of maak een e-mailsjabloon en open het scherm voor het bewerken van de inhoud in de e-mail Designer.

1. Schakel in het deelvenster **[!UICONTROL Body]** aan de rechterkant de optie **[!UICONTROL Governance]** in.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Mode]** de gewenste vergrendelingsmodus voor de sjabloon:

   * **[!UICONTROL Content locking]**: Vergrendel specifieke gedeelten van inhoud binnen de sjabloon. Standaard worden alle structuren en componenten bewerkbaar. Vervolgens kunt u afzonderlijke elementen selectief vergrendelen.
   * **[!UICONTROL Read only]**: Vergrendel de volledige inhoud van de sjabloon, zodat wijzigingen niet worden doorgevoerd.

   ![](assets/template-lock-enable.png)

1. Als u de modus **[!UICONTROL Content locking]** hebt geselecteerd, kunt u nader bepalen hoe gebruikers kunnen communiceren met de sjabloon. Schakel de optie **[!UICONTROL Enable content addition]** in en kies een van de volgende opties:

   * **[!UICONTROL Allow structure & content addition]**: gebruikers kunnen structuren tussen bestaande structuren toevoegen en inhoudscomponenten of fragmenten binnen bewerkbare structuren toevoegen.

   * **[!UICONTROL Allow content addition only]**: gebruikers kunnen inhoudscomponenten of fragmenten toevoegen binnen bewerkbare structuren, maar ze kunnen geen structuren toevoegen of dupliceren.

1. Nadat u de vergrendelingsmodus hebt geselecteerd, kunt u definiëren welke structuren en/of componenten u wilt vergrendelen als u de modus **[!UICONTROL Content locking]** hebt geselecteerd:

   * [Leer hoe u structuren kunt vergrendelen](#lock-structures)
   * [Leer hoe u componenten kunt vergrendelen](#lock-components)

   Als u de modus **[!UICONTROL Read only]** kiest, voert u de voltooide bewerking uit en slaat u de sjabloon op de gebruikelijke manier op.

U kunt de instellingen van **[!UICONTROL Governance]** op elk gewenst moment tijdens het ontwerpen van de sjabloon aanpassen door de hoofdtekst van de sjabloon te selecteren. Klik hiertoe op de koppeling **[!UICONTROL Body]** in de navigatieregel die zich boven aan het rechterzijvenster bevindt.

![](assets/template-lock-body.png)

### Vergrendelingsstructuren {#lock-structures}

>[!CONTEXTUALHELP]
>id="ajo_locking_structure"
>title="Inhoud vergrendelen in structuur"
>abstract="Om de structuur in het malplaatje te sluiten, selecteer **Vergrendelde** van het **type van het Slot** drop-down. Standaard kunnen gebruikers vergrendelde structuren niet verwijderen. U kunt deze beperking negeren door de optie **[!UICONTROL Allow delete]** in te schakelen."

Een structuur in de sjabloon vergrendelen:

1. Selecteer de structuur die u wilt vergrendelen.

1. Kies **[!UICONTROL Lock type]** in de vervolgkeuzelijst **[!UICONTROL Locked]** .

   ![](assets/template-lock-structure.png)

   >[!NOTE]
   >
   >Standaard kunnen gebruikers vergrendelde structuren niet verwijderen. U kunt deze beperking negeren door de optie **[!UICONTROL Allow delete]** in te schakelen.

Nadat een structuur is vergrendeld, kunnen er geen verdere inhoudcomponenten of -fragmenten in worden gedupliceerd of toegevoegd. Alle componenten in een vergrendelde structuur zijn standaard ook vergrendeld. Een component bewerkbaar maken binnen een vergrendelde structuur:

1. Selecteer de component die u wilt ontgrendelen.

1. Schakel de optie **[!UICONTROL Use specific locking]** in.

1. Kies **[!UICONTROL Lock type]** in de vervolgkeuzelijst **[!UICONTROL Editable]** . Selecteer **[!UICONTROL Editable content only]** als u het bewerken van inhoud tijdens het vergrendelen van stijlen wilt toestaan. [&#x200B; leer hoe te om componenten &#x200B;](#lock-components) te sluiten

   ![](assets/template-lock-editable-component.png)

### Componenten vergrendelen {#lock-components}

>[!CONTEXTUALHELP]
>id="ajo_locking_component"
>title="Specifieke vergrendeling in onderdeel gebruiken"
>abstract="Om de component in het malplaatje te sluiten, knevel op de **specifieke vergrendelings** optie van het Gebruik. Van de **[!UICONTROL Lock type]** drop-down lijst, selecteer uw aangewezen vergrendelingsoptie: **Bewerkbare inhoudsslot slechts** staat u toe om de stijlen van de component te sluiten maar staat inhoud het uitgeven toe, terwijl **Vergrendelde** zowel de inhoud als de stijlen van de component volledig sluit."

Een specifieke component in een structuur vergrendelen:

1. Selecteer de component en schakel de optie **[!UICONTROL Use specific locking]** in het rechterdeelvenster in.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Lock type]** de gewenste vergrendelingsoptie:

   ![](assets/template-lock-component.png)

   * **[!UICONTROL Editable content only]**: vergrendel de stijlen van de component, maar sta het bewerken van inhoud toe.
   * **[!UICONTROL Locked]**: vergrendel zowel de inhoud als de stijlen van de component volledig.

   >[!NOTE]
   >
   >Met het vergrendelingstype **[!UICONTROL Editable]** kunnen gebruikers een component bewerken, zelfs binnen een vergrendelde structuur. [&#x200B; leer hoe te om structuren &#x200B;](#lock-structures) te sluiten

1. Standaard kunnen gebruikers vergrendelde componenten niet verwijderen. U kunt verwijdering inschakelen door de optie **[!UICONTROL Allow delete]** te activeren.

### Vergrendelde inhoud identificeren {#identify}

Als u vergrendelde structuren en componenten in de sjabloon gemakkelijk wilt identificeren, gebruikt u de **[!UICONTROL Navigation tree]** in het menu aan de linkerkant. Dit menu biedt een visueel overzicht van alle sjabloonelementen, waarbij vergrendelde items worden gemarkeerd met een vergrendelingspictogram en bewerkbare items met een potloodpictogram.

In het onderstaande voorbeeld wordt governance ingeschakeld voor het sjabloonlichaam. *Structuur 2* is gesloten met *Component 1* editable, terwijl *Structuur 3* volledig gesloten is.

![](assets/template-lock-navigation.png)

## Sjablonen gebruiken met vergrendelde inhoud {#use}

>[!CONTEXTUALHELP]
>id="ajo_email_editable_areas"
>title="Bewerkbare gebieden markeren"
>abstract="Afhankelijk van het type vergrendeling dat op de sjabloon wordt toegepast, kunt u verschillende handelingen uitvoeren op de structuren en componenten van de sjabloon. Schakel de optie **[!UICONTROL Highlight editable areas]** in als u snel alle bewerkbare gebieden in de sjabloon wilt identificeren."

Als u een sjabloon met vergrendelde inhoud gebruikt, wordt er een bericht weergegeven in het rechterdeelvenster.

Afhankelijk van het type vergrendeling dat op de sjabloon wordt toegepast, kunt u verschillende handelingen uitvoeren op de structuren en componenten van de sjabloon. Schakel de optie **[!UICONTROL Highlight editable areas]** in als u snel alle bewerkbare gebieden in de sjabloon wilt identificeren.

In de onderstaande sjabloon zijn bijvoorbeeld alle gebieden bewerkbaar, behalve de bovenste afbeelding, die vergrendeld is. Dit betekent dat u de afbeelding niet kunt bewerken of verwijderen.

![](assets/template-lock-highlight.png)

In de volgende secties vindt u gedetailleerde informatie over de verschillende typen vergrendeling die kunnen worden toegepast:

* [Vergrendelingsstructuren](#lock-structures)
* [Componenten vergrendelen](#lock-components)

Hier volgen enkele voorbeelden van e-mailedities en de bijbehorende configuraties voor vergrendeling van inhoud die zijn ingesteld:

| Type inhoudvergrendeling | Sjabloonconfiguratie | E-maileditie |
| ------- | ------- | ------- |
| Sjabloon voor alleen-lezen inhoud | ![](assets/locking-sample-read-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-read-only.png){zoomable="yes"} |
| Volledige inhoud kan worden bewerkt, maar gebruikers kunnen geen structuur of component toevoegen | ![](assets/locking-sample-no-addition-conf.png){zoomable="yes"} | ![](assets/locking-sample-no-addition.png){zoomable="yes"} |
| Vergrendelde structuur die niet kan worden verwijderd | ![](assets/locking-sample-structure-locked-conf.png){zoomable="yes"} | ![](assets/locking-sample-structure-locked.png){zoomable="yes"} |
| Component met vergrendelde stijlen die niet kunnen worden verwijderd. Gebruikers kunnen alleen de inhoud wijzigen. | ![](assets/locking-sample-content-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-content-only.png){zoomable="yes"} |
| Bewerkbare component binnen een vergrendelde structuur. | ![](assets/locking-sample-editable-component-conf.png){zoomable="yes"} | ![](assets/locking-sample-editable-component.png){zoomable="yes"} |

## Hoe kan ik-video {#video}

Leer hoe u inhoud in e-mailsjablonen kunt vergrendelen.

>[!VIDEO](https://video.tv.adobe.com/v/3451591?quality=12)
