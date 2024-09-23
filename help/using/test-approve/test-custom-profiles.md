---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud testen met voorbeeldprofielen
description: Leer hoe u een voorbeeld van e-mailinhoud bekijkt en proefdrukken verzendt met behulp van voorbeeldprofielen.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Inhoud testen met voorbeeldprofielen {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuleren met voorbeeldprofielen"
>abstract="In dit scherm kunt u e-mailinhoud voorvertonen en proefdrukken verzenden terwijl u voorbeeldprofielen imiteert die u vanuit een CSV-bestand kunt uploaden of handmatig vanuit dit scherm kunt toevoegen."


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>Deze functies zijn momenteel alleen beschikbaar als bètaversie voor geselecteerde gebruikers.

Met Reis optimaliseren kunt u e-mailinhoud voorvertonen en testen met voorbeeldprofielen die u kunt uploaden vanuit een CSV-bestand of u kunt deze inhoud handmatig toevoegen wanneer u de inhoud simuleert. Met deze functie kunt u voorbeeldprofielen selecteren voor een voorvertoning van uw inhoud en proefdrukken. Alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie, worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor uw tests.

Klik op de knop **[!UICONTROL Simulate content]** en kies **[!UICONTROL Simulate with CSV(Beta)]** voor toegang tot deze ervaring.

![](assets/simulate-sample.png)


De belangrijkste stappen om uw inhoud te testen zijn als volgt:

1. Voeg maximaal 30 voorbeeldprofielen toe door een CSV-bestand te uploaden of door deze handmatig toe te voegen. [ leer hoe te om steekproefprofielen toe te voegen ](#profiles)
1. Controleer de voorvertoning van uw inhoud met de toegevoegde profielen. [ Leer hoe te om uw inhoud ](#preview) voor te vertonen
1. U kunt maximaal 10 proefdrukken naar de e-mailadressen verzenden en tegelijkertijd de gewenste voorbeeldprofielen weergeven. [ Leer hoe te om proefdrukken ](#proofs) te verzenden


## Afbeeldingen en beperkingen {#limitations}

Overweeg de volgende instructies en voorwaarden voordat u begint met het testen van de inhoud met gebruik van voorbeeldprofielen.

* Het testen met voorbeeldprofielen is nu alleen beschikbaar in campagnes en voor het e-mailkanaal.
* De volgende functies zijn niet beschikbaar in de huidige ervaring: Inbox rendering, spamrapporten, meertalige content en content experiment. Als u deze functies wilt gebruiken, selecteert u de knop **[!UICONTROL Simulate content]** in de inhoud om toegang te krijgen tot de vorige gebruikersinterface.
* Momenteel worden alleen profielkenmerken ondersteund. Als contextafhankelijke kenmerken in uw inhoud worden gebruikt voor personalisatie, kunt u de inhoud niet testen met deze kenmerken.
* Alleen de volgende gegevenstypen worden ondersteund bij het invoeren van gegevens voor uw voorbeeldprofielen: getal (geheel getal en decimaal), tekenreeks, Booleaanse waarde en datumtype. Voor elk ander gegevenstype wordt een fout weergegeven.

## Voorbeeldprofielen toevoegen {#profiles}

U kunt maximaal 30 voorbeeldprofielen toevoegen om uw inhoud te testen met een CSV-bestand of handmatig:

* Als u profielen wilt uploaden vanuit een CSV-bestand, klikt u op de koppeling **[!UICONTROL Download template]** om een CSV-bestandssjabloon op te halen. Deze sjablonen bevatten een kolom voor elk profielkenmerk dat in uw inhoud wordt gebruikt voor personalisatie.

  Vul het CSV-bestand in en klik op **[!UICONTROL Upload sample profiles]** om het te laden om de inhoud te testen.

* Als u handmatig een profiel wilt toevoegen, klikt u op de knop **[!UICONTROL Create sample profile]** en vult u de gegevens voor het profiel in. Er wordt één veld weergegeven voor elk profielkenmerk dat in uw inhoud wordt gebruikt voor personalisatie.

  ![](assets/simulate-custom-add.png)

Nadat de profielen zijn geselecteerd, verschijnt er één vak voor elk profiel aan de linkerkant van het scherm. U kunt deze profielen gebruiken om een voorvertoning van uw inhoud weer te geven en proefdrukken te verzenden.

>[!NOTE]
>
>De toegevoegde voorbeeldprofielen dienen alleen als testdoeleinden voor uw huidige inhoud. De bestanden worden niet opgeslagen in Adobe Experience Platform, maar in uw gebruikersbrowsersessie. Dit houdt in dat ze niet worden weergegeven wanneer ze worden afgemeld of dat ze vanaf een ander apparaat worden gebruikt.

## Inhoud voorvertonen met voorbeeldprofielen {#preview}

Als u een voorvertoning van de inhoud wilt weergeven met een van de profielen, schakelt u het desbetreffende vak in om de voorvertoning van de inhoud in de rechtersectie bij te werken met de informatie die u voor dit profiel hebt ingevoerd.

U kunt een vak op elk gewenst moment verwijderen met de ellipknop in de rechterbovenhoek en door **[!UICONTROL Remove]** te selecteren. Als u informatie voor een profiel wilt bewerken, klikt u op de knop voor weglatingsteken en selecteert u **[!UICONTROL Edit]** .

![](assets/simulate-custom-boxes.png)

## Proefdrukken verzenden {#proofs}

Met Journey Optimizer kunt u proefdrukken naar e-mailadressen verzenden en tegelijkertijd een of meerdere voorbeeldprofielen nabootsen die u in het simulatiescherm hebt toegevoegd. De stappen zijn als volgt:

1. Controleer of er voorbeeldprofielen zijn toegevoegd om de inhoud te testen en klik op de knop **[!UICONTROL Send Proof]** .

1. Voer in het veld **[!UICONTROL Recipients]** het e-mailadres in waarnaar u de proefdruk wilt verzenden en klik vervolgens op **[!UICONTROL Add]** . Herhaal de bewerking om de proefdruk naar extra e-mailadressen te verzenden. U kunt maximaal tien proefontvangers toevoegen.

1. Selecteer in het onderste gedeelte van het scherm de voorbeeldprofielen die u wilt weergeven in de proefdruk. U kunt meerdere profielen selecteren. In dat geval bevat de e-mail evenveel proefdrukken als geselecteerde profielen.

   Selecteer de koppeling **[!UICONTROL View profile details]** voor meer informatie over een profiel. Op deze manier kunt u de informatie die u in het vorige scherm hebt ingevoerd, weergeven voor de verschillende profielkenmerken.

   ![](assets/simulate-custom-proofs.png)

1. Klik op de knop **[!UICONTROL Send Proof]** om de proefdruk te verzenden.

U kunt het verzenden op elk gewenst moment volgen door op de knop **[!UICONTROL View proofs]** in het scherm met gesimuleerde inhoud te klikken.

![](assets/simulate-custom-sent-proofs.png)
