---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud testen met behulp van voorbeeldinvoergegevens
description: Leer hoe u een voorbeeld van e-mailinhoud bekijkt en proefdrukken verzendt met behulp van voorbeeldinvoer.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 854a1398e1619f75c201b79e957088a1b6fef0d2
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---


# Inhoud testen met behulp van voorbeeldinvoergegevens {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuleren met behulp van voorbeeldinvoer"
>abstract="In dit scherm kunt u verschillende varianten van uw e-mailinhoud testen door waarden op te geven voor verpersoonlijkingsvelden via een CSV-sjabloon (download CSV) of door de waarden handmatig in te voeren.

>[!AVAILABILITY]
>
>Deze functies zijn momenteel alleen beschikbaar als bètaversie voor geselecteerde gebruikers.

Met Reisoptimalisator kunt u verschillende varianten van uw e-mailinhoud testen door deze voor te vertonen en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die zijn geüpload uit een CSV-bestand of handmatig zijn toegevoegd. Alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor uw tests om meerdere varianten te maken.

Klik op de knop **[!UICONTROL Simulate content]** en kies **[!UICONTROL Simulate with CSV(Beta)]** voor toegang tot deze ervaring.

![](assets/simulate-sample.png)

De belangrijkste stappen om uw inhoud te testen zijn als volgt:

1. Voeg maximaal 30 varianten toe met voorbeeldinvoergegevens door een CSV-bestand te uploaden of door gegevens handmatig toe te voegen. [ Leer hoe te om variabelen toe te voegen ](#profiles)
1. Controleer de voorvertoning van de inhoud met de verschillende varianten. [ Leer hoe te om uw inhoud ](#preview) voor te vertonen
1. U kunt maximaal 10 proefdrukken naar e-mailadressen verzenden met de verschillende varianten. [ Leer hoe te om proefdrukken ](#proofs) te verzenden


## Afbeeldingen en beperkingen {#limitations}

Overweeg de volgende instructies en voorwaarden voordat u begint met het testen van de inhoud met behulp van voorbeeldinvoergegevens.

* Het testen met behulp van voorbeeldinvoergegevens is nu alleen beschikbaar voor het e-mailkanaal. U hebt geen toegang tot deze ervaring via de knop Inhoud simuleren in de Designer-e-mail.
* De volgende functies zijn niet beschikbaar in de huidige ervaring: Inbox rendering, spamrapporten, meertalige content en content experiment. Als u deze functies wilt gebruiken, selecteert u de knop **[!UICONTROL Simulate content]** in de inhoud om toegang te krijgen tot de vorige gebruikersinterface.
* Momenteel worden alleen profielkenmerken ondersteund. Als contextafhankelijke kenmerken in uw inhoud worden gebruikt voor personalisatie, kunt u de inhoud niet testen met deze kenmerken.
* Alleen de volgende gegevenstypen worden ondersteund bij het invoeren van gegevens voor de varianten: getal (geheel getal en decimaal), tekenreeks, boolean en datumtype. Voor elk ander gegevenstype wordt een fout weergegeven.


niet van acrite

## Varianten toevoegen {#profiles}

U kunt maximaal 30 varianten toevoegen om de inhoud te testen met behulp van een CSV-bestand of handmatig:

* Als u voorbeeldinvoergegevens uit een CSV-bestand wilt uploaden, klikt u op de koppeling **[!UICONTROL download CSV]** om een CSV-bestandssjabloon op te halen. Deze sjablonen bevatten een kolom voor elk profielkenmerk dat in uw inhoud wordt gebruikt voor personalisatie.

  Vul het CSV-bestand in en klik op **[!UICONTROL Upload Input data]** om het te laden om de inhoud te testen.

* Als u handmatig een variant wilt toevoegen, klikt u op de knop **[!UICONTROL Create sample input]** en vult u de gegevens van de voorbeeldinvoer voor de variant in. Er wordt één veld weergegeven voor elk profielkenmerk dat in uw inhoud wordt gebruikt voor personalisatie.

  ![](assets/simulate-custom-add.png)

Nadat de profielen zijn geselecteerd, wordt aan de linkerkant van het scherm één vak weergegeven voor elke variant. U kunt deze profielen gebruiken om een voorvertoning van uw inhoud weer te geven en proefdrukken te verzenden.

>[!NOTE]
>
>De toegevoegde varianten dienen alleen als testdoeleinden voor de huidige inhoud. De bestanden worden niet opgeslagen in Adobe Experience Platform, maar in uw gebruikersbrowsersessie. Dit houdt in dat ze niet worden weergegeven wanneer ze worden afgemeld of dat ze vanaf een ander apparaat worden gebruikt.

## Een voorvertoning van de inhoudvarianten weergeven {#preview}

Als u een voorvertoning van de inhoud wilt weergeven met een van de varianten, selecteert u het desbetreffende vak om de voorvertoning van de inhoud in de rechtersectie bij te werken met de informatie die u voor deze variant hebt ingevoerd.

U kunt een variant op elk gewenst moment verwijderen met de ellipknop in de rechterbovenhoek en door **[!UICONTROL Remove]** te selecteren. Als u informatie voor een variant wilt bewerken, klikt u op de knop voor weglatingsteken en selecteert u **[!UICONTROL Edit]** .

![](assets/simulate-custom-boxes.png)

## Proefdrukken verzenden {#proofs}

Met Journey Optimizer kunt u proefdrukken naar e-mailadressen verzenden en tegelijkertijd een of meerdere varianten nabootsen die u in het simulatiescherm hebt toegevoegd. De stappen zijn als volgt:

1. Controleer of er varianten zijn toegevoegd om de inhoud te testen en klik op de knop **[!UICONTROL Send Proof]** .

1. Voer in het veld **[!UICONTROL Recipients]** het e-mailadres in waarnaar u de proefdruk wilt verzenden en klik vervolgens op **[!UICONTROL Add]** . Herhaal de bewerking om de proefdruk naar extra e-mailadressen te verzenden. U kunt maximaal tien proefontvangers toevoegen.

1. Selecteer in het onderste gedeelte van het scherm de variant die u wilt gebruiken in de proefdruk. U kunt meerdere varianten selecteren. In dat geval bevat het e-mailbericht evenveel proefdrukken als geselecteerde varianten.

   Selecteer de koppeling **[!UICONTROL View profile details]** voor meer informatie over een variant. Op deze manier kunt u de informatie die u in het vorige scherm hebt ingevoerd, weergeven voor de verschillende varianten.

   ![](assets/simulate-custom-proofs.png)

1. Klik op de knop **[!UICONTROL Send Proof]** om de proefdruk te verzenden.

1. Klik op de knop **[!UICONTROL View proofs]** in het scherm Inhoud simuleren om het verzenden van de proefdrukken bij te houden.

![](assets/simulate-custom-sent-proofs.png)
